---
layout: default
title: Team
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap');

  :root {
    --bg: #f5f4ef;
    --surface: #eceae2;
    --border: #d8d5c8;
    --accent: #b8860b;
    --accent2: #c4521a;
    --accent3: #1a6fa8;
    --text: #1a1a16;
    --muted: #7a7a72;
  }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    margin: 0;
    padding: 0;
  }

  .page-header {
    padding: 80px 60px 60px;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .page-header::before {
    content: 'Team';
    position: absolute;
    right: -10px;
    top: 50%;
    transform: translateY(-50%);
    font-family: 'Space Mono', monospace;
    font-size: clamp(80px, 12vw, 180px);
    font-weight: 700;
    color: transparent;
    -webkit-text-stroke: 1px #c8c5b8;
    pointer-events: none;
    user-select: none;
    line-height: 1;
    white-space: nowrap;
  }

  .breadcrumb {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 24px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .breadcrumb a { color: var(--muted); text-decoration: none; transition: color 0.2s; }
  .breadcrumb a:hover { color: var(--accent); }
  .breadcrumb span { color: var(--accent); }

  .page-header h1 {
    font-size: clamp(36px, 5vw, 64px);
    font-weight: 800;
    letter-spacing: -0.02em;
    margin: 0 0 16px 0;
    line-height: 1.05;
  }

  .page-header p {
    font-size: 18px;
    color: var(--muted);
    max-width: 480px;
    line-height: 1.7;
    margin: 0;
  }

  /* ── Team grid ── */
  .team-wrap {
    max-width: 1100px;
    margin: 0 auto;
    padding: 80px 60px 100px;
  }

  .team-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
  }

  .member-card {
    background: var(--surface);
    padding: 48px 40px;
    display: flex;
    flex-direction: column;
    gap: 24px;
    transition: background 0.2s;
  }

  .member-card:hover {
    background: #e4e1d8;
  }

  .member-num {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.2em;
    color: var(--accent);
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .member-num::before {
    content: '';
    display: inline-block;
    width: 20px;
    height: 1px;
    background: var(--accent);
  }

  .member-name {
    font-size: 26px;
    font-weight: 800;
    letter-spacing: -0.01em;
    line-height: 1.15;
    color: var(--text);
    margin: 0;
  }

  .member-id {
    display: flex;
    flex-direction: column;
    gap: 6px;
    border-top: 1px solid var(--border);
    padding-top: 20px;
  }

  .member-id-label {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .member-id-value {
    font-family: 'Space Mono', monospace;
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
  }

  /* ── Doc nav ── */
  .doc-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 40px 60px;
    border-top: 1px solid var(--border);
    flex-wrap: wrap;
    gap: 16px;
  }

  .doc-nav a {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: color 0.2s;
  }

  .doc-nav a:hover { color: var(--accent); }

  .doc-nav-center {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #aaa9a0;
  }

  @media (max-width: 768px) {
    .page-header, .team-wrap { padding-left: 24px; padding-right: 24px; }
    .team-grid { grid-template-columns: 1fr; }
    .doc-nav { padding: 32px 24px; }
    .page-header::before { display: none; }
  }
</style>

<div class="page-header">
  <div class="breadcrumb">
    <a href="index.html">Home</a>
    /
    <span>Team</span>
  </div>
  <h1>Power of Three</h1>
  <p>The team behind the PowerOf2 project — CS 175, UC Irvine.</p>
</div>

<div class="team-wrap">
  <div class="team-grid">

    <div class="member-card">
      <span class="member-num">01</span>
      <h2 class="member-name">Amy Lee</h2>
      <div class="member-id">
        <span class="member-id-label">UCI Net ID</span>
        <span class="member-id-value">leeat5</span>
      </div>
    </div>

    <div class="member-card">
      <span class="member-num">02</span>
      <h2 class="member-name">Michelle Lee</h2>
      <div class="member-id">
        <span class="member-id-label">UCI Net ID</span>
        <span class="member-id-value">michel27</span>
      </div>
    </div>

    <div class="member-card">
      <span class="member-num">03</span>
      <h2 class="member-name">Rebecca Tio</h2>
      <div class="member-id">
        <span class="member-id-label">UCI Net ID</span>
        <span class="member-id-value">tior</span>
      </div>
    </div>

  </div>
</div>

<div class="doc-nav">
  <a href="index.html">← Home</a>
  <span class="doc-nav-center">PowerOf2 · CS 175</span>
  <a href="proposal.html">Proposal →</a>
</div>
