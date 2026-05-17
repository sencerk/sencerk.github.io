<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="3 Kök Gübre">
<meta name="theme-color" content="#FAF9F5">
<title>3 Kök Ceviz — Gübreleme 2026</title>
<style>
:root {
  --bg-page: #FAF9F5;
  --bg-card: #FFFFFF;
  --bg-secondary: #F1EFE8;
  --bg-info: #E6F1FB;
  --bg-warning: #FAEEDA;
  --bg-danger: #FCEBEB;
  --bg-success: #EAF3DE;
  --text-primary: #1F1E1B;
  --text-secondary: #5F5E5A;
  --text-tertiary: #888780;
  --text-info: #0C447C;
  --text-warning: #854F0B;
  --text-danger: #791F1F;
  --text-success: #3B6D11;
  --border: rgba(0,0,0,0.10);
  --border-strong: rgba(0,0,0,0.18);
  --border-info: #B5D4F4;
  --border-warning: #FAC775;
  --border-success: #C0DD97;
}
@media (prefers-color-scheme: dark) {
  :root {
    --bg-page: #1F1E1B;
    --bg-card: #2A2926;
    --bg-secondary: #34322E;
    --bg-info: #042C53;
    --bg-warning: #412402;
    --bg-danger: #501313;
    --bg-success: #173404;
    --text-primary: #F1EFE8;
    --text-secondary: #B4B2A9;
    --text-tertiary: #888780;
    --text-info: #B5D4F4;
    --text-warning: #FAC775;
    --text-danger: #F7C1C1;
    --text-success: #C0DD97;
    --border: rgba(255,255,255,0.12);
    --border-strong: rgba(255,255,255,0.20);
  }
}
* { box-sizing: border-box; -webkit-tap-highlight-color: transparent; }
html, body {
  margin: 0; padding: 0;
  background: var(--bg-page);
  color: var(--text-primary);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", system-ui, sans-serif;
  font-size: 15px;
  line-height: 1.5;
  -webkit-font-smoothing: antialiased;
}
.app {
  max-width: 480px;
  margin: 0 auto;
  padding: env(safe-area-inset-top, 12px) 14px env(safe-area-inset-bottom, 12px);
}
.header {
  display: flex; align-items: baseline; justify-content: space-between;
  gap: 8px; padding: 12px 2px 8px;
}
.title { font-size: 17px; font-weight: 500; line-height: 1.2; }
.subtitle { font-size: 12px; color: var(--text-secondary); margin-top: 2px; }
.btn {
  font-size: 12px; padding: 6px 10px;
  background: transparent; color: var(--text-primary);
  border: 0.5px solid var(--border-strong);
  border-radius: 8px; cursor: pointer;
  font-family: inherit;
}
.btn:active { background: var(--bg-secondary); transform: scale(0.97); }
.btn-primary { background: var(--bg-info); color: var(--text-info); border-color: var(--border-info); }
.tabs {
  display: flex; gap: 3px;
  background: var(--bg-secondary);
  padding: 3px;
  border-radius: 10px;
  margin: 6px 0 12px;
}
.tab {
  flex: 1; border: none; background: transparent;
  font-size: 13px; padding: 9px 4px;
  color: var(--text-primary); font-family: inherit;
  border-radius: 7px; cursor: pointer;
}
.tab.active { background: var(--bg-card); font-weight: 500; }
.summary {
  font-size: 12px; color: var(--text-secondary);
  padding: 0 4px 12px; line-height: 1.5;
}
.summary strong { color: var(--text-primary); }
.stat-grid {
  display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 12px;
}
.stat-card {
  background: var(--bg-secondary);
  padding: 10px 12px; border-radius: 8px;
}
.stat-label { font-size: 11px; color: var(--text-secondary); }
.stat-value {
  font-size: 19px; font-weight: 500;
  font-variant-numeric: tabular-nums; margin-top: 2px;
}
.stat-unit { font-size: 12px; color: var(--text-secondary); font-weight: 400; }
.stage-list { display: flex; flex-direction: column; gap: 8px; }
.stage {
  background: var(--bg-card);
  border: 0.5px solid var(--border);
  border-radius: 12px;
  padding: 12px 14px;
}
.stage.done { background: var(--bg-secondary); }
.stage-header {
  display: flex; align-items: center; justify-content: space-between;
  gap: 8px; cursor: pointer;
}
.stage-title { font-size: 14px; font-weight: 500; line-height: 1.3; flex: 1; min-width: 0; }
.stage-meta { font-size: 11px; color: var(--text-secondary); margin-top: 3px; }
.check {
  width: 26px; height: 26px; min-width: 26px;
  border-radius: 7px;
  border: 1px solid var(--border-strong);
  background: transparent;
  display: flex; align-items: center; justify-content: center;
  padding: 0; cursor: pointer;
}
.check.on {
  background: var(--bg-success);
  border-color: var(--border-success);
  color: var(--text-success);
}
.chev {
  width: 16px; height: 16px;
  color: var(--text-tertiary);
  transition: transform 0.15s;
  flex-shrink: 0;
}
.stage.open .chev { transform: rotate(90deg); }
.stage-body { display: none; margin-top: 10px; padding-top: 10px; border-top: 0.5px solid var(--border); }
.stage.open .stage-body { display: block; }
.fert-row {
  display: flex; justify-content: space-between; align-items: baseline;
  padding: 9px 0; border-top: 0.5px solid var(--border);
  font-size: 13px; gap: 10px;
}
.fert-row:first-of-type { border-top: 0; padding-top: 10px; }
.fert-name { flex: 1; min-width: 0; }
.fert-amounts { text-align: right; font-variant-numeric: tabular-nums; min-width: 100px; }
.fert-rate { font-weight: 500; font-size: 13px; }
.fert-total { font-size: 11px; color: var(--text-secondary); margin-top: 2px; }
.nutrient { font-size: 10px; color: var(--text-tertiary); margin-top: 2px; display: block; }
.nutrient.alt { color: var(--text-warning); }
.note-box {
  font-size: 11px; padding: 8px 10px;
  border-radius: 8px; margin-top: 10px;
  line-height: 1.45;
}
.note-box svg {
  width: 13px; height: 13px;
  vertical-align: -2px;
  margin-right: 6px;
}
.note-warn { background: var(--bg-warning); color: var(--text-warning); }
.note-info { background: var(--bg-info); color: var(--text-info); }
.note-danger { background: var(--bg-danger); color: var(--text-danger); }
.note-success { background: var(--bg-success); color: var(--text-success); }
.note-box + .note-box { margin-top: 6px; }
.breakdown { margin-top: 12px; }
.breakdown summary {
  font-size: 12px; color: var(--text-info);
  cursor: pointer; padding: 6px 0;
  list-style: none;
}
.breakdown summary::-webkit-details-marker { display: none; }
.breakdown summary::before { content: "▸ "; }
.breakdown[open] summary::before { content: "▾ "; }
.breakdown-content {
  margin-top: 8px; padding: 10px;
  background: var(--bg-secondary);
  border-radius: 8px;
  font-size: 11px;
  font-variant-numeric: tabular-nums;
  overflow-x: auto;
}
.breakdown-content table { width: 100%; border-collapse: collapse; min-width: 100%; }
.breakdown-content th {
  text-align: right; padding: 3px 5px;
  color: var(--text-secondary); font-weight: 500;
  white-space: nowrap;
}
.breakdown-content th:first-child { text-align: left; }
.breakdown-content td { padding: 4px 5px; text-align: right; white-space: nowrap; }
.breakdown-content td:first-child { text-align: left; font-weight: 500; }
.copy-btn {
  margin-top: 10px; width: 100%;
  font-size: 12px; padding: 9px;
  background: var(--bg-info); color: var(--text-info);
  border: 0.5px solid var(--border-info);
  border-radius: 8px; cursor: pointer;
  font-family: inherit;
}
.copy-btn:active { transform: scale(0.98); }
.block-row {
  display: grid; grid-template-columns: 56px 1fr auto auto;
  align-items: center; gap: 10px;
  padding: 9px 0; border-top: 0.5px solid var(--border);
  font-size: 13px;
}
.block-row:first-of-type { border-top: 0; }
.block-name { font-weight: 500; }
.block-da { font-variant-numeric: tabular-nums; text-align: right; color: var(--text-secondary); }
.block-mult {
  font-size: 10px; color: var(--text-warning);
  background: var(--bg-warning); padding: 2px 6px;
  border-radius: 4px; font-weight: 500;
}
.block-eff {
  font-size: 11px; color: var(--text-tertiary);
  font-variant-numeric: tabular-nums;
  min-width: 44px; text-align: right;
}
.kural {
  padding: 10px 12px; border-radius: 8px;
  margin-bottom: 8px; font-size: 12px; line-height: 1.5;
}
.kural svg {
  width: 13px; height: 13px;
  vertical-align: -2px;
  margin-right: 8px;
}
.kural-danger { background: var(--bg-danger); color: var(--text-danger); }
.kural-warn { background: var(--bg-warning); color: var(--text-warning); }
.kural-info { background: var(--bg-info); color: var(--text-info); }
.kural-success { background: var(--bg-success); color: var(--text-success); }
.sequence {
  margin-top: 16px; padding: 12px 14px;
  background: var(--bg-card);
  border: 0.5px solid var(--border);
  border-radius: 12px;
}
.sequence-title { font-size: 13px; font-weight: 500; margin-bottom: 8px; }
.seq-step {
  display: flex; gap: 10px; padding: 7px 0;
  font-size: 13px;
  border-top: 0.5px solid var(--border);
}
.seq-step:first-child { border-top: 0; }
.seq-num {
  color: var(--text-tertiary);
  font-variant-numeric: tabular-nums;
  min-width: 16px;
}
.toast {
  position: fixed; bottom: 24px; left: 50%;
  transform: translateX(-50%);
  background: var(--text-primary); color: var(--bg-page);
  padding: 10px 16px; border-radius: 8px;
  font-size: 13px; font-weight: 500;
  opacity: 0; transition: opacity 0.2s;
  pointer-events: none; z-index: 100;
}
.toast.show { opacity: 1; }
.sr-only {
  position: absolute; width: 1px; height: 1px;
  padding: 0; margin: -1px; overflow: hidden;
  clip: rect(0,0,0,0); white-space: nowrap; border: 0;
}
</style>
</head>
<body>
<div class="app">

  <div class="header">
    <div>
      <div class="title">3 Kök Ceviz — Gübreleme 2026</div>
      <div class="subtitle">Chandler + Tulare</div>
    </div>
    <button class="btn" id="reset-all" aria-label="Takibi sıfırla">sıfırla</button>
  </div>

  <div class="tabs">
    <button class="tab active" data-tab="program">Program</button>
    <button class="tab" data-tab="blocks">Bloklar</button>
    <button class="tab" data-tab="rules">Kurallar</button>
  </div>

  <div class="summary" id="block-summary"></div>

  <div id="tab-program"></div>
  <div id="tab-blocks" style="display: none;"></div>
  <div id="tab-rules" style="display: none;"></div>

</div>

<div class="toast" id="toast">Kopyalandı</div>

<script>
(function() {
  const STORAGE_KEY = '3kok-fertigation-2026';

  // SVG icon helpers (inline so no CDN dep)
  const ICONS = {
    check: '<svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"/></svg>',
    chev: '<svg class="chev" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="9 18 15 12 9 6"/></svg>',
    warn: '<svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M10.29 3.86 1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"/><line x1="12" y1="9" x2="12" y2="13"/><line x1="12" y1="17" x2="12.01" y2="17"/></svg>',
    info: '<svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="16" x2="12" y2="12"/><line x1="12" y1="8" x2="12.01" y2="8"/></svg>',
    danger: '<svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><line x1="15" y1="9" x2="9" y2="15"/><line x1="9" y1="9" x2="15" y2="15"/></svg>',
    flask: '<svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 2v6l-5 9a2 2 0 0 0 2 3h12a2 2 0 0 0 2-3l-5-9V2"/><line x1="9" y1="2" x2="15" y2="2"/></svg>'
  };

  // Block configuration — baked in, total 218 da effective
  const BLOCKS = [
    { id: 'KG1', da: 29, mult: 1.0 },
    { id: 'KG2', da: 16, mult: 1.0 },
    { id: 'KG3', da: 26, mult: 1.0 },
    { id: 'CG1', da: 17, mult: 1.0 },
    { id: 'CG2', da: 22, mult: 1.0 },
    { id: 'CG3', da: 22, mult: 1.0 },
    { id: 'CG4', da: 22, mult: 1.0 },
    { id: 'CG5', da: 16, mult: 1.0 },
    { id: 'CG6', da: 20, mult: 1.0 },
    { id: 'CG7', da: 20, mult: 0.7 },
    { id: 'CG8', da: 20, mult: 0.7 }
  ];

  const TOTAL_DA = BLOCKS.reduce((s, b) => s + b.da, 0);
  const EFFECTIVE_DA = BLOCKS.reduce((s, b) => s + b.da * b.mult, 0);

  const stages = [
    {
      id: 'bbch07',
      title: 'BBCH 07–09 · Fe uygulaması',
      date: 'Nis 24–26',
      ferts: [
        { name: 'Fe-EDDHA %6', rate: 0.4, nutrients: 'Fe: 0.9 g/ağaç' }
      ],
      notes: [
        { type: 'info', text: 'Tek başına uygulanır. Diğer gübrelerle karıştırma.' }
      ]
    },
    {
      id: 'bbch15',
      title: 'BBCH 15 · Sürgün',
      date: 'Nis 25–30',
      ferts: [
        { name: 'AS %21', rate: 4.5, nutrients: 'N: 35.0 · S: 40.0', alt: 'Geç kalındıysa: AN %33 @ 3.2 kg/da (N: 39.2)' },
        { name: 'KNO₃ (13-0-46)', rate: 0.9, nutrients: 'K₂O: 15.3 · N: 4.3' },
        { name: 'SOP (0-0-50)', rate: 0.7, nutrients: 'K₂O: 13.0' },
        { name: 'UP (12-61-0)', rate: 1.0, nutrients: 'P₂O₅: 22.6 · N: 4.4' },
        { name: 'Mg-nitrat (11+16MgO)', rate: 1.6, nutrients: 'MgO: 9.5 · N: 6.5' }
      ],
      notes: [
        { type: 'success', text: 'AN kullanılıyorsa AN + KNO₃ + Mg-nitrat aynı tankta karıştırılabilinir.' },
        { type: 'info', text: 'Uygulama sırası: 1. AN + KNO₃ + Mg-nitrat, 2. SOP, 3. UP'},
        { type: 'danger', text: 'AS kullanılıyorsa AS ve Mg-nitrat aynı tankta KARIŞTIRMA!' },
        { type: 'info', text: 'KNO₃ kullanma sebebi: sezon başı <15°C suda SOP çözünmüyor. Mg-nitrat\'ı AS ile karıştırma.' }
      ],
      target: 'N: 50 · P₂O₅: 23 · K₂O: 28'
    },
    {
      id: 'bbch15-zn1',
      title: 'BBCH 15–19 · Zn yaprak 1',
      date: 'Nis 28–May 5',
      ferts: [
        { name: 'ZnSO₄ yaprak', rate: 1.0, nutrients: 'Zn 1. uyg.' }
      ],
      notes: [
        { type: 'info', text: 'Yaprak uygulaması — fertigasyondan ayrı.' }
      ]
    },
    {
      id: 'bbch65',
      title: 'BBCH 65 · Tozlaşma',
      date: 'May 10–20',
      ferts: [
        { name: 'AS %21', rate: 5.0, nutrients: 'N: 38.9 · S: 44.4' },
        { name: 'SOP (0-0-50)', rate: 1.6, nutrients: 'K₂O: 29.6' },
        { name: 'UP (12-61-0)', rate: 1.0, nutrients: 'P₂O₅: 22.6 · N: 4.4' },
        { name: 'Mg-nitrat (11+16MgO)', rate: 1.6, nutrients: 'MgO: 9.5 · N: 6.5' },
        { name: 'Solubor (%20.5 B)', rate: 0.066, nutrients: 'B: 0.5 · 1. uyg.' }
      ],
      notes: [
        { type: 'warn', text: 'SOP + UP ayrı uygula. Mg-nitrat\'ı AS ile karıştırma.' }
      ],
      target: 'N: 50 · P₂O₅: 23 · K₂O: 30'
    },
    {
      id: 'leaf1',
      title: 'YAPRAK ANALİZİ',
      date: 'May 25–31',
      ferts: [],
      notes: [
        { type: 'info', text: 'Erken sezon: N/Zn/B durumu. B <20 ppm → Haziran B artır. B >100 → Haziran B atla. CG3/CG4 ayrı: Fe klorozu + B.' }
      ],
      isAnalysis: true
    },
    {
      id: 'bbch71',
      title: 'BBCH 71 · Kabuk sertleşme',
      date: 'Haz 10–20',
      ferts: [
        { name: 'AS %21', rate: 5.0, nutrients: 'N: 38.9 · S: 44.4' },
        { name: 'SOP (0-0-50)', rate: 1.6, nutrients: 'K₂O: 29.6' },
        { name: 'UP (12-61-0)', rate: 1.0, nutrients: 'P₂O₅: 22.6 · N: 4.4' },
        { name: 'Mg-nitrat (11+16MgO)', rate: 1.6, nutrients: 'MgO: 9.5 · N: 6.5' },
        { name: 'Solubor (%20.5 B)', rate: 0.066, nutrients: 'B: 0.5 · 2. uyg.' }
      ],
      notes: [
        { type: 'warn', text: 'SOP + UP ayrı uygula. Mg-nitrat\'ı AS ile karıştırma.' }
      ],
      target: 'N: 50 · P₂O₅: 23 · K₂O: 30'
    },
    {
      id: 'bbch71-zn2',
      title: 'BBCH 71–73 · Zn yaprak 2',
      date: 'Haz 15–25',
      ferts: [
        { name: 'ZnSO₄ yaprak', rate: 1.0, nutrients: 'Zn 2. uyg.' }
      ],
      notes: [
        { type: 'info', text: 'Yaprak uygulaması — fertigasyondan ayrı.' }
      ]
    },
    {
      id: 'bbch75',
      title: 'BBCH 75–77 · İç dolumu',
      date: 'Tem 10–20',
      ferts: [
        { name: 'AS %21', rate: 5.0, nutrients: 'N: 38.9 · S: 44.4' },
        { name: 'SOP (0-0-50)', rate: 1.6, nutrients: 'K₂O: 29.6' },
        { name: 'UP (12-61-0)', rate: 1.0, nutrients: 'P₂O₅: 22.6 · N: 4.4' },
        { name: 'Mg-nitrat (11+16MgO)', rate: 1.6, nutrients: 'MgO: 9.5 · N: 6.5' }
      ],
      notes: [
        { type: 'warn', text: 'SOP + UP ayrı uygula. Mg-nitrat\'ı AS ile karıştırma.' }
      ],
      target: 'N: 50 · P₂O₅: 23 · K₂O: 30'
    },
    {
      id: 'leaf2',
      title: 'YAPRAK ANALİZİ',
      date: 'Tem 15–20',
      ferts: [],
      notes: [
        { type: 'info', text: 'Kanonik: N, P, K, Zn, Fe, B. Ağustos/Eylül dozları + Eylül B kararı.' }
      ],
      isAnalysis: true
    },
    {
      id: 'bbch77-zn3',
      title: 'BBCH 77–79 · Zn yaprak 3',
      date: 'Tem 20–30',
      ferts: [
        { name: 'ZnSO₄ yaprak', rate: 1.0, nutrients: 'Zn 3. uyg.' }
      ],
      notes: [
        { type: 'info', text: 'Yaprak uygulaması — fertigasyondan ayrı.' }
      ]
    },
    {
      id: 'bbch79',
      title: 'BBCH 79–81 · Son N+P',
      date: 'Ağu 10–20',
      ferts: [
        { name: 'AS %21', rate: 5.9, nutrients: 'N: 45.9 · S: 52.4', alt: 'Yaprak N >%2.8 → %50 azalt (rate: 3.0 kg/da)' },
        { name: 'SOP (0-0-50)', rate: 1.6, nutrients: 'K₂O: 29.6' },
        { name: 'UP (12-61-0)', rate: 1.0, nutrients: 'P₂O₅: 22.6 · N: 4.4' }
      ],
      notes: [
        { type: 'warn', text: 'Son N+P uygulaması. Mg-nitrat bu aşamadan sonra YOK.' }
      ],
      target: 'N: 50 · P₂O₅: 23 · K₂O: 30'
    },
    {
      id: 'bbch85',
      title: 'BBCH 85–87 · Sadece K (+B?)',
      date: 'Eyl 5–15',
      ferts: [
        { name: 'SOP (0-0-50)', rate: 1.6, nutrients: 'K₂O: 29.6' },
        { name: 'Solubor (%20.5 B)', rate: 0.066, nutrients: 'B: 0.5 · KOŞULLU: B<36 ppm' }
      ],
      notes: [
        { type: 'warn', text: 'Solubor yalnızca Temmuz yaprak analizinde B<36 ppm ise. Aksi halde sadece SOP.' }
      ],
      target: 'K₂O: 30'
    }
  ];

  const mixingRules = [
    { type: 'danger', text: 'Mg-nitrat + AS — KARIŞTIRMA. Operasyonu bozuyorsa Mg-nitrat\'ı sezona düşür (Şubat\'ta toprağa veya yaprak).' },
    { type: 'danger', text: 'SOP + UP — Ayrı uygula.' },
    { type: 'warn', text: 'AN + KNO₃ + Mg-nitrat — Karıştırılabilir (BBCH 15).' },
    { type: 'warn', text: 'AS + UP — Karıştırılabilir, asidik pH faydalı.' },
    { type: 'warn', text: 'CG7 + CG8 — Genç ağaçlar, %70 doz uygulanır. Tüm kg değerleri otomatik düzeltilmiştir.' },
    { type: 'info', text: 'Uygulama sırası: 15 dk temiz sulama → asitleme (pH 6.5) → gübre → durdur → 30 dk temiz su.' },
    { type: 'info', text: 'BBCH 15 KNO₃ sebebi: sezon başı <15°C suda SOP çözünmüyor. Daha sonra SOP\'a geç.' },
    { type: 'success', text: 'AS, AN\'a kıyasla daha ucuz (per N) + S sağlıyor + yüksek pH topraklarda asidik etki.' }
  ];

  function loadState() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (raw) return JSON.parse(raw);
    } catch (e) {}
    return { tracking: {}, openStages: {} };
  }
  function saveState(s) {
    try { localStorage.setItem(STORAGE_KEY, JSON.stringify(s)); } catch (e) {}
  }

  let state = loadState();
  if (!state.tracking) state.tracking = {};
  if (!state.openStages) state.openStages = {};

  function fmt(n, dp) {
    if (!isFinite(n)) return '0';
    if (Math.abs(n) < 0.005) return '0';
    const d = dp != null ? dp : (Math.abs(n) < 10 ? 2 : Math.abs(n) < 100 ? 1 : 0);
    return n.toFixed(d).replace(/\.?0+$/, '');
  }

  function showToast(msg) {
    const t = document.getElementById('toast');
    t.textContent = msg;
    t.classList.add('show');
    setTimeout(() => t.classList.remove('show'), 1800);
  }

  function copyText(text) {
    if (navigator.clipboard && navigator.clipboard.writeText) {
      navigator.clipboard.writeText(text).then(
        () => showToast('Kopyalandı'),
        () => fallbackCopy(text)
      );
    } else {
      fallbackCopy(text);
    }
  }
  function fallbackCopy(text) {
    const ta = document.createElement('textarea');
    ta.value = text;
    ta.style.position = 'fixed';
    ta.style.left = '-9999px';
    document.body.appendChild(ta);
    ta.select();
    try { document.execCommand('copy'); showToast('Kopyalandı'); }
    catch (e) { showToast('Kopyalanamadı'); }
    document.body.removeChild(ta);
  }

  function buildCopyText(stage) {
    let lines = [`${stage.title} — ${stage.date}`];
    BLOCKS.forEach(b => {
      const parts = stage.ferts.map(f => {
        const kg = b.da * b.mult * f.rate;
        return `${f.name.split(' ')[0]}: ${fmt(kg)} kg`;
      });
      const tag = b.mult < 1 ? ` (×${b.mult})` : '';
      lines.push(`${b.id} (${b.da} da${tag}): ${parts.join(' · ')}`);
    });
    lines.push('');
    lines.push('TOPLAM:');
    stage.ferts.forEach(f => {
      lines.push(`${f.name}: ${fmt(EFFECTIVE_DA * f.rate)} kg (${fmt(f.rate)} kg/da)`);
    });
    return lines.join('\n');
  }

  function renderSummary() {
    document.getElementById('block-summary').innerHTML =
      `<strong>${TOTAL_DA} da</strong> · 11 blok · etkin alan <strong>${fmt(EFFECTIVE_DA, 1)} da</strong> (CG7+CG8 @ 0.7×)`;
  }

  function renderProgram() {
    const root = document.getElementById('tab-program');
    const totalStages = stages.filter(s => !s.isAnalysis).length;
    const doneStages = stages.filter(s => !s.isAnalysis && state.tracking[s.id]?.done).length;

    let html = `<div class="stat-grid">
      <div class="stat-card">
        <div class="stat-label">Etkin alan</div>
        <div class="stat-value">${fmt(EFFECTIVE_DA, 1)} <span class="stat-unit">da</span></div>
      </div>
      <div class="stat-card">
        <div class="stat-label">Tamamlanan</div>
        <div class="stat-value">${doneStages}<span class="stat-unit">/${totalStages}</span></div>
      </div>
    </div>`;

    html += '<div class="stage-list">';

    stages.forEach(stage => {
      const tr = state.tracking[stage.id] || {};
      const isOpen = state.openStages[stage.id];
      const isDone = tr.done;
      const isAnalysis = stage.isAnalysis;

      html += `<div class="stage ${isOpen ? 'open' : ''} ${isDone ? 'done' : ''}">`;
      html += `<div class="stage-header" data-toggle="${stage.id}">`;
      html += `<div style="flex:1;min-width:0;">`;
      html += `<div class="stage-title">${stage.title}</div>`;
      html += `<div class="stage-meta">${stage.date}${stage.target ? ' · hedef ' + stage.target : ''}${isDone && tr.date ? ' · ✓ ' + tr.date : ''}</div>`;
      html += `</div>`;
      if (!isAnalysis) {
        html += `<button class="check ${isDone ? 'on' : ''}" data-check="${stage.id}" aria-label="Uygulandı olarak işaretle">${isDone ? ICONS.check : ''}</button>`;
      } else {
        html += `<span style="color:var(--text-info);display:flex;align-items:center;">${ICONS.flask}</span>`;
      }
      html += ICONS.chev;
      html += `</div>`;

      html += `<div class="stage-body">`;

      if (stage.ferts.length > 0) {
        stage.ferts.forEach(f => {
          const totalKg = EFFECTIVE_DA * f.rate;
          html += `<div class="fert-row">`;
          html += `<div class="fert-name">`;
          html += `<div>${f.name}</div>`;
          html += `<span class="nutrient">${f.nutrients}</span>`;
          if (f.alt) html += `<span class="nutrient alt">↪ ${f.alt}</span>`;
          html += `</div>`;
          html += `<div class="fert-amounts">`;
          html += `<div class="fert-rate">${fmt(f.rate)} kg/da</div>`;
          html += `<div class="fert-total">= ${fmt(totalKg)} kg</div>`;
          html += `</div>`;
          html += `</div>`;
        });

        html += `<details class="breakdown"><summary>Blok bazlı dağılım</summary>`;
        html += `<div class="breakdown-content"><table><thead><tr><th>Blok</th>`;
        stage.ferts.forEach(f => {
          html += `<th>${f.name.split(' ')[0]}</th>`;
        });
        html += `</tr></thead><tbody>`;
        BLOCKS.forEach(b => {
          const tag = b.mult < 1 ? ` <span class="block-mult" style="font-size:9px;">×${b.mult}</span>` : '';
          html += `<tr><td>${b.id} <span style="color:var(--text-tertiary);font-weight:400;">(${b.da})${tag}</span></td>`;
          stage.ferts.forEach(f => {
            html += `<td>${fmt(b.da * b.mult * f.rate)}</td>`;
          });
          html += `</tr>`;
        });
        html += `</tbody></table>`;
        html += `<div style="font-size:10px;color:var(--text-tertiary);margin-top:6px;">tüm değerler kg · CG7+CG8 düzeltildi</div>`;
        html += `</div>`;
        html += `<button class="copy-btn" data-copy="${stage.id}">📋 WhatsApp için kopyala</button>`;
        html += `</details>`;
      }

      if (stage.notes && stage.notes.length) {
        stage.notes.forEach(n => {
          const icon = n.type === 'danger' ? ICONS.danger
                     : n.type === 'warn' ? ICONS.warn
                     : n.type === 'success' ? ICONS.check
                     : ICONS.info;
          html += `<div class="note-box note-${n.type}">${icon}<span>${n.text}</span></div>`;
        });
      }

      html += `</div></div>`;
    });

    html += '</div>';
    root.innerHTML = html;

    root.querySelectorAll('[data-toggle]').forEach(el => {
      el.addEventListener('click', () => {
        const id = el.getAttribute('data-toggle');
        state.openStages[id] = !state.openStages[id];
        saveState(state);
        renderProgram();
      });
    });
    root.querySelectorAll('[data-check]').forEach(el => {
      el.addEventListener('click', (e) => {
        e.stopPropagation();
        const id = el.getAttribute('data-check');
        if (!state.tracking[id]) state.tracking[id] = {};
        state.tracking[id].done = !state.tracking[id].done;
        if (state.tracking[id].done) {
          state.tracking[id].date = new Date().toISOString().slice(0, 10);
        } else {
          delete state.tracking[id].date;
        }
        saveState(state);
        renderProgram();
      });
    });
    root.querySelectorAll('[data-copy]').forEach(el => {
      el.addEventListener('click', (e) => {
        e.stopPropagation();
        e.preventDefault();
        const id = el.getAttribute('data-copy');
        const stage = stages.find(s => s.id === id);
        if (stage) copyText(buildCopyText(stage));
      });
    });
  }

  function renderBlocks() {
    const root = document.getElementById('tab-blocks');
    let html = '<div class="summary">Blok boyutları sabit. CG7+CG8 için 0.7× çarpan (genç ağaçlar).</div>';
    html += '<div style="background:var(--bg-card);border:0.5px solid var(--border);border-radius:12px;padding:8px 14px;">';
    BLOCKS.forEach(b => {
      html += `<div class="block-row">`;
      html += `<div class="block-name">${b.id}</div>`;
      html += `<div class="block-da">${b.da} <span style="font-size:11px;">da</span></div>`;
      if (b.mult < 1) {
        html += `<div class="block-mult">×${b.mult}</div>`;
      } else {
        html += `<div></div>`;
      }
      html += `<div class="block-eff">${fmt(b.da * b.mult, 1)} etk</div>`;
      html += `</div>`;
    });
    html += '</div>';
    html += `<div class="stat-grid" style="margin-top:12px;">
      <div class="stat-card"><div class="stat-label">Fiziksel da</div><div class="stat-value">${TOTAL_DA}</div></div>
      <div class="stat-card"><div class="stat-label">Etkin da</div><div class="stat-value">${fmt(EFFECTIVE_DA, 1)}</div></div>
    </div>`;
    root.innerHTML = html;
  }

  function renderRules() {
    const root = document.getElementById('tab-rules');
    let html = '<div class="summary">Karıştırma ve uygulama kuralları. Dökmeden önce kontrol et.</div>';
    mixingRules.forEach(r => {
      const icon = r.type === 'danger' ? ICONS.danger
                 : r.type === 'warn' ? ICONS.warn
                 : r.type === 'success' ? ICONS.check
                 : ICONS.info;
      html += `<div class="kural kural-${r.type}">${icon}<span>${r.text}</span></div>`;
    });

    html += `<div class="sequence">`;
    html += `<div class="sequence-title">Uygulama sırası</div>`;
    const steps = [
      '15 dk temiz sulama',
      'Asitleme başla — pH 6.5',
      'Gübreleme',
      'Gübre durdur',
      '30 dk temiz su — boruları temizle'
    ];
    steps.forEach((s, i) => {
      html += `<div class="seq-step"><span class="seq-num">${i + 1}</span><span>${s}</span></div>`;
    });
    html += `</div>`;

    root.innerHTML = html;
  }

  function switchTab(name) {
    document.querySelectorAll('.tab').forEach(b => {
      b.classList.toggle('active', b.getAttribute('data-tab') === name);
    });
    ['program', 'blocks', 'rules'].forEach(t => {
      document.getElementById('tab-' + t).style.display = t === name ? 'block' : 'none';
    });
    if (name === 'program') renderProgram();
    else if (name === 'blocks') renderBlocks();
    else renderRules();
  }

  document.querySelectorAll('.tab').forEach(b => {
    b.addEventListener('click', () => switchTab(b.getAttribute('data-tab')));
  });

  document.getElementById('reset-all').addEventListener('click', () => {
    if (confirm('Takip sıfırlansın mı? Tüm uygulama işaretleri silinir. Blok boyutları sabit kalır.')) {
      state = { tracking: {}, openStages: {} };
      saveState(state);
      renderProgram();
    }
  });

  renderSummary();
  renderProgram();
})();
</script>

</body>
</html>
