<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Babe <3</title>
  <script src="https://unpkg.com/peerjs@1.5.2/dist/peerjs.min.js"></script>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: -apple-system, system-ui, sans-serif; background: #0f0f12; color: white; }
    #root { min-height: 100vh; display: flex; flex-direction: column; align-items: center; padding: 24px 16px; }
    .title { color: #ff4d6d; font-size: 22px; font-weight: 600; margin-bottom: 4px; }
    .sub { color: #ffb3c1; font-size: 13px; margin-bottom: 20px; text-align: center; opacity: 0.8; }
    .card { background: #1a1a22; border-radius: 14px; padding: 22px; width: 100%; max-width: 440px; border: 0.5px solid #2e2e3e; box-shadow: 0 10px 25px rgba(0,0,0,0.5); }
    .inp { width: 100%; padding: 12px; border-radius: 8px; border: 0.5px solid #3a3a4e; background: #0f0f18; color: white; font-size: 14px; margin-bottom: 10px; outline: none; }
    .inp:focus { border-color: #ff4d6d; }
    .btn { width: 100%; padding: 12px; border-radius: 8px; border: none; color: white; cursor: pointer; font-size: 14px; font-weight: 600; margin-bottom: 8px; }
    .btn-red { background: #c9184a; }
    .btn-dark { background: #2a2a3a; }
    .btn-score { background: #7209b7; width: auto; padding: 8px 16px; font-size: 13px; margin-bottom: 0; }
    .code-box { font-size: 32px; font-weight: 700; letter-spacing: 6px; color: #ff4d6d; text-align: center; margin: 16px 0; background: #0f0f18; padding: 16px; border-radius: 10px; border: 1px dashed #ff4d6d; }
    .turn-bar { border-radius: 8px; padding: 10px; font-size: 13px; margin-bottom: 12px; text-align: center; font-weight: 600; }
    .q-box { background: #0f0f18; border-radius: 10px; padding: 16px; color: #ffb3c1; font-size: 15px; min-height: 60px; margin-bottom: 12px; border: 0.5px solid #2e2e3e; text-align: center; display: flex; align-items: center; justify-content: center; line-height: 1.4; }
    .cat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 12px; }
    .cat-btn { padding: 10px; border-radius: 8px; border: none; color: white; cursor: pointer; font-size: 12px; font-weight: 600; }
    .chat-box { border: 0.5px solid #2e2e3e; border-radius: 10px; height: 160px; overflow-y: auto; padding: 10px; margin-bottom: 10px; background: #0f0f18; display: flex; flex-direction: column; }
    .msg { font-size: 13px; margin-bottom: 8px; padding: 8px 12px; border-radius: 12px; max-width: 85%; line-height: 1.4; }
    .msg-me { background: #ff4d6d; color: white; align-self: flex-end; border-bottom-right-radius: 2px; }
    .msg-other { background: #2e2e3e; color: #ffb3c1; align-self: flex-start; border-bottom-left-radius: 2px; }
    .msg-info { background: transparent; color: #888; align-self: center; font-style: italic; font-size: 11px; text-align: center; margin: 5px 0; }
    .msg b { display: block; font-size: 10px; opacity: 0.7; margin-bottom: 2px; text-transform: uppercase; }
    .score-row { display: flex; align-items: center; gap: 8px; margin-top: 10px; background: #0f0f18; padding: 8px; border-radius: 10px; border: 0.5px solid #2e2e3e; }
    .score-label { font-size: 13px; color: #ff4d6d; min-width: 40px; font-weight: bold; }
    input[type=range] { flex: 1; accent-color: #ff4d6d; cursor: pointer; }
  </style>
</head>
<body>

<div id="root">
  <div class="title">BABE <3</div>
  <div class="sub">Taux de satisfaction 💕</div>
  <div id="app-card" class="card"></div>
</div>

<script>
const Q = {
  romantic: ["Quel moment avec moi t'a rendu le plus heureux ?", "Qu'est-ce que tu aimes le plus chez moi ?", "Quel souvenir veux-tu recréer avec moi ?", "Quelle vie voudrais-tu mener avec moi dans 5 ans ?", "Quelle chanson te fait penser à moi ?", "Quel geste de ma part t'a le plus touché ?", "Si tu devais décrire notre relation en un mot ?", "Quel est le premier détail physique que tu as aimé chez moi ?", "C'est quoi pour toi une soirée parfaite avec moi ?", "Quelle est la chose la plus mignonne que j'ai faite pour toi ?", "Si on partait demain, on irait où tous les deux ?", "Est-ce qu'il y a une odeur ou un objet qui te fait direct penser à moi ?", "Quel est ton moment préféré de la journée quand on est ensemble ?"],
  tease: ["Quel truc que je fais te rend fou/folle sans que je le sache ?", "À quelles situations tu penses à moi ?", "Qu'est-ce qui te ferait craquer en 10 secondes ?", "Quand es ce que tu me regarde et que je ne le sais pas ?", "Qu'est-ce que je fais qui te fait sourire bêtement ?", "Quel surnom me donnerais-tu si tu pouvais ?", "Qu'est-ce que j'ai dit un jour que tu n'as pas oublié ?"],
  spicy: ["Qu'est-ce qui te donne envie de te rapprocher de moi ?", "Quel détail chez moi pourrait m'exciter le plus ?", "Qu'est-ce que tu aimerais que je fasse là maintenant ?", "Où voudrais-tu aller avec moi pour une nuit ?", "Qu'est-ce qui te ferait penser à moi toute la nuit ?", "Si on avait une soirée sans limites, tu proposerais quoi ?", "Donne moi un truc que tu voudrais essayer mais que n'a jamais osé dire "],
  dare: ["Envoie-moi une photo de la partie de ton corps que je préfère.", "Envoie-moi une vidéo qui me donnerait très envie de toi.", "Prends une photo sexy là tout de suite.", "Prends une photo de tes lèvres et envoie-la.", "Envoie une photo de toi dans ton miroir.","Prends une photo sexy la plus osée que tu n'ai jamais faite","Quelle genre de photos ou vidéos tu prefere que je t'envoi", "Envoie-moi une photo de la partie de ton corps que TU préfère." ]
};

let state = { screen: 'home', myName: '', joinCode: '', roomCode: '', playerNum: null, turn: 1, currentQ: 'Choisis une catégorie 👇', chat: [], scoreVal: 50 };
let peer = null, conn = null;

function render() {
  const card = document.getElementById('app-card');
  if (state.screen === 'home') {
    card.innerHTML = `
      <input class="inp" id="n" placeholder="Ton prénom" value="${state.myName}">
      <button class="btn btn-red" onclick="create()">✨ Créer une partie</button>
      <div style="text-align:center;color:#444;font-size:12px;margin:10px">OU</div>
      <input class="inp" id="c" placeholder="Code du partenaire" value="${state.joinCode}">
      <button class="btn btn-dark" onclick="join()">🔗 Rejoindre</button>`;
    document.getElementById('n').oninput = e => state.myName = e.target.value;
    document.getElementById('c').oninput = e => state.joinCode = e.target.value.toUpperCase();
  } else if (state.screen === 'waiting') {
    card.innerHTML = `<div class="sub">Donne ce code à ton partenaire :</div><div class="code-box">${state.roomCode}</div><div class="sub">En attente...</div>`;
  } else {
    const isMyTurn = state.playerNum === state.turn;
    card.innerHTML = `
      <div class="turn-bar" style="background:${isMyTurn?'#1a3a22':'#1a1a2e'};color:${isMyTurn?'#4ade80':'#7dd3fc'}">${isMyTurn?'🎯 C\'est ton tour !':'⏳ Son tour...'}</div>
      <div class="q-box">${state.currentQ}</div>
      <div class="cat-grid">
        <button class="cat-btn" style="background:#c9184a" onclick="pick('romantic')">❤️ Romantique</button>
        <button class="cat-btn" style="background:#7209b7" onclick="pick('tease')">😏 Teasing</button>
        <button class="cat-btn" style="background:#e07a00" onclick="pick('spicy')">🔥 Spicy</button>
        <button class="cat-btn" style="background:#2b9348" onclick="pick('dare')">🎯 Défi</button>
      </div>
      <div class="chat-box" id="chat">${state.chat.map(m=>`<div class="msg ${m.type==='s'?'msg-info':(m.p==state.playerNum?'msg-me':'msg-other')}">${m.type==='c'?'<b>'+m.n+'</b>':''} ${m.t}</div>`).join('')}</div>
      <div style="display:flex;gap:5px;margin-bottom:10px"><input class="inp" id="mi" placeholder="Message..." style="margin:0"><button class="btn btn-red" onclick="send()" style="width:70px;margin:0">OK</button></div>
      <div class="score-row">
        <span class="score-label">${state.scoreVal}%</span>
        <input type="range" min="0" max="100" value="${state.scoreVal}" id="sl">
        <button class="btn btn-score" onclick="sendScore()">⭐ Score</button>
      </div>`;
    const c = document.getElementById('chat'); if(c) c.scrollTop = c.scrollHeight;
    document.getElementById('mi').onkeydown = e => { if(e.key==='Enter') send(); };
    document.getElementById('sl').oninput = e => { state.scoreVal = e.target.value; document.querySelector('.score-label').innerText = e.target.value + '%'; };
  }
}

const prefix = "LOVE-STABLE-V5-";

function create() {
  if(!state.myName) return alert("Ton prénom ?");
  state.roomCode = Math.random().toString(36).substring(2,6).toUpperCase();
  peer = new Peer(prefix + state.roomCode);
  peer.on('open', () => { state.screen = 'waiting'; render(); });
  peer.on('connection', c => { conn = c; state.playerNum = 1; setup(); });
}

function join() {
  if(!state.myName || !state.joinCode) return alert("Nom + Code ?");
  peer = new Peer();
  peer.on('open', () => {
    conn = peer.connect(prefix + state.joinCode);
    state.playerNum = 2;
    setup();
  });
}

function setup() {
  conn.on('open', () => {
    state.screen = 'game'; render();
    conn.on('data', d => {
      if(d.type==='c' || d.type==='s') { state.chat.push(d); if(d.type==='c') state.turn = state.playerNum; render(); }
      if(d.type==='q') { state.currentQ = d.q; render(); }
    });
  });
}

function send() {
  const i = document.getElementById('mi'); if(!i.value) return;
  const m = { type:'c', n:state.myName, t:i.value, p:state.playerNum };
  conn.send(m); state.chat.push(m); state.turn = (state.playerNum===1?2:1); i.value=''; render();
}

function sendScore() {
  const m = { type:'s', t: `⭐ ${state.myName} score : ${state.scoreVal}%`, p:state.playerNum };
  conn.send(m); state.chat.push(m); render();
}

function pick(cat) {
  const qList = Q[cat];
  const q = qList[Math.floor(Math.random()*qList.length)];
  state.currentQ = q; 
  if(conn) conn.send({type:'q', q:q}); 
  render();
}

render();
</script>
</body>
</html>
