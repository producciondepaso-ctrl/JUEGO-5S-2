<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>Juego 5S — Panadería Industrial</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }
  body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; background: #f5f4f0; min-height: 100vh; padding: 12px; }
  h1 { font-size: 16px; font-weight: 600; color: #1a1a1a; margin-bottom: 2px; }
  .subtitle { font-size: 12px; color: #888; margin-bottom: 10px; }

  #scorebar { display: flex; gap: 8px; margin-bottom: 10px; }
  .scard { background: #fff; border-radius: 10px; padding: 8px 10px; flex: 1; border: 1px solid #e8e6e0; }
  .scard-label { font-size: 10px; color: #999; text-transform: uppercase; letter-spacing: 0.04em; }
  .scard-val { font-size: 18px; font-weight: 600; color: #1a1a1a; }

  #progress { display: flex; gap: 5px; margin-bottom: 10px; align-items: center; }
  .prog-dot { width: 10px; height: 10px; border-radius: 50%; background: #ddd; transition: background 0.3s; }
  .prog-dot.done { background: #1D9E75; }
  .prog-dot.current { background: #378ADD; }

  #phase-banner { background: #e8f2fc; border-radius: 10px; padding: 10px 13px; margin-bottom: 8px; border-left: 3px solid #378ADD; }
  #phase-title { font-size: 14px; font-weight: 600; color: #185FA5; }
  #phase-desc { font-size: 12px; color: #378ADD; margin-top: 2px; }

  #instruction { background: #fff; border-radius: 10px; padding: 9px 12px; margin-bottom: 10px; font-size: 12px; color: #555; border: 1px solid #e8e6e0; }

  #arena { position: relative; width: 100%; background: #fff; border-radius: 14px; border: 1px solid #e8e6e0; overflow: hidden; touch-action: none; }

  .zone { position: absolute; border-radius: 10px; border: 2px dashed transparent; transition: border-color 0.15s, background 0.15s; }
  .zone.hover-drop { border-color: #378ADD !important; background: rgba(55,138,221,0.10) !important; }
  .zone-label { position: absolute; bottom: 5px; left: 0; right: 0; font-size: 9px; font-weight: 600; text-align: center; pointer-events: none; text-transform: uppercase; letter-spacing: 0.03em; }

  .item { position: absolute; cursor: grab; border-radius: 10px; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 2px; padding: 5px 4px; border: 1.5px solid #e0ddd6; background: #fff; z-index: 10; width: 72px; height: 62px; box-shadow: 0 1px 4px rgba(0,0,0,0.08); transition: box-shadow 0.1s; }
  .item.dragging { opacity: 0.6; box-shadow: 0 6px 18px rgba(0,0,0,0.18); z-index: 30; }
  .item-icon { font-size: 20px; pointer-events: none; line-height: 1; }
  .item-name { font-size: 9px; text-align: center; color: #666; pointer-events: none; max-width: 64px; line-height: 1.2; }

  #bottom-bar { margin-top: 10px; display: flex; align-items: center; gap: 8px; }
  #status-msg { font-size: 12px; color: #888; flex: 1; }
  #verify-btn { padding: 10px 18px; border-radius: 10px; border: none; background: #185FA5; color: #fff; font-size: 13px; font-weight: 600; cursor: pointer; display: none; white-space: nowrap; }
  #verify-btn:active { background: #0c447c; }

  #phase-result { display: none; margin-top: 10px; border-radius: 10px; padding: 11px 14px; font-size: 13px; font-weight: 500; }
  #phase-result.ok { background: #E1F5EE; color: #0F6E56; border: 1px solid #5DCAA5; }
  #phase-result.err { background: #FCEBEB; color: #A32D2D; border: 1px solid #F09595; }

  #next-btn { display: none; margin-top: 10px; width: 100%; padding: 13px; border-radius: 10px; border: none; background: #1D9E75; color: #fff; font-size: 14px; font-weight: 600; cursor: pointer; }
  #next-btn:active { background: #0F6E56; }

  #result-screen { display: none; padding: 2rem 1rem; text-align: center; }
  .result-emoji { font-size: 56px; margin-bottom: 12px; }
  #result-title { font-size: 24px; font-weight: 700; color: #1a1a1a; margin-bottom: 8px; }
  #result-body { font-size: 14px; color: #666; margin-bottom: 20px; line-height: 1.5; }
  #result-score { font-size: 38px; font-weight: 700; color: #185FA5; margin-bottom: 24px; }
  #result-details { background: #fff; border-radius: 12px; padding: 14px; margin-bottom: 20px; border: 1px solid #e8e6e0; text-align: left; }
  .result-row { display: flex; justify-content: space-between; font-size: 13px; padding: 5px 0; border-bottom: 1px solid #f0ede8; }
  .result-row:last-child { border-bottom: none; }
  .result-row span:first-child { color: #888; }
  .result-row span:last-child { font-weight: 600; color: #1a1a1a; }
  #restart-btn { width: 100%; padding: 14px; border-radius: 10px; border: none; background: #185FA5; color: #fff; font-size: 15px; font-weight: 600; cursor: pointer; }
  #restart-btn:active { background: #0c447c; }
</style>
</head>
<body>

<div id="game">
  <h1>Metodología 5S</h1>
  <div class="subtitle">Área de producción — Panadería industrial</div>

  <div id="scorebar">
    <div class="scard"><div class="scard-label">Puntos</div><div class="scard-val" id="score">0</div></div>
    <div class="scard"><div class="scard-label">Aciertos</div><div class="scard-val" id="correct-count">0</div></div>
    <div class="scard"><div class="scard-label">Errores</div><div class="scard-val" id="error-count">0</div></div>
    <div class="scard"><div class="scard-label">Fase</div><div class="scard-val" id="phase-num">1/5</div></div>
  </div>

  <div id="progress"></div>

  <div id="phase-banner">
    <div id="phase-title"></div>
    <div id="phase-desc"></div>
  </div>

  <div id="instruction"></div>
  <div id="arena"></div>

  <div id="bottom-bar">
    <div id="status-msg"></div>
    <button id="verify-btn">Verificar ✓</button>
  </div>

  <div id="phase-result"></div>
  <button id="next-btn">Siguiente fase →</button>
</div>

<div id="result-screen">
  <div class="result-emoji" id="result-emoji"></div>
  <div id="result-title"></div>
  <div id="result-body"></div>
  <div id="result-score"></div>
  <div id="result-details"></div>
  <button id="restart-btn">Jugar de nuevo</button>
</div>

<script>
const PHASES = [
  {
    id:1, name:"1S — Seiri: Clasificar", icon:"🔴",
    desc:"Separa lo necesario de lo innecesario",
    instruction:"Arrastra TODOS los elementos a alguna zona. Cuando termines pulsa Verificar.",
    zones:[
      {id:"necesario", label:"✅ Necesario", x:2,y:4,w:46,h:90, color:"rgba(29,158,117,0.07)", border:"#1D9E75", labelColor:"#0F6E56"},
      {id:"innecesario", label:"🗑 Innecesario", x:52,y:4,w:46,h:90, color:"rgba(226,75,74,0.07)", border:"#E24B4A", labelColor:"#A32D2D"}
    ],
    items:[
      {id:"rodillo",icon:"🎲",name:"Rodillo de masa",correct:"necesario"},
      {id:"bandeja",icon:"🔥",name:"Bandeja de horno",correct:"necesario"},
      {id:"caja_rota",icon:"📦",name:"Caja rota vacía",correct:"innecesario"},
      {id:"mop_viejo",icon:"🧹",name:"Trapeador viejo",correct:"innecesario"},
      {id:"batidora",icon:"⚙️",name:"Batidora industrial",correct:"necesario"},
      {id:"bolsa_vacia",icon:"🛍️",name:"Bolsas vacías",correct:"innecesario"},
      {id:"charola",icon:"🍞",name:"Charola panadera",correct:"necesario"},
      {id:"llave_rota",icon:"🔧",name:"Llave rota sin uso",correct:"innecesario"}
    ]
  },
  {
    id:2, name:"2S — Seiton: Ordenar", icon:"🟡",
    desc:"Un lugar para cada cosa, cada cosa en su lugar",
    instruction:"Arrastra cada elemento a su zona correcta. Cuando termines pulsa Verificar.",
    zones:[
      {id:"herramientas",label:"🔨 Herramientas",x:1,y:4,w:30,h:44, color:"rgba(55,138,221,0.07)", border:"#378ADD", labelColor:"#185FA5"},
      {id:"ingredientes",label:"🌾 Ingredientes",x:35,y:4,w:30,h:44, color:"rgba(239,159,39,0.07)", border:"#EF9F27", labelColor:"#854F0B"},
      {id:"empaque",label:"📦 Empaque",x:69,y:4,w:30,h:44, color:"rgba(127,119,221,0.07)", border:"#7F77DD", labelColor:"#534AB7"},
      {id:"equipo",label:"⚙️ Equipo mayor",x:1,y:53,w:98,h:42, color:"rgba(99,153,34,0.07)", border:"#639922", labelColor:"#3B6D11"}
    ],
    items:[
      {id:"espatula",icon:"🥄",name:"Espátula",correct:"herramientas"},
      {id:"harina",icon:"🌾",name:"Harina 50 kg",correct:"ingredientes"},
      {id:"bolsas",icon:"🛍️",name:"Bolsas de pan",correct:"empaque"},
      {id:"amasadora",icon:"⚙️",name:"Amasadora",correct:"equipo"},
      {id:"cuchillo",icon:"🔪",name:"Cuchillo molde",correct:"herramientas"},
      {id:"azucar",icon:"🍚",name:"Azúcar 25 kg",correct:"ingredientes"},
      {id:"etiquetas",icon:"🏷️",name:"Etiquetas",correct:"empaque"},
      {id:"horno_rot",icon:"🔥",name:"Horno rotativo",correct:"equipo"}
    ]
  },
  {
    id:3, name:"3S — Seiso: Limpiar", icon:"🟢",
    desc:"Limpia e identifica fuentes de suciedad",
    instruction:"Arrastra cada problema a su acción de limpieza. Cuando termines pulsa Verificar.",
    zones:[
      {id:"barrer",label:"🧹 Barrer/aspirar",x:1,y:4,w:47,h:43, color:"rgba(29,158,117,0.07)", border:"#1D9E75", labelColor:"#0F6E56"},
      {id:"limpiar_equipo",label:"🧼 Limpiar equipo",x:52,y:4,w:47,h:43, color:"rgba(55,138,221,0.07)", border:"#378ADD", labelColor:"#185FA5"},
      {id:"desinfectar",label:"💊 Desinfectar",x:1,y:53,w:47,h:43, color:"rgba(239,159,39,0.07)", border:"#EF9F27", labelColor:"#854F0B"},
      {id:"reparar",label:"🔩 Reportar/reparar",x:52,y:53,w:47,h:43, color:"rgba(226,75,74,0.07)", border:"#E24B4A", labelColor:"#A32D2D"}
    ],
    items:[
      {id:"harina_piso",icon:"🌾",name:"Harina en piso",correct:"barrer"},
      {id:"grasa_bat",icon:"🛢️",name:"Grasa en batidora",correct:"limpiar_equipo"},
      {id:"mesa_sucia",icon:"🍞",name:"Residuos en mesa",correct:"desinfectar"},
      {id:"fuga_agua",icon:"💧",name:"Fuga de tubería",correct:"reparar"},
      {id:"polvo_est",icon:"📦",name:"Polvo en estantes",correct:"barrer"},
      {id:"horno_restos",icon:"🔥",name:"Restos en horno",correct:"limpiar_equipo"},
      {id:"area_prep",icon:"🥄",name:"Residuos área prep.",correct:"desinfectar"},
      {id:"cadena_rota",icon:"⛓️",name:"Cadena desgastada",correct:"reparar"}
    ]
  },
  {
    id:4, name:"4S — Seiketsu: Estandarizar", icon:"🔵",
    desc:"Establece estándares visuales y de control",
    instruction:"Asigna cada herramienta visual a su categoría. Cuando termines pulsa Verificar.",
    zones:[
      {id:"senalizacion",label:"📍 Señalización",x:1,y:4,w:47,h:43, color:"rgba(55,138,221,0.07)", border:"#378ADD", labelColor:"#185FA5"},
      {id:"etiquetado",label:"🏷️ Etiquetado",x:52,y:4,w:47,h:43, color:"rgba(239,159,39,0.07)", border:"#EF9F27", labelColor:"#854F0B"},
      {id:"checklist",label:"📋 Checklist",x:1,y:53,w:47,h:43, color:"rgba(29,158,117,0.07)", border:"#1D9E75", labelColor:"#0F6E56"},
      {id:"codigo_color",label:"🎨 Código colores",x:52,y:53,w:47,h:43, color:"rgba(127,119,221,0.07)", border:"#7F77DD", labelColor:"#534AB7"}
    ],
    items:[
      {id:"cinta_piso",icon:"📍",name:"Cinta delimitadora",correct:"senalizacion"},
      {id:"rotulo_h",icon:"🏷️",name:"Rótulo HARINA",correct:"etiquetado"},
      {id:"lista_aseo",icon:"📋",name:"Lista diaria aseo",correct:"checklist"},
      {id:"trapo_rojo",icon:"🔴",name:"Rojo = peligro",correct:"codigo_color"},
      {id:"flechas",icon:"➡️",name:"Flechas de flujo",correct:"senalizacion"},
      {id:"fecha_venc",icon:"📅",name:"Fecha venc. levadura",correct:"etiquetado"},
      {id:"firma_limp",icon:"✅",name:"Firma responsable",correct:"checklist"},
      {id:"verde_op",icon:"🟢",name:"Verde = operativo",correct:"codigo_color"}
    ]
  },
  {
    id:5, name:"5S — Shitsuke: Disciplina", icon:"⚫",
    desc:"Mantén los hábitos y la cultura 5S",
    instruction:"Clasifica cada situación como buena práctica o mal hábito. Luego pulsa Verificar.",
    zones:[
      {id:"buena",label:"✅ Buena práctica",x:2,y:4,w:46,h:90, color:"rgba(29,158,117,0.07)", border:"#1D9E75", labelColor:"#0F6E56"},
      {id:"mala",label:"❌ Mal hábito",x:52,y:4,w:46,h:90, color:"rgba(226,75,74,0.07)", border:"#E24B4A", labelColor:"#A32D2D"}
    ],
    items:[
      {id:"audit_sem",icon:"📋",name:"Auditoría semanal 5S",correct:"buena"},
      {id:"dejar_tools",icon:"🔧",name:"Herramientas fuera zona",correct:"mala"},
      {id:"capacitar",icon:"👥",name:"Capacitar operarios",correct:"buena"},
      {id:"saltar_check",icon:"❌",name:"Omitir checklist",correct:"mala"},
      {id:"reunion_5m",icon:"⏱️",name:"Reunión 5 min turno",correct:"buena"},
      {id:"ignorar_s",icon:"🗑️",name:"Ignorar suciedad",correct:"mala"},
      {id:"foto_avance",icon:"📸",name:"Registro fotográfico",correct:"buena"},
      {id:"comer_zona",icon:"🍕",name:"Comer en producción",correct:"mala"}
    ]
  }
];

let state = { phase:0, score:0, correct:0, errors:0, assignments:{}, verified:false, phaseResults:[] };
let dragItem=null, dragOffX=0, dragOffY=0;
const arena = document.getElementById("arena");

function shuffle(arr){
  const a=[...arr];
  for(let i=a.length-1;i>0;i--){
    const j=Math.floor(Math.random()*(i+1));
    [a[i],a[j]]=[a[j],a[i]];
  }
  return a;
}

function generatePositions(count, W, H){
  const iW=74, iH=64, pad=6;
  const positions=[];
  let tries=0;
  while(positions.length<count && tries<600){
    tries++;
    const x=pad+Math.random()*(W-iW-pad*2);
    const y=pad+Math.random()*(H-iH-pad*2);
    let ok=true;
    for(const p of positions){
      if(Math.abs(p.x-x)<iW+6 && Math.abs(p.y-y)<iH+6){ok=false;break;}
    }
    if(ok) positions.push({x,y});
  }
  while(positions.length<count){
    positions.push({x:pad+Math.random()*(W-iW-pad*2), y:pad+Math.random()*(H-iH-pad*2)});
  }
  return positions;
}

function setArenaHeight(){
  const vw=window.innerWidth;
  const h=Math.min(Math.max(vw*0.95, 320), 460);
  arena.style.height=Math.round(h)+"px";
}

function getPhase(){ return PHASES[state.phase]; }

function renderProgress(){
  document.getElementById("progress").innerHTML=PHASES.map((p,i)=>{
    let c="prog-dot";
    if(i<state.phase) c+=" done";
    else if(i===state.phase) c+=" current";
    return `<div class="${c}"></div>`;
  }).join("");
}

function renderPhase(){
  setArenaHeight();
  const p=getPhase();
  state.assignments={};
  state.verified=false;
  document.getElementById("phase-num").textContent=`${p.id}/5`;
  document.getElementById("phase-title").textContent=p.name;
  document.getElementById("phase-desc").textContent=p.desc;
  document.getElementById("instruction").textContent=p.instruction;
  document.getElementById("verify-btn").style.display="none";
  document.getElementById("next-btn").style.display="none";
  document.getElementById("phase-result").style.display="none";
  document.getElementById("phase-result").className="";
  document.getElementById("status-msg").textContent="Arrastra todos los elementos";
  renderProgress();
  renderArena();
}

function renderArena(){
  arena.innerHTML="";
  const p=getPhase();
  const W=arena.clientWidth||360;
  const H=arena.clientHeight||380;

  p.zones.forEach(z=>{
    const el=document.createElement("div");
    el.className="zone";
    el.id="zone-"+z.id;
    el.style.cssText=`left:${z.x/100*W}px;top:${z.y/100*H}px;width:${z.w/100*W}px;height:${z.h/100*H}px;background:${z.color};border-color:${z.border}66;border-style:dashed;border-width:2px;`;
    el.dataset.zoneId=z.id;
    const lbl=document.createElement("div");
    lbl.className="zone-label";
    lbl.style.color=z.labelColor||"#666";
    lbl.textContent=z.label;
    el.appendChild(lbl);
    arena.appendChild(el);
  });

  const shuffled=shuffle(p.items);
  const positions=generatePositions(shuffled.length, W, H);

  shuffled.forEach((item,i)=>{
    const pos=positions[i];
    const el=document.createElement("div");
    el.className="item";
    el.id="item-"+item.id;
    el.style.left=Math.round(pos.x)+"px";
    el.style.top=Math.round(pos.y)+"px";
    el.dataset.itemId=item.id;
    el.innerHTML=`<div class="item-icon">${item.icon}</div><div class="item-name">${item.name}</div>`;
    el.addEventListener("mousedown", startDrag);
    el.addEventListener("touchstart", startDragTouch, {passive:false});
    arena.appendChild(el);
  });
}

function startDrag(e){
  e.preventDefault();
  if(state.verified) return;
  dragItem=e.currentTarget;
  const rect=dragItem.getBoundingClientRect();
  dragOffX=e.clientX-rect.left;
  dragOffY=e.clientY-rect.top;
  dragItem.classList.add("dragging");
  dragItem.style.zIndex=30;
  document.addEventListener("mousemove", onMouseMove);
  document.addEventListener("mouseup", onMouseUp);
}
function onMouseMove(e){ if(!dragItem)return; moveItem(dragItem,e.clientX,e.clientY); highlightZone(e.clientX,e.clientY); }
function onMouseUp(e){
  if(!dragItem)return;
  dragItem.classList.remove("dragging");
  dragItem.style.zIndex=10;
  const z=getZoneAt(e.clientX,e.clientY);
  if(z) assignItem(dragItem,z);
  clearHighlights();
  dragItem=null;
  document.removeEventListener("mousemove",onMouseMove);
  document.removeEventListener("mouseup",onMouseUp);
}

function startDragTouch(e){
  e.preventDefault();
  if(state.verified)return;
  dragItem=e.currentTarget;
  const t=e.touches[0];
  const rect=dragItem.getBoundingClientRect();
  dragOffX=t.clientX-rect.left;
  dragOffY=t.clientY-rect.top;
  dragItem.classList.add("dragging");
  dragItem.style.zIndex=30;
  document.addEventListener("touchmove",onTouchMove,{passive:false});
  document.addEventListener("touchend",onTouchEnd);
}
function onTouchMove(e){
  if(!dragItem)return;
  e.preventDefault();
  const t=e.touches[0];
  moveItem(dragItem,t.clientX,t.clientY);
  highlightZone(t.clientX,t.clientY);
}
function onTouchEnd(e){
  if(!dragItem)return;
  dragItem.classList.remove("dragging");
  dragItem.style.zIndex=10;
  const t=e.changedTouches[0];
  const z=getZoneAt(t.clientX,t.clientY);
  if(z) assignItem(dragItem,z);
  clearHighlights();
  dragItem=null;
  document.removeEventListener("touchmove",onTouchMove);
  document.removeEventListener("touchend",onTouchEnd);
}

function moveItem(el,cx,cy){
  const aR=arena.getBoundingClientRect();
  let nx=cx-aR.left-dragOffX;
  let ny=cy-aR.top-dragOffY;
  nx=Math.max(0,Math.min(nx,aR.width-74));
  ny=Math.max(0,Math.min(ny,aR.height-64));
  el.style.left=nx+"px";
  el.style.top=ny+"px";
}

function assignItem(itemEl,zoneEl){
  state.assignments[itemEl.dataset.itemId]=zoneEl.dataset.zoneId;
  checkAllPlaced();
}

function checkAllPlaced(){
  const p=getPhase();
  const total=p.items.length;
  const placed=Object.keys(state.assignments).length;
  document.getElementById("status-msg").textContent=`${placed} de ${total} colocados`;
  if(placed===total){
    document.getElementById("verify-btn").style.display="block";
    document.getElementById("status-msg").textContent="¡Listo! Verifica tu respuesta.";
  }
}

function highlightZone(cx,cy){
  document.querySelectorAll(".zone").forEach(z=>{
    const r=z.getBoundingClientRect();
    z.classList.toggle("hover-drop",cx>=r.left&&cx<=r.right&&cy>=r.top&&cy<=r.bottom);
  });
}
function clearHighlights(){ document.querySelectorAll(".zone").forEach(z=>z.classList.remove("hover-drop")); }
function getZoneAt(cx,cy){
  for(const z of document.querySelectorAll(".zone")){
    const r=z.getBoundingClientRect();
    if(cx>=r.left&&cx<=r.right&&cy>=r.top&&cy<=r.bottom) return z;
  }
  return null;
}

document.getElementById("verify-btn").addEventListener("click",()=>{
  const p=getPhase();
  let ok=0, fail=0, wrong=[];
  p.items.forEach(item=>{
    const chosen=state.assignments[item.id];
    const el=document.getElementById("item-"+item.id);
    if(chosen===item.correct){
      ok++;
      el.style.border="1.5px solid #1D9E75";
      el.style.background="#E1F5EE";
    } else {
      fail++;
      wrong.push(item.name);
      el.style.border="1.5px solid #E24B4A";
      el.style.background="#FCEBEB";
    }
  });
  state.correct+=ok;
  state.errors+=fail;
  state.score+=ok*10;
  if(fail===0) state.score+=20;
  state.verified=true;
  state.phaseResults.push({phase:p.name, correct:ok, total:p.items.length});
  document.getElementById("score").textContent=state.score;
  document.getElementById("correct-count").textContent=state.correct;
  document.getElementById("error-count").textContent=state.errors;
  const pr=document.getElementById("phase-result");
  pr.style.display="block";
  if(fail===0){
    pr.className="ok";
    pr.textContent=`¡Perfecto! ${ok}/${p.items.length} correctos. +20 pts bonus 🎉`;
  } else {
    pr.className="err";
    pr.textContent=`${ok}/${p.items.length} correctos. Incorrectos: ${wrong.join(", ")}.`;
  }
  document.getElementById("verify-btn").style.display="none";
  document.getElementById("next-btn").style.display="block";
  document.getElementById("next-btn").textContent=state.phase<PHASES.length-1?"Siguiente fase →":"Ver resultados →";
  window.scrollTo({top:document.body.scrollHeight, behavior:"smooth"});
});

document.getElementById("next-btn").addEventListener("click",()=>{
  if(state.phase<PHASES.length-1){ state.phase++; renderPhase(); window.scrollTo({top:0,behavior:"smooth"}); }
  else showResult();
});

function showResult(){
  document.getElementById("game").style.display="none";
  document.getElementById("result-screen").style.display="block";
  const total=PHASES.reduce((a,p)=>a+p.items.length,0);
  const pct=Math.round(state.correct/total*100);
  let emoji,title,body;
  if(pct>=90){emoji="🏆";title="¡Maestro 5S!";body="Dominas la metodología. Tu panadería queda impecable y lista para producción de alta calidad.";}
  else if(pct>=70){emoji="🎯";title="¡Muy bien!";body="Buen dominio de las 5S. Unos pocos conceptos más y serás experto en mejora continua.";}
  else if(pct>=50){emoji="📈";title="En proceso";body="Vas por buen camino. Repasa los conceptos clave de cada S y vuelve a intentarlo.";}
  else{emoji="💪";title="Sigue practicando";body="Las 5S requieren práctica constante. ¡Cada intento te acerca más a dominarlas!";}
  document.getElementById("result-emoji").textContent=emoji;
  document.getElementById("result-title").textContent=title;
  document.getElementById("result-body").textContent=body;
  document.getElementById("result-score").textContent=`${state.score} pts — ${pct}%`;
  const det=document.getElementById("result-details");
  det.innerHTML=state.phaseResults.map(r=>`<div class="result-row"><span>${r.phase}</span><span>${r.correct}/${r.total}</span></div>`).join("")+
    `<div class="result-row"><span>Total errores</span><span>${state.errors}</span></div>`;
  window.scrollTo({top:0,behavior:"smooth"});
}

document.getElementById("restart-btn").addEventListener("click",()=>{
  state={phase:0,score:0,correct:0,errors:0,assignments:{},verified:false,phaseResults:[]};
  ["score","correct-count","error-count"].forEach(id=>document.getElementById(id).textContent=0);
  document.getElementById("result-screen").style.display="none";
  document.getElementById("game").style.display="block";
  renderPhase();
  window.scrollTo({top:0,behavior:"smooth"});
});

window.addEventListener("resize", ()=>{ if(!state.verified) renderArena(); });
renderPhase();
</script>
</body>
</html>
