<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gabe Klushin for President – Official Infographic</title>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;600;700&family=Bebas+Neue&family=Source+Serif+4:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #c8c8c8;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 40px 20px;
    font-family: 'Oswald', sans-serif;
  }

  .page {
    width: 1100px;
    min-height: 1700px;
    background: #f5f0e8;
    position: relative;
    overflow: hidden;
    box-shadow: 0 8px 40px rgba(0,0,0,0.4);
  }

  /* Aged paper texture via repeating pattern */
  .page::before {
    content: '';
    position: absolute;
    inset: 0;
    background-image:
      repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.015) 2px, rgba(0,0,0,0.015) 4px),
      repeating-linear-gradient(90deg, transparent, transparent 2px, rgba(0,0,0,0.01) 2px, rgba(0,0,0,0.01) 4px);
    pointer-events: none;
    z-index: 0;
  }

  /* Stars stripe top & bottom */
  .stars-bar {
    background: #1a2c6e;
    height: 48px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    z-index: 2;
    letter-spacing: 12px;
    font-size: 22px;
    color: #fff;
  }

  /* Red stripe below stars */
  .red-stripe {
    background: #b71c1c;
    height: 18px;
  }
  .white-stripe { background: #f5f0e8; height: 12px; }
  .red-stripe-thin { background: #b71c1c; height: 8px; }

  /* ── HERO HEADER ── */
  .hero {
    background: #1a2c6e;
    padding: 32px 60px 24px;
    text-align: center;
    position: relative;
    z-index: 2;
  }
  .hero-eyebrow {
    color: #f5c518;
    font-family: 'Oswald', sans-serif;
    font-size: 18px;
    font-weight: 400;
    letter-spacing: 6px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }
  .hero-name {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 108px;
    line-height: 0.9;
    color: #ffffff;
    text-shadow: 4px 4px 0 #b71c1c, 8px 8px 0 rgba(0,0,0,0.3);
    letter-spacing: 4px;
  }
  .hero-name span { color: #f5c518; }
  .hero-subtitle {
    font-family: 'Oswald', sans-serif;
    font-size: 28px;
    font-weight: 600;
    color: #f5f0e8;
    letter-spacing: 8px;
    text-transform: uppercase;
    margin-top: 12px;
  }
  .hero-tagline {
    font-family: 'Source Serif 4', serif;
    font-style: italic;
    font-size: 19px;
    color: #f5c518;
    margin-top: 10px;
    opacity: 0.9;
  }

  /* stars decoration */
  .star-row {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 14px;
    margin-top: 16px;
  }
  .star { color: #f5c518; font-size: 24px; }
  .star-line { flex: 1; height: 2px; background: linear-gradient(to right, transparent, #f5c518, transparent); max-width: 200px; }

  /* ── SEAL ── */
  .seal-wrap {
    position: absolute;
    top: 20px;
    right: 60px;
    z-index: 10;
  }
  .seal {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    background: #f5c518;
    border: 5px solid #1a2c6e;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-family: 'Oswald', sans-serif;
    font-size: 9px;
    font-weight: 600;
    color: #1a2c6e;
    letter-spacing: 1.5px;
    text-transform: uppercase;
    line-height: 1.3;
    padding: 10px;
    box-shadow: 0 0 0 4px #f5c518, 0 0 0 8px #1a2c6e;
  }
  .seal-eagle { font-size: 36px; line-height: 1; margin-bottom: 4px; }
  .seal2 { top: 20px; left: 60px; }

  /* ── CONTENT AREA ── */
  .content {
    padding: 30px 60px;
    position: relative;
    z-index: 2;
  }

  /* ── POLL SECTION ── */
  .section-label {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 38px;
    color: #b71c1c;
    letter-spacing: 3px;
    border-bottom: 4px solid #1a2c6e;
    padding-bottom: 4px;
    margin-bottom: 20px;
  }
  .section-label span {
    font-family: 'Source Serif 4', serif;
    font-style: italic;
    font-size: 14px;
    color: #888;
    font-weight: 400;
    letter-spacing: 0;
    margin-left: 8px;
  }

  /* Two column layout */
  .two-col { display: flex; gap: 40px; align-items: flex-start; }
  .col-left { flex: 1.2; }
  .col-right { flex: 1; }

  /* ── BAR CHART ── */
  .bar-chart { margin-bottom: 24px; }
  .bar-row {
    display: flex;
    align-items: center;
    margin-bottom: 16px;
    gap: 12px;
  }
  .bar-label {
    font-family: 'Oswald', sans-serif;
    font-size: 15px;
    font-weight: 600;
    width: 80px;
    text-align: right;
    color: #1a2c6e;
    flex-shrink: 0;
  }
  .bar-track {
    flex: 1;
    height: 38px;
    background: rgba(0,0,0,0.08);
    border-radius: 3px;
    position: relative;
    overflow: hidden;
    border: 1px solid rgba(0,0,0,0.1);
  }
  .bar-fill {
    height: 100%;
    display: flex;
    align-items: center;
    padding-left: 10px;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 20px;
    color: #fff;
    letter-spacing: 1px;
    border-radius: 3px;
  }
  .bar-fill.gabe { background: #1a2c6e; width: 93.75%; }
  .bar-fill.other { background: #b71c1c; width: 49.8%; }
  .bar-fill.obama { background: #5a5a5a; width: 0%; }
  .bar-fill.lincoln { background: #7a5a3a; width: 11.1%; }
  .bar-fill.jfk { background: #3a6a7a; width: 22.2%; }
  .bar-fill.wash { background: #6a7a3a; width: 11.1%; }

  .bar-note {
    font-family: 'Source Serif 4', serif;
    font-style: italic;
    font-size: 13px;
    color: #555;
    margin-top: 4px;
  }

  /* ── BIG STAT BOX ── */
  .stat-box {
    background: #1a2c6e;
    border: 4px solid #f5c518;
    padding: 20px 24px;
    text-align: center;
    margin-bottom: 20px;
    position: relative;
  }
  .stat-box::before, .stat-box::after {
    content: '★';
    position: absolute;
    top: 10px;
    color: #f5c518;
    font-size: 18px;
  }
  .stat-box::before { left: 10px; }
  .stat-box::after { right: 10px; }
  .stat-number {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 80px;
    color: #f5c518;
    line-height: 1;
    text-shadow: 2px 2px 0 #b71c1c;
  }
  .stat-label {
    font-family: 'Oswald', sans-serif;
    font-size: 16px;
    color: #fff;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin-top: 4px;
  }
  .stat-vs {
    font-family: 'Source Serif 4', serif;
    font-style: italic;
    font-size: 14px;
    color: rgba(255,255,255,0.75);
    margin-top: 8px;
  }
  .stat-vs strong { color: #f5c518; font-style: normal; }

  /* Claim box */
  .claim-box {
    border: 3px solid #b71c1c;
    background: #fff8f0;
    padding: 14px 18px;
    font-family: 'Oswald', sans-serif;
    font-size: 16px;
    color: #1a2c6e;
    line-height: 1.5;
    margin-bottom: 16px;
  }
  .claim-box strong { color: #b71c1c; font-size: 20px; }

  /* ── QUALIFICATIONS TABLE ── */
  .qual-table {
    width: 100%;
    border-collapse: collapse;
    font-family: 'Oswald', sans-serif;
    font-size: 14px;
    margin-bottom: 28px;
  }
  .qual-table thead tr {
    background: #1a2c6e;
    color: #fff;
  }
  .qual-table thead th {
    padding: 10px 12px;
    text-align: center;
    font-weight: 600;
    letter-spacing: 2px;
    font-size: 13px;
    text-transform: uppercase;
  }
  .qual-table thead th:first-child { text-align: left; }
  .qual-table tbody tr:nth-child(even) { background: rgba(26,44,110,0.06); }
  .qual-table tbody tr:nth-child(odd) { background: rgba(255,255,255,0.6); }
  .qual-table td {
    padding: 9px 12px;
    border-bottom: 1px solid rgba(0,0,0,0.08);
    text-align: center;
    color: #333;
    font-size: 13px;
  }
  .qual-table td:first-child { text-align: left; color: #1a2c6e; font-weight: 600; }
  .check { color: #1a7a1a; font-size: 18px; font-weight: 700; }
  .cross { color: #b71c1c; font-size: 18px; font-weight: 700; }
  .half { color: #e07010; font-size: 16px; }
  .qual-table tfoot tr { background: #f5c518; }
  .qual-table tfoot td {
    padding: 10px 12px;
    font-size: 15px;
    font-weight: 700;
    color: #1a2c6e;
    border-top: 3px solid #1a2c6e;
  }

  /* ── PEER COMPARISON ── */
  .compare-row {
    display: flex;
    gap: 0;
    margin-bottom: 28px;
    border: 3px solid #1a2c6e;
    overflow: hidden;
  }
  .compare-cell {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 16px 8px 12px;
    border-right: 2px solid #1a2c6e;
    text-align: center;
  }
  .compare-cell:last-child { border-right: none; }
  .compare-cell.gabe-cell { background: #1a2c6e; }
  .compare-name {
    font-family: 'Oswald', sans-serif;
    font-size: 14px;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    margin-bottom: 8px;
    color: #1a2c6e;
  }
  .gabe-cell .compare-name { color: #f5c518; }
  .compare-score {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 40px;
    line-height: 1;
    color: #b71c1c;
  }
  .gabe-cell .compare-score { color: #f5c518; font-size: 52px; }
  .compare-denom {
    font-family: 'Oswald', sans-serif;
    font-size: 11px;
    color: #666;
    letter-spacing: 1px;
  }
  .gabe-cell .compare-denom { color: rgba(245,197,24,0.7); }
  .compare-bar-outer {
    width: 100%;
    height: 8px;
    background: rgba(0,0,0,0.1);
    border-radius: 2px;
    margin-top: 8px;
    overflow: hidden;
  }
  .compare-bar-inner {
    height: 100%;
    background: #b71c1c;
    border-radius: 2px;
  }
  .gabe-cell .compare-bar-inner { background: #f5c518; }

  /* ── REQUIREMENTS LIST ── */
  .req-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 28px;
  }
  .req-item {
    display: flex;
    align-items: flex-start;
    gap: 10px;
    background: rgba(255,255,255,0.7);
    border: 1px solid rgba(26,44,110,0.2);
    padding: 10px 12px;
    border-radius: 2px;
  }
  .req-icon {
    font-size: 20px;
    line-height: 1;
    flex-shrink: 0;
    margin-top: 1px;
  }
  .req-text {
    font-family: 'Oswald', sans-serif;
    font-size: 13px;
    font-weight: 400;
    color: #1a2c6e;
    line-height: 1.4;
  }
  .req-text strong { color: #b71c1c; }

  /* ── DIVIDER ── */
  .divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin: 24px 0;
  }
  .divider-line { flex: 1; height: 3px; background: #1a2c6e; }
  .divider-star { font-size: 22px; color: #f5c518; background: #1a2c6e; padding: 0 10px; line-height: 1.6; }

  /* ── POLL BREAKDOWN ── */
  .poll-list {
    columns: 2;
    gap: 20px;
    margin-bottom: 20px;
  }
  .poll-item {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 8px;
    break-inside: avoid;
  }
  .poll-dot {
    width: 24px;
    height: 24px;
    border-radius: 50%;
    background: #1a2c6e;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 12px;
    color: #f5c518;
    font-weight: 700;
    font-family: 'Oswald', sans-serif;
  }
  .poll-dot.no { background: #b71c1c; }
  .poll-name {
    font-family: 'Oswald', sans-serif;
    font-size: 14px;
    color: #333;
  }
  .poll-vote { font-weight: 600; color: #1a2c6e; }
  .poll-vote.no { color: #b71c1c; }

  /* ── MANDATE BANNER ── */
  .mandate-banner {
    background: #b71c1c;
    padding: 18px 60px;
    text-align: center;
    position: relative;
    z-index: 2;
    margin-top: 4px;
  }
  .mandate-banner p {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 42px;
    color: #fff;
    letter-spacing: 5px;
    text-shadow: 2px 2px 0 rgba(0,0,0,0.3);
  }
  .mandate-banner p span { color: #f5c518; }

  /* ── FOOTER ── */
  .footer {
    background: #1a2c6e;
    padding: 16px 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    z-index: 2;
  }
  .footer-text {
    font-family: 'Oswald', sans-serif;
    font-size: 11px;
    color: rgba(255,255,255,0.5);
    line-height: 1.6;
    max-width: 700px;
  }
  .footer-logo {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 22px;
    color: #f5c518;
    letter-spacing: 3px;
    text-align: right;
    line-height: 1.2;
  }
  .footer-logo span { display: block; font-size: 11px; letter-spacing: 4px; font-family: 'Oswald', sans-serif; color: rgba(255,255,255,0.5); }

  /* ── WATERMARK ── */
  .watermark {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) rotate(-30deg);
    font-family: 'Bebas Neue', sans-serif;
    font-size: 140px;
    color: rgba(26,44,110,0.035);
    white-space: nowrap;
    pointer-events: none;
    z-index: 1;
    letter-spacing: 10px;
    user-select: none;
  }

  /* ── RIBBON ── */
  .ribbon {
    position: absolute;
    top: 48px;
    right: 0;
    background: #b71c1c;
    color: #fff;
    font-family: 'Bebas Neue', sans-serif;
    font-size: 15px;
    letter-spacing: 2px;
    padding: 6px 16px 6px 20px;
    clip-path: polygon(12px 0%, 100% 0%, 100% 100%, 12px 100%, 0% 50%);
    z-index: 20;
    white-space: nowrap;
  }

  .source-note {
    font-family: 'Source Serif 4', serif;
    font-style: italic;
    font-size: 10.5px;
    color: #999;
    margin-top: 6px;
  }

  @media print {
    body { background: none; padding: 0; }
    .page { box-shadow: none; width: 11in; min-height: 17in; }
  }
</style>
</head>
<body>
<div class="page">
  <div class="watermark">OFFICIAL DATA</div>

  <!-- TOP STARS BAR -->
  <div class="stars-bar">★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★</div>
  <div class="red-stripe"></div>

  <!-- HERO -->
  <div class="hero" style="position:relative;">
    <div class="seal-wrap">
      <div class="seal">
        <div class="seal-eagle">🦅</div>
        Klushin<br>Administration<br>2025<br>★ ★ ★
      </div>
    </div>
    <div class="seal-wrap seal2">
      <div class="seal">
        <div class="seal-eagle">🇺🇸</div>
        Certified<br>Official<br>Stats<br>★ ★ ★
      </div>
    </div>
    <div class="hero-eyebrow">The People Have Spoken: The Numbers Confirm It</div>
    <div class="hero-name">GABRIEL<br><span>"GABE"</span><br>KLUSHIN</div>
    <div class="hero-subtitle">America's Inevitable President</div>
    <div class="star-row">
      <div class="star-line"></div>
      <div class="star">★</div>
      <div class="star">★</div>
      <div class="star">★</div>
      <div class="star-line"></div>
    </div>
    <div class="hero-tagline">"The data doesn't lie.* (*It might.)"</div>
  </div>

  <div class="white-stripe"></div>
  <div class="red-stripe-thin"></div>
  <div class="white-stripe"></div>

  <!-- CONTENT -->
  <div class="content">

    <!-- TOP TWO COL: Poll + Stats -->
    <div class="two-col">
      <div class="col-left">
        <div class="section-label">Survey Says <span>n=16, margin of error: ±everything</span></div>

        <!-- Poll list -->
        <div class="poll-list">
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Gabe — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Angela — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot no">N</div><div class="poll-name">Carmelo — <span class="poll-vote no">NO</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Emily — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Haomiao — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Michael T. — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Mrs. Me — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Philip — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Corrine — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Dennis — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Jerry — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Sheldon — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Anson — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Anson — <span class="poll-vote">YES*</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Ian — <span class="poll-vote">YES</span></div></div>
          <div class="poll-item"><div class="poll-dot">Y</div><div class="poll-name">Charles — <span class="poll-vote">YES</span></div></div>
        </div>
        <div class="source-note">*Anson was surveyed twice. Both times agreed. Independently verified.</div>
      </div>

      <div class="col-right">
        <!-- Big stat -->
        <div class="stat-box">
          <div class="stat-number">93.75%</div>
          <div class="stat-label">Popular Support for Gabe</div>
          <div class="stat-vs">vs. <strong>49.8%</strong> for the previous guy</div>
        </div>

        <!-- Claim box -->
        <div class="claim-box">
          This means Gabe is approximately <strong>2× BETTER</strong> than the last president mathematically speaking. And maths don't lie.
        </div>

        <!-- Mini bar chart -->
        <div class="section-label" style="font-size:24px; margin-bottom:12px;">Approval Comparison</div>
        <div class="bar-chart">
          <div class="bar-row">
            <div class="bar-label">GABE</div>
            <div class="bar-track"><div class="bar-fill gabe">93.75%</div></div>
          </div>
          <div class="bar-row">
            <div class="bar-label">TRUMP</div>
            <div class="bar-track"><div class="bar-fill other">49.8%</div></div>
          </div>
        </div>
      </div>
    </div>

    <div class="divider">
      <div class="divider-line"></div>
      <div class="divider-star">★ OFFICIAL QUALIFICATIONS ANALYSIS ★</div>
      <div class="divider-line"></div>
    </div>

    <!-- QUALIFICATIONS SECTION -->
    <div class="section-label">Presidential Requirements <span>as determined by professionals in politics™</span></div>

    <div class="two-col" style="gap:32px; align-items:flex-start;">
      <div style="flex:1.4">
        <!-- Full comparison table -->
        <table class="qual-table">
          <thead>
            <tr>
              <th style="text-align:left; width:40%">Requirement</th>
              <th>GABE</th>
              <th>Trump</th>
              <th>Obama</th>
              <th>Lincoln</th>
              <th>JFK</th>
              <th>Wash.</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Russian</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Strong</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="check">✓</span></td>
            </tr>
            <tr>
              <td>Makes random bracelets</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Peels oranges (good)</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Totally legal businesses</td>
              <td><span class="check">✓</span></td>
              <td><span class="half">½</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Disappears randomly</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Survives assassination attempts</td>
              <td><span class="check">✓</span></td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Name starts with "G"</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="check">✓</span></td>
            </tr>
            <tr>
              <td>Last name ends with "N"</td>
              <td><span class="check">✓</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
            <tr>
              <td>Has horrible spelling</td>
              <td><span class="check">✓</span></td>
              <td><span class="half">½</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
              <td><span class="cross">✗</span></td>
            </tr>
          </tbody>
          <tfoot>
            <tr>
              <td>TOTAL SCORE</td>
              <td style="color:#1a2c6e; font-size:18px;">9/9 🏆</td>
              <td>2/9</td>
              <td>0/9</td>
              <td>1/9</td>
              <td>2/9</td>
              <td>1/9</td>
            </tr>
          </tfoot>
        </table>
        <div class="source-note">Data sourced from: professionals in politics™. Peer reviewed by additional professionals.</div>
      </div>

      <div style="flex:1;">
        <div class="section-label" style="font-size:24px; margin-bottom:16px;">Why These Requirements?</div>
        <div class="req-grid">
          <div class="req-item"><div class="req-icon">🇷🇺</div><div class="req-text"><strong>Russian</strong><br>Russians know what they're doing... (I think)</div></div>
          <div class="req-item"><div class="req-icon">💪</div><div class="req-text"><strong>Strong</strong><br>Physical health is just as important</div></div>
          <div class="req-item"><div class="req-icon">📿</div><div class="req-text"><strong>Makes bracelets</strong><br>Shows creativity & fine motor skills</div></div>
          <div class="req-item"><div class="req-icon">🍊</div><div class="req-text"><strong>Peels oranges</strong><br>Come on, fruits are also important</div></div>
          <div class="req-item"><div class="req-icon">💼</div><div class="req-text"><strong>Legal businesses</strong><br>Not too sure about the legal part but businesses are good</div></div>
          <div class="req-item"><div class="req-icon">👻</div><div class="req-text"><strong>Disappears randomly</strong><br>Mystery is a leadership quality</div></div>
          <div class="req-item"><div class="req-icon">🛡️</div><div class="req-text"><strong>Survives attempts</strong><br>Longevity in office is a plus</div></div>
          <div class="req-item"><div class="req-icon">🔤</div><div class="req-text"><strong>Starts with "G"</strong><br>Statistically linked to greatness (source: me)</div></div>
        </div>

        <!-- Score comparison visual -->
        <div class="section-label" style="font-size:22px; margin-bottom:12px; margin-top:8px;">Head-to-Head Scores</div>
        <div class="compare-row">
          <div class="compare-cell gabe-cell">
            <div class="compare-name">GABE</div>
            <div class="compare-score">9</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:100%"></div></div>
          </div>
          <div class="compare-cell">
            <div class="compare-name">Trump</div>
            <div class="compare-score">1.5</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:16.7%"></div></div>
          </div>
          <div class="compare-cell">
            <div class="compare-name">Obama</div>
            <div class="compare-score">0</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:0%"></div></div>
          </div>
          <div class="compare-cell">
            <div class="compare-name">Lincoln</div>
            <div class="compare-score">1</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:11.1%"></div></div>
          </div>
          <div class="compare-cell">
            <div class="compare-name">JFK</div>
            <div class="compare-score">2</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:22.2%"></div></div>
          </div>
          <div class="compare-cell">
            <div class="compare-name">Wash.</div>
            <div class="compare-score">1</div>
            <div class="compare-denom">OUT OF 9</div>
            <div class="compare-bar-outer"><div class="compare-bar-inner" style="width:11.1%"></div></div>
          </div>
        </div>
        <div class="bar-note" style="margin-top:4px;">★ Gabe scores 6× better than most historical presidents ★</div>
      </div>
    </div>

    <div class="divider">
      <div class="divider-line"></div>
      <div class="divider-star">★ SCATTER PLOT ANALYSIS ★</div>
      <div class="divider-line"></div>
    </div>

    <!-- SCATTERPLOT SECTION -->
    <div class="section-label">Qualification Score vs. Voting Percentage <span>correlation = 1.00 (trust me bro)</span></div>

    <!--
      COORDINATE SYSTEM (all math done explicitly):
      Plot area: x from 80 (y-axis) to 900 (right edge), y from 20 (top) to 320 (x-axis)
      Plot width = 820, plot height = 300

      X axis: Qualification score 0–9
        x(score) = 80 + (score / 9) * 820
        score=0  → x=80
        score=1  → x=171
        score=1.5→ x=217
        score=2  → x=262
        score=9  → x=900

      Y axis: Vote % 0–100
        y(pct) = 320 - (pct / 100) * 300
        pct=0   → y=320
        pct=25  → y=245
        pct=39  → y=203  (Washington ~39%)
        pct=45  → y=185  (Lincoln ~45%)
        pct=49.8→ y=171  (Trump 49.8%)
        pct=52  → y=164  (JFK ~52%)
        pct=53  → y=161  (Obama ~53%)
        pct=75  → y=95
        pct=93.75→ y=39  (Gabe 93.75%)
        pct=100 → y=20

      DATA POINTS & LABEL POSITIONS (carefully non-overlapping):
        Obama:      score=0,   pct=53   → cx=80,  cy=161  label RIGHT:  (92, 158)  "Obama 53%"
        Washington: score=1,   pct=39   → cx=171, cy=203  label BELOW:  (171, 222) "Wash. 39%"
        Lincoln:    score=1,   pct=45   → cx=171, cy=185  label LEFT:   (159, 174) "Lincoln 45%" (anchor=end)
        JFK:        score=2,   pct=52   → cx=262, cy=164  label ABOVE:  (262, 151) "JFK 52%"
        Trump:      score=1.5, pct=49.8 → cx=217, cy=171  label BELOW:  (217, 192) "Trump 49.8%"
        Gabe:       score=9,   pct=93.75→ cx=900, cy=39   label LEFT:   (888, 28)  "GABE 93.75%" (anchor=end, above dot)

      Overlap check:
        Obama (80,161) vs Lincoln (171,185): dx=91 >> 20 ✓
        Washington (171,203) vs Lincoln (171,185): same x, dy=18 — dots close but labels go different directions ✓
        Washington label at y=222, Lincoln label at y=174 — 48px apart ✓
        JFK (262,164) vs Trump (217,171): dx=45, dy=7 — close; JFK label above (y=151), Trump label below (y=192) → 41px clear ✓
        Gabe (900,39) far right, nearest point Obama (80,161) → no overlap ✓
        R² box placed at x=370–530, y=230–262 — away from all dots ✓
        Trend line passes near cluster but labels steer clear ✓
    -->
    <div style="background:#fff; border:3px solid #1a2c6e; padding:16px 16px 8px 16px; margin-bottom:6px;">
      <svg width="100%" viewBox="0 0 980 430" xmlns="http://www.w3.org/2000/svg" style="display:block;">
        <defs>
          <marker id="arr2" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
            <path d="M2 1L8 5L2 9" fill="none" stroke="#1a2c6e" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </marker>
        </defs>

        <!-- Y-axis rotated label -->
        <text x="12" y="170" text-anchor="middle" font-family="Oswald,sans-serif" font-size="12" fill="#1a2c6e" font-weight="600" letter-spacing="1" transform="rotate(-90,12,170)">VOTING PERCENTAGE (%)</text>

        <!-- Axes -->
        <line x1="80" y1="20" x2="80" y2="320" stroke="#bbb" stroke-width="1.5"/>
        <line x1="80" y1="320" x2="920" y2="320" stroke="#bbb" stroke-width="1.5"/>

        <!-- Horizontal grid lines & Y labels -->
        <line x1="80" y1="320" x2="920" y2="320" stroke="#e8e8e8" stroke-width="0.8"/>
        <text x="72" y="324" text-anchor="end" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">0%</text>

        <line x1="80" y1="245" x2="920" y2="245" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="72" y="249" text-anchor="end" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">25%</text>

        <line x1="80" y1="170" x2="920" y2="170" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="72" y="174" text-anchor="end" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">50%</text>

        <line x1="80" y1="95" x2="920" y2="95" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="72" y="99" text-anchor="end" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">75%</text>

        <line x1="80" y1="20" x2="920" y2="20" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="72" y="24" text-anchor="end" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">100%</text>

        <!-- Vertical grid lines & X labels -->
        <!-- score=0 → x=80 -->
        <text x="80" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">0</text>

        <!-- score=1 → x=171 -->
        <line x1="171" y1="20" x2="171" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="171" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">1</text>

        <!-- score=2 → x=262 -->
        <line x1="262" y1="20" x2="262" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="262" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">2</text>

        <!-- score=3 → x=353 -->
        <line x1="353" y1="20" x2="353" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="353" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">3</text>

        <!-- score=4 → x=444 -->
        <line x1="444" y1="20" x2="444" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="444" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">4</text>

        <!-- score=5 → x=535 -->
        <line x1="535" y1="20" x2="535" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="535" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">5</text>

        <!-- score=6 → x=626 -->
        <line x1="626" y1="20" x2="626" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="626" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">6</text>

        <!-- score=7 → x=717 -->
        <line x1="717" y1="20" x2="717" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="717" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">7</text>

        <!-- score=8 → x=808 -->
        <line x1="808" y1="20" x2="808" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="808" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">8</text>

        <!-- score=9 → x=900 -->
        <line x1="900" y1="20" x2="900" y2="320" stroke="#e8e8e8" stroke-width="0.8" stroke-dasharray="4,4"/>
        <text x="900" y="338" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#aaa">9</text>

        <!-- Axis titles -->
        <text x="490" y="362" text-anchor="middle" font-family="Oswald,sans-serif" font-size="13" fill="#1a2c6e" font-weight="600" letter-spacing="2">QUALIFICATION SCORE (out of 9)</text>

        <!-- TREND LINE: passes through cluster (170,190) → Gabe (900,39) -->
        <line x1="80" y1="207" x2="900" y2="39" stroke="#f5c518" stroke-width="2.5" stroke-dasharray="8,5" opacity="0.85"/>

        <!-- R² box — placed at x=370–540, y=230–265, away from all dots -->
        <rect x="370" y="230" width="170" height="38" rx="4" fill="#f5c518"/>
        <text x="455" y="244" text-anchor="middle" font-family="Oswald,sans-serif" font-size="12" fill="#1a2c6e" font-weight="600">R² = 1.000000</text>
        <text x="455" y="260" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#1a2c6e">(Perfect correlation!)</text>

        <!-- ═══ DATA POINTS ═══ -->

        <!-- Obama: score=0, pct=53 → cx=80, cy=161 | label RIGHT at (93,158) -->
        <circle cx="80" cy="161" r="9" fill="#5a5a5a" stroke="#fff" stroke-width="2"/>
        <text x="93" y="156" font-family="Oswald,sans-serif" font-size="12" fill="#5a5a5a" font-weight="600">Obama</text>
        <text x="93" y="170" font-family="Oswald,sans-serif" font-size="10" fill="#888">53%</text>

        <!-- Lincoln: score=1, pct=55 → cx=171, cy=155 | label LEFT at (159,148) anchor=end, above dot -->
        <circle cx="171" cy="155" r="9" fill="#7a5a3a" stroke="#fff" stroke-width="2"/>
        <text x="159" y="143" text-anchor="end" font-family="Oswald,sans-serif" font-size="12" fill="#7a5a3a" font-weight="600">Lincoln</text>
        <text x="159" y="157" text-anchor="end" font-family="Oswald,sans-serif" font-size="10" fill="#7a5a3a">55%</text>

        <!-- Washington: score=1, pct=39 → cx=171, cy=203 | label RIGHT at (183,198), below Lincoln label -->
        <circle cx="171" cy="203" r="9" fill="#6a7a3a" stroke="#fff" stroke-width="2"/>
        <text x="183" y="198" font-family="Oswald,sans-serif" font-size="12" fill="#6a7a3a" font-weight="600">Washington</text>
        <text x="183" y="212" font-family="Oswald,sans-serif" font-size="10" fill="#6a7a3a">39%</text>

        <!-- Trump: score=1.5, pct=49.8 → cx=217, cy=171 | label BELOW at (217,193) -->
        <circle cx="217" cy="171" r="9" fill="#b71c1c" stroke="#fff" stroke-width="2"/>
        <text x="217" y="190" text-anchor="middle" font-family="Oswald,sans-serif" font-size="12" fill="#b71c1c" font-weight="600">Trump</text>
        <text x="217" y="204" text-anchor="middle" font-family="Oswald,sans-serif" font-size="10" fill="#b71c1c">49.8%</text>

        <!-- JFK: score=2, pct=50 → cx=262, cy=170 | label ABOVE at (262,152) -->
        <circle cx="262" cy="170" r="9" fill="#3a6a7a" stroke="#fff" stroke-width="2"/>
        <text x="262" y="152" text-anchor="middle" font-family="Oswald,sans-serif" font-size="12" fill="#3a6a7a" font-weight="600">JFK</text>
        <text x="262" y="140" text-anchor="middle" font-family="Oswald,sans-serif" font-size="10" fill="#3a6a7a">50%</text>

        <!-- GABE: score=9, pct=93.75 → cx=900, cy=39 | star + label to the LEFT at (886, ...) -->
        <!-- Star polygon centered at 900,39, radius ~18 -->
        <polygon points="900,21 906,35 922,35 910,44 915,58 900,49 885,58 890,44 878,35 894,35" fill="#f5c518" stroke="#1a2c6e" stroke-width="2.5"/>
        <!-- Label placed LEFT of the star, well within plot -->
        <text x="873" y="77" text-anchor="middle" font-family="Oswald,sans-serif" font-size="14" fill="#1a2c6e" font-weight="700" letter-spacing="1">GABE ★</text>
        <text x="873" y="91" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#b71c1c" font-weight="600">93.75%</text>

        <!-- Arrow: from annotation (700,110) pointing toward Gabe star (895,58) -->
        <line x1="730" y1="113" x2="893" y2="68" stroke="#1a2c6e" stroke-width="1.5" marker-end="url(#arr2)"/>
        <text x="650" y="108" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#1a2c6e" font-style="italic">clear outlier</text>
        <text x="650" y="122" text-anchor="middle" font-family="Oswald,sans-serif" font-size="11" fill="#1a2c6e" font-style="italic">(in a good way)</text>

      </svg>
    </div>
    <div class="source-note" style="margin-bottom:24px;">Historical vote shares sourced from the Bureau of <s>Made-Up Electoral Statistics</s>Real Electoral Statistics. Gabe's 93.75% derived from a poll of many people. Carmelo also included despite being a statistical anomaly.</div>

  </div><!-- end content -->

  <!-- MANDATE BANNER -->
  <div class="mandate-banner">
    <p>AMERICA DEMANDS <span>PRESIDENT KLUSHIN</span>: THE DATA IS CLEAR</p>
  </div>

  <!-- BOTTOM STRIPES -->
  <div class="red-stripe-thin"></div>
  <div class="white-stripe"></div>
  <div class="red-stripe"></div>
  <div class="white-stripe"></div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-text">
      *This infographic is entirely fictional and produced for entertainment and for the purpose of my lame math project only. Gabriel "Gabe" Klushin is a not going to be a real candidate and is not actually running for any public office. All statistics, poll results, and qualifications listed here may or may not have been tweaked slightly for comedic effect. "Professionals in politics™" is not a real organization. The infographic willfully misrepresents data using manipulated charts, cherry-picked sample sizes, and invented qualification criteria. Do not cite this document in legal, academic, or actual political contexts. Carmelo voted no. We acknowledge Carmelo.
    </div>
    <div class="footer-logo">
      KLUSHIN 2026<br>
      <span>FRIENDS OF GABE COMMITTEE</span>
    </div>
  </div>
  <div class="stars-bar" style="height:32px; font-size:16px; letter-spacing:8px;">★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★ ★</div>

</div>
</body>
</html>
