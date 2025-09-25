<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=no"/>
<title>Recycle Rush ♻️ – Endless Emoji</title>
<style>
  :root{
    --bg1:#0e1633; --bg2:#0a1127; --text:#eef3ff; --muted:#a9b8ff;
    --accent:#1dd1a1; --accent2:#78e08f; --glass:rgba(255,255,255,.08); --stroke:rgba(255,255,255,.16);
    --btn:#182656; --btnH:#20306a;
  }
  html,body{height:100%;margin:0;background:radial-gradient(1200px 900px at 50% 8%, var(--bg1) 0%, var(--bg2) 60%);color:var(--text);font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif}
  #wrap{width:min(100vw,720px);height:min(100vh,1280px);aspect-ratio:9/16;margin:auto;position:relative;overflow:hidden;border-radius:18px;box-shadow:0 24px 60px rgba(0,0,0,.45);background:linear-gradient(180deg,var(--bg1),var(--bg2))}
  canvas{width:100%;height:100%;display:block}
  .ui{position:absolute;inset:0;pointer-events:none}

  .hud{position:absolute;top:8px;left:8px;right:8px;display:flex;gap:6px;justify-content:space-between;align-items:center}
  .pill{pointer-events:auto;background:var(--glass);border:1px solid var(--stroke);backdrop-filter:blur(6px);padding:7px 10px;border-radius:999px;font-weight:900}
  .btn{pointer-events:auto;cursor:pointer;background:var(--btn);border:1px solid var(--stroke);padding:9px 12px;border-radius:12px;font-weight:900;letter-spacing:.2px;transition:.15s}
  .btn:hover{background:var(--btnH)}
  .toast{position:absolute;top:64px;left:50%;transform:translateX(-50%);background:var(--glass);border:1px solid var(--stroke);padding:8px 14px;border-radius:999px;font-weight:900;opacity:0;transition:.25s}
  .show{opacity:1;transform:translate(-50%,-8px)}

  .goalBar{position:absolute;top:36px;left:12px;right:12px;height:10px;border-radius:999px;background:rgba(255,255,255,.08);overflow:hidden}
  .goalFill{height:100%;width:0%;background:linear-gradient(90deg,var(--accent),var(--accent2));transition:width .15s}

  .screen{position:absolute;inset:0;display:flex;align-items:center;justify-content:center}
  .center{max-width:92%;width:560px;background:rgba(15,22,58,.92);border:1px solid var(--stroke);border-radius:18px;padding:22px 20px;box-shadow:0 18px 60px rgba(0,0,0,.45);text-align:center}
  .logo{font-weight:1000;font-size:42px;letter-spacing:.3px;background:linear-gradient(90deg,var(--accent),var(--accent2));-webkit-background-clip:text;background-clip:text;color:transparent;margin:6px 0 4px}
  .subtitle{color:var(--muted);margin:2px 0 12px}
  .heroWrap{display:flex;justify-content:center;margin:8px 0 12px}
  #hero{width:440px;max-width:96%;height:auto;border-radius:12px;display:block}
  .row{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin:6px 0}
  select{background:var(--btn);color:var(--text);border:1px solid var(--stroke);border-radius:10px;padding:8px 10px;font-weight:900}
  label{color:#cfe7ff;opacity:.9;margin-right:6px}
  .footer{position:absolute;bottom:10px;left:0;right:0;text-align:center;font-size:12px;color:#cfe7ff70}

  .modal{position:absolute;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,.45)}
  .modal .card{background:#0f1b3d; border:1px solid var(--stroke); padding:18px 16px;border-radius:14px; max-width:90%; text-align:center}
  .modal h2{margin:6px 0 4px}
  .emojiBig{font-size:64px;line-height:1.1}

  .shopGrid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:10px;margin-top:8px}
  .shopItem{background:rgba(255,255,255,.06);border:1px solid var(--stroke);border-radius:12px;padding:10px}
  .shopItem h3{margin:0 0 6px;font-size:16px}
  .price{font-weight:900;color:#ffd36a;margin:6px 0}
  .tiny{font-size:12px;color:#cfe7ffb0}

  .comboMeter{position:absolute;bottom:12px;left:12px;right:12px;height:12px;border-radius:10px;background:rgba(255,255,255,.08);overflow:hidden}
  .comboFill{height:100%;width:0%;background:linear-gradient(90deg,#ffd36a,#ffb24a,#ff8b4a);transition:width .12s}

  @media (max-width:420px){
    .logo{font-size:34px}
    .pill{padding:6px 9px;font-size:13px}
    .btn{padding:8px 11px}
  }
</style>
</head>
<body>
<div id="wrap">
  <canvas id="game" width="540" height="960" aria-label="Recycle Rush game canvas"></canvas>

  <div class="ui">
    <div class="hud">
      <div class="row" style="gap:6px">
        <div class="pill">Score: <b id="score">0</b></div>
        <div class="pill">Combo: <b id="combo">0</b> <span id="mult"></span></div>
        <div class="pill">Goal: <b id="goal">1200</b></div>
        <div class="pill">Lvl: <b id="level">1</b></div>
        <div class="pill">🪙 <b id="coins">0</b></div>
      </div>
      <div class="row">
        <div class="btn" id="pauseBtn">⏸ Pause</div>
        <div class="btn" id="shopBtn">🛒 Shop</div>
        <div class="btn" id="muteBtn">🔊</div>
      </div>
    </div>
    <div class="goalBar"><div class="goalFill" id="goalFill"></div></div>
    <div class="comboMeter"><div class="comboFill" id="comboFill"></div></div>
    <div class="toast" id="toast">Nice!</div>
  </div>

  <!-- Start/Menu -->
  <div class="screen" id="startScreen">
    <div class="center">
      <div class="logo">♻️ Recycle Rush – Endless</div>
      <div class="subtitle">Tap recyclables, dodge the rest. Earn coins, upgrade, and climb endless levels.</div>
      <div class="heroWrap"><canvas id="hero" width="440" height="220"></canvas></div>
      <div class="row">
        <label for="difficulty">Difficulty</label>
        <select id="difficulty">
          <option value="chill">Chill</option>
          <option value="normal" selected>Normal</option>
          <option value="brisk">Brisk</option>
        </select>
        <label for="goalSel">Lvl 1 Goal</label>
        <select id="goalSel">
          <option value="1200" selected>1200</option>
          <option value="1500">1500</option>
          <option value="1800">1800</option>
        </select>
      </div>
      <div class="row">
        <div class="btn" id="startBtn">▶ Start</div>
        <div class="btn" id="optBtn">⚙ Options</div>
      </div>
      <div class="footer">Mobile-friendly. Progress autosaves. “A little color makes a big difference.”</div>
    </div>
  </div>

  <!-- Options -->
  <div class="screen" id="optScreen" style="display:none">
    <div class="center">
      <div class="logo" style="font-size:28px">Options</div>
      <div class="row" style="justify-content:center">
        <label><input type="checkbox" id="muteChk"> Mute all sounds & music</label>
        <div class="btn" id="resetSave">🗑 Reset Save</div>
      </div>
      <div class="row"><div class="btn" id="backBtn">⬅ Back</div></div>
    </div>
  </div>

  <!-- Checkpoint -->
  <div class="screen" id="winScreen" style="display:none">
    <div class="center">
      <div class="logo" style="font-size:32px">Checkpoint!</div>
      <div class="subtitle">You hit the goal. Coins awarded.</div>
      <div style="margin:10px 0 6px;font-size:18px">Score: <b id="finalScore">0</b></div>
      <div style="margin:0 0 12px;font-size:18px">🪙 +<b id="coinsEarned">0</b></div>
      <div class="row">
        <div class="btn" id="nextBtn">➡ Keep Going</div>
        <div class="btn" id="openShopFromWin">🛒 Shop</div>
        <div class="btn" id="menuBtn">🏠 Main Menu</div>
      </div>
    </div>
  </div>

  <!-- New Item Modal (gates level start) -->
  <div class="modal" id="newItemModal">
    <div class="card">
      <h2>New recyclable unlocked!</h2>
      <div class="emojiBig" id="newItemEmoji">🧴</div>
      <p id="newItemText" style="margin:8px 0 10px;color:#cfe7ff">This can be recycled here. Tap it for points & combo!</p>
      <div class="btn" id="newItemOk">Got it</div>
    </div>
  </div>

  <!-- Shop -->
  <div class="modal" id="shopModal">
    <div class="card" style="max-width:600px">
      <h2>Upgrade Shop 🛒</h2>
      <p class="tiny">Coins: <b id="coinsShop">0</b></p>
      <div class="shopGrid" id="shopGrid"></div>
      <div class="row" style="margin-top:10px">
        <div class="btn" id="closeShop">Close</div>
      </div>
    </div>
  </div>
</div>

<script>
(() => {
  const $ = s => document.querySelector(s);
  const canvas = $("#game"), ctx = canvas.getContext("2d");
  const W = canvas.width, H = canvas.height;
  const clamp=(v,a,b)=>Math.max(a,Math.min(b,v));
  const rand=(a,b)=>Math.random()*(b-a)+a;

  const scoreEl=$("#score"), comboEl=$("#combo"), multEl=$("#mult");
  const goalEl=$("#goal"), lvlEl=$("#level"), toast=$("#toast");
  const coinsEl=$("#coins"), goalFill=$("#goalFill"), comboFill=$("#comboFill");

  // Start hero
  const hero=$("#hero"), hctx=hero.getContext("2d");
  function drawHero(){
    const w=hero.width,h=hero.height;
    const g=hctx.createLinearGradient(0,0,w,h);
    g.addColorStop(0,"#11245d"); g.addColorStop(1,"#0c173d");
    hctx.fillStyle=g; hctx.fillRect(0,0,w,h);
    for(let i=0;i<3;i++){
      const ww=w-60- i*30, x=(w-ww)/2, y=h*(0.28+0.24*i);
      drawBelt(hctx, x, y, ww, 36, 12, i*0.15, 0.35);
    }
    hctx.font="bold 62px Apple Color Emoji, Segoe UI Emoji, Noto Color Emoji, system-ui";
    hctx.textAlign="center"; hctx.textBaseline="middle";
    hctx.fillText("📦", w*0.3, h*0.62);
    hctx.fillText("🧃", w*0.5, h*0.50);
    hctx.fillText("🍾", w*0.7, h*0.66);
  }
  (function loopHero(){ drawHero(); requestAnimationFrame(loopHero); })();

  // Audio
  let audioCtx=null, muted=false, musicGain=null, musicTimer=null, shakeT=0;
  function ensureAudio(){ if(!audioCtx){ try{ audioCtx=new (window.AudioContext||window.webkitAudioContext)(); }catch(e){} } }
  function beep(freq=440,dur=0.09,type="triangle",gain=0.10){ if(muted||!audioCtx) return; const t=audioCtx.currentTime; const o=audioCtx.createOscillator(), g=audioCtx.createGain(); o.type=type; o.frequency.setValueAtTime(freq,t); g.gain.setValueAtTime(0.0001,t); g.gain.exponentialRampToValueAtTime(gain,t+0.01); g.gain.exponentialRampToValueAtTime(0.0001,t+dur); o.connect(g).connect(audioCtx.destination); o.start(t); o.stop(t+dur+0.02); }
  function chord(base=420,combo=1){ const steps=Math.min(4,1+Math.floor(combo/4)); for(let i=0;i<steps;i++) setTimeout(()=>beep(base*(1+i*0.08),0.08,"sine",0.12), i*40); }
  function coinPing(){ beep(1200,0.08,"square",0.14); }
  function errorBuzz(){ if(muted||!audioCtx) return; const t=audioCtx.currentTime; const o=audioCtx.createOscillator(), g=audioCtx.createGain(); o.type="sawtooth"; o.frequency.setValueAtTime(380,t); o.frequency.linearRampToValueAtTime(120,t+0.25); g.gain.setValueAtTime(0.0001,t); g.gain.exponentialRampToValueAtTime(0.16,t+0.02); g.gain.exponentialRampToValueAtTime(0.0001,t+0.28); o.connect(g).connect(audioCtx.destination); o.start(t); o.stop(t+0.3); shakeT=220; }
  function fanfare(){ if(muted||!audioCtx) return; const seq=[[784,0.11],[988,0.11],[1174,0.13],[1318,0.18],[1568,0.16]]; let d=0; for(const [f,du] of seq){ setTimeout(()=>beep(f,du,"square",0.14), d*1000); d+=du*0.85; } }
  function startMusic(level){ if(muted) return; stopMusic(); if(!audioCtx) return; const ctxA=audioCtx; musicGain=ctxA.createGain(); const tier=((level-1)%3)+1; musicGain.gain.value=tier===1?0.16:tier===2?0.18:0.20; musicGain.connect(ctxA.destination); const tempo=tier===1?102:tier===2?118:132, interval=60/tempo; const scales={1:[261.63,293.66,329.63,392,523.25],2:[246.94,293.66,369.99,440,554.37],3:[277.18,329.63,369.99,415.3,493.88,587.33]}; const scale=scales[tier]; let step=0, t=ctxA.currentTime+0.05; musicTimer=setInterval(()=>{ note(scale[step%scale.length]/2,t,interval*0.95,"sine",0.18); note(scale[(step*2+3)%scale.length],t,interval*0.6,tier===1?"triangle":"square",tier===1?0.14:0.16); hat(t,interval*0.2,0.08); step++; t+=interval; }, interval*1000); function note(freq,t0,len,type,gain){ const o=ctxA.createOscillator(), g=ctxA.createGain(); o.type=type; o.frequency.setValueAtTime(freq,t0); g.gain.setValueAtTime(0.0001,t0); g.gain.exponentialRampToValueAtTime(gain,t0+0.01); g.gain.exponentialRampToValueAtTime(0.0001,t0+len); o.connect(g).connect(musicGain); o.start(t0); o.stop(t0+len);} function hat(t0,len,vol){ const b=ctxA.createBuffer(1,ctxA.sampleRate*len,ctxA.sampleRate); const d=b.getChannelData(0); for(let i=0;i<d.length;i++){ d[i]=(Math.random()*2-1)*Math.exp(-i/d.length);} const s=ctxA.createBufferSource(); s.buffer=b; const g=ctxA.createGain(); g.gain.value=vol; s.connect(g).connect(musicGain); s.start(t0);} }
  function stopMusic(){ if(musicTimer){ clearInterval(musicTimer); musicTimer=null; } }

  // Conveyor
  function beltRect(){ const beltW=Math.floor(W * (window.innerWidth<480? 0.56 : 0.64)); const beltX=(W-beltW)/2; return {x:beltX,y:0,w:beltW,h:H}; }
  function drawBelt(g,x,y,w,h,rollerR=16,anim=0,opacity=1){
    g.save(); g.globalAlpha=opacity; g.fillStyle="#09102a"; g.fillRect(x-14,y,14,h); g.fillRect(x+w,y,14,h);
    const grad=g.createLinearGradient(x,y,x+w,y); grad.addColorStop(0,"#233056"); grad.addColorStop(1,"#1b2548"); g.fillStyle=grad; g.fillRect(x,y,w,h);
    g.strokeStyle="rgba(255,255,255,.07)"; g.lineWidth=2; const step=24; const off=(Date.now()/6 + anim*120)%step;
    for(let yy=y-40; yy<y+h+40; yy+=step){ g.beginPath(); g.moveTo(x,yy+off); g.lineTo(x+w,yy+off-18); g.stroke(); }
    g.fillStyle="#0a0f22"; for(let i=0;i<w;i+=rollerR*2){ g.beginPath(); g.arc(x+i+rollerR, y+4, rollerR, 0, Math.PI*2); g.fill(); g.beginPath(); g.arc(x+i+rollerR, y+h-4, rollerR, 0, Math.PI*2); g.fill(); }
    g.restore();
  }

  // Lanes/items
  const LANE_COUNT=3; function laneX(l){ const {x,w}=beltRect(); const laneW=w/LANE_COUNT; return x+laneW*l+laneW/2; }
  const LEVEL_THEMES=[ {accent:"#1dd1a1",accent2:"#78e08f",bg1:"#0e1633",bg2:"#0a1127"}, {accent:"#58a6ff",accent2:"#8bd3ff",bg1:"#0e1536",bg2:"#0a0f2b"}, {accent:"#ffb24a",accent2:"#ffd36a",bg1:"#231323",bg2:"#160d2a"} ];
  const NONREC=["👟","🛍️","🍔","🥚"];
  const RECYCLABLES_ORDER=["🍾","🧃","📦","🧴","🥤","📄","🪫","🧯"];
  const NEW_ITEM_TEXT={"🧴":"Toiletry bottle (rinsed) – recyclable","🥤":"Take-out cup (clean) – recyclable","📄":"Paper – recyclable","🪫":"Battery – drop-off (bonus points)","🧯":"Metal canister – empty & recyclable"};

  const SAVE_KEY="recycle_rush_save_v3";
  function loadSave(){ try{ return JSON.parse(localStorage.getItem(SAVE_KEY)||"{}"); }catch(e){ return {}; } }
  function saveState(){ localStorage.setItem(SAVE_KEY, JSON.stringify({coins, level, upgrades, unlockedCount})); }
  const save = loadSave();

  const upgrades={
    valuePlus: save.upgrades?.valuePlus||0,
    slowBelt: save.upgrades?.slowBelt||0,
    luckyGreen: save.upgrades?.luckyGreen||0,
    bigEmoji:  save.upgrades?.bigEmoji||0,
    buffer:    save.upgrades?.buffer||0
  };
  const items=[], pops=[], particles=[];
  let running=false, paused=false, level=save.level||1;
  let score=0, combo=0, mult=1, goal=1200;
  let beltSpeed=100, spawnInterval=600, spawnTimer=0, lastT=performance.now();
  let difficulty="normal", coins=save.coins||0, unlockedCount=save.unlockedCount||3, mistakes=0;
  let comingFromWinShop=false; // <-- fix for “stall after shop from win”

  function upgradeList(){
    const cost=(base,lvl)=>Math.floor(base*Math.pow(1.7,lvl));
    return [
      {id:"valuePlus", name:"Greener Bonus", desc:"+2 points per recyclable per level", base:60, max:10},
      {id:"slowBelt",  name:"Smooth Conveyor", desc:"Belt accelerates slower", base:80, max:8},
      {id:"luckyGreen",name:"Recycling Luck", desc:"+5% recyclable spawn each", base:90, max:8},
      {id:"bigEmoji",  name:"Bigger Items", desc:"+6% item size per rank", base:70, max:6},
      {id:"buffer",    name:"Safety Net", desc:"1 extra mistake allowed per level", base:120, max:3}
    ].map(u=>({...u, price:cost(u.base, upgrades[u.id]||0), lvl:upgrades[u.id]||0}));
  }

  function applyTheme(lvl){ const t=LEVEL_THEMES[(lvl-1)%LEVEL_THEMES.length]; const r=document.documentElement.style; r.setProperty('--accent',t.accent); r.setProperty('--accent2',t.accent2); r.setProperty('--bg1',t.bg1); r.setProperty('--bg2',t.bg2); }

  // Level setup (don’t start moving if a new-item modal appears)
  function resetForLevel(lvl, fromStart=false){
    items.length=0; pops.length=0; particles.length=0; combo=0; mult=1; mistakes=0;
    level=lvl; lvlEl.textContent=lvl; applyTheme(lvl);
    let willGate=false;
    if(lvl>1 && lvl%2===0 && unlockedCount<RECYCLABLES_ORDER.length){
      unlockedCount++; const newEmoji=RECYCLABLES_ORDER[unlockedCount-1];
      $("#newItemEmoji").textContent=newEmoji; $("#newItemText").textContent=NEW_ITEM_TEXT[newEmoji]||"New recyclable item!";
      $("#newItemModal").style.display="flex"; paused=true; willGate=true;
    }
    if(lvl===1){
      goal = parseInt($("#goalSel").value||"1200",10);
      beltSpeed = (difficulty==="chill"? 90: difficulty==="brisk"? 125: 105);
      spawnInterval = (difficulty==="chill"? 720: difficulty==="brisk"? 520: 600);
      if(fromStart){ score=0; }
    } else {
      goal = Math.floor(goal*1.6 + 400);
      beltSpeed += 24 - upgrades.slowBelt*2;
      spawnInterval = Math.max(420, spawnInterval- (90 - upgrades.slowBelt*5));
    }
    goalEl.textContent=goal; updateGoalFill();
    if(!willGate){ ensureAudio(); startMusic(level); } // music starts only if no modal
  }

  function recPool(){ return RECYCLABLES_ORDER.slice(0, unlockedCount); }

  function spawnItem(){
    // 3% chance of ⭐ Golden Item
    if(Math.random()<0.03){
      const lane=Math.floor(Math.random()*LANE_COUNT);
      const baseSize=(window.innerWidth<480? 70: 80)*(1+upgrades.bigEmoji*0.06);
      items.push({ emoji:"⭐", rec:true, golden:true, lane, x:laneX(lane), y:H+60, size:baseSize+6, clickable:true, rot:0, wobbleT:Math.random()*6.28, fade:1 });
      return;
    }
    const recs=recPool();
    const bias=0.60 + upgrades.luckyGreen*0.05;
    const pool=Math.random()<bias ? recs : recs.concat(NONREC);
    const emoji=pool[Math.floor(Math.random()*pool.length)];
    const lane=Math.floor(Math.random()*LANE_COUNT);
    const baseSize=(window.innerWidth<480? 68: 76);
    const size=(baseSize+Math.random()*8)*(1+upgrades.bigEmoji*0.06);
    const rot=(Math.random()*0.28-0.14);
    items.push({emoji, rec:recs.includes(emoji), lane, x:laneX(lane), y:H+60, vy:-beltSpeed, size, clickable:true, red:0, rot, wobbleT:Math.random()*6.28, fade:1});
  }

  function pickAt(px,py){
    for(let i=items.length-1;i>=0;i--){
      const it=items[i]; const r=38;
      if(px>it.x-r && px<it.x+r && py>it.y-r && py<it.y+r && it.clickable) return {it,idx:i};
    }
    return null;
  }
  function screenToCanvas(cx,cy){ const r=canvas.getBoundingClientRect(); return {x:(cx-r.left)*(canvas.width/r.width), y:(cy-r.top)*(canvas.height/r.height)}; }

  canvas.addEventListener("pointerdown", e=>{
    if(!running||paused) return; ensureAudio();
    const {x,y}=screenToCanvas(e.clientX,e.clientY); const hit=pickAt(x,y); if(!hit) return;
    const it=hit.it;
    if(it.rec){
      // Golden item jackpot
      if(it.golden){
        const pts=200 + upgrades.valuePlus*20; score+=pts; for(let i=0;i<10;i++) spawnCoinBurst(it.x,it.y); chord(600, 10);
        pops.push({x:it.x,y:it.y,t:0,txt:`⭐ +${pts}`,col:"#ffe680"}); it.clickable=false; it.fade=0;
        updateGoalFill(); updateHUD(); if(score>=goal) checkpoint(); return;
      }
      combo++; mult = 1 + Math.floor(combo/5)*0.25;
      const base=12 + upgrades.valuePlus*2, bonus=Math.floor((combo-1)*3), pts=Math.floor((base+bonus)*mult);
      score+=pts; chord(360*Math.pow(2,combo/16), combo);
      pops.push({x:it.x,y:it.y,t:0,txt:`+${pts}`,col:"#aef1c2"});
      spawnCoinBurst(it.x,it.y, (combo%3===0?2:1));
      it.clickable=false; it.collected=true;
      beltSpeed=Math.min(beltSpeed+1.6, (difficulty==="chill"? 190: 245));
      spawnInterval=Math.max(spawnInterval-5, (difficulty==="chill"? 520: 430));
      flashToast(combo>=12?"🔥🔥 Mega Streak!": combo>=7?"🔥 Hot Streak!":"Nice!");
      updateGoalFill(); updateComboFill(true);
    } else {
      mistakes++;
      if(mistakes<=upgrades.buffer){ pops.push({x:it.x,y:it.y,t:0,txt:"⚠",col:"#ffd36a"}); flashToast("Safety Net used!", true); errorBuzz(); }
      else { combo=0; mult=1; it.red=1; errorBuzz(); pops.push({x:it.x,y:it.y,t:0,txt:"✖",col:"#ff9a9a"}); updateComboFill(false); }
    }
    updateHUD(); if(score>=goal) checkpoint(); saveState();
  }, {passive:true});

  function spawnCoinBurst(x,y,n=1){ for(let i=0;i<n;i++){ particles.push({type:"coin",x,y,vx:rand(-150,150),vy:rand(-260,-140),t:0}); } coinPing(); }

  window.addEventListener("touchstart", ()=>ensureAudio(), {once:true, passive:true});

  function updateHUD(){ scoreEl.textContent=score; comboEl.textContent=combo; multEl.textContent=mult>1?`×${mult.toFixed(2)}`:""; coinsEl.textContent=coins; }
  function updateGoalFill(){ goalFill.style.width=(clamp(score/goal,0,1)*100).toFixed(1)+"%"; }
  function updateComboFill(grow){ comboFill.style.width=(clamp(grow?combo/15:0,0,1)*100).toFixed(1)+"%"; }
  function flashToast(t,warn=false){ toast.textContent=t; toast.style.borderColor=warn?"rgba(255,107,107,.35)":"rgba(120,224,143,.35)"; toast.classList.remove("show"); void toast.offsetWidth; toast.classList.add("show"); setTimeout(()=>toast.classList.remove("show"),900); }

  function update(dt){
    spawnTimer-=dt; if(spawnTimer<=0){ spawnItem(); spawnTimer+=spawnInterval; }
    const br=beltRect(), laneW=br.w/LANE_COUNT;

    for(let i=items.length-1;i>=0;i--){
      const it=items[i];
      it.y += -beltSpeed*dt/1000;
      it.wobbleT+=dt*0.003; const wobble=Math.sin(it.wobbleT)*(laneW*0.08); it.x=laneX(it.lane)+wobble; it.rot+=(Math.sin(it.wobbleT*0.7))*0.001;
      it.red=Math.max(0,it.red-dt*0.006);
      if(it.collected){ it.fade=Math.max(0,it.fade-dt*0.0065); it.y-=dt*0.08; if(it.fade===0){ items.splice(i,1); continue; } }
      if(it.y<-80) items.splice(i,1);
    }

    for(let i=particles.length-1;i>=0;i--){
      const p=particles[i]; p.t+=dt; p.x+=p.vx*dt/1000; p.y+=p.vy*dt/1000; p.vy+=400*dt/1000;
      if(p.type==="coin"){
        const target={x:W-110,y:24}; const dx=target.x-p.x, dy=target.y-p.y, d=Math.hypot(dx,dy);
        if(d<30||p.t>1300){ coins++; updateHUD(); particles.splice(i,1); continue; }
        const pull=clamp(18000/(d*d+1200),0,0.7); p.vx+=dx*pull; p.vy+=dy*pull;
      }
      if(p.t>2500) particles.splice(i,1);
    }
    beltSpeed=Math.min(beltSpeed+dt*0.002,(difficulty==="chill"?195:250));
    if(shakeT>0) shakeT-=dt;
  }

  function draw(){
    const sx=shakeT>0?rand(-2,2):0, sy=shakeT>0?rand(-2,2):0; ctx.save(); ctx.translate(sx,sy);
    ctx.clearRect(0,0,W,H);

    for(let b=0;b<4;b++){ const ww=W*(0.76-b*0.06), hh=34, xx=(W-ww)/2, yy=H*(0.18+0.18*b); drawBelt(ctx,xx,yy,ww,hh,10,b*0.2,0.55-b*0.1); }
    const br=beltRect(); drawBelt(ctx,br.x,br.y,br.w,br.h,18,0,1);
    ctx.strokeStyle="rgba(255,255,255,.08)"; ctx.lineWidth=2; for(let i=1;i<LANE_COUNT;i++){ const lx=br.x+(br.w/LANE_COUNT)*i; ctx.beginPath(); ctx.moveTo(lx,0); ctx.lineTo(lx,H); ctx.stroke(); }

    ctx.textAlign="center"; ctx.textBaseline="middle";
    for(const it of items){
      ctx.save(); ctx.translate(it.x,it.y); ctx.rotate(it.rot); ctx.globalAlpha=it.collected?it.fade*0.9:1;
      ctx.font=`bold ${it.size}px Apple Color Emoji, Segoe UI Emoji, Noto Color Emoji, system-ui`; ctx.fillText(it.emoji,0,0);
      if(it.golden){ ctx.globalAlpha=0.8; ctx.font="bold 20px system-ui"; ctx.fillText("✨",20,-22); ctx.globalAlpha=1; }
      if(it.red>0){ ctx.globalAlpha=it.red*0.6; ctx.fillStyle="rgba(255,0,0,.25)"; ctx.beginPath(); ctx.arc(0,0,36,0,Math.PI*2); ctx.fill(); }
      ctx.restore();
    }

    for(const p of particles){ if(p.type==="coin"){ ctx.save(); ctx.translate(p.x,p.y); ctx.font="bold 22px system-ui, -apple-system"; ctx.fillText("🪙",0,0); ctx.restore(); } }
    ctx.font="900 24px system-ui, -apple-system";
    for(let i=pops.length-1;i>=0;i--){ const p=pops[i]; const a=1-p.t/700; ctx.strokeStyle=`rgba(0,0,0,${a*0.45})`; ctx.lineWidth=4; ctx.strokeText(p.txt,p.x,p.y); ctx.fillStyle=p.col; ctx.fillText(p.txt,p.x,p.y); p.t+=16; p.y-=0.96; if(p.t>700) pops.splice(i,1); }
    ctx.restore();
  }

  function loop(){ if(!running||paused){ lastT=performance.now(); return; } const t=performance.now(), dt=Math.min(50,t-lastT); lastT=t; update(dt); draw(); requestAnimationFrame(loop); }

  function checkpoint(){
    running=false; stopMusic(); fanfare();
    const earned=Math.max(5,Math.floor((goal/200)+combo*0.5)); coins+=earned; updateHUD(); saveState();
    $("#finalScore").textContent=score; $("#coinsEarned").textContent=earned; $("#winScreen").style.display="flex";
  }

  // Controls
  $("#pauseBtn").addEventListener("click", ()=>{ if(!running) return; paused=!paused; $("#pauseBtn").textContent=paused?"▶ Resume":"⏸ Pause"; if(!paused){ lastT=performance.now(); requestAnimationFrame(loop); }});
  $("#muteBtn").addEventListener("click", ()=>{ muted=!muted; $("#muteBtn").textContent=muted?"🔇":"🔊"; $("#muteChk").checked=muted; if(muted) stopMusic(); else { ensureAudio(); startMusic(level); }});

  // Shop (with “coming from win” resume fix)
  const shopModal=$("#shopModal"), shopGrid=$("#shopGrid"), coinsShop=$("#coinsShop");
  function openShop(fromWin=false){
    comingFromWinShop = fromWin; coinsShop.textContent=coins; shopGrid.innerHTML="";
    for(const u of upgradeList()){
      const div=document.createElement("div"); div.className="shopItem";
      div.innerHTML=`<h3>${u.name} ${u.lvl>0?`(Lv.${u.lvl})`:""}</h3><div class="tiny">${u.desc}</div><div class="price">🪙 ${u.price}</div><div class="btn buy" data-id="${u.id}">${u.lvl>=u.max?"Maxed":"Buy"}</div>`;
      shopGrid.appendChild(div);
    }
    shopModal.style.display="flex"; paused=true;
  }
  $("#shopBtn").addEventListener("click", ()=>openShop(false));
  $("#openShopFromWin").addEventListener("click", ()=>{ $("#winScreen").style.display="none"; openShop(true); });
  $("#closeShop").addEventListener("click", ()=>{
    shopModal.style.display="none";
    if(comingFromWinShop){ comingFromWinShop=false; // advance level and start
      resetForLevel(level+1);
      running=true; paused=false; ensureAudio(); startMusic(level); lastT=performance.now(); requestAnimationFrame(loop);
    } else { paused=false; lastT=performance.now(); requestAnimationFrame(loop); }
    saveState();
  });
  shopGrid.addEventListener("click", e=>{
    const btn=e.target.closest(".buy"); if(!btn) return;
    const id=btn.getAttribute("data-id"); const list=upgradeList(); const u=list.find(x=>x.id===id); if(!u) return;
    if(u.lvl>=u.max){ return; }
    if(coins>=u.price){ coins-=u.price; upgrades[id]++; coinPing(); coinsShop.textContent=coins; updateHUD(); // refresh grid
      openShop(comingFromWinShop);
    } else { flashToast("Not enough coins!", true); }
  });

  // Options
  $("#optBtn").addEventListener("click", ()=>{ $("#optScreen").style.display="flex"; $("#startScreen").style.display="none"; });
  $("#backBtn").addEventListener("click", ()=>{ $("#optScreen").style.display="none"; $("#startScreen").style.display="flex"; });
  $("#resetSave").addEventListener("click", ()=>{ localStorage.removeItem(SAVE_KEY); location.reload(); });

  // Start / next
  $("#startBtn").addEventListener("click", ()=>{
    ensureAudio();
    difficulty=$("#difficulty").value;
    $("#startScreen").style.display="none"; $("#optScreen").style.display="none"; $("#winScreen").style.display="none";
    updateHUD(); resetForLevel(1,true);
    running=true; paused=false; // if there was a new-item modal, paused will be set true and music delayed
    if(!paused){ startMusic(level); }
    lastT=performance.now(); requestAnimationFrame(loop);
  });
  $("#menuBtn").addEventListener("click", ()=>{ $("#winScreen").style.display="none"; $("#startScreen").style.display="flex"; stopMusic(); });
  $("#nextBtn").addEventListener("click", ()=>{ $("#winScreen").style.display="none"; resetForLevel(level+1); running=true; paused=false; ensureAudio(); startMusic(level); lastT=performance.now(); requestAnimationFrame(loop); });

  // New item modal acknowledge (belt/music start here)
  $("#newItemOk").addEventListener("click", ()=>{
    $("#newItemModal").style.display="none";
    paused=false; ensureAudio(); startMusic(level);
    lastT=performance.now(); requestAnimationFrame(loop);
  });

  $("#muteChk").addEventListener("change", e=>{ muted=e.target.checked; $("#muteBtn").textContent=muted?"🔇":"🔊"; if(muted) stopMusic(); else { ensureAudio(); startMusic(level); } });

  window.addEventListener("keydown", e=>{ if(!running) return; if(e.key===" "){ e.preventDefault(); $("#pauseBtn").click(); } if(e.key.toLowerCase()==="s"){ openShop(false); } });

  coinsEl.textContent=coins;

  function drawBelt(g,x,y,w,h,rollerR=16,anim=0,opacity=1){
    g.save(); g.globalAlpha=opacity; g.fillStyle="#09102a"; g.fillRect(x-14,y,14,h); g.fillRect(x+w,y,14,h);
    const grad=g.createLinearGradient(x,y,x+w,y); grad.addColorStop(0,"#233056"); grad.addColorStop(1,"#1b2548"); g.fillStyle=grad; g.fillRect(x,y,w,h);
    g.strokeStyle="rgba(255,255,255,.07)"; g.lineWidth=2; const step=24; const off=(Date.now()/6 + anim*120)%step;
    for(let yy=y-40; yy<y+h+40; yy+=step){ g.beginPath(); g.moveTo(x,yy+off); g.lineTo(x+w,yy+off-18); g.stroke(); }
    g.fillStyle="#0a0f22"; for(let i=0;i<w;i+=rollerR*2){ g.beginPath(); g.arc(x+i+rollerR,y+4,rollerR,0,Math.PI*2); g.fill(); g.beginPath(); g.arc(x+i+rollerR,y+h-4,rollerR,0,Math.PI*2); g.fill(); }
    g.restore();
  }
})();
</script>
</body>
</html>
