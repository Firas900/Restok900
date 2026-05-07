
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>RESTOK — Investor Pitch 2026</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Instrument+Serif:ital,wght@0,400;1,400&family=IBM+Plex+Mono:wght@300;400;500&family=Syne:wght@400;700;800&display=swap" rel="stylesheet"/>
<style>
*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html { scroll-behavior: smooth; }

:root {
  --ink:    #0c0d0f;
  --cream:  #f0ebe2;
  --gold:   #c9a84c;
  --gold2:  #e4c97a;
  --usdt:   #26a17b;
  --coral:  #e8705a;
  --border: rgba(255,255,255,0.08);
  --dim:    rgba(240,235,226,0.45);
}

body {
  background: var(--ink);
  color: var(--cream);
  font-family: 'IBM Plex Mono', monospace;
  line-height: 1;
  overflow-x: hidden;
}

/* ════════════════════════════════════
   SLIDE SYSTEM
════════════════════════════════════ */
.slide {
  min-height: 100vh;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 80px 100px;
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid rgba(255,255,255,0.04);
}

.slide-number {
  position: absolute;
  top: 40px; right: 60px;
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.2em;
  color: rgba(255,255,255,0.15);
  text-transform: uppercase;
}

.slide-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  letter-spacing: 0.3em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 32px;
  display: flex;
  align-items: center;
  gap: 16px;
}
.slide-label::before {
  content: '';
  width: 32px;
  height: 1px;
  background: var(--gold);
  opacity: 0.5;
}

/* ════════════════════════════════════
   SLIDE 01 — COVER
════════════════════════════════════ */
.cover {
  background: var(--ink);
  justify-content: space-between;
  padding: 80px 100px;
}
.cover-bg {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 70% 70% at 85% 30%, rgba(201,168,76,0.07) 0%, transparent 60%),
    radial-gradient(ellipse 50% 50% at 20% 80%, rgba(38,161,123,0.05) 0%, transparent 60%);
}
.cover-grid {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(var(--border) 1px, transparent 1px),
    linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 60px 60px;
  mask-image: radial-gradient(ellipse at center, black 30%, transparent 80%);
}
.cover-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
  z-index: 2;
}
.cover-logo-word {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 18px;
  letter-spacing: 0.25em;
  color: var(--cream);
}
.cover-logo-mark {
  display: flex;
  align-items: center;
  gap: 10px;
}
.cover-logo-box {
  width: 36px; height: 36px;
  border: 1.5px solid var(--gold);
  border-radius: 6px;
  display: flex; align-items: center; justify-content: center;
  font-family: 'Instrument Serif', serif;
  font-size: 18px;
  color: var(--gold);
}
.cover-meta {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  color: rgba(255,255,255,0.2);
  letter-spacing: 0.12em;
  text-align: right;
}

.cover-center {
  position: relative;
  z-index: 2;
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 60px 0;
}
.cover-kicker {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 11px;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--usdt);
  margin-bottom: 28px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.kicker-dot {
  width: 7px; height: 7px;
  background: var(--usdt);
  border-radius: 50%;
  animation: breathe 2.5s infinite;
}
@keyframes breathe {
  0%,100% { opacity:1; transform:scale(1); }
  50%      { opacity:0.3; transform:scale(0.5); }
}

.cover-h1 {
  font-family: 'Instrument Serif', serif;
  font-size: clamp(56px, 7vw, 96px);
  font-weight: 400;
  line-height: 1.0;
  color: var(--cream);
  margin-bottom: 32px;
}
.cover-h1 em {
  font-style: italic;
  color: var(--gold);
}
.cover-sub {
  font-size: 13px;
  line-height: 1.8;
  color: var(--dim);
  max-width: 540px;
  letter-spacing: 0.02em;
}

.cover-bottom {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  position: relative;
  z-index: 2;
}
.cover-thesis {
  max-width: 480px;
  border-left: 2px solid var(--gold);
  padding-left: 20px;
}
.cover-thesis p {
  font-family: 'Instrument Serif', serif;
  font-style: italic;
  font-size: 16px;
  color: rgba(240,235,226,0.65);
  line-height: 1.55;
}
.cover-stats {
  display: flex;
  gap: 40px;
}
.cover-stat-val {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 40px;
  color: var(--cream);
  line-height: 1;
}
.cover-stat-lbl {
  font-size: 9px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.3);
  margin-top: 4px;
}

/* ════════════════════════════════════
   SLIDE 02 — THE PROBLEM
════════════════════════════════════ */
.problem { background: #0f1013; }
.problem-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 50% 80% at 0% 50%, rgba(232,112,90,0.04) 0%, transparent 60%);
}
.problem-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: start;
}
.problem-left {}
.problem-h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 72px;
  line-height: 0.88;
  color: var(--cream);
  letter-spacing: 0.02em;
  margin-bottom: 32px;
}
.problem-h2 span { color: var(--coral); }
.problem-body {
  font-size: 12px;
  line-height: 1.9;
  color: var(--dim);
  letter-spacing: 0.02em;
}
.problem-right {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding-top: 24px;
}
.problem-card {
  border: 1px solid rgba(232,112,90,0.2);
  border-radius: 8px;
  padding: 24px;
  position: relative;
  background: rgba(232,112,90,0.03);
  transition: border-color 0.3s;
}
.problem-card:hover { border-color: rgba(232,112,90,0.4); }
.problem-card-num {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 11px;
  letter-spacing: 0.2em;
  color: var(--coral);
  margin-bottom: 10px;
  text-transform: uppercase;
}
.problem-card-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 15px;
  color: var(--cream);
  margin-bottom: 8px;
}
.problem-card-body {
  font-size: 11px;
  line-height: 1.7;
  color: var(--dim);
}
.problem-quote {
  margin-top: 36px;
  padding: 24px;
  border-left: 3px solid var(--coral);
  background: rgba(232,112,90,0.04);
  border-radius: 0 6px 6px 0;
}
.problem-quote p {
  font-family: 'Instrument Serif', serif;
  font-style: italic;
  font-size: 17px;
  color: rgba(240,235,226,0.75);
  line-height: 1.5;
}
.problem-quote cite {
  display: block;
  margin-top: 10px;
  font-style: normal;
  font-size: 10px;
  letter-spacing: 0.12em;
  color: var(--coral);
  text-transform: uppercase;
}

/* ════════════════════════════════════
   SLIDE 03 — THE INSIGHT
════════════════════════════════════ */
.insight {
  background: var(--gold);
  color: var(--ink);
}
.insight-inner {
  position: relative;
  z-index: 2;
}
.insight-bg-text {
  position: absolute;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 280px;
  color: rgba(0,0,0,0.07);
  right: -20px;
  top: 50%;
  transform: translateY(-50%);
  line-height: 1;
  pointer-events: none;
  letter-spacing: -0.02em;
}
.insight .slide-label { color: rgba(0,0,0,0.5); }
.insight .slide-label::before { background: rgba(0,0,0,0.3); }

.insight-h2 {
  font-family: 'Instrument Serif', serif;
  font-size: clamp(36px, 4.5vw, 64px);
  font-weight: 400;
  color: var(--ink);
  line-height: 1.15;
  max-width: 820px;
  margin-bottom: 56px;
}
.insight-h2 em { font-style: italic; }
.insight-h2 strong {
  font-style: normal;
  text-decoration: underline;
  text-decoration-thickness: 3px;
  text-underline-offset: 4px;
}

.insight-three {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2px;
  background: rgba(0,0,0,0.15);
  border: 2px solid rgba(0,0,0,0.2);
  border-radius: 6px;
  overflow: hidden;
}
.insight-pillar {
  background: var(--gold);
  padding: 36px 28px;
  position: relative;
  transition: background 0.25s;
}
.insight-pillar:hover { background: #d4b558; }
.insight-pillar-num {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 80px;
  color: rgba(0,0,0,0.08);
  line-height: 1;
  position: absolute;
  top: 12px; right: 16px;
}
.insight-pillar-icon {
  font-size: 28px;
  margin-bottom: 18px;
}
.insight-pillar-title {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 26px;
  color: var(--ink);
  letter-spacing: 0.03em;
  margin-bottom: 12px;
  line-height: 1.05;
}
.insight-pillar-body {
  font-size: 11px;
  line-height: 1.75;
  color: rgba(0,0,0,0.6);
}
.insight-pillar-check {
  margin-top: 20px;
  font-size: 10px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: rgba(0,0,0,0.45);
  display: flex;
  align-items: center;
  gap: 6px;
}

/* ════════════════════════════════════
   SLIDE 04 — SOLUTION
════════════════════════════════════ */
.solution { background: #0c0d0f; }
.solution-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 60% 60% at 80% 20%, rgba(38,161,123,0.06) 0%, transparent 60%);
}
.solution-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 80px;
  align-items: center;
}
.solution-h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 72px;
  line-height: 0.88;
  color: var(--cream);
  letter-spacing: 0.02em;
  margin-bottom: 28px;
}
.solution-h2 span { color: var(--usdt); }
.solution-body {
  font-size: 12px;
  line-height: 1.9;
  color: var(--dim);
  margin-bottom: 36px;
}

.solution-pillars {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.solution-pillar {
  display: flex;
  align-items: flex-start;
  gap: 18px;
  padding: 20px;
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 8px;
  transition: border-color 0.3s, background 0.3s;
}
.solution-pillar:hover {
  border-color: rgba(38,161,123,0.3);
  background: rgba(38,161,123,0.04);
}
.solution-pillar-icon {
  width: 40px; height: 40px;
  border-radius: 8px;
  background: rgba(38,161,123,0.15);
  border: 1px solid rgba(38,161,123,0.3);
  display: flex; align-items: center; justify-content: center;
  font-size: 18px;
  flex-shrink: 0;
}
.solution-pillar-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 13px;
  color: var(--cream);
  margin-bottom: 5px;
}
.solution-pillar-body {
  font-size: 10px;
  line-height: 1.6;
  color: var(--dim);
}

/* Protocol card */
.protocol-card {
  background: #151719;
  border: 1px solid rgba(201,168,76,0.25);
  border-radius: 12px;
  overflow: hidden;
}
.protocol-card-header {
  background: rgba(201,168,76,0.08);
  border-bottom: 1px solid rgba(201,168,76,0.2);
  padding: 16px 24px;
  font-size: 10px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--gold);
  display: flex;
  align-items: center;
  gap: 8px;
}
.protocol-card-body { padding: 24px; }
.flow-item {
  display: flex;
  gap: 14px;
  align-items: flex-start;
  margin-bottom: 18px;
}
.flow-item:last-child { margin-bottom: 0; }
.flow-dot {
  width: 28px; height: 28px;
  border-radius: 50%;
  background: rgba(201,168,76,0.12);
  border: 1px solid rgba(201,168,76,0.3);
  display: flex; align-items: center; justify-content: center;
  font-size: 11px;
  color: var(--gold);
  flex-shrink: 0;
  font-family: 'Bebas Neue', sans-serif;
}
.flow-content-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 12px;
  color: var(--cream);
  margin-bottom: 3px;
}
.flow-content-body {
  font-size: 10px;
  color: var(--dim);
  line-height: 1.5;
}
.flow-connector {
  width: 1px;
  height: 14px;
  background: linear-gradient(180deg, rgba(201,168,76,0.3), transparent);
  margin-left: 14px;
}

/* ════════════════════════════════════
   SLIDE 05 — MARKET OPPORTUNITY
════════════════════════════════════ */
.market { background: #0f1013; }
.market-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 60% 60% at 70% 50%, rgba(201,168,76,0.05) 0%, transparent 60%);
}
.market-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
}
.market-h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 70px;
  line-height: 0.88;
  color: var(--cream);
  margin-bottom: 24px;
}
.market-h2 em {
  font-style: normal;
  color: var(--gold);
}
.market-body {
  font-size: 12px;
  line-height: 1.9;
  color: var(--dim);
  margin-bottom: 40px;
}
.market-numbers {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}
.market-num-card {
  padding: 24px;
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 8px;
  background: rgba(255,255,255,0.02);
}
.market-num-big {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 44px;
  color: var(--gold);
  line-height: 1;
  margin-bottom: 4px;
}
.market-num-label {
  font-size: 9px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--dim);
  line-height: 1.5;
}

/* TAM/SAM/SOM visual */
.tam-visual {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.tam-row {
  display: flex;
  align-items: center;
  gap: 16px;
}
.tam-bar {
  height: 52px;
  border-radius: 6px;
  display: flex;
  align-items: center;
  padding-left: 18px;
  position: relative;
}
.tam-bar-tam { background: rgba(201,168,76,0.25); border: 1px solid rgba(201,168,76,0.3); width: 100%; }
.tam-bar-sam { background: rgba(201,168,76,0.4);  border: 1px solid rgba(201,168,76,0.5); width: 62%; }
.tam-bar-som { background: var(--gold);             border: none;                            width: 28%; }
.tam-label {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 14px;
  color: var(--ink);
  letter-spacing: 0.08em;
}
.tam-label-light { color: var(--cream); }
.tam-side {
  flex-shrink: 0;
  text-align: right;
}
.tam-side-val {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 22px;
  color: var(--cream);
  line-height: 1;
}
.tam-side-lbl {
  font-size: 9px;
  letter-spacing: 0.1em;
  color: var(--dim);
  text-transform: uppercase;
}

/* ════════════════════════════════════
   SLIDE 06 — BUSINESS MODEL
════════════════════════════════════ */
.business { background: var(--ink); }
.business-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: start;
}
.business-h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 64px;
  line-height: 0.9;
  color: var(--cream);
  margin-bottom: 24px;
}
.business-h2 span { color: var(--gold); }
.business-body {
  font-size: 12px;
  line-height: 1.9;
  color: var(--dim);
  margin-bottom: 36px;
}

.revenue-streams {
  display: flex;
  flex-direction: column;
  gap: 14px;
}
.revenue-stream {
  padding: 22px;
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 8px;
  display: flex;
  align-items: flex-start;
  gap: 18px;
  transition: border-color 0.3s;
}
.revenue-stream:hover { border-color: rgba(201,168,76,0.3); }
.revenue-pct {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 36px;
  color: var(--gold);
  line-height: 1;
  flex-shrink: 0;
  min-width: 70px;
}
.revenue-info-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 13px;
  color: var(--cream);
  margin-bottom: 4px;
}
.revenue-info-body {
  font-size: 10px;
  line-height: 1.6;
  color: var(--dim);
}

/* Musharakah formula box */
.formula-box {
  background: #151719;
  border: 1px solid rgba(201,168,76,0.25);
  border-radius: 12px;
  padding: 32px;
  position: sticky;
  top: 40px;
}
.formula-box-title {
  font-size: 10px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 24px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.formula-line {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 11px 0;
  border-bottom: 1px solid rgba(255,255,255,0.06);
}
.formula-line:last-child { border-bottom: none; }
.formula-k { font-size: 11px; color: var(--dim); letter-spacing: 0.03em; }
.formula-v { font-family: 'Instrument Serif', serif; font-size: 20px; color: var(--cream); }
.formula-v.gold { color: var(--gold); }
.formula-v.green { color: var(--usdt); }
.formula-divider-line {
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(201,168,76,0.4), transparent);
  margin: 8px 0;
}
.formula-split-bar {
  margin-top: 20px;
  height: 12px;
  border-radius: 6px;
  overflow: hidden;
  display: flex;
}
.split-seller { background: linear-gradient(90deg, var(--gold), var(--gold2)); flex: 72.5; }
.split-lp     { background: linear-gradient(90deg, var(--usdt), #3dd6a3);    flex: 27.5; }
.split-labels {
  display: flex;
  justify-content: space-between;
  margin-top: 8px;
  font-size: 10px;
}
.split-l { color: var(--gold); }
.split-r { color: var(--usdt); }

.unit-economics {
  margin-top: 24px;
  padding: 20px;
  background: rgba(38,161,123,0.06);
  border: 1px solid rgba(38,161,123,0.2);
  border-radius: 8px;
}
.ue-title {
  font-size: 9px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--usdt);
  margin-bottom: 14px;
}
.ue-row {
  display: flex;
  justify-content: space-between;
  margin-bottom: 8px;
  font-size: 10px;
}
.ue-k { color: var(--dim); }
.ue-v { color: var(--cream); }
.ue-v.green { color: var(--usdt); }

/* ════════════════════════════════════
   SLIDE 07 — TRACTION / ROADMAP
════════════════════════════════════ */
.roadmap { background: #0f1013; }
.roadmap-h2 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 64px;
  line-height: 0.9;
  color: var(--cream);
  margin-bottom: 52px;
}
.roadmap-h2 span { color: var(--usdt); }

.timeline {
  position: relative;
  padding-left: 40px;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 0; top: 12px; bottom: 12px;
  width: 1px;
  background: linear-gradient(180deg, var(--gold), rgba(201,168,76,0.2), transparent);
}

.timeline-phase {
  display: grid;
  grid-template-columns: 180px 1fr;
  gap: 32px;
  margin-bottom: 40px;
  position: relative;
}
.timeline-phase::before {
  content: '';
  position: absolute;
  left: -44px;
  top: 14px;
  width: 10px; height: 10px;
  border-radius: 50%;
  background: var(--gold);
  border: 2px solid var(--ink);
  box-shadow: 0 0 0 4px rgba(201,168,76,0.2);
}
.timeline-phase.current::before { background: var(--usdt); box-shadow: 0 0 0 4px rgba(38,161,123,0.2); }
.timeline-phase.future::before  { background: rgba(255,255,255,0.15); box-shadow: none; }

.timeline-time {
  font-size: 10px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  padding-top: 2px;
}
.time-label-past    { color: rgba(255,255,255,0.3); }
.time-label-current { color: var(--usdt); }
.time-label-future  { color: rgba(255,255,255,0.2); }

.timeline-content {}
.timeline-phase-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 15px;
  color: var(--cream);
  margin-bottom: 10px;
}
.timeline-milestones {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}
.milestone {
  font-size: 10px;
  letter-spacing: 0.06em;
  padding: 5px 12px;
  border-radius: 3px;
}
.milestone-done    { background: rgba(255,255,255,0.05); color: rgba(255,255,255,0.5); border: 1px solid rgba(255,255,255,0.08); }
.milestone-active  { background: rgba(38,161,123,0.12); color: var(--usdt); border: 1px solid rgba(38,161,123,0.3); }
.milestone-planned { background: transparent; color: rgba(255,255,255,0.25); border: 1px solid rgba(255,255,255,0.08); border-style: dashed; }

/* ════════════════════════════════════
   SLIDE 08 — WHY NOW
════════════════════════════════════ */
.whynow { background: var(--ink); }
.whynow-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 50% 60% at 50% 50%, rgba(201,168,76,0.04) 0%, transparent 70%);
}
.whynow-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
  margin-top: 56px;
}
.whynow-card {
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 10px;
  padding: 32px 28px;
  position: relative;
  transition: border-color 0.3s, transform 0.3s;
  background: rgba(255,255,255,0.02);
}
.whynow-card:hover {
  border-color: rgba(201,168,76,0.3);
  transform: translateY(-3px);
}
.whynow-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 2px;
  border-radius: 10px 10px 0 0;
}
.wc1::before { background: var(--gold); }
.wc2::before { background: var(--usdt); }
.wc3::before { background: var(--coral); }
.wc4::before { background: #7b6cf0; }
.wc5::before { background: var(--gold); }
.wc6::before { background: var(--usdt); }

.whynow-icon { font-size: 30px; margin-bottom: 18px; }
.whynow-title {
  font-family: 'Syne', sans-serif;
  font-weight: 700;
  font-size: 15px;
  color: var(--cream);
  margin-bottom: 10px;
  line-height: 1.2;
}
.whynow-body {
  font-size: 11px;
  line-height: 1.7;
  color: var(--dim);
}
.whynow-stat {
  margin-top: 16px;
  font-family: 'Bebas Neue', sans-serif;
  font-size: 32px;
  line-height: 1;
}
.stat-gold  { color: var(--gold); }
.stat-green { color: var(--usdt); }
.stat-coral { color: var(--coral); }
.stat-purple{ color: #9b8fef; }

/* ════════════════════════════════════
   SLIDE 09 — THE ASK
════════════════════════════════════ */
.ask { background: var(--ink); }
.ask-bg {
  position: absolute;
  inset: 0;
  background:
    radial-gradient(ellipse 60% 70% at 50% 60%, rgba(201,168,76,0.06) 0%, transparent 65%),
    radial-gradient(ellipse 30% 30% at 80% 20%, rgba(38,161,123,0.04) 0%, transparent 50%);
}
.ask-center {
  text-align: center;
  position: relative;
  z-index: 2;
}
.ask-arabic {
  font-family: 'Instrument Serif', serif;
  font-size: 18px;
  color: rgba(201,168,76,0.35);
  letter-spacing: 0.2em;
  margin-bottom: 40px;
  display: block;
}
.ask-h2 {
  font-family: 'Instrument Serif', serif;
  font-size: clamp(44px, 5.5vw, 76px);
  font-weight: 400;
  color: var(--cream);
  line-height: 1.1;
  margin-bottom: 20px;
}
.ask-h2 em { font-style: italic; color: var(--gold); }
.ask-sub {
  font-size: 12px;
  color: var(--dim);
  max-width: 500px;
  margin: 0 auto 56px;
  line-height: 1.8;
}

.ask-boxes {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  max-width: 900px;
  margin: 0 auto 56px;
}
.ask-box {
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 10px;
  padding: 28px;
  background: rgba(255,255,255,0.02);
  text-align: left;
}
.ask-box-label {
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 12px;
}
.ask-box-val {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 38px;
  color: var(--cream);
  line-height: 1;
  margin-bottom: 8px;
}
.ask-box-desc {
  font-size: 10px;
  line-height: 1.6;
  color: var(--dim);
}

.ask-use-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
  max-width: 900px;
  margin: 0 auto 48px;
}
.ask-use-item {
  text-align: center;
  padding: 16px;
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 8px;
  background: rgba(255,255,255,0.02);
}
.ask-use-pct {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 28px;
  color: var(--gold);
  line-height: 1;
  margin-bottom: 4px;
}
.ask-use-label {
  font-size: 9px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--dim);
  line-height: 1.5;
}

.ask-badges {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 0;
}
.ask-badge {
  font-size: 10px;
  letter-spacing: 0.1em;
  color: var(--dim);
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 8px 16px;
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 4px;
}
.ask-badge-dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: var(--gold);
}

/* ════════════════════════════════════
   SLIDE 10 — CLOSE
════════════════════════════════════ */
.close-slide {
  background: #0c0d0f;
  min-height: 60vh;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 80px;
}
.close-bg {
  position: absolute;
  inset: 0;
  background: radial-gradient(ellipse 50% 50% at 50% 50%, rgba(201,168,76,0.05) 0%, transparent 70%);
}
.close-logo {
  font-family: 'Bebas Neue', sans-serif;
  font-size: 80px;
  letter-spacing: 0.12em;
  color: var(--cream);
  position: relative;
  z-index: 2;
  line-height: 1;
  margin-bottom: 8px;
}
.close-logo span { color: var(--gold); }
.close-tagline {
  font-family: 'Instrument Serif', serif;
  font-style: italic;
  font-size: 20px;
  color: var(--dim);
  margin-bottom: 40px;
  position: relative;
  z-index: 2;
}
.close-divider {
  width: 80px; height: 1px;
  background: var(--gold);
  margin: 0 auto 40px;
  opacity: 0.4;
  position: relative;
  z-index: 2;
}
.close-contact {
  font-size: 11px;
  letter-spacing: 0.1em;
  color: var(--dim);
  position: relative;
  z-index: 2;
  line-height: 2;
}
.close-contact strong { color: var(--cream); }

/* ════════════════════════════════════
   NAV DOTS
════════════════════════════════════ */
.nav-dots {
  position: fixed;
  right: 24px;
  top: 50%;
  transform: translateY(-50%);
  display: flex;
  flex-direction: column;
  gap: 8px;
  z-index: 100;
}
.nav-dot {
  width: 6px; height: 6px;
  border-radius: 50%;
  background: rgba(255,255,255,0.2);
  cursor: pointer;
  transition: background 0.3s, transform 0.3s;
}
.nav-dot.active {
  background: var(--gold);
  transform: scale(1.4);
}
.nav-dot:hover { background: rgba(255,255,255,0.5); }

/* ════════════════════════════════════
   PROGRESS BAR
════════════════════════════════════ */
.progress-bar {
  position: fixed;
  top: 0; left: 0;
  height: 2px;
  background: var(--gold);
  z-index: 101;
  transition: width 0.1s;
}

/* ════════════════════════════════════
   CONFIDE STRIP
════════════════════════════════════ */
.confide-strip {
  background: rgba(201,168,76,0.06);
  border-top: 1px solid rgba(201,168,76,0.15);
  border-bottom: 1px solid rgba(201,168,76,0.15);
  padding: 10px 100px;
  font-size: 9px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: rgba(201,168,76,0.4);
  text-align: center;
}
</style>
</head>
<body>

<div class="progress-bar" id="progress"></div>
<div class="nav-dots" id="navDots"></div>

<!-- ══════════════════════════════════
     SLIDE 01 — COVER
══════════════════════════════════ -->
<section class="slide cover" data-slide="1">
  <div class="cover-bg"></div>
  <div class="cover-grid"></div>

  <div class="cover-top">
    <div class="cover-logo-mark">
      <div class="cover-logo-box">R</div>
      <div class="cover-logo-word">RESTOK</div>
    </div>
    <div class="cover-meta">
      Investor Briefing · Series Seed · 2026<br/>
      Confidential — Not for distribution
    </div>
  </div>

  <div class="cover-center">
    <div class="cover-kicker">
      <span class="kicker-dot"></span>
      Sharia-Compliant · USDT Native · GCC + Emerging Markets
    </div>
    <h1 class="cover-h1">
      The e-commerce<br/>
      financing protocol<br/>
      built for the<br/>
      <em>other 4 billion.</em>
    </h1>
    <p class="cover-sub">
      RESTOK connects e-commerce sellers in the GCC to a global pool of USDT liquidity — disbursing working capital as local fiat in under 15 minutes, with no interest charged and every deal Sharia-certified on-chain.
    </p>
  </div>

  <div class="cover-bottom">
    <div class="cover-thesis">
      <p>"Three things must be true at once: it works the first time without a tutorial, it earns yield without requiring DeFi literacy, and it doesn't put your entire financial history on a public ledger by default."</p>
    </div>
    <div class="cover-stats">
      <div>
        <div class="cover-stat-val">$650B</div>
        <div class="cover-stat-lbl">MENA e-com GMV<br/>by 2025</div>
      </div>
      <div>
        <div class="cover-stat-val">72%</div>
        <div class="cover-stat-lbl">SME financing<br/>gap in MENA</div>
      </div>
      <div>
        <div class="cover-stat-val">&lt;15m</div>
        <div class="cover-stat-lbl">Seller to fiat<br/>settlement</div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 02 — THE PROBLEM
══════════════════════════════════ -->
<section class="slide problem" data-slide="2">
  <div class="problem-bg"></div>
  <div class="slide-number">02 / 09</div>
  <div class="slide-label">The Problem</div>

  <div class="problem-grid">
    <div class="problem-left">
      <h2 class="problem-h2">THREE<br/>BROKEN<br/><span>SYSTEMS.</span></h2>
      <p class="problem-body">
        The MENA e-commerce seller sits at the intersection of three systems that each fail them independently — and catastrophically when combined. The marketplace holds their money. The bank won't lend without collateral. And the Islamic finance system is too slow and too analog to serve them at the speed they need.
        <br/><br/>
        Meanwhile, the emerging-market saver — in Malaysia, Nigeria, Indonesia — watches their local currency depreciate and earns 1–3% at a bank that took 3 weeks to open their account. They have smartphones. They have capital. They have no product designed for them.
        <br/><br/>
        These two people need to find each other. RESTOK is the protocol that connects them.
      </p>
      <div class="problem-quote">
        <p>"My Salla store did SAR 800,000 last quarter. Salla pays me in 30 days. My supplier wants payment in 3. My bank said I need 6 months of statements and a guarantor."</p>
        <cite>— Salla seller, Riyadh · interviewed Q1 2026</cite>
      </div>
    </div>

    <div class="problem-right">
      <div class="problem-card">
        <div class="problem-card-num">Problem 01</div>
        <div class="problem-card-title">The Payout Gap</div>
        <div class="problem-card-body">GCC marketplaces hold seller payouts for 14–45 days. A seller with SAR 500,000 in pending payouts has zero access to that capital — while inventory, staff, and suppliers cannot wait. This is a $40B+ structural gap across MENA e-commerce alone.</div>
      </div>
      <div class="problem-card">
        <div class="problem-card-num">Problem 02</div>
        <div class="problem-card-title">Islamic Finance Friction</div>
        <div class="problem-card-body">72% of MENA SMEs cite religious concerns about conventional lending. Islamic banks offer Musharakah — but the process takes 8–12 weeks, requires in-person meetings, and turns away digital sellers without physical assets or long banking history.</div>
      </div>
      <div class="problem-card">
        <div class="problem-card-num">Problem 03</div>
        <div class="problem-card-title">The DeFi Literacy Wall</div>
        <div class="problem-card-body">Existing on-chain yield products offer high returns — but require seed phrases, gas fees, slippage understanding, and tolerance for protocol risk. The person in Lagos or Jakarta with $5,000 to deploy has no product that meets them where they are.</div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 03 — THE INSIGHT
══════════════════════════════════ -->
<section class="slide insight" data-slide="3">
  <div class="insight-bg-text">THREE</div>
  <div class="insight-inner">
    <div class="slide-label">The Core Insight</div>

    <h2 class="insight-h2">
      The product doesn't exist yet because<br/>
      no one has solved all three constraints<br/>
      <em>at the same time.</em> <strong>We did.</strong>
    </h2>

    <div class="insight-three">
      <div class="insight-pillar">
        <div class="insight-pillar-num">1</div>
        <div class="insight-pillar-icon">⚡</div>
        <div class="insight-pillar-title">Works The First Time.<br/>No Tutorial.</div>
        <div class="insight-pillar-body">The blockchain is infrastructure, not the interface. Sellers connect via OAuth. LPs deposit USDT. No seed phrases. No gas management. No whitepaper required. The protocol complexity is invisible — by design, not by accident.</div>
        <div class="insight-pillar-check">→ Zero-friction onboarding proven in pilot</div>
      </div>
      <div class="insight-pillar" style="background: rgba(0,0,0,0.08);">
        <div class="insight-pillar-num">2</div>
        <div class="insight-pillar-icon">💰</div>
        <div class="insight-pillar-title">Real Yield.<br/>No DeFi Literacy.</div>
        <div class="insight-pillar-body">LPs deposit USDT and earn 8–28% APY backed by real trade profit — not algorithmic emissions, not synthetic yields, not protocol token inflation. Profit is split by Musharakah agreement. If the trade doesn't profit, the protocol doesn't profit either.</div>
        <div class="insight-pillar-check">→ Yield backed by verified e-commerce deals</div>
      </div>
      <div class="insight-pillar">
        <div class="insight-pillar-num">3</div>
        <div class="insight-pillar-icon">🔐</div>
        <div class="insight-pillar-title">Privacy By Architecture.<br/>Not Policy.</div>
        <div class="insight-pillar-body">Financial activity is anchored on-chain via hashed certificates — not broadcast. KYC, IBAN, revenue data, and store history stay in encrypted off-chain vaults. The ledger proves compliance without exposing the person. This is not a toggle. It is structural.</div>
        <div class="insight-pillar-check">→ Sharia audit log: proof without dossier</div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 04 — SOLUTION
══════════════════════════════════ -->
<section class="slide solution" data-slide="4">
  <div class="solution-bg"></div>
  <div class="slide-number">04 / 09</div>
  <div class="slide-label">The Solution</div>

  <div class="solution-grid">
    <div>
      <h2 class="solution-h2">THE PROTOCOL<br/>STACK THAT<br/><span>MAKES IT WORK.</span></h2>
      <p class="solution-body">
        RESTOK is not an app. It is a protocol — a set of interlocking technical systems that each solve one of the three constraints, and only work when assembled together. Six months of engineering decisions, each one made with a specific person in mind: the seller in Riyadh who needs money now, and the saver in Lagos who needs yield that doesn't require a PhD.
      </p>

      <div class="solution-pillars">
        <div class="solution-pillar">
          <div class="solution-pillar-icon">🏪</div>
          <div>
            <div class="solution-pillar-title">Store Data API Layer</div>
            <div class="solution-pillar-body">Rutter/Apideck aggregation normalizes Salla, Amazon SA, and Noon into one data schema. OAuth in one tap. Store health scored in 30 seconds from live data.</div>
          </div>
        </div>
        <div class="solution-pillar">
          <div class="solution-pillar-icon">☪️</div>
          <div>
            <div class="solution-pillar-title">Sharia Gatekeeper Middleware</div>
            <div class="solution-pillar-body">Hard technical block — not a checkbox. Funds are released only when a Purchase Order or marketplace payout is confirmed via API. The blockchain cannot execute without it.</div>
          </div>
        </div>
        <div class="solution-pillar">
          <div class="solution-pillar-icon">⛓️</div>
          <div>
            <div class="solution-pillar-title">Vault.sol on Polygon</div>
            <div class="solution-pillar-body">OpenZeppelin-audited smart contract. USDT pools in three tiers. allocateFunds(), distributeYield(), and ShariaAuditLog events make every deal immutable and transparent.</div>
          </div>
        </div>
        <div class="solution-pillar">
          <div class="solution-pillar-icon">🏦</div>
          <div>
            <div class="solution-pillar-title">GCC Fiat Ramp</div>
            <div class="solution-pillar-body">Rain (SAR/BHD) and BitOasis (AED/KWD) convert USDT to fiat in under 60 seconds. SARIE and UAEFTS bank transfer. Seller receives local currency. Never touches crypto.</div>
          </div>
        </div>
      </div>
    </div>

    <div>
      <div class="protocol-card">
        <div class="protocol-card-header">
          ⚙ End-to-End Protocol Flow
        </div>
        <div class="protocol-card-body">
          <div class="flow-item">
            <div class="flow-dot">1</div>
            <div>
              <div class="flow-content-title">OAuth Store Connect</div>
              <div class="flow-content-body">Seller links Salla / Amazon SA / Noon. Rutter normalizes data. KYC completed once. ← 2 minutes.</div>
            </div>
          </div>
          <div class="flow-connector"></div>
          <div class="flow-item">
            <div class="flow-dot">2</div>
            <div>
              <div class="flow-content-title">Store Health Score</div>
              <div class="flow-content-body">Sales velocity (45%), return rate (30%), payout days (25%). Score 0–100. Limit generated real-time.</div>
            </div>
          </div>
          <div class="flow-connector"></div>
          <div class="flow-item">
            <div class="flow-dot" style="background:rgba(201,168,76,0.15);border-color:rgba(201,168,76,0.4);color:var(--gold);">3</div>
            <div>
              <div class="flow-content-title">Sharia Gate ← Critical Path</div>
              <div class="flow-content-body">PO or payout verified via API. Certificate hash generated. Hard block enforced. No asset = no disbursement.</div>
            </div>
          </div>
          <div class="flow-connector"></div>
          <div class="flow-item">
            <div class="flow-dot" style="background:rgba(38,161,123,0.15);border-color:rgba(38,161,123,0.4);color:var(--usdt);">4</div>
            <div>
              <div class="flow-content-title">Vault.sol Disburses USDT</div>
              <div class="flow-content-body">allocateFunds() called by ALLOCATOR_ROLE multisig. ShariaAuditLog emitted on-chain. TxHash recorded.</div>
            </div>
          </div>
          <div class="flow-connector"></div>
          <div class="flow-item">
            <div class="flow-dot" style="background:rgba(38,161,123,0.2);border-color:var(--usdt);color:var(--usdt);">5</div>
            <div>
              <div class="flow-content-title">SAR / AED in Seller's Bank</div>
              <div class="flow-content-body">Rain / BitOasis quote locked in 5s. USDT transferred. SARIE bank wire executed. ← Under 15 minutes total.</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 05 — MARKET
══════════════════════════════════ -->
<section class="slide market" data-slide="5">
  <div class="market-bg"></div>
  <div class="slide-number">05 / 09</div>
  <div class="slide-label">Market Opportunity</div>

  <div class="market-grid">
    <div>
      <h2 class="market-h2">TWO MARKETS.<br/>ONE<br/><em>PROTOCOL.</em></h2>
      <p class="market-body">
        RESTOK sits at the intersection of two under-served, rapidly growing markets: MENA e-commerce seller financing, and emerging-market dollar yield for retail savers. Both are large. Both are underserved by incumbent systems. Neither has a product that solves all three constraints simultaneously.
      </p>

      <div class="market-numbers">
        <div class="market-num-card">
          <div class="market-num-big">$40B+</div>
          <div class="market-num-label">Annual MENA SME financing gap in e-commerce</div>
        </div>
        <div class="market-num-card">
          <div class="market-num-big">$650B</div>
          <div class="market-num-label">MENA e-commerce GMV by 2025 (RedSeer)</div>
        </div>
        <div class="market-num-card">
          <div class="market-num-big">72%</div>
          <div class="market-num-label">MENA SMEs cite religious concerns about conventional financing</div>
        </div>
        <div class="market-num-card">
          <div class="market-num-big">4.2B</div>
          <div class="market-num-label">Underbanked individuals globally with smartphone access</div>
        </div>
      </div>
    </div>

    <div>
      <div class="tam-visual">
        <div style="font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:var(--dim);margin-bottom:20px;">Addressable Market — Seller Financing</div>
        <div class="tam-row">
          <div class="tam-bar tam-bar-tam">
            <span class="tam-label tam-label-light" style="font-size:12px;">TAM</span>
          </div>
          <div class="tam-side">
            <div class="tam-side-val">$320B</div>
            <div class="tam-side-lbl">Global Islamic<br/>trade finance</div>
          </div>
        </div>
        <div class="tam-row">
          <div class="tam-bar tam-bar-sam">
            <span class="tam-label" style="font-size:12px;">SAM</span>
          </div>
          <div class="tam-side">
            <div class="tam-side-val">$40B</div>
            <div class="tam-side-lbl">MENA e-com<br/>seller financing gap</div>
          </div>
        </div>
        <div class="tam-row">
          <div class="tam-bar tam-bar-som">
            <span class="tam-label" style="font-size:12px;">SOM</span>
          </div>
          <div class="tam-side">
            <div class="tam-side-val">$500M</div>
            <div class="tam-side-lbl">3-year target:<br/>GCC + Malaysia</div>
          </div>
        </div>
        <div style="margin-top:32px;padding:20px;background:rgba(38,161,123,0.06);border:1px solid rgba(38,161,123,0.2);border-radius:8px;">
          <div style="font-size:9px;letter-spacing:.18em;text-transform:uppercase;color:var(--usdt);margin-bottom:12px;">LP Opportunity — Dollar Yield for Emerging Markets</div>
          <div style="font-size:11px;line-height:1.75;color:var(--dim);">
            350M+ people in Malaysia, Nigeria, Indonesia, Pakistan, and Egypt hold savings in depreciating local currencies. They earn 1–4% at local banks. RESTOK offers 8–28% APY in USDT — backed by real trade, not algorithms. This market has no incumbent. No product has solved the UX problem. Ours does.
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 06 — BUSINESS MODEL
══════════════════════════════════ -->
<section class="slide business" data-slide="6">
  <div class="slide-number">06 / 09</div>
  <div class="slide-label">Business Model</div>

  <div class="business-grid">
    <div>
      <h2 class="business-h2">HOW<br/>RESTOK<br/><span>MAKES MONEY.</span></h2>
      <p class="business-body">
        Every dollar of revenue is generated from real trade activity — not token inflation, not protocol fees on speculation. RESTOK earns when sellers earn. The business model is structurally Sharia-compliant: no income without underlying commerce.
      </p>

      <div class="revenue-streams">
        <div class="revenue-stream">
          <div class="revenue-pct">10%</div>
          <div>
            <div class="revenue-info-title">Platform Fee on Gross Profit</div>
            <div class="revenue-info-body">Taken from distributable profit before LP and seller split. On $1M GMV at 50% margin, this is $50,000 per deal cycle. Primary revenue driver at scale.</div>
          </div>
        </div>
        <div class="revenue-stream">
          <div class="revenue-pct">2%</div>
          <div>
            <div class="revenue-info-title">Insurance Reserve</div>
            <div class="revenue-info-body">2% of each deal is held in a first-loss insurance fund. If unclaimed, this compounds as protocol-owned capital — a balance sheet that grows with deal volume.</div>
          </div>
        </div>
        <div class="revenue-stream">
          <div class="revenue-pct">B2B</div>
          <div>
            <div class="revenue-info-title">White-Label LP Portal (V2)</div>
            <div class="revenue-info-body">Islamic banks with idle treasury balances pay a licensing fee to deploy into RESTOK pools under their own brand — accessing institutional Musharakah yield infrastructure without building it.</div>
          </div>
        </div>
      </div>
    </div>

    <div>
      <div class="formula-box">
        <div class="formula-box-title">
          ✦ Musharakah Deal Example
        </div>
        <div class="formula-line">
          <span class="formula-k">Gross Sales (S)</span>
          <span class="formula-v">$1,000,000</span>
        </div>
        <div class="formula-line">
          <span class="formula-k">Profit Margin</span>
          <span class="formula-v">50%</span>
        </div>
        <div class="formula-line">
          <span class="formula-k">Gross Profit</span>
          <span class="formula-v">$500,000</span>
        </div>
        <div class="formula-divider-line"></div>
        <div class="formula-line">
          <span class="formula-k">Platform Fee (10%)</span>
          <span class="formula-v gold">$50,000</span>
        </div>
        <div class="formula-line">
          <span class="formula-k">Distributable (D)</span>
          <span class="formula-v">$450,000</span>
        </div>
        <div class="formula-divider-line"></div>
        <div class="formula-line">
          <span class="formula-k">Store Health Score</span>
          <span class="formula-v gold">75 / 100</span>
        </div>
        <div class="formula-line">
          <span class="formula-k">Seller Share (72.5%)</span>
          <span class="formula-v gold">$326,250</span>
        </div>
        <div class="formula-line">
          <span class="formula-k">LP Share (27.5%)</span>
          <span class="formula-v green">$123,750</span>
        </div>

        <div class="formula-split-bar">
          <div class="split-seller"></div>
          <div class="split-lp"></div>
        </div>
        <div class="split-labels">
          <span class="split-l">Seller 72.5%</span>
          <span class="split-r">LP 27.5%</span>
        </div>

        <div class="unit-economics">
          <div class="ue-title">Unit Economics at Scale</div>
          <div class="ue-row">
            <span class="ue-k">Avg deal size</span>
            <span class="ue-v">$75,000 USDT</span>
          </div>
          <div class="ue-row">
            <span class="ue-k">Avg deal duration</span>
            <span class="ue-v">45 days</span>
          </div>
          <div class="ue-row">
            <span class="ue-k">Pool turns/year</span>
            <span class="ue-v">~8×</span>
          </div>
          <div class="ue-row">
            <span class="ue-k">Platform fee/turn</span>
            <span class="ue-v">$7,500</span>
          </div>
          <div class="ue-row">
            <span class="ue-k">Fee/year per $1M pool</span>
            <span class="ue-v green">~$60,000</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 07 — ROADMAP
══════════════════════════════════ -->
<section class="slide roadmap" data-slide="7">
  <div class="slide-number">07 / 09</div>
  <div class="slide-label">Roadmap</div>

  <h2 class="roadmap-h2">FROM PILOT<br/>TO <span>PROTOCOL.</span></h2>

  <div class="timeline">
    <div class="timeline-phase">
      <div class="timeline-time time-label-past">Q1 2026<br/>Foundation</div>
      <div class="timeline-content">
        <div class="timeline-phase-title">MVP — Prove the Core Loop</div>
        <div class="timeline-milestones">
          <span class="milestone milestone-done">Salla OAuth integration</span>
          <span class="milestone milestone-done">Store Health Score v1</span>
          <span class="milestone milestone-done">Sharia Gatekeeper middleware</span>
          <span class="milestone milestone-done">Vault.sol testnet deployment</span>
          <span class="milestone milestone-done">Rain ramp integration</span>
          <span class="milestone milestone-done">5 pilot sellers onboarded</span>
          <span class="milestone milestone-done">First live Musharakah deal</span>
        </div>
      </div>
    </div>

    <div class="timeline-phase current">
      <div class="timeline-time time-label-current">Q2–Q3 2026<br/>← Current</div>
      <div class="timeline-content">
        <div class="timeline-phase-title">V1 — Automate & Expand</div>
        <div class="timeline-milestones">
          <span class="milestone milestone-active">Amazon SA + Noon via Rutter</span>
          <span class="milestone milestone-active">BitOasis integration (AED)</span>
          <span class="milestone milestone-active">Vault.sol mainnet (Polygon)</span>
          <span class="milestone milestone-active">LP self-serve dashboard</span>
          <span class="milestone milestone-planned">Smart contract audit (Certik)</span>
          <span class="milestone milestone-planned">SAMA ExPermit application</span>
          <span class="milestone milestone-planned">50 active sellers</span>
          <span class="milestone milestone-planned">$5M USDT in pools</span>
        </div>
      </div>
    </div>

    <div class="timeline-phase future">
      <div class="timeline-time time-label-future">Q4 2026<br/>Scale</div>
      <div class="timeline-content">
        <div class="timeline-phase-title">V2 — Secondary Markets + Institutional</div>
        <div class="timeline-milestones">
          <span class="milestone milestone-planned">ERC-4626 tokenized LP shares</span>
          <span class="milestone milestone-planned">ML underwriting model</span>
          <span class="milestone milestone-planned">Islamic bank white-label API</span>
          <span class="milestone milestone-planned">Egypt (Fawry ramp) + Kuwait</span>
          <span class="milestone milestone-planned">Malaysia (MY-first LP product)</span>
          <span class="milestone milestone-planned">$50M USDT deployed annualised</span>
        </div>
      </div>
    </div>

    <div class="timeline-phase future">
      <div class="timeline-time time-label-future">2027–2028<br/>Protocol</div>
      <div class="timeline-content">
        <div class="timeline-phase-title">V3 — Open Protocol + RWA Expansion</div>
        <div class="timeline-milestones">
          <span class="milestone milestone-planned">Cross-chain (Base / Arbitrum)</span>
          <span class="milestone milestone-planned">Supplier invoice financing</span>
          <span class="milestone milestone-planned">Open API for Islamic fintech</span>
          <span class="milestone milestone-planned">$500M+ annualised volume</span>
          <span class="milestone milestone-planned">SAMA full license</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 08 — WHY NOW
══════════════════════════════════ -->
<section class="slide whynow" data-slide="8">
  <div class="whynow-bg"></div>
  <div class="slide-number">08 / 09</div>
  <div class="slide-label">Why Now</div>

  <div style="max-width:680px;">
    <h2 style="font-family:'Bebas Neue',sans-serif;font-size:64px;line-height:.9;color:var(--cream);margin-bottom:16px;">SIX FORCES<br/>CONVERGING.</h2>
    <p style="font-size:12px;line-height:1.8;color:var(--dim);">None of these tailwinds existed three years ago simultaneously. The window is open now — and it closes as incumbents arrive.</p>
  </div>

  <div class="whynow-grid">
    <div class="whynow-card wc1">
      <div class="whynow-icon">🏪</div>
      <div class="whynow-title">MENA E-Commerce Explosion</div>
      <div class="whynow-body">Post-pandemic digital commerce adoption permanently shifted purchasing behavior. Salla alone hosts 200,000+ Saudi merchants. Marketplace GMV is growing 28% YoY with no native financing solution.</div>
      <div class="whynow-stat stat-gold">28%</div>
    </div>
    <div class="whynow-card wc2">
      <div class="whynow-icon">🌐</div>
      <div class="whynow-title">Stablecoin Infrastructure Matured</div>
      <div class="whynow-body">USDT on Polygon settles in 2 seconds for under $0.01. Rain and BitOasis now offer institutional-grade API access for fiat conversion. The infrastructure cost to build this in 2022 was prohibitive. Today it is not.</div>
      <div class="whynow-stat stat-green">$0.01</div>
    </div>
    <div class="whynow-card wc3">
      <div class="whynow-icon">☪️</div>
      <div class="whynow-title">Islamic Finance Demand Gap</div>
      <div class="whynow-body">The global Islamic finance market is $3.8T and growing. But digital-native Musharakah products don't exist at scale. There is no Stripe for halal trade financing. RESTOK is building it.</div>
      <div class="whynow-stat stat-coral">$3.8T</div>
    </div>
    <div class="whynow-card wc4">
      <div class="whynow-icon">📱</div>
      <div class="whynow-title">Smartphone Penetration</div>
      <div class="whynow-body">92% smartphone penetration in the GCC. 78% in Malaysia. 60%+ in Nigeria. The distribution problem for financial products in emerging markets is effectively solved. The product problem is not.</div>
      <div class="whynow-stat stat-purple">92%</div>
    </div>
    <div class="whynow-card wc5">
      <div class="whynow-icon">🏛️</div>
      <div class="whynow-title">Regulatory Readiness</div>
      <div class="whynow-body">SAMA's FinTech ExPermit, VARA in Dubai, and CBB sandbox in Bahrain are explicitly designed for protocols like RESTOK. The regulatory pathway is defined. Incumbents have not yet occupied it.</div>
      <div class="whynow-stat stat-gold">3</div>
    </div>
    <div class="whynow-card wc6">
      <div class="whynow-icon">📉</div>
      <div class="whynow-title">Local Currency Debasement</div>
      <div class="whynow-body">The Nigerian naira lost 70% against the dollar in 18 months. The Indonesian rupiah hit 30-year lows. The demand for dollar-denominated savings products in these markets is structural, not cyclical.</div>
      <div class="whynow-stat stat-green">−70%</div>
    </div>
  </div>
</section>

<!-- ══════════════════════════════════
     SLIDE 09 — THE ASK
══════════════════════════════════ -->
<section class="slide ask" data-slide="9">
  <div class="ask-bg"></div>
  <div class="slide-number">09 / 09</div>

  <div class="ask-center">
    <span class="ask-arabic">بِسْمِ اللهِ</span>
    <h2 class="ask-h2">
      Raising <em>$3.5M Seed</em><br/>
      to deploy the first<br/>
      $50M in deals.
    </h2>
    <p class="ask-sub">We have the protocol. We have pilot deals. We have the regulatory path. We need the capital to automate, audit, and scale.</p>

    <div class="ask-boxes">
      <div class="ask-box">
        <div class="ask-box-label">Round Size</div>
        <div class="ask-box-val">$3.5M</div>
        <div class="ask-box-desc">Seed round. SAFE instrument. 20% discount. $18M cap. Targeting close Q3 2026.</div>
      </div>
      <div class="ask-box">
        <div class="ask-box-label">18-Month Target</div>
        <div class="ask-box-val">$50M</div>
        <div class="ask-box-desc">USDT deployed into Musharakah deals. Equivalent to ~667 deals at average $75K deal size.</div>
      </div>
      <div class="ask-box">
        <div class="ask-box-label">Revenue at Target</div>
        <div class="ask-box-val">$3M+</div>
        <div class="ask-box-desc">Platform fees at 10% of gross profit across $50M deployed. 8× pool turns/year.</div>
      </div>
    </div>

    <div style="font-size:10px;letter-spacing:.18em;text-transform:uppercase;color:var(--dim);margin-bottom:16px;">Use of Proceeds</div>
    <div class="ask-use-grid">
      <div class="ask-use-item">
        <div class="ask-use-pct">40%</div>
        <div class="ask-use-label">Engineering &amp; Smart Contract Audit</div>
      </div>
      <div class="ask-use-item">
        <div class="ask-use-pct">25%</div>
        <div class="ask-use-label">Regulatory &amp; Legal (SAMA, VARA, CBB)</div>
      </div>
      <div class="ask-use-item">
        <div class="ask-use-pct">20%</div>
        <div class="ask-use-label">LP Acquisition &amp; Seller Onboarding</div>
      </div>
      <div class="ask-use-item">
        <div class="ask-use-pct">15%</div>
        <div class="ask-use-label">Operations &amp; Sharia Board</div>
      </div>
    </div>

    <div class="ask-badges">
      <div class="ask-badge"><span class="ask-badge-dot"></span> Sharia SSB Certification in progress</div>
      <div class="ask-badge"><span class="ask-badge-dot"></span> Smart contract audit Q3 2026</div>
      <div class="ask-badge"><span class="ask-badge-dot" style="background:var(--usdt)"></span> SAMA ExPermit application filed</div>
      <div class="ask-badge"><span class="ask-badge-dot" style="background:var(--usdt)"></span> 5 pilot deals live on testnet</div>
    </div>
  </div>
</section>

<!-- CLOSE -->
<section class="slide close-slide" data-slide="10">
  <div class="close-bg"></div>
  <div style="position:relative;z-index:2;text-align:center;">
    <div class="close-logo">REST<span>OK</span></div>
    <div class="close-tagline">Capital flows where trade is verified.</div>
    <div class="close-divider"></div>
    <div class="close-contact">
      <strong>restok.io</strong><br/>
      hello@restok.io · Confidential investor briefing 2026<br/><br/>
      Built on Polygon · Musharakah Protocol · USDT Native<br/>
      Sharia Supervisory Board Certified · GCC + Emerging Markets
    </div>
  </div>
</section>

<div class="confide-strip">Confidential — Prepared for accredited investors only — Not a solicitation of investment — Subject to final Sharia board approval</div>

<script>
  // Build nav dots
  const slides = document.querySelectorAll('[data-slide]');
  const dotsContainer = document.getElementById('navDots');
  const progress = document.getElementById('progress');

  slides.forEach((slide, i) => {
    const dot = document.createElement('div');
    dot.className = 'nav-dot' + (i === 0 ? ' active' : '');
    dot.title = `Slide ${i + 1}`;
    dot.addEventListener('click', () => {
      slide.scrollIntoView({ behavior: 'smooth' });
    });
    dotsContainer.appendChild(dot);
  });

  // Update active dot + progress on scroll
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const idx = Array.from(slides).indexOf(entry.target);
        document.querySelectorAll('.nav-dot').forEach((d, i) => {
          d.classList.toggle('active', i === idx);
        });
        const pct = ((idx + 1) / slides.length) * 100;
        progress.style.width = pct + '%';
      }
    });
  }, { threshold: 0.5 });

  slides.forEach(s => observer.observe(s));
</script>
</body>
</html>
