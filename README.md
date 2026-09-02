<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1, viewport-fit=cover">
  <meta name="theme-color" content="#241209">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="mobile-web-app-capable" content="yes">
  <link rel="icon" type="image/svg+xml" href="https://cdn.jsdelivr.net/gh/microsoft/fluentui-emoji@main/assets/Violin/Flat/violin_flat.svg">
  <link rel="apple-touch-icon" href="https://cdn.jsdelivr.net/gh/microsoft/fluentui-emoji@main/assets/Violin/Flat/violin_flat.svg">
  <title>Docinho de Amendoim 🐈🎻</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;0,700;1,600&family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
/* =========================================================
   Docinho de Amendoim — estilos
   Tema: madeira de violino
   ========================================================= */

:root {
  --wood-deepest: #201007;
  --wood-dark: #3A1F10;
  --wood-mid: #542D16;
  --wood-mid-2: #6b3a1b;
  --varnish-amber: #C97D3A;
  --varnish-light: #E3A458;
  --string-gold: #D9B463;
  --parchment: #F3E6C8;
  --parchment-dim: #D8C6A0;
  --ink: #2A1608;
  --danger: #A63D2F;
  --danger-light: #C1543F;
  --shadow: rgba(10, 4, 0, 0.55);
  --radius-lg: 22px;
  --radius-md: 14px;
  --radius-sm: 9px;
  --font-display: "Cormorant Garamond", serif;
  --font-body: "Quicksand", sans-serif;
}

* {
  box-sizing: border-box;
  -webkit-tap-highlight-color: transparent;
}

html,
body {
  margin: 0;
  padding: 0;
  min-height: 100%;
}

body {
  font-family: var(--font-body);
  color: var(--parchment);
  min-height: 100vh;
  background-color: var(--wood-deepest);
  background-image:
    repeating-linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.1) 0px,
      rgba(0, 0, 0, 0.1) 1px,
      transparent 1px,
      transparent 7px
    ),
    repeating-linear-gradient(
      93deg,
      rgba(255, 180, 100, 0.035) 0px,
      transparent 2px,
      transparent 46px,
      rgba(255, 180, 100, 0.035) 48px
    ),
    radial-gradient(ellipse at 25% 10%, rgba(140, 80, 35, 0.3), transparent 55%),
    radial-gradient(ellipse at 80% 90%, rgba(90, 45, 15, 0.35), transparent 55%),
    linear-gradient(165deg, var(--wood-dark), var(--wood-deepest) 65%);
  background-attachment: fixed;
  -webkit-font-smoothing: antialiased;
  padding-bottom: 40px;
}

button,
input,
select,
textarea {
  font-family: inherit;
}

::selection {
  background: var(--varnish-amber);
  color: var(--wood-deepest);
}

:focus-visible {
  outline: 2px solid var(--string-gold);
  outline-offset: 2px;
}

.hidden {
  display: none !important;
}

/* ---------- Layout ---------- */
#app {
  max-width: 960px;
  margin: 0 auto;
  padding: 16px 14px 24px;
}

header.top {
  text-align: center;
  padding: 12px 8px 4px;
}

.logo-wrap {
  width: 72px;
  height: 80px;
  margin: 0 auto 4px;
  filter: drop-shadow(0 6px 10px rgba(0, 0, 0, 0.5));
}

.logo-wrap svg {
  width: 100%;
  height: 100%;
  display: block;
}

@media (prefers-reduced-motion: no-preference) {
  .logo-wrap {
    animation: sway 6s ease-in-out infinite;
    transform-origin: 50% 90%;
  }
  @keyframes sway {
    0%,
    100% {
      transform: rotate(-2deg);
    }
    50% {
      transform: rotate(2deg);
    }
  }
}

h1.brand {
  font-family: var(--font-display);
  font-weight: 700;
  font-style: italic;
  font-size: clamp(26px, 6.5vw, 38px);
  margin: 2px 0;
  color: var(--parchment);
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
}

p.tagline {
  margin: 0 0 6px;
  color: var(--parchment-dim);
  font-size: 13px;
  letter-spacing: 0.4px;
}

.fhole-divider {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  margin: 8px auto 14px;
  opacity: 0.85;
}

.fhole-divider .line {
  height: 1px;
  width: 56px;
  background: linear-gradient(90deg, transparent, var(--string-gold), transparent);
}

.fhole-divider .fhole-icon svg {
  width: 20px;
  height: 32px;
  display: block;
}

/* ---------- Tabs ---------- */
.tabs {
  display: flex;
  gap: 6px;
  margin-bottom: 16px;
  flex-wrap: wrap;
}

.tab {
  flex: 1;
  min-width: 100px;
  padding: 11px 12px;
  border-radius: var(--radius-md);
  border: 1px solid rgba(217, 180, 99, 0.28);
  background: rgba(0, 0, 0, 0.22);
  color: var(--parchment);
  font-weight: 600;
  font-size: 13px;
  cursor: pointer;
  transition: background 0.15s, border-color 0.15s;
}

.tab:hover {
  background: rgba(217, 180, 99, 0.12);
  border-color: var(--string-gold);
}

.tab.active {
  background: linear-gradient(160deg, var(--varnish-light), var(--varnish-amber));
  color: var(--ink);
  border-color: var(--varnish-amber);
}

.panel {
  display: none;
}

.panel.active {
  display: block;
}

/* ---------- Violino ---------- */
.violin-stage {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
  align-items: flex-start;
  justify-content: center;
}

.violin-body-wrap {
  position: relative;
  width: min(100%, 340px);
  margin: 0 auto;
}

.violin-svg {
  width: 100%;
  height: auto;
  display: block;
  filter: drop-shadow(0 12px 28px rgba(0, 0, 0, 0.45));
}

/* Grade de notas sobre o fingerboard */
.note-grid {
  position: absolute;
  /* Ajustado ao viewBox do fingerboard (x 138–182, y 118–398) */
  left: 42.5%;
  top: 16.4%;
  width: 14.2%;
  height: 38.8%;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(12, 1fr);
  gap: 1px;
  pointer-events: auto;
  z-index: 5;
}

.note-cell {
  border-radius: 3px;
  cursor: pointer;
  background: transparent;
  border: none;
  padding: 0;
  transition: background 0.1s;
  position: relative;
}

.note-cell:hover,
.note-cell:focus-visible {
  background: rgba(217, 180, 99, 0.35);
}

.note-cell.playing {
  background: rgba(227, 164, 88, 0.65);
  box-shadow: 0 0 10px rgba(227, 164, 88, 0.6);
}

.note-cell .tip {
  display: none;
  position: absolute;
  bottom: 100%;
  left: 50%;
  transform: translateX(-50%);
  background: var(--ink);
  color: var(--parchment);
  font-size: 10px;
  font-weight: 700;
  padding: 2px 6px;
  border-radius: 6px;
  white-space: nowrap;
  pointer-events: none;
  z-index: 10;
  border: 1px solid rgba(217, 180, 99, 0.4);
}

.note-cell:hover .tip {
  display: block;
}

.play-info {
  flex: 1;
  min-width: 180px;
  max-width: 260px;
  background: rgba(0, 0, 0, 0.22);
  border: 1px solid rgba(217, 180, 99, 0.22);
  border-radius: var(--radius-lg);
  padding: 16px;
}

.now-playing .label {
  display: block;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.4px;
  color: var(--string-gold);
  font-weight: 700;
  margin-bottom: 4px;
}

.now-playing .note-name {
  font-family: var(--font-display);
  font-size: 36px;
  font-weight: 700;
  font-style: italic;
  color: var(--parchment);
  line-height: 1.1;
}

.now-playing .note-detail {
  display: block;
  font-size: 13px;
  color: var(--parchment-dim);
  margin-top: 4px;
}

.string-legend {
  margin-top: 18px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.leg-item {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
  color: var(--parchment-dim);
}

.leg-item .dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}

.leg-item .dot.g {
  background: #c8b89a;
}
.leg-item .dot.d {
  background: #d4c4a8;
}
.leg-item .dot.a {
  background: #e0d0b4;
}
.leg-item .dot.e {
  background: #ecdcbc;
}

/* Duração */
.duration-bar {
  margin-top: 18px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 10px;
  background: rgba(0, 0, 0, 0.2);
  border: 1px solid rgba(217, 180, 99, 0.2);
  border-radius: var(--radius-md);
  padding: 12px 14px;
}

.bar-label {
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 0.35px;
  color: var(--string-gold);
  font-weight: 700;
}

.duration-btns {
  display: flex;
  gap: 4px;
  flex-wrap: wrap;
}

.duration-btns button {
  min-width: 42px;
  padding: 8px 10px;
  border-radius: 8px;
  border: 1px solid rgba(217, 180, 99, 0.3);
  background: rgba(0, 0, 0, 0.25);
  color: var(--parchment);
  font-weight: 700;
  font-size: 13px;
  cursor: pointer;
}

.duration-btns button.active {
  background: var(--varnish-amber);
  color: var(--ink);
  border-color: var(--varnish-amber);
}

.btn-record,
.btn-stop {
  margin-left: auto;
  padding: 9px 14px;
  border-radius: 20px;
  border: none;
  font-weight: 700;
  font-size: 13px;
  cursor: pointer;
}

.btn-record {
  background: var(--danger-light);
  color: #fff;
}

.btn-record.recording {
  animation: pulse 1s ease-in-out infinite;
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.65;
  }
}

.btn-stop {
  background: rgba(0, 0, 0, 0.35);
  color: var(--parchment);
  border: 1px solid rgba(217, 180, 99, 0.35);
}

.record-hint {
  margin-top: 8px;
  font-size: 12px;
  color: var(--parchment-dim);
  text-align: center;
  min-height: 18px;
}

/* ---------- Partitura ---------- */
.score-header {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-bottom: 12px;
}

.field {
  margin-bottom: 12px;
}

.field.inline {
  flex: 1;
  min-width: 140px;
  margin-bottom: 0;
}

.field label {
  display: block;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.3px;
  color: var(--string-gold);
  margin-bottom: 4px;
  text-transform: uppercase;
}

.field input,
.field select {
  width: 100%;
  padding: 10px 12px;
  border-radius: var(--radius-sm);
  border: 1px solid rgba(217, 180, 99, 0.3);
  background: rgba(0, 0, 0, 0.28);
  color: var(--parchment);
  font-size: 15px;
}

.score-canvas-wrap {
  background: #faf6eb;
  border-radius: var(--radius-md);
  overflow-x: auto;
  padding: 10px 8px;
  min-height: 150px;
  border: 1px solid rgba(217, 180, 99, 0.3);
  margin-bottom: 12px;
}

#scoreCanvas {
  min-width: 100%;
}

.score-toolbar {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 12px;
}

.score-toolbar .group {
  display: flex;
  flex-wrap: wrap;
  gap: 4px;
  align-items: center;
  background: rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  padding: 5px;
}

.score-toolbar .label {
  font-size: 10px;
  color: var(--string-gold);
  font-weight: 700;
  text-transform: uppercase;
  padding: 0 4px;
}

.score-toolbar button {
  background: rgba(0, 0, 0, 0.25);
  border: 1px solid rgba(217, 180, 99, 0.3);
  color: var(--parchment);
  border-radius: 8px;
  padding: 7px 10px;
  font-size: 12px;
  font-weight: 600;
  cursor: pointer;
}

.score-toolbar button.active {
  background: var(--varnish-amber);
  color: var(--ink);
  border-color: var(--varnish-amber);
}

.score-play-bar {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 12px;
}

.btn-primary {
  background: linear-gradient(160deg, var(--varnish-light), var(--varnish-amber));
  color: var(--ink);
  border: none;
  padding: 11px 18px;
  border-radius: 24px;
  font-weight: 700;
  font-size: 14px;
  cursor: pointer;
  box-shadow: 0 6px 14px rgba(201, 125, 58, 0.35);
}

.btn-primary:hover {
  transform: translateY(-1px);
}

.btn-secondary {
  background: rgba(0, 0, 0, 0.25);
  color: var(--parchment);
  border: 1px solid rgba(217, 180, 99, 0.3);
  padding: 11px 16px;
  border-radius: 24px;
  font-weight: 600;
  font-size: 14px;
  cursor: pointer;
}

.note-list {
  max-height: 110px;
  overflow-y: auto;
  background: rgba(0, 0, 0, 0.18);
  border-radius: var(--radius-sm);
  padding: 8px;
  font-size: 12px;
  color: var(--parchment-dim);
}

.note-list .chip {
  display: inline-flex;
  align-items: center;
  gap: 4px;
  background: rgba(217, 180, 99, 0.15);
  border-radius: 6px;
  padding: 3px 8px;
  margin: 2px;
  color: var(--parchment);
}

.note-list .chip button {
  background: none;
  border: none;
  color: var(--danger-light);
  cursor: pointer;
  font-size: 12px;
  padding: 0 2px;
}

/* ---------- Biblioteca ---------- */
.library-toolbar {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 14px;
}

.library-toolbar input[type="search"] {
  flex: 1;
  min-width: 160px;
  padding: 10px 12px;
  border-radius: var(--radius-md);
  border: 1px solid rgba(217, 180, 99, 0.25);
  background: rgba(0, 0, 0, 0.25);
  color: var(--parchment);
  font-size: 14px;
}

.icon-btn {
  padding: 10px 14px;
  border-radius: var(--radius-md);
  border: 1px solid rgba(217, 180, 99, 0.3);
  background: rgba(0, 0, 0, 0.22);
  color: var(--parchment);
  font-weight: 600;
  font-size: 13px;
  cursor: pointer;
}

.empty-lib {
  text-align: center;
  padding: 40px 16px;
  color: var(--parchment-dim);
}

.empty-lib .hint {
  font-size: 13px;
  margin-top: 6px;
}

.lib-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.lib-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
  background: linear-gradient(150deg, var(--wood-mid-2), var(--wood-dark) 80%);
  border: 1px solid rgba(217, 180, 99, 0.2);
  border-radius: var(--radius-md);
  padding: 12px 14px;
  box-shadow: 0 6px 14px var(--shadow);
}

.lib-item .info {
  flex: 1;
  min-width: 0;
}

.lib-item .title {
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 18px;
  color: var(--parchment);
}

.lib-item .meta {
  font-size: 12px;
  color: var(--parchment-dim);
  margin-top: 2px;
}

.lib-item .actions {
  display: flex;
  gap: 6px;
  flex-shrink: 0;
}

.lib-item .actions button {
  background: rgba(217, 180, 99, 0.12);
  border: 1px solid rgba(217, 180, 99, 0.3);
  color: var(--parchment);
  border-radius: 8px;
  padding: 7px 10px;
  font-size: 12px;
  font-weight: 600;
  cursor: pointer;
}

.lib-item .actions button.danger {
  color: var(--danger-light);
  border-color: var(--danger-light);
}

/* ---------- Modal / Toast ---------- */
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(10, 5, 2, 0.72);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 100;
  padding: 16px;
  backdrop-filter: blur(3px);
}

.modal {
  background: linear-gradient(165deg, var(--wood-mid), var(--wood-dark));
  border: 1px solid rgba(217, 180, 99, 0.25);
  border-radius: var(--radius-lg);
  width: 100%;
  max-width: 400px;
  padding: 22px;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.6);
}

.modal h2 {
  font-family: var(--font-display);
  font-style: italic;
  font-weight: 700;
  font-size: 24px;
  margin: 0 0 14px;
}

.modal-actions {
  display: flex;
  gap: 10px;
  margin-top: 16px;
}

.modal-actions .btn-primary,
.modal-actions .btn-secondary {
  flex: 1;
}

.toast {
  position: fixed;
  left: 50%;
  bottom: 28px;
  transform: translateX(-50%) translateY(16px);
  background: var(--ink);
  color: var(--parchment);
  padding: 10px 18px;
  border-radius: 30px;
  font-size: 13px;
  font-weight: 600;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.5);
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.2s, transform 0.2s;
  z-index: 300;
  border: 1px solid rgba(217, 180, 99, 0.3);
}

.toast.show {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}

footer.credits {
  text-align: center;
  font-size: 11px;
  color: rgba(216, 198, 160, 0.4);
  padding: 28px 10px 8px;
}

/* Mobile */
@media (max-width: 640px) {
  .violin-stage {
    flex-direction: column;
    align-items: center;
  }

  .play-info {
    max-width: 100%;
    width: 100%;
  }

  .duration-bar {
    flex-direction: column;
    align-items: stretch;
  }

  .btn-record,
  .btn-stop {
    margin-left: 0;
  }
}

</style>
</head>
<body>
  <div id="app">
    <!-- Header -->
    <header class="top">
      <div class="logo-wrap" id="headerLogo" aria-hidden="true"></div>
      <h1 class="brand">Docinho de Amendoim</h1>
      <p class="tagline">seu violino digital · clave de sol</p>
    </header>

    <div class="fhole-divider">
      <span class="line"></span>
      <div class="fhole-icon" id="fholeIcon"></div>
      <span class="line"></span>
    </div>

    <!-- Navegação principal -->
    <nav class="tabs" role="tablist">
      <button class="tab active" data-tab="violin" role="tab" aria-selected="true">🎻 Violino</button>
      <button class="tab" data-tab="score" role="tab" aria-selected="false">♪ Partitura</button>
      <button class="tab" data-tab="library" role="tab" aria-selected="false">📚 Biblioteca</button>
    </nav>

    <!-- ========== ABA VIOLINO ========== -->
    <section id="panel-violin" class="panel active" role="tabpanel">
      <div class="violin-stage">
        <!-- Corpo do violino (SVG interativo) -->
        <div class="violin-body-wrap">
          <svg class="violin-svg" viewBox="0 0 320 720" xmlns="http://www.w3.org/2000/svg" aria-label="Violino interativo">
            <!-- Fundo / sombra do corpo -->
            <defs>
              <linearGradient id="woodGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#8B5A2B"/>
                <stop offset="40%" stop-color="#C97D3A"/>
                <stop offset="70%" stop-color="#A05A2C"/>
                <stop offset="100%" stop-color="#6B3A1B"/>
              </linearGradient>
              <linearGradient id="fingerboardGrad" x1="0%" y1="0%" x2="0%" y2="100%">
                <stop offset="0%" stop-color="#1a1008"/>
                <stop offset="100%" stop-color="#0d0804"/>
              </linearGradient>
              <filter id="softShadow" x="-20%" y="-20%" width="140%" height="140%">
                <feDropShadow dx="0" dy="4" stdDeviation="6" flood-color="#000" flood-opacity="0.45"/>
              </filter>
            </defs>

            <!-- Voluta + cravelheira (simplificada) -->
            <g class="scroll" filter="url(#softShadow)">
              <path d="M148 28 C 120 20, 110 48, 128 58 C 118 70, 140 78, 152 68 C 168 78, 190 70, 180 58 C 198 48, 188 20, 160 28 C 158 12, 150 12, 148 28 Z"
                    fill="url(#woodGrad)" stroke="#3A1F10" stroke-width="2"/>
              <!-- Cravelhas -->
              <circle cx="132" cy="48" r="5" fill="#E3A458" stroke="#3A1F10" stroke-width="1"/>
              <circle cx="148" cy="42" r="5" fill="#E3A458" stroke="#3A1F10" stroke-width="1"/>
              <circle cx="164" cy="42" r="5" fill="#E3A458" stroke="#3A1F10" stroke-width="1"/>
              <circle cx="180" cy="48" r="5" fill="#E3A458" stroke="#3A1F10" stroke-width="1"/>
            </g>

            <!-- Braço -->
            <rect x="148" y="72" width="24" height="48" rx="3" fill="url(#woodGrad)" stroke="#3A1F10" stroke-width="1.5"/>

            <!-- Espelho / fingerboard -->
            <rect x="138" y="118" width="44" height="280" rx="4" fill="url(#fingerboardGrad)" stroke="#0a0603" stroke-width="1"/>

            <!-- Marcadores de posição (casas aproximadas — violino não tem trastes, mas posições) -->
            <g class="position-markers" opacity="0.35" stroke="#D9B463" stroke-width="1">
              <line x1="142" y1="155" x2="178" y2="155"/> <!-- 1ª pos ~ -->
              <line x1="142" y1="188" x2="178" y2="188"/>
              <line x1="142" y1="218" x2="178" y2="218"/>
              <line x1="142" y1="245" x2="178" y2="245"/>
              <line x1="142" y1="270" x2="178" y2="270"/>
              <line x1="142" y1="293" x2="178" y2="293"/>
              <line x1="142" y1="314" x2="178" y2="314"/>
              <line x1="142" y1="333" x2="178" y2="333"/>
              <line x1="142" y1="350" x2="178" y2="350"/>
              <line x1="142" y1="366" x2="178" y2="366"/>
            </g>

            <!-- Cordas no braço (G D A E — da esquerda para a direita, como o violinista vê) -->
            <!-- Áreas clicáveis das cordas no fingerboard -->
            <g id="fingerboardHits" class="fingerboard-hits"></g>

            <!-- Linhas visuais das cordas no braço -->
            <g class="strings-neck" stroke-linecap="round">
              <line class="string-line" data-string="G" x1="146" y1="120" x2="146" y2="398" stroke="#C8B89A" stroke-width="1.6"/>
              <line class="string-line" data-string="D" x1="156" y1="120" x2="156" y2="398" stroke="#D4C4A8" stroke-width="1.5"/>
              <line class="string-line" data-string="A" x1="166" y1="120" x2="166" y2="398" stroke="#E0D0B4" stroke-width="1.4"/>
              <line class="string-line" data-string="E" x1="176" y1="120" x2="176" y2="398" stroke="#ECDCBC" stroke-width="1.3"/>
            </g>

            <!-- Cavalete -->
            <path d="M140 398 L180 398 L176 412 L144 412 Z" fill="#F3E6C8" stroke="#3A1F10" stroke-width="1.2"/>

            <!-- Corpo (forma superior + inferior) -->
            <g class="body" filter="url(#softShadow)">
              <!-- Forma clássica do corpo -->
              <path d="M160 412
                       C 100 412, 70 450, 72 500
                       C 74 540, 100 560, 100 580
                       C 70 600, 78 650, 110 670
                       C 130 682, 150 688, 160 688
                       C 170 688, 190 682, 210 670
                       C 242 650, 250 600, 220 580
                       C 220 560, 246 540, 248 500
                       C 250 450, 220 412, 160 412 Z"
                    fill="url(#woodGrad)" stroke="#3A1F10" stroke-width="2.5"/>
              <!-- F-holes -->
              <path d="M108 520 C 98 530, 100 560, 112 568 C 106 555, 108 535, 114 528 M112 545 h-6"
                    fill="none" stroke="#1a1008" stroke-width="3" stroke-linecap="round"/>
              <path d="M212 520 C 222 530, 220 560, 208 568 C 214 555, 212 535, 206 528 M208 545 h6"
                    fill="none" stroke="#1a1008" stroke-width="3" stroke-linecap="round"/>
              <!-- Cordas sobre o corpo até o cordal -->
              <line x1="146" y1="412" x2="150" y2="640" stroke="#C8B89A" stroke-width="1.5"/>
              <line x1="156" y1="412" x2="157" y2="640" stroke="#D4C4A8" stroke-width="1.4"/>
              <line x1="166" y1="412" x2="163" y2="640" stroke="#E0D0B4" stroke-width="1.3"/>
              <line x1="176" y1="412" x2="170" y2="640" stroke="#ECDCBC" stroke-width="1.2"/>
              <!-- Cordal -->
              <ellipse cx="160" cy="648" rx="28" ry="14" fill="#2A1608" stroke="#3A1F10" stroke-width="1.5"/>
              <!-- Queixeira -->
              <ellipse cx="195" cy="655" rx="22" ry="16" fill="#1a1008" stroke="#0d0804" stroke-width="1" transform="rotate(-12 195 655)"/>
            </g>
          </svg>

          <!-- Overlay de notas clicáveis (gerado por JS) -->
          <div class="note-grid" id="noteGrid" aria-label="Casas do violino"></div>
        </div>

        <!-- Painel lateral: corda ativa + nota tocada -->
        <div class="play-info">
          <div class="now-playing">
            <span class="label">Tocando</span>
            <span class="note-name" id="nowNote">—</span>
            <span class="note-detail" id="nowDetail"></span>
          </div>
          <div class="string-legend">
            <div class="leg-item" data-s="G"><span class="dot g"></span> Sol (G3)</div>
            <div class="leg-item" data-s="D"><span class="dot d"></span> Ré (D4)</div>
            <div class="leg-item" data-s="A"><span class="dot a"></span> Lá (A4)</div>
            <div class="leg-item" data-s="E"><span class="dot e"></span> Mi (E5)</div>
          </div>
        </div>
      </div>

      <!-- Seletor de duração -->
      <div class="duration-bar">
        <span class="bar-label">Duração da nota</span>
        <div class="duration-btns" id="durationBtns">
          <button type="button" data-dur="1" title="Semibreve">1</button>
          <button type="button" data-dur="2" title="Mínima">1/2</button>
          <button type="button" data-dur="4" class="active" title="Semínima">1/4</button>
          <button type="button" data-dur="8" title="Colcheia">1/8</button>
          <button type="button" data-dur="16" title="Semicolcheia">1/16</button>
        </div>
        <button type="button" class="btn-record" id="btnRecord" title="Gravar sequência">● Gravar</button>
        <button type="button" class="btn-stop hidden" id="btnStopRec" title="Parar gravação">■ Parar</button>
      </div>

      <div class="record-hint" id="recordHint">Toque as casas para gravar. Depois salve na Biblioteca.</div>
    </section>

    <!-- ========== ABA PARTITURA ========== -->
    <section id="panel-score" class="panel" role="tabpanel" hidden>
      <div class="score-header">
        <div class="field inline">
          <label for="scoreTitle">Título</label>
          <input type="text" id="scoreTitle" placeholder="Minha melodia" maxlength="80">
        </div>
        <div class="field inline">
          <label for="scoreTime">Compasso</label>
          <select id="scoreTime">
            <option value="4/4">4/4</option>
            <option value="3/4">3/4</option>
            <option value="2/4">2/4</option>
            <option value="6/8">6/8</option>
          </select>
        </div>
      </div>

      <div class="score-canvas-wrap">
        <div id="scoreCanvas"></div>
      </div>

      <div class="score-toolbar">
        <div class="group">
          <span class="label">Nota</span>
          <button type="button" data-pitch="c" class="pitch-btn">Dó</button>
          <button type="button" data-pitch="d" class="pitch-btn">Ré</button>
          <button type="button" data-pitch="e" class="pitch-btn">Mi</button>
          <button type="button" data-pitch="f" class="pitch-btn">Fá</button>
          <button type="button" data-pitch="g" class="pitch-btn active">Sol</button>
          <button type="button" data-pitch="a" class="pitch-btn">Lá</button>
          <button type="button" data-pitch="b" class="pitch-btn">Si</button>
        </div>
        <div class="group">
          <span class="label">Oitava</span>
          <button type="button" data-oct="3" class="oct-btn">3</button>
          <button type="button" data-oct="4" class="oct-btn active">4</button>
          <button type="button" data-oct="5" class="oct-btn">5</button>
          <button type="button" data-oct="6" class="oct-btn">6</button>
        </div>
        <div class="group">
          <span class="label">Duração</span>
          <button type="button" data-sdur="w" class="sdur-btn">1</button>
          <button type="button" data-sdur="h" class="sdur-btn">2</button>
          <button type="button" data-sdur="q" class="sdur-btn active">4</button>
          <button type="button" data-sdur="8" class="sdur-btn">8</button>
          <button type="button" data-sdur="16" class="sdur-btn">16</button>
        </div>
        <div class="group">
          <span class="label">Alt.</span>
          <button type="button" data-acc="" class="acc-btn active">♮</button>
          <button type="button" data-acc="#" class="acc-btn">♯</button>
          <button type="button" data-acc="b" class="acc-btn">♭</button>
        </div>
        <div class="group actions">
          <button type="button" id="addScoreNote">+ Nota</button>
          <button type="button" id="addScoreRest">+ Pausa</button>
          <button type="button" id="addScoreBar">| Barra</button>
          <button type="button" id="undoScoreNote">↩</button>
          <button type="button" id="clearScore">Limpar</button>
        </div>
      </div>

      <div class="score-play-bar">
        <button type="button" class="btn-primary" id="playScore">▶ Tocar no violino</button>
        <button type="button" class="btn-secondary" id="stopScore">■ Parar</button>
        <button type="button" class="btn-primary" id="saveScore">Salvar na Biblioteca</button>
      </div>

      <div class="note-list" id="scoreNoteList"></div>
    </section>

    <!-- ========== ABA BIBLIOTECA ========== -->
    <section id="panel-library" class="panel" role="tabpanel" hidden>
      <div class="library-toolbar">
        <input type="search" id="libSearch" placeholder="Buscar músicas..." autocomplete="off">
        <button type="button" class="icon-btn" id="exportLib" title="Exportar backup">Backup</button>
        <button type="button" class="icon-btn" id="importLib" title="Importar">Restaurar</button>
        <input type="file" id="importFile" accept="application/json" class="hidden">
      </div>

      <div class="empty-lib hidden" id="emptyLib">
        <p>Nenhuma música salva ainda.</p>
        <p class="hint">Grave no Violino ou crie na Partitura e salve aqui.</p>
      </div>

      <div class="lib-list" id="libList"></div>
    </section>

    <footer class="credits">feito com carinho para suas horas de violino 🎻</footer>
  </div>

  <!-- Toast -->
  <div class="toast" id="toast"></div>

  <!-- Modal salvar gravação -->
  <div class="modal-overlay hidden" id="saveModal">
    <div class="modal">
      <h2>Salvar gravação</h2>
      <div class="field">
        <label for="recName">Nome da música *</label>
        <input type="text" id="recName" placeholder="Ex: Escala de Sol" required>
      </div>
      <div class="modal-actions">
        <button type="button" class="btn-secondary" id="cancelSave">Cancelar</button>
        <button type="button" class="btn-primary" id="confirmSave">Salvar</button>
      </div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vexflow@4.2.5/build/cjs/vexflow.js"></script>
<script>
/* =========================================================
   Docinho de Amendoim — app.js
   Violino interativo · Partitura · Biblioteca
   ========================================================= */

(function () {
  "use strict";

  const STORAGE_KEY = "docinhoDeAmendoim_violin_v1";
  const VF = typeof Vex !== "undefined" ? Vex.Flow : null;

  /* -------------------------------------------------------
     Dados de notas do violino (clave de sol)
     Cordas em ordem: G3, D4, A4, E5 (da mais grave à aguda)
     Cada corda tem 12 posições (corda solta + 11 casas)
     ------------------------------------------------------- */
  const STRING_NAMES = ["G", "D", "A", "E"];
  const OPEN_STRINGS = {
    G: { midi: 55, name: "Sol", sci: "G3" }, // G3
    D: { midi: 62, name: "Ré", sci: "D4" },  // D4
    A: { midi: 69, name: "Lá", sci: "A4" },  // A4
    E: { midi: 76, name: "Mi", sci: "E5" }   // E5
  };

  const PITCH_NAMES_PT = {
    C: "Dó", D: "Ré", E: "Mi", F: "Fá", G: "Sol", A: "Lá", B: "Si"
  };

  const NOTE_NAMES = ["C", "C#", "D", "D#", "E", "F", "F#", "G", "G#", "A", "A#", "B"];

  function midiToNote(midi) {
    const name = NOTE_NAMES[midi % 12];
    const octave = Math.floor(midi / 12) - 1;
    return { name, octave, sci: name + octave, midi };
  }

  function noteDisplay(midi) {
    const n = midiToNote(midi);
    const base = n.name.replace("#", "");
    const sharp = n.name.includes("#");
    const pt = PITCH_NAMES_PT[base] || base;
    return {
      label: pt + (sharp ? "♯" : "") + n.octave,
      sci: n.sci,
      midi
    };
  }

  /** Frequência em Hz a partir do MIDI */
  function midiToFreq(midi) {
    return 440 * Math.pow(2, (midi - 69) / 12);
  }

  /* -------------------------------------------------------
     Áudio — síntese simples estilo corda / violino
     ------------------------------------------------------- */
  let audioCtx = null;
  let masterGain = null;

  function ensureAudio() {
    if (audioCtx) return audioCtx;
    const Ctx = window.AudioContext || window.webkitAudioContext;
    audioCtx = new Ctx();
    masterGain = audioCtx.createGain();
    masterGain.gain.value = 0.35;
    masterGain.connect(audioCtx.destination);
    return audioCtx;
  }

  /**
   * Toca uma nota com envelope e harmônicos leves (aproximação de corda).
   * @param {number} midi
   * @param {number} durationSec
   */
  function playTone(midi, durationSec) {
    const ctx = ensureAudio();
    if (ctx.state === "suspended") ctx.resume();

    const freq = midiToFreq(midi);
    const now = ctx.currentTime;
    const dur = Math.max(0.08, durationSec);

    // Oscilador principal + harmônicos
    const partials = [
      { mult: 1, gain: 0.55 },
      { mult: 2, gain: 0.22 },
      { mult: 3, gain: 0.12 },
      { mult: 4, gain: 0.06 }
    ];

    const noteGain = ctx.createGain();
    noteGain.connect(masterGain);

    // Envelope ADSR curto
    noteGain.gain.setValueAtTime(0, now);
    noteGain.gain.linearRampToValueAtTime(1, now + 0.02);
    noteGain.gain.exponentialRampToValueAtTime(0.35, now + Math.min(0.25, dur * 0.3));
    noteGain.gain.exponentialRampToValueAtTime(0.001, now + dur);

    partials.forEach((p) => {
      const osc = ctx.createOscillator();
      const g = ctx.createGain();
      osc.type = "sawtooth";
      osc.frequency.value = freq * p.mult;
      g.gain.value = p.gain;
      // Filtro leve para suavizar
      const filter = ctx.createBiquadFilter();
      filter.type = "lowpass";
      filter.frequency.value = 2800 + freq * 0.5;
      filter.Q.value = 0.7;
      osc.connect(g);
      g.connect(filter);
      filter.connect(noteGain);
      osc.start(now);
      osc.stop(now + dur + 0.05);
    });
  }

  /* Duração em segundos (BPM base 80) */
  const BPM = 80;
  function durationToSeconds(divisor) {
    // divisor: 1 = semibreve, 2 = mínima, 4 = semínima...
    const beat = 60 / BPM;
    return (4 / divisor) * beat;
  }

  function vexDurationToSeconds(vexDur) {
    const map = { w: 1, h: 2, q: 4, "8": 8, "16": 16 };
    return durationToSeconds(map[vexDur] || 4);
  }

  /* -------------------------------------------------------
     Estado
     ------------------------------------------------------- */
  let currentDuration = 4; // semínima
  let isRecording = false;
  let recordedNotes = []; // { midi, duration, string, position, time }
  let recordStart = 0;

  // Partitura
  let scoreNotes = [];
  let selectedPitch = "g";
  let selectedOct = 4;
  let selectedSDur = "q";
  let selectedAcc = "";
  let scorePlaying = false;
  let scoreStopFlag = false;

  // Biblioteca
  let library = [];

  /* -------------------------------------------------------
     Logo (gatinho preto com olhos azuis tocando violino)
     ------------------------------------------------------- */
  function renderLogo(target) {
    target.innerHTML = `
      <svg viewBox="0 0 200 220" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <!-- rabo -->
        <path d="M148 165 C 178 150, 182 110, 158 92" fill="none" stroke="#0a0604" stroke-width="16" stroke-linecap="round"/>
        <!-- corpo -->
        <ellipse cx="100" cy="168" rx="56" ry="44" fill="#0d0a08"/>
        <!-- violino -->
        <g>
          <rect x="96" y="60" width="8" height="72" rx="3" fill="#6b3a1b" stroke="#3A1F10" stroke-width="1.5"/>
          <circle cx="100" cy="58" r="8" fill="#6b3a1b" stroke="#3A1F10" stroke-width="1.5"/>
          <path d="M100 128 C 78 128, 74 145, 82 156 C 88 164, 74 168, 78 180 C 82 192, 118 192, 122 180 C 126 168, 112 164, 118 156 C 126 145, 122 128, 100 128 Z"
                fill="#C97D3A" stroke="#3A1F10" stroke-width="2"/>
          <path d="M90 148 q-4 8 0 16" fill="none" stroke="#3A1F10" stroke-width="2" stroke-linecap="round"/>
          <path d="M110 148 q4 8 0 16" fill="none" stroke="#3A1F10" stroke-width="2" stroke-linecap="round"/>
          <line x1="100" y1="132" x2="100" y2="186" stroke="#3A1F10" stroke-width="1"/>
        </g>
        <!-- arco -->
        <path d="M60 190 L150 118" stroke="#E3A458" stroke-width="3.5" stroke-linecap="round"/>
        <path d="M60 190 L150 118" stroke="#F3E6C8" stroke-width="0.8" stroke-linecap="round"/>
        <!-- patas -->
        <ellipse cx="122" cy="182" rx="10" ry="13" fill="#0d0a08" transform="rotate(18 122 182)"/>
        <ellipse cx="70" cy="188" rx="11" ry="14" fill="#0d0a08"/>
        <!-- cabeça preta -->
        <circle cx="98" cy="95" r="50" fill="#0a0806"/>
        <!-- orelhas -->
        <polygon points="58,68 74,18 94,70" fill="#0a0806"/>
        <polygon points="63,62 74,32 84,64" fill="#C97D3A"/>
        <polygon points="138,68 122,18 102,70" fill="#0a0806"/>
        <polygon points="133,62 122,32 112,64" fill="#C97D3A"/>
        <!-- olhos AZUIS -->
        <ellipse cx="78" cy="92" rx="11.5" ry="15" fill="#5B9BD5"/>
        <ellipse cx="118" cy="92" rx="11.5" ry="15" fill="#5B9BD5"/>
        <ellipse cx="78" cy="95" rx="3.4" ry="10.5" fill="#0d0602"/>
        <ellipse cx="118" cy="95" rx="3.4" ry="10.5" fill="#0d0602"/>
        <ellipse cx="75" cy="88" rx="2.2" ry="2.8" fill="#E8F4FF" opacity="0.85"/>
        <ellipse cx="115" cy="88" rx="2.2" ry="2.8" fill="#E8F4FF" opacity="0.85"/>
        <!-- nariz e boca -->
        <polygon points="93,110 103,110 98,116" fill="#C97D3A"/>
        <path d="M98 116 Q90 123 80 118" fill="none" stroke="#F3E6C8" stroke-width="2" stroke-linecap="round"/>
        <path d="M98 116 Q106 123 116 118" fill="none" stroke="#F3E6C8" stroke-width="2" stroke-linecap="round"/>
        <!-- bigodes -->
        <line x1="52" y1="98" x2="14" y2="92" stroke="#F3E6C8" stroke-width="1.4" opacity="0.85"/>
        <line x1="52" y1="106" x2="14" y2="110" stroke="#F3E6C8" stroke-width="1.4" opacity="0.85"/>
        <line x1="144" y1="98" x2="182" y2="92" stroke="#F3E6C8" stroke-width="1.4" opacity="0.85"/>
        <line x1="144" y1="106" x2="182" y2="110" stroke="#F3E6C8" stroke-width="1.4" opacity="0.85"/>
      </svg>`;
  }

  function renderFHole(target) {
    target.innerHTML = `
      <svg viewBox="0 0 24 40" xmlns="http://www.w3.org/2000/svg">
        <path d="M15 2 C 6 6, 4 14, 9 19 C 12 22, 6 25, 9 30 C 11 34, 17 33, 16 38
                 M9 8 q-3 1 -2 4 M15 28 q3 -1 2 -4"
              fill="none" stroke="#D9B463" stroke-width="1.6" stroke-linecap="round"/>
      </svg>`;
  }

  /* -------------------------------------------------------
     Grade de casas do violino
     12 linhas (posições 0–11) × 4 colunas (G D A E)
     ------------------------------------------------------- */
  function buildNoteGrid() {
    const grid = document.getElementById("noteGrid");
    grid.innerHTML = "";

    // Linhas: posição 0 (corda solta) no topo → posições mais altas embaixo
    for (let pos = 0; pos < 12; pos++) {
      for (let s = 0; s < 4; s++) {
        const stringName = STRING_NAMES[s];
        const open = OPEN_STRINGS[stringName];
        const midi = open.midi + pos;
        const info = noteDisplay(midi);

        const btn = document.createElement("button");
        btn.type = "button";
        btn.className = "note-cell";
        btn.dataset.midi = String(midi);
        btn.dataset.string = stringName;
        btn.dataset.pos = String(pos);
        btn.setAttribute("aria-label", `${info.label} corda ${stringName} posição ${pos}`);
        btn.innerHTML = `<span class="tip">${info.label}</span>`;

        btn.addEventListener("click", () => onNoteCellClick(midi, stringName, pos, btn));
        grid.appendChild(btn);
      }
    }
  }

  function onNoteCellClick(midi, stringName, pos, el) {
    const sec = durationToSeconds(currentDuration);
    playTone(midi, sec);

    // Feedback visual
    el.classList.add("playing");
    setTimeout(() => el.classList.remove("playing"), Math.min(sec * 1000, 600));

    const info = noteDisplay(midi);
    document.getElementById("nowNote").textContent = info.label;
    document.getElementById("nowDetail").textContent =
      `${info.sci} · corda ${stringName} · casa ${pos === 0 ? "solta" : pos}`;

    if (isRecording) {
      recordedNotes.push({
        midi,
        duration: currentDuration,
        string: stringName,
        position: pos,
        time: performance.now() - recordStart
      });
      document.getElementById("recordHint").textContent =
        `Gravando… ${recordedNotes.length} nota(s)`;
    }
  }

  /* -------------------------------------------------------
     Controles de duração / gravação
     ------------------------------------------------------- */
  function setupDurationBar() {
    document.getElementById("durationBtns").addEventListener("click", (e) => {
      const btn = e.target.closest("button[data-dur]");
      if (!btn) return;
      currentDuration = parseInt(btn.dataset.dur, 10);
      document.querySelectorAll("#durationBtns button").forEach((b) => {
        b.classList.toggle("active", b === btn);
      });
    });

    document.getElementById("btnRecord").addEventListener("click", startRecording);
    document.getElementById("btnStopRec").addEventListener("click", stopRecording);
  }

  function startRecording() {
    ensureAudio();
    isRecording = true;
    recordedNotes = [];
    recordStart = performance.now();
    document.getElementById("btnRecord").classList.add("hidden", "recording");
    document.getElementById("btnStopRec").classList.remove("hidden");
    document.getElementById("recordHint").textContent = "Gravando… toque as casas";
  }

  function stopRecording() {
    isRecording = false;
    document.getElementById("btnRecord").classList.remove("hidden", "recording");
    document.getElementById("btnStopRec").classList.add("hidden");

    if (recordedNotes.length === 0) {
      document.getElementById("recordHint").textContent = "Nenhuma nota gravada.";
      showToast("Nada gravado.");
      return;
    }

    document.getElementById("recordHint").textContent =
      `${recordedNotes.length} nota(s) gravadas. Salve na biblioteca.`;
    document.getElementById("recName").value = "";
    document.getElementById("saveModal").classList.remove("hidden");
  }

  function setupSaveModal() {
    document.getElementById("cancelSave").addEventListener("click", () => {
      document.getElementById("saveModal").classList.add("hidden");
    });
    document.getElementById("confirmSave").addEventListener("click", () => {
      const name = document.getElementById("recName").value.trim();
      if (!name) {
        showToast("Dê um nome à música.");
        return;
      }
      const item = {
        id: uid(),
        name,
        type: "recording",
        notes: recordedNotes.map((n) => ({ ...n })),
        createdAt: Date.now()
      };
      library.unshift(item);
      saveLibrary();
      document.getElementById("saveModal").classList.add("hidden");
      recordedNotes = [];
      document.getElementById("recordHint").textContent = "Salvo na Biblioteca!";
      showToast("Música salva! 🎻");
      renderLibrary();
    });
    document.getElementById("saveModal").addEventListener("click", (e) => {
      if (e.target.id === "saveModal") {
        document.getElementById("saveModal").classList.add("hidden");
      }
    });
  }

  /* -------------------------------------------------------
     Abas
     ------------------------------------------------------- */
  function setupTabs() {
    document.querySelectorAll(".tab").forEach((tab) => {
      tab.addEventListener("click", () => {
        const id = tab.dataset.tab;
        document.querySelectorAll(".tab").forEach((t) => {
          t.classList.toggle("active", t === tab);
          t.setAttribute("aria-selected", t === tab ? "true" : "false");
        });
        document.querySelectorAll(".panel").forEach((p) => {
          const match = p.id === "panel-" + id;
          p.classList.toggle("active", match);
          p.hidden = !match;
        });
        if (id === "score") renderScoreCanvas();
        if (id === "library") renderLibrary();
      });
    });
  }

  /* -------------------------------------------------------
     Editor de partitura (clave de sol)
     ------------------------------------------------------- */
  function setupScoreEditor() {
    document.querySelectorAll(".pitch-btn").forEach((b) => {
      b.addEventListener("click", () => {
        selectedPitch = b.dataset.pitch;
        document.querySelectorAll(".pitch-btn").forEach((x) => x.classList.toggle("active", x === b));
      });
    });
    document.querySelectorAll(".oct-btn").forEach((b) => {
      b.addEventListener("click", () => {
        selectedOct = parseInt(b.dataset.oct, 10);
        document.querySelectorAll(".oct-btn").forEach((x) => x.classList.toggle("active", x === b));
      });
    });
    document.querySelectorAll(".sdur-btn").forEach((b) => {
      b.addEventListener("click", () => {
        selectedSDur = b.dataset.sdur;
        document.querySelectorAll(".sdur-btn").forEach((x) => x.classList.toggle("active", x === b));
      });
    });
    document.querySelectorAll(".acc-btn").forEach((b) => {
      b.addEventListener("click", () => {
        selectedAcc = b.dataset.acc;
        document.querySelectorAll(".acc-btn").forEach((x) => x.classList.toggle("active", x === b));
      });
    });

    document.getElementById("addScoreNote").addEventListener("click", () => {
      scoreNotes.push({
        type: "note",
        pitch: selectedPitch,
        octave: selectedOct,
        duration: selectedSDur,
        accidental: selectedAcc || null
      });
      refreshScoreUI();
    });

    document.getElementById("addScoreRest").addEventListener("click", () => {
      scoreNotes.push({ type: "rest", duration: selectedSDur });
      refreshScoreUI();
    });

    document.getElementById("addScoreBar").addEventListener("click", () => {
      scoreNotes.push({ type: "bar" });
      refreshScoreUI();
    });

    document.getElementById("undoScoreNote").addEventListener("click", () => {
      scoreNotes.pop();
      refreshScoreUI();
    });

    document.getElementById("clearScore").addEventListener("click", () => {
      if (scoreNotes.length && confirm("Limpar a partitura?")) {
        scoreNotes = [];
        refreshScoreUI();
      }
    });

    document.getElementById("scoreTime").addEventListener("change", renderScoreCanvas);

    document.getElementById("playScore").addEventListener("click", playScoreOnViolin);
    document.getElementById("stopScore").addEventListener("click", () => {
      scoreStopFlag = true;
      scorePlaying = false;
    });

    document.getElementById("saveScore").addEventListener("click", saveCurrentScore);

    document.getElementById("scoreNoteList").addEventListener("click", (e) => {
      if (e.target.dataset.rm !== undefined) {
        scoreNotes.splice(parseInt(e.target.dataset.rm, 10), 1);
        refreshScoreUI();
      }
    });
  }

  function refreshScoreUI() {
    renderScoreCanvas();
    renderScoreNoteList();
  }

  function renderScoreNoteList() {
    const el = document.getElementById("scoreNoteList");
    if (!scoreNotes.length) {
      el.innerHTML = "<em>Nenhuma nota. Escolha altura e toque em + Nota.</em>";
      return;
    }
    const names = { c: "Dó", d: "Ré", e: "Mi", f: "Fá", g: "Sol", a: "Lá", b: "Si" };
    el.innerHTML = scoreNotes
      .map((n, i) => {
        if (n.type === "bar") return `<span class="chip">| <button type="button" data-rm="${i}">×</button></span>`;
        if (n.type === "rest") return `<span class="chip">⏸ ${n.duration} <button type="button" data-rm="${i}">×</button></span>`;
        const acc = n.accidental === "#" ? "♯" : n.accidental === "b" ? "♭" : "";
        return `<span class="chip">${names[n.pitch] || n.pitch}${acc}${n.octave}/${n.duration} <button type="button" data-rm="${i}">×</button></span>`;
      })
      .join("");
  }

  function renderScoreCanvas() {
    const container = document.getElementById("scoreCanvas");
    if (!container || !VF) return;
    container.innerHTML = "";

    const timeSig = document.getElementById("scoreTime").value || "4/4";
    const [beats, beatValue] = timeSig.split("/").map(Number);
    const noteCount = scoreNotes.filter((n) => n.type !== "bar").length || 1;
    const width = Math.max(420, 80 + noteCount * 38);
    const height = 170;

    const renderer = new VF.Renderer(container, VF.Renderer.Backends.SVG);
    renderer.resize(width, height);
    const context = renderer.getContext();

    const stave = new VF.Stave(10, 25, width - 20);
    stave.addClef("treble").addTimeSignature(timeSig);
    stave.setContext(context).draw();

    if (!scoreNotes.length) return;

    const tickables = [];
    scoreNotes.forEach((n) => {
      if (n.type === "bar") {
        tickables.push(new VF.BarNote());
        return;
      }
      if (n.type === "rest") {
        tickables.push(
          new VF.StaveNote({
            clef: "treble",
            keys: ["b/4"],
            duration: n.duration + "r"
          })
        );
        return;
      }
      let key = n.pitch + (n.accidental || "") + "/" + n.octave;
      const note = new VF.StaveNote({
        clef: "treble",
        keys: [key],
        duration: n.duration
      });
      if (n.accidental) {
        note.addAccidental(0, new VF.Accidental(n.accidental));
      }
      tickables.push(note);
    });

    if (!tickables.length) return;

    try {
      const durMap = { w: 4, h: 2, q: 1, "8": 0.5, "16": 0.25 };
      let totalBeats = 0;
      scoreNotes.forEach((n) => {
        if (n.type === "note" || n.type === "rest") totalBeats += durMap[n.duration] || 1;
      });
      const numBeats = Math.max(beats, Math.ceil(totalBeats) || beats);
      const voice = new VF.Voice({ num_beats: numBeats, beat_value: beatValue });
      voice.setStrict(false);
      voice.addTickables(tickables);
      new VF.Formatter().joinVoices([voice]).format([voice], width - 80);
      voice.draw(context, stave);
    } catch (err) {
      console.warn("VexFlow:", err);
    }
  }

  /** Converte nota da partitura → MIDI */
  function scoreNoteToMidi(n) {
    if (n.type !== "note") return null;
    const base = { c: 0, d: 2, e: 4, f: 5, g: 7, a: 9, b: 11 }[n.pitch];
    if (base === undefined) return null;
    let midi = (n.octave + 1) * 12 + base;
    if (n.accidental === "#") midi += 1;
    if (n.accidental === "b") midi -= 1;
    return midi;
  }

  async function playScoreOnViolin() {
    if (!scoreNotes.length) {
      showToast("Adicione notas na partitura.");
      return;
    }
    if (scorePlaying) return;
    ensureAudio();
    scorePlaying = true;
    scoreStopFlag = false;

    for (const n of scoreNotes) {
      if (scoreStopFlag) break;
      if (n.type === "bar") continue;
      const sec = vexDurationToSeconds(n.duration);
      if (n.type === "rest") {
        await wait(sec * 1000);
        continue;
      }
      const midi = scoreNoteToMidi(n);
      if (midi != null) {
        playTone(midi, sec * 0.95);
        const info = noteDisplay(midi);
        document.getElementById("nowNote").textContent = info.label;
        document.getElementById("nowDetail").textContent = "partitura · " + info.sci;
      }
      await wait(sec * 1000);
    }
    scorePlaying = false;
  }

  function wait(ms) {
    return new Promise((r) => setTimeout(r, ms));
  }

  function saveCurrentScore() {
    const title = document.getElementById("scoreTitle").value.trim() || "Partitura sem título";
    if (!scoreNotes.length) {
      showToast("Partitura vazia.");
      return;
    }
    const item = {
      id: uid(),
      name: title,
      type: "score",
      timeSignature: document.getElementById("scoreTime").value,
      notes: scoreNotes.map((n) => ({ ...n })),
      createdAt: Date.now()
    };
    library.unshift(item);
    saveLibrary();
    showToast("Partitura salva! ♪");
    renderLibrary();
  }

  /* -------------------------------------------------------
     Biblioteca
     ------------------------------------------------------- */
  function loadLibrary() {
    try {
      const raw = localStorage.getItem(STORAGE_KEY);
      library = raw ? JSON.parse(raw) : [];
      if (!Array.isArray(library)) library = [];
    } catch {
      library = [];
    }
  }

  function saveLibrary() {
    try {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(library));
      return true;
    } catch {
      showToast("Não foi possível salvar (armazenamento cheio).");
      return false;
    }
  }

  function renderLibrary() {
    const list = document.getElementById("libList");
    const empty = document.getElementById("emptyLib");
    const q = (document.getElementById("libSearch").value || "").trim().toLowerCase();

    let items = library;
    if (q) items = items.filter((x) => (x.name || "").toLowerCase().includes(q));

    if (!library.length) {
      empty.classList.remove("hidden");
      list.innerHTML = "";
      return;
    }
    empty.classList.add("hidden");

    if (!items.length) {
      list.innerHTML =
        '<p style="text-align:center;color:var(--parchment-dim);font-style:italic;">Nada encontrado.</p>';
      return;
    }

    list.innerHTML = items
      .map((item) => {
        const typeLabel = item.type === "score" ? "Partitura" : "Gravação";
        const count =
          item.type === "score"
            ? (item.notes || []).filter((n) => n.type === "note").length
            : (item.notes || []).length;
        const date = new Date(item.createdAt).toLocaleDateString("pt-BR");
        return `
          <div class="lib-item" data-id="${item.id}">
            <div class="info">
              <div class="title">${escapeHtml(item.name)}</div>
              <div class="meta">${typeLabel} · ${count} nota(s) · ${date}</div>
            </div>
            <div class="actions">
              <button type="button" data-act="play">▶ Tocar</button>
              <button type="button" data-act="load">Abrir</button>
              <button type="button" class="danger" data-act="del">Excluir</button>
            </div>
          </div>`;
      })
      .join("");
  }

  function setupLibrary() {
    document.getElementById("libSearch").addEventListener("input", renderLibrary);

    document.getElementById("libList").addEventListener("click", async (e) => {
      const btn = e.target.closest("[data-act]");
      if (!btn) return;
      const itemEl = btn.closest(".lib-item");
      const id = itemEl && itemEl.dataset.id;
      const item = library.find((x) => x.id === id);
      if (!item) return;

      if (btn.dataset.act === "del") {
        if (confirm(`Excluir "${item.name}"?`)) {
          library = library.filter((x) => x.id !== id);
          saveLibrary();
          renderLibrary();
          showToast("Excluído.");
        }
        return;
      }

      if (btn.dataset.act === "play") {
        await playLibraryItem(item);
        return;
      }

      if (btn.dataset.act === "load") {
        if (item.type === "score") {
          scoreNotes = (item.notes || []).map((n) => ({ ...n }));
          document.getElementById("scoreTitle").value = item.name;
          if (item.timeSignature) {
            document.getElementById("scoreTime").value = item.timeSignature;
          }
          // Ir para aba partitura
          document.querySelector('.tab[data-tab="score"]').click();
          refreshScoreUI();
          showToast("Partitura carregada.");
        } else {
          // Gravação: só tocar
          await playLibraryItem(item);
        }
      }
    });

    document.getElementById("exportLib").addEventListener("click", () => {
      const blob = new Blob([JSON.stringify(library, null, 2)], { type: "application/json" });
      const url = URL.createObjectURL(blob);
      const a = document.createElement("a");
      a.href = url;
      a.download = `docinho-biblioteca-${new Date().toISOString().slice(0, 10)}.json`;
      a.click();
      URL.revokeObjectURL(url);
      showToast("Backup baixado!");
    });

    document.getElementById("importLib").addEventListener("click", () => {
      document.getElementById("importFile").click();
    });

    document.getElementById("importFile").addEventListener("change", (e) => {
      const file = e.target.files[0];
      if (!file) return;
      const reader = new FileReader();
      reader.onload = () => {
        try {
          const data = JSON.parse(reader.result);
          if (!Array.isArray(data)) throw new Error("formato");
          const merge = confirm("OK = juntar · Cancelar = substituir tudo");
          if (merge) {
            const ids = new Set(library.map((x) => x.id));
            data.forEach((x) => {
              if (!ids.has(x.id)) library.push(x);
            });
          } else {
            library = data;
          }
          saveLibrary();
          renderLibrary();
          showToast("Backup restaurado!");
        } catch {
          showToast("Arquivo inválido.");
        }
      };
      reader.readAsText(file);
      e.target.value = "";
    });
  }

  async function playLibraryItem(item) {
    ensureAudio();
    scoreStopFlag = false;
    scorePlaying = true;

    if (item.type === "score") {
      for (const n of item.notes || []) {
        if (scoreStopFlag) break;
        if (n.type === "bar") continue;
        const sec = vexDurationToSeconds(n.duration);
        if (n.type === "rest") {
          await wait(sec * 1000);
          continue;
        }
        const midi = scoreNoteToMidi(n);
        if (midi != null) {
          playTone(midi, sec * 0.95);
          const info = noteDisplay(midi);
          document.getElementById("nowNote").textContent = info.label;
          document.getElementById("nowDetail").textContent = item.name;
        }
        await wait(sec * 1000);
      }
    } else {
      // Gravação: usa duração relativa
      for (const n of item.notes || []) {
        if (scoreStopFlag) break;
        const sec = durationToSeconds(n.duration || 4);
        playTone(n.midi, sec * 0.95);
        const info = noteDisplay(n.midi);
        document.getElementById("nowNote").textContent = info.label;
        document.getElementById("nowDetail").textContent = item.name;
        await wait(sec * 1000);
      }
    }
    scorePlaying = false;
  }

  /* -------------------------------------------------------
     Utilitários
     ------------------------------------------------------- */
  function uid() {
    return Date.now().toString(36) + Math.random().toString(36).slice(2, 8);
  }

  function escapeHtml(str) {
    const d = document.createElement("div");
    d.textContent = str || "";
    return d.innerHTML;
  }

  let toastTimer = null;
  function showToast(msg) {
    const t = document.getElementById("toast");
    t.textContent = msg;
    t.classList.add("show");
    clearTimeout(toastTimer);
    toastTimer = setTimeout(() => t.classList.remove("show"), 2400);
  }

  /* -------------------------------------------------------
     Init
     ------------------------------------------------------- */
  function init() {
    renderLogo(document.getElementById("headerLogo"));
    renderFHole(document.getElementById("fholeIcon"));
    buildNoteGrid();
    setupDurationBar();
    setupSaveModal();
    setupTabs();
    setupScoreEditor();
    loadLibrary();
    setupLibrary();
    renderScoreCanvas();

    // Primeiro clique destrava áudio em mobile
    document.body.addEventListener(
      "click",
      () => {
        ensureAudio();
      },
      { once: true }
    );
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", init);
  } else {
    init();
  }
})();

</script>
</body>
</html>
