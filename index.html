<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>🔥 Jeu de Couple</title>
  <script src="https://unpkg.com/peerjs@1.5.2/dist/peerjs.min.js"></script>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; background: #0f0f12; color: white; }
    #root {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 24px 16px;
    }
    .title { color: #ff4d6d; font-size: 22px; font-weight: 600; margin-bottom: 4px; }
    .sub { color: #ffb3c1; font-size: 13px; margin-bottom: 20px; text-align: center; }
    .card {
      background: #1a1a22;
      border-radius: 14px;
      padding: 22px;
      width: 100%;
      max-width: 440px;
      border: 0.5px solid #2e2e3e;
      box-shadow: 0 10px 25px rgba(0,0,0,0.3);
    }
    .inp {
      width: 100%; padding: 12px 13px; border-radius: 8px;
      border: 0.5px solid #3a3a4e; background: #0f0f18;
      color: white; font-size: 14px; margin-bottom: 10px;
      outline: none;
    }
    .inp:focus { border-color: #ff4d6d; }
    .btn {
      width: 100%; padding: 12px; border-radius: 8px;
      border: none; color: white; cursor: pointer;
      font-size: 14px; font-weight: 600; margin-bottom: 8px;
      transition: transform 0.1s;
    }
    .btn:active { transform: scale(0.98); }
    .btn-red { background: #c9184a; }
    .btn-dark { background: #2a2a3a; }
    .divider { color: #444; text-align: center; font-size: 12px; margin: 12px 0; }
    .code-box {
      font-size: 32px; font-weight: 700; letter-spacing: 6px;
      color: #ff4d6d; text-align: center; margin: 16px 0;
      background: #0f0f18; padding: 16px; border-radius: 10px;
      border: 1px dashed #ff4d6d;
    }
    .turn-bar {
      border-radius: 8px; padding: 10px;
      font-size: 13px; margin-bottom: 12px; text-align: center;
      font-weight: 600;
    }
    .q-box {
      background: #0f0f18; border-radius: 10px; padding: 16px;
      color: #ffb3c1; font-size: 15px; min-height: 60px;
      margin-bottom: 12px; border: 0.5px solid #2e2e3e;
      line-height: 1.5; display: flex; align-items: center; justify-content: center; text-align: center;
    }
    .cat-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 12px;
    }
    .cat-btn {
      padding: 10px; border-radius: 8px; border: none;
      color: white; cursor: pointer; font-size: 12px; font-weight: 600;
    }
    .chat-box {
      border: 0.5px solid #2e2e3e; border-radius: 10px;
      height: 160px; overflow-y: auto; padding: 10px;
      margin-bottom: 10px; background: #0f0f18;
    }
    .msg { font-size: 13px; margin-bottom: 8px; padding: 6px 10px; border-radius: 6px; width: fit-content; max-width: 80%; }
    .msg-me { background: #c9184a22; margin-left: auto; border: 0.5px solid #c9184a44; }
    .msg-other { background: #2a2a3a; margin-right: auto; border: 0.5px solid #3a3a4e; }
    .msg b { display: block; font-size: 10px; text-transform: uppercase; margin-bottom: 2px; opacity: 0.7; }
    .err { color: #ff6b6b; font-size: 13px; text-align: center; margin-bottom: 10px; font-weight: 500; }
  </style>
</head>
<body>

<div id="root">
  <div class="title">🔥 Jeu de Couple</div>
  <div class="sub">Jouez ensemble, même à distance 💕</div>
  <div class="card" id="app-card"></div>
</div>

<script>
const Q = {
  romantic: ["Quel moment avec moi t'a rendu le plus heureux(se) ?", "Qu'est-ce que tu aimes le plus chez moi ?", "Quel souvenir veux-tu recréer avec moi ?", "Quelle vie voudrais-tu mener avec moi dans 5 ans ?", "Quelle chanson te fait penser à moi ?", "Quel geste de ma part t'a le plus touché(e) ?", "Si tu devais décrire notre relation en un mot, lequel ?", "Qu'est-ce que tu apprécieras encore plus chez moi dans 10 ans ?", "Quel serait le voyage de rêve qu'on ferait ensemble ?", "Comment sais-tu que tu tiens vraiment à quelqu'un ?"],
  tease: ["Quel truc que je fais te rend fou/folle sans que je le sache ?", "Qu'est-ce que tu remarques en premier quand tu me regardes ?", "À quelles situations tu penses à moi ?", "Qu'est-ce qui te ferait craquer en 10 secondes ?", "Quel est ton regard préféré que je t'adresse ?", "Tu me regardes comment quand je ne le sais pas ?", "Qu'est-ce que je fais qui te fait sourire bêtement ?", "Quel surnom me donnerais-tu si tu pouvais ?", "Quelle petite habitude de moi tu adorerais garder pour toujours ?", "Qu'est-ce que j'ai dit un jour que tu n'as pas oublié ?"],
  spicy: ["Qu'est-ce qui te donne envie de te rapprocher de moi ?", "Quel détail chez moi pourrait m'exciter le plus ?", "Dis-moi ce que tu aimerais faire avec moi mais que tu ne m'as jamais dit", "Qu'est-ce que tu aimerais que je fasse là maintenant ?", "Où voudrais-tu aller avec moi pour une nuit secrète ?", "Qu'est-ce qui te ferait penser à moi toute la nuit ?", "Quelle surprise me ferait le plus d'effet selon toi ?", "Qu'est-ce que tu n'as jamais osé me dire mais tu penses souvent ?", "Si on avait une soirée sans limites, tu proposerais quoi ?", "Qu'est-ce que tu attendrais de moi si on était seuls quelque part ?"],
  dare: ["Envoie-moi un message qui me fait plaisir", "Dis-moi quelque chose que tu n'as jamais osé dire", "Envoie une photo sur snap de la partie de ton corps que tu préfères", "Envoie une photo sur snap de la partie que je préfère à ton avis", "Fais-moi sourire avec un message inattendu", "Donne-moi un défi à ton tour", "Envoie-moi un voice message avec une voix drôle", "Raconte-moi un souvenir que je ne connais pas encore", "Dis-moi 3 choses que tu adorerais faire avec moi", "Invente une blague sur nous deux"]
};

let state = {
  screen: 'home', myName: '', joinCode: '', roomCode: '',
  playerNum: null, turn: 1, currentQ: 'Choisis une catégorie 👇',
  chat: [], err: ''
};

let peer = null, conn = null;

function render() {
  const card = document.getElementById('app-card');
  if (state.screen === 'home') {
    card.innerHTML = `
      ${state.err ? `<div class="err">${state.err}</div>` : ''}
      <input class="inp" id="myname" placeholder="Ton prénom" value="${state.myName}">
      <button class="btn btn-red" onclick="createRoom()">✨ Créer une partie</button>
      <div class="divider">— ou —</div>
      <input class="inp" id="jcode" placeholder="Entrer le code reçu" value="${state.joinCode}">
      <button class="btn btn-dark" onclick="joinRoom()">🔗 Rejoindre</button>
    `;
    document.getElementById('myname').oninput = e => state.myName = e.target.value;
    document.getElementById('jcode').oninput = e => state.joinCode = e.target.value.toUpperCase();
  } else if (state.screen === 'waiting') {
    card.innerHTML = `
      <div class="sub">Envoie ce code à ton partenaire :</div>
      <div class="code-box">${state.roomCode}</div>
      <div class="sub" style="margin-top:10px">Attends qu'il/elle rejoigne...</div>
      <button class="btn btn-dark" onclick="location.reload()" style="margin-top:15px">Annuler</button>
    `;
  } else if (state.screen === 'game') {
    const isMyTurn = state.playerNum === state.turn;
    card.innerHTML = `
      <div class="turn-bar" style="background:${isMyTurn?'#1a3a22':'#1a1a2e'}; color:${isMyTurn?'#4ade80':'#7dd3fc'}">
        ${isMyTurn ? '🎯 C\'est ton tour !' : '⏳ Attends sa réponse...'}
      </div>
      <div class="q-box">${state.currentQ}</div>
      <div class="cat-grid">
        <button class="cat-btn" style="background:#c9184a" onclick="pickQ('romantic')">❤️ Romantique</button>
        <button class="cat-btn" style="background:#7209b7" onclick="pickQ('tease')">😏 Teasing</button>
        <button class="cat-btn" style="background:#e07a00" onclick="pickQ('spicy')">🔥 Spicy</button>
        <button class="cat-btn" style="background:#2b9348" onclick="pickQ('dare')">🎯 Défi</button>
      </div>
      <div class="chat-box" id="chat">
        ${state.chat.map(m => `
          <div class="msg ${m.pn === state.playerNum ? 'msg-me' : 'msg-other'}">
            <b>${m.name}</b>${m.text}
          </div>
        `).join('')}
      </div>
      <div style="display:flex; gap:5px">
        <input class="inp" id="msginp" placeholder="Écris ici..." style="margin-bottom:0">
        <button class="btn btn-red" onclick="sendMsg()" style="width:80px; margin-bottom:0">OK</button>
      </div>
    `;
    const c = document.getElementById('chat'); 
    if(c) c.scrollTop = c.scrollHeight;
    document.getElementById('msginp').onkeydown = e => { if(e.key==='Enter') sendMsg(); };
  }
}

function createRoom() {
  if(!state.myName) { state.err = "Entre ton prénom d'abord !"; render(); return; }
  state.roomCode = Math.random().toString(36).substring(2,6).toUpperCase();
  peer = new Peer('LOVE-' + state.roomCode);
  
  peer.on('open', () => { state.screen = 'waiting'; render(); });
  peer.on('connection', c => {
    conn = c;
    state.playerNum = 1;
    setupConn();
  });
  peer.on('error', () => { state.err = "Erreur de connexion. Réessaie."; render(); });
}

function joinRoom() {
  if(!state.myName || !state.joinCode) { state.err = "Nom et Code requis !"; render(); return; }
  peer = new Peer();
  peer.on('open', () => {
    conn = peer.connect('LOVE-' + state.joinCode);
    state.playerNum = 2;
    setupConn();
  });
  peer.on('error', () => { state.err = "Code invalide."; render(); });
}

function setupConn() {
  conn.on('open', () => {
    state.screen = 'game';
    render();
    conn.on('data', data => {
      if(data.type === 'chat') {
        state.chat.push(data);
        state.turn = state.playerNum; // C'est à mon tour quand je reçois un msg
      }
      if(data.type === 'q') {
        state.currentQ = data.q;
      }
      render();
    });
  });
  conn.on('close', () => { alert("Partenaire déconnecté"); location.reload(); });
}

function sendMsg() {
  const i = document.getElementById('msginp');
  if(!i.value || !conn) return;
  const m = { type:'chat', name:state.myName, text:i.value, pn:state.playerNum };
  conn.send(m);
  state.chat.push(m);
  state.turn = (state.playerNum === 1 ? 2 : 1);
  i.value = '';
  render();
}

function pickQ(cat) {
  const q = Q[cat][Math.floor(Math.random() * Q[cat].length)];
  state.currentQ = q;
  if(conn) conn.send({ type: 'q', q: q });
  render();
}

render();
</script>
</body>
</html>
