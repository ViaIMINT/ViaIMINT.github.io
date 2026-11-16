<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>四國高松親子自駕慢遊手帖 2026</title>
  
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="default">
  <meta name="apple-mobile-web-app-title" content="四國慢遊">
  
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Zen+Maru+Gothic:wght@400;500;700;900&display=swap" rel="stylesheet">
  
  <style>
    :root {
      --bg-main: #FBF8F2;
      --bg-card: #FFFFFF;
      --border-color: #4A3E39;
      --border-light: #E8DFD5;
      --text-main: #3E342F;
      --text-muted: #82756E;
      --c-brown: #7C6053;
      --c-brown-light: #F4EBE3;
      --c-coral: #E68574;
      --c-coral-light: #FDF1EE;
      --c-yellow: #E8BE65;
      --c-yellow-light: #FCF6E8;
      --c-blue: #8AB8CD;
      --c-blue-light: #EFF6FA;
      --c-green: #9EBE88;
      --c-green-light: #F3F8EE;
      --nav-bg: #FFFFFF;
      --card-radius: 20px;
      --pill-radius: 12px;
      --border-w: 2.5px;
    }

    [data-theme="dark"] {
      --bg-main: #252321;
      --bg-card: #3A3531;
      --border-color: #8C7D73;
      --border-light: #524B45;
      --text-main: #F7F1E9;
      --text-muted: #C0B4AB;
      --c-brown: #C49F8C;
      --c-brown-light: #443C36;
      --c-coral: #E29587;
      --c-coral-light: #483A36;
      --c-yellow: #D8B262;
      --c-yellow-light: #453F32;
      --c-blue: #93B8C7;
      --c-blue-light: #343E44;
      --c-green: #A3BF90;
      --c-green-light: #374133;
      --nav-bg: #2E2926;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      font-family: 'Zen Maru Gothic', sans-serif, system-ui;
      background-color: var(--bg-main);
      color: var(--text-main);
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      transition: background-color 0.3s ease, color 0.3s ease;
      padding-top: 74px;
      padding-bottom: 40px;
    }

    header.top-nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      height: 70px;
      background-color: var(--nav-bg);
      border-bottom: var(--border-w) solid var(--border-color);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0 16px;
      transition: background-color 0.3s;
    }

    .brand-title {
      display: flex;
      align-items: center;
      gap: 8px;
      font-weight: 900;
      font-size: 1.15rem;
      color: var(--text-main);
      cursor: pointer;
      flex-shrink: 0;
    }

    .nav-scroll-wrap {
      display: flex;
      align-items: center;
      overflow-x: auto;
      gap: 6px;
      padding: 4px 6px;
      scrollbar-width: none;
    }
    .nav-scroll-wrap::-webkit-scrollbar { display: none; }

    .nav-btn {
      background: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      color: var(--text-main);
      border-radius: 999px;
      padding: 6px 14px;
      font-size: 0.86rem;
      font-weight: 700;
      white-space: nowrap;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 5px;
      transition: all 0.2s ease;
      font-family: inherit;
    }

    .nav-btn.active {
      background-color: var(--c-yellow);
      transform: translateY(-2px);
      box-shadow: 0 3px 0 var(--border-color);
    }

    .theme-toggle-btn {
      background: var(--c-coral-light);
      border: var(--border-w) solid var(--border-color);
      color: var(--text-main);
      width: 42px;
      height: 42px;
      border-radius: 50%;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      margin-left: 6px;
      font-size: 1.1rem;
    }

    main.container {
      max-width: 640px;
      width: 100%;
      margin: 0 auto;
      padding: 16px;
      flex: 1;
    }

    .tab-content {
      display: none;
      animation: fadeIn 0.25s ease forwards;
    }
    .tab-content.active { display: block; }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(5px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .top-notice-bubble {
      background: var(--c-brown-light);
      border: 2px solid var(--border-color);
      border-radius: 18px;
      padding: 12px 16px;
      font-size: 0.9rem;
      font-weight: 700;
      margin-bottom: 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .app-nav-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-bottom: 20px;
    }

    .app-nav-card {
      background: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      border-radius: 18px;
      padding: 14px 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      font-size: 0.98rem;
      font-weight: 800;
      cursor: pointer;
      box-shadow: 0 4px 0 var(--border-color);
      transition: all 0.15s ease;
      color: var(--text-main);
    }
    .app-nav-card:active {
      transform: translateY(2px);
      box-shadow: 0 2px 0 var(--border-color);
    }
    .app-nav-card.active-tab {
      background-color: var(--c-brown);
      color: #FFFFFF;
      box-shadow: 0 4px 0 rgba(0,0,0,0.25);
    }

    .day-selector-scroll {
      display: flex;
      gap: 10px;
      overflow-x: auto;
      padding: 4px 2px 14px 2px;
      scrollbar-width: none;
    }
    .day-selector-scroll::-webkit-scrollbar { display: none; }

    .day-selector-card {
      min-width: 90px;
      background: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      border-radius: 16px;
      padding: 10px 8px;
      text-align: center;
      cursor: pointer;
      box-shadow: 0 3px 0 var(--border-color);
      transition: all 0.2s ease;
      flex-shrink: 0;
    }
    .day-selector-card .d-name {
      font-size: 0.98rem;
      font-weight: 900;
    }
    .day-selector-card .d-date {
      font-size: 0.76rem;
      font-weight: 700;
      color: var(--text-muted);
      margin-top: 2px;
    }
    .day-selector-card.active {
      background-color: var(--c-brown);
      color: #FFFFFF;
      transform: translateY(-2px);
      box-shadow: 0 4px 0 var(--border-color);
    }
    .day-selector-card.active .d-date {
      color: #E6D7CD;
    }

    .day-header-bar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin: 10px 0 16px 0;
    }
    .day-header-title {
      font-size: 1.15rem;
      font-weight: 900;
      letter-spacing: -0.3px;
    }
    .btn-add-schedule {
      background: var(--c-brown);
      color: #FFFFFF;
      border: 2px solid var(--border-color);
      border-radius: 12px;
      padding: 6px 14px;
      font-size: 0.85rem;
      font-weight: 800;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 4px;
      box-shadow: 0 3px 0 var(--border-color);
      font-family: inherit;
    }
    .btn-add-schedule:active {
      transform: translateY(2px);
      box-shadow: 0 1px 0 var(--border-color);
    }

    .timeline-stream {
      position: relative;
      padding-left: 20px;
    }
    .timeline-stream::before {
      content: '';
      position: absolute;
      left: 7px;
      top: 14px;
      bottom: 24px;
      width: 4px;
      background-color: #E2D6CA;
      border-radius: 2px;
    }
    [data-theme="dark"] .timeline-stream::before {
      background-color: #554D47;
    }

    .timeline-row {
      position: relative;
      margin-bottom: 16px;
      padding-left: 14px;
    }

    .timeline-dot {
      position: absolute;
      left: -20px;
      top: 18px;
      width: 14px;
      height: 14px;
      border-radius: 50%;
      background-color: #C29E88;
      border: 3px solid var(--bg-main);
      z-index: 2;
    }

    .schedule-white-card {
      background-color: var(--bg-card);
      border: 2px solid var(--border-light);
      border-radius: 20px;
      padding: 14px 16px;
      box-shadow: 0 3px 6px rgba(0, 0, 0, 0.04);
      position: relative;
      transition: all 0.2s ease;
    }
    [data-theme="dark"] .schedule-white-card {
      border-color: var(--border-color);
    }

    .card-top-header {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 8px;
    }

    .time-badge {
      background: #F3EAE1;
      color: #6C483B;
      font-size: 0.95rem;
      font-weight: 900;
      padding: 4px 10px;
      border-radius: 10px;
      letter-spacing: 0.5px;
    }
    [data-theme="dark"] .time-badge {
      background: #4A3E38;
      color: #E5BEAF;
    }

    .spot-name {
      font-size: 1.05rem;
      font-weight: 800;
      color: var(--text-main);
      flex: 1;
    }

    .tag-bubble {
      background: #F7EFE8;
      color: #8C6A5A;
      font-size: 0.72rem;
      font-weight: 800;
      padding: 2px 8px;
      border-radius: 8px;
    }
    [data-theme="dark"] .tag-bubble {
      background: #4E443F;
      color: #D3B9AC;
    }

    .card-detail-memo {
      font-size: 0.85rem;
      color: var(--text-muted);
      margin-bottom: 12px;
      line-height: 1.45;
      padding-left: 2px;
    }

    .card-actions-bar {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .action-sub-pill {
      background: #F8F4EE;
      border: 1.5px solid #E4D9CE;
      color: var(--text-main);
      padding: 6px 12px;
      border-radius: 12px;
      font-size: 0.82rem;
      font-weight: 700;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 5px;
      cursor: pointer;
      transition: all 0.15s ease;
      font-family: inherit;
    }
    [data-theme="dark"] .action-sub-pill {
      background: #433D38;
      border-color: #615750;
    }
    .action-sub-pill:active {
      transform: scale(0.96);
      background: var(--c-yellow-light);
    }

    .book-card {
      background-color: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      border-radius: var(--card-radius);
      padding: 18px;
      margin-bottom: 18px;
      box-shadow: 3px 4px 0px var(--border-color);
    }
    .book-card.coral { border-top: 8px solid var(--c-coral); }
    .book-card.yellow { border-top: 8px solid var(--c-yellow); }
    .book-card.blue { border-top: 8px solid var(--c-blue); }
    .book-card.green { border-top: 8px solid var(--c-green); }

    .card-title {
      font-size: 1.15rem;
      font-weight: 900;
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 10px;
    }

    .badge {
      display: inline-block;
      padding: 3px 10px;
      border-radius: 999px;
      font-size: 0.72rem;
      font-weight: 800;
      border: 2px solid var(--border-color);
      background-color: var(--c-yellow);
      color: #3E342F;
    }

    .btn-action {
      background-color: var(--c-yellow);
      border: var(--border-w) solid var(--border-color);
      color: #3E342F;
      font-weight: 800;
      font-family: inherit;
      padding: 10px 18px;
      border-radius: 14px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      box-shadow: 2px 3px 0 var(--border-color);
      text-decoration: none;
      font-size: 0.9rem;
    }
    .btn-action.coral { background-color: var(--c-coral); color: #FFF; }
    .btn-action.blue { background-color: var(--c-blue); color: #3E342F; }
    .btn-action.green { background-color: var(--c-green); color: #3E342F; }

    .input-field {
      width: 100%;
      padding: 10px 14px;
      border: 2px solid var(--border-color);
      border-radius: 12px;
      background-color: var(--bg-main);
      color: var(--text-main);
      font-family: inherit;
      font-size: 0.95rem;
      margin-bottom: 12px;
      outline: none;
    }

    .list-item-box {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 12px 14px;
      border: 2px solid var(--border-color);
      border-radius: 14px;
      margin-bottom: 10px;
      background-color: var(--bg-main);
      gap: 10px;
    }
    .todo-checkbox { width: 20px; height: 20px; accent-color: var(--c-green); cursor: pointer; }
    .todo-done { text-decoration: line-through; color: var(--text-muted); opacity: 0.6; }
    .btn-icon { background: none; border: none; cursor: pointer; font-size: 1.1rem; padding: 4px; }
    .btn-edit { color: var(--c-blue); }
    .btn-delete { color: var(--c-coral); }

    .stat-banner {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
      margin-bottom: 18px;
    }
    .stat-card {
      background: var(--c-blue-light);
      border: 2px solid var(--border-color);
      border-radius: 16px;
      padding: 12px;
      text-align: center;
      box-shadow: 2px 3px 0 var(--border-color);
    }
    .stat-num { font-size: 1.35rem; font-weight: 900; color: var(--text-main); }
    .stat-label { font-size: 0.78rem; font-weight: 800; color: var(--text-muted); }

    .day-summary {
      background: var(--c-blue-light);
      border: 2px solid var(--border-color);
      border-radius: 14px;
      padding: 10px 14px;
      font-size: 0.84rem;
      font-weight: 700;
      line-height: 1.5;
      margin-bottom: 16px;
    }
    .drive-chip {
      display: inline-block;
      font-size: 0.74rem;
      font-weight: 800;
      color: var(--c-brown);
      background: var(--c-brown-light);
      border-radius: 8px;
      padding: 1px 8px;
      margin-bottom: 6px;
    }
    .notes-box {
      background: var(--c-yellow-light);
      border-left: 5px solid var(--c-yellow);
      border-radius: 10px;
      padding: 8px 12px;
      margin-bottom: 12px;
      font-size: 0.82rem;
      line-height: 1.5;
    }
    .notes-title { font-weight: 900; margin-bottom: 2px; }
    .notes-box ul { padding-left: 18px; }
    .notes-box li { margin-bottom: 2px; }
    .check-list { padding-left: 18px; font-size: 0.88rem; line-height: 1.7; }

    .mini-label { font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px; }
    .shop-card {
      background: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      border-radius: var(--card-radius);
      margin-bottom: 18px;
      box-shadow: 3px 4px 0 var(--border-color);
      overflow: hidden;
    }
    .shop-head {
      display: flex; align-items: center; gap: 12px;
      padding: 12px 14px; cursor: pointer;
    }
    .shop-logo {
      width: 46px; height: 46px; flex-shrink: 0;
      border: 2px solid var(--border-color); border-radius: 14px;
      background: var(--c-brown-light);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.3rem; font-weight: 900;
    }
    .shop-title-wrap { flex: 1; min-width: 0; }
    .shop-name { font-size: 1.08rem; font-weight: 900; }
    .shop-sub { font-size: 0.78rem; color: var(--text-muted); font-weight: 700; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
    .shop-progress {
      background: var(--c-yellow-light); border: 2px solid var(--border-color);
      border-radius: 999px; padding: 2px 12px; font-size: 0.85rem; font-weight: 900; flex-shrink: 0;
    }
    .shop-arrow { font-size: 1rem; flex-shrink: 0; transition: transform 0.2s; }
    .shop-card.collapsed .shop-arrow { transform: rotate(180deg); }
    .shop-card.collapsed .shop-body { display: none; }
    .shop-body { border-top: var(--border-w) solid var(--border-color); }
    .shop-intro { background: var(--c-blue-light); padding: 12px 14px; }
    .shop-tip { font-size: 0.85rem; font-weight: 700; margin-bottom: 10px; }
    .shop-tip::before { content: '● '; color: var(--c-coral); }
    .shop-btn-row { display: flex; gap: 8px; flex-wrap: wrap; }
    .shop-btn {
      flex: 1; min-width: 110px; justify-content: center;
      background: var(--bg-card); border: var(--border-w) solid var(--border-color);
      border-radius: 14px; padding: 8px 10px; font-size: 0.85rem; font-weight: 800;
      color: var(--text-main); text-decoration: none; cursor: pointer; font-family: inherit;
      display: inline-flex; align-items: center; gap: 6px; box-shadow: 2px 3px 0 var(--border-color);
    }
    .shop-btn.blue { background: var(--c-blue); color: #3E342F; }
    .shop-btn:active { transform: translateY(2px); box-shadow: 0 1px 0 var(--border-color); }
    .shop-cat {
      display: flex; align-items: center; gap: 8px; padding: 10px 14px 2px;
      font-weight: 800; font-size: 0.9rem; color: var(--text-muted); border-top: 2px dashed var(--border-light);
    }
    .shop-cat i { width: 16px; height: 16px; border-radius: 5px; background: var(--c-yellow); border: 2px solid var(--border-color); display: inline-block; }
    .shop-item { display: flex; gap: 10px; padding: 12px 14px; align-items: flex-start; border-top: 2px dashed var(--border-light); }
    .shop-item:first-of-type { border-top: none; }
    .shop-cb { width: 24px; height: 24px; accent-color: var(--c-green); cursor: pointer; margin-top: 4px; flex-shrink: 0; }
    .shop-img {
      width: 72px; height: 72px; border-radius: 14px; border: 2px solid var(--border-color);
      object-fit: cover; flex-shrink: 0; background: var(--c-brown-light);
      display: flex; align-items: center; justify-content: center; font-size: 1.6rem;
    }
    .shop-info { flex: 1; min-width: 0; }
    .shop-item-name { font-weight: 800; font-size: 0.98rem; }
    .shop-item.done .shop-item-name { text-decoration: line-through; color: var(--text-muted); opacity: 0.7; }
    .shop-item-cat { font-size: 0.76rem; color: var(--text-muted); font-weight: 700; }
    .shop-price { display: inline-block; background: var(--c-yellow-light); border: 2px solid var(--border-color); border-radius: 10px; padding: 0 8px; font-size: 0.82rem; font-weight: 900; margin: 3px 0; }
    .shop-desc { font-size: 0.82rem; color: var(--text-muted); margin-bottom: 6px; }
    .shop-code {
      display: inline-block; border: 2px dashed var(--border-color); border-radius: 12px;
      padding: 1px 10px; font-size: 0.8rem; font-weight: 800; cursor: pointer; background: var(--bg-card);
      color: var(--text-main); font-family: inherit; margin-right: 6px;
    }
    .shop-item-actions { display: flex; gap: 6px; margin-top: 6px; flex-wrap: wrap; }
    .shop-foot { padding: 10px 14px 14px; display: flex; gap: 8px; border-top: 2px dashed var(--border-light); }

    .modal-backdrop {
      display: none;
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(35, 30, 27, 0.65);
      z-index: 2000;
      align-items: center;
      justify-content: center;
      padding: 20px;
    }
    .modal-backdrop.open { display: flex; }
    .modal-box {
      max-height: 92vh;
      overflow-y: auto;
      background: var(--bg-card);
      border: var(--border-w) solid var(--border-color);
      border-radius: 22px;
      max-width: 440px;
      width: 100%;
      padding: 20px;
      box-shadow: 4px 6px 0 var(--border-color);
    }
  </style>
</head>
<body>

  <header class="top-nav">
    <div class="brand-title" onclick="switchTab('schedule')">
      <svg width="26" height="26" viewBox="0 0 32 32" fill="none">
        <path d="M4 26L16 6L28 26H4Z" fill="#E68574" stroke="#4A3E39" stroke-width="2.5" stroke-linejoin="round"/>
        <path d="M12 13L16 6L20 13H12Z" fill="#FFFFFF" stroke="#4A3E39" stroke-width="2"/>
        <circle cx="24" cy="9" r="4" fill="#E8BE65" stroke="#4A3E39" stroke-width="1.5"/>
      </svg>
      <span>四國慢遊手帖</span>
    </div>

    <div class="nav-scroll-wrap">
      <button class="nav-btn active" data-tab="schedule" onclick="switchTab('schedule')">🗓️ 每日行程</button>
      <button class="nav-btn" data-tab="flight" onclick="switchTab('flight')">✈️ 航班住宿</button>
      <button class="nav-btn" data-tab="budget" onclick="switchTab('budget')">💰 旅行記帳</button>
      <button class="nav-btn" data-tab="todo" onclick="switchTab('todo')">✅ 待辦事項</button>
      <button class="nav-btn" data-tab="shop" onclick="switchTab('shop')">🛍️ 購物</button>
      <button class="nav-btn" data-tab="emergency" onclick="switchTab('emergency')">🏥 備用資料</button>
      <button class="nav-btn" data-tab="home" onclick="switchTab('home')">🏠 旅程總覽</button>
    </div>

    <button class="theme-toggle-btn" id="themeToggle" title="切換日夜模式"><span id="themeIcon">☀️</span></button>
  </header>

  <main class="container">

    <section id="tab-schedule" class="tab-content active">
      
      <div class="top-notice-bubble">
        <span>👨‍👩‍👧‍👦 4位大人 ＋ 1位幼童（1歲10個月）自駕慢活</span>
        <span class="badge" style="background:#FFFFFF; font-size: 0.7rem;">5晚連住瓦町</span>
      </div>

      <div class="app-nav-grid">
        <div class="app-nav-card active-tab" onclick="switchTab('schedule')">
          <span>🗓️ 每日行程</span>
        </div>
        <div class="app-nav-card" onclick="switchTab('flight')">
          <span>✈️ 航班住宿</span>
        </div>
        <div class="app-nav-card" onclick="switchTab('budget')">
          <span>💰 旅行記帳</span>
        </div>
        <div class="app-nav-card" onclick="switchTab('todo')">
          <span>✅ 待辦事項</span>
        </div>
        <div class="app-nav-card" onclick="switchTab('shop')">
          <span>🛍️ 購物清單</span>
        </div>
        <div class="app-nav-card" onclick="switchTab('emergency')">
          <span>🏥 備用資料</span>
        </div>
      </div>

      <div class="day-selector-scroll">
        <div class="day-selector-card active" onclick="selectDay(1, this)">
          <div class="d-name">Day 1</div>
          <div class="d-date">12-23(三)</div>
        </div>
        <div class="day-selector-card" onclick="selectDay(2, this)">
          <div class="d-name">Day 2</div>
          <div class="d-date">12-24(四)</div>
        </div>
        <div class="day-selector-card" onclick="selectDay(3, this)">
          <div class="d-name">Day 3</div>
          <div class="d-date">12-25(五)</div>
        </div>
        <div class="day-selector-card" onclick="selectDay(4, this)">
          <div class="d-name">Day 4</div>
          <div class="d-date">12-26(六)</div>
        </div>
        <div class="day-selector-card" onclick="selectDay(5, this)">
          <div class="d-name">Day 5</div>
          <div class="d-date">12-27(日)</div>
        </div>
        <div class="day-selector-card" onclick="selectDay(6, this)">
          <div class="d-name">Day 6</div>
          <div class="d-date">12-28(一)</div>
        </div>
      </div>

      <div class="day-header-bar">
        <div class="day-header-title" id="currentDayTitle">2026-12-23 | 每日行程</div>
        <button class="btn-add-schedule" onclick="openAddEventModal()">＋ 新增行程</button>
      </div>

      <div class="day-summary" id="daySummary"></div>

      <div class="timeline-stream" id="timelineContainer">
      </div>

    </section>

    <section id="tab-flight" class="tab-content">
      <div class="day-header-bar" style="margin-top: 0;">
        <div class="day-header-title">✈️ 航班與住宿資訊</div>
        <button class="btn-add-schedule" onclick="openAddFlightHotelModal()">＋ 新增備註/卡片</button>
      </div>

      <div id="flightHotelContainer">
        <!-- 動態渲染航班與住宿卡片 -->
      </div>
    </section>

    <section id="tab-budget" class="tab-content">
      <div class="stat-banner">
        <div class="stat-card"><div class="stat-num" id="totalJpy">¥0</div><div class="stat-label">累積花費 (JPY)</div></div>
        <div class="stat-card"><div class="stat-num" id="totalTwd">NT$ 0</div><div class="stat-label">約合台幣 (匯率 0.22)</div></div>
      </div>
      <div class="book-card green">
        <div class="card-title"><span>➕ 新增支出項目</span></div>
        <div style="display: flex; gap: 8px; flex-wrap: wrap;">
          <input type="text" id="expenseName" class="input-field" placeholder="品項名稱 (例：讚岐烏龍、阿卡將)" style="flex: 2;">
          <input type="number" id="expenseAmount" class="input-field" placeholder="日幣金額 (¥)" style="flex: 1;">
          <select id="expenseCategory" class="input-field" style="flex: 1;">
            <option value="🍽️ 餐飲">🍽️ 餐飲</option><option value="🚗 交通">🚗 交通</option>
            <option value="🎟️ 門票">🎟️ 門票</option><option value="🛍️ 購物">🛍️ 購物</option>
            <option value="🏨 住宿">🏨 住宿</option><option value="✨ 其他">✨ 其他</option>
          </select>
        </div>
        <button class="btn-action green" style="width: 100%; justify-content: center;" onclick="addExpense()">💾 記錄一筆</button>
      </div>
      <div class="book-card blue">
        <div class="card-title" style="justify-content: space-between;">
          <span>📋 記帳明細</span>
          <button class="btn-action" style="padding: 4px 10px; font-size: 0.75rem;" onclick="clearExpenses()">清空</button>
        </div>
        <div id="expenseList"></div>
      </div>
    </section>

    <section id="tab-todo" class="tab-content">
      <div class="book-card green">
        <div class="card-title"><span>📝 待辦事項清單</span></div>
        <div style="display: flex; gap: 8px; margin-bottom: 12px;">
          <input type="text" id="newTodoInput" class="input-field" placeholder="新增待辦 (例：換日幣、確認汽座)" style="margin-bottom: 0;">
          <button class="btn-action green" style="flex-shrink: 0;" onclick="addTodo()">新增</button>
        </div>
        <div id="todoList"></div>
      </div>
    </section>

    <section id="tab-shop" class="tab-content">
      <div class="day-header-bar" style="margin-top: 0;">
        <div class="day-header-title">🛍️ 購物清單</div>
        <button class="btn-add-schedule" onclick="openShopModal(-1)">＋ 新增店家</button>
      </div>
      <div class="stat-banner">
        <div class="stat-card"><div class="stat-num" id="shopDoneNum">0/0</div><div class="stat-label">已買商品</div></div>
        <div class="stat-card"><div class="stat-num" id="shopLeftPrice">¥0</div><div class="stat-label">未買商品合計（有填價格者）</div></div>
      </div>
      <div id="shopContainer"></div>
    </section>

    <section id="tab-emergency" class="tab-content">
      <div class="book-card coral">
        <div class="card-title"><span>🚑 小兒急診與緊急電話</span></div>
        <p><strong>#8000</strong> 日本小兒救急電話諮詢（24小時撥打）</p>
        <p style="margin-top: 8px;">🏥 <strong>香川縣立中央病院</strong>：087-811-3333（高松市朝日町 1-2-1，設有小兒專任急診部）</p>
      </div>
      <div class="book-card yellow">
        <div class="card-title"><span>⛽ 加油實務提醒</span></div>
        <p>租用汽油休旅車一律加 <strong>紅色油槍 Regular (レギュラー)</strong>，還車前索取滿油證明發票。</p>
      </div>
    </section>

    <section id="tab-home" class="tab-content">
      <div class="book-card coral">
        <div class="card-title"><span>🌸 香川四國慢遊特點</span></div>
        <p>定點高松 5 晚不搬遷行李，每天只跑一個方向，午睡盡量排在車上或飯店步行範圍。景點日期依公休日與營業時間重新排過。</p>
      </div>
      <div class="book-card blue">
        <div class="card-title"><span>🚗 每日動線與車程</span></div>
        <ul class="check-list">
          <li><strong>12/23 三</strong>：機場 → 栗林公園 → 飯店，約 45 分</li>
          <li><strong>12/24 四</strong>：高屋神社 + 父母濱，約 3 小時（最遠的一天）</li>
          <li><strong>12/25 五</strong>：宇多津（水族館、おか泉、公園），約 1.5 小時</li>
          <li><strong>12/26 六</strong>：玩具美術館 + 丸龜町（步行）+ 屋島夕陽，約 45 分</li>
          <li><strong>12/27 日</strong>：琴平金刀比羅宮，約 1 小時 40 分</li>
          <li><strong>12/28 一</strong>：兒童之國 → 加油 → 還車，約 50 分</li>
        </ul>
      </div>
      <div class="book-card yellow">
        <div class="card-title"><span>📅 公休與營業時間速查</span></div>
        <ul class="check-list">
          <li>栗林公園：12 月 7:00–17:00</li>
          <li>讚岐玩具美術館：週四休、10:00–16:00（最終入館 15:30）</li>
          <li>屋島やしまーる：週二休；週五六到 21:00，其餘到 17:00</li>
          <li>おか泉：週一二休、11:00–19:00</li>
          <li>四國水族館：約 9:00–18:00，冬季有維護休館，須確認</li>
          <li>讚岐兒童之國：原則週一休，12/25–1/7 冬休無休、9:00–17:00</li>
          <li>天空鳥居林道：曾多次落石封閉，出發前查</li>
          <li>日落：約 16:55，12 月天黑很快</li>
        </ul>
        <p style="font-size:0.78rem; color: var(--text-muted); margin-top:8px;">資料來自公開網頁，可能更新，出發前請再查官網。</p>
      </div>
    </section>

    <div id="editEventModal" class="modal-backdrop">
      <div class="modal-box">
        <div class="card-title"><span id="eventModalTitle">✏️ 編輯行程節點</span></div>
        <input type="hidden" id="eventIndex">
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">時間 (例如 12:20)</label>
          <input type="text" id="eventTime" class="input-field">
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">行程標題</label>
          <input type="text" id="eventTitle" class="input-field">
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">類別標籤 (例如 景點、美食、交通)</label>
          <input type="text" id="eventTag" class="input-field">
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">詳細備註說明</label>
          <input type="text" id="eventMemo" class="input-field">
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">注意事項（一行一條）</label>
          <textarea id="eventNotes" class="input-field" style="height: 110px; resize: vertical;"></textarea>
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">車程提示（例如 🚗 約 20 分，可留空）</label>
          <input type="text" id="eventDrive" class="input-field">
        </div>
        <div style="margin-bottom: 16px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">Google 地圖查詢關鍵字</label>
          <input type="text" id="eventMapQuery" class="input-field">
        </div>
        <div style="display: flex; gap: 10px; justify-content: flex-end;">
          <button class="btn-action" style="background: var(--bg-main);" onclick="closeEventModal()">取消</button>
          <button class="btn-action coral" onclick="saveEventItem()">儲存</button>
        </div>
      </div>
    </div>

    <div id="editExpenseModal" class="modal-backdrop">
      <div class="modal-box">
        <div class="card-title"><span>✏️ 編輯記帳內容</span></div>
        <input type="hidden" id="editExpenseId">
        <input type="text" id="editExpenseName" class="input-field">
        <input type="number" id="editExpenseAmount" class="input-field">
        <select id="editExpenseCategory" class="input-field">
          <option value="🍽️ 餐飲">🍽️ 餐飲</option><option value="🚗 交通">🚗 交通</option>
          <option value="🎟️ 門票">🎟️ 門票</option><option value="🛍️ 購物">🛍️ 購物</option>
          <option value="🏨 住宿">🏨 住宿</option><option value="✨ 其他">✨ 其他</option>
        </select>
        <div style="display: flex; gap: 10px; justify-content: flex-end;">
          <button class="btn-action" onclick="closeEditModal()">取消</button>
          <button class="btn-action coral" onclick="saveEditedExpense()">儲存修改</button>
        </div>
      </div>
    </div>


    <div id="shopModal" class="modal-backdrop">
      <div class="modal-box">
        <div class="card-title"><span id="shopModalTitle">🏬 店家</span></div>
        <input type="hidden" id="shopIdx">
        <label class="mini-label">店名</label>
        <input type="text" id="shopName" class="input-field">
        <label class="mini-label">分店 / 備註（例：瓦町 FLAG 5F）</label>
        <input type="text" id="shopPlace" class="input-field">
        <label class="mini-label">購買日（連到當天行程）</label>
        <select id="shopDay" class="input-field">
          <option value="0">不指定</option>
          <option value="1">Day 1　12/23</option><option value="2">Day 2　12/24</option>
          <option value="3">Day 3　12/25</option><option value="4">Day 4　12/26</option>
          <option value="5">Day 5　12/27</option><option value="6">Day 6　12/28</option>
        </select>
        <label class="mini-label">Google 地圖關鍵字</label>
        <input type="text" id="shopMap" class="input-field">
        <label class="mini-label">小提醒</label>
        <input type="text" id="shopTip" class="input-field">
        <div style="display: flex; gap: 10px; justify-content: space-between; align-items: center;">
          <button id="btnDeleteShop" class="btn-action" style="background: #FFF; color: var(--c-coral); border-color: var(--c-coral);" onclick="deleteShop()">刪除</button>
          <div style="display: flex; gap: 8px;">
            <button class="btn-action" style="background: var(--bg-main);" onclick="closeModalById('shopModal')">取消</button>
            <button class="btn-action coral" onclick="saveShop()">儲存</button>
          </div>
        </div>
      </div>
    </div>

    <div id="shopItemModal" class="modal-backdrop">
      <div class="modal-box">
        <div class="card-title"><span id="shopItemModalTitle">🛒 商品</span></div>
        <input type="hidden" id="itemShopIdx">
        <input type="hidden" id="itemIdx">
        <label class="mini-label">商品名稱</label>
        <input type="text" id="itemName" class="input-field">
        <div style="display: flex; gap: 8px;">
          <div style="flex: 1;"><label class="mini-label">分類（例：收納包）</label><input type="text" id="itemCat" class="input-field"></div>
          <div style="flex: 1;"><label class="mini-label">價格（日圓，可空）</label><input type="number" id="itemPrice" class="input-field"></div>
        </div>
        <label class="mini-label">說明</label>
        <input type="text" id="itemDesc" class="input-field">
        <label class="mini-label">商品編號（可空，點擊可複製給店員看）</label>
        <input type="text" id="itemCode" class="input-field">
        <label class="mini-label">官網連結（可空）</label>
        <input type="text" id="itemUrl" class="input-field" placeholder="https://...">
        <label class="mini-label">圖片網址（可空，無則顯示圖示）</label>
        <input type="text" id="itemImg" class="input-field" placeholder="https://...">
        <div style="display: flex; gap: 10px; justify-content: space-between; align-items: center;">
          <button id="btnDeleteItem" class="btn-action" style="background: #FFF; color: var(--c-coral); border-color: var(--c-coral);" onclick="deleteShopItem()">刪除</button>
          <div style="display: flex; gap: 8px;">
            <button class="btn-action" style="background: var(--bg-main);" onclick="closeModalById('shopItemModal')">取消</button>
            <button class="btn-action coral" onclick="saveShopItem()">儲存</button>
          </div>
        </div>
      </div>
    </div>

    <!-- 航班與住宿編輯彈跳視窗 (Modal) -->
    <div id="editFlightHotelModal" class="modal-backdrop">
      <div class="modal-box">
        <div class="card-title"><span id="flightHotelModalTitle">✏️ 編輯航班 / 住宿</span></div>
        <input type="hidden" id="fhIndex">
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">卡片標題 (例：🛫 星宇航空 去程 JX300)</label>
          <input type="text" id="fhTitle" class="input-field">
        </div>
        <div style="display: flex; gap: 8px; margin-bottom: 10px;">
          <div style="flex: 1;">
            <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">右上標籤 (例：台中直飛、5晚連住)</label>
            <input type="text" id="fhBadge" class="input-field">
          </div>
          <div style="flex: 1;">
            <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">主題色卡</label>
            <select id="fhColor" class="input-field">
              <option value="blue">水色藍 (Blue)</option>
              <option value="coral">珊瑚粉 (Coral)</option>
              <option value="yellow">山吹黃 (Yellow)</option>
              <option value="green">若竹綠 (Green)</option>
            </select>
          </div>
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">核心資訊 / 時間路線 (例：12/23 08:50 台中 ➔ 12:20 高松)</label>
          <input type="text" id="fhMainInfo" class="input-field">
        </div>
        <div style="margin-bottom: 10px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">自訂備註說明 (可自行調整備註、停車、取車事項)</label>
          <textarea id="fhMemo" class="input-field" style="height: 75px; resize: vertical;"></textarea>
        </div>
        <div style="margin-bottom: 14px;">
          <label style="font-size: 0.8rem; font-weight: 800; color: var(--text-muted); display: block; margin-bottom: 4px;">Google 地圖查詢地點 (選填，無則不顯示地點按鈕)</label>
          <input type="text" id="fhMapQuery" class="input-field" placeholder="例：KOKO HOTEL Takamatsu 或留空">
        </div>
        <div style="display: flex; gap: 10px; justify-content: space-between; align-items: center;">
          <button id="btnDeleteFh" class="btn-action" style="background: #FFF; color: var(--c-coral); border-color: var(--c-coral);" onclick="deleteFlightHotelItem()">刪除</button>
          <div style="display: flex; gap: 8px;">
            <button class="btn-action" style="background: var(--bg-main);" onclick="closeFlightHotelModal()">取消</button>
            <button class="btn-action coral" onclick="saveFlightHotelItem()">儲存</button>
          </div>
        </div>
      </div>
    </div>

  </main>

  <script>
    /* v4：依區域重新排序，並依各景點公休日/營業時間排日期。車程為預估，請以 Google 地圖即時為準。
       星期：12/23 三、12/24 四、12/25 五、12/26 六、12/27 日、12/28 一 */
    const defaultSchedules = {
      1: {
        dateStr: "2026-12-23 (三)",
        summary: "🚗 今日車程合計約 45 分（機場→栗林公園→飯店），晚餐與採買都在飯店步行範圍。栗林公園 12 月 17:00 閉園，所以先去公園再進飯店。",
        events: [
          { time: "08:50", title: "搭機起飛", tag: "航班", memo: "星宇航空 JX300（台中清泉崗 RMQ → 高松 TAK）", notes: "國際線建議提前約 2 小時到機場\n嬰兒/幼童餐、嬰兒推車（可在登機門前交付）請先向航空公司確認\n隨身包備奶瓶或點心、替換衣物（起降耳壓可讓幼兒吸吮）", mapQuery: "Taichung International Airport" },
          { time: "12:20", title: "抵達高松機場", tag: "交通", memo: "入境、領行李；先處理尿布與洗手間再去取車", notes: "先填好 Visit Japan Web 並存 QR Code，入境最快\n駕照正本 + 日文譯本 + 護照放同一個隨手包", mapQuery: "Takamatsu Airport" },
          { time: "13:05", title: "機場內午餐", tag: "美食", memo: "取車前先吃飽，避免進市區才找店（幼童已空腹多時）", notes: "航廈不大，同班機旅客會集中用餐，入境後先去排隊\n幼童麵條請店家剪短或自備食物剪刀、高湯加熱水稀釋", mapQuery: "Takamatsu Airport" },
          { time: "13:40", title: "取車出發", tag: "自駕", memo: "1F TOYOTA 櫃台搭接駁車約 3 分鐘取車；導航直接設定「栗林公園 東門」", notes: "兒童座椅安裝請請店員一起確認（日本 6 歲未滿須使用兒童座椅）\n繞車一圈錄影存證車況\n確認 ETC 卡、油種（Regular 紅色油槍）\n8 人座車體大，起步先熟悉車寬與後視鏡", mapQuery: "TOYOTA Rent a Car Takamatsu Airport" },
          { time: "14:35", title: "栗林公園 散策", tag: "景點", drive: "🚗 機場 → 約 35 分", memo: "直接從機場過去，比先進飯店再折返省約 20 分。路線：東門 → 南湖偃月橋 → 掬月亭 → 北湖，約 1.5 小時", notes: "12 月開園 7:00–17:00（全年最短），北門關閉後只能走東門，建議 16:30 前出園\n門票成人 ¥500，學齡前兒童免費\n推車可進，但南側是石板路難推，備背巾較輕鬆\n公園可借輪椅與雨傘（免費），資料未見推車租借，原行程「東門借推車」請以現場為準\n飛來峰需爬階，帶幼童可略過\n行李留車內請勿外露、務必上鎖", mapQuery: "Ritsurin Garden East Gate Takamatsu" },
          { time: "16:45", title: "KOKO HOTEL 入住", tag: "住宿", drive: "🚗 栗林公園 → 約 10 分", memo: "停特約停車場、卸行李、先讓幼兒休息", notes: "8 人座車高約 1.9–2 公尺，立體/機械式停車場常有限高，入庫前先向飯店確認可停哪一座\n停車折抵：出庫前先到櫃台蓋章（詳見航班住宿頁）", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "17:30", title: "讚岐麵業 兵庫町本店", tag: "美食", drive: "🚶 飯店步行約 10 分", memo: "道地烏龍麵，榻榻米和室席位，高湯過水去鹹後分食幼童", notes: "營業時間與公休日未能在公開資料確認，請先查官網或來電\n熱湯小心燙傷，湯麵先放涼\n聖誕週用餐時段可能排隊", mapQuery: "Sanuki Mengyo Hyogomachi" },
          { time: "18:45", title: "阿卡將本舖 瓦町FLAG店", tag: "購物", drive: "🚶 步行約 10 分", memo: "瓦町 FLAG 5F 採買保暖發熱衣、副食品米餅與尿布", notes: "原資料營業至 20:00，請現場確認\n護照隨身帶，免稅規定以店內公告為準\n先買明天會用到的暖暖包、備用衣褲（Day 2、Day 4 吹海風/山風）", mapQuery: "Akachan Honpo KAWARAMACHI FLAG" }
        ]
      },
      2: {
        dateStr: "2026-12-24 (四)",
        summary: "🚗 今日是最遠的一天，車程合計約 3 小時（去 70 分 + 景點間 20～30 分 + 回程 70 分）。幼兒午睡安排在車上。排在週四是因為：週四玩具美術館休館、屋島やしまーる 17:00 就關，且高屋神社週末假日有車輛管制。",
        events: [
          { time: "10:15", title: "出發前往高屋神社", tag: "交通", drive: "🚗 約 70 分", memo: "高松自動車道往三豊方向，下さぬき豊中 IC 後轉林道上山", notes: "出發前一天、當天早上各查一次三豊市「林道 豊中七宝山線」是否通行（過去多次因落石封閉）\n若封路：天空鳥居改走下宮步道（單程約 50 分，不適合幼童）或直接跳過，改把時間留給父母濱\n出發前先加滿油、備好尿布與點心", mapQuery: "Takaya Shrine Hongu Kanonji" },
          { time: "11:25", title: "高屋神社 本宮（天空鳥居）", tag: "絕景", memo: "平日可開上本宮停車場；停車後上坡約 150 公尺到本宮，預留 60～75 分鐘", notes: "林道很窄，部分路段普通車難以會車，8 人座大車務必慢速、遇車先讓\n停車後上坡陡，鳥居周邊另有石階（資料寫約 270 階），原行程「步行 3 分鐘免爬」不要全信，請準備背巾\n穿運動鞋，山頂風大，帶防風外套；雨後或結冰石階很滑，當天天氣不好就放棄\n本宮附近廁所很少（男女各 1），先在山下上完\n週末假日 10:00–18:30 一般車輛可能被管制改搭接駁", mapQuery: "Takaya Shrine Hongu Kanonji" },
          { time: "12:45", title: "三豊市區 午餐", tag: "美食", drive: "🚗 約 20 分", memo: "在下山路上、往父母濱的路線選一間烏龍或定食（取代原本繞去觀音寺市區）", notes: "冬季不少店 14:00 前就收，12:45 前入座\n先在地圖選好並確認今天不是公休\n飯後上車讓幼兒補眠", mapQuery: "Mitoyo Toyonaka udon" },
          { time: "14:20", title: "抵達父母濱（車內午睡＋踩點）", tag: "絕景", drive: "🚗 約 25 分", memo: "幼兒在車上睡到約 15:30；大人看潮位、風向、挑拍照位置", notes: "關鍵：退潮 + 無風 + 日落前後約 1 小時才有完整倒影。請先查氣象廳潮位與三豊市觀光交流局的最佳時間\n免費停車場；旺季才有預約制付費停車\n不要把睡著的幼童單獨留在車上，大人輪流看顧", mapQuery: "Chichibugahama Beach Mitoyo" },
          { time: "15:30", title: "父母濱 天空之鏡 日落", tag: "絕景", memo: "沙灘與潮間帶玩耍、拍倒影，日落約 16:55，17:05 收工", notes: "潮間帶泥濘，備替換衣褲鞋襪、防水墊或塑膠袋\n日落後氣溫驟降，帽子、手套、暖暖包必備\n風大水面會起波紋、倒影變差\n天黑很快，備手機燈照路\n水邊絕對不離開視線", mapQuery: "Chichibugahama Beach Mitoyo" },
          { time: "17:10", title: "返回高松", tag: "交通", drive: "🚗 約 70 分", memo: "高速公路返回飯店，幼兒車上睡", notes: "夜間山區與高速注意休息\n進市區前打電話確認晚餐訂位", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "18:45", title: "海鮮鍋物與雜炊（聖誕夜）", tag: "美食", memo: "飯店周邊選一間有座敷或兒童椅的海鮮鍋物店，暖身收尾", notes: "聖誕夜非常熱門，務必提前預約\n預約時說明有 1 歲多幼童，要求座敷或兒童椅\n鍋物與雜炊要放涼再給幼童", mapQuery: "Takamatsu Seafood Izakaya" }
        ]
      },
      3: {
        dateStr: "2026-12-25 (五)",
        summary: "🚗 車程合計約 1 小時 30 分（去 40 + 回 40，加景點間約 10 分）。水族館、午餐、公園都在宇多津，彼此約 5 分鐘；晚餐步行抵達。",
        events: [
          { time: "08:50", title: "出發前往宇多津", tag: "交通", drive: "🚗 約 40 分", memo: "走高松自動車道 + 一般道，目標 09:30 到水族館", notes: "設定停車場為導航終點（水族館停車場資料顯示約 223 台）\n幼童在車上先吃點心", mapQuery: "Shikoku Aquarium Utazu" },
          { time: "09:30", title: "四國水族館", tag: "親子", memo: "趁幼兒精神好先逛；低水槽平視水母與企鵝，約 2 小時", notes: "資料顯示約 9:00–18:00，最終入館為閉館前 30 分；冬季曾有維護休館，行前請查官網公告\n3 歲未滿免費\n海豚秀時間與哺乳室、推車租借資訊請看官網或入館公告\n館內外溫差大，穿脫方便的外套\n停車場約一次 ¥600（資料，可能調整）", mapQuery: "Shikoku Aquarium Utazu" },
          { time: "11:40", title: "Okasen（おか泉）烏龍", tag: "美食", drive: "🚗 約 5 分", memo: "宇多津名店，提早到避開午餐尖峰；大蝦天婦羅可分食", notes: "營業 11:00–19:00，週一週二公休（今天週五營業）\n原行程寫 10:30 到，但店 11:00 才開，已改 11:40\n停車場與座敷席資料未能確認，請先查地圖或來電\n天婦羅切小塊，幼童先吃白麵", mapQuery: "Okasen Udon Utazu" },
          { time: "12:55", title: "宇多津臨海公園", tag: "放電", drive: "🚗 約 5 分", memo: "緊鄰水族館的海濱大草皮，遠眺瀨戶大橋，約 45 分", notes: "冬季海風強，帽子外套手套必備\n13:45 前離開，讓幼兒在回程車上睡午覺\n草皮濕冷時別讓幼童坐地", mapQuery: "Utazu Rinkai Park" },
          { time: "13:50", title: "返回飯店 午睡", tag: "休息", drive: "🚗 約 40 分", memo: "幼兒車上睡，到飯店回房繼續午睡；大人也休息", notes: "車上睡著的幼兒抱進房間時動作輕，避免吵醒\n停車請依 Day 1 的特約停車場", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "16:00", title: "丸龜町商店街 散步", tag: "逛街", drive: "🚶 步行約 10 分", memo: "有頂拱廊避冬風，地面平整適合推車，順路逛街補貨", notes: "聖誕節傍晚人潮多，推車注意讓行\n商店街內有餐廳與咖啡座，可讓幼兒喝點熱飲", mapQuery: "Marugamemachi Street Takamatsu" },
          { time: "17:15", title: "Ito Loin（イトーロイン）燒肉", tag: "美食", drive: "🚶 步行約 5 分", memo: "高松市丸亀町 12-5，預約包廂（2～16 人），肉切小片拌飯給幼童", notes: "營業 17:00 起（週五），請提前預約並說明帶幼童\n未明確確認公休日，請再向店家確認\n燒肉煙味重，外套先放車上或用袋子裝\n肉要全熟、切小塊再給幼童", mapQuery: "Ito Loin Takamatsu Marugamemachi" }
        ]
      },
      4: {
        dateStr: "2026-12-26 (六)",
        summary: "🚗 車程合計約 45 分（飯店⇄屋島各約 20 分），上午下午都在步行圈。屋島只跑一趟：週六やしまーる營業到 21:00，可看夕陽。わら家 因為會讓屋島多跑一趟，已從午餐移除（見航班住宿頁備註）。",
        events: [
          { time: "10:00", title: "讚岐玩具美術館", tag: "室內", drive: "🚶 飯店步行約 10 分", memo: "高松市大工町 8-1，有 0～2 歲專用「赤ちゃん木育ひろば」，約 1.5 小時", notes: "開館 10:00–16:00（最終入館 15:30），每週四休館，12/29–1/3 休館（今天週六營業）\n成人約 ¥900、小學以下約 ¥700、6 個月未滿免費（資料，請以官網為準）\n需脫鞋，大人也要穿襪子\n週末與寒假可能有入場管制，出發前查官網\n小學生以下不可單獨入館", mapQuery: "Sanuki Toy Museum Takamatsu" },
          { time: "11:45", title: "丸龜町周邊 午餐", tag: "美食", memo: "玩具美術館步行範圍內選烏龍或定食，吃完走商店街回飯店", notes: "週六中午商店街人多，11:45 前入座\n先在地圖選 2 間備案", mapQuery: "Marugamemachi Udon Takamatsu" },
          { time: "13:00", title: "飯店午睡", tag: "休息", drive: "🚶 步行約 10 分", memo: "13:00–15:00 午睡，大人整理行李與保暖用品", notes: "15:10 要出發前往屋島，13:00 前務必躺下\n整理暖暖包、帽子手套", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "15:10", title: "前往屋島山頂", tag: "交通", drive: "🚗 約 20 分", memo: "跟著導航上山，停車場在やしまーる西側", notes: "山路彎，幼童易暈車，上山前別吃太飽\n停車場到やしまーる步行約 550 公尺（資料），備背巾", mapQuery: "Yashimaru Takamatsu" },
          { time: "15:40", title: "屋島山上交流拠點施設 やしまーる", tag: "夕陽", memo: "全景落地窗避風，欣賞瀨戶內海落日，日落約 16:55", notes: "週五六營業到 21:00；週一三四日僅到 17:00；週二休館\n室內可避風，室外展望台風大，帽子外套暖暖包\n廁所在主入口旁，先上再看夕陽\n看完夕陽就下山，不要等夜景（幼兒太晚）\n屋島寺與獅子之靈巖有階梯，有餘力再逛", mapQuery: "Yashimaru Takamatsu" },
          { time: "17:15", title: "下山回市區", tag: "交通", drive: "🚗 約 20 分", memo: "直接開去餐廳，行李不用回飯店", notes: "下山天已黑，山路慢開\n先打電話確認訂位", mapQuery: "Ikkaku Takamatsu" },
          { time: "17:45", title: "骨付鳥 一鶴 高松店", tag: "美食", memo: "香酥鮮嫩雛雞腿；幼兒點雞肉炊飯とりめし與清雞湯", notes: "週六晚上人多，務必先預約並指定 17:30–17:45\n烤雞要約 20 分鐘，先點炊飯與湯讓幼兒墊肚子\n招牌雞腿帶辣味調味（おやどり偏硬較辣、ひなどり較嫩），點餐時說明有幼童，請店家建議少辣或另點不辣的炊飯與湯\n雞骨小心，肉撕小塊", mapQuery: "Ikkaku Takamatsu" }
        ]
      },
      5: {
        dateStr: "2026-12-27 (日)",
        summary: "🚗 車程合計約 1 小時 40 分（去回各約 50 分）。下午回飯店午睡，晚餐在市區。週日參道人多，早出發。",
        events: [
          { time: "08:45", title: "出發前往琴平", tag: "交通", drive: "🚗 約 50 分", memo: "高松自動車道或國道 11 號，目標 09:40 抵達", notes: "週日琴平停車場易滿，越早越好\n幼童在車上先吃點心", mapQuery: "Kotohira-gu Shrine Kotohira" },
          { time: "09:40", title: "琴平 金刀比羅宮", tag: "參拜", memo: "表參道 → 大門（365 階）→ 旭社（628 階）→ 御本宮（785 階），體力不足就折返", notes: "御本宮 785 階、奧社 1,368 階；往返御本宮約 1.5～2 小時\n推車不能上，請輪流用背巾；抱 12 公斤左右的幼童爬 785 階很累，建議最遠到旭社或御本宮擇一\n冬季或雨後石階濕滑，穿防滑鞋\n參道商店可能提供借用拐杖（資料）\n廁所位置請先在地圖確認，出發前先上\n12:00 前一定要下到參道，趕午餐與幼兒午睡", mapQuery: "Kotohira-gu Shrine Kotohira" },
          { time: "12:00", title: "中野うどん学校 琴平校", tag: "美食", drive: "🚶 步行/短程車 約 10 分", memo: "琴平町 796，大桌座位寬敞；飯後可採買和三盆糖", notes: "資料顯示 9:00–15:00（體驗），店鋪營業到 17:30，無休\n停車場約 30 台、先到先停、付費（週日約 ¥700 起，以現場公告為準）\n熱湯與麵條先放涼，幼童麵條剪短", mapQuery: "Nakano Udon School Kotohira" },
          { time: "13:15", title: "返回飯店 午睡", tag: "休息", drive: "🚗 約 50 分", memo: "幼兒車上睡，到飯店繼續午睡；下午自由休息", notes: "若精神好，可順路到丸龜町補買伴手禮", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "17:30", title: "焼肉正（和牛慶功宴）", tag: "美食", drive: "🚶 或 🚗 市區內", memo: "掘式榻榻米座位、無煙抽風，一家人乾杯慶祝旅程圓滿", notes: "營業時間與公休日未能在公開資料確認，請提前電話確認並預約\n要求掘式或座敷席\n肉要全熟、切小塊\n外套會沾味，備好袋子", mapQuery: "Yakiniku Sho Takamatsu" }
        ]
      },
      6: {
        dateStr: "2026-12-28 (一)",
        summary: "🚗 車程約 50 分，兒童之國在機場旁，不繞路；11:00 前抵達航廈，13:20 起飛前時間寬裕。原行程的加油 11:20 與航班頁寫的 10:45 互相矛盾，已統一提前。",
        events: [
          { time: "08:30", title: "退房出發", tag: "退房", memo: "全體行李上車，確認護照、停車券、尿布包", notes: "檢查房間與抽屜，別留下幼兒用品\n出庫前先到櫃台蓋章折抵停車費\n導航設定「さぬきこどもの国」", mapQuery: "KOKO HOTEL Takamatsu" },
          { time: "09:15", title: "讚岐兒童之國", tag: "親子", drive: "🚗 約 35 分", memo: "高松市香南町由佐 3209，緊鄰機場；わくわく児童館有幼兒コーナー、授乳室，約 1 小時", notes: "開園 9:00–17:00；原則週一休園，但 12/25–1/7（12/30–1/1 除外）冬休期間無休，所以今天週一仍營業\n資料可能過期，請出發前查官網（sanuki.or.jp）\n入園免費\n冬季戶外遊具冷，主要玩室內與看飛機\n10:20 一定要離開，避免耽誤還車", mapQuery: "Sanuki Kodomo no Kuni" },
          { time: "10:25", title: "機場旁加油站 滿油", tag: "加油", drive: "🚗 約 10 分", memo: "加滿紅色油槍 Regular，並索取發票", notes: "還車點交時店員會看油量，發票先收好\n前一天先在導航存好離機場最近的加油站", mapQuery: "Gas Station Takamatsu Airport" },
          { time: "10:40", title: "TOYOTA 還車", tag: "還車", memo: "點交、歸還 ETC 卡與兒童座椅，接駁車約 3 分鐘到航廈", notes: "拍照存證車況與里程\n行李先全部帶下車再交車\n提醒：原航班頁寫 11:00 前還車，現在 10:40 比較有餘裕", mapQuery: "TOYOTA Rent a Car Takamatsu Airport" },
          { time: "11:00", title: "高松機場 報到出境", tag: "機場", memo: "辦理登機托運，之後免稅店採買、機場內午餐", notes: "國際線櫃台建議最晚 11:20 前報到\n幼兒推車可在登機門前交付航空公司", mapQuery: "Takamatsu Airport" },
          { time: "13:20", title: "搭機返台", tag: "航班", memo: "星宇航空 JX301（預計 15:40 抵達台中清泉崗）", notes: "登機前讓幼兒換好尿布、上洗手間\n起降時餵奶或給水，減輕耳壓", mapQuery: "Takamatsu Airport" }
        ]
      }
    };

    /* 儲存鍵改為 v3：舊版 v2 已存的行程不會覆蓋新行程 */
    let schedules = JSON.parse(localStorage.getItem('shikoku_schedules_v3')) || defaultSchedules;
    let currentDay = 1;

    function esc(t) {
      return String(t == null ? '' : t).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
    }

    function renderDayTimeline(day) {
      currentDay = day;
      const data = schedules[day];
      if (!data) return;

      document.getElementById('currentDayTitle').textContent = `${data.dateStr} | 每日行程`;
      const summaryEl = document.getElementById('daySummary');
      if (summaryEl) {
        summaryEl.textContent = data.summary || '';
        summaryEl.style.display = data.summary ? 'block' : 'none';
      }
      const container = document.getElementById('timelineContainer');
      container.innerHTML = '';

      data.events.forEach((item, index) => {
        const row = document.createElement('div');
        row.className = 'timeline-row';

        const mapUrl = `https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(item.mapQuery || item.title)}`;
        const routeUrl = `https://www.google.com/maps/dir/?api=1&destination=${encodeURIComponent(item.mapQuery || item.title)}`;

        const driveHtml = item.drive ? `<div class="drive-chip">${esc(item.drive)}</div>` : '';
        const noteLines = (item.notes || '').split('\n').map(x => x.trim()).filter(Boolean);
        const notesHtml = noteLines.length
          ? `<div class="notes-box"><div class="notes-title">⚠️ 注意事項</div><ul>${noteLines.map(x => `<li>${esc(x)}</li>`).join('')}</ul></div>`
          : '';

        row.innerHTML = `
          <div class="timeline-dot"></div>
          <div class="schedule-white-card">
            ${driveHtml}
            <div class="card-top-header">
              <span class="time-badge">${esc(item.time)}</span>
              <span class="spot-name">${esc(item.title)}</span>
              <span class="tag-bubble">${esc(item.tag || '行程')}</span>
            </div>
            <div class="card-detail-memo">${esc(item.memo || '')}</div>
            ${notesHtml}
            <div class="card-actions-bar">
              <a class="action-sub-pill" href="${mapUrl}" target="_blank" rel="noopener">
                📍 地點
              </a>
              <a class="action-sub-pill" href="${routeUrl}" target="_blank" rel="noopener">
                🧭 路線
              </a>
              <button class="action-sub-pill" onclick="openEditEventModal(${index})">
                ✏️ 編輯
              </button>
            </div>
          </div>
        `;
        container.appendChild(row);
      });
    }

    function selectDay(day, element) {
      document.querySelectorAll('.day-selector-card').forEach(c => c.classList.remove('active'));
      element.classList.add('active');
      renderDayTimeline(day);
    }

    function openEditEventModal(index) {
      const event = schedules[currentDay].events[index];
      if (!event) return;

      document.getElementById('eventModalTitle').textContent = '✏️ 編輯行程節點';
      document.getElementById('eventIndex').value = index;
      document.getElementById('eventTime').value = event.time;
      document.getElementById('eventTitle').value = event.title;
      document.getElementById('eventTag').value = event.tag || '行程';
      document.getElementById('eventMemo').value = event.memo || '';
      document.getElementById('eventNotes').value = event.notes || '';
      document.getElementById('eventDrive').value = event.drive || '';
      document.getElementById('eventMapQuery').value = event.mapQuery || event.title;

      document.getElementById('editEventModal').classList.add('open');
    }

    function openAddEventModal() {
      document.getElementById('eventModalTitle').textContent = '＋ 新增行程節點';
      document.getElementById('eventIndex').value = -1;
      document.getElementById('eventTime').value = '12:00';
      document.getElementById('eventTitle').value = '';
      document.getElementById('eventTag').value = '景點';
      document.getElementById('eventMemo').value = '';
      document.getElementById('eventNotes').value = '';
      document.getElementById('eventDrive').value = '';
      document.getElementById('eventMapQuery').value = '';

      document.getElementById('editEventModal').classList.add('open');
    }

    function closeEventModal() {
      document.getElementById('editEventModal').classList.remove('open');
    }

    function saveEventItem() {
      const index = parseInt(document.getElementById('eventIndex').value);
      const time = document.getElementById('eventTime').value.trim();
      const title = document.getElementById('eventTitle').value.trim();
      const tag = document.getElementById('eventTag').value.trim();
      const memo = document.getElementById('eventMemo').value.trim();
      const notes = document.getElementById('eventNotes').value.trim();
      const drive = document.getElementById('eventDrive').value.trim();
      const mapQuery = document.getElementById('eventMapQuery').value.trim() || title;

      if (!time || !title) {
        alert('請填寫時間與行程名稱！');
        return;
      }

      if (index === -1) {
        schedules[currentDay].events.push({ time, title, tag, memo, notes, drive, mapQuery });
      } else {
        schedules[currentDay].events[index] = { time, title, tag, memo, notes, drive, mapQuery };
      }

      schedules[currentDay].events.sort((a, b) => a.time.localeCompare(b.time));

      localStorage.setItem('shikoku_schedules_v3', JSON.stringify(schedules));
      renderDayTimeline(currentDay);
      closeEventModal();
    }

    function switchTab(tabId) {
      document.querySelectorAll('.tab-content').forEach(el => el.classList.remove('active'));
      document.querySelectorAll('.nav-btn').forEach(btn => btn.classList.remove('active'));

      const target = document.getElementById('tab-' + tabId);
      if (target) target.classList.add('active');

      const activeBtn = document.querySelector(`.nav-btn[data-tab="${tabId}"]`);
      if (activeBtn) {
        activeBtn.classList.add('active');
        activeBtn.scrollIntoView({ behavior: 'smooth', inline: 'center', block: 'nearest' });
      }

      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    const themeToggleBtn = document.getElementById('themeToggle');
    const themeIcon = document.getElementById('themeIcon');
    function applyTheme(theme) {
      if (theme === 'dark') {
        document.documentElement.setAttribute('data-theme', 'dark');
        if (themeIcon) themeIcon.textContent = '🌙';
      } else {
        document.documentElement.removeAttribute('data-theme');
        if (themeIcon) themeIcon.textContent = '☀️';
      }
      try { localStorage.setItem('shikoku_theme', theme); } catch(e){}
    }
    const savedTheme = localStorage.getItem('shikoku_theme');
    applyTheme(savedTheme || (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light'));
    if (themeToggleBtn) {
      themeToggleBtn.addEventListener('click', () => {
        applyTheme(document.documentElement.getAttribute('data-theme') === 'dark' ? 'light' : 'dark');
      });
    }

    let expenses = [];
    try {
      expenses = JSON.parse(localStorage.getItem('shikoku_expenses')) || [
        { id: 1, name: '阿卡將尿布與濕紙巾', amount: 3200, category: '🛍️ 購物' },
        { id: 2, name: '讚岐麵業 兵庫町本店', amount: 4800, category: '🍽️ 餐飲' }
      ];
    } catch(e) { expenses = []; }

    function saveAndRenderExpenses() {
      try { localStorage.setItem('shikoku_expenses', JSON.stringify(expenses)); } catch(e){}
      const listEl = document.getElementById('expenseList');
      if (!listEl) return;
      listEl.innerHTML = '';
      let total = 0;
      expenses.forEach(item => {
        total += Number(item.amount);
        const div = document.createElement('div');
        div.className = 'list-item-box';
        div.innerHTML = `
          <div style="flex: 1;">
            <div style="font-weight: 700;">${item.name}</div>
            <div style="font-size: 0.8rem; color: var(--text-muted);">${item.category}</div>
          </div>
          <div style="display: flex; align-items: center; gap: 8px;">
            <div style="font-weight: 900; font-size: 1.05rem;">¥${Number(item.amount).toLocaleString()}</div>
            <button class="btn-icon btn-edit" onclick="openEditExpenseModal(${item.id})">✏️</button>
            <button class="btn-icon btn-delete" onclick="deleteExpense(${item.id})">✕</button>
          </div>
        `;
        listEl.appendChild(div);
      });
      const jpyEl = document.getElementById('totalJpy');
      const twdEl = document.getElementById('totalTwd');
      if (jpyEl) jpyEl.textContent = '¥' + total.toLocaleString();
      if (twdEl) twdEl.textContent = 'NT$ ' + Math.round(total * 0.22).toLocaleString();
    }

    function addExpense() {
      const name = document.getElementById('expenseName').value.trim();
      const amount = document.getElementById('expenseAmount').value;
      const category = document.getElementById('expenseCategory').value;
      if (!name || !amount) { alert('請填寫品項名稱與金額！'); return; }
      expenses.unshift({ id: Date.now(), name, amount: Number(amount), category });
      document.getElementById('expenseName').value = '';
      document.getElementById('expenseAmount').value = '';
      saveAndRenderExpenses();
    }

    function deleteExpense(id) {
      if (confirm('確定要刪除這筆記帳嗎？')) {
        expenses = expenses.filter(x => x.id !== id);
        saveAndRenderExpenses();
      }
    }

    function clearExpenses() {
      if (confirm('確定要清空所有記帳項目嗎？')) { expenses = []; saveAndRenderExpenses(); }
    }

    function openEditExpenseModal(id) {
      const item = expenses.find(x => x.id === id);
      if (!item) return;
      document.getElementById('editExpenseId').value = item.id;
      document.getElementById('editExpenseName').value = item.name;
      document.getElementById('editExpenseAmount').value = item.amount;
      document.getElementById('editExpenseCategory').value = item.category;
      document.getElementById('editExpenseModal').classList.add('open');
    }
    function closeEditModal() { document.getElementById('editExpenseModal').classList.remove('open'); }
    function saveEditedExpense() {
      const id = Number(document.getElementById('editExpenseId').value);
      const name = document.getElementById('editExpenseName').value.trim();
      const amount = document.getElementById('editExpenseAmount').value;
      const category = document.getElementById('editExpenseCategory').value;
      if (!name || !amount) { alert('請填寫完整資訊！'); return; }
      const idx = expenses.findIndex(x => x.id === id);
      if (idx !== -1) {
        expenses[idx].name = name;
        expenses[idx].amount = Number(amount);
        expenses[idx].category = category;
        saveAndRenderExpenses();
        closeEditModal();
      }
    }

    let todos = [];
    try {
      todos = JSON.parse(localStorage.getItem('shikoku_todos')) || [
        { id: 1, text: '辦理台灣駕照日文譯本（攜帶正本）', done: true },
        { id: 2, text: '確認 TOYOTA 8人座休旅車與汽座', done: true },
        { id: 3, text: '準備幼兒隨身保溫水壺與食物剪刀', done: false },
        { id: 4, text: '準備金刀比羅宮專用人體工學背巾', done: false }
      ];
    } catch(e) { todos = []; }

    const extraTodos = [
      { id: 101, text: '行前一天與出發當天早上：查三豊市「林道 豊中七宝山線」是否通行（天空鳥居）', done: false },
      { id: 102, text: '查父母濱 12/24 退潮時間、風向與日落（氣象廳潮位／三豊市觀光交流局）', done: false },
      { id: 103, text: '預約：12/24 海鮮鍋物、12/25 Ito Loin 包廂、12/26 一鶴、12/27 焼肉正（說明有幼童）', done: false },
      { id: 104, text: '確認四國水族館冬季營業時間與維護休館、海豚秀時間', done: false },
      { id: 105, text: '確認 さぬきこどもの国 12/28 開園（冬休期間無休，官網再確認）', done: false },
      { id: 106, text: '向 KOKO HOTEL 確認特約停車場可停 8 人座車（限高）', done: false },
      { id: 107, text: '防寒備品：暖暖包、幼兒帽子手套、備用衣褲鞋襪（父母濱與屋島）', done: false }
    ];
    extraTodos.forEach(t => { if (!todos.some(x => x.id === t.id)) todos.push(t); });

    function saveAndRenderTodos() {
      try { localStorage.setItem('shikoku_todos', JSON.stringify(todos)); } catch(e){}
      const listEl = document.getElementById('todoList');
      if (!listEl) return;
      listEl.innerHTML = '';
      todos.forEach(item => {
        const div = document.createElement('div');
        div.className = 'list-item-box';
        div.innerHTML = `
          <div style="display: flex; align-items: center; gap: 10px; flex: 1;">
            <input type="checkbox" class="todo-checkbox" ${item.done ? 'checked' : ''} onchange="toggleTodo(${item.id})">
            <span class="${item.done ? 'todo-done' : ''}">${item.text}</span>
          </div>
          <button class="btn-icon btn-delete" onclick="deleteTodo(${item.id})">✕</button>
        `;
        listEl.appendChild(div);
      });
    }

    function addTodo() {
      const input = document.getElementById('newTodoInput');
      const text = input ? input.value.trim() : '';
      if (!text) return;
      todos.push({ id: Date.now(), text, done: false });
      input.value = '';
      saveAndRenderTodos();
    }
    function toggleTodo(id) {
      const item = todos.find(x => x.id === id);
      if (item) item.done = !item.done;
      saveAndRenderTodos();
    }
    function deleteTodo(id) {
      todos = todos.filter(x => x.id !== id);
      saveAndRenderTodos();
    }


    /* ============================================================
       航班與住宿動態管理 (支援自訂編輯、備註與 localStorage)
       ============================================================ */
    const defaultFlightHotel = [
      {
        id: 1,
        title: "🛫 星宇航空 去程 JX300",
        badge: "台中直飛",
        color: "blue",
        mainInfo: "12/23 (三) 08:50 台中清泉崗 (RMQ) ➔ 12:20 高松機場 (TAK)",
        memo: "出關後至 1F 國際線大廳 TOYOTA 櫃台搭接駁車 3 分鐘取 8 人座車。備妥全家護照、駕照日文譯本正本。",
        mapQuery: "Takamatsu Airport"
      },
      {
        id: 2,
        title: "🛬 星宇航空 回程 JX301",
        badge: "滿載而歸",
        color: "coral",
        mainInfo: "12/28 (一) 13:20 高松機場 (TAK) ➔ 15:40 台中清泉崗 (RMQ)",
        memo: "最晚 10:25 於機場旁加油站加滿 Regular 紅色油槍，保留發票收據，10:40 前至 TOYOTA 完成還車，11:00 抵達航廈報到（國際線建議最晚 11:20 前報到）。",
        mapQuery: "Gas Station Takamatsu Airport"
      },
      {
        id: 3,
        title: "🏨 KOKO HOTEL 高松 (瓦町)",
        badge: "5 晚連住",
        color: "yellow",
        mainInfo: "地址：〒760-0052 香川縣高松市瓦町 2-2-3 ｜ 電話：087-832-7111",
        memo: "下樓步行 3 分鐘即達瓦町 FLAG (阿卡將 5F) 與琴電瓦町站。特約停車場：瓦町丸い亀さん (24H 1,200日圓)、Grand Parking (18H 1,000日圓)，退房或出庫前請先至飯店櫃台蓋章折抵。",
        mapQuery: "KOKO HOTEL Takamatsu"
      },
      {
        id: 4,
        title: "🚗 8 人座車停車提醒",
        badge: "入庫前確認",
        color: "green",
        mainInfo: "立體或機械式停車場常有限高，8 人座車高約 1.9–2 公尺",
        memo: "入住時請飯店確認哪一座特約停車場可以停。Day 1 先到栗林公園再入住，行李會暫留車內，請上鎖並勿外露。",
        mapQuery: "KOKO HOTEL Takamatsu"
      },
      {
        id: 5,
        title: "📝 備案：わら家 (Waraya) 釜揚烏龍",
        badge: "已從午餐移除",
        color: "yellow",
        mainInfo: "屋島山腳，營業 9:30–17:30，年中無休，午餐時段平日也要排隊",
        memo: "原本 Day 2 午餐在わら家、下午又回屋島，會多跑一趟約 40 分。現在屋島只排在 Day 4 傍晚。若仍想吃，可在 Day 4 把 15:10 出發提早到 14:30，先到わら家吃熱湯麵再上山。",
        mapQuery: "Waraya Yashima"
      }
    ];

    let flightHotelList = JSON.parse(localStorage.getItem('shikoku_flight_hotel_v2')) || defaultFlightHotel;

    function renderFlightHotelList() {
      const container = document.getElementById('flightHotelContainer');
      if (!container) return;
      container.innerHTML = '';

      flightHotelList.forEach((item, index) => {
        const card = document.createElement('div');
        card.className = `book-card ${item.color || 'blue'}`;
        card.style.position = 'relative';

        const mapBtn = item.mapQuery ? `
          <a class="action-sub-pill" href="https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(item.mapQuery)}" target="_blank" rel="noopener">
            📍 地圖
          </a>
        ` : '';

        card.innerHTML = `
          <div class="card-title" style="justify-content: space-between; align-items: flex-start;">
            <div style="display: flex; align-items: center; gap: 8px; flex-wrap: wrap;">
              <span>${item.title}</span>
              ${item.badge ? `<span class="badge">${item.badge}</span>` : ''}
            </div>
            <button class="action-sub-pill" style="margin-left: auto; flex-shrink: 0;" onclick="openEditFlightHotelModal(${index})">
              ✏️ 編輯
            </button>
          </div>
          <p style="font-weight: 700; font-size: 0.98rem; margin-bottom: 6px; color: var(--text-main);">
            ${item.mainInfo || ''}
          </p>
          <p style="font-size: 0.88rem; color: var(--text-muted); line-height: 1.5; white-space: pre-wrap; margin-bottom: 10px;">
            ${item.memo || ''}
          </p>
          <div style="display: flex; gap: 8px; justify-content: flex-end;">
            ${mapBtn}
          </div>
        `;
        container.appendChild(card);
      });
    }

    function openEditFlightHotelModal(index) {
      const item = flightHotelList[index];
      if (!item) return;

      document.getElementById('flightHotelModalTitle').textContent = '✏️ 編輯航班 / 住宿';
      document.getElementById('fhIndex').value = index;
      document.getElementById('fhTitle').value = item.title || '';
      document.getElementById('fhBadge').value = item.badge || '';
      document.getElementById('fhColor').value = item.color || 'blue';
      document.getElementById('fhMainInfo').value = item.mainInfo || '';
      document.getElementById('fhMemo').value = item.memo || '';
      document.getElementById('fhMapQuery').value = item.mapQuery || '';
      document.getElementById('btnDeleteFh').style.display = 'block';

      document.getElementById('editFlightHotelModal').classList.add('open');
    }

    function openAddFlightHotelModal() {
      document.getElementById('flightHotelModalTitle').textContent = '＋ 新增航班 / 住宿備註';
      document.getElementById('fhIndex').value = -1;
      document.getElementById('fhTitle').value = '📝 新增備註項目';
      document.getElementById('fhBadge').value = '重要提醒';
      document.getElementById('fhColor').value = 'yellow';
      document.getElementById('fhMainInfo').value = '';
      document.getElementById('fhMemo').value = '';
      document.getElementById('fhMapQuery').value = '';
      document.getElementById('btnDeleteFh').style.display = 'none';

      document.getElementById('editFlightHotelModal').classList.add('open');
    }

    function closeFlightHotelModal() {
      document.getElementById('editFlightHotelModal').classList.remove('open');
    }

    function saveFlightHotelItem() {
      const index = parseInt(document.getElementById('fhIndex').value);
      const title = document.getElementById('fhTitle').value.trim();
      const badge = document.getElementById('fhBadge').value.trim();
      const color = document.getElementById('fhColor').value;
      const mainInfo = document.getElementById('fhMainInfo').value.trim();
      const memo = document.getElementById('fhMemo').value.trim();
      const mapQuery = document.getElementById('fhMapQuery').value.trim();

      if (!title) {
        alert('請填寫卡片標題！');
        return;
      }

      const itemData = {
        id: index >= 0 && flightHotelList[index] ? flightHotelList[index].id : Date.now(),
        title,
        badge,
        color,
        mainInfo,
        memo,
        mapQuery
      };

      if (index === -1) {
        flightHotelList.push(itemData);
      } else {
        flightHotelList[index] = itemData;
      }

      localStorage.setItem('shikoku_flight_hotel_v2', JSON.stringify(flightHotelList));
      renderFlightHotelList();
      closeFlightHotelModal();
    }

    function deleteFlightHotelItem() {
      const index = parseInt(document.getElementById('fhIndex').value);
      if (index >= 0) {
        if (confirm('確定要刪除這張卡片嗎？')) {
          flightHotelList.splice(index, 1);
          localStorage.setItem('shikoku_flight_hotel_v2', JSON.stringify(flightHotelList));
          renderFlightHotelList();
          closeFlightHotelModal();
        }
      }
    }


    /* ============================================================
       購物清單（可展開店家卡、勾選、商品編號複製、跳到當天行程）
       ============================================================ */
    const defaultShops = [
      {
        id: 1, name: "阿卡將本舖", place: "瓦町 FLAG 5F", day: 1,
        mapQuery: "Akachan Honpo KAWARAMACHI FLAG", open: true,
        tip: "營業時間請現場確認；備好護照。先買 Day 2、Day 4 吹風會用到的保暖品。",
        items: [
          { id: 11, name: "保暖發熱衣", cat: "衣物", price: "", desc: "幼童保暖內層，父母濱與屋島風大時使用", code: "", url: "", img: "", done: false },
          { id: 12, name: "副食品米餅", cat: "食品", price: "", desc: "車上與午睡前點心", code: "", url: "", img: "", done: false },
          { id: 13, name: "尿布與濕紙巾", cat: "日用品", price: "", desc: "備用量，避免旅程中斷貨", code: "", url: "", img: "", done: false }
        ]
      },
      {
        id: 2, name: "中野うどん学校 琴平校", place: "琴平町 796", day: 5,
        mapQuery: "Nakano Udon School Kotohira", open: false,
        tip: "用餐後在店內採買伴手禮。",
        items: [
          { id: 21, name: "和三盆糖", cat: "伴手禮", price: "", desc: "香川名產", code: "", url: "", img: "", done: false }
        ]
      },
      {
        id: 3, name: "高松機場 免稅店", place: "出境後", day: 6,
        mapQuery: "Takamatsu Airport", open: false,
        tip: "還車後預留時間；退稅與規定以店內公告為準。",
        items: []
      }
    ];
    let shops = [];
    try { shops = JSON.parse(localStorage.getItem('shikoku_shop_v1')) || JSON.parse(JSON.stringify(defaultShops)); }
    catch (e) { shops = JSON.parse(JSON.stringify(defaultShops)); }

    function saveShops() { try { localStorage.setItem('shikoku_shop_v1', JSON.stringify(shops)); } catch (e) {} }
    function closeModalById(id) { document.getElementById(id).classList.remove('open'); }
    function safeUrl(u) { return /^https?:\/\//i.test(u || '') ? u : ''; }

    function renderShops() {
      const box = document.getElementById('shopContainer');
      if (!box) return;
      box.innerHTML = '';
      let done = 0, total = 0, left = 0;
      shops.forEach((shop, si) => {
        const items = shop.items || [];
        const d = items.filter(i => i.done).length;
        items.forEach(i => { total++; if (i.done) done++; else left += Number(i.price) || 0; });

        const card = document.createElement('div');
        card.className = 'shop-card' + (shop.open ? '' : ' collapsed');
        const sub = [shop.place, shop.day ? `Day ${shop.day}` : ''].filter(Boolean).join(' · ');

        let listHtml = '';
        const cats = [];
        items.forEach(i => { const c = i.cat || '其他'; if (!cats.includes(c)) cats.push(c); });
        cats.forEach(c => {
          listHtml += `<div class="shop-cat"><i></i>${esc(c)}</div>`;
          items.forEach((it, ii) => {
            if ((it.cat || '其他') !== c) return;
            const img = safeUrl(it.img)
              ? `<img class="shop-img" src="${esc(it.img)}" alt="" loading="lazy">`
              : `<div class="shop-img">🛍️</div>`;
            const price = it.price !== '' && it.price != null && !isNaN(Number(it.price))
              ? `<div class="shop-price">¥${Number(it.price).toLocaleString()}</div>` : '';
            const code = it.code ? `<button class="shop-code" onclick="copyCode(this, '${esc(it.code).replace(/'/g, '')}')">編號 ${esc(it.code)}</button>` : '';
            const url = safeUrl(it.url) ? `<a class="action-sub-pill" href="${esc(it.url)}" target="_blank" rel="noopener">官網</a>` : '';
            listHtml += `
              <div class="shop-item ${it.done ? 'done' : ''}">
                <input type="checkbox" class="shop-cb" ${it.done ? 'checked' : ''} onchange="toggleShopItem(${si}, ${ii})">
                ${img}
                <div class="shop-info">
                  <div class="shop-item-name">${esc(it.name)}</div>
                  <div class="shop-item-cat">${esc(it.cat || '其他')}</div>
                  ${price}
                  ${it.desc ? `<div class="shop-desc">${esc(it.desc)}</div>` : ''}
                  <div>${code}</div>
                  <div class="shop-item-actions">${url}<button class="action-sub-pill" onclick="openShopItemModal(${si}, ${ii})">✏️ 編輯</button></div>
                </div>
              </div>`;
          });
        });
        if (!items.length) listHtml = `<div style="padding: 14px; color: var(--text-muted); font-size: 0.85rem; font-weight: 700;">還沒有商品，點下方「新增商品」。</div>`;

        card.innerHTML = `
          <div class="shop-head" onclick="toggleShop(${si})">
            <div class="shop-logo">${esc((shop.name || '店').charAt(0))}</div>
            <div class="shop-title-wrap">
              <div class="shop-name">${esc(shop.name)}</div>
              <div class="shop-sub">${esc(sub)}</div>
            </div>
            <span class="shop-progress">${d}/${items.length}</span>
            <span class="shop-arrow">▲</span>
          </div>
          <div class="shop-body">
            <div class="shop-intro">
              ${shop.tip ? `<div class="shop-tip">${esc(shop.tip)}</div>` : ''}
              <div class="shop-btn-row">
                <a class="shop-btn blue" href="https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(shop.mapQuery || shop.name)}" target="_blank" rel="noopener">📍 Google 地圖</a>
                ${shop.day ? `<button class="shop-btn" onclick="goToDay(${shop.day})">🗓️ 看 Day ${shop.day} 行程</button>` : ''}
              </div>
            </div>
            ${listHtml}
            <div class="shop-foot">
              <button class="shop-btn" onclick="openShopItemModal(${si}, -1)">＋ 新增商品</button>
              <button class="shop-btn" onclick="openShopModal(${si})">✏️ 編輯店家</button>
            </div>
          </div>`;
        box.appendChild(card);
      });
      const n = document.getElementById('shopDoneNum');
      const l = document.getElementById('shopLeftPrice');
      if (n) n.textContent = `${done}/${total}`;
      if (l) l.textContent = '¥' + left.toLocaleString();
    }

    function toggleShop(si) { shops[si].open = !shops[si].open; saveShops(); renderShops(); }
    function toggleShopItem(si, ii) { shops[si].items[ii].done = !shops[si].items[ii].done; saveShops(); renderShops(); }

    function goToDay(day) {
      switchTab('schedule');
      const el = document.querySelectorAll('.day-selector-card')[day - 1];
      if (el) selectDay(day, el);
    }

    function copyCode(btn, code) {
      const old = btn.textContent;
      const done = () => { btn.textContent = '已複製 ✓'; setTimeout(() => { btn.textContent = old; }, 1200); };
      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(code).then(done).catch(() => fallbackCopy(code, done));
      } else { fallbackCopy(code, done); }
    }
    function fallbackCopy(text, cb) {
      const ta = document.createElement('textarea');
      ta.value = text; document.body.appendChild(ta); ta.select();
      try { document.execCommand('copy'); } catch (e) {}
      document.body.removeChild(ta); cb();
    }

    function openShopModal(si) {
      const shop = si >= 0 ? shops[si] : { name: '', place: '', day: 0, mapQuery: '', tip: '' };
      document.getElementById('shopModalTitle').textContent = si >= 0 ? '✏️ 編輯店家' : '＋ 新增店家';
      document.getElementById('shopIdx').value = si;
      document.getElementById('shopName').value = shop.name;
      document.getElementById('shopPlace').value = shop.place || '';
      document.getElementById('shopDay').value = String(shop.day || 0);
      document.getElementById('shopMap').value = shop.mapQuery || '';
      document.getElementById('shopTip').value = shop.tip || '';
      document.getElementById('btnDeleteShop').style.display = si >= 0 ? 'block' : 'none';
      document.getElementById('shopModal').classList.add('open');
    }
    function saveShop() {
      const si = parseInt(document.getElementById('shopIdx').value);
      const name = document.getElementById('shopName').value.trim();
      if (!name) { alert('請填寫店名！'); return; }
      const data = {
        name,
        place: document.getElementById('shopPlace').value.trim(),
        day: parseInt(document.getElementById('shopDay').value) || 0,
        mapQuery: document.getElementById('shopMap').value.trim() || name,
        tip: document.getElementById('shopTip').value.trim()
      };
      if (si >= 0) { Object.assign(shops[si], data); }
      else { shops.push({ id: Date.now(), open: true, items: [], ...data }); }
      saveShops(); renderShops(); closeModalById('shopModal');
    }
    function deleteShop() {
      const si = parseInt(document.getElementById('shopIdx').value);
      if (si >= 0 && confirm('確定要刪除這間店與所有商品嗎？')) {
        shops.splice(si, 1); saveShops(); renderShops(); closeModalById('shopModal');
      }
    }

    function openShopItemModal(si, ii) {
      const it = ii >= 0 ? shops[si].items[ii] : { name: '', cat: '', price: '', desc: '', code: '', url: '', img: '' };
      document.getElementById('shopItemModalTitle').textContent = ii >= 0 ? '✏️ 編輯商品' : '＋ 新增商品';
      document.getElementById('itemShopIdx').value = si;
      document.getElementById('itemIdx').value = ii;
      document.getElementById('itemName').value = it.name;
      document.getElementById('itemCat').value = it.cat || '';
      document.getElementById('itemPrice').value = it.price;
      document.getElementById('itemDesc').value = it.desc || '';
      document.getElementById('itemCode').value = it.code || '';
      document.getElementById('itemUrl').value = it.url || '';
      document.getElementById('itemImg').value = it.img || '';
      document.getElementById('btnDeleteItem').style.display = ii >= 0 ? 'block' : 'none';
      document.getElementById('shopItemModal').classList.add('open');
    }
    function saveShopItem() {
      const si = parseInt(document.getElementById('itemShopIdx').value);
      const ii = parseInt(document.getElementById('itemIdx').value);
      const name = document.getElementById('itemName').value.trim();
      if (!name) { alert('請填寫商品名稱！'); return; }
      const data = {
        name,
        cat: document.getElementById('itemCat').value.trim() || '其他',
        price: document.getElementById('itemPrice').value,
        desc: document.getElementById('itemDesc').value.trim(),
        code: document.getElementById('itemCode').value.trim(),
        url: document.getElementById('itemUrl').value.trim(),
        img: document.getElementById('itemImg').value.trim()
      };
      if (ii >= 0) { Object.assign(shops[si].items[ii], data); }
      else { shops[si].items.push({ id: Date.now(), done: false, ...data }); }
      saveShops(); renderShops(); closeModalById('shopItemModal');
    }
    function deleteShopItem() {
      const si = parseInt(document.getElementById('itemShopIdx').value);
      const ii = parseInt(document.getElementById('itemIdx').value);
      if (ii >= 0 && confirm('確定要刪除這項商品嗎？')) {
        shops[si].items.splice(ii, 1); saveShops(); renderShops(); closeModalById('shopItemModal');
      }
    }

    document.addEventListener('DOMContentLoaded', () => {
      renderFlightHotelList();
      renderShops();
      renderDayTimeline(1);
      saveAndRenderExpenses();
      saveAndRenderTodos();
    });
  </script>
</body>
</html>
