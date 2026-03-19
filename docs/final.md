---
layout: default
title: Final Report
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

  /* ── Page Header ── */
  .page-header {
    padding: 80px 60px 60px;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .page-header::before {
    content: 'Final';
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
    max-width: 560px;
    line-height: 1.7;
    margin: 0;
  }

  /* ── Layout ── */
  .content-wrap {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 60px 100px;
  }

  .section {
    padding: 72px 0;
    border-bottom: 1px solid var(--border);
    display: grid;
    grid-template-columns: 260px 1fr;
    gap: 60px;
    align-items: start;
  }

  .section:last-child { border-bottom: none; }

  .section-meta { padding-top: 6px; }

  .section-num {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .section-num::before {
    content: '';
    display: inline-block;
    width: 20px;
    height: 1px;
    background: var(--accent);
  }

  .section-title {
    font-size: 26px;
    font-weight: 800;
    letter-spacing: -0.01em;
    line-height: 1.2;
    margin: 0;
    color: var(--text);
  }

  .section-body {
    font-size: 17px;
    line-height: 1.9;
    color: #4a4a44;
  }

  .section-body p { margin: 0 0 20px 0; }
  .section-body p:last-child { margin-bottom: 0; }
  .section-body strong { color: var(--text); font-weight: 700; }

  /* ── Sub-heading ── */
  .sub-heading {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    margin: 32px 0 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .sub-heading::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── Progress states ── */
  .progress-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1px;
    background: var(--border);
    margin: 24px 0;
  }

  .progress-card {
    background: var(--surface);
    padding: 28px 24px;
  }

  .progress-label {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .progress-label::before {
    content: '';
    display: inline-block;
    width: 14px;
    height: 1px;
    background: var(--accent);
  }

  .progress-card p {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.75;
    margin: 0;
  }

  /* ── Key design choices ── */
  .design-grid {
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
    margin-bottom: 32px;
  }

  .design-card {
    background: var(--surface);
    padding: 24px 28px;
    display: grid;
    grid-template-columns: 28px 1fr;
    gap: 16px;
    align-items: start;
  }

  .design-icon {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--accent);
    padding-top: 3px;
  }

  .design-content {}

  .design-title {
    font-size: 16px;
    font-weight: 700;
    color: var(--text);
    margin: 0 0 6px 0;
    line-height: 1.3;
  }

  .design-desc {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.75;
    margin: 0;
  }

  /* ── Math formula block ── */
  .formula-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent);
    padding: 20px 24px;
    margin: 20px 0;
    font-family: 'Space Mono', monospace;
    font-size: 15px;
    color: var(--text);
    overflow-x: auto;
    white-space: pre;
  }

  /* ── Hyperparameter grid ── */
  .hyperparam-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1px;
    background: var(--border);
    margin: 20px 0;
  }

  .hyperparam-item {
    background: var(--surface);
    padding: 16px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
  }

  .hyperparam-key {
    font-family: 'Space Mono', monospace;
    font-size: 14px;
    color: var(--muted);
  }

  .hyperparam-val {
    font-family: 'Space Mono', monospace;
    font-size: 15px;
    font-weight: 700;
    color: var(--accent);
  }

  /* ── Bug / fix cards ── */
  .bug-list {
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
    margin-bottom: 24px;
  }

  .bug-card {
    background: var(--surface);
    padding: 28px 32px;
  }

  .bug-header {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    margin-bottom: 14px;
  }

  .bug-tag {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    padding: 4px 10px;
    border: 1px solid;
    white-space: nowrap;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .bug-tag.issue   { color: var(--accent2); border-color: var(--accent2); }
  .bug-tag.fix     { color: #5ec47a;        border-color: #5ec47a; }
  .bug-tag.insight { color: var(--accent3); border-color: var(--accent3); }

  .bug-title {
    font-size: 17px;
    font-weight: 700;
    color: var(--text);
    line-height: 1.4;
  }

  .bug-body {
    font-size: 15px;
    color: var(--muted);
    line-height: 1.8;
  }

  .bug-fix {
    margin-top: 14px;
    padding-top: 14px;
    border-top: 1px solid var(--border);
    display: flex;
    gap: 14px;
    align-items: flex-start;
  }

  .bug-fix p {
    font-size: 13px;
    color: #4a4a44;
    line-height: 1.7;
    margin: 0;
  }

  /* ── Evaluation image ── */
  .eval-img-wrap {
    position: relative;
    margin: 24px 0;
    display: inline-block;
    width: 100%;
  }

  .eval-img-wrap::before {
    content: '';
    position: absolute;
    inset: -1px;
    border: 1px solid var(--border);
    pointer-events: none;
    z-index: 1;
  }

  .eval-img-wrap.no-caption::after { display: none; }

  .eval-img-wrap img {
    display: block;
    width: 100%;
    height: auto;
  }

  .img-caption {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-top: 10px;
  }

  /* ── Stat row ── */
  .stat-row {
    display: flex;
    gap: 40px;
    margin: 24px 0;
    flex-wrap: wrap;
  }

  .stat { display: flex; flex-direction: column; gap: 4px; }

  .stat-value {
    font-family: 'Space Mono', monospace;
    font-size: 28px;
    font-weight: 700;
    color: var(--accent);
    line-height: 1;
  }

  .stat-label {
    font-size: 13px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
  }

  /* ── Comparison table ── */
  .compare-table {
    width: 100%;
    border-collapse: collapse;
    margin: 24px 0;
    font-size: 15px;
  }

  .compare-table th {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--accent);
    padding: 14px 20px;
    background: var(--surface);
    border: 1px solid var(--border);
    text-align: left;
    font-weight: 400;
  }

  .compare-table td {
    padding: 14px 20px;
    border: 1px solid var(--border);
    color: #4a4a44;
    vertical-align: top;
    line-height: 1.6;
  }

  .compare-table tr:nth-child(even) td { background: var(--surface); }
  .compare-table td:first-child { font-weight: 700; color: var(--text); font-size: 14px; }

  /* ── Goals list ── */
  .goals-list {
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
  }

  .goal-item {
    background: var(--surface);
    padding: 20px 28px;
    display: flex;
    align-items: center;
    gap: 16px;
    font-size: 16px;
    color: #4a4a44;
    line-height: 1.6;
  }

  .goal-dot {
    width: 6px;
    height: 6px;
    border-radius: 50%;
    background: var(--accent);
    flex-shrink: 0;
  }

  .goal-dot.pending { background: var(--muted); }

  /* ── Resources ── */
  .refs-list {
    display: flex;
    flex-direction: column;
    gap: 0;
    border-top: 1px solid var(--border);
  }

  .ref-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 18px 0;
    border-bottom: 1px solid var(--border);
    text-decoration: none;
    color: var(--muted);
    font-size: 16px;
    transition: color 0.2s;
    gap: 20px;
  }

  .ref-item:hover { color: var(--text); }
  .ref-item:hover .ref-arrow { color: var(--accent); transform: translate(4px, -4px); }

  .ref-name { font-weight: 600; color: var(--text); font-size: 14px; min-width: 220px; }
  .ref-url { font-family: 'Space Mono', monospace; font-size: 11px; color: var(--muted); flex: 1; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
  .ref-arrow { font-size: 14px; transition: transform 0.2s, color 0.2s; flex-shrink: 0; }

  /* ── AI disclaimer tags ── */
  .ai-tags {
    display: flex;
    flex-direction: column;
    gap: 1px;
    background: var(--border);
  }

  .ai-tag-item {
    background: var(--surface);
    padding: 16px 24px;
    font-size: 16px;
    color: #4a4a44;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .ai-tag-item::before {
    content: '⌥';
    color: var(--accent);
    font-size: 14px;
    flex-shrink: 0;
  }

  /* ── Video embed ── */
  .video-wrapper {
    position: relative;
    width: 100%;
    padding-bottom: 56.25%;
    height: 0;
    overflow: hidden;
    border: 1px solid var(--border);
    margin-top: 20px;
  }

  .video-wrapper iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
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
    .page-header, .content-wrap { padding-left: 24px; padding-right: 24px; }
    .section { grid-template-columns: 1fr; gap: 24px; }
    .hyperparam-grid, .progress-grid { grid-template-columns: 1fr; }
    .doc-nav { padding: 32px 24px; }
    .page-header::before { display: none; }
  }
</style>

<div class="page-header">
  <div class="breadcrumb">
    <a href="index.html">Home</a>
    /
    <span>Final Report</span>
  </div>
  <h1>Final Report</h1>
  <p>A comprehensive overview of our approach, models, results, and insights from training agents to play 2048.</p>
</div>

<div class="content-wrap">

  <!-- Video -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">00</div>
      <h2 class="section-title">Video Submission</h2>
    </div>
    <div class="section-body">
      <p>A final walkthrough video covering our complete approach, all three models, results, and takeaways.</p>
      <div class="video-wrapper">
        <iframe
          src="https://www.youtube.com/embed/YkONd-Powgs"
          title="PowerOf2 — Final Video Submission"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          allowfullscreen>
        </iframe>
      </div>
    </div>
  </div>

  <!-- Introduction -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">01</div>
      <h2 class="section-title">Introduction</h2>
    </div>
    <div class="section-body">
      <div class="sub-heading">What is 2048?</div>

      <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--border); margin: 20px 0;">
        <div class="eval-img-wrap no-caption" style="margin: 0;">
          <img src="1.png" alt="2048 game example" />
        </div>
        <div class="eval-img-wrap no-caption" style="margin: 0;">
          <img src="2.png" alt="2048 game example" />
        </div>
      </div>

      <p>
        2048 is a solo player web game where the objective is to merge like tiles to eventually — hopefully — produce the 2048 tile. Each tile is a power of 2, and the player begins with twos and fours scattered across the board.
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="3.png" alt="2048 gameplay illustration" />
      </div>

      <div class="sub-heading">How to Play</div>
      <p>
        There are 4 possible moves a player can make on any given turn: <strong>up, down, left, right</strong>. After each move, the game adds a random tile (2 or 4) into a random empty cell. Each move slides all existing tiles in the chosen direction. Only when two like tiles — tiles of the same power of two — collide can they merge into one new tile of the next power of two; the two merged tiles disappear and are replaced by their combined value.
      </p>
    </div>
  </div>

  <!-- Progress States -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">02</div>
      <h2 class="section-title">Progress States</h2>
    </div>
    <div class="section-body">
      <div class="progress-grid">
        <div class="progress-card">
          <div class="progress-label">Past</div>
          <p>In the beginning of our project, we were only able to just barely get 1024 as the maximum tile. Most of our models were reaching 512.</p>
        </div>
        <div class="progress-card">
          <div class="progress-label">Present</div>
          <p>Presently, we have reached our goal of 2048 using two models — MCTS and PPO (CNN + MLP). All three of our models now consistently reach 1024.</p>
        </div>
        <div class="progress-card">
          <div class="progress-label">Future</div>
          <p>Our goal going forward is to reach 4096 (one power above 2048) and to have all three models, including DQN, reach 2048. We can also explore imitation learning or longer training runs on existing models.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Motivation -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">03</div>
      <h2 class="section-title">Motivation</h2>
    </div>
    <div class="section-body">
      <p>
        Our motivation for selecting this topic was that everyone on our team already knows how to play 2048. We believed the game had a straightforward success state, and that the action space could be simplified since there are only four possible moves. Lastly, we felt our own gameplay experience and general knowledge of the game allowed us to design better heuristics for reward shaping.
      </p>
      <p>
        In hindsight, we made some blunders in reward shaping early on — but after additional trials and iteration those were resolved successfully.
      </p>
    </div>
  </div>

  <!-- Problem Statement -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">04</div>
      <h2 class="section-title">Problem Statement</h2>
    </div>
    <div class="section-body">
      <p>
        The core challenge we found interesting is that 2048 is an <strong>inherently random game</strong>, making it difficult to learn — especially without heuristics to guide model decision making.
      </p>
      <p>
        2048 rewards delayed actions combined with a non-linear state space due to the collapsing of tiles column- and row-wise. Rewarding small movements instead of long-term gains causes tiles to be combined without any strict strategy, leading to small noisy movements that produce game-overs. Tile generation is also random — new tiles can appear anywhere on the board as either 2 or 4 — which means RL algorithms cannot rely on strictly deterministic patterns and must develop probabilistic strategies instead.
      </p>
      <p>
        The real goal is making long-term decisions that increase the mergeability of tiles, extending the reward horizon rather than chasing greedy local score increases. Humans make this same mistake when playing naively. We want models that can exploit strategies leading to good games despite an environment of randomness, non-linear state transitions, and long reward horizons.
      </p>
    </div>
  </div>

  <!-- DQN Approach -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">05</div>
      <h2 class="section-title">Approach — DQN</h2>
    </div>
    <div class="section-body">
      <p>
        One of the models we trained is a <strong>Deep Q-Network (DQN)</strong> using a Multilayer Perceptron policy. DQN takes in a 4×4 2D array representing the board state, where <strong>0 represents empty cells</strong> and positive integers represent the power of 2 occupying that cell — for example, a cell with value 3 represents 2³ = 8. This encoded array is passed to a hidden MLP network that learns patterns correlated with high rewards, then outputs a discrete action (0–3, corresponding to up, down, left, right) based on the estimated Q-value for each action.
      </p>
      <p>
        After making the selected move, the transition is stored in a <strong>replay buffer</strong>. During training, DQN samples randomly from this buffer and checks the resulting board state, receiving rewards for transitions that lead to a higher total score. This decouples the temporal order of experience from learning, reducing correlation between consecutive updates.
      </p>

      <div class="sub-heading">Loss Function</div>
      <div class="formula-block">L(θ) = E[(y − Q(s, a; θ))²]

where  y = r + γ · max_a' Q(s', a'; θ⁻)</div>
      <p>
        The target Q-value <strong>y</strong> is computed using a separate frozen target network (θ⁻), updated periodically. This stabilizes training by preventing the moving target problem inherent in naive Q-learning, where the network would otherwise chase a constantly shifting objective. Gradients are backpropagated through the loss to update the online network θ. This separate target network is why the loss function can appear unstable during training.
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="DQNLoss.png" alt="DQN loss curve" />
      </div>
      <p class="img-caption">DQN Loss Curve</p>

      <p>
        With the default DQN environment provided by stable_baselines3, the model does not learn to avoid illegal moves — moves where the board state does not change — and ultimately gets stuck repeating them indefinitely. Penalizing illegal moves was attempted, but the model still lacked persistent memory of <em>why</em> a specific move was illegal for a given board state. In the end, we wrapped the environment to train with an illegal move punishment and a corner reward, implementing the corner strategy.
      </p>

      <div class="sub-heading">Final Hyperparameters</div>
      <div class="hyperparam-grid">
        <div class="hyperparam-item"><span class="hyperparam-key">learning_rate</span><span class="hyperparam-val">1e-4</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">buffer_size</span><span class="hyperparam-val">100,000</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">learning_starts</span><span class="hyperparam-val">1,000</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">batch_size</span><span class="hyperparam-val">512</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">exploration_fraction</span><span class="hyperparam-val">0.3</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">total_timesteps</span><span class="hyperparam-val">10,000</span></div>
      </div>

      <p>
        Hyperparameters were not fully fine-tuned due to time constraints. On the hpc3 server without sbatch, training took much longer — sometimes hours — for performance ending in a maximum tile of 64. On the openlab server, training was substantially faster. With larger timesteps, buffer sizes, and batch sizes, training could result in maximum tiles of 100+, though it never reached 1000+. The final DQN implementation shows signs of successfully training with the corner strategy, but reward plateaus prevent it from reaching higher tiles.
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="DQNReward.png" alt="DQN reward curve" />
      </div>
      <p class="img-caption">DQN Reward Curve</p>

      <div class="eval-img-wrap no-caption">
        <img src="DQNMaxTiles.png" alt="DQN max tile over training" />
      </div>
      <p class="img-caption">DQN Max Tile Over Training</p>

      <p>
        In the future, we would want to increase or eliminate this reward plateau so the model can learn to reach higher maximum tiles. This could involve implementing more strategies, adjusting the exploration fraction to better account for 2048's inherent randomness, or using a stronger network architecture with additional layers and larger batch sizes.
      </p>
    </div>
  </div>

  <!-- MCTS Approach -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">06</div>
      <h2 class="section-title">Approach — MCTS</h2>
    </div>
    <div class="section-body">
      <p>
        Another algorithm we implemented is a heuristic-guided <strong>Monte Carlo Tree Search (MCTS)</strong> that performs <em>n</em> rollouts per move. Unlike PPO and DQN, MCTS does not learn a policy or a value function — it relies entirely on the tree built during search, aggregating rollout results to select moves at each decision point.
      </p>
      <p>
        At each decision point, MCTS expands nodes for different board states and performs rollouts. While traditional MCTS follows fully random rollouts, this naive approach does not account for two key issues: 2048's inherent randomness and its rapidly changing state space. Results from each rollout are backpropagated up through the tree to update node values, allowing the algorithm to estimate which action will yield the best outcome based on the <strong>Upper Confidence Bounds (UCB)</strong> formula:
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="4.png" alt="MCTS tree diagram" />
      </div>
      <p class="img-caption">Graphic via poomstas/2048_MCTS @ github</p>

      <div class="formula-block">UCB = exploitation_term + c · sqrt(ln(N) / n)

where  N = total visits to parent node
       n = visits to this child node
       c = exploration constant</div>

      <div class="eval-img-wrap no-caption">
        <img src="5.png" alt="UCB formula diagram" />
      </div>
      <p class="img-caption">Graphic via StackOverflow</p>

      <div class="sub-heading">Heuristics</div>
      <p>
        Random rollouts introduce significant noise — especially in a stochastic state space. We added heuristics to guide rollout selection so they follow strategies grounded in real 2048 gameplay:
      </p>
      <div class="design-grid">
        <div class="design-card">
          <span class="design-icon">01</span>
          <div class="design-content">
            <p class="design-title">Empty Tile Weighting</p>
            <p class="design-desc">Boards with more empty cells are rewarded. Any move can spawn an unmergeable tile anywhere on the board, so maintaining flexibility by keeping cells open increases future merge opportunities.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">02</span>
          <div class="design-content">
            <p class="design-title">Monotonicity Score</p>
            <p class="design-desc">Tiles are rewarded for following a snake-like ordering — consistently increasing or decreasing across rows and columns — enabling strategic chaining of merges in a single sweep.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">03</span>
          <div class="design-content">
            <p class="design-title">Corner Bias</p>
            <p class="design-desc">High-value tiles positioned in a corner receive a bonus. Corner anchoring enables cascading collapses by keeping the highest tile stationary while merging descending tiles around it.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">04</span>
          <div class="design-content">
            <p class="design-title">Smoothness</p>
            <p class="design-desc">Adjacent tiles with similar values are rewarded because they can be merged given the right opportunity. Smooth boards reduce the number of moves needed to collapse adjacent tiles.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">05</span>
          <div class="design-content">
            <p class="design-title">Exploration Constant c</p>
            <p class="design-desc">Controls the balance between exploitation of high-value nodes and exploration of less-visited ones in the UCB formula. Tuned experimentally against the other heuristic weights.</p>
          </div>
        </div>
      </div>

      <div class="sub-heading">Experimental Findings</div>
      <p>
        Based on these heuristics, we could then do experimental analysis to find the best combination of parameters:
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="6.png" alt="MCTS heuristic parameter grid search results" />
      </div>

      <div class="sub-heading">Rollout Parameters</div>
      <p>Three rollout parameters were tuned to balance performance against computational cost:</p>
      <div class="hyperparam-grid">
        <div class="hyperparam-item"><span class="hyperparam-key">Time per Move</span><span class="hyperparam-val">Budget (s)</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Num. Simulations</span><span class="hyperparam-val">n rollouts</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Rollout Depth</span><span class="hyperparam-val">max steps</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Heuristic weights</span><span class="hyperparam-val">tuned grid</span></div>
      </div>

      <div class="sub-heading">Results</div>
      <p>This ultimately results in the best combination of parameters which came out to be:</p>

      <div class="eval-img-wrap no-caption">
        <img src="7.png" alt="MCTS best parameter combination" />
      </div>

      <p>
        More rollouts and deeper rollout depth generally produce higher scores by giving the tree more information — but this directly increases time per game. Games that ran faster (less compute) scored lower because they reached game-over sooner, while slower games running around 8 minutes were able to reach the 2048 tile.
      </p>
      <p>When ran on our baseline of 20 games, we saw:</p>

      <div class="eval-img-wrap no-caption">
        <img src="8.png" alt="MCTS 20-game results 1" />
      </div>

      <div class="eval-img-wrap no-caption">
        <img src="9.png" alt="MCTS 20-game results 2" />
      </div>

      <div class="eval-img-wrap no-caption">
        <img src="10.png" alt="MCTS 20-game results 3" />
      </div>

      <div style="display: flex; justify-content: center; margin: 24px 0;">
        <div class="eval-img-wrap no-caption" style="width: 50%; margin: 0;">
          <img src="11.png" alt="MCTS 20-game results 4" />
        </div>
      </div>

      <div class="sub-heading">Key Insight</div>
      <div class="bug-card">
        <div class="bug-header">
          <span class="bug-tag insight">Insight</span>
          <span class="bug-title">Performance Scales with Compute</span>
        </div>
        <p class="bug-body">
          MCTS performance is directly tied to hardware speed. Machines with faster CPUs can run more simulations within the same time budget, producing stronger play. This means identical configurations yield different results across machines — beyond 2048's inherent randomness — and time-based limits are hardware-dependent. MCTS does not retain knowledge between games, making it much more expensive and less scalable than trained models. While it can perform comparably to a tuned RL model given sufficient compute, the runtime cost is substantially higher.
        </p>
      </div>
    </div>
  </div>

  <!-- PPO Approach -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">07</div>
      <h2 class="section-title">Approach — PPO (CNN + MLP)</h2>
    </div>
    <div class="section-body">
      <p>
        The PPO model uses a fully custom training loop with a <strong>CNN + MLP dual-path architecture</strong>. Unlike DQN's off-policy Q-value approach, PPO is an on-policy actor-critic method that directly optimizes a clipped surrogate objective, preventing destructively large policy updates while still making meaningful gradient steps each iteration.
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="12.png" alt="PPO CNN + MLP architecture diagram" />
      </div>

      <div class="sub-heading">Input Encoding</div>
      <p>
        The board is first <strong>log₂-encoded</strong>: each tile value t is mapped to log₂(t) / 17, compressing the range 2–131072 into a uniform [0, 1] scale. Raw tile values span five orders of magnitude, making them poor direct inputs. Log₂ encoding gives both the convolutional and flat MLP paths equally scaled features to work with.
      </p>

      <div class="sub-heading">Network Architecture</div>
      <p>
        The encoded board is processed by two parallel paths:
      </p>
      <div class="hyperparam-grid" style="margin-bottom: 20px;">
        <div class="hyperparam-item"><span class="hyperparam-key">Spatial path (Conv2d)</span><span class="hyperparam-val">1→64→128→128 channels</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Flat path (MLP)</span><span class="hyperparam-val">16→256→256</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Combined head</span><span class="hyperparam-val">1408→512→256→4</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">Value head output</span><span class="hyperparam-val">1408→512→256→1</span></div>
      </div>
      <p>
        The convolutional path sees the board spatially as a (1, 4, 4) image, learning positional tile relationships: corner anchoring, adjacency for merging, diagonal arrangements. The flat MLP path treats the board as a vector of 16 numbers — every cell talks to every other equally, regardless of position — providing global context over tile distribution. Their outputs are concatenated and passed to separate policy and value heads.
      </p>

      <div class="sub-heading">Actor-Critic (PPO)</div>
      <p>
        PPO is an actor-critic framework. The <strong>actor</strong> is the policy π(a|s) that looks at the current board state and decides which of the four actions to take. The <strong>critic</strong> is the value function V(s) — it looks at the board and produces a score quantifying how good the current state actually is. The critic never takes actions; it only judges the actor.
      </p>
      <p>
        A critical problem in policy gradient methods is that overly aggressive updates can erase all previously learned strategies. PPO counters this using the ratio between the new and old policy:
      </p>
      <div class="formula-block">r(θ) = π_θ(a|s) / π_θ_old(a|s)   =   exp(log π_θ(a|s) − log π_θ_old(a|s))

L_CLIP = E[ min(r(θ) · Â,  clip(r(θ), 1−ε, 1+ε) · Â) ]   where ε = 0.2

L_policy = −L_CLIP − 0.02 · H[π_θ]</div>
      <p>
        The entropy bonus <strong>H[π_θ]</strong> (coefficient 0.02) discourages premature convergence to a deterministic policy, keeping the agent exploring alternative move sequences throughout training. The value loss is computed separately:
      </p>
      <div class="formula-block">L_value = 0.5 · E[ (Rᵢ − V_φ(sᵢ))² ]</div>

      <div class="sub-heading">Generalized Advantage Estimation (GAE)</div>
      <p>
        Rather than using raw returns or single-step TD errors, advantages are computed via GAE with γ = 0.997 and λ = 0.95. Starting from the last step in the rollout buffer and working backwards:
      </p>
      <div class="formula-block">δᵢ    = rᵢ + γ · V(sᵢ₊₁) · (1 − doneᵢ) − V(sᵢ)
Âᵢ    = δᵢ + γλ · (1 − doneᵢ) · Âᵢ₊₁
Rᵢ    = Âᵢ + V(sᵢ)         [returns for value loss]</div>
      <p>
        δᵢ is the one-step TD error. GAE exponentially discounts future TD errors, controlled by λ: λ = 0 reduces to pure TD (low variance, high bias), λ = 1 reduces to full Monte Carlo (high variance, low bias). λ = 0.95 sits close to the Monte Carlo end, capturing long multi-step merge sequences without excessive variance. Advantages are then normalized across the batch: Â ← (Â − mean(Â)) / (std(Â) + ε).
      </p>

      <div class="sub-heading">Adam Optimizers</div>
      <p>
        The actor and critic use independent Adam optimizers with separate learning rates. Adam provides two key improvements over basic gradient descent:
      </p>
      <div class="formula-block">m = β₁·m + (1-β₁)·g          # running mean of gradient
v = β₂·v + (1-β₂)·g²         # running mean of squared gradient
w = w - α · m / (√v + ε)      # weight update</div>
      <p>
        <strong>Momentum:</strong> instead of using only the current gradient, Adam maintains a running average of past gradients, smoothing noisy updates. If the model has historically pointed in a given direction, it takes a larger step that way. <strong>Adaptive learning rates:</strong> each parameter receives its own effective learning rate — parameters with consistently large gradients are scaled down, small gradients are scaled up. The m/√v term is what makes learning adaptive.
      </p>
      <p>
        Using separate optimizers means the critic (value_lr = 5e-4) and actor (policy_lr = 1e-4) can move at different speeds. In practice, the critic converges earlier, supplying better advantage signals to the actor sooner — our model reached 2048 at around 50k episodes.
      </p>

      <div class="sub-heading">Reward Function</div>
      <p>The shaped reward for each step combines four components:</p>
      <div class="formula-block">r = log₂(merge_score + 1)
  + 0.30 · log₂(max_tile + 1)   [if max_tile is in a corner]
  + 0.10 · empty_cells
  − 0.05 · monotonicity_penalty</div>
      <p>
        The base term <strong>log₂(merge_score + 1)</strong> is scale-invariant — merging two 512 tiles (score 1024) yields log₂(1025) ≈ 10, while merging two 2 tiles (score 4) yields log₂(5) ≈ 2.3, a proportional difference rather than a 256× raw difference. The monotonicity penalty accumulates log₂ differences across adjacent tile pairs that violate ascending order in any row or column:
      </p>
      <div class="formula-block">mono = Σ_{rows} Σ_{j} max(0, log₂(row[j]) − log₂(row[j+1]))
     + Σ_{cols} Σ_{i} max(0, log₂(col[i]) − log₂(col[i+1]))</div>

      <div class="sub-heading">Hyperparameters</div>
      <div class="hyperparam-grid">
        <div class="hyperparam-item"><span class="hyperparam-key">γ (discount)</span><span class="hyperparam-val">0.997</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">λ (GAE)</span><span class="hyperparam-val">0.95</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">ε (clip)</span><span class="hyperparam-val">0.2</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">policy_lr</span><span class="hyperparam-val">1e-4</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">value_lr</span><span class="hyperparam-val">5e-4</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">ppo_epochs</span><span class="hyperparam-val">8</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">mini_batch</span><span class="hyperparam-val">512</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">rollout_steps</span><span class="hyperparam-val">4096</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">entropy_coef</span><span class="hyperparam-val">0.02</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">value_coef</span><span class="hyperparam-val">0.5</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">max_grad_norm</span><span class="hyperparam-val">0.5</span></div>
        <div class="hyperparam-item"><span class="hyperparam-key">LR schedule</span><span class="hyperparam-val">Cosine (T₀=2M)</span></div>
      </div>

      <div class="sub-heading">Key Design Choices</div>
      <div class="design-grid">
        <div class="design-card">
          <span class="design-icon">01</span>
          <div class="design-content">
            <p class="design-title">Log₂-Encoded Board → CNN + MLP Dual-Path Network</p>
            <p class="design-desc">Raw tile values span five orders of magnitude (2–131072), making them poor direct inputs. Log₂ encoding compresses this to a uniform 1–17 range, giving both paths equally scaled features to work with.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">02</span>
          <div class="design-content">
            <p class="design-title">Reward = log₂(merge_score + 1)</p>
            <p class="design-desc">Using raw merge scores creates extremely high-variance signal — merging a 1024 tile gives 500× more reward than merging a 2 tile. Log₂ transformation keeps the signal bounded and consistent across all tile magnitudes.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">03</span>
          <div class="design-content">
            <p class="design-title">Corner Placement Bonus</p>
            <p class="design-desc">The agent receives +0.30 · log₂(max_tile + 1) when the maximum tile occupies any corner. Corner anchoring enables cascading collapses — a sequence of moves that merges multiple descending tiles in one sweep without displacing the highest tile.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">04</span>
          <div class="design-content">
            <p class="design-title">Monotonicity Penalty</p>
            <p class="design-desc">Penalizes moves that produce non-monotonic tile arrangements by accumulating log₂ differences across all adjacent pairs that violate ascending order. Monotonic rows and columns make multi-tile chain merges possible in a single move.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">05</span>
          <div class="design-content">
            <p class="design-title">Empty Cell Bonus (+0.10 per cell)</p>
            <p class="design-desc">A bonus per empty cell discourages filling the board prematurely. As empty cells decrease, legal moves decrease, accelerating game-over. This term keeps the agent seeking merge opportunities rather than spreading tiles.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">06</span>
          <div class="design-content">
            <p class="design-title">GAE (γ=0.997, λ=0.95)</p>
            <p class="design-desc">High γ (0.997) values future rewards heavily — critical for 2048 where the payoff of a strategic merge may not materialize for dozens of moves. λ=0.95 keeps advantage estimates close to Monte Carlo, capturing long multi-step merge sequences without excessive variance.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">07</span>
          <div class="design-content">
            <p class="design-title">Large Rollout Buffer (4096 steps)</p>
            <p class="design-desc">4096 steps spans multiple complete games, ensuring each policy update sees diverse board configurations — both early-game open boards and late-game crowded states. This prevents gradient updates from overfitting to any single game trajectory.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">08</span>
          <div class="design-content">
            <p class="design-title">Mini-Batch PPO (8 epochs, batch 512)</p>
            <p class="design-desc">The 4096-step buffer is shuffled and split into 512-sample mini-batches, updated for 8 epochs per rollout. The ε=0.2 clip limits the probability ratio r(θ) to [0.8, 1.2], preventing any single update from overshooting into a bad policy region.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">09</span>
          <div class="design-content">
            <p class="design-title">Separate Adam Optimizers + Cosine LR</p>
            <p class="design-desc">Policy (lr=1e-4) and value (lr=5e-4) networks use independent Adam optimizers. Cosine annealing with warm restarts (T₀=2M steps) progressively reduces both rates while periodically resetting to escape local minima.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">10</span>
          <div class="design-content">
            <p class="design-title">Gradient Clipping (max_norm=0.5)</p>
            <p class="design-desc">Applied after each backward pass via torch.nn.utils.clip_grad_norm_. Without clipping, rare high-reward merges produce gradient spikes that can catastrophically overwrite previously learned strategies in a single step.</p>
          </div>
        </div>
        <div class="design-card">
          <span class="design-icon">11</span>
          <div class="design-content">
            <p class="design-title">Two Saved Checkpoints</p>
            <p class="design-desc">The <em>latest</em> checkpoint saves every 500 episodes and on every new best tile. The <em>best-average</em> checkpoint saves only when the 100-episode rolling mean improves by more than 1%, preventing frequent overwrites from lucky individual games.</p>
          </div>
        </div>
      </div>

      <div class="sub-heading">Issues &amp; Fixes During Training</div>
      <div class="bug-list">
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag issue">Issue</span>
            <span class="bug-title">Illegal Moves — Board Never Changes</span>
          </div>
          <p class="bug-body">In the beginning, the model never made any valid moves. With the GUI it was immediately obvious because the board would never change even as the move counter incremented.</p>
          <div class="bug-fix">
            <span class="bug-tag fix">Fix</span>
            <p>The environment was modified to strictly filter actions — only moves that result in a board state change are permitted. The action selection layer masks illegal moves before sampling.</p>
          </div>
        </div>
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag issue">Issue</span>
            <span class="bug-title">Cyclic Move Pattern — LEFT → DOWN → RIGHT → UP Loop</span>
          </div>
          <p class="bug-body">Using imitation training in early iterations, the model converged on a deterministic ring pattern: LEFT, DOWN, RIGHT, UP, repeating until the board was full.</p>
          <div class="bug-fix">
            <span class="bug-tag fix">Fix</span>
            <p>The learning rate was increased to give the optimizer enough momentum to escape this local minimum, and the CNN + MLP dual-path architecture replaced the flat MLP, enabling spatial awareness that disrupted the cyclic attractor.</p>
          </div>
        </div>
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag issue">Issue</span>
            <span class="bug-title">Diagonal Tiles — Mergeable Tiles Unable to Merge</span>
          </div>
          <p class="bug-body">Mergeable tiles were unable to merge because their positions were diagonally opposite. With only a flat MLP there was no spatial awareness to recognize and resolve diagonal separation.</p>
          <div class="bug-fix">
            <span class="bug-tag fix">Fix</span>
            <p>Adding the empty tiles heuristic combined with introducing the MLP path alongside the CNN resolved this. Training had to restart from scratch.</p>
          </div>
        </div>
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag issue">Issue</span>
            <span class="bug-title">Failed Reward — Overly Lucrative High-Tile Bonus</span>
          </div>
          <p class="bug-body">One reward for high tiles in general was made too lucrative. The actor went on a merging spree and produced many "holes" — isolated low-power tiles trapped among high tiles — breaking monotonicity and fragmenting the board.</p>
          <div class="bug-fix">
            <span class="bug-tag fix">Fix</span>
            <p>The reward coefficient was reduced and replaced with the more targeted corner placement bonus, which rewards high tiles only when they occupy a corner rather than anywhere on the board.</p>
          </div>
        </div>
      </div>

      <div class="sub-heading">Results</div>
      <div class="stat-row">
        <div class="stat">
          <span class="stat-value">10%</span>
          <span class="stat-label">2048 Rate (20 games)</span>
        </div>
        <div class="stat">
          <span class="stat-value">1024</span>
          <span class="stat-label">Avg Max Tile</span>
        </div>
        <div class="stat">
          <span class="stat-value">512</span>
          <span class="stat-label">Min Max Tile</span>
        </div>
        <div class="stat">
          <span class="stat-value">~1.5s</span>
          <span class="stat-label">Avg Time / Game</span>
        </div>
      </div>
      <p>
        10% of results from a 20-game test end with a max tile of 2048. The average max tile across all 20 games is 1024, and the lowest max tile recorded is 512. Average time per game is approximately 1.5 seconds — at maximum, 3 seconds. This model was trained to approximately 23 million steps. Total testing time for all 20 games is under 30 seconds.
      </p>

      <div class="eval-img-wrap no-caption">
        <img src="13.png" alt="PPO results — 3 graphs" />
      </div>

      <div style="display: flex; justify-content: center; margin: 24px 0;">
        <div class="eval-img-wrap no-caption" style="width: 50%; margin: 0;">
          <img src="14.png" alt="PPO results 2" />
        </div>
      </div>
    </div>
  </div>

  <!-- Evaluation -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">08</div>
      <h2 class="section-title">Evaluation &amp; Discussion</h2>
    </div>
    <div class="section-body">
      <p>
        The two primary evaluation metrics are <strong>total score</strong> (sum of all merge values across the game, matching standard 2048 scoring) and <strong>maximum tile reached</strong>. These objectively capture both the quantity of merges and their quality.
      </p>

      <div class="sub-heading">Model Comparison</div>
      <table class="compare-table">
        <thead>
          <tr>
            <th>Model</th>
            <th>2048 Rate</th>
            <th>Avg Max Tile</th>
            <th>Avg Time / Game</th>
            <th>Learns Between Games</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>PPO (CNN + MLP)</td>
            <td>10% (20-game test)</td>
            <td>1024</td>
            <td>~1.5s</td>
            <td>Yes — trained weights</td>
          </tr>
          <tr>
            <td>MCTS (heuristic)</td>
            <td>Reaches 2048 w/ sufficient compute</td>
            <td>Variable by hardware</td>
            <td>Minutes per game</td>
            <td>No — search from scratch</td>
          </tr>
          <tr>
            <td>DQN (MLP)</td>
            <td>Not yet</td>
            <td>~64–100+</td>
            <td>Fast</td>
            <td>Yes — trained weights</td>
          </tr>
        </tbody>
      </table>

      <div class="sub-heading">Insights</div>
      <div class="bug-list">
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag insight">Insight</span>
            <span class="bug-title">Score and Max Tile are Directly Correlated</span>
          </div>
          <p class="bug-body">
            There is a clear direct correlation between max tile reached and total score across all three models. The main outlier is the time required per game — MCTS is the primary concern when comparing time vs. score, while PPO and DQN can be rapidly evaluated. This is inherent to MCTS's architecture of performing n rollouts per move.
          </p>
        </div>
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag insight">Insight</span>
            <span class="bug-title">PPO is the Best Overall Model</span>
          </div>
          <p class="bug-body">
            There is a clear tradeoff between time and score when comparing MCTS to PPO. While MCTS achieves higher 2048 rates with sufficient compute, PPO is more stable — its 1024 and 512 rates are higher than MCTS's across equivalent test runs. PPO's robust design choices and carefully tuned heuristics make it the strongest model overall: it reaches 2048 at a reasonable training cost (50k episodes) and evaluates in approximately 1.5 seconds per game.
          </p>
        </div>
        <div class="bug-card">
          <div class="bug-header">
            <span class="bug-tag insight">Insight</span>
            <span class="bug-title">DQN Has Room to Grow</span>
          </div>
          <p class="bug-body">
            With further research into DQN parameterization and longer training times, we believe there is more to be achieved. DQN's reward plateau currently prevents it from reaching higher tiles, but with more compute and stronger architecture choices (additional layers, larger batch sizes, more timesteps), it could close the gap. More broadly, we can explore imitation learning with additional data, or train existing models on modified 2048 variants — such as including 8 as a randomly spawning tile, using a larger board, or adding move timers — to encourage adaptability.
          </p>
        </div>
      </div>

      <div class="eval-img-wrap no-caption">
        <img src="15.png" alt="Evaluation comparison 1" />
      </div>

      <div class="eval-img-wrap no-caption">
        <img src="16.png" alt="Evaluation comparison 2" />
      </div>

      <div class="eval-img-wrap no-caption">
        <img src="17.png" alt="Evaluation comparison 3" />
      </div>

      <div style="display: flex; justify-content: center; margin: 24px 0;">
        <div class="eval-img-wrap no-caption" style="width: 50%; margin: 0;">
          <img src="18.png" alt="Final evaluation summary" />
        </div>
      </div>
    </div>
  </div>

  <!-- Resources -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">09</div>
      <h2 class="section-title">Resources Used</h2>
    </div>
    <div class="section-body">
      <div class="refs-list">
        <a href="https://github.com/Quentin18/gymnasium-2048/blob/main/README.md" class="ref-item" target="_blank">
          <span class="ref-name">2048 GitHub Repository</span>
          <span class="ref-url">github.com/Quentin18/gymnasium-2048</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://stable-baselines3.readthedocs.io/en/master/modules/dqn.html" class="ref-item" target="_blank">
          <span class="ref-name">Stable Baselines3 DQN</span>
          <span class="ref-url">stable-baselines3.readthedocs.io</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://arxiv.org/pdf/1312.5602" class="ref-item" target="_blank">
          <span class="ref-name">DeepMind DQN Paper</span>
          <span class="ref-url">arxiv.org/pdf/1312.5602</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://arxiv.org/html/2507.05465v1" class="ref-item" target="_blank">
          <span class="ref-name">Stanford 2048 Paper</span>
          <span class="ref-url">arxiv.org/html/2507.05465v1</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://medium.com/data-science/a-puzzle-for-ai-eb7a3cb8e599" class="ref-item" target="_blank">
          <span class="ref-name">Medium — A Puzzle for AI</span>
          <span class="ref-url">medium.com/data-science</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://royf.org/crs/CS175/W26/CS175L2.pdf" class="ref-item" target="_blank">
          <span class="ref-name">CS175 Slides</span>
          <span class="ref-url">royf.org/crs/CS175/W26</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://github.com/poomstas/2048_MCTS" class="ref-item" target="_blank">
          <span class="ref-name">MCTS Graphic — poomstas/2048_MCTS</span>
          <span class="ref-url">github.com/poomstas/2048_MCTS</span>
          <span class="ref-arrow">↗</span>
        </a>
        <a href="https://stackoverflow.com" class="ref-item" target="_blank">
          <span class="ref-name">MCTS UCB Graphic — StackOverflow</span>
          <span class="ref-url">stackoverflow.com</span>
          <span class="ref-arrow">↗</span>
        </a>
      </div>
    </div>
  </div>

  <!-- AI Disclaimer -->
  <div class="section">
    <div class="section-meta">
      <div class="section-num">10</div>
      <h2 class="section-title">AI Disclaimer</h2>
    </div>
    <div class="section-body">
      <p>AI tooling was used in the following capacities:</p>
      <div class="ai-tags" style="margin-top: 16px;">
        <div class="ai-tag-item">Integrate libraries and dependencies</div>
        <div class="ai-tag-item">Create frontend design for GitHub Pages</div>
        <div class="ai-tag-item">Create GUI for 2048 games</div>
        <div class="ai-tag-item">Supplement personal learning of RL models</div>
      </div>
    </div>
  </div>

</div>

<div class="doc-nav">
  <a href="status.html">← Status Report</a>
  <span class="doc-nav-center">PowerOf2 · CS 175</span>
  <a href="index.html">Home →</a>
</div>
