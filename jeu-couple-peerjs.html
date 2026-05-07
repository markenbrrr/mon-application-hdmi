<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🔥 Jeu de Couple</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/peerjs/1.5.4/peerjs.min.js"></script>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body {
  font-family: Arial, sans-serif;
  background: #0f0f12;
  color: white;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 24px 16px;
}
h1 { color: #ff4d6d; font-size: 24px; margin-bottom: 4px; text-align: center; }
.sub { color: #ffb3c1; font-size: 13px; margin-bottom: 20px; text-align: center; }
.card {
  background: #1a1a22; border-radius: 14px;
  padding: 22px; width: 100%; max-width: 420px;
  border: 1px solid #2e2e3e;
}
.inp {
  width: 100%; padding: 10px 13px; border-radius: 8px;
  border: 1px solid #3a3a4e; background: #0f0f18;
  color: white; font-size: 14px; margin-bottom: 10px; outline: none;
}
.inp:focus { border-color: #ff4d6d; }
.inp::placeholder { color: #555; }
.inp:disabled { opacity: 0.35; }
.btn {
  width: 100%; padding: 11px; border-radius: 8px;
  border: none; color: white; cursor: pointer;
  font-size: 14px; font-weight: bold; margin-bottom: 8px;
}
.btn:disabled { opacity: 0.35; cursor: default; }
.btn-red    { background: #c9184a; }
.btn-dark   { background: #2a2a3a; }
.btn-purple { background: #7209b7; }
.btn-sm     { width: auto; padding: 8px 14px; font-size: 13px; }
.divider { color: #444; text-align: center; font-size: 12px; margin: 10px 0; }
.code-box {
  font-size: 32px; font-weight: bold; letter-spacing: 6px;
  color: #ff4d6d; text-align: center; margin: 14px 0;
  background: #0f0f18; padding: 14px; border-radius: 10px;
  border: 1px solid #2e2e3e; word-break: break-all;
}
.turn-bar { border-radius: 8px; padding: 9px 12px; font-size: 13px; margin-bottom: 12px; text-align: center; }
.q-box {
  background: #0f0f18; border-radius: 10px; padding: 14px;
  color: #ffb3c1; font-size: 15px; min-height: 54px;
  margin-bottom: 12px; border: 1px solid #2e2e3e; line-height: 1.5;
}
.cat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 7px; margin-bottom: 12px; }
.cat-btn {
  padding: 10px; border-radius: 8px; border: none;
  color: white; cursor: pointer; font-size: 13px; font-weight: bold;
}
.cat-btn:active { opacity: 0.7; }
.chat-box {
  border: 1px solid #2e2e3e; border-radius: 10px;
  height: 175px; overflow-y: auto; padding: 10px;
  margin-bottom: 10px; background: #0f0f18;
}
.msg { font-size: 13px; margin-bottom: 6px; line-height: 1.4; }
.msg-score { color: #888; font-style: italic; font-size: 12px; }
.score-row { display: flex; align-items: center; gap: 8px; margin-top: 10px; }
.score-row input[type=range] { flex: 1; accent-color: #c9184a; }
.err { color: #ff6b6b; font-size: 13px; text-align: center; margin-bottom: 8px; }
.hint { color: #444; font-size: 11px; text-align: center; margin-top: 8px; }
.badge {
  display: inline-block; padding: 2px 8px; border-radius: 5px;
  font-size: 11px; font-weight: bold; margin-left: 6px;
  background: #c9184a33; color: #ff4d6d;
}
.status { color: #555; font-size: 12px; text-align: center; margin-top: 10px; }
</style>
</head>
<body>

<h1>🔥 Jeu de Couple</h1>
<div class="sub">Jouez ensemble, même à distance 💕</div>
<div class="card" id="app"></div>

<script>
const Q = {
  romantic: [
    "Quel moment avec moi t'a rendu le plus heureux(se) ?",
    "Qu'est-ce que tu aimes le plus chez moi ?",
    "Quel souvenir veux-tu recréer avec moi ?",
    "Quelle vie voudrais-tu mener avec moi dans 5 ans ?",
    "Quelle chanson te fait penser à moi ?",
    "Quel geste de ma part t'a le plus touché(e) ?",
    "Si tu devais décrire notre relation en un mot, lequel ?",
    "Qu'est-ce que tu apprécieras encore plus chez moi dans 10 ans ?",
    "Quel serait le voyage de rêve qu'on ferait ensemble ?",
    "Comment sais-tu que tu tiens vraiment à quelqu'un ?"
  ],
  tease: [
    "Quel truc que je fais te rend fou/folle sans que je le sache ?",
    "Qu'est-ce que tu remarques en premier quand tu me regardes ?",
    "À quelles situations tu penses à moi ?",
    "Qu'est-ce qui te ferait craquer en 10 secondes ?",
    "Quel est ton regard préféré que je t'adresse ?",
    "Tu me regardes comment quand je ne le sais pas ?",
    "Qu'est-ce que je fais qui te fait sourire bêtement ?",
    "Quel surnom me donnerais-tu si tu pouvais ?",
    "Quelle petite habitude de moi tu adorerais garder pour toujours ?",
    "Qu'est-ce que j'ai dit un jour que tu n'as pas oublié ?"
  ],
  spicy: [
    "Qu'est-ce qui te donne envie de te rapprocher de moi ?",
    "Quel détail chez moi pourrait m'exciter le plus ?",
    "Dis-moi ce que tu aimerais faire avec moi mais que tu ne m'as jamais dit",
    "Qu'est-ce que tu aimerais que je fasse là maintenant ?",
    "Où voudrais-tu aller avec moi pour une nuit secrète ?",
    "Qu'est-ce qui te ferait penser à moi toute la nuit ?",
    "Quelle surprise me ferait le plus d'effet selon toi ?",
    "Qu'est-ce que tu n'as jamais osé me dire mais tu penses souvent ?",
    "Si on avait une soirée sans limites, tu proposerais quoi ?",
    "Qu'est-ce que tu attendrais de moi si on était seuls quelque part ?"
  ],
  dare: [
    "Envoie-moi un message qui me fait plaisir",
    "Dis-moi quelque chose que tu n'as jamais osé dire",
    "Envoie une photo sur snap de la partie de ton corps que tu préfères",
    "Envoie une photo sur snap de la partie que je préfère à ton avis",
    "Fais-moi sourire avec un message inattendu",
    "Donne-moi un défi à ton tour",
    "Envoie-moi un voice message avec une voix drôle",
    "Raconte-moi un souvenir que je ne connais pas encore",
    "Dis-moi 3 choses que tu adorerais faire avec moi",
    "Invente une blague sur nous deux"
  ]
};

// ---- State ----
let S = {
  screen: 'home',
  myName: '', joinCode: '',
  playerNum: null,
  peer: null, conn: null,
  gs: { p1: null, p2: null, turn: 1, chat: [], total: 0, count: 0, currentQ: 'Choisis une catégorie 👇' },
  msg: '', scoreVal: 50, err: '', connStatus: ''
};

// ---- PeerJS ----
function initPeer(id) {
  const peer = id
    ? new Peer(id, { debug: 0 })
    : new Peer({ debug: 0 });
  S.peer = peer;

  peer.on('open', peerId => {
    if (S.playerNum === 1) {
      S.gs.peerId = peerId;
      S.screen = 'waiting';
      render();
    }
  });

  peer.on('connection', c => {
    S.conn = c;
    setupConn(c);
  });

  peer.on('error', e => {
    S.err = 'Erreur de connexion. Vérifie le code !';
    render();
  });
}

function setupConn(c) {
  c.on('open', () => {
    S.connStatus = 'connecté';
    if (S.playerNum === 1) {
      S.gs.p2 = S.gs.pendingP2 || 'Joueur 2';
      S.screen = 'game';
      send({ type: 'state', gs: S.gs });
    }
    render();
  });

  c.on('data', data => {
    if (data.type === 'state') {
      S.gs = data.gs;
      if (S.screen !== 'game') S.screen = 'game';
      render();
      scrollChat();
    }
    if (data.type === 'join') {
      S.gs.p2 = data.name;
      S.gs.pendingP2 = data.name;
    }
  });

  c.on('close', () => {
    S.connStatus = 'déconnecté';
    S.err = '⚠️ Connexion perdue. Relancez le jeu.';
    render();
  });
}

function send(data) {
  if (S.conn && S.conn.open) S.conn.send(data);
}

// ---- Actions ----
function createGame() {
  const name = S.myName.trim();
  if (!name) { S.err = 'Entre ton prénom !'; render(); return; }
  S.gs.p1 = name;
  S.playerNum = 1;
  S.err = '';
  initPeer();
}

function joinGame() {
  const name = S.myName.trim();
  const code = S.joinCode.trim();
  if (!name) { S.err = 'Entre ton prénom !'; render(); return; }
  if (!code) { S.err = 'Entre le code !'; render(); return; }
  S.gs.p2 = name;
  S.playerNum = 2;
  S.err = '';

  const peer = new Peer({ debug: 0 });
  S.peer = peer;
  peer.on('open', () => {
    const c = peer.connect(code, { reliable: true });
    S.conn = c;
    setupConn(c);
    c.on('open', () => {
      c.send({ type: 'join', name });
    });
  });
  peer.on('error', () => {
    S.err = 'Code introuvable. Vérifie !';
    render();
  });
  S.screen = 'connecting';
  render();
}

function pickQ(type) {
  const list = Q[type];
  S.gs.currentQ = list[Math.floor(Math.random() * list.length)];
  send({ type: 'state', gs: S.gs });
  render();
}

function sendMsg() {
  const txt = S.msg.trim();
  if (!txt) return;
  const name = S.playerNum === 1 ? S.gs.p1 : S.gs.p2;
  S.gs.chat.push({ name, text: txt, pn: S.playerNum });
  S.gs.turn = S.gs.turn === 1 ? 2 : 1;
  send({ type: 'state', gs: S.gs });
  S.msg = '';
  render();
  scrollChat();
}

function rateScore() {
  const v = S.scoreVal;
  S.gs.total = (S.gs.total || 0) + v;
  S.gs.count = (S.gs.count || 0) + 1;
  const avg = Math.round(S.gs.total / S.gs.count);
  S.gs.chat.push({ score: true, val: v, avg });
  send({ type: 'state', gs: S.gs });
  render();
}

function scrollChat() {
  setTimeout(() => {
    const c = document.getElementById('chat');
    if (c) c.scrollTop = c.scrollHeight;
  }, 40);
}

// ---- Render ----
function render() {
  const el = document.getElementById('app');
  if (!el) return;

  if (S.screen === 'home') {
    el.innerHTML = `
      ${S.err ? `<div class="err">${S.err}</div>` : ''}
      <input class="inp" id="n" placeholder="Ton prénom" value="${S.myName}">
      <button class="btn btn-red" id="bCreate">✨ Créer une partie (Joueur 1)</button>
      <div class="divider">— tu as reçu un code ? —</div>
      <input class="inp" id="jc" placeholder="Code reçu de ton/ta partenaire" value="${S.joinCode}">
      <button class="btn btn-dark" id="bJoin">🔗 Rejoindre (Joueur 2)</button>
    `;
    document.getElementById('n').oninput = e => { S.myName = e.target.value; S.err = ''; };
    document.getElementById('jc').oninput = e => { S.joinCode = e.target.value; S.err = ''; };
    document.getElementById('bCreate').onclick = createGame;
    document.getElementById('bJoin').onclick = joinGame;

  } else if (S.screen === 'connecting') {
    el.innerHTML = `
      <div style="text-align:center; padding:10px 0;">
        <div style="font-size:28px; margin-bottom:10px;">🔄</div>
        <div style="color:#aaa; font-size:14px;">Connexion en cours...</div>
        <div style="color:#555; font-size:12px; margin-top:8px;">Assure-toi que Joueur 1 a bien ouvert le jeu</div>
      </div>
    `;

  } else if (S.screen === 'waiting') {
    const code = S.peer ? S.peer.id : '...';
    el.innerHTML = `
      <div style="text-align:center">
        <div style="color:#aaa; font-size:14px; margin-bottom:8px;">Envoie ce code à ton/ta partenaire :</div>
        <div class="code-box">${code}</div>
        <div style="color:#555; font-size:12px; margin-bottom:16px;">Elle/il entre ce code pour rejoindre 💕</div>
        <div style="color:#666; font-size:13px;">⏳ En attente de Joueur 2...</div>
      </div>
    `;

  } else if (S.screen === 'game') {
    const gs = S.gs;
    const isMyTurn = S.playerNum === gs.turn;
    const myName = S.playerNum === 1 ? gs.p1 : gs.p2;
    const turnName = gs.turn === 1 ? gs.p1 : gs.p2;
    const turnBg = isMyTurn ? '#1a3a22' : '#1a1a2e';
    const turnColor = isMyTurn ? '#4ade80' : '#7dd3fc';

    const chatHtml = (gs.chat || []).map(m => {
      if (m.score) return `<div class="msg msg-score">⭐ Score : ${m.val}% (moy. ${m.avg}%)</div>`;
      const color = m.pn === S.playerNum ? '#ff4d6d' : '#7dd3fc';
      return `<div class="msg"><b style="color:${color}">${m.name}</b>  ${m.text}</div>`;
    }).join('');

    el.innerHTML = `
      <div class="turn-bar" style="background:${turnBg}; color:${turnColor}">
        ${isMyTurn ? `🎯 C'est ton tour, <b>${myName}</b> !` : `⏳ C'est le tour de <b>${turnName}</b>...`}
        <span class="badge">Joueur ${S.playerNum}</span>
      </div>
      <div class="q-box">${gs.currentQ || 'Choisis une catégorie 👇'}</div>
      <div class="cat-grid">
        <button class="cat-btn" style="background:#c9184a" data-t="romantic">❤️ Romantique</button>
        <button class="cat-btn" style="background:#7209b7" data-t="tease">😏 Teasing</button>
        <button class="cat-btn" style="background:#e07a00" data-t="spicy">🔥 Spicy</button>
        <button class="cat-btn" style="background:#2b9348" data-t="dare">🎯 Défi</button>
      </div>
      <div class="chat-box" id="chat">
        ${chatHtml || '<div style="color:#333; font-size:12px; text-align:center; padding-top:55px;">Les messages apparaîtront ici 💬</div>'}
      </div>
      <input class="inp" id="msgi" placeholder="${isMyTurn ? 'Ta réponse...' : 'Attends ton tour...'}" value="${S.msg}" ${isMyTurn ? '' : 'disabled'}>
      <button class="btn ${isMyTurn ? 'btn-red' : 'btn-dark'}" id="bSend" ${isMyTurn ? '' : 'disabled'}>
        ${isMyTurn ? '📤 Envoyer' : '⏳ Attends ton tour'}
      </button>
      <div class="score-row">
        <span id="slbl" style="color:#aaa; font-size:13px; min-width:36px">${S.scoreVal}%</span>
        <input type="range" min="0" max="100" step="1" value="${S.scoreVal}" id="sl">
        <button class="btn btn-purple btn-sm" id="bRate">⭐ Score</button>
      </div>
      <div class="hint">🟢 Connecté · Joueur 1 : ${gs.p1 || '?'} · Joueur 2 : ${gs.p2 || '?'}</div>
    `;

    document.querySelectorAll('.cat-btn').forEach(b => b.onclick = () => pickQ(b.dataset.t));
    const mi = document.getElementById('msgi');
    if (mi) {
      mi.oninput = e => S.msg = e.target.value;
      mi.onkeydown = e => { if (e.key === 'Enter' && !mi.disabled) sendMsg(); };
    }
    document.getElementById('bSend').onclick = sendMsg;
    const sl = document.getElementById('sl');
    if (sl) sl.oninput = e => {
      S.scoreVal = Number(e.target.value);
      const lbl = document.getElementById('slbl');
      if (lbl) lbl.textContent = S.scoreVal + '%';
    };
    document.getElementById('bRate').onclick = rateScore;
    scrollChat();
  }
}

render();
</script>
</body>
</html>
