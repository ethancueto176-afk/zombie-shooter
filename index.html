<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ZOMBIE OUTBREAK: CO-OP</title>
<style>
  html,body{margin:0;padding:0;width:100%;height:100%;background:#0a0a0f;overflow:hidden;font-family:'Courier New',monospace;color:#c8ffc8;}
  #wrap{position:fixed;inset:0;}
  canvas{display:block;width:100%;height:100%;cursor:crosshair;}
  #hud{position:fixed;top:10px;left:10px;z-index:5;pointer-events:none;text-shadow:0 0 6px #000;}
  #hud .row{margin-bottom:6px;font-size:18px;letter-spacing:1px;}
  #hpbar{width:220px;height:14px;border:2px solid #4f4;border-radius:2px;background:#200;}
  #hpfill{height:100%;width:100%;background:linear-gradient(90deg,#f55,#5f5);transition:width .15s;}
  #bossbar{position:fixed;top:10px;left:50%;transform:translateX(-50%);width:420px;z-index:5;display:none;pointer-events:none;text-align:center;}
  #bossbar .name{color:#f66;font-size:20px;letter-spacing:3px;text-shadow:0 0 8px #000;}
  #bossfill{height:12px;width:100%;background:linear-gradient(90deg,#f33,#fa0);transition:width .2s;}
  #overlay{position:fixed;inset:0;z-index:10;display:flex;flex-direction:column;align-items:center;justify-content:center;background:rgba(5,5,10,.9);text-align:center;}
  #overlay h1{color:#5f5;font-size:44px;letter-spacing:6px;margin:0 0 10px;text-shadow:0 0 18px #3f3;}
  #overlay p{max-width:560px;line-height:1.5;font-size:16px;color:#cfc;}
  #overlay button{margin-top:22px;padding:14px 34px;font-size:20px;font-family:inherit;background:#0f0;color:#050;border:none;border-radius:4px;cursor:pointer;letter-spacing:2px;}
  #overlay button:hover{background:#3f3;}
  .keys{margin-top:14px;color:#8c8;font-size:14px;}
  #mp{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin-top:16px;max-width:560px;}
  #mp button{margin-top:0;padding:10px 18px;font-size:16px;}
  #joinrow{display:none;gap:8px;justify-content:center;width:100%;align-items:center;}
  #codein{width:120px;padding:10px;font-size:18px;font-family:inherit;text-align:center;text-transform:uppercase;background:#020;color:#5f5;border:2px solid #4f4;border-radius:4px;letter-spacing:4px;}
  #netstatus{width:100%;color:#ff5;font-size:14px;min-height:18px;}
  #ownerbtn{margin-top:14px;background:#111;color:#999;border:1px solid #444;padding:8px 16px;font-size:13px;letter-spacing:2px;}
  #ownerbtn:hover{background:#222;}
  #ownerp{position:fixed;inset:0;z-index:20;background:rgba(5,5,10,.96);display:none;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:20px;}
  #ownerp input{padding:10px;font-size:16px;font-family:inherit;background:#020;color:#5f5;border:2px solid #4f4;border-radius:4px;width:170px;text-align:center;}
  #ownerp button{margin:8px;padding:10px 16px;font-size:15px;font-family:inherit;background:#0f0;color:#050;border:none;border-radius:4px;letter-spacing:1px;}
  #pinmsg{color:#ff5;font-size:14px;min-height:18px;margin:4px;}
  #banlist{margin-top:10px;color:#cfc;font-size:14px;max-width:420px;}
  #banlist button{margin:4px;padding:6px 10px;font-size:12px;}
  #weapbtn{position:fixed;left:50%;bottom:16px;transform:translateX(-50%);z-index:7;padding:10px 20px;font-size:16px;font-family:inherit;background:#020;color:#5f5;border:2px solid #4f4;border-radius:6px;display:none;letter-spacing:2px;}
  #banbtn{position:fixed;top:60px;right:10px;z-index:7;display:none;background:#300;color:#f88;border:2px solid #f66;border-radius:4px;padding:8px 12px;font-family:inherit;font-size:13px;}
  #banner{position:fixed;top:35%;left:0;right:0;z-index:6;text-align:center;font-size:46px;color:#f55;letter-spacing:8px;pointer-events:none;opacity:0;text-shadow:0 0 20px #900;}
  #banner.show{animation:banner 2.2s ease forwards;}
  @keyframes banner{0%{opacity:0;transform:scale(.6)}20%{opacity:1;transform:scale(1.05)}80%{opacity:1}100%{opacity:0;transform:scale(1.1)}}
</style>
</head>
<body>
<div id="wrap"><canvas id="game"></canvas></div>
<div id="hud">
  <div class="row">HP <div id="hpbar"><div id="hpfill"></div></div></div>
  <div class="row">WAVE <span id="wave">1</span> &nbsp; SCORE <span id="score">0</span> &nbsp; AMMO <span id="ammo">12/12</span></div>
  <div class="row" id="buff"></div>
</div>
<div id="bossbar"><div class="name" id="bossname">THE BUTCHER</div><div style="border:2px solid #f66;border-radius:2px;background:#300;"><div id="bossfill"></div></div></div>
<div id="banner"></div>
<div id="overlay">
  <h1>ZOMBIE OUTBREAK</h1>
  <p id="story">The city is gone. The dead walk in waves, and every fifth wave a BOSS hunts you. Survive as long as you can. Or play co-op: one of you hosts, the other joins with the room code.</p>
  <p class="keys">WASD / arrows to move &middot; mouse to aim &middot; hold click to shoot &middot; R to reload &middot; P to pause</p>
  <button id="startbtn">SOLO GAME</button>
  <div id="mp">
    <button id="hostbtn">HOST CO-OP</button>
    <button id="joinbtn">JOIN CO-OP</button>
    <div id="joinrow"><input id="codein" maxlength="4" placeholder="CODE" autocomplete="off"><button id="joingo">GO</button></div>
    <div id="netstatus"></div>
    <button id="ownerbtn">OWNER</button>
  </div>
</div>
<div id="ownerp">
  <h1 style="color:#5f5;font-size:30px;letter-spacing:4px;margin:0 0 14px;">OWNER</h1>
  <div id="pinrow"><input id="pinin" type="password" maxlength="24" placeholder="PIN" autocomplete="off"><button id="pinok">ENTER</button></div>
  <div id="pinmsg"></div>
  <div id="ownertools" style="display:none">
    <button id="swbtn">SECRET WEAPONS: OFF</button>
    <div style="margin-top:10px;"><input id="addin" maxlength="24" placeholder="new owner pin" autocomplete="off" style="margin-right:6px;"><button id="addok">ADD OWNER</button></div>
    <div id="banlist"></div>
  </div>
  <button id="ownerback">BACK</button>
</div>
<button id="weapbtn">PISTOL</button>
<button id="banbtn">BAN PLAYER</button>
</div>
<script>
"use strict";
const cv=document.getElementById('game'),ctx=cv.getContext('2d');
let W=0,H=0;function resize(){W=cv.width=innerWidth;H=cv.height=innerHeight;}addEventListener('resize',resize);resize();

// ---------- audio ----------
let AC=null;function ac(){if(!AC){try{AC=new (window.AudioContext||window.webkitAudioContext)();}catch(e){}}return AC;}
function sfx(type){const a=ac();if(!a)return;const t=a.currentTime,o=a.createOscillator(),g=a.createGain();o.connect(g);g.connect(a.destination);
 if(type==='shoot'){o.type='square';o.frequency.setValueAtTime(220,t);o.frequency.exponentialRampToValueAtTime(60,t+.08);g.gain.setValueAtTime(.06,t);g.gain.exponentialRampToValueAtTime(.001,t+.09);o.start(t);o.stop(t+.1);}
 else if(type==='hit'){o.type='sawtooth';o.frequency.setValueAtTime(160,t);o.frequency.exponentialRampToValueAtTime(40,t+.12);g.gain.setValueAtTime(.08,t);g.gain.exponentialRampToValueAtTime(.001,t+.13);o.start(t);o.stop(t+.14);}
 else if(type==='hurt'){o.type='triangle';o.frequency.setValueAtTime(90,t);o.frequency.exponentialRampToValueAtTime(30,t+.25);g.gain.setValueAtTime(.15,t);g.gain.exponentialRampToValueAtTime(.001,t+.3);o.start(t);o.stop(t+.3);}
 else if(type==='boss'){o.type='sawtooth';o.frequency.setValueAtTime(55,t);o.frequency.linearRampToValueAtTime(35,t+.8);g.gain.setValueAtTime(.2,t);g.gain.exponentialRampToValueAtTime(.001,t+.9);o.start(t);o.stop(t+.9);}
 else if(type==='pick'){o.type='sine';o.frequency.setValueAtTime(500,t);o.frequency.linearRampToValueAtTime(900,t+.12);g.gain.setValueAtTime(.1,t);g.gain.exponentialRampToValueAtTime(.001,t+.15);o.start(t);o.stop(t+.16);}}

// ---------- state ----------
const keys={};let mouse={x:W/2,y:H/2,down:false},paused=false,playing=false;
let player,wave,score,zombies,bullets,parts,pickups,projectiles,spawnQueue,waveTimer,shake,boss,gameTime,fireCd;
const BOSS_EVERY=5;
const MAG=12;let mag=MAG,reloading=0;
let p2=null,remote={x:0,y:0,ang:0},rem={};

function reset(){
 player={x:W/2,y:H/2,r:14,hp:100,maxhp:100,speed:4.2,ang:0,iframes:0,rapid:0,shotgun:0};
 wave=0;score=0;zombies=[];bullets=[];parts=[];pickups=[];projectiles=[];spawnQueue=[];waveTimer=90;shake=0;boss=null;gameTime=0;fireCd=0;
 mag=magSize;reloading=0;
 if(!net.isHost)p2=null;
 document.getElementById('bossbar').style.display='none';updHud();
}

// ---------- input ----------
addEventListener('keydown',e=>{keys[e.key.toLowerCase()]=true;if(e.key.toLowerCase()==='r')reload();if(e.key.toLowerCase()==='p'&&playing)paused=!paused;if(['arrowup','arrowdown','arrowleft','arrowright',' '].includes(e.key.toLowerCase()))e.preventDefault();});
addEventListener('keyup',e=>{keys[e.key.toLowerCase()]=false;});
cv.addEventListener('mousemove',e=>{mouse.x=e.clientX;mouse.y=e.clientY;});
cv.addEventListener('mousedown',e=>{mouse.down=true;if(AC&&AC.state==='suspended')AC.resume();});
addEventListener('mouseup',()=>{mouse.down=false;});
cv.addEventListener('contextmenu',e=>e.preventDefault());
// ---------- touch controls (phones) ----------
let touch={active:false,x:0,y:0};
cv.addEventListener('touchstart',e=>{e.preventDefault();const t=e.touches[0];touch.active=true;touch.x=t.clientX;touch.y=t.clientY;if(AC&&AC.state==='suspended')AC.resume();},{passive:false});
cv.addEventListener('touchmove',e=>{e.preventDefault();const t=e.touches[0];touch.x=t.clientX;touch.y=t.clientY;},{passive:false});
cv.addEventListener('touchend',e=>{e.preventDefault();touch.active=false;},{passive:false});
function autoAim(){
 let best=null,bd=1e9;
 if(boss){const d=Math.hypot(boss.x-player.x,boss.y-player.y);if(d<bd){bd=d;best=boss;}}
 for(const z of zombies){const d=Math.hypot(z.x-player.x,z.y-player.y);if(d<bd){bd=d;best=z;}}
 if(best)player.ang=Math.atan2(best.y-player.y,best.x-player.x);
 else player.ang=Math.atan2(touch.y-player.y,touch.x-player.x);
}
function aimNearestNet(){
 let best=null,bd=1e9;
 for(const z of (rem.zs||[])){const d=Math.hypot(z[0]-player.x,z[1]-player.y);if(d<bd){bd=d;best=z;}}
 if(rem.bo){const d=Math.hypot(rem.bo[0]-player.x,rem.bo[1]-player.y);if(d<bd){bd=d;best=rem.bo;}}
 if(best)player.ang=Math.atan2(best[1]-player.y,best[0]-player.x);
 else player.ang=Math.atan2(touch.y-player.y,touch.x-player.x);
}
if('ontouchstart' in window){const k=document.querySelector('.keys');if(k)k.textContent='touch and drag anywhere to move, it aims and fires for you. tap a button below to play';}

// ---------- weapons ----------
function reload(){if(reloading<=0&&mag<magSize){reloading=60;}}
const SPD=12;

function shoot(){
 const w=WEAPONS[wi];
 if(reloading>0)return;
 if(mag<=0){reload();return;}
 mag--;
 spawnShots(player,player.ang,w);
 sfx('shoot');fireCd=w.cd*(player.rapid>0?.6:1);
}

// ---------- enemies ----------
function spawnZombie(type){
 const side=Math.floor(Math.random()*4);let x,y;
 if(side===0){x=Math.random()*W;y=-40;}else if(side===1){x=Math.random()*W;y=H+40;}else if(side===2){x=-40;y=Math.random()*H;}else{x=W+40;y=Math.random()*H;}
 if(type==='runner'){zombies.push({x,y,type,hit:0,r:11,hp:26,sp:3.1,dmg:8,color:'#8f8',ci:1,score:15});}
 else if(type==='tank'){zombies.push({x,y,type,hit:0,r:22,hp:130,sp:1.1,dmg:22,color:'#4a4',ci:2,score:40});}
 else{zombies.push({x,y,type,hit:0,r:14,hp:48,sp:1.7,dmg:12,color:'#5a5',ci:0,score:10});}
}

function spawnBoss(){
 const n=Math.floor(wave/BOSS_EVERY);
 boss={x:-60,y:H/2,r:46+6*n,hp:600+350*n,maxhp:600+350*n,sp:1.5+.12*n,dmg:30,ang:0,hit:0,cd:120,name:['THE BUTCHER','ROT KING','GRAVE LORD','THE ABOMINATION','DEATHBRINGER'][Math.min(n-1,4)]+ (n>5?' MK.'+n:'')};
 document.getElementById('bossname').textContent=boss.name;
 document.getElementById('bossbar').style.display='block';
 banner('BOSS INCOMING');sfx('boss');
}

function banner(txt){const b=document.getElementById('banner');b.textContent=txt;b.classList.remove('show');void b.offsetWidth;b.classList.add('show');if(net.isHost&&net.open)send({t:'msg',x:txt});}

// ---------- particles ----------
function boom(x,y,color,n,spd){for(let i=0;i<n;i++){const a=Math.random()*Math.PI*2,s=Math.random()*spd;parts.push({x,y,vx:Math.cos(a)*s,vy:Math.sin(a)*s,life:20+Math.random()*20,color});}}

function dropPickup(x,y){
 if(Math.random()<.18){const kinds=['hp','rapid','shotgun'];pickups.push({x,y,kind:kinds[Math.floor(Math.random()*3)],t:600});}
}

// ---------- waves ----------
function nextWave(){
 wave++;
 if(wave%BOSS_EVERY===0){spawnBoss();return;}
 const n=Math.min(6+wave*3,40);banner('WAVE '+wave);
 for(let i=0;i<n;i++){let t='walker';if(wave>=3&&Math.random()<.25)t='runner';if(wave>=4&&Math.random()<.15)t='tank';spawnQueue.push({t,delay:i*14});}
 waveTimer=0;
}

// ---------- multiplayer (cloudflare relay) ----------
let MYUID=localStorage.getItem('zob_uid');
if(!MYUID){MYUID='p'+Math.random().toString(36).slice(2,9);localStorage.setItem('zob_uid',MYUID);}
const MYTAG='#'+MYUID.slice(1,7).toUpperCase();
const SRV='https://zombie-outbreak.ethancueto176-ace.workers.dev';let net={room:null,open:false,isHost:false,code:'',lastIn:0,lastOther:0,guestUid:'',hostUid:'',dead:false,ws:null};

function nstatus(t){const e=document.getElementById('netstatus');if(e)e.textContent=t;}
function makeCode(){const l='ABCDEFGHJKMNPQRSTUVWXYZ23456789';let c='';for(let i=0;i<4;i++)c+=l[Math.floor(Math.random()*l.length)];return c;}
function roomPath(c){return c;}
async function api(path,opts){const r=await fetch(SRV+'/api/'+path,opts);return r.json().catch(()=>({}));}
function wsSend(o){try{if(net.ws&&net.ws.readyState===1)net.ws.send(JSON.stringify(o));}catch(e){}}
function send(o){if(!net.ws)return;o.u=MYUID;wsSend({t:'ev',d:o});}
function openRoom(code,role){
 return new Promise((res,rej)=>{
  let done=false;const WSURL='wss://zombie-outbreak.ethancueto176-ace.workers.dev/ws';
  const ws=new WebSocket(WSURL+'?room='+encodeURIComponent(code)+'&uid='+encodeURIComponent(MYUID));
  net.ws=ws;
  const fail=r=>{if(done)return;done=true;try{ws.onclose=null;}catch(e){}try{ws.close();}catch(e){}net.ws=null;rej(r);};
  ws.onopen=()=>{ws.send(JSON.stringify({t:'join',role:role,uid:MYUID}));};
  ws.onmessage=ev=>{
   let m;try{m=JSON.parse(ev.data);}catch(e){return;}
   if(m.t==='joined'){if(!done){done=true;net.open=true;res(m);}}
   else if(m.t==='noroom'){fail('noroom');}
   else if(m.t==='full'){fail('full');}
   else if(m.t==='banned'){fail('banned');}
   else if(m.t==='meta'){onMeta(m.m);}
   else if(m.t==='ev'){net.lastIn++;net.lastOther=Date.now();onNet(m.d);}
   else if(m.t==='snap'){net.lastOther=Date.now();try{rem=JSON.parse(m.j);}catch(e){}}
  };
  ws.onclose=()=>{if(!done)fail('closed');net.ws=null;};
  ws.onerror=()=>{if(!done)fail('error');};
  setTimeout(()=>{if(!done)fail('timeout');},8000);
 });
}
function onMeta(m){
 if(!m)m={};
 if(net.isHost){
  if(m.g&&m.g!==MYUID&&net.guestUid!==m.g){net.guestUid=m.g;addP2();nstatus('friend joined! ('+('#'+m.g.slice(1,7).toUpperCase())+')');if(playing)pushStart(true);}
  if(m.g&&Date.now()-(m.gp||0)>12000&&net.open&&playing){nstatus('friend lost connection...');}
 }else{
  net.hostUid=m.h||net.hostUid;
  if(m.st==='p'&&!playing&&!net.dead){
   net.open=true;reset();document.getElementById('overlay').style.display='none';playing=true;banner('CO-OP START');
  }
  if(net.open&&Date.now()-(m.hp||0)>12000){
   if(playing){playing=false;showOverlay('CONNECTION LOST','The host left the game.','PLAY SOLO');}
   else nstatus('host went away, try again');
   leaveRoom();
  }
 }
}
function pushStart(quiet){
 wsSend({t:'start'});
 if(!quiet){reset();document.getElementById('overlay').style.display='none';playing=true;nextWave();}
}
async function hostGame(){
 if(bannedMe){nstatus('you are banned');return;}
 net.isHost=true;net.dead=false;net.code=makeCode();net.open=false;net.guestUid='';net.lastIn=0;
 nstatus('making room '+net.code+'...');
 try{
  await openRoom(net.code,'host');
  net.lastOther=Date.now();
  nstatus('room code: '+net.code+'. tell your friend to join with it, then hit SOLO GAME to start');
 }catch(e){net.isHost=false;net.open=false;nstatus(e==='banned'?'you are banned from this game':'room error, try again');}
}
async function joinGame(code){
 if(bannedMe){nstatus('you are banned');return;}
 code=(code||'').trim().toUpperCase();
 if(code.length<4){nstatus('type the 4-letter room code first');return;}
 net.isHost=false;net.dead=false;nstatus('joining '+code+'...');
 try{
  const b=await api('banned/'+MYUID);
  if(b.banned){nstatus('you are banned from this game');return;}
  await openRoom(code,'guest');
  net.code=code;net.lastIn=0;
  send({t:'hello'});
  nstatus('connected! waiting for the host to start...');
 }catch(e){
  nstatus(e==='full'?'room is full':(e==='noroom'?'no room with that code':(e==='banned'?'you are banned from this game':'could not join, try again')));
 }
}
function leaveRoom(){
 try{if(net.ws){net.ws.onclose=null;net.ws.close();}}catch(e){}
 net.ws=null;net.open=false;
}
function addP2(){p2={x:player.x+40,y:player.y,r:14,hp:100,maxhp:100,iframes:60,rapid:0,shotgun:0,ang:0};}

function onNet(d){
 if(!d||typeof d!=='object')return;
 if(net.isHost){
  if(d.t==='hello'&&!net.guestUid){/* wait for meta */}
  else if(d.t==='sh'&&p2){const w=WEAPONS[Math.min(d.w||0,WEAPONS.length-1)];spawnShots(p2,d.a,w);sfx('shoot');}
  else if(d.t==='gin'&&p2){try{const g=JSON.parse(d.j);p2.x=g.x;p2.y=g.y;p2.ang=g.a;}catch(e){}}
 }else{
  if(d.t==='start'){/* handled by meta st */}
  else if(d.t==='msg'){banner(d.x);}
  else if(d.t==='go'){net.dead=true;leaveRoom();playing=false;showOverlay('YOU DIED','You survived '+d.w+' waves with a score of '+d.sc+'. The horde always comes back.','PLAY SOLO');}
 }
}

function sendSnap(){
 const ZC=['#ff5','#f80','#f84'];
 const zs=[];for(const z of zombies)zs.push([Math.round(z.x),Math.round(z.y),z.r,z.hit>0?1:0,z.ci]);
 const bs=[];for(const b of bullets)bs.push([Math.round(b.x),Math.round(b.y),b.r,b.c===undefined?0:ZC.indexOf(b.c)<0?0:ZC.indexOf(b.c)]);
 const pr=[];for(const p of projectiles)pr.push([Math.round(p.x),Math.round(p.y)]);
 const pk=[];for(const p of pickups)pk.push([Math.round(p.x),Math.round(p.y),p.kind==='hp'?0:p.kind==='rapid'?1:2]);
 try{wsSend({t:'snap',j:JSON.stringify({w:wave,sc:score,me:{x:Math.round(player.x),y:Math.round(player.y),ang:Math.round(player.ang*100)/100},p2:p2?{x:Math.round(p2.x),y:Math.round(p2.y),hp:Math.max(0,p2.hp),rapid:p2.rapid>0?1:0,shotgun:p2.shotgun>0?1:0}:null,zs:zs,bs:bs,pr:pr,pk:pk,bo:boss?[Math.round(boss.x),Math.round(boss.y),boss.r,Math.round(boss.hp/boss.maxhp*100)/100,boss.name]:null})});}catch(e){}
}

// ---------- owner / bans / secret weapons ----------
function ph(s){let h=5381;for(let i=0;i<s.length;i++)h=(((h<<5)+h)+s.charCodeAt(i))>>>0;return 'o'+h.toString(36);}
let isOwner=localStorage.getItem('zob_owner')==='1';
function swOn(){return isOwner&&localStorage.getItem('zob_sw')==='1';}
function openOwner(){
 if(playing)paused=true;
 document.getElementById('ownerp').style.display='flex';
 document.getElementById('pinmsg').textContent='';
 const tools=document.getElementById('ownertools');
 tools.style.display=isOwner?'block':'none';
 document.getElementById('pinrow').style.display=isOwner?'none':'flex';
 if(!isOwner){
  api('owners').then(j=>{
   const v=j.owners||{};
   document.getElementById('pinmsg').textContent=(v&&Object.keys(v).length)?'type the owner pin':'no owner yet: type a pin to claim it';
  }).catch(()=>{});
 }else renderBans();
}
function closeOwner(){
 document.getElementById('ownerp').style.display='none';
 if(paused)paused=false;
}
function tryPin(){
 const pin=document.getElementById('pinin').value;
 if(!pin){document.getElementById('pinmsg').textContent='type a pin first';return;}
 const h=ph(pin);
 api('owners').then(async j=>{
  const v=j.owners||{};
  const n=Object.keys(v).length;
  if(n===0||v[h]){
   if(n===0&&!v[h])await api('owner/add',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({h:h})});
   isOwner=true;localStorage.setItem('zob_owner','1');
   document.getElementById('pinmsg').textContent=(n===0)?'you claimed owner!':'welcome back, owner';
   setTimeout(()=>{openOwnerRefresh();},400);
  }else document.getElementById('pinmsg').textContent='wrong pin';
 }).catch(()=>document.getElementById('pinmsg').textContent='no connection yet');
}
function openOwnerRefresh(){
 const tools=document.getElementById('ownertools');
 tools.style.display=isOwner?'block':'none';
 document.getElementById('pinrow').style.display=isOwner?'none':'flex';
 document.getElementById('pinin').value='';
 updSwBtn();renderBans();
}
function updSwBtn(){document.getElementById('swbtn').textContent='SECRET WEAPONS: '+(localStorage.getItem('zob_sw')==='1'?'ON':'OFF');}
function toggleSw(){
 if(!isOwner)return;
 const on=localStorage.getItem('zob_sw')==='1';
 if(on){localStorage.setItem('zob_sw','0');document.getElementById('weapbtn').style.display='none';}
 else localStorage.setItem('zob_sw','1');
 updSwBtn();
}
function addOwner(){
 const pin=document.getElementById('addin').value;
 if(!pin)return;
 api('owner/add',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({h:ph(pin)})});
 document.getElementById('addin').value='';
 document.getElementById('pinmsg').textContent='owner added';
}
async function renderBans(){
 if(!isOwner)return;
 const el=document.getElementById('banlist');
 if(!el.dataset.boot){el.dataset.boot=1;el.innerHTML='<div id="ownl"></div><div id="banl"></div>';}
 const ownl=document.getElementById('ownl'),banl=document.getElementById('banl');
 const oj=await api('owners').catch(()=>({})),bj=await api('bans').catch(()=>({}));
 const ov=oj.owners||{},bv=bj.bans||{};
 const ks=Object.keys(ov);
 let h='OWNERS ('+ks.length+'):'+(ks.length?'':' none');
 for(const k of ks)h+='<br>pin '+k.slice(1,5)+' <button data-unown="'+k+'">REMOVE</button>';
 ownl.innerHTML=h;
 ownl.querySelectorAll('button').forEach(b=>b.addEventListener('click',async()=>{
  await api('owner/remove',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({h:b.dataset.unown})});
  document.getElementById('pinmsg').textContent='owner removed';renderBans();
 }));
 let html='<br>BANNED IDS:';
 const bks=Object.keys(bv);
 if(!bks.length)html+=' none';
 else for(const k of bks)html+='<br>#'+k.slice(1,7).toUpperCase()+' <button data-un="'+k+'">UNBAN</button>';
 if(net.isHost&&net.guestUid)html+='<br>PLAYER HERE: '+('#'+net.guestUid.slice(1,7).toUpperCase())+' <button data-ban="'+net.guestUid+'">BAN</button>';
 if(!net.isHost&&net.hostUid)html+='<br>PLAYER HERE: '+('#'+net.hostUid.slice(1,7).toUpperCase())+' <button data-ban="'+net.hostUid+'">BAN</button>';
 banl.innerHTML=html;
 banl.querySelectorAll('button').forEach(b=>b.addEventListener('click',async()=>{
  if(b.dataset.ban){await api('ban/set',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({uid:b.dataset.ban})});document.getElementById('pinmsg').textContent='banned '+('#'+b.dataset.ban.slice(1,7).toUpperCase());renderBans();}
  else if(b.dataset.un){await api('ban/clear',{method:'POST',headers:{'Content-Type':'application/json'},body:JSON.stringify({uid:b.dataset.un})});document.getElementById('pinmsg').textContent='unbanned '+('#'+b.dataset.un.slice(1,7).toUpperCase());renderBans();}
 }));
}
let bannedMe=false;
function showBanned(){
 bannedMe=true;
 showOverlay('YOU WERE BANNED','The owner banned your player id. Your id is '+MYTAG+'. You cannot play until the owner unbans you.','BANNED');
}
let banPoll=null;
function watchBanMe(){
 if(banPoll)return;
 banPoll=setInterval(()=>{
  api('banned/'+MYUID).then(j=>{
   if(j.banned&&!bannedMe){
    playing=false;paused=false;
    leaveRoom();closeOwner();showBanned();
   }
  }).catch(()=>{});
 },5000);
}

// ---------- weapons ----------
const WEAPONS=[
 {n:'PISTOL',mag:12,cd:10,dmg:34,spread:.06,bs:4,c:'#ff5'},
 {n:'MINIGUN',mag:180,cd:3,dmg:7,spread:.15,bs:3.5,c:'#5ff'},
 {n:'ROCKET',mag:10,cd:45,dmg:30,bs:7,c:'#f84',rok:1},
 {n:'FLAMER',mag:320,cd:2,dmg:1.7,range:130,arc:.4,c:'#f80',fl:1}
];
let wi=0,magSize=WEAPONS[0].mag;
function spawnShots(pl,ang,w){
 const px=pl.x+Math.cos(ang)*18,py=pl.y+Math.sin(ang)*18;
 if(w.fl){
  for(let i=0;i<3;i++){const a=ang+(Math.random()-.5)*w.arc*2;const s=w.range*(.55+Math.random()*.5);bullets.push({x:px,y:py,vx:Math.cos(a)*s/13,vy:Math.sin(a)*s/13,r:6,life:13,dmg:w.dmg,c:w.c,fl:1});}
 }else if(w.rok){
  bullets.push({x:px,y:py,vx:Math.cos(ang)*w.bs,vy:Math.sin(ang)*w.bs,r:7,life:90,dmg:w.dmg,c:w.c,rok:1});
 }else{
  const sh=(pl.shotgun>0&&w.n==='PISTOL')?5:1;
  for(let i=0;i<sh;i++){const sp=(pl.shotgun>0&&w.n==='PISTOL')?(i-2)*.12:(Math.random()-.5)*w.spread;bullets.push({x:px,y:py,vx:Math.cos(ang+sp)*SPD,vy:Math.sin(ang+sp)*SPD,r:w.bs,life:60,dmg:w.dmg,c:w.c});}
 }
}
function cycleWeapon(){
 if(!swOn())return;
 setWeapon((wi+1)%WEAPONS.length);
}
function setWeapon(i){
 wi=i;const w=WEAPONS[i];magSize=w.mag;mag=w.mag;reloading=0;fireCd=0;
 const btn=document.getElementById('weapbtn');if(btn){btn.textContent=w.n;btn.style.display=(swOn()&&playing)?'block':'none';}
 updHud();
}
function rocketBoom(x,y){
 boom(x,y,'#f84',26,7);shake=Math.max(shake,9);const R=55;
 if(boss&&Math.hypot(boss.x-x,boss.y-y)<R+boss.r){boss.hp-=30;boss.hit=8;
  if(boss.hp<=0){score+=500*Math.floor(wave/BOSS_EVERY);boom(boss.x,boss.y,'#f44',80,7);shake=18;banner('BOSS DOWN');document.getElementById('bossbar').style.display='none';boss=null;sfx('boss');}}
 for(let j=zombies.length-1;j>=0;j--){const z=zombies[j];if(Math.hypot(z.x-x,z.y-y)<R+z.r){z.hp-=30;z.hit=6;
  if(z.hp<=0){score+=z.score;boom(z.x,z.y,'#6a6',18,4);dropPickup(z.x,z.y);zombies.splice(j,1);sfx('hit');}}}
}

function showOverlay(h1,story,btn){
 document.getElementById('overlay').style.display='flex';
 document.getElementById('overlay').querySelector('h1').textContent=h1;
 document.getElementById('story').textContent=story;
 document.getElementById('startbtn').textContent=btn;
}

// ---------- hud ----------
function updHud(){
 const cm=net.open&&!net.isHost;
 document.getElementById('wave').textContent=cm?(rem.w||0):wave;
 document.getElementById('score').textContent=cm?(rem.sc||0):score;
 const hp=cm?(rem.p2?rem.p2.hp:100):player.hp;
 const f=document.getElementById('hpfill');f.style.width=Math.max(0,hp/player.maxhp*100)+'%';
 document.getElementById('ammo').textContent=reloading>0?'...':mag+'/'+magSize;
 document.getElementById('buff').textContent=cm?'':((swOn()?WEAPONS[wi].n+' ':'')+(player.rapid>0?'RAPID FIRE ':'')+(player.shotgun>0?'SHOTGUN ':''));
}

function update(){
 if(!playing||paused)return;
 gameTime++;shake*=.9;
 if(gameTime%240===0)wsSend({t:'hb'});
 if(gameTime%30===0){const wb=document.getElementById('weapbtn');if(wb)wb.style.display=(swOn()&&playing)?'block':'none';const bb=document.getElementById('banbtn');if(bb)bb.style.display=(isOwner&&net.open&&playing)?'block':'none';}
 let dx=0,dy=0;
 if(keys['w']||keys['arrowup'])dy--;if(keys['s']||keys['arrowdown'])dy++;
 if(keys['a']||keys['arrowleft'])dx--;if(keys['d']||keys['arrowright'])dx++;
 if(dx||dy){const l=Math.hypot(dx,dy);player.x+=dx/l*player.speed;player.y+=dy/l*player.speed;}
 if(touch.active){const tx=touch.x-player.x,ty=touch.y-player.y,td=Math.hypot(tx,ty);if(td>10){player.x+=tx/td*player.speed;player.y+=ty/td*player.speed;}}
 player.x=Math.max(player.r,Math.min(W-player.r,player.x));player.y=Math.max(player.r,Math.min(H-player.r,player.y));
 if(player.iframes>0)player.iframes--;if(player.rapid>0)player.rapid--;if(player.shotgun>0)player.shotgun--;
 const cm=net.open&&!net.isHost;
 if(cm){
  if(touch.active)aimNearestNet();else player.ang=Math.atan2(mouse.y-player.y,mouse.x-player.x);
  if((mouse.down||touch.active)&&fireCd<=0){
   if(mag>0){mag--;send({t:'sh',a:player.ang,w:wi});sfx('shoot');fireCd=WEAPONS[wi].cd*(player.rapid>0?.6:1);}
   else reload();
  }
  if(fireCd>0)fireCd--;
  if(reloading>0){reloading--;if(reloading<=0)mag=magSize;}
  if(rem.p2){if(rem.p2.rapid)player.rapid=1;if(rem.p2.shotgun)player.shotgun=1;}
  if(gameTime%4===0&&net.open&&!net.isHost)wsSend({t:'gin',j:JSON.stringify({x:Math.round(player.x),y:Math.round(player.y),a:player.ang})});
 }else{
  if(touch.active){autoAim();if(fireCd<=0)shoot();}
  else{player.ang=Math.atan2(mouse.y-player.y,mouse.x-player.x);if(mouse.down&&fireCd<=0)shoot();}
  if(fireCd>0)fireCd--;
  if(reloading>0){reloading--;if(reloading<=0)mag=magSize;}
  hostSim();
  if(net.isHost&&net.open&&gameTime%4===0)sendSnap();
 }
 for(let i=parts.length-1;i>=0;i--){const p=parts[i];p.x+=p.vx;p.y+=p.vy;p.vx*=.92;p.vy*=.92;p.life--;if(p.life<=0)parts.splice(i,1);}
 updHud();
}

function nearestPl(x,y){let t=player,bd=Math.hypot(player.x-x,player.y-y);if(p2){const d=Math.hypot(p2.x-x,p2.y-y);if(d<bd){bd=d;t=p2;}}return t;}

function hostSim(){
 if(!boss&&zombies.length===0&&spawnQueue.length===0){waveTimer++;if(waveTimer>140)nextWave();}
 for(let i=spawnQueue.length-1;i>=0;i--){spawnQueue[i].delay--;if(spawnQueue[i].delay<=0){spawnZombie(spawnQueue[i].t);spawnQueue.splice(i,1);}}
 // bullets
 for(let i=bullets.length-1;i>=0;i--){const b=bullets[i];b.x+=b.vx;b.y+=b.vy;b.life--;
  if(b.life<=0||b.x<-20||b.x>W+20||b.y<-20||b.y>H+20){if(b.rok)rocketBoom(b.x,b.y);bullets.splice(i,1);continue;}
  let hit=false;
  if(boss){const d=Math.hypot(b.x-boss.x,b.y-boss.y);if(d<boss.r){boss.hp-=b.dmg;boss.hit=8;boom(b.x,b.y,'#a33',4,3);hit=true;
    if(boss.hp<=0){score+=500*Math.floor(wave/BOSS_EVERY);boom(boss.x,boss.y,'#f44',80,7);shake=18;banner('BOSS DOWN');document.getElementById('bossbar').style.display='none';boss=null;sfx('boss');}}}
  if(!hit)for(let j=zombies.length-1;j>=0;j--){const z=zombies[j];const d=Math.hypot(b.x-z.x,b.y-z.y);
   if(d<z.r+b.r){z.hp-=b.dmg;z.hit=6;boom(b.x,b.y,'#a44',5,4);hit=true;
    if(z.hp<=0){score+=z.score;boom(z.x,z.y,'#6a6',18,4);dropPickup(z.x,z.y);zombies.splice(j,1);sfx('hit');}
    break;}}
  if(hit){if(b.rok)rocketBoom(b.x,b.y);bullets.splice(i,1);}}
 // boss
 if(boss){if(boss.hit>0)boss.hit--;const t=nearestPl(boss.x,boss.y);const d=Math.hypot(t.x-boss.x,t.y-boss.y);boss.ang=Math.atan2(t.y-boss.y,t.x-boss.x);
  if(d>boss.r+t.r+6){boss.x+=Math.cos(boss.ang)*boss.sp;boss.y+=Math.sin(boss.ang)*boss.sp;}
  boss.cd--;if(boss.cd<=0&&d<560){boss.cd=Math.max(50,130-wave);const a=Math.atan2(t.y-boss.y,t.x-boss.x);
   for(let k=-1;k<=1;k++)projectiles.push({x:boss.x,y:boss.y,vx:Math.cos(a+k*.25)*5.5,vy:Math.sin(a+k*.25)*5.5,r:8,life:180});
   sfx('hit');}
  document.getElementById('bossfill').style.width=Math.max(0,boss.hp/boss.maxhp*100)+'%';
  const dd=Math.hypot(player.x-boss.x,player.y-boss.y);
  if(dd<boss.r+player.r&&player.iframes<=0){hurt(boss.dmg);player.x+=(player.x-boss.x)/dd*22;player.y+=(player.y-boss.y)/dd*22;}
  if(p2){const d2=Math.hypot(p2.x-boss.x,p2.y-boss.y);if(d2<boss.r+p2.r&&p2.iframes<=0){hurt2(boss.dmg);p2.x+=(p2.x-boss.x)/d2*22;p2.y+=(p2.y-boss.y)/d2*22;}}}
 // projectiles
 for(let i=projectiles.length-1;i>=0;i--){const p=projectiles[i];p.x+=p.vx;p.y+=p.vy;p.life--;
  if(p.life<=0||p.x<-30||p.x>W+30||p.y<-30||p.y>H+30){projectiles.splice(i,1);continue;}
  if(Math.hypot(p.x-player.x,p.y-player.y)<p.r+player.r&&player.iframes<=0){hurt(14);projectiles.splice(i,1);boom(p.x,p.y,'#f84',8,3);continue;}
  if(p2&&Math.hypot(p.x-p2.x,p.y-p2.y)<p.r+p2.r&&p2.iframes<=0){hurt2(14);projectiles.splice(i,1);boom(p.x,p.y,'#f84',8,3);}}
 // zombies
 for(let i=zombies.length-1;i>=0;i--){const z=zombies[i];if(z.hit>0)z.hit--;
  const t=nearestPl(z.x,z.y);const a=Math.atan2(t.y-z.y,t.x-z.x);z.x+=Math.cos(a)*z.sp;z.y+=Math.sin(a)*z.sp;
  const d=Math.hypot(z.x-player.x,z.y-player.y);
  if(d<z.r+player.r&&player.iframes<=0){hurt(z.dmg);zombies.splice(i,1);boom(player.x,player.y,'#a55',10,4);continue;}
  if(p2&&Math.hypot(z.x-p2.x,z.y-p2.y)<z.r+p2.r&&p2.iframes<=0){hurt2(z.dmg);zombies.splice(i,1);boom(p2.x,p2.y,'#a55',10,4);}}
 // pickups
 for(let i=pickups.length-1;i>=0;i--){const p=pickups[i];p.t--;
  if(p.t<=0){pickups.splice(i,1);continue;}
  let taken=false;
  if(Math.hypot(p.x-player.x,p.y-player.y)<24){sfx('pick');applyPickup(player,p.kind);taken=true;}
  else if(p2&&Math.hypot(p.x-p2.x,p.y-p2.y)<24){sfx('pick');applyPickup(p2,p.kind);taken=true;}
  if(taken){boom(p.x,p.y,'#ff5',12,3);pickups.splice(i,1);}}
}

function applyPickup(pl,kind){
 if(kind==='hp')pl.hp=Math.min(pl.maxhp,pl.hp+35);
 else if(kind==='rapid')pl.rapid=480;
 else pl.shotgun=420;
}

function hurt(d){player.hp-=d;player.iframes=36;shake=10;sfx('hurt');if(player.hp<=0){endGame();}}
function hurt2(d){if(!p2)return;p2.hp-=d;p2.iframes=36;sfx('hurt');if(p2.hp<=0){endGame();}}
function endGame(){
 if(!playing)return;playing=false;
 if(net.isHost&&net.open)send({t:'go',w:wave,sc:score});
 gameOver();
}

// ---------- draw ----------
function draw(){
 ctx.setTransform(1,0,0,1,0,0);
 ctx.fillStyle='#0a0a0f';ctx.fillRect(0,0,W,H);
 ctx.strokeStyle='rgba(40,70,40,.25)';ctx.lineWidth=1;
 for(let x=((-gameTime*.4)%60+60)%60;x<W;x+=60){ctx.beginPath();ctx.moveTo(x,0);ctx.lineTo(x,H);ctx.stroke();}
 for(let y=((-gameTime*.4)%60+60)%60;y<H;y+=60){ctx.beginPath();ctx.moveTo(0,y);ctx.lineTo(W,y);ctx.stroke();}
 const sx=(Math.random()-.5)*shake,sy=(Math.random()-.5)*shake;ctx.translate(sx,sy);
 const cm=net.open&&!net.isHost;
 if(cm)drawNet();else drawLocal();
 ctx.setTransform(1,0,0,1,0,0);
 if(paused&&playing){ctx.fillStyle='rgba(0,0,0,.6)';ctx.fillRect(0,0,W,H);ctx.fillStyle='#cfc';ctx.font='40px monospace';ctx.textAlign='center';ctx.fillText('PAUSED',W/2,H/2);}
}

function drawLocal(){
 for(const p of pickups){const c=p.kind==='hp'?'#f55':p.kind==='rapid'?'#ff5':'#5af';ctx.globalAlpha=p.t<90?(p.t/90):1;
  ctx.fillStyle=c;ctx.beginPath();ctx.arc(p.x,p.y,10,0,7);ctx.fill();ctx.fillStyle='#050';ctx.font='bold 11px monospace';ctx.textAlign='center';ctx.fillText(p.kind==='hp'?'+':p.kind==='rapid'?'R':'S',p.x,p.y+4);ctx.globalAlpha=1;}
 for(const p of parts){ctx.globalAlpha=Math.max(0,p.life/40);ctx.fillStyle=p.color;ctx.fillRect(p.x-2,p.y-2,4,4);}ctx.globalAlpha=1;
 for(const z of zombies){ctx.fillStyle=z.hit>0?'#fff':z.color;ctx.beginPath();ctx.arc(z.x,z.y,z.r,0,7);ctx.fill();
  ctx.fillStyle='#111';ctx.beginPath();ctx.arc(z.x-4,z.y-4,2.5,0,7);ctx.arc(z.x+4,z.y-4,2.5,0,7);ctx.fill();}
 if(boss){ctx.fillStyle=boss.hit>0?'#fff':'#b33';ctx.beginPath();ctx.arc(boss.x,boss.y,boss.r,0,7);ctx.fill();
  ctx.fillStyle='#111';ctx.beginPath();ctx.arc(boss.x-12,boss.y-10,6,0,7);ctx.arc(boss.x+12,boss.y-10,6,0,7);ctx.fill();
  ctx.strokeStyle='#f66';ctx.lineWidth=3;ctx.beginPath();ctx.arc(boss.x,boss.y,boss.r+8,0,7);ctx.stroke();}
 for(const p of projectiles){ctx.fillStyle='#f84';ctx.beginPath();ctx.arc(p.x,p.y,p.r,0,7);ctx.fill();}
 if(player){ctx.fillStyle=player.iframes>0&&(gameTime%6<3)?'#fff':'#7df';
  ctx.beginPath();ctx.arc(player.x,player.y,player.r,0,7);ctx.fill();
  ctx.strokeStyle='#7df';ctx.lineWidth=4;ctx.beginPath();ctx.moveTo(player.x,player.y);ctx.lineTo(player.x+Math.cos(player.ang)*24,player.y+Math.sin(player.ang)*24);ctx.stroke();}
 if(p2){ctx.fillStyle=p2.iframes>0&&(gameTime%6<3)?'#fff':'#f7a';
  ctx.beginPath();ctx.arc(p2.x,p2.y,p2.r,0,7);ctx.fill();
  ctx.strokeStyle='#f7a';ctx.lineWidth=4;ctx.beginPath();ctx.moveTo(p2.x,p2.y);ctx.lineTo(p2.x+Math.cos(p2.ang)*24,p2.y+Math.sin(p2.ang)*24);ctx.stroke();}
 for(const b of bullets){ctx.fillStyle=b.c||'#ff5';if(b.fl)ctx.globalAlpha=.75;ctx.beginPath();ctx.arc(b.x,b.y,b.r,0,7);ctx.fill();ctx.globalAlpha=1;}
}

function drawNet(){
 const ZC=['#5a5','#8f8','#4a4'];
 for(const p of rem.pk||[]){const c=p[2]===0?'#f55':p[2]===1?'#ff5':'#5af';ctx.fillStyle=c;ctx.beginPath();ctx.arc(p[0],p[1],10,0,7);ctx.fill();}
 for(const p of parts){ctx.globalAlpha=Math.max(0,p.life/40);ctx.fillStyle=p.color;ctx.fillRect(p.x-2,p.y-2,4,4);}ctx.globalAlpha=1;
 for(const z of rem.zs||[]){ctx.fillStyle=z[3]?'#fff':ZC[z[4]||0];ctx.beginPath();ctx.arc(z[0],z[1],z[2],0,7);ctx.fill();
  ctx.fillStyle='#111';ctx.beginPath();ctx.arc(z[0]-4,z[1]-4,2.5,0,7);ctx.arc(z[0]+4,z[1]-4,2.5,0,7);ctx.fill();}
 if(rem.bo){ctx.fillStyle='#b33';ctx.beginPath();ctx.arc(rem.bo[0],rem.bo[1],rem.bo[2],0,7);ctx.fill();
  ctx.strokeStyle='#f66';ctx.lineWidth=3;ctx.beginPath();ctx.arc(rem.bo[0],rem.bo[1],rem.bo[2]+8,0,7);ctx.stroke();
  document.getElementById('bossname').textContent=rem.bo[4];document.getElementById('bossbar').style.display='block';document.getElementById('bossfill').style.width=Math.max(0,rem.bo[3]*100)+'%';}
 else document.getElementById('bossbar').style.display='none';
 for(const p of rem.pr||[]){ctx.fillStyle='#f84';ctx.beginPath();ctx.arc(p[0],p[1],8,0,7);ctx.fill();}
 const NC=['#ff5','#f80','#f84'];for(const b of rem.bs||[]){ctx.fillStyle=NC[b[3]||0];ctx.beginPath();ctx.arc(b[0],b[1],b[2]||4,0,7);ctx.fill();}
 if(rem.me){ctx.fillStyle='#7df';ctx.beginPath();ctx.arc(rem.me.x,rem.me.y,14,0,7);ctx.fill();
  ctx.strokeStyle='#7df';ctx.lineWidth=4;ctx.beginPath();ctx.moveTo(rem.me.x,rem.me.y);ctx.lineTo(rem.me.x+Math.cos(rem.me.ang)*24,rem.me.y+Math.sin(rem.me.ang)*24);ctx.stroke();}
 if(player){ctx.fillStyle='#f7a';ctx.beginPath();ctx.arc(player.x,player.y,player.r,0,7);ctx.fill();
  ctx.strokeStyle='#f7a';ctx.lineWidth=4;ctx.beginPath();ctx.moveTo(player.x,player.y);ctx.lineTo(player.x+Math.cos(player.ang)*24,player.y+Math.sin(player.ang)*24);ctx.stroke();}
}

function loop(){try{update();draw();}catch(e){}requestAnimationFrame(loop);}
reset();
requestAnimationFrame(loop);

function gameOver(){
 showOverlay('YOU DIED','You survived '+wave+' wave'+(wave===1?'':'s')+' with a score of '+score+'. The horde always comes back.','PLAY AGAIN');
}

document.getElementById('startbtn').addEventListener('click',()=>{
 if(bannedMe){showBanned();return;}
 if(net.open&&!net.isHost){nstatus('wait for the host to start the game');return;}
 if(net.isHost&&net.open){pushStart(false);return;}
 reset();document.getElementById('overlay').style.display='none';playing=true;nextWave();
});
document.getElementById('hostbtn').addEventListener('click',hostGame);
document.getElementById('joinbtn').addEventListener('click',()=>{document.getElementById('joinrow').style.display='flex';document.getElementById('codein').focus();});
document.getElementById('joingo').addEventListener('click',()=>joinGame(document.getElementById('codein').value));
document.getElementById('codein').addEventListener('keydown',e=>{if(e.key==='Enter')joinGame(e.target.value);});
document.getElementById('ownerbtn').addEventListener('click',openOwner);
document.getElementById('pinok').addEventListener('click',tryPin);
document.getElementById('pinin').addEventListener('keydown',e=>{if(e.key==='Enter')tryPin();});
document.getElementById('addok').addEventListener('click',addOwner);
document.getElementById('swbtn').addEventListener('click',toggleSw);
document.getElementById('ownerback').addEventListener('click',closeOwner);
document.getElementById('weapbtn').addEventListener('click',cycleWeapon);
document.getElementById('banbtn').addEventListener('click',openOwner);
addEventListener('keydown',e=>{if(e.key.toLowerCase()==='q')cycleWeapon();});
watchBanMe();
</script>
</body>
</html>
