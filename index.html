<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Babe <3</title>
  <script src="https://unpkg.com/peerjs@1.5.2/dist/peerjs.min.js"></script>
  <style>
    :root {
      --bg: #0a0a0c;
      --card-bg: rgba(26, 26, 34, 0.85);
      --primary: #ff4d6d;
      --secondary: #c9184a;
      --accent: #ffb3c1;
      --glass: rgba(255, 255, 255, 0.03);
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }
    
    body { 
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; 
      background: var(--bg);
      background-image: radial-gradient(circle at 50% -20%, #2e1018 0%, #0a0a0c 60%);
      color: white; 
      min-height: 100vh;
      overflow-x: hidden;
    }

    /* Animation du fond */
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; width: 100%; height: 100%;
      background: linear-gradient(45deg, rgba(255, 77, 109, 0.05) 0%, transparent 100%);
      pointer-events: none;
      z-index: -1;
    }

    #root { min-height: 100vh; display: flex; flex-direction: column; align-items: center; padding: 32px 16px; }

    .title { 
      color: var(--primary); 
      font-size: 28px; 
      font-weight: 800; 
      letter-spacing: 2px;
      margin-bottom: 4px;
      text-shadow: 0 0 15px rgba(255, 77, 109, 0.4);
    }

    .sub { color: var(--accent); font-size: 14px; margin-bottom: 24px; text-align: center; opacity: 0.7; font-weight: 300; }

    .card { 
      background: var(--card-bg); 
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border-radius: 24px; 
      padding: 24px; 
      width: 100%; 
      max-width: 440px; 
      border: 1px solid rgba(255, 255, 255, 0.08); 
      box-shadow: 0 20px 40px rgba(0,0,0,0.6);
    }

    .inp { 
      width: 100%; padding: 14px; border-radius: 12px; 
      border: 1px solid rgba(255, 255, 255, 0.1); 
      background: rgba(0, 0, 0, 0.3); 
      color: white; font-size: 15px; margin-bottom: 12px; outline: none; 
      transition: all 0.3s ease;
    }

    .inp:focus { border-color: var(--primary); background: rgba(0, 0, 0, 0.5); }

    .btn { 
      width: 100%; padding: 14px; border-radius: 12px; border: none; 
      color: white; cursor: pointer; font-size: 15px; font-weight: 700; 
      margin-bottom: 10px; transition: all 0.2s ease;
      display: flex; align-items: center; justify-content: center; gap: 8px;
    }

    .btn:active { transform: scale(0.98); }
    .btn-red { background: linear-gradient(135deg, var(--primary), var(--secondary)); }
    .btn-red:hover { box-shadow: 0 0 15px rgba(255, 77, 109, 0.4); }
    .btn-dark { background: rgba(255, 255, 255, 0.08); }
    .btn-dark:hover { background: rgba(255, 255, 255, 0.12); }
    
    .btn-score { 
      background: #7209b7; width: auto; padding: 10px 18px; 
      font-size: 13px; margin-bottom: 0; border-radius: 10px;
    }

    .code-box { 
      font-size: 36px; font-weight: 800; letter-spacing: 8px; 
      color: var(--primary); text-align: center; margin: 20px 0; 
      background: rgba(0,0,0,0.4); padding: 20px; border-radius: 16px; 
      border: 1px dashed rgba(255, 77, 109, 0.5); 
    }

    .turn-bar { 
      border-radius: 12px; padding: 12px; font-size: 14px; 
      margin-bottom: 16px; text-align: center; font-weight: 700;
      transition: all 0.4s ease;
    }

    .q-box { 
      background: rgba(255, 255, 255, 0.03); 
      border-radius: 16px; padding: 20px; color: var(--accent); 
      font-size: 16px; min-height: 80px; margin-bottom: 16px; 
      border: 1px solid rgba(255, 255, 255, 0.05); 
      text-align: center; display: flex; align-items: center; 
      justify-content: center; line-height: 1.5; font-style: italic;
    }

    .cat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 16px; }
    
    .cat-btn { 
      padding: 12px; border-radius: 12px; border: none; color: white; 
      cursor: pointer; font-size: 13px; font-weight: 700;
      transition: transform 0.2s ease;
    }
    .cat-btn:hover { transform: translateY(-2px); filter: brightness(1.1); }

    .chat-box { 
      border: 1px solid rgba(255, 255, 255, 0.05); border-radius: 16px; 
      height: 180px; overflow-y: auto; padding: 12px; margin-bottom: 12px; 
      background: rgba(0, 0, 0, 0.2); display: flex; flex-direction: column; 
    }

    .msg { 
      font-size: 13.5px; margin-bottom: 10px; padding: 10px 14px; 
      border-radius: 18px; max-width: 85%; line-height: 1.4;
      animation: fadeIn 0.3s ease;
    }
    @keyframes fadeIn { from { opacity: 0; transform: translateY(5px); } to { opacity: 1; transform: translateY(0); } }

    .msg-me { background: var(--primary); color: white; align-self: flex-end; border-bottom-right-radius: 4px; }
    .msg-other { background: rgba(255, 255, 255, 0.1); color: var(--accent); align-self: flex-start; border-bottom-left-radius: 4px; }
    .msg-info { background: transparent; color: #888; align-self: center; font-style: italic; font-size: 11px; margin: 8px 0; }
    .msg b { display: block; font-size: 10px; opacity: 0.8; margin-bottom: 3px; }

    .score-row { 
      display: flex; align-items: center; gap: 12px; margin-top: 10px; 
      background: rgba(0,0,0,0.3); padding: 12px; border-radius: 16px; 
      border: 1px solid rgba(255, 255, 255, 0.05); 
    }
    .score-label { font-size: 15px; color: var(--primary); min-width: 45px; font-weight: 800; }
    
    input[type=range] { 
      flex: 1; accent-color: var(--primary); cursor: pointer; height: 6px; 
      background: rgba(255,255,255,0.1); border-radius: 5px; appearance: none;
    }

    /* Scrollbar minimaliste */
    .chat-box::-webkit-scrollbar { width: 4px; }
    .chat-box::-webkit-scrollbar-thumb { background: rgba(255,255,255,0.1); border-radius: 10px; }
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
  rom: [
    "Si on devait s'enfuir tous les deux un week-end, tu choisirais la mer ou la montagne ?",
    "Quel est le plus beau compliment que je t'ai fait ?",
    "Quelle est la première chose à laquelle tu penses quand tu te réveilles à côté de moi ?",
    "Quel est le vêtement que je porte que tu préfères ?",
    "Quelle activité on n'a jamais faite ensemble et que tu meurs d'envie d'essayer ?",
    "Si tu pouvais figer un moment de notre histoire pour toujours, ce serait lequel ?",
    "Qu'est-ce qui te rend le plus fier dans notre couple ?",
    "Quel est l'endroit le plus insolite où tu aimerais m'embrasser ?",
    "Quel petit rituel quotidien avec moi tu ne voudrais jamais perdre ?"
  ],
  ver: [
    "Quelle a été ta première impression quand tu m'as vu pour la toute première fois ?",
    "Y a-t-il un secret sur toi que tu n'as encore osé dire à personne, même pas à moi ?",
    "Quelle est la chose la plus folle que tu aies faite par amour que je ne sache pas ?",
    "Si tu pouvais changer une seule petite habitude chez moi, ce serait quoi ?",
    "Quel est ton plus grand regret dans notre relation ?",
    "Si on te proposait 1 million d'euros pour ne plus jamais me voir, tu hésiterais combien de secondes ?",
    "Quelle est la partie de mon corps qui te rend le plus emoustiller ?"
  ],
  cha: [
    "Quelle est ta zone érogène la plus sensible que je n'explore pas assez ?",
    "Décris-moi ton fantasme le plus récurrent quand tu penses à nous deux.",
    "Quelle tenue aimerais-tu me voir porter ce soir ?",
    "Est-ce que tu préfères quand je suis tendre ou quand je suis plus dominant ?",
    "Tu préfère dominr ou etre dominé", 
    "Quel est l'endroit le plus risqué où tu aimerais qu'on le fasse ?",
    "Quelle est la chose la plus osée que tu aies envie que je te chuchote à l'oreille ?",
    "Si tu devais utiliser un seul mot pour décrire nos moments intimes, ce serait quoi ?",
    "Quel est le souvenir le plus 'chaud' que tu gardes de nous ?",
    "Quel est la position que tu aimerais fair qu'on a jamais faite",
    "Qu'aimerais tu essayer de nouveau?",
    "Quelle serais le fantasme que tu voudrais réaliser avec moi?"
  ],
  act: [
    "Envoie-moi une photo de la partie de ton corps que je préfère.", 
    "Envoie-moi une vidéo qui me donnerait très envie de toi.", 
    "Prends une photo sexy là tout de suite.", 
    "Prends une photo de tes lèvres et envoie-la.", 
    "Envoie une photo de toi dans ton miroir.",
    "Prends une photo sexy la plus osée que tu n'aies jamais faite",
    "Quel genre de photos ou vidéos tu préfères que je t'envoie ?", 
    "Envoie-moi une photo de la partie de ton corps que TU préfères."
  ]
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
    card.innerHTML = `<div class="sub">Donne ce code à ton partenaire :</div><div class="code-box">${state.roomCode}</div><div class="sub">En attente d'une connexion...</div>`;
  } else {
    const isMyTurn = state.playerNum === state.turn;
    card.innerHTML = `
      <div class="turn-bar" style="background:${isMyTurn?'rgba(74, 222, 128, 0.1)':'rgba(125, 211, 252, 0.1)'};color:${isMyTurn?'#4ade80':'#7dd3fc'};border:1px solid ${isMyTurn?'rgba(74, 222, 128, 0.2)':'rgba(125, 211, 252, 0.2)'}">${isMyTurn?'🎯 C\'est ton tour !':'⏳ Tour de ton partenaire...'}</div>
      <div class="q-box">${state.currentQ}</div>
      <div class="cat-grid">
        <button class="cat-btn" style="background:#c9184a" onclick="pick('rom')">❤️ Romantique</button>
        <button class="cat-btn" style="background:#7209b7" onclick="pick('ver')">💡 Vérité</button>
        <button class="cat-btn" style="background:#e07a00" onclick="pick('cha')">🔥 Chaud</button>
        <button class="cat-btn" style="background:#2b9348" onclick="pick('act')">⚡ Action</button>
      </div>
      <div class="chat-box" id="chat">${state.chat.map(m=>`<div class="msg ${m.type==='s'?'msg-info':(m.p==state.playerNum?'msg-me':'msg-other')}">${m.type==='c'?'<b>'+m.n+'</b>':''} ${m.t}</div>`).join('')}</div>
      <div style="display:flex;gap:8px;margin-bottom:12px"><input class="inp" id="mi" placeholder="Message..." style="margin:0"><button class="btn btn-red" onclick="send()" style="width:70px;margin:0">OK</button></div>
      <div class="score-row">
        <span class="score-label">${state.scoreVal}%</span>
        <input type="range" min="0" max="100" value="${state.scoreVal}" id="sl">
        <button class="btn btn-score" onclick="sendScore()">⭐ Envoyer</button>
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
  const list = Q[cat];
  if(!list) return;
  const question = list[Math.floor(Math.random()*list.length)];
  state.currentQ = question;
  if(conn) conn.send({type:'q', q:question});
  render();
}

render();
</script>
</body>
</html>
