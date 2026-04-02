<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1.0,viewport-fit=cover"/>
<title>Guitar Chord Viewer v6</title>
<style>
:root{
  --bg:#1a1a1a; --surface:#222; --card:#2a2a2a; --border:#3a3a3a;
  --text:#f0f0f0; --muted:#a0a0a0; --faint:#555;
  --accent:#c9a84c; --accent-fg:#1a1a1a;
  --nut:#d4c5a0; --fret:#5a5a5a; --string:#6a6a6a;
  --root-col:#ef4444;
  --left-w:290px;
}
*{box-sizing:border-box;margin:0;padding:0}
html,body{min-height:100%;background:var(--bg);color:var(--text);
  font-family:-apple-system,BlinkMacSystemFont,"Hiragino Sans","Noto Sans JP",sans-serif}
button{font:inherit;cursor:pointer}
svg{display:block}

/* ── MOBILE ── */
.app-shell{max-width:480px;margin:0 auto;padding:8px 12px 40px}
.title{padding:8px 0 0;text-align:center;font-size:11px;font-weight:700;
  letter-spacing:5px;color:var(--muted)}
.sec{margin-top:10px}
.sec-label{margin:0 0 7px 2px;font-size:10px;font-weight:700;
  letter-spacing:3px;color:var(--muted)}
.row{display:flex;gap:5px}
.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:5px}
.btn{flex:1;padding:10px 0;border-radius:10px;
  border:1.5px solid var(--border);background:var(--card);color:var(--text)}
.btn.active{border-color:var(--accent);background:var(--accent);
  color:var(--accent-fg);font-weight:800}
.btn.root{font-size:18px;font-weight:900}
.btn.acc{font-size:15px;font-weight:700}
.btn.type{font-size:15px;font-weight:800}

.card{margin-top:14px;background:var(--surface);
  border:1px solid var(--border);border-radius:18px;overflow:hidden}
.card-head{padding:10px 14px 8px;border-bottom:1px solid var(--border);
  display:flex;align-items:center;gap:10px}
.chord-name{font-size:44px;font-weight:900;letter-spacing:-2px;line-height:1}
.comp-wrap{margin-left:auto;display:flex;align-items:center;gap:8px;
  flex-wrap:wrap;justify-content:flex-end}
.comp-label{font-size:16px;color:var(--muted);font-weight:800;white-space:nowrap}
.comp-list{display:flex;gap:5px;flex-wrap:wrap;justify-content:flex-end}
.comp-item{display:flex;flex-direction:column;align-items:center;gap:1px}
.comp-note{width:42px;height:42px;border-radius:50%;display:flex;align-items:center;
  justify-content:center;font-size:22px;font-weight:900;border:2px solid currentColor}
.comp-note.is-root{width:48px;height:48px;border-width:3px}
.comp-role{font-size:20px;font-weight:700}

.tabs{display:flex;gap:6px;padding:8px;
  border-bottom:1px solid var(--border);background:var(--card)}
.tab{flex:1;padding:11px 0;border:1px solid var(--border);
  border-right:2px solid color-mix(in srgb,var(--text) 22%,var(--border));
  background:transparent;color:var(--muted);font-size:16px;font-weight:700;
  border-bottom:2.5px solid transparent}
.tab:last-child{border-right:1px solid var(--border)}
.tab.active{color:var(--accent);border-color:var(--accent);
  border-bottom-color:var(--accent);
  background:color-mix(in srgb,var(--accent) 22%,transparent);
  box-shadow:inset 0 0 0 1px color-mix(in srgb,var(--accent) 35%,transparent)}

.empty{margin:24px 14px;font-size:14px;color:var(--muted);text-align:center}

.diag-scroll{overflow-x:auto;-webkit-overflow-scrolling:touch;
  padding:8px 10px 4px;
  scrollbar-width:thin;scrollbar-color:var(--border) transparent}
.diag-scroll::-webkit-scrollbar{height:3px}
.diag-scroll::-webkit-scrollbar-thumb{background:var(--border);border-radius:2px}
.diag-row{display:flex;gap:10px;width:max-content;align-items:flex-start}

/* ＋ボタン（カスタム追加） */
.add-card{flex-shrink:0;width:100px;min-height:180px;background:var(--card);
  border:2px dashed var(--border);border-radius:14px;
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  gap:8px;cursor:pointer;transition:border-color .15s,background .15s;
  color:var(--muted);align-self:center}
.add-card:hover{border-color:var(--accent);background:color-mix(in srgb,var(--accent) 7%,var(--card));color:var(--accent)}
.add-card-icon{font-size:32px;font-weight:300;line-height:1}
.add-card-label{font-size:11px;font-weight:700;letter-spacing:1px}

.diag-card{flex-shrink:0;width:260px;background:var(--card);
  border:1px solid var(--border);border-radius:14px;
  padding:12px 10px 10px;display:flex;flex-direction:column;
  align-items:center;gap:8px;position:relative;
  cursor:pointer;transition:border-color .15s,box-shadow .15s,background .15s}
.diag-card:hover{border-color:color-mix(in srgb,var(--accent) 50%,transparent)}
.diag-card.selected{
  border-color:var(--accent);
  background:color-mix(in srgb,var(--accent) 7%,var(--card));
  box-shadow:0 0 0 2px color-mix(in srgb,var(--accent) 25%,transparent)}
.diag-card-meta{width:100%;display:flex;gap:5px;
  justify-content:center;flex-wrap:wrap;align-items:center}
.meta-badge{display:inline-block;padding:3px 9px;border-radius:10px;
  border:1px solid var(--border);background:var(--surface);
  font-size:11px;font-weight:800;color:var(--text)}
.meta-badge.inversion{
  color:#38bdf8;
  border-color:color-mix(in srgb,#38bdf8 50%,transparent);
  background:color-mix(in srgb,#38bdf8 10%,transparent)}
.meta-badge.custom{
  color:#f59e0b;
  border-color:color-mix(in srgb,#f59e0b 50%,transparent);
  background:color-mix(in srgb,#f59e0b 10%,transparent)}
.diagram-wrap{display:flex;align-items:flex-start;gap:4px;justify-content:center}
.string-notes{display:flex;flex-direction:column;margin-top:-4px;padding-bottom:28px}
.sn-row{display:flex;align-items:center;gap:5px;height:36px}
.sn-box{width:36px;height:28px;border-radius:5px;display:flex;
  align-items:center;justify-content:center;
  font-size:15px;font-weight:900;letter-spacing:-0.3px}
.sn-box.lowest{border-width:2.5px}
.sn-role{font-size:16px;font-weight:900;min-width:24px}
.sn-role.is-root{font-size:18px}

/* delete btn on card */
.card-del-btn{position:absolute;top:6px;right:6px;
  width:22px;height:22px;border-radius:50%;border:none;
  background:rgba(0,0,0,.45);color:#fff;font-size:13px;font-weight:700;
  display:flex;align-items:center;justify-content:center;
  opacity:0;transition:opacity .15s;line-height:1;padding:0}
.diag-card:hover .card-del-btn{opacity:1}
.card-del-btn:hover{background:rgba(239,68,68,.8)!important;opacity:1!important}
/* edit btn on card */
.card-edit-btn{position:absolute;top:6px;right:32px;
  width:22px;height:22px;border-radius:50%;border:none;
  background:rgba(0,0,0,.45);color:#fff;font-size:12px;font-weight:700;
  display:flex;align-items:center;justify-content:center;
  opacity:0;transition:opacity .15s;line-height:1;padding:0}
.diag-card:hover .card-edit-btn{opacity:1}
.card-edit-btn:hover{background:color-mix(in srgb,var(--accent) 80%,#000)!important;opacity:1!important}
/* モバイル: hover が効かないため常時表示・サイズ拡大 */
@media (hover: none), (pointer: coarse) {
  .card-del-btn,
  .card-edit-btn {
    opacity: 1;
    width: 28px;
    height: 28px;
  }
  .card-edit-btn {
    right: 38px;
  }
}

.fb-wrap{padding:8px 8px 4px;overflow-x:auto;-webkit-overflow-scrolling:touch}
.mb-tab-row{border-top:1px solid var(--border);
  padding:8px 10px 6px;display:flex;gap:6px;flex-wrap:wrap}
.mb-tab-row .tab{border-radius:8px;flex:1;min-width:72px}
.mb-theme-row{border-top:1px solid var(--border);
  padding:10px 14px 14px;
  display:flex;align-items:center;justify-content:flex-end;gap:10px}
.theme-btn{width:22px;height:22px;border-radius:50%;
  border:2px solid var(--border);cursor:pointer;padding:0;transition:all .2s}
.theme-btn.active{width:28px;height:28px;border:3px solid var(--text)}

/* ── DESKTOP ── */
@media(min-width:1024px){
  body{padding:0;overflow:hidden;height:100vh}
  .app-shell{max-width:none;margin:0;padding:0;
    display:grid;grid-template-columns:var(--left-w) 1fr;
    grid-template-rows:100vh;height:100vh;overflow:hidden}

  .left-panel{grid-column:1;grid-row:1;background:var(--surface);
    border-right:1px solid var(--border);
    overflow-y:auto;overflow-x:hidden;display:flex;flex-direction:column;
    scrollbar-width:thin;scrollbar-color:var(--border) transparent}
  .left-panel::-webkit-scrollbar{width:4px}
  .left-panel::-webkit-scrollbar-thumb{background:var(--border);border-radius:2px}

  .right-panel{grid-column:2;grid-row:1;
    overflow-y:auto;overflow-x:hidden;display:flex;flex-direction:column;
    scrollbar-width:thin;scrollbar-color:var(--border) transparent}
  .right-panel::-webkit-scrollbar{width:6px}
  .right-panel::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px}

  .title{padding:18px 16px 14px;text-align:left;font-size:10px;
    letter-spacing:6px;border-bottom:1px solid var(--border);color:var(--accent)}
  .pc-sec{padding:14px 16px 10px;border-bottom:1px solid var(--border)}
  .pc-sec-label{font-size:9px;font-weight:800;letter-spacing:3px;
    color:var(--muted);margin-bottom:8px;text-transform:uppercase}
  .pc-root-row{display:grid;grid-template-columns:repeat(7,1fr);gap:4px}
  .pc-root-row .btn.root{font-size:15px;padding:8px 0;border-radius:8px}
  .pc-acc-row{display:grid;grid-template-columns:1fr 1fr;gap:4px}
  .pc-acc-row .btn.acc{font-size:13px;padding:7px 0;border-radius:8px}
  .pc-cat-label{font-size:9px;font-weight:800;letter-spacing:2px;
    color:var(--faint);text-transform:uppercase;margin-bottom:5px;padding-left:2px}
  .pc-type-row{display:grid;grid-template-columns:repeat(4,1fr);
    gap:4px;margin-bottom:10px}
  .pc-type-row .btn.type{font-size:13px;padding:7px 2px;border-radius:8px}
  .pc-theme-strip{padding:12px 16px 16px;margin-top:auto;
    border-top:1px solid var(--border);display:flex;align-items:center;gap:10px}

  .mobile-only{display:none!important}

  .pc-result{flex:1;display:flex;flex-direction:column;
    padding:8px 18px 12px;gap:6px}
  .pc-header{display:flex;align-items:center;gap:14px;padding:6px 16px;
    background:var(--surface);border:1px solid var(--border);
    border-radius:14px;flex-shrink:0}
  .pc-header .chord-name{font-size:44px}
  .pc-fretboard-wrap{background:var(--surface);border:1px solid var(--border);
    border-radius:16px;padding:8px 14px;flex-shrink:0}
  .pc-fb-header{display:flex;align-items:center;
    justify-content:space-between;margin-bottom:8px;gap:10px}
  .pc-fb-title{font-size:9px;font-weight:800;letter-spacing:3px;
    color:var(--muted);text-transform:uppercase}
  .pc-tab-row{display:flex;gap:6px;flex-wrap:wrap;justify-content:flex-end}
  .pc-tab-btn{padding:6px 16px;border-radius:10px;
    border:1.5px solid var(--border);background:var(--card);
    color:var(--muted);font-size:13px;font-weight:700}
  .pc-tab-btn.active{border-color:var(--accent);
    background:color-mix(in srgb,var(--accent) 18%,transparent);
    color:var(--accent)}
  .diag-card{width:270px;padding:14px 10px 12px;gap:10px}
  .add-card{min-height:200px}
}
@media(max-width:1023px){
  .pc-only{display:none!important}
  .left-panel,.right-panel{display:contents}
}

/* ══════════════════════════════════════
   CUSTOM BUILDER MODAL
══════════════════════════════════════ */
.cb-overlay{
  position:fixed;inset:0;z-index:1000;
  background:rgba(0,0,0,.75);backdrop-filter:blur(4px);
  display:flex;align-items:flex-end;justify-content:center;
  opacity:0;pointer-events:none;transition:opacity .2s}
.cb-overlay.open{opacity:1;pointer-events:all}

.cb-sheet{
  width:100%;max-width:480px;max-height:92vh;
  background:var(--bg);border-radius:22px 22px 0 0;
  overflow-y:auto;overflow-x:hidden;
  transform:translateY(40px);transition:transform .25s;
  padding:0 0 32px;
  scrollbar-width:thin;scrollbar-color:var(--border) transparent}
.cb-overlay.open .cb-sheet{transform:translateY(0)}
@media(min-width:1024px){
  .cb-overlay{align-items:center}
  .cb-sheet{max-width:520px;border-radius:20px;max-height:88vh}}

.cb-handle{width:36px;height:4px;border-radius:2px;background:var(--border);
  margin:12px auto 0}
.cb-header{padding:14px 16px 10px;display:flex;align-items:center;gap:10px;
  border-bottom:1px solid var(--border)}
.cb-title{font-size:14px;font-weight:800;letter-spacing:2px;color:var(--muted)}
.cb-chord-lbl{font-size:22px;font-weight:900;color:var(--accent)}
.cb-close{margin-left:auto;width:32px;height:32px;border-radius:50%;
  border:1px solid var(--border);background:transparent;
  color:var(--muted);font-size:18px;display:flex;align-items:center;justify-content:center}

/* comp chips in modal */
.cb-comp{display:flex;gap:5px;flex-wrap:wrap;padding:10px 14px;
  border-bottom:1px solid var(--border);align-items:center}
.cb-chip{padding:4px 10px;border-radius:16px;font-size:12px;font-weight:800;border:2px solid}

/* range slider */
.cb-range-row{display:flex;align-items:center;gap:8px;
  padding:8px 14px 4px}
.cb-range-lbl{font-size:10px;font-weight:700;letter-spacing:2px;color:var(--muted)}
.cb-fret-lbl{font-size:14px;font-weight:800;color:var(--accent);min-width:28px;text-align:right}
.cb-track{flex:1;height:4px;border-radius:2px;background:var(--border);position:relative;cursor:pointer}
.cb-thumb{position:absolute;top:50%;transform:translate(-50%,-50%);
  width:18px;height:18px;border-radius:50%;background:var(--accent);
  border:2px solid var(--accent-fg);cursor:grab}

/* fretboard */
.cb-fb-wrap{padding:6px 10px 2px;user-select:none}
#cb-svg{display:block;width:100%;touch-action:pan-y}
.cb-hint{font-size:10px;color:var(--muted);text-align:center;margin-top:4px;padding:0 14px}

/* name input + actions */
.cb-actions{padding:12px 14px;border-top:1px solid var(--border);display:flex;flex-direction:column;gap:8px}
.cb-name-input{width:100%;padding:10px 12px;border-radius:10px;
  border:1.5px solid var(--border);background:var(--card);
  color:var(--text);font-size:14px;font-weight:700;outline:none}
.cb-name-input:focus{border-color:var(--accent)}
.cb-btn-row{display:flex;gap:8px}
.cb-clear{flex:1;padding:11px;border-radius:12px;
  border:1.5px solid var(--border);background:transparent;
  color:var(--muted);font-size:14px;font-weight:700}
.cb-save{flex:2;padding:11px;border-radius:12px;
  border:none;background:var(--accent);color:var(--accent-fg);
  font-size:14px;font-weight:800}
.cb-save:disabled{opacity:.35}
.cb-err{font-size:12px;color:#ef4444;text-align:center;min-height:16px}
</style>
</head>
<body>
<div class="app-shell">

  <div class="left-panel">
    <div class="title">GUITAR CHORD</div>

    <div class="sec mobile-only" style="padding:0 12px">
      <div class="sec-label" style="margin-top:10px">ROOT</div>
      <div class="row" id="rootRow-mb"></div>
    </div>
    <div class="pc-sec pc-only">
      <div class="pc-sec-label">ROOT</div>
      <div class="pc-root-row" id="rootRow-pc"></div>
    </div>

    <div class="sec mobile-only" style="padding:0 12px">
      <div class="sec-label" style="margin-top:10px">♯ / ♭</div>
      <div class="row" id="accRow-mb"></div>
    </div>
    <div class="pc-sec pc-only">
      <div class="pc-sec-label">♯ / ♭</div>
      <div class="pc-acc-row" id="accRow-pc"></div>
    </div>

    <div class="sec mobile-only" style="padding:0 12px">
      <div class="sec-label" style="margin-top:10px">TYPE</div>
      <div class="grid" id="typeGrid-mb"></div>
    </div>
    <div class="pc-sec pc-only" style="flex:1">
      <div class="pc-sec-label">TYPE</div>
      <div id="typeGrid-pc"></div>
    </div>

    <div class="pc-theme-strip pc-only" id="themeRow-pc"></div>
  </div>

  <div class="right-panel">
    <div id="app-mb" class="mobile-only"></div>
    <div id="app-pc" class="pc-only"></div>
  </div>

</div>

<!-- ══ CUSTOM BUILDER MODAL ══ -->
<div class="cb-overlay" id="cbOverlay">
  <div class="cb-sheet" id="cbSheet">
    <div class="cb-handle"></div>
    <div class="cb-header">
      <span class="cb-title" id="cbTitle">CUSTOM FORM</span>
      <span class="cb-chord-lbl" id="cbChordLbl"></span>
      <button class="cb-close" id="cbClose">✕</button>
    </div>
    <div class="cb-comp" id="cbComp"></div>
    <div class="cb-range-row">
      <span class="cb-range-lbl">POSITION</span>
      <div class="cb-track" id="cbTrack"><div class="cb-thumb" id="cbThumb"></div></div>
      <span class="cb-fret-lbl" id="cbFretLbl">1f</span>
    </div>
    <div class="cb-fb-wrap">
      <svg id="cb-svg" viewBox="0 0 320 200"></svg>
      <div class="cb-hint">構成音をタップして配置 • 配置済みをタップで解除 • 弦名をタップでミュート</div>
    </div>
    <div class="cb-actions">
      <input class="cb-name-input" id="cbNameInput" type="text" placeholder="フォーム名（任意）" maxlength="32"/>
      <div class="cb-err" id="cbErr"></div>
      <div class="cb-btn-row">
        <button class="cb-clear" id="cbClearBtn">配置クリア</button>
        <button class="cb-save" id="cbSaveBtn" disabled>保存</button>
      </div>
    </div>
  </div>
</div>

<script>
'use strict';

/* ============================================================
   § 0. UI SPEC
   ============================================================ */
const NOOP_ACC = {
  b: new Set(['C', 'F']),
  '#': new Set(['E', 'B']),
};
const isNoopAcc = (base, acc) => NOOP_ACC[acc]?.has(base) ?? false;

/* ============================================================
   § 1. NOTE UTILITIES
   ============================================================ */
const CHROMATIC    = ['C','C#','D','D#','E','F','F#','G','G#','A','A#','B'];
const OPEN_STRINGS = ['E','A','D','G','B','E'];
const FLAT_MAP     = { Db:'C#', Eb:'D#', Gb:'F#', Ab:'G#', Bb:'A#', Cb:'B', Fb:'E' };
const SHARP_MAP    = { 'E#':'F', 'B#':'C' };
const NATURALS     = ['C','D','E','F','G','A','B'];
const LETTER_ORDER = ['C','D','E','F','G','A','B'];

const canon   = n        => FLAT_MAP[n] || SHARP_MAP[n] || n;
const noteIdx = n        => CHROMATIC.indexOf(canon(n));
const noteAt  = (s, f)   => CHROMATIC[(noteIdx(OPEN_STRINGS[s]) + f) % 12];
const transp  = (r, semi)=> { const i = noteIdx(r); return i < 0 ? null : CHROMATIC[(i+semi+120)%12]; };

const IV_TO_DEGREE_SPELL = {
   0: { lo:0, alt: 0 },
   1: { lo:0, alt:+1 },
   2: { lo:1, alt: 0 },
   3: { lo:2, alt:-1 },
   4: { lo:2, alt: 0 },
   5: { lo:3, alt: 0 },
   6: { lo:4, alt:-1 },
   7: { lo:4, alt: 0 },
   8: { lo:4, alt:+1 },
   9: { lo:5, alt: 0 },
  10: { lo:6, alt:-1 },
  11: { lo:6, alt: 0 },
};

function rootLetterIdx(rootSpell) {
  return LETTER_ORDER.indexOf(rootSpell[0]);
}
function alterStr(alt) {
  if (alt <= -2) return '𝄫';
  if (alt === -1) return '♭';
  if (alt === +1) return '♯';
  if (alt >= +2)  return '𝄪';
  return '';
}
function spellNote(rootSpell, iv, typeId) {
  const rli = rootLetterIdx(rootSpell);
  let { lo, alt } = IV_TO_DEGREE_SPELL[iv] || { lo:0, alt:0 };

  if (typeId === '7#9'  && iv === 3) { lo = 1; alt = +1; }
  if (typeId === 'dim7' && iv === 9) { lo = 5; alt =  0; }
  if (typeId === 'b13'  && iv === 8) { lo = 5; alt = -1; }
  if (typeId === 'aug'  && iv === 8) { lo = 4; alt = +1; }

  const letterIdx    = (rli + lo) % 7;
  const letter       = LETTER_ORDER[letterIdx];
  const expectedPc   = (noteIdx(rootSpell) + iv + 120) % 12;
  const baseLetterPc = noteIdx(letter);
  const spellPc      = (baseLetterPc + alt + 12) % 12;
  let finalAlt = alt;
  const diff = (expectedPc - spellPc + 12) % 12;
  if      (diff === 1)  finalAlt += 1;
  else if (diff === 2)  finalAlt += 2;
  else if (diff === 11) finalAlt -= 1;
  else if (diff === 10) finalAlt -= 2;

  return letter + alterStr(finalAlt);
}

/* ============================================================
   § 2. CHORD TYPE DICTIONARY
   ============================================================ */
const CHORD_TYPES = [
  { id:'M',    label:'M',      intervals:[0,4,7]        },
  { id:'m',    label:'m',      intervals:[0,3,7]        },
  { id:'M7',   label:'M7',     intervals:[0,4,7,11]     },
  { id:'m7',   label:'m7',     intervals:[0,3,7,10]     },
  { id:'7',    label:'7',      intervals:[0,4,7,10]     },
  { id:'m7b5', label:'m7♭5',   intervals:[0,3,6,10]     },
  { id:'mM7',  label:'mM7',    intervals:[0,3,7,11]     },
  { id:'7#9',  label:'7(♯9)',  intervals:[0,4,7,10,3]   },
  { id:'aug',  label:'aug',    intervals:[0,4,8]        },
  { id:'dim',  label:'dim',    intervals:[0,3,6]        },
  { id:'dim7', label:'dim7',   intervals:[0,3,6,9]      },
  { id:'69',   label:'69',     intervals:[0,4,7,9,2]    },
  { id:'6',    label:'6',      intervals:[0,4,7,9]      },
  { id:'m6',   label:'m6',     intervals:[0,3,7,9]      },
  { id:'11',   label:'11',     intervals:[0,4,7,10,2,5] },
  { id:'m11',  label:'m11',    intervals:[0,3,7,10,2,5] },
  { id:'9',    label:'9',      intervals:[0,4,7,10,2]   },
  { id:'m9',   label:'m9',     intervals:[0,3,7,10,2]   },
  { id:'M9',   label:'M9',     intervals:[0,4,7,11,2]   },
  { id:'sus4', label:'sus4',   intervals:[0,5,7]        },
  { id:'13',   label:'13',     intervals:[0,4,7,10,2,9] },
  { id:'b13',  label:'b13',    intervals:[0,4,7,10,8]   },
  { id:'M13',  label:'M13',    intervals:[0,4,7,11,2,9] },
  { id:'add9', label:'add9',   intervals:[0,4,7,2]      },
];
const TYPE_MAP = Object.fromEntries(CHORD_TYPES.map(t => [t.id, t]));
const DISP_SUFFIX = {
  M:'', m:'m', M7:'M7', m7:'m7', '7':'7', m7b5:'m7(♭5)', mM7:'mM7',
  '7#9':'7(♯9)', aug:'aug', dim:'dim', dim7:'dim7', '69':'69',
  '6':'6', m6:'m6', '11':'11', m11:'m11', '9':'9', m9:'m9',
  M9:'M9', sus4:'sus4', '13':'13', b13:'b13', M13:'M13', add9:'add9',
};
const TYPE_CATS = [
  { label:'基本',       ids:['M','m','sus4','aug','dim'] },
  { label:'7系',        ids:['M7','m7','7','mM7','m7b5','dim7'] },
  { label:'テンション', ids:['9','m9','M9','11','m11','13','M13','b13','add9','69'] },
  { label:'特殊',       ids:['7#9','6','m6'] },
];

/* ============================================================
   § 3. DEGREE ROLES
   ============================================================ */
const ROLES = {
  R:    { name:'R',    color:'#ef4444' },
  '3':  { name:'3',    color:'#8b5cf6' },
  m3:   { name:'m3',   color:'#a78bfa' },
  '5':  { name:'5',    color:'#10b981' },
  b5:   { name:'♭5',   color:'#94a3b8' },
  s5:   { name:'♯5',   color:'#fb923c' },
  M7:   { name:'M7',   color:'#f59e0b' },
  b7:   { name:'♭7',   color:'#f97316' },
  bb7:  { name:'bb7',  color:'#f43f5e' },
  '9':  { name:'9',    color:'#06b6d4' },
  s9:   { name:'♯9',   color:'#e879f9' },
  '11': { name:'11',   color:'#84cc16' },
  '4':  { name:'4',    color:'#84cc16' },
  '6':  { name:'6',    color:'#14b8a6' },
  '13': { name:'13',   color:'#0ea5e9' },
  b13:  { name:'♭13',  color:'#38bdf8' },
};
const IV_ROLE_DEFAULT = {
   0: ROLES.R, 2: ROLES['9'], 3: ROLES.m3, 4: ROLES['3'],
   5: null, 6: null, 7: ROLES['5'], 8: null, 9: null, 10: ROLES.b7, 11: ROLES.M7,
};
const IV_ROLE_EXCEPTION = {
  '7#9':  { 3: ROLES.s9 },
  'sus4': { 5: ROLES['4'] },
  '11':   { 5: ROLES['11'] },
  'm11':  { 5: ROLES['11'] },
  'm7b5': { 6: ROLES.b5 },
  'dim':  { 6: ROLES.b5 },
  'dim7': { 6: ROLES.b5, 9: ROLES.bb7 },
  'aug':  { 7: null, 8: ROLES.s5 },
  'b13':  { 8: ROLES.b13 },
  '6':    { 9: ROLES['6'] },
  'm6':   { 9: ROLES['6'] },
  '69':   { 9: ROLES['6'] },
  '13':   { 9: ROLES['13'] },
  'M13':  { 9: ROLES['13'] },
};
function getRoleByIv(iv, typeId) {
  const exc = IV_ROLE_EXCEPTION[typeId];
  if (exc && Object.prototype.hasOwnProperty.call(exc, iv)) return exc[iv];
  return IV_ROLE_DEFAULT[iv] ?? null;
}

/* ============================================================
   § 4. COMP BUILDER
   ============================================================ */
function buildComp(rootPc, typeId) {
  const t = TYPE_MAP[typeId];
  if (!t) return [];
  return [...new Set(t.intervals)].map(iv => ({ iv }));
}

/* ============================================================
   § 5. BARRE / POS / TONEPOINT
   ============================================================ */
function normBarre(frets, rawBarre) {
  const candidate = rawBarre || autoDetectBarre(frets);
  if (!candidate) return null;
  if (candidate.fret <= 0) return null;
  const covered = [];
  for (let s = candidate.to; s <= candidate.from; s++) covered.push(s);
  const barrable = covered.filter(s => {
    const f = frets[s];
    return typeof f === 'number' && f > 0;
  });
  if (barrable.length < 2) return null;
  return { fret: candidate.fret, from: Math.max(...barrable), to: Math.min(...barrable) };
}
function autoDetectBarre(frets) {
  if (frets.some(f => f === 0)) return null;
  const pos = frets.filter(f => typeof f === 'number' && f > 0);
  if (!pos.length) return null;
  const minF  = Math.min(...pos);
  const bStrs = frets.map((f,s) => ({f,s})).filter(x => x.f === minF).map(x => x.s);
  if (bStrs.length < 2) return null;
  const played = frets.map((f,s) => ({f,s})).filter(x => typeof x.f==='number'&&x.f>=0).map(x=>x.s);
  const lo = Math.min(...played), hi = Math.max(...played);
  const bLo = Math.min(...bStrs), bHi = Math.max(...bStrs);
  const hasHigher = frets.some(f => typeof f==='number' && f > minF);
  if (bStrs.length===2 && bHi-bLo===1 && hasHigher) return null;
  if (bLo===lo && bHi===hi) return { fret:minF, from:hi, to:lo };
  if (bStrs.length>=3 || (bStrs.length>=2 && hasHigher))
    return { fret:minF, from:Math.max(...bStrs), to:Math.min(...bStrs) };
  return null;
}
function makePos({ frets, barre=undefined, priority=0, scope='all', allowIntervals=[], tag=null, note=null, noRoot=false }) {
  const normFrets = frets.map(f => f ?? null);
  const resolvedBarre = barre === null ? null : barre === undefined ? normBarre(normFrets, null) : normBarre(normFrets, barre);
  return {
    id: '',
    frets: normFrets,
    tonePoints: null,
    barre: resolvedBarre,
    priority,
    scope,
    allowIntervals,
    tag,
    note,
    noRoot,
    source: scope === 'custom' ? 'custom' : 'base',
    customName: null,
  };
}
function startFret(frets) {
  if (frets.some(f => f === 0)) return 1;
  const p = frets.filter(f => typeof f==='number' && f > 0);
  return p.length ? Math.min(...p) : 1;
}
function buildTonePoints(frets, rootPc, typeId) {
  const played = frets.map((f,s) => ({f,s})).filter(x => x.f!=null && x.f>=0);
  const bassStr = played.length ? Math.min(...played.map(x=>x.s)) : null;
  const pcCount = {};
  played.forEach(({f,s}) => {
    const pc = (noteIdx(OPEN_STRINGS[s]) + f) % 12;
    pcCount[pc] = (pcCount[pc]||0) + 1;
  });

  return frets.map((f, s) => {
    if (f == null || f < 0) {
      return {
        stringIndex:s, fret:null, pc:null, noteName:null,
        intervalFromRoot:null, degree:null, degreeColor:null,
        isRoot:false, isBass:false, isDuplicated:false,
      };
    }
    const openPc = noteIdx(OPEN_STRINGS[s]);
    const pc     = (openPc + f) % 12;
    const note   = CHROMATIC[pc];
    const iv     = (pc - noteIdx(rootPc) + 12) % 12;
    const role   = getRoleByIv(iv, typeId);
    return {
      stringIndex:s,
      fret:f,
      pc:pc,
      noteName:note,
      intervalFromRoot:iv,
      degree:role ? role.name : null,
      degreeColor:role ? role.color : null,
      isRoot:role ? role.name === 'R' : false,
      isBass:s === bassStr,
      isDuplicated:(pcCount[pc] || 0) > 1,
    };
  });
}
function validatePos(pos, rootPc, typeId) {
  const compIvs  = new Set(TYPE_MAP[typeId]?.intervals || []);
  const allow    = new Set(pos.allowIntervals);
  const played   = pos.frets.map((f,s) => ({f,s})).filter(x => typeof x.f==='number' && x.f>=0);
  if (!played.length) return false;
  if (!pos.noRoot) {
    const roots = played.filter(x => (noteIdx(noteAt(x.s, x.f)) - noteIdx(rootPc) + 12) % 12 === 0);
    if (!roots.length) return false;
    if (Math.min(...roots.map(r => r.f)) > 15) return false;
  }
  return !played.some(x => {
    const iv = (noteIdx(noteAt(x.s, x.f)) - noteIdx(rootPc) + 12) % 12;
    if (compIvs.has(iv)) return false;
    return !allow.has(iv);
  });
}
function movableToFrets(shape, targetRoot) {
  const rs      = shape.rootStr ?? 0;
  const openIdx = noteIdx(OPEN_STRINGS[rs]);
  let rf        = (noteIdx(targetRoot) - openIdx + 12) % 12;
  while ((shape.minRootFret ?? 0) > rf) rf += 12;
  const minOff = Math.min(...shape.offsets.filter(o => o != null));
  while (rf + minOff < 0) rf += 12;
  return {
    frets: shape.offsets.map(o => o == null ? null : rf + o),
    barre: shape.barre ? { fret: rf + (shape.barre.offset ?? 0), from: shape.barre.from, to: shape.barre.to } : null,
  };
}

/* ============================================================
   § 6. FORM DEFINITIONS
   ============================================================ */
const ALL_ROOT_SHAPES = [
  { type:'M', rootStr:0, offsets:[0,2,2,1,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form', note:'Eフォーム移調型' },
  { type:'M', rootStr:1, offsets:[null,0,2,2,2,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form', note:'Aフォーム移調型' },
  { type:'m', rootStr:0, offsets:[0,2,2,0,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'Em-form', note:'Emフォーム移調型' },
  { type:'m', rootStr:2, offsets:[null,null,0,2,3,1], priority:1, tag:'Dm-form', note:'Dmフォーム移調型' },
  { type:'m', rootStr:1, offsets:[null,0,2,2,1,0], barre:{ offset:0, from:5, to:1 }, priority:2, tag:'Am-form', note:'Amフォーム移調型' },
  { type:'m', rootStr:4, offsets:[null,null,0,-1,0,-2], barre:null, minRootFret:2, priority:3, tag:'inversion-m3bass', note:'mトライアド第1転回形（m3ベース）' },
  { type:'m', rootStr:3, offsets:[null,null,null,0,-1,-2], barre:null, minRootFret:2, priority:4, tag:'inversion-rootbass', note:'mトライアド転回形（3弦Rootベース）' },
  { type:'m', rootStr:4, offsets:[null,null,0,-1,0,null], barre:null, minRootFret:1, priority:5, tag:'inversion-m3bass-compact', note:'mトライアド第1転回形（m3ベース・コンパクト）' },
  { type:'m', rootStr:5, offsets:[null,null,null,0,0,0], barre:{ offset:0, from:5, to:3 }, minRootFret:1, priority:6, tag:'inversion-m3bass-barre', note:'mトライアド第1転回形（m3ベース・バレー）' },
  { type:'m', rootStr:4, offsets:[null,null,null,-1,0,-2], barre:null, minRootFret:2, priority:7, tag:'inversion-5thbass', note:'mトライアド第2転回形（5thベース）' },
  { type:'m7', rootStr:0, offsets:[0,2,0,0,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form', note:'Eフォームm7移調型' },
  { type:'m7', rootStr:1, offsets:[null,0,2,0,1,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form', note:'Aフォームm7移調型' },
  { type:'m7', rootStr:2, offsets:[null,null,0,2,1,1], barre:null, priority:2, tag:'D-form', note:'Dフォームm7移調型' },
  { type:'m7', rootStr:1, offsets:[null,0,-2,0,-2,null], barre:{ offset:-2, from:4, to:2 }, minRootFret:2, priority:3, tag:'A-form-compact', note:'m7コンパクトボイシング（5弦root）' },
  { type:'m7', rootStr:4, offsets:[null,null,0,2,0,2], barre:null, minRootFret:1, priority:4, tag:'inversion-m3bass', note:'m7第1転回形（m3ベース）' },
  { type:'m7', rootStr:3, offsets:[null,null,0,0,-1,1], barre:null, minRootFret:1, priority:5, tag:'inversion-5thbass', note:'m7第2転回形（5thベース）' },
  { type:'m7', rootStr:3, offsets:[null,1,3,0,3,null], barre:null, minRootFret:1, priority:6, tag:'inversion-m3bass-drop', note:'m7第1転回形（m3ベース・drop）' },
  { type:'m7', rootStr:1, offsets:[null,0,-2,-3,-4,null], barre:null, minRootFret:4, priority:7, tag:'A-form-descending', note:'m7下降ボイシング（5弦root）' },
  { type:'m7', rootStr:5, offsets:[null,null,0,0,0,0], barre:{ offset:0, from:5, to:2 }, minRootFret:1, priority:8, tag:'inversion-rootbass', note:'m7転回形（1弦Rootベース・バレー）' },
  { type:'m7', rootStr:2, offsets:[null,0,0,-2,1,null], barre:null, minRootFret:2, priority:9, tag:'inversion-5thbass-drop', note:'m7第2転回形（5thベース・drop）' },
  { type:'M9', rootStr:0, offsets:[0,null,1,-1,0,null], barre:null, priority:0, tag:'E-form' },
  { type:'M9', rootStr:1, offsets:[null,0,-1,1,0,null], barre:null, priority:1, tag:'A-form-1' },
  { type:'M9', rootStr:1, offsets:[null,0,2,1,0,0], barre:{ offset:0, from:5, to:1 }, priority:2, tag:'A-form-2' },
  { type:'M9', rootStr:1, offsets:[null,0,-3,-3,-3,-3], barre:{ offset:-3, from:5, to:2 }, minRootFret:3, priority:4, tag:'A-form-3' },
  { type:'M9', rootStr:2, offsets:[null,null,0,2,2,0], barre:{ offset:0, from:5, to:2 }, priority:3, tag:'D-form' },
  { type:'M9', rootStr:2, offsets:[null,null,-1,-1,-2,0], barre:null, minRootFret:2, priority:5, tag:'inversion-M7bass', noRoot:true, note:'M9転回形（M7ベース・rootなし）' },
  { type:'M9', rootStr:2, offsets:[null,null,-5,-3,-5,-3], barre:{ offset:-5, from:4, to:2 }, minRootFret:5, priority:6, tag:'inversion-5thbass', noRoot:true, note:'M9転回形（5thベース・rootなし）' },
  { type:'M9', rootStr:2, offsets:[null,0,2,-1,2,null], barre:null, minRootFret:1, priority:7, tag:'inversion-5thbass-drop', noRoot:true, note:'M9転回形（5thベース・drop・rootなし）' },
  { type:'M9', rootStr:4, offsets:[null,null,4,6,4,6], barre:{ offset:4, from:4, to:2 }, minRootFret:1, priority:6, tag:'inversion-5thbass', noRoot:true, note:'M9転回形（5thベース・rootなし）' },
  { type:'M13', rootStr:0, offsets:[0,null,1,1,2,null], barre:null, priority:0, tag:'E-form-1' },
  { type:'M13', rootStr:0, offsets:[0,-1,-1,-1,0,-1], barre:{ offset:-1, from:5, to:1 }, minRootFret:3, priority:1, tag:'E-form-2' },
  { type:'M13', rootStr:1, offsets:[null,0,2,1,2,2], barre:{ offset:2, from:5, to:4 }, priority:2, tag:'A-form' },
  { type:'M13', rootStr:3, offsets:[null,null,4,0,0,0], barre:{ offset:0, from:5, to:3 }, minRootFret:1, priority:3, tag:'inversion-M7bass', note:'M13転回形（M7ベース）' },
  { type:'M13', rootStr:5, offsets:[null,null,-1,1,2,-1], barre:{ offset:-1, from:5, to:2 }, minRootFret:1, priority:4, tag:'inversion-13bass', noRoot:true, note:'M13転回形（13thベース・rootなし）' },
  { type:'M13', rootStr:2, offsets:[null,null,0,-1,0,-3], barre:null, minRootFret:3, priority:5, tag:'inversion-rootbass', note:'M13転回形（4弦Rootベース）' },
  { type:'M13', rootStr:3, offsets:[null,null,0,-1,0,0], barre:null, minRootFret:1, priority:6, tag:'inversion-5thbass', noRoot:true, note:'M13転回形（5thベース・rootなし）' },
  { type:'b13', rootStr:0, offsets:[0,null,0,1,1,null], barre:null, priority:0, tag:'E-form' },
  { type:'b13', rootStr:1, offsets:[null,0,-1,-2,-4,null], barre:null, minRootFret:4, priority:3, tag:'A-form-3' },
  { type:'b13', rootStr:1, offsets:[null,0,2,0,2,1], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form' },
  { type:'b13', rootStr:4, offsets:[null,0,1,0,0,null], barre:null, minRootFret:1, priority:4, tag:'inversion-b7bass', note:'b13第1転回形（b7ベース）' },
  { type:'b13', rootStr:5, offsets:[null,null,0,1,1,0], barre:null, minRootFret:1, priority:5, tag:'inversion-rootbass', note:'b13転回形（1弦Rootベース）' },
  { type:'13', rootStr:4, offsets:[null,0,1,1,0,null], barre:null, priority:4, tag:'inversion-b7bass' },
  { type:'13', rootStr:0, offsets:[0,2,0,1,2,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form-full' },
  { type:'13', rootStr:0, offsets:[0,null,0,1,2,null], barre:null, priority:1, tag:'E-form' },
  { type:'13', rootStr:1, offsets:[null,0,2,0,2,2], barre:{ offset:0, from:5, to:1 }, priority:2, tag:'A-form-1' },
  { type:'13', rootStr:1, offsets:[null,0,-1,0,0,2], barre:{ offset:0, from:4, to:3 }, priority:3, tag:'A-form-2' },
  { type:'13', rootStr:5, offsets:[null,null,0,1,2,0], barre:null, minRootFret:1, priority:5, tag:'inversion-rootbass', note:'13転回形（1弦Rootベース）' },
  { type:'13', rootStr:2, offsets:[null,null,-2,-3,-5,-5], barre:{ offset:-5, from:5, to:4 }, minRootFret:5, priority:6, tag:'inversion-b7bass', noRoot:true, note:'13転回形（b7ベース・rootなし）' },
  { type:'m11', rootStr:1, offsets:[null,0,0,0,1,0], barre:{ offset:0, from:5, to:1 }, priority:0, tag:'A-form-1' },
  { type:'m11', rootStr:0, offsets:[0,null,0,0,-2,null], barre:null, priority:1, tag:'E-form' },
  { type:'m11', rootStr:0, offsets:[0,0,0,0,0,2], barre:{ offset:0, from:4, to:0 }, priority:2, tag:'E-form-2' },
  { type:'m11', rootStr:1, offsets:[null,0,-2,0,0,-2], barre:{ offset:-2, from:5, to:2 }, priority:3, tag:'A-form-2' },
  { type:'m11', rootStr:2, offsets:[null,null,0,0,1,1], barre:{ offset:0, from:5, to:2 }, priority:4, tag:'D-form' },
  { type:'11', rootStr:0, offsets:[0,null,0,-1,-2,null], barre:null, priority:0, tag:'E-form' },
  { type:'11', rootStr:1, offsets:[null,0,0,0,0,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form-1' },
  { type:'11', rootStr:1, offsets:[null,0,null,0,0,-2], barre:null, priority:2, tag:'A-form-2' },
  { type:'11', rootStr:2, offsets:[null,null,0,0,1,0], barre:{ offset:0, from:5, to:2 }, priority:3, tag:'D-form' },
  { type:'11', rootStr:0, offsets:[0,null,0,1,-2,null], barre:null, minRootFret:2, priority:4, tag:'E-form-drop2', note:'11 Eフォームdrop2ボイシング' },
  { type:'11', rootStr:5, offsets:[null,0,0,1,0,0], barre:{ offset:0, from:5, to:1 }, minRootFret:1, priority:5, tag:'inversion-rootbass', note:'11転回形（1弦Rootベース・バレー）' },
  { type:'11', rootStr:3, offsets:[null,null,0,0,1,1], barre:{ offset:0, from:5, to:2 }, minRootFret:1, priority:6, tag:'inversion-rootbass', note:'11転回形（3弦Rootベース・バレー）' },
  { type:'m9', rootStr:1, offsets:[null,0,-2,0,0,null], barre:null, priority:0, tag:'A-form' },
  { type:'m9', rootStr:0, offsets:[0,2,0,0,0,2], barre:{ offset:0, from:5, to:0 }, priority:1, tag:'E-form' },
  { type:'m9', rootStr:2, offsets:[null,null,0,-2,1,0], barre:null, priority:2, tag:'D-form' },
  { type:'m9', rootStr:0, offsets:[0,null,0,0,0,2], barre:{ offset:0, from:5, to:2 }, minRootFret:1, priority:3, tag:'E-form-drop2', note:'m9 Eフォームdrop2ボイシング' },
  { type:'9', rootStr:0, offsets:[0,2,0,1,0,2], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form-1' },
  { type:'9', rootStr:0, offsets:[0,null,0,-1,0,null], barre:null, priority:1, tag:'E-form-2' },
  { type:'9', rootStr:1, offsets:[null,0,-1,0,0,0], barre:{ offset:0, from:5, to:3 }, priority:2, tag:'C-form' },
  { type:'9', rootStr:2, offsets:[null,null,0,-1,1,0], barre:null, priority:3, tag:'D-form' },
  { type:'9', rootStr:5, offsets:[null,null,0,-1,-3,0], barre:null, minRootFret:3, priority:4, tag:'inversion-rootbass', note:'9転回形（1弦Rootベース）' },
  { type:'9', rootStr:0, offsets:[0,null,0,-1,-3,null], barre:null, minRootFret:3, priority:5, tag:'E-form-drop2', note:'9 Eフォームdrop2ボイシング' },
  { type:'9', rootStr:4, offsets:[null,0,-1,-1,0,-1], barre:{ offset:-1, from:5, to:2 }, minRootFret:1, priority:6, tag:'inversion-b7bass', note:'9転回形（b7ベース）' },
  { type:'9', rootStr:2, offsets:[null,null,-2,-1,-2,0], barre:null, minRootFret:2, priority:7, tag:'inversion-b7bass', noRoot:true, note:'9転回形（b7ベース・rootなし）' },
  { type:'69', rootStr:0, offsets:[0,-1,-1,-1,0,0], barre:{ offset:-1, from:3, to:1 }, priority:0, tag:'E-form' },
  { type:'69', rootStr:1, offsets:[null,0,-1,-1,0,0], barre:{ offset:-1, from:3, to:2 }, priority:1, tag:'A-form' },
  { type:'69', rootStr:2, offsets:[null,null,0,-1,0,0], barre:null, priority:2, tag:'D-form' },
  { type:'7#9', rootStr:0, offsets:[0,-1,0,0,null,null], barre:null, priority:0, tag:'E-form' },
  { type:'7#9', rootStr:1, offsets:[null,0,-1,0,1,null], barre:null, priority:1, tag:'A-form' },
  { type:'7#9', rootStr:2, offsets:[null,null,0,-1,1,1], barre:{ offset:1, from:5, to:4 }, priority:2, tag:'D-form' },
  { type:'7', rootStr:0, offsets:[0,2,0,1,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'7', rootStr:1, offsets:[null,0,2,0,2,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form' },
  { type:'7', rootStr:2, offsets:[null,null,0,2,1,2], barre:null, priority:2, tag:'D-form' },
  { type:'7', rootStr:1, offsets:[null,0,-1,0,-2,null], barre:null, minRootFret:3, priority:3, tag:'C-form' },
  { type:'7', rootStr:4, offsets:[null,null,1,2,0,null], barre:null, minRootFret:1, priority:4, tag:'inversion-m3bass', note:'7第1転回形（m3ベース）' },
  { type:'7', rootStr:4, offsets:[null,null,1,2,0,2], barre:null, minRootFret:1, priority:5, tag:'inversion-m3bass-drop', note:'7第1転回形（m3ベース・5th付き）' },
  { type:'7', rootStr:1, offsets:[null,0,-1,0,null,null], barre:null, minRootFret:1, priority:6, tag:'inversion-rootbass', note:'7転回形（5弦Rootベース）' },
  { type:'7', rootStr:3, offsets:[null,2,3,0,3,null], barre:null, minRootFret:1, priority:7, tag:'inversion-3rdbass-drop', note:'7第1転回形（3rdベース・drop）' },
  { type:'7', rootStr:3, offsets:[null,null,0,0,0,1], barre:{ offset:0, from:4, to:2 }, minRootFret:1, priority:8, tag:'inversion-rootbass', note:'7転回形（3弦Rootベース・バレー）' },
  { type:'7', rootStr:0, offsets:[0,null,0,1,0,null], barre:null, minRootFret:1, priority:9, tag:'E-form-drop2', note:'7 Eフォームdrop2ボイシング' },
  { type:'7', rootStr:5, offsets:[null,null,0,1,0,0], barre:{ offset:0, from:5, to:2 }, minRootFret:1, priority:10, tag:'inversion-rootbass', note:'7転回形（1弦Rootベース・バレー）' },
  { type:'7', rootStr:2, offsets:[null,null,0,-1,-2,-4], barre:null, minRootFret:4, priority:11, tag:'inversion-rootbass-drop', note:'7転回形（4弦Rootベース・下降）' },
  { type:'7', rootStr:2, offsets:[null,0,0,-1,1,null], barre:null, minRootFret:1, priority:12, tag:'inversion-5thbass-drop', note:'7第2転回形（5thベース・drop）' },
  { type:'7', rootStr:4, offsets:[null,0,1,-1,0,null], barre:null, minRootFret:1, priority:13, tag:'inversion-rootbass', note:'7転回形（2弦Rootベース）' },
  { type:'dim', rootStr:0, offsets:[0,null,null,0,-1,0], barre:null, priority:0, tag:'E-form' },
  { type:'dim', rootStr:1, offsets:[null,0,1,2,1,null], barre:null, priority:0, tag:'A-form' },
  { type:'dim', rootStr:5, offsets:[null,null,null,0,-1,0], barre:null, minRootFret:1, priority:1, tag:'inversion-rootbass', note:'dim転回形（1弦Rootベース）' },
  { type:'dim', rootStr:3, offsets:[null,null,null,0,-1,-3], barre:null, minRootFret:3, priority:2, tag:'inversion-rootbass', note:'dim転回形（3弦Rootベース・下降）' },
  { type:'dim', rootStr:1, offsets:[null,0,1,null,1,null], barre:null, minRootFret:1, priority:3, tag:'inversion-rootbass', note:'dim転回形（5弦Rootベース）' },
  { type:'dim', rootStr:2, offsets:[null,null,0,1,null,1], barre:null, minRootFret:1, priority:4, tag:'inversion-rootbass', note:'dim転回形（4弦Rootベース）' },
  { type:'dim', rootStr:1, offsets:[null,0,-2,-4,null,null], barre:null, minRootFret:4, priority:5, tag:'inversion-rootbass', note:'dim転回形（5弦Rootベース・下降）' },
  { type:'mM7', rootStr:0, offsets:[0,2,1,0,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'mM7', rootStr:1, offsets:[null,0,-2,-3,-3,null], barre:null, minRootFret:3, priority:1, tag:'C-form' },
  { type:'mM7', rootStr:1, offsets:[null,0,2,1,1,0], barre:{ offset:0, from:5, to:1 }, priority:2, tag:'A-form' },
  { type:'mM7', rootStr:2, offsets:[null,null,0,2,2,1], barre:null, priority:3, tag:'D-form' },
  { type:'mM7', rootStr:5, offsets:[null,null,1,0,0,0], barre:{ offset:0, from:5, to:3 }, minRootFret:1, priority:4, tag:'inversion-rootbass', note:'mM7転回形（1弦Rootベース）' },
  { type:'mM7', rootStr:2, offsets:[null,null,0,-2,-2,-3], barre:null, minRootFret:3, priority:5, tag:'inversion-rootbass', note:'mM7転回形（4弦Rootベース）' },
  { type:'m6', rootStr:0, offsets:[0,2,2,0,2,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'m6', rootStr:0, offsets:[0,null,-1,0,0,null], barre:null, priority:1, tag:'E-form-2' },
  { type:'m6', rootStr:1, offsets:[null,0,-2,-1,-2,null], barre:{ offset:-2, from:4, to:2 }, minRootFret:1, priority:1, tag:'C-form' },
  { type:'m6', rootStr:1, offsets:[null,0,null,-1,1,0], barre:null, minRootFret:1, priority:3, tag:'C-form-3' },
  { type:'m6', rootStr:2, offsets:[null,null,0,2,0,1], barre:{ offset:0, from:4, to:2 }, priority:2, tag:'D-form' },
  { type:'m6', rootStr:4, offsets:[null,null,0,1,0,2], barre:{ offset:0, from:4, to:2 }, minRootFret:1, priority:4, tag:'inversion-m3bass', note:'m6第1転回形（m3ベース）' },
  { type:'m6', rootStr:1, offsets:[null,0,2,-1,1,null], barre:null, minRootFret:1, priority:5, tag:'A-form-drop', note:'m6 Aフォームdropボイシング' },
  { type:'m6', rootStr:3, offsets:[null,null,0,0,-1,0], barre:null, minRootFret:1, priority:6, tag:'inversion-rootbass', note:'m6転回形（3弦Rootベース）' },
  { type:'m6', rootStr:3, offsets:[null,1,2,0,3,null], barre:null, minRootFret:1, priority:7, tag:'inversion-m3bass-drop', note:'m6第1転回形（m3ベース・drop）' },
  { type:'m6', rootStr:5, offsets:[null,null,-1,0,0,0], barre:null, minRootFret:1, priority:8, tag:'inversion-rootbass', note:'m6転回形（1弦Rootベース）' },
  { type:'m6', rootStr:2, offsets:[null,0,0,-2,0,null], barre:null, minRootFret:2, priority:9, tag:'inversion-5thbass-drop', note:'m6第2転回形（5thベース・drop）' },
  { type:'6', rootStr:0, offsets:[0,null,2,1,2,null], barre:null, priority:0, tag:'E-form' },
  { type:'6', rootStr:1, offsets:[null,0,2,2,2,2], barre:{ offset:2, from:5, to:2 }, priority:3, tag:'A-form' },
  { type:'6', rootStr:2, offsets:[null,null,0,2,0,2], barre:{ offset:0, from:5, to:2 }, priority:2, tag:'D-form' },
  { type:'6', rootStr:0, offsets:[0,null,-1,1,0,null], barre:null, priority:1, tag:'E-form-2' },
  { type:'6', rootStr:1, offsets:[null,0,-1,-1,-2,null], barre:null, minRootFret:1, priority:1, tag:'C-form' },
  { type:'6', rootStr:2, offsets:[null,0,0,-1,0,null], barre:null, minRootFret:1, priority:4, tag:'inversion-rootbass', note:'6転回形（4弦Rootベース）' },
  { type:'6', rootStr:2, offsets:[null,null,0,-1,0,-2], barre:null, minRootFret:2, priority:5, tag:'inversion-rootbass', note:'6転回形（4弦Rootベース・4声）' },
  { type:'6', rootStr:3, offsets:[null,null,2,0,0,0], barre:{ offset:0, from:5, to:3 }, minRootFret:1, priority:6, tag:'inversion-rootbass', note:'6転回形（3弦Rootベース・バレー）' },
  { type:'aug', rootStr:0, offsets:[0,null,2,1,1,null], barre:null, priority:0, tag:'E-form' },
  { type:'aug', rootStr:2, offsets:[null,null,0,-1,-1,-2], barre:null, minRootFret:2, priority:1, tag:'D-form' },
  { type:'aug', rootStr:1, offsets:[null,0,-1,-2,-2,null], barre:{ offset:-2, from:4, to:3 }, minRootFret:1, priority:0, tag:'C-form' },
  { type:'aug', rootStr:3, offsets:[null,null,null,0,0,-1], barre:null, minRootFret:1, priority:2, tag:'inversion-rootbass', note:'aug転回形（3弦Rootベース）' },
  { type:'aug', rootStr:2, offsets:[null,null,0,-1,-1,null], barre:null, minRootFret:1, priority:3, tag:'inversion-#5bass', note:'aug転回形（#5ベース）' },
  { type:'aug', rootStr:1, offsets:[null,0,-1,-2,null,null], barre:null, minRootFret:2, priority:4, tag:'inversion-rootbass', note:'aug転回形（5弦Rootベース）' },
  { type:'m7b5', rootStr:0, offsets:[0,null,0,0,-1,null], barre:null, priority:0, tag:'E-form' },
  { type:'m7b5', rootStr:1, offsets:[null,0,1,0,1,null], barre:null, priority:1, tag:'A-form' },
  { type:'m7b5', rootStr:2, offsets:[null,null,0,1,1,1], barre:{ offset:1, from:5, to:3 }, priority:2, tag:'D-form' },
  { type:'m7b5', rootStr:1, offsets:[null,0,null,0,1,-1], barre:null, minRootFret:1, priority:3, tag:'A-form-compact', note:'m7b5コンパクトボイシング（5弦root）' },
  { type:'m7b5', rootStr:3, offsets:[null,null,-1,0,-1,1], barre:null, minRootFret:1, priority:4, tag:'inversion-rootbass', note:'m7b5転回形（3弦Rootベース）' },
  { type:'m7b5', rootStr:3, offsets:[null,1,3,0,2,null], barre:null, minRootFret:1, priority:5, tag:'inversion-m3bass-drop', note:'m7b5第1転回形（m3ベース・drop）' },
  { type:'m7b5', rootStr:2, offsets:[null,null,0,-2,-3,-4], barre:null, minRootFret:4, priority:6, tag:'inversion-rootbass', note:'m7b5転回形（4弦Rootベース・下降）' },
  { type:'m7b5', rootStr:2, offsets:[null,-1,0,-2,1,null], barre:null, minRootFret:2, priority:7, tag:'inversion-b5bass-drop', note:'m7b5第2転回形（b5ベース・drop）' },
  { type:'dim7', rootStr:0, offsets:[0,null,-1,0,-1,null], barre:{ offset:-1, from:4, to:2 }, priority:0, tag:'E-form' },
  { type:'dim7', rootStr:1, offsets:[null,0,1,-1,1,null], barre:null, priority:1, tag:'A-form' },
  { type:'dim7', rootStr:2, offsets:[null,null,0,1,0,1], barre:null, priority:2, tag:'D-form' },
  { type:'add9', rootStr:0, offsets:[0,2,4,1,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'add9', rootStr:2, offsets:[null,null,0,-1,-2,0], barre:null, minRootFret:2, priority:1, tag:'D-form' },
  { type:'add9', rootStr:2, offsets:[null,null,0,2,3,0], barre:{ offset:0, from:5, to:2 }, minRootFret:2, priority:2, tag:'D-form-2' },
  { type:'add9', rootStr:1, offsets:[null,0,2,2,0,0], barre:{ offset:0, from:5, to:1 }, priority:0, tag:'A-form' },
  { type:'add9', rootStr:5, offsets:[null,null,4,1,0,0], barre:{ offset:0, from:5, to:4 }, minRootFret:1, priority:3, tag:'inversion-9bass', note:'add9転回形（9thベース）' },
  { type:'add9', rootStr:5, offsets:[null,null,-3,-1,-3,0], barre:{ offset:-3, from:4, to:2 }, minRootFret:3, priority:4, tag:'inversion-5thbass', note:'add9転回形（5thベース）' },
  { type:'sus4', rootStr:0, offsets:[0,2,2,2,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'sus4', rootStr:1, offsets:[null,0,2,2,3,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form' },
  { type:'sus4', rootStr:4, offsets:[null,null,null,-1,0,0], barre:null, minRootFret:1, priority:2, tag:'inversion-5thbass', note:'sus4第2転回形（5thベース）' },
  { type:'sus4', rootStr:2, offsets:[null,null,0,0,-2,null], barre:null, minRootFret:2, priority:3, tag:'inversion-rootbass', note:'sus4転回形（4弦Rootベース）' },
  { type:'sus4', rootStr:3, offsets:[null,null,0,0,1,null], barre:{ offset:0, from:3, to:2 }, minRootFret:1, priority:4, tag:'inversion-5thbass', note:'sus4第2転回形（5thベース・バレー）' },
  { type:'sus4', rootStr:4, offsets:[null,null,2,-1,0,null], barre:null, minRootFret:1, priority:5, tag:'inversion-4thbass', note:'sus4第1転回形（4thベース）' },
  { type:'M7', rootStr:0, offsets:[0,2,1,1,0,0], barre:{ offset:0, from:5, to:0 }, priority:0, tag:'E-form' },
  { type:'M7', rootStr:1, offsets:[null,0,2,1,2,0], barre:{ offset:0, from:5, to:1 }, priority:1, tag:'A-form' },
  { type:'M7', rootStr:2, offsets:[null,null,0,2,2,2], barre:{ offset:2, from:5, to:3 }, priority:3, tag:'D-form' },
  { type:'M7', rootStr:2, offsets:[null,null,0,-1,-2,-3], minRootFret:2, priority:4, tag:'D-form-drop' },
  { type:'M7', rootStr:1, offsets:[null,0,-1,-3,-3,-3], barre:{ offset:-3, from:5, to:3 }, minRootFret:3, priority:2, tag:'C-form' },
  { type:'M7', rootStr:4, offsets:[null,null,1,3,0,2], barre:null, minRootFret:1, priority:5, tag:'inversion-3rdbass', note:'M7第1転回形（3rdベース）' },
  { type:'M7', rootStr:3, offsets:[null,null,0,0,0,2], barre:{ offset:0, from:4, to:2 }, minRootFret:1, priority:6, tag:'inversion-5thbass', note:'M7第2転回形（5thベース）' },
  { type:'M7', rootStr:0, offsets:[0,null,1,1,0,-1], barre:null, minRootFret:1, priority:7, tag:'E-form-drop2', note:'M7 Eフォームdrop2ボイシング' },
  { type:'M7', rootStr:3, offsets:[null,2,4,0,3,null], barre:null, minRootFret:1, priority:8, tag:'inversion-3rdbass-drop', note:'M7第1転回形（3rdベース・drop）' },
  { type:'M7', rootStr:5, offsets:[null,null,1,1,0,0], barre:{ offset:0, from:5, to:4 }, minRootFret:1, priority:9, tag:'inversion-rootbass', note:'M7転回形（1弦Rootベース）' },
  { type:'M7', rootStr:2, offsets:[null,0,0,-1,2,null], barre:null, minRootFret:1, priority:10, tag:'inversion-5thbass-drop', note:'M7第2転回形（5thベース・drop）' },
  { type:'M', rootStr:1, offsets:[null,0,-1,-3,-2,-3], barre:{ offset:-3, from:5, to:3 }, minRootFret:3, priority:2, tag:'C-form' },
  { type:'M', rootStr:0, offsets:[0,null,-3,-3,-3,null], barre:{ offset:-3, from:4, to:2 }, minRootFret:3, priority:3, tag:'C-form-high', note:'6弦root高フレットCフォーム型' },
  { type:'M', rootStr:4, offsets:[null,null,1,-1,0,-1], barre:{ offset:-1, from:5, to:3 }, minRootFret:1, priority:4, tag:'inversion-3rdbass', note:'Mトライアド第1転回形（3rdベース）' },
  { type:'M', rootStr:4, offsets:[null,null,null,-1,0,-1], barre:null, minRootFret:1, priority:5, tag:'inversion-5thbass', note:'Mトライアド第2転回形（5thベース）' },
  { type:'M', rootStr:3, offsets:[null,null,null,0,0,-2], barre:null, minRootFret:2, priority:6, tag:'inversion-rootbass', note:'Mトライアド第2転回形（Rootベース・高声部）' },
  { type:'M', rootStr:2, offsets:[null,null,0,-1,-2,null], barre:null, minRootFret:2, priority:9, tag:'inversion-rootbass-4str', note:'Mトライアド転回形（4弦Rootベース）' },
  { type:'M', rootStr:3, offsets:[null,null,0,0,0,null], barre:{ offset:0, from:4, to:2 }, minRootFret:1, priority:7, tag:'inversion-5thbass-barre', note:'Mトライアド第2転回形（5thベース・バレー）' },
  { type:'M', rootStr:5, offsets:[null,null,null,1,0,0], barre:{ offset:0, from:5, to:4 }, minRootFret:1, priority:8, tag:'inversion-3rdbass-high', note:'Mトライアド第1転回形（3rdベース・高声部）' },
];

const SINGLE_FORMS = [
  { root:'G', type:'M',    frets:[3,2,0,0,0,3],               tag:'open' },
  { root:'D', type:'M',    frets:[null,null,0,2,3,2],          tag:'open' },
  { root:'G', type:'6',    frets:[3,2,0,0,0,0], barre:null,    tag:'open' },
  { root:'C', type:'add9', frets:[null,3,2,0,3,0], barre:null, tag:'open' },
  { root:'D', type:'sus4', frets:[null,null,0,2,3,3],          tag:'open' },
  { root:'C', type:'sus4', frets:[null,3,3,0,1,1], barre:{ fret:1, from:5, to:4 }, tag:'open' },
  { root:'G', type:'sus4', frets:[3,3,0,0,1,3],                tag:'open' },
  { root:'C', type:'m',    frets:[null,3,1,0,1,null],          tag:'open' },
  { root:'B', type:'m7',   frets:[null,2,0,2,0,2],             tag:'open' },
];

/* ============================================================
   § 7. CHORD DB + CUSTOM DB
   ============================================================ */
function buildChordDB() {
  const db = {};
  function addPos(rootPc, typeId, raw) {
    const pos = makePos(raw);
    if (!validatePos(pos, rootPc, typeId)) return;
    const key = `${rootPc}-${typeId}`;
    (db[key] = db[key] || []).push(pos);
  }

  CHROMATIC.forEach(rootPc => {
    ALL_ROOT_SHAPES.forEach(shape => {
      if (shape.skipRoots?.map(canon).includes(canon(rootPc))) return;
      const { frets, barre } = movableToFrets(shape, rootPc);
      addPos(rootPc, shape.type, {
        frets,
        barre: shape.barre === null ? null : barre,
        priority: shape.priority ?? 0,
        scope: 'all',
        allowIntervals: shape.allowIntervals ?? [],
        tag: shape.tag ?? null,
        note: shape.note ?? null,
        noRoot: shape.noRoot ?? false,
      });
    });
  });

  SINGLE_FORMS.forEach(({ root:rootPc, type, frets, barre, priority, allowIntervals, tag, note, noRoot }) => {
    addPos(rootPc, type, {
      frets,
      barre: barre ?? null,
      priority: priority ?? 0,
      scope: 'single',
      allowIntervals: allowIntervals ?? [],
      tag: tag ?? null,
      note: note ?? null,
      noRoot: noRoot ?? false,
    });
  });

  const FORM_TAG_SCORE = { open: -2, 'inversion-b7bass': +14 };
  const barreScore = pos => {
    if (!pos.barre) return 0;
    const strings = Math.abs(pos.barre.from - pos.barre.to) + 1;
    const base = strings >= 6 ? 5 : strings >= 5 ? 4 : strings >= 4 ? 3 : 2;
    return base + (pos.barre.fret >= 7 ? 1 : 0);
  };
  const formQualityScore = pos => {
    const frets   = pos.frets;
    const pressed = frets.filter(f => typeof f === 'number' && f > 0);
    const maxF    = pressed.length ? Math.max(...pressed) : 0;
    const minF    = pressed.length ? Math.min(...pressed) : 0;
    const span    = maxF - minF;
    const openCnt = frets.filter(f => f === 0).length;
    const muteCnt = frets.filter(f => f == null).length;
    const hasLowRootGuess = frets[0] != null || frets[1] != null;
    return maxF*3 - openCnt*6 + span*2 + muteCnt*2 + barreScore(pos) - (hasLowRootGuess ? 3 : 0) + (FORM_TAG_SCORE[pos.tag] ?? 0);
  };

  Object.keys(db).forEach(key => {
    const [rootPc, ...rest] = key.split('-');
    const typeId = rest.join('-');
    const seen = new Set();
    db[key] = db[key].filter(p => {
      const fp = p.frets.map(f => f ?? 'x').join(',');
      if (seen.has(fp)) return false;
      seen.add(fp);
      return true;
    });
    db[key].sort((a,b) => formQualityScore(a) - formQualityScore(b));
    db[key].forEach((pos, i) => {
      pos.id = `${key}-${i}`;
      pos.tonePoints = buildTonePoints(pos.frets, rootPc, typeId);
    });
  });

  return db;
}
const CHORD_DB = buildChordDB();
const CUSTOM_FORM_DB = {};

/* ── localStorage 永続化 ── */
const CUSTOM_DB_STORAGE_KEY = 'guitar_chord_viewer_custom_forms_v1';
const CUSTOM_DB_VERSION = 1;

function serializeCustomDB() {
  const out = { version: CUSTOM_DB_VERSION, forms: {} };
  Object.keys(CUSTOM_FORM_DB).forEach(key => {
    out.forms[key] = CUSTOM_FORM_DB[key].map(pos => ({
      id: pos.id,
      frets: pos.frets,
      barre: pos.barre ?? null,
      customName: pos.customName ?? null,
      note: pos.note ?? 'ユーザー追加',
      createdAt: pos.createdAt ?? Date.now(),
      updatedAt: pos.updatedAt ?? Date.now(),
    }));
  });
  return out;
}
function persistCustomDB() {
  try { localStorage.setItem(CUSTOM_DB_STORAGE_KEY, JSON.stringify(serializeCustomDB())); }
  catch(err) { console.error('custom db save failed', err); }
}
function loadCustomDB() {
  try {
    const raw = localStorage.getItem(CUSTOM_DB_STORAGE_KEY);
    if (!raw) return;
    const parsed = JSON.parse(raw);
    if (!parsed || parsed.version !== CUSTOM_DB_VERSION || !parsed.forms) return;
    Object.keys(parsed.forms).forEach(key => {
      const [rootPc, ...rest] = key.split('-');
      const typeId = rest.join('-');
      const items = Array.isArray(parsed.forms[key]) ? parsed.forms[key] : [];
      CUSTOM_FORM_DB[key] = items.map(item => {
        const pos = makePos({
          frets: item.frets,
          barre: item.barre ?? undefined,
          priority: 0, scope: 'custom', allowIntervals: [],
          tag: 'custom', note: item.note ?? 'ユーザー追加',
        });
        if (!validatePos(pos, rootPc, typeId)) return null;
        pos.id = item.id || `custom-${key}-${Date.now()}-${Math.random().toString(36).slice(2,8)}`;
        pos.source = 'custom';
        pos.customName = item.customName ?? null;
        pos.createdAt = item.createdAt ?? Date.now();
        pos.updatedAt = item.updatedAt ?? pos.createdAt;
        pos.tonePoints = buildTonePoints(pos.frets, rootPc, typeId);
        return pos;
      }).filter(Boolean);
    });
  } catch(err) { console.error('custom db load failed', err); }
}

function getBassTonePoint(pos) {
  return pos?.tonePoints?.find(tp => tp.isBass) || null;
}
function isCustomForm(pos) { return pos?.source === 'custom'; }
function getInversionNameFromBass(rootSpell, typeId, bassIv) {
  const bassRole = getRoleByIv(bassIv, typeId);
  if (!bassRole) return '転回形';
  if (bassRole.name === '3' || bassRole.name === 'm3') return '第1転回形';
  if (bassRole.name === '5' || bassRole.name === '♭5' || bassRole.name === '♯5') return '第2転回形';
  if (bassRole.name === '♭7' || bassRole.name === 'M7' || bassRole.name === 'bb7') return '第3転回形';
  return `転回形 (${bassRole.name})`;
}
function sortStandardForms(forms) { return [...forms]; }
function sortInversionForms(forms) {
  const rank = roleName => {
    if (roleName === '3' || roleName === 'm3') return 0;
    if (roleName === '5' || roleName === '♭5' || roleName === '♯5') return 1;
    if (roleName === '♭7' || roleName === 'M7' || roleName === 'bb7') return 2;
    return 9;
  };
  return [...forms].sort((a,b) => {
    const ar = rank(getBassTonePoint(a)?.degree);
    const br = rank(getBassTonePoint(b)?.degree);
    if (ar !== br) return ar - br;
    const aMax = Math.max(...a.frets.filter(f => typeof f === 'number' && f >= 0), 99);
    const bMax = Math.max(...b.frets.filter(f => typeof f === 'number' && f >= 0), 99);
    return aMax - bMax;
  });
}
function sortCustomForms(forms) {
  return [...forms].sort((a, b) => (b.updatedAt || 0) - (a.updatedAt || 0));
}
// tag が 'inversion-' で始まるフォームは転回形タブ専用
const isInversionTagged = pos => typeof pos.tag === 'string' && pos.tag.startsWith('inversion-');

function getVisibleFormsByMode(forms, mode) {
  const custom    = forms.filter(f => isCustomForm(f));
  const nonCustom = forms.filter(f => !isCustomForm(f));

  // inversion タグ付きは転回形タブ専用
  const invForms = nonCustom.filter(f => isInversionTagged(f));
  const standard = nonCustom.filter(f => !isInversionTagged(f));

  if (mode === 'standard')  return sortStandardForms(standard);
  if (mode === 'inversion') return sortInversionForms(invForms);
  if (mode === 'custom')    return sortCustomForms(custom);

  return sortStandardForms(standard);
}
function getAllFormsForEntity(rootPc, typeId) {
  const key = `${rootPc}-${typeId}`;
  return [...(CHORD_DB[key] || []), ...(CUSTOM_FORM_DB[key] || [])];
}
function addCustomForm(rootPc, typeId, form) {
  const key = `${rootPc}-${typeId}`;
  const pos = makePos({
    frets: form.frets, barre: form.barre ?? undefined,
    priority: 0, scope: 'custom',
    allowIntervals: form.allowIntervals ?? [],
    tag: 'custom', note: form.note ?? 'ユーザー追加',
  });
  if (!validatePos(pos, rootPc, typeId)) return false;
  const list = CUSTOM_FORM_DB[key] || (CUSTOM_FORM_DB[key] = []);
  const now = Date.now();
  pos.id = `custom-${key}-${now}-${list.length}`;
  pos.source = 'custom';
  pos.customName = form.customName ?? null;
  pos.createdAt = now;
  pos.updatedAt = now;
  pos.tonePoints = buildTonePoints(pos.frets, rootPc, typeId);
  list.push(pos);
  persistCustomDB();
  return true;
}
function deleteCustomForm(rootPc, typeId, formId) {
  const key = `${rootPc}-${typeId}`;
  if (!CUSTOM_FORM_DB[key]) return;
  CUSTOM_FORM_DB[key] = CUSTOM_FORM_DB[key].filter(p => p.id !== formId);
  if (!CUSTOM_FORM_DB[key].length) delete CUSTOM_FORM_DB[key];
  persistCustomDB();
}
function updateCustomForm(rootPc, typeId, formId, updates) {
  const key = `${rootPc}-${typeId}`;
  const list = CUSTOM_FORM_DB[key];
  if (!list) return false;
  const idx = list.findIndex(p => p.id === formId);
  if (idx < 0) return false;
  const next = makePos({
    frets: updates.frets, barre: updates.barre ?? undefined,
    priority: 0, scope: 'custom', allowIntervals: [],
    tag: 'custom', note: updates.note ?? 'ユーザー追加',
  });
  if (!validatePos(next, rootPc, typeId)) return false;
  const prev = list[idx];
  next.id = prev.id;
  next.source = 'custom';
  next.customName = updates.customName ?? prev.customName ?? null;
  next.createdAt = prev.createdAt ?? Date.now();
  next.updatedAt = Date.now();
  next.tonePoints = buildTonePoints(next.frets, rootPc, typeId);
  list[idx] = next;
  persistCustomDB();
  return true;
}
function findCustomFormById(rootPc, typeId, formId) {
  const key = `${rootPc}-${typeId}`;
  return (CUSTOM_FORM_DB[key] || []).find(p => p.id === formId) || null;
}

/* ============================================================
   § 8. CHORD ENTITY
   ============================================================ */
function buildChordEntity(rootPc, typeId) {
  const forms = getAllFormsForEntity(rootPc, typeId);
  const comp  = buildComp(rootPc, typeId);
  const suffix = DISP_SUFFIX[typeId] ?? typeId;
  return { root: rootPc, typeId, label: `${rootPc}${suffix}`, comp, forms };
}

/* ============================================================
   § 9. STATE
   ============================================================ */
const S = {
  root: 'C', acc: '', type: 'M',
  selectedFormId: undefined, tab: 'notes', theme: 'dark',
  formMode: 'standard', currentEntity: null,
};
const isDesktop = () => window.innerWidth >= 1024;
const curRoot   = () => resolveRoot(S.root, S.acc);
const dispRoot  = () => S.acc==='#' ? `${S.root}♯` : S.acc==='b' ? `${S.root}♭` : S.root;

function resolveRoot(base, acc) {
  const sharp = { C:'C#',D:'D#',E:'F', F:'F#',G:'G#',A:'A#',B:'C' };
  const flat  = { C:'B', D:'C#',E:'D#',F:'E', G:'F#',A:'G#',B:'A#' };
  if (acc === '#') return sharp[base];
  if (acc === 'b') return flat[base];
  return base;
}
function resolveRootDisplay(base, acc) {
  if (acc === '#') {
    const sharp = { C:'C#', D:'D#', E:'E#', F:'F#', G:'G#', A:'A#', B:'B#' };
    return sharp[base] || base;
  }
  if (acc === 'b') {
    const flat = { C:'Cb', D:'Db', E:'Eb', F:'Fb', G:'Gb', A:'Ab', B:'Bb' };
    return flat[base] || base;
  }
  return base;
}
const curRootDisp = () => resolveRootDisplay(S.root, S.acc);
/* ── selection 整合性管理 ── */

// visibleForms に対して selectedFormId を正規化する
// - visibleForms が空 → null
// - selectedFormId が undefined → 未初期化、visibleForms[0].id を選ぶ
// - selectedFormId が null → 意図的解除、そのまま維持
// - selectedFormId が存在しない → visibleForms[0].id にフォールバック
function normalizeSelectedFormId(visibleForms) {
  if (visibleForms.length === 0) {
    S.selectedFormId = null;
    return;
  }
  if (S.selectedFormId === undefined) {
    S.selectedFormId = visibleForms[0].id;
    return;
  }
  if (S.selectedFormId === null) return;
  if (!visibleForms.some(f => f.id === S.selectedFormId)) {
    S.selectedFormId = visibleForms[0].id;
  }
}

// entity再構築 + selection正規化 + visible返却
function refreshCurrentEntityAndSelection() {
  S.currentEntity = buildChordEntity(curRoot(), S.type);
  const visible = getVisibleFormsByMode(S.currentEntity.forms, S.formMode);
  normalizeSelectedFormId(visible);
  return visible;
}

// 描画に必要な全コンテキストを一括取得
// renderDesktop / renderMobile / updateFretboard から呼ぶ唯一の取得口
function getSelectionContext() {
  const positions    = refreshCurrentEntityAndSelection();
  const entity       = S.currentEntity;
  const rootDisp     = curRootDisp();
  const typeId       = S.type;
  const label        = `${dispRoot()}${DISP_SUFFIX[typeId]??''}`;
  const comp         = entity.comp;
  const si           = S.tab === 'interval';
  const formMode     = S.formMode;
  const selectedFormId = S.selectedFormId;
  const selectedForm = positions.find(f => f.id === selectedFormId) || null;
  const selectedTps  = selectedForm?.tonePoints || null;
  return { entity, positions, selectedForm, selectedTps,
           rootDisp, label, comp, si, typeId, formMode, selectedFormId };
}

/* ============================================================
   § 10. THEMES
   ============================================================ */
const THEMES = {
  dark: {
    id:'dark', label:'ダーク', dot:'#c9a84c',
    bg:'#1a1a1a', surface:'#222', card:'#2a2a2a', border:'#383838',
    text:'#f0f0f0', muted:'#a0a0a0', faint:'#555',
    accent:'#c9a84c', accentFg:'#1a1a1a',
    nut:'#d4c5a0', fret:'#383838', string:'#4a4a4a',
  },
  parchment: {
    id:'parchment', label:'パーチメント', dot:'#c8b99a',
    bg:'#f0ead8', surface:'#f7f1e3', card:'#ede5d0', border:'#a89070',
    text:'#241a0e', muted:'#6a5540', faint:'#9a8060',
    accent:'#8b4513', accentFg:'#fff',
    nut:'#4a3728', fret:'#a89070', string:'#8a7050',
  },
};
function applyTheme(id) {
  const t = THEMES[id] || THEMES.dark, r = document.documentElement;
  r.style.setProperty('--bg',       t.bg);
  r.style.setProperty('--surface',  t.surface);
  r.style.setProperty('--card',     t.card);
  r.style.setProperty('--border',   t.border);
  r.style.setProperty('--text',     t.text);
  r.style.setProperty('--muted',    t.muted);
  r.style.setProperty('--faint',    t.faint);
  r.style.setProperty('--accent',   t.accent);
  r.style.setProperty('--accent-fg',t.accentFg);
  r.style.setProperty('--nut',      t.nut);
  r.style.setProperty('--fret',     t.fret);
  r.style.setProperty('--string',   t.string);
}

/* ============================================================
   § 11. RENDER HELPERS (diagram, string notes, fretboard)
   ============================================================ */
function getPrimaryRoot(pos, rootPc) {
  const played = pos.frets.map((f,s) => ({f,s})).filter(x => typeof x.f==='number' && x.f>=0);
  if (!played.length) return null;
  const loStr = Math.min(...played.map(x => x.s));
  const roots = played.filter(x => canon(noteAt(x.s, x.f)) === canon(rootPc));
  if (!roots.length) return null;
  return roots.find(r => r.s === loStr) || roots[0];
}

function renderDiagram(pos, rootSpell, typeId) {
  const rootPc = canon(rootSpell);
  const SYM_W=22, LABEL_H=28, PAD_T=14, PAD_R=14;
  const gridW=150, gridH=180;
  const W=SYM_W+gridW+PAD_R, H=PAD_T+gridH+LABEL_H;
  const PL=SYM_W, sf=startFret(pos.frets);
  const pf   = pos.frets.filter(f => typeof f==='number'&&f>0);
  const maxF = pf.length ? Math.max(...pf) : sf;
  const FRETS = Math.max(4, maxF-sf+1);
  const fGap=gridW/FRETS, sGap=gridH/5, DR=12;
  const sy = s => PAD_T + (5-s)*sGap;
  const fx = f => PL + (f-sf+0.5)*fGap;
  const lblY = PAD_T + gridH + LABEL_H*0.9;

  const tps = pos.tonePoints;
  const bassTp = tps ? tps.find(tp => tp.isBass) : null;
  const isInv = bassTp && !bassTp.isRoot;
  const bassDisp = isInv && bassTp ? spellNote(rootSpell, bassTp.intervalFromRoot, typeId) : null;
  const prim = isInv ? null : getPrimaryRoot(pos, rootPc);

  let h = `<svg width="${W}" height="${H}" viewBox="0 0 ${W} ${H}" style="display:block">`;
  if (sf===1) h += `<rect x="${PL-4}" y="${PAD_T}" width="5" height="${gridH}" rx="2" fill="var(--nut)"/>`;
  for (let i=0;i<=FRETS;i++) h += `<line x1="${PL+i*fGap}" y1="${PAD_T}" x2="${PL+i*fGap}" y2="${PAD_T+gridH}" stroke="var(--fret)" stroke-width="1.5"/>`;
  [5,4,3,2,1,0].forEach((s,idx) =>
    h += `<line x1="${PL}" y1="${sy(s)}" x2="${PL+gridW}" y2="${sy(s)}" stroke="var(--string)" stroke-width="${0.9+idx*0.3}"/>`
  );

  if (pos.barre) {
    const bx=fx(pos.barre.fret), yA=sy(pos.barre.from), yB=sy(pos.barre.to);
    const yT=Math.min(yA,yB), yBo=Math.max(yA,yB);
    h += `<rect x="${bx-DR}" y="${yT-DR}" width="${DR*2}" height="${yBo-yT+DR*2}" rx="${DR}" fill="#ef4444"/>`;
    if (!isInv) {
      const barreHasPrim = prim && prim.f===pos.barre.fret && prim.s>=pos.barre.to && prim.s<=pos.barre.from;
      if (barreHasPrim) {
        h += `<text x="${bx}" y="${sy(prim.s)}" text-anchor="middle" dominant-baseline="central" font-size="15" fill="#fff" font-weight="900">R</text>`;
        h += `<text x="${bx}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">${pos.barre.fret}f</text>`;
      }
    } else {
      const bassS = bassTp.stringIndex;
      const barreHasBass = bassS >= pos.barre.to && bassS <= pos.barre.from && bassTp.fret === pos.barre.fret;
      if (barreHasBass) {
        const fs = bassDisp.length > 2 ? 12 : 15;
        h += `<text x="${bx}" y="${sy(bassS)}" text-anchor="middle" dominant-baseline="central" font-size="${fs}" fill="#fff" font-weight="900">${bassDisp}</text>`;
        h += `<text x="${bx}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">${pos.barre.fret}f</text>`;
      }
    }
  }

  pos.frets.forEach((f, s) => {
    if (typeof f!=='number'||f<=0) return;
    if (pos.barre && f===pos.barre.fret && s>=pos.barre.to && s<=pos.barre.from) return;
    const isBassStr = isInv && bassTp && s===bassTp.stringIndex && f===bassTp.fret;
    const isPrim = !isInv && prim && s===prim.s && f===prim.f;
    const cx=fx(f), cy=sy(s), r=(isPrim||isBassStr)?DR*1.15:DR;
    h += `<circle cx="${cx}" cy="${cy}" r="${r}" fill="#ef4444"/>`;
    if (isPrim) {
      h += `<text x="${cx}" y="${cy}" text-anchor="middle" dominant-baseline="central" font-size="15" fill="#fff" font-weight="900">R</text>`;
      h += `<text x="${cx}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">${f}f</text>`;
    } else if (isBassStr) {
      const fs = bassDisp.length > 2 ? 12 : 15;
      h += `<text x="${cx}" y="${cy}" text-anchor="middle" dominant-baseline="central" font-size="${fs}" fill="#fff" font-weight="900">${bassDisp}</text>`;
      h += `<text x="${cx}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">${f}f</text>`;
    }
  });

  [5,4,3,2,1,0].forEach(s => {
    const f=pos.frets[s], mx=SYM_W*0.45, my=sy(s);
    const isPrimOpen = !isInv && prim && prim.s===s && prim.f===0;
    const isBassOpen = isInv && bassTp && s===bassTp.stringIndex && bassTp.fret===0;
    if (f==null||f<0) {
      h += `<text x="${mx}" y="${my+5}" text-anchor="middle" font-size="16" fill="var(--muted)" font-weight="700">×</text>`;
    } else if (f===0) {
      h += `<circle cx="${mx}" cy="${my}" r="7" fill="none" stroke="#ef4444" stroke-width="2.2"/>`;
      if (isPrimOpen) {
        h += `<text x="${mx}" y="${my}" text-anchor="middle" dominant-baseline="central" font-size="11" fill="#ef4444" font-weight="900">R</text>`;
        h += `<text x="${PL+fGap*0.5}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">0f</text>`;
      } else if (isBassOpen) {
        const fs = bassDisp.length > 2 ? 10 : 12;
        h += `<text x="${mx}" y="${my}" text-anchor="middle" dominant-baseline="central" font-size="${fs}" fill="#ef4444" font-weight="900">${bassDisp}</text>`;
        h += `<text x="${PL+fGap*0.5}" y="${lblY}" text-anchor="middle" font-size="13" fill="var(--accent)" font-weight="900">0f</text>`;
      }
    }
  });
  h += `</svg>`;
  return h;
}

function renderStringNotes(pos, rootSpell, typeId) {
  const rootPc = canon(rootSpell);
  const tps = pos.tonePoints || buildTonePoints(pos.frets, rootPc, typeId);
  const bassStr = tps.reduce((acc, tp) => tp.fret != null && (acc === null || tp.stringIndex < acc) ? tp.stringIndex : acc, null);
  let h = `<div class="string-notes">`;
  [5,4,3,2,1,0].forEach(s => {
    const tp = tps[s];
    const muted = tp.fret == null;
    const col = tp.degreeColor || 'var(--faint)';
    const isLo = !muted && s === bassStr;
    h += `<div class="sn-row">
      <div class="sn-box${isLo?' lowest':''}" style="background:${muted?'transparent':col+'28'};border:1.5px solid ${muted?'var(--border)':col+'99'};color:${muted?'var(--faint)':col}">
        ${muted ? '×' : spellNote(rootSpell, tp.intervalFromRoot, typeId)}
      </div>
      ${!muted && tp.degree ? `<span class="sn-role${tp.isRoot?' is-root':''}" style="color:${col}">${tp.degree}</span>` : ''}
    </div>`;
  });
  h += `</div>`;
  return h;
}

function renderFretboard(comp, rootSpell, typeId, showInterval, bigMode=false, selectedTps=null) {
  const rootPc = canon(rootSpell);
  const compIvSet = new Set(comp.map(({ iv }) => iv));
  const LAST=21, H=bigMode?130:220;
  const PL=bigMode?28:26, PR=10, PT=bigMode?14:24, PB=bigMode?22:32;
  const fGap=bigMode?(480-28-10)/15:36;
  const gridW=fGap*LAST, W=Math.ceil(gridW+PL+PR);
  const gridH=H-PT-PB, sGap=gridH/5;
  const DR=Math.min(bigMode?8:14, fGap*0.4);
  const sx=f=>PL+f*fGap, sy=s=>PT+(5-s)*sGap;

  const selSet = new Map();
  if (selectedTps) selectedTps.forEach(tp => { if (tp.fret != null) selSet.set(`${tp.stringIndex},${tp.fret}`, tp); });
  const hasSel = selSet.size > 0;
  let h = `<svg width="${bigMode?'100%':W}" viewBox="0 0 ${W} ${H}" style="display:block">`;
  h += `<defs><filter id="glow-r" x="-50%" y="-50%" width="200%" height="200%">
    <feGaussianBlur stdDeviation="2.5" result="blur"/>
    <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
  </filter></defs>`;
  h += `<rect x="${PL-3}" y="${PT}" width="4" height="${gridH}" fill="var(--nut)"/>`;
  for (let i=0;i<=LAST;i++) {
    const acc=i===3||i===5||i===7||i===9||i===12||i===15||i===17||i===19||i===21;
    h += `<line x1="${sx(i)}" y1="${PT}" x2="${sx(i)}" y2="${PT+gridH}" stroke="${acc?'#8a8a8a':'var(--fret)'}" stroke-width="${i===0?(bigMode?3:3.4):(acc?(bigMode?2:2.4):(bigMode?1.4:1.8))}"/>`;
  }
  [5,4,3,2,1,0].forEach((s,idx) =>
    h += `<line x1="${PL}" y1="${sy(s)}" x2="${PL+gridW}" y2="${sy(s)}" stroke="var(--string)" stroke-width="${(bigMode?.7:.8)+idx*(bigMode?.25:.3)}"/>`
  );
  for (let i=0;i<=LAST;i++) {
    const tx=i===0?PL-14:sx(i)-fGap/2;
    h += `<text x="${tx}" y="${H-3}" text-anchor="middle" font-size="${bigMode?8:9}" fill="${bigMode?'var(--muted)':'#fff'}" font-family="monospace" font-weight="600">${i}</text>`;
  }
  for (let s=0;s<6;s++) {
    for (let f=0;f<=LAST;f++) {
      const note=noteAt(s,f);
      const iv=(noteIdx(note)-noteIdx(rootPc)+12)%12;
      if (!compIvSet.has(iv)) continue;
      const role=getRoleByIv(iv,typeId);
      const isRoot=role&&role.name==='R';
      const dX=f===0?PL-14:sx(f)-fGap/2, dY=sy(s);
      const col=role?role.color:'var(--muted)';
      const lbl=showInterval?(role?role.name:'?'):spellNote(rootSpell,iv,typeId);
      const fs=lbl.length>2?DR*.92:DR*1.08;
      const selTp=hasSel?selSet.get(`${s},${f}`):null;
      const isSel=!!selTp;
      if (hasSel&&!isSel) {
        h += `<circle cx="${dX}" cy="${dY}" r="${DR}" fill="transparent" stroke="${col}" stroke-width="1.5" opacity="0.6"/>`;
        h += `<text x="${dX}" y="${dY+fs*.4}" text-anchor="middle" font-size="${fs}" fill="${col}" font-weight="700" opacity="0.6">${lbl}</text>`;
      } else if (isSel&&isRoot) {
        h += `<circle cx="${dX}" cy="${dY}" r="${DR*1.2}" fill="none" stroke="#ef4444" stroke-width="1.5" opacity="0.7" filter="url(#glow-r)"/>`;
        h += `<circle cx="${dX}" cy="${dY}" r="${DR}" fill="#ef4444" filter="url(#glow-r)"/>`;
        h += `<text x="${dX}" y="${dY+4}" text-anchor="middle" font-size="${bigMode?11:14}" fill="#fff" font-weight="900">R</text>`;
      } else if (isSel) {
        h += `<circle cx="${dX}" cy="${dY}" r="${DR}" fill="${col}"/>`;
        h += `<text x="${dX}" y="${dY+fs*.4}" text-anchor="middle" font-size="${fs}" fill="#fff" font-weight="800">${lbl}</text>`;
      } else {
        if (isRoot) {
          h += `<circle cx="${dX}" cy="${dY}" r="${DR*1.2}" fill="none" stroke="#ef4444" stroke-width="1.5" opacity="0.7" filter="url(#glow-r)"/>`;
          h += `<circle cx="${dX}" cy="${dY}" r="${DR}" fill="#ef4444" filter="url(#glow-r)"/>`;
          h += `<text x="${dX}" y="${dY+4}" text-anchor="middle" font-size="14" fill="#fff" font-weight="900">R</text>`;
        } else {
          h += `<circle cx="${dX}" cy="${dY}" r="${DR}" fill="#000" stroke="${col}" stroke-width="1.2"/>`;
          h += `<text x="${dX}" y="${dY+fs*.4}" text-anchor="middle" font-size="${fs}" fill="#fff" font-weight="800">${lbl}</text>`;
        }
      }
    }
  }
  h += `</svg>`;
  return h;
}

/* ============================================================
   § 12. HTML FRAGMENTS
   ============================================================ */
function buildCompHTML(comp, rootSpell, typeId) {
  return comp.map(({ iv }) => {
    const role = getRoleByIv(iv, typeId);
    const isR  = role && role.name === 'R';
    const col  = role ? role.color : 'var(--faint)';
    const name = spellNote(rootSpell, iv, typeId);
    return `<div class="comp-item">
      <div class="comp-note${isR?' is-root':''}" style="color:${col};background:${col}28">${name}</div>
      <div class="comp-role" style="color:${col}">${role ? role.name : ''}</div>
    </div>`;
  }).join('');
}

function buildDiagCardsHTML(positions, rootSpell, typeId, formMode, selectedFormId) {
  const rootPc   = canon(rootSpell);
  const activeId = selectedFormId || null;

  let addBtn = '';
  if (formMode === 'custom') {
    addBtn = `<div class="add-card" id="addCustomBtn">
      <span class="add-card-icon">＋</span>
      <span class="add-card-label">追加</span>
    </div>`;
  }

  let cardsHTML = '';
  if (!positions.length && formMode !== 'custom') {
    const emptyLabel =
      formMode === 'inversion' ? 'このコードの転回形フォームはまだありません' :
      'フォーム未登録';
    cardsHTML = `<div class="empty" style="padding:24px">${emptyLabel}</div>`;
  } else {
    cardsHTML = positions.map(pos => {
      let topLabel = '—', extraBadge = '';
      if (formMode === 'standard') {
        const pr = getPrimaryRoot(pos, rootPc);
        topLabel = pr ? `R ${6-pr.s}弦${pr.f}F` : '—';
      }
      if (formMode === 'inversion') {
        const bass = getBassTonePoint(pos);
        if (bass && bass.intervalFromRoot != null) {
          topLabel = getInversionNameFromBass(rootSpell, typeId, bass.intervalFromRoot);
          extraBadge = `<span class="meta-badge inversion">${bass.degree || 'bass'}</span>`;
        } else {
          topLabel = '転回形';
          extraBadge = `<span class="meta-badge inversion">bass</span>`;
        }
      }
      if (formMode === 'custom') {
        topLabel = pos.customName || '';
        extraBadge = `<span class="meta-badge custom">custom</span>`;
      }
      const isSelected = pos.id === activeId;
      const delBtnHTML = formMode === 'custom'
        ? `<button class="card-del-btn" data-del-id="${pos.id}" data-del-root="${rootPc}" data-del-type="${typeId}">×</button>
           <button class="card-edit-btn" data-edit-id="${pos.id}">✎</button>`
        : '';
      const topBadge = topLabel ? `<span class="meta-badge">${topLabel}</span>` : '';
      return `<div class="diag-card${isSelected?' selected':''}" data-form-id="${pos.id}">
        ${delBtnHTML}
        <div class="diag-card-meta">
          ${topBadge}
          ${extraBadge}
        </div>
        <div class="diagram-wrap">
          ${renderDiagram(pos,rootSpell,typeId)}
          ${renderStringNotes(pos,rootSpell,typeId)}
        </div>
      </div>`;
    }).join('');
  }

  return formMode === 'custom' ? cardsHTML + addBtn : cardsHTML;
}

// 左パネルUI状態専用スナップショット（副作用なし・読み出しのみ）
// renderButtons / buildThemeHTML はここから値を受け取る
// getSelectionContext（フォーム・描画文脈）とは分離して混ぜない
function getUIStateSnapshot() {
  return {
    root:  S.root,
    acc:   S.acc,
    type:  S.type,
    theme: S.theme,
  };
}

function buildThemeHTML(theme) {
  return Object.values(THEMES).map(t => {
    const bg = t.id==='dark' ? '#1a1a1a' : t.dot;
    const bd = t.id==='dark' ? '#c9a84c' : 'transparent';
    return `<button class="theme-btn${theme===t.id?' active':''}" data-theme="${t.id}" title="${t.label}" style="background:${bg};border-color:${bd}"></button>`;
  }).join('');
}

const tabBtnsPC = si =>
  `<button class="pc-tab-btn${!si?' active':''}" data-tab="notes">音名</button>
   <button class="pc-tab-btn${si?' active':''}" data-tab="interval">度数</button>`;
const tabBtnsMB = si =>
  `<button class="tab${!si?' active':''}" data-tab="notes" style="border-radius:8px;flex:1">音名</button>
   <button class="tab${si?' active':''}" data-tab="interval" style="border-radius:8px;flex:1">度数</button>`;
const formModeBtnsPC = (mode, invCount) => {
  const invStyle = invCount === 0 ? ' style="color:var(--faint)"' : '';
  return `<button class="pc-tab-btn${mode==='standard'?' active':''}" data-form-mode="standard">標準</button>
   <button class="pc-tab-btn${mode==='inversion'?' active':''}" data-form-mode="inversion"${invStyle}>転回形</button>
   <button class="pc-tab-btn${mode==='custom'?' active':''}" data-form-mode="custom">カスタム</button>`;
};
const formModeBtnsMB = (mode, invCount) => {
  const baseStyle = 'border-radius:8px;flex:1';
  const invStyle  = invCount === 0 ? `${baseStyle};color:var(--faint)` : baseStyle;
  return `<button class="tab${mode==='standard'?' active':''}" data-form-mode="standard" style="${baseStyle}">標準</button>
   <button class="tab${mode==='inversion'?' active':''}" data-form-mode="inversion" style="${invStyle}">転回形</button>
   <button class="tab${mode==='custom'?' active':''}" data-form-mode="custom" style="${baseStyle}">カスタム</button>`;
};

/* ============================================================
   § 13. PARTIAL UPDATE
   ============================================================ */

// カード selected クラスの付け外しを専任する関数
// [data-form-id] の selected 状態を selectedFormId に合わせて同期する
function updateSelectedCardUI(selectedFormId) {
  document.querySelectorAll('[data-form-id]').forEach(el =>
    el.classList.toggle('selected', el.dataset.formId === selectedFormId)
  );
}

// 再同期込みで指板表示を更新する
// 注: 内部で getSelectionContext() → refreshCurrentEntityAndSelection() を呼ぶため
//     「指板だけ」ではなく「状態整流 + 指板 DOM 差し替え」を兼ねた関数
function updateFretboard() {
  const { comp, rootDisp, typeId, si, selectedTps } = getSelectionContext();
  if (isDesktop()) {
    const fb=document.getElementById('pc-fretboard');
    const tt=document.getElementById('pc-fb-title');
    const tb=document.getElementById('pc-tab-btns');
    if (fb) fb.innerHTML = renderFretboard(comp, rootDisp, typeId, si, true, selectedTps);
    if (tt) tt.textContent = si ? 'INTERVALS' : 'NOTES ON FRETBOARD';
    if (tb) tb.innerHTML = tabBtnsPC(si);
  } else {
    const fb=document.getElementById('mb-fretboard');
    const tb=document.getElementById('mb-tab-btns');
    if (fb) fb.innerHTML = renderFretboard(comp, rootDisp, typeId, si, false, selectedTps);
    if (tb) tb.innerHTML = tabBtnsMB(si);
  }
  bind();
}

/* ============================================================
   § 14. LAYOUT RENDERERS
   ============================================================ */
function renderDesktop() {
  const el = document.getElementById('app-pc'); if (!el) return;
  const ctx = getSelectionContext();
  const { entity, positions, label, comp, rootDisp, typeId, si, selectedTps, formMode, selectedFormId } = ctx;
  const allForms = entity?.forms ?? [];
  const invCount = getVisibleFormsByMode(allForms, 'inversion').length;
  el.innerHTML = `<div class="pc-result">
    <div class="pc-header">
      <div class="chord-name">${label}</div>
      <div class="comp-wrap">
        <div class="comp-label">構成音</div>
        <div class="comp-list">${buildCompHTML(comp,rootDisp,typeId)}</div>
      </div>
    </div>
    <div class="pc-fretboard-wrap" style="padding-bottom:10px">
      <div class="pc-fb-header">
        <div class="pc-fb-title">FORM MODE</div>
        <div class="pc-tab-row">${formModeBtnsPC(formMode, invCount)}</div>
      </div>
    </div>
    <div class="diag-scroll">
      <div class="diag-row">${buildDiagCardsHTML(positions,rootDisp,typeId,formMode,selectedFormId)}</div>
    </div>
    <div class="pc-fretboard-wrap">
      <div class="pc-fb-header">
        <div id="pc-fb-title" class="pc-fb-title">${si?'INTERVALS':'NOTES ON FRETBOARD'}</div>
        <div id="pc-tab-btns" class="pc-tab-row">${tabBtnsPC(si)}</div>
      </div>
      <div id="pc-fretboard">${renderFretboard(comp,rootDisp,typeId,si,true,selectedTps)}</div>
    </div>
  </div>`;
}

function renderMobile() {
  const el = document.getElementById('app-mb'); if (!el) return;
  const ctx = getSelectionContext();
  const { entity, positions, label, comp, rootDisp, typeId, si, selectedTps, formMode, selectedFormId } = ctx;
  const { theme } = getUIStateSnapshot();
  const allForms = entity?.forms ?? [];
  const invCount = getVisibleFormsByMode(allForms, 'inversion').length;
  el.innerHTML = `<div class="card">
    <div class="card-head">
      <div class="chord-name">${label}</div>
      <div class="comp-wrap">
        <div class="comp-label">構成音</div>
        <div class="comp-list">${buildCompHTML(comp,rootDisp,typeId)}</div>
      </div>
    </div>
    <div class="mb-tab-row">${formModeBtnsMB(formMode, invCount)}</div>
    <div class="diag-scroll">
      <div class="diag-row">${buildDiagCardsHTML(positions,rootDisp,typeId,formMode,selectedFormId)}</div>
    </div>
    <div class="fb-wrap" id="mb-fretboard">${renderFretboard(comp,rootDisp,typeId,si,false,selectedTps)}</div>
    <div class="mb-tab-row" id="mb-tab-btns">${tabBtnsMB(si)}</div>
    <div class="mb-theme-row">${buildThemeHTML(theme)}</div>
  </div>`;
}

/* ============================================================
   § 15. BUTTONS
   ============================================================ */
function renderButtons() {
  const { root, acc, type, theme } = getUIStateSnapshot();
  const d = isDesktop();
  const rootH = NATURALS.map(r =>
    `<button class="btn root${root===r?' active':''}" data-root="${r}">${r}</button>`).join('');
  const accH = [{id:'b',lbl:'♭ 半音下'},{id:'#',lbl:'♯ 半音上'}].map(x => {
    const noop = isNoopAcc(root, x.id);
    const cls  = `btn acc${acc===x.id?' active':''}`;
    const style = noop ? ' style="color:var(--faint);cursor:default"' : '';
    return `<button class="${cls}" data-acc="${x.id}"${style}>${x.lbl}</button>`;
  }).join('');
  const typeHFlat = CHORD_TYPES.map(t =>
    `<button class="btn type${type===t.id?' active':''}" data-type="${t.id}">${t.label}</button>`).join('');
  const typeHCat = TYPE_CATS.map(cat => {
    const btns = cat.ids.map(id => {
      const t = CHORD_TYPES.find(x => x.id===id); if (!t) return '';
      return `<button class="btn type${type===t.id?' active':''}" data-type="${t.id}">${t.label}</button>`;
    }).join('');
    return `<div class="pc-cat-label">${cat.label}</div><div class="pc-type-row">${btns}</div>`;
  }).join('');
  const set = (id, html) => { const el=document.getElementById(id); if(el) el.innerHTML=html; };
  if (d) {
    set('rootRow-pc', rootH); set('accRow-pc', accH);
    set('typeGrid-pc', typeHCat); set('themeRow-pc', buildThemeHTML(theme));
  } else {
    set('rootRow-mb', rootH); set('accRow-mb', accH); set('typeGrid-mb', typeHFlat);
  }
}

/* ============================================================
   § 16. MAIN RENDER & BIND
   ============================================================ */
function renderApp() {
  renderButtons();
  if (isDesktop()) renderDesktop();
  else renderMobile();
  bind();
}

function bind() {
  document.querySelectorAll('[data-root]').forEach(el =>
    el.onclick = () => {
      S.root=el.dataset.root;
      if(isNoopAcc(S.root,S.acc)) S.acc='';
      S.selectedFormId=undefined;
      refreshCurrentEntityAndSelection();
      renderApp();
    });
  document.querySelectorAll('[data-acc]').forEach(el =>
    el.onclick = () => {
      const next=S.acc===el.dataset.acc?'':el.dataset.acc;
      S.acc=isNoopAcc(S.root,next)?'':next;
      S.selectedFormId=undefined;
      refreshCurrentEntityAndSelection();
      renderApp();
    });
  document.querySelectorAll('[data-type]').forEach(el =>
    el.onclick = () => {
      S.type=el.dataset.type;
      S.selectedFormId=undefined;
      refreshCurrentEntityAndSelection();
      renderApp();
    });
  document.querySelectorAll('[data-theme]').forEach(el =>
    el.onclick = () => { S.theme=el.dataset.theme; applyTheme(S.theme); renderApp(); });
  document.querySelectorAll('[data-tab]').forEach(el =>
    el.onclick = () => { S.tab=el.dataset.tab; updateFretboard(); });
  document.querySelectorAll('[data-form-mode]').forEach(el =>
    el.onclick = () => {
      S.formMode=el.dataset.formMode;
      S.selectedFormId=undefined;
      refreshCurrentEntityAndSelection();
      renderApp();
    });
  document.querySelectorAll('[data-form-id]').forEach(el => {
    el.onclick = e => {
      if (e.target.closest('[data-del-id]')) return;
      if (e.target.closest('[data-edit-id]')) return;
      // 1. selectedFormId 更新（同じカード再タップで null に戻す）
      const fid = el.dataset.formId;
      S.selectedFormId = (S.selectedFormId === fid) ? null : fid;
      // 2. カード selected クラスを同期
      updateSelectedCardUI(S.selectedFormId);
      // 3. 指板を再同期 + 更新
      updateFretboard();
    };
  });

  // 削除ボタン
  document.querySelectorAll('[data-del-id]').forEach(el => {
    el.onclick = e => {
      e.stopPropagation();
      if (!confirm('このカスタムフォームを削除しますか？')) return;
      const { delId, delRoot, delType } = el.dataset;
      deleteCustomForm(delRoot, delType, delId);
      S.selectedFormId=undefined;
      refreshCurrentEntityAndSelection();
      renderApp();
    };
  });

  // 編集ボタン
  document.querySelectorAll('[data-edit-id]').forEach(el => {
    el.onclick = e => {
      e.stopPropagation();
      const pos = findCustomFormById(curRoot(), S.type, el.dataset.editId);
      if (pos) openBuilderForEdit(pos);
    };
  });

  // カスタム追加ボタン
  const addBtn = document.getElementById('addCustomBtn');
  if (addBtn) addBtn.onclick = openBuilderForCreate;
}

/* ============================================================
   § 17. CUSTOM BUILDER — state machine
   ============================================================ */

/*
  ── Builder State Machine ──

  States:
    IDLE        : builder は閉じている。CB は初期値。
    OPEN_CREATE : 新規作成モードで builder が開いている。
    OPEN_EDIT   : 既存フォームの編集モードで builder が開いている。

  Transitions:
    IDLE        --openBuilderForCreate()-->  OPEN_CREATE
    IDLE        --openBuilderForEdit(pos)--> OPEN_EDIT
    OPEN_CREATE --commitBuilder(name)----->  IDLE  (保存成功 → 本体 renderApp)
    OPEN_EDIT   --commitBuilder(name)----->  IDLE  (上書き保存 → 本体 renderApp)
    OPEN_*      --cancelBuilder()--------->  IDLE  (×ボタン / overlay クリック)
    OPEN_*      --clearBuilderPlacement()-> OPEN_* (指板配置だけリセット。mode は維持)

  Rule: CB.mode は BUILDER_MODE の値のみ許可。
        それ以外の文字列を直接代入しない。

  ── Lifecycle 監査チェックリスト ──
  変更時は以下8項目を確認すること:
  [1] create 開始    : openBuilderForCreate → resetBuilderState (IDLE) → OPEN_CREATE
  [2] edit 開始      : openBuilderForEdit   → CB.mode=EDIT, editingId 設定 → OPEN_EDIT
  [3] clear          : clearBuilderPlacement → placed/startFret リセット、mode 維持
  [4] cancel         : cancelBuilder → overlay 閉じる → resetBuilderState (IDLE)
  [5] save 成功      : commitBuilder → 退避 → cancelBuilder(IDLE) → 本体更新
  [6] save 失敗      : commitBuilder → null 返却、state は OPEN_* のまま変化なし
  [7] delete 後      : cancelBuilder は不要（builder は閉じている）、本体だけ更新
  [8] root/type 変更後に builder を開いた場合
                     : getBuilderContext() は常に curRoot()/S.type を読むため自動追従
*/

/* ── Builder 状態定数（IDLE を含む完全体） ── */
const BUILDER_MODE = Object.freeze({
  IDLE:   'idle',
  CREATE: 'create',
  EDIT:   'edit',
});

/* ── CB: builder 操作状態 ── */
const CB = {
  mode:      BUILDER_MODE.IDLE,            // BUILDER_MODE の値のみ。初期は IDLE
  editingId: null,                         // edit 時の form id（create / idle 時は null）
  placed:    new Array(6).fill(undefined), // undefined=未配置 null=ミュート 0=開放 n=フレット
  startFret: 1,
};
const CB_MAX_FRET = 15;
const CB_FRETS    = 5;

/* SVG consts */
const CB_W=320, CB_H=200, CB_SYM_W=30, CB_PAD_T=14, CB_PAD_R=12, CB_LABEL_H=24;
const CB_gridW=CB_W-CB_SYM_W-CB_PAD_R, CB_gridH=CB_H-CB_PAD_T-CB_LABEL_H;
const CB_fGap=CB_gridW/CB_FRETS, CB_sGap=CB_gridH/5, CB_DR=11, CB_PL=CB_SYM_W;
const cbSy = s => CB_PAD_T + (5-s)*CB_sGap;
const cbFx = f => CB_PL + (f - CB.startFret + 0.5) * CB_fGap;

// ── Builder Context ──
// builder専用文脈スナップショット（副作用なし・読み出しのみ）
// getSelectionContext（本体描画）/ getUIStateSnapshot（左パネル）とは分離する
function getBuilderContext() {
  const rootPc   = curRoot();
  const rootSpell = curRootDisp();
  const rootLabel = dispRoot();
  const typeId    = S.type;
  const typeLabel = DISP_SUFFIX[typeId] ?? typeId;
  const comp      = buildComp(rootPc, typeId);
  const compIvs   = TYPE_MAP[typeId]?.intervals || [];
  return { rootPc, rootSpell, rootLabel, typeId, typeLabel, comp, compIvs };
}

// ── CB 状態操作プリミティブ ──

// IDLE 値に戻す（DOM は触らない）
// cancelBuilder の内部で呼ぶ。直接呼ぶ場合は overlay が閉じていることを確認すること
function resetBuilderState() {
  CB.mode      = BUILDER_MODE.IDLE;
  CB.editingId = null;
  CB.placed    = new Array(6).fill(undefined);
  CB.startFret = 1;
}

// 指板上の配置だけクリア（OPEN_* → OPEN_*）
// mode / editingId は維持するため、編集中のフォームは失われない
function clearBuilderPlacement() {
  CB.placed    = new Array(6).fill(undefined);
  CB.startFret = 1;
  cbUpdate();
}

// モーダル表示の共通後処理（title セット → cbRenderComp → cbUpdate → overlay 開く）
// openBuilderForCreate / openBuilderForEdit からのみ呼ぶ
function showBuilderModal(title) {
  document.getElementById('cbTitle').textContent = title;
  document.getElementById('cbErr').textContent   = '';
  cbRenderComp();
  cbUpdate();
  document.getElementById('cbOverlay').classList.add('open');
  document.body.style.overflow = 'hidden';
}

// ── ライフサイクル関数 ──

// IDLE → OPEN_CREATE
function openBuilderForCreate() {
  resetBuilderState();
  CB.mode = BUILDER_MODE.CREATE;
  document.getElementById('cbNameInput').value = '';
  showBuilderModal('CUSTOM FORM');
}

// IDLE → OPEN_EDIT
function openBuilderForEdit(pos) {
  CB.mode      = BUILDER_MODE.EDIT;
  CB.editingId = pos.id;
  CB.placed    = pos.frets.map(f => f == null ? null : f);
  const pressed = pos.frets.filter(f => typeof f === 'number' && f > 0);
  CB.startFret = pressed.length
    ? Math.max(1, Math.min(Math.min(...pressed), CB_MAX_FRET))
    : 1;
  document.getElementById('cbNameInput').value = pos.customName || '';
  showBuilderModal('EDIT CUSTOM FORM');
}

// OPEN_* → IDLE（×ボタン / overlay クリック）
// state を IDLE へ戻し、モーダルを閉じる
function cancelBuilder() {
  document.getElementById('cbOverlay').classList.remove('open');
  document.body.style.overflow = '';
  resetBuilderState();
}
// closeBuilder は cancelBuilder の別名として維持（bind 内で使用）
const closeBuilder = cancelBuilder;

// OPEN_* → IDLE（保存成功）
// mode / editingId を退避 → cancelBuilder で state を IDLE へ → 本体更新
function commitBuilder(customName) {
  const { rootPc, typeId } = getBuilderContext();
  const frets = [...CB.placed].map(f => f === undefined ? null : f);
  const barre = normBarre(frets.map(f => f === null ? null : f), null);
  const payload = { frets, barre, customName };

  // cancelBuilder が resetBuilderState を呼ぶ前に退避
  const wasEdit   = CB.mode === BUILDER_MODE.EDIT;
  const editingId = CB.editingId;

  let ok = false;
  if (wasEdit && editingId) {
    ok = updateCustomForm(rootPc, typeId, editingId, payload);
  } else {
    ok = addCustomForm(rootPc, typeId, payload);
  }
  if (!ok) return null; // validation 失敗（エラー表示は呼び出し側）

  cancelBuilder(); // モーダルを閉じ state を IDLE へ

  // 本体選択を更新（edit 時は編集した id を優先、create 時は undefined → normalize 先頭へ）
  S.formMode       = 'custom';
  S.selectedFormId = wasEdit && editingId ? editingId : undefined;
  refreshCurrentEntityAndSelection();
  renderApp();
  return ok;
}

// builder内の音名情報取得（getBuilderContext経由）
function cbNoteInfo(note, bctx) {
  const { rootPc, rootSpell, typeId } = bctx;
  const iv = (noteIdx(note) - noteIdx(rootPc) + 12) % 12;
  const role = getRoleByIv(iv, typeId);
  const spelled = spellNote(rootSpell, iv, typeId);
  return { iv, role, spelled };
}

function cbRenderFB() {
  const svg = document.getElementById('cb-svg');
  if (!svg) return;
  const bctx = getBuilderContext();
  const { rootPc, typeId, compIvs } = bctx;
  const compNotes = new Set(
    compIvs.map(iv => CHROMATIC[(noteIdx(rootPc)+iv+120)%12])
  );
  const { placed, startFret } = CB;
  let h = '';

  // nut
  if (startFret === 1)
    h += `<rect x="${CB_PL-4}" y="${CB_PAD_T}" width="5" height="${CB_gridH}" rx="2" fill="var(--nut)"/>`;

  // frets
  for (let i=0; i<=CB_FRETS; i++) {
    const acc = [3,5,7,9,12].includes(startFret+i);
    h += `<line x1="${CB_PL+i*CB_fGap}" y1="${CB_PAD_T}" x2="${CB_PL+i*CB_fGap}" y2="${CB_PAD_T+CB_gridH}" stroke="${acc?'#7a7a7a':'var(--fret)'}" stroke-width="${i===0?3.5:(acc?2:1.5)}"/>`;
  }
  // strings
  [5,4,3,2,1,0].forEach((s,idx) =>
    h += `<line x1="${CB_PL}" y1="${cbSy(s)}" x2="${CB_PL+CB_gridW}" y2="${cbSy(s)}" stroke="var(--string)" stroke-width="${0.9+idx*0.28}"/>`
  );
  // fret labels
  for (let i=0; i<=CB_FRETS; i++) {
    const tx = i===0 ? CB_PL-15 : CB_PL+i*CB_fGap-CB_fGap/2;
    h += `<text x="${tx}" y="${CB_H-4}" text-anchor="middle" font-size="9" fill="var(--muted)" font-family="monospace">${startFret+i-1}</text>`;
  }

  // 弦名ラベル
  for (let s=0; s<6; s++) {
    if (placed[s] !== undefined) continue;
    const mx = CB_SYM_W*0.45, my = cbSy(s);
    h += `<text x="${mx}" y="${my+4}" text-anchor="middle" font-size="9" fill="var(--faint)" font-weight="700" class="cb-str-tap" data-s="${s}" style="cursor:pointer">${6-s}</text>`;
  }

  // GHOST DOTS
  for (let s=0; s<6; s++) {
    if (placed[s] !== undefined) continue;
    // 開放弦
    const note0 = noteAt(s, 0);
    if (compNotes.has(note0)) {
      const { role, spelled } = cbNoteInfo(note0, bctx);
      if (role) {
        const mx=CB_SYM_W*0.45, my=cbSy(s), col=role.color;
        const fs=spelled.length>2?7.5:9;
        h += `<circle cx="${mx}" cy="${my}" r="9" fill="${col}20" stroke="${col}88" stroke-width="1.5" class="cb-ghost" data-s="${s}" data-f="0" style="cursor:pointer"/>`;
        h += `<text x="${mx}" y="${my+3.5}" text-anchor="middle" font-size="${fs}" fill="${col}cc" font-weight="800" pointer-events="none">${spelled}</text>`;
      }
    }
    // フレット上
    for (let i=0; i<CB_FRETS; i++) {
      const f = startFret + i;
      const note = noteAt(s, f);
      if (!compNotes.has(note)) continue;
      const { role, spelled } = cbNoteInfo(note, bctx);
      if (!role) continue;
      const cx=cbFx(f), cy=cbSy(s), col=role.color;
      const fs=spelled.length>2?CB_DR*0.72:CB_DR*0.88;
      h += `<circle cx="${cx}" cy="${cy}" r="${CB_DR}" fill="${col}20" stroke="${col}88" stroke-width="1.5" class="cb-ghost" data-s="${s}" data-f="${f}" style="cursor:pointer"/>`;
      h += `<text x="${cx}" y="${cy+fs*0.38}" text-anchor="middle" font-size="${fs}" fill="${col}cc" font-weight="800" pointer-events="none">${spelled}</text>`;
    }
  }

  // PLACED DOTS
  for (let s=0; s<6; s++) {
    const f = placed[s];
    if (f === undefined) continue;
    const mx=CB_SYM_W*0.45, my=cbSy(s);

    if (f === null) {
      h += `<text x="${mx}" y="${my+5}" text-anchor="middle" font-size="18" fill="#22c55e" font-weight="700" class="cb-placed-tap" data-s="${s}" style="cursor:pointer">×</text>`;
    } else if (f === 0) {
      const note=noteAt(s,0);
      const { role, spelled } = cbNoteInfo(note, bctx);
      const isR=role&&role.name==='R', col=role?role.color:'#888';
      if (isR) {
        h += `<circle cx="${mx}" cy="${my}" r="12" fill="${col}22" class="cb-placed-tap" data-s="${s}" style="cursor:pointer"/>`;
        h += `<circle cx="${mx}" cy="${my}" r="10" fill="none" stroke="${col}" stroke-width="3" pointer-events="none"/>`;
        h += `<text x="${mx}" y="${my+4}" text-anchor="middle" font-size="9" fill="${col}" font-weight="900" pointer-events="none">R</text>`;
      } else {
        const fs=spelled.length>2?7:9;
        h += `<circle cx="${mx}" cy="${my}" r="11" fill="transparent" class="cb-placed-tap" data-s="${s}" style="cursor:pointer"/>`;
        h += `<circle cx="${mx}" cy="${my}" r="9" fill="none" stroke="${col}" stroke-width="2.2" pointer-events="none"/>`;
        if (role) h += `<text x="${mx}" y="${my+3.5}" text-anchor="middle" font-size="${fs}" fill="${col}" font-weight="900" pointer-events="none">${spelled}</text>`;
      }
    } else if (f >= startFret && f < startFret+CB_FRETS) {
      const note=noteAt(s,f);
      const { role, spelled } = cbNoteInfo(note, bctx);
      const isR=role&&role.name==='R', col=role?role.color:'#888', cx=cbFx(f);
      if (isR) {
        h += `<circle cx="${cx}" cy="${my}" r="${CB_DR*1.6}" fill="${col}22" pointer-events="none"/>`;
        h += `<circle cx="${cx}" cy="${my}" r="${CB_DR*1.3}" fill="${col}" class="cb-placed-tap" data-s="${s}" style="cursor:pointer"/>`;
        h += `<text x="${cx}" y="${my+5}" text-anchor="middle" font-size="14" fill="#fff" font-weight="900" pointer-events="none">R</text>`;
      } else {
        const fs=spelled.length>2?CB_DR*0.72:CB_DR*0.94;
        h += `<circle cx="${cx}" cy="${my}" r="${CB_DR}" fill="${col}" class="cb-placed-tap" data-s="${s}" style="cursor:pointer"/>`;
        h += `<text x="${cx}" y="${my+fs*0.38}" text-anchor="middle" font-size="${fs}" fill="#fff" font-weight="900" pointer-events="none">${spelled}</text>`;
      }
    } else if (f > 0) {
      h += `<text x="${mx}" y="${my+4}" text-anchor="middle" font-size="10" fill="var(--accent)" font-weight="800" class="cb-placed-tap" data-s="${s}" style="cursor:pointer">${f}f</text>`;
    }
  }

  svg.innerHTML = h;

  svg.querySelectorAll('.cb-ghost').forEach(el =>
    el.addEventListener('click', () => { CB.placed[+el.dataset.s]=+el.dataset.f; cbUpdate(); }));
  svg.querySelectorAll('.cb-placed-tap').forEach(el =>
    el.addEventListener('click', () => { CB.placed[+el.dataset.s]=undefined; cbUpdate(); }));
  svg.querySelectorAll('.cb-str-tap').forEach(el =>
    el.addEventListener('click', () => { CB.placed[+el.dataset.s]=null; cbUpdate(); }));
}

function cbRenderComp() {
  const { rootSpell, rootLabel, typeId, typeLabel, compIvs } = getBuilderContext();
  document.getElementById('cbComp').innerHTML =
    compIvs.map(iv => {
      const role = getRoleByIv(iv, typeId);
      const col = role ? role.color : '#888';
      const name = role ? role.name : '?';
      const isR = name === 'R';
      const noteName = spellNote(rootSpell, iv, typeId);
      return `<span class="cb-chip" style="color:${col};border-color:${col};background:${col}18;${isR?'border-width:3px;padding:5px 13px;font-size:14px;':''}">${noteName}<span style="font-size:10px;margin-left:4px;opacity:.75">${name}</span></span>`;
    }).join('');
  document.getElementById('cbChordLbl').textContent = `${rootLabel}${typeLabel}`;
}


function cbUpdateThumb() {
  const thumb = document.getElementById('cbThumb');
  if (!thumb) return;
  const pct = (CB.startFret - 1) / (CB_MAX_FRET - 1) * 100;
  thumb.style.left = `${pct}%`;
  document.getElementById('cbFretLbl').textContent = `${CB.startFret}f`;
}

function cbUpdate() {
  cbRenderFB();
  cbUpdateThumb();
  const hasSolid = CB.placed.some(f => f != null && f !== undefined);
  document.getElementById('cbSaveBtn').disabled = !hasSolid;
  document.getElementById('cbErr').textContent = '';
}

// ── Builder スライダー / スワイプ初期化 ──
// builder が DOM に存在する状態で一度だけ呼ぶ（§ 18 INIT から呼び出す）
function initBuilderSlider() {
  const getTrack  = () => document.getElementById('cbTrack');
  let dragging = false;

  function getTrackPct(clientX) {
    const r = getTrack().getBoundingClientRect();
    return Math.max(0, Math.min(1, (clientX - r.left) / r.width));
  }
  function pctToFret(p) { return Math.round(1 + p * (CB_MAX_FRET - 1)); }
  function setFret(f) {
    f = Math.max(1, Math.min(CB_MAX_FRET, f));
    if (f === CB.startFret) return;
    CB.startFret = f;
    cbUpdate();
  }

  // スライダー（マウス）
  document.addEventListener('mousedown', e => {
    const track = getTrack();
    if (!track) return;
    if (track.contains(e.target)) { dragging=true; setFret(pctToFret(getTrackPct(e.clientX))); e.preventDefault(); }
  });
  document.addEventListener('mousemove', e => { if (dragging && getTrack()) setFret(pctToFret(getTrackPct(e.clientX))); });
  document.addEventListener('mouseup',   () => { dragging = false; });

  // スライダー（タッチ）
  document.addEventListener('touchstart', e => {
    const track = getTrack();
    if (!track) return;
    if (track.contains(e.target)) { dragging=true; setFret(pctToFret(getTrackPct(e.touches[0].clientX))); }
  }, {passive:true});
  document.addEventListener('touchmove', e => {
    if (dragging && getTrack()) setFret(pctToFret(getTrackPct(e.touches[0].clientX)));
  }, {passive:true});
  document.addEventListener('touchend', () => { dragging = false; });

  // 指板スワイプ
  const getFbWrap = () => document.querySelector('.cb-fb-wrap');
  let swipeStartX = null, swipeStartFret = null;

  document.addEventListener('touchstart', e => {
    const fw = getFbWrap();
    if (fw && fw.contains(e.target) && !getTrack()?.contains(e.target)) {
      swipeStartX    = e.touches[0].clientX;
      swipeStartFret = CB.startFret;
    }
  }, {passive:true});
  document.addEventListener('touchmove', e => {
    if (swipeStartX === null) return;
    const fw = getFbWrap();
    if (!fw) return;
    const dx    = e.touches[0].clientX - swipeStartX;
    const fretW = fw.getBoundingClientRect().width / CB_FRETS;
    setFret(swipeStartFret + Math.round(-dx / fretW));
  }, {passive:true});
  document.addEventListener('touchend', () => { swipeStartX = null; });
}

/* ── builder ハンドラ ── */

/* save: バリデーション → commitBuilder */

// 名前未入力時の自動命名：最小押弦フレットから "5f form" 形式、なければ "Custom Form"
function makeDefaultCustomName(frets) {
  const pressed = frets.filter(f => typeof f === 'number' && f > 0);
  if (!pressed.length) return 'Custom Form';
  return `${Math.min(...pressed)}f form`;
}

document.getElementById('cbSaveBtn').addEventListener('click', () => {
  const { rootPc } = getBuilderContext();
  const frets  = [...CB.placed].map(f => f === undefined ? null : f);
  const errEl  = document.getElementById('cbErr');

  // 条件1: 実音が2音以上
  const realPlayed = frets.filter(f => typeof f === 'number' && f >= 0);
  if (realPlayed.length < 2) { errEl.textContent = '2音以上配置してください'; return; }

  // 条件2: root音を1つ以上含む
  const rootPcCanon = canon(rootPc);
  const hasRootNote = frets.some((f, s) => {
    if (typeof f !== 'number' || f < 0) return false;
    return canon(noteAt(s, f)) === rootPcCanon;
  });
  if (!hasRootNote) { errEl.textContent = 'ルート音を1つ以上含めてください'; return; }

  const rawName = document.getElementById('cbNameInput').value.trim();
  const customName = rawName || makeDefaultCustomName(frets);
  const ok = commitBuilder(customName);
  if (!ok) errEl.textContent = '構成音以外の音が含まれています';
});

/* clear: 配置だけリセット（mode / editingId は維持） */
document.getElementById('cbClearBtn').addEventListener('click', clearBuilderPlacement);

/* close: キャンセル遷移 */
document.getElementById('cbClose').addEventListener('click', cancelBuilder);
document.getElementById('cbOverlay').addEventListener('click', e => {
  if (e.target === document.getElementById('cbOverlay')) cancelBuilder();
});

/* ============================================================
   § 18. INIT
   ============================================================ */
let _rt;
window.addEventListener('resize', () => { clearTimeout(_rt); _rt = setTimeout(renderApp, 120); });

applyTheme(S.theme);
loadCustomDB();
refreshCurrentEntityAndSelection();
initBuilderSlider();
renderApp();
</script>
</body>
</html>
