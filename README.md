[life-os-2026 (1).html](https://github.com/user-attachments/files/26627008/life-os-2026.1.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>My 2026 Life OS</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<script src="https://accounts.google.com/gsi/client" async defer></script>
<style>
:root {
  --bg: #F5F0E8;
  --surface: #FDFAF5;
  --surface2: #F0EBE0;
  --border: #E2D9C8;
  --gold: #B8892A;
  --gold-light: #D4A84B;
  --teal: #2B5F52;
  --teal-light: #3D7A6A;
  --rose: #C1544A;
  --text: #1C1510;
  --text2: #6B5E4E;
  --text3: #9C8E7E;
  --white: #FFFFFF;
  --shadow: 0 2px 16px rgba(28,21,16,0.08);
  --shadow-lg: 0 8px 32px rgba(28,21,16,0.12);
  --radius: 16px;
  --radius-sm: 10px;
  --nav-h: 64px;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Jost',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden;}
h1,h2,h3,.serif{font-family:'Cormorant Garamond',serif;}

/* ——— SETUP / AUTH SCREENS ——— */
.splash{position:fixed;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center;background:var(--teal);z-index:9999;padding:32px;text-align:center;}
.splash.hidden{display:none;}
.splash-logo{font-family:'Cormorant Garamond',serif;font-size:clamp(42px,8vw,72px);color:#FAF5EC;font-weight:300;letter-spacing:2px;line-height:1;}
.splash-sub{color:rgba(250,245,236,0.65);font-size:13px;letter-spacing:3px;text-transform:uppercase;margin-top:8px;font-weight:400;}
.splash-divider{width:60px;height:1px;background:rgba(250,245,236,0.3);margin:32px auto;}
.splash-card{background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.15);border-radius:var(--radius);padding:32px;max-width:420px;width:100%;}
.splash h2{color:#FAF5EC;font-size:22px;font-weight:400;margin-bottom:8px;}
.splash p{color:rgba(250,245,236,0.7);font-size:14px;line-height:1.6;margin-bottom:24px;}
.splash label{display:block;color:rgba(250,245,236,0.85);font-size:12px;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:8px;text-align:left;}
.splash input{width:100%;background:rgba(255,255,255,0.1);border:1px solid rgba(255,255,255,0.2);border-radius:8px;padding:12px 16px;color:#FAF5EC;font-family:'Jost',sans-serif;font-size:14px;outline:none;margin-bottom:16px;transition:.2s;}
.splash input:focus{border-color:rgba(250,245,236,0.5);background:rgba(255,255,255,0.15);}
.splash input::placeholder{color:rgba(250,245,236,0.35);}
.btn-primary{width:100%;background:var(--gold-light);color:var(--text);border:none;border-radius:8px;padding:14px 24px;font-family:'Jost',sans-serif;font-size:14px;font-weight:600;letter-spacing:0.5px;cursor:pointer;transition:.2s;}
.btn-primary:hover{background:#C49A3A;transform:translateY(-1px);}
.btn-ghost{background:transparent;color:rgba(250,245,236,0.7);border:1px solid rgba(255,255,255,0.2);border-radius:8px;padding:12px 24px;font-family:'Jost',sans-serif;font-size:13px;cursor:pointer;transition:.2s;margin-top:10px;width:100%;}
.btn-ghost:hover{border-color:rgba(255,255,255,0.4);color:rgba(250,245,236,0.9);}

/* ——— APP LAYOUT ——— */
#app{display:none;min-height:100vh;}
.layout{display:flex;min-height:100vh;}
.sidebar{width:240px;background:var(--teal);position:fixed;top:0;left:0;height:100vh;overflow-y:auto;z-index:100;display:flex;flex-direction:column;transition:.3s;}
.sidebar-header{padding:28px 24px 20px;border-bottom:1px solid rgba(255,255,255,0.1);}
.sidebar-logo{font-family:'Cormorant Garamond',serif;font-size:26px;color:#FAF5EC;font-weight:300;line-height:1.2;}
.sidebar-year{font-size:11px;color:rgba(250,245,236,0.5);letter-spacing:2px;text-transform:uppercase;margin-top:2px;}
.nav-section{padding:16px 12px 8px;}
.nav-section-title{font-size:10px;letter-spacing:2px;text-transform:uppercase;color:rgba(250,245,236,0.35);padding:0 12px;margin-bottom:4px;font-weight:500;}
.nav-item{display:flex;align-items:center;gap:10px;padding:10px 12px;border-radius:8px;cursor:pointer;transition:.15s;color:rgba(250,245,236,0.7);font-size:13.5px;font-weight:400;}
.nav-item:hover{background:rgba(255,255,255,0.08);color:rgba(250,245,236,0.95);}
.nav-item.active{background:rgba(255,255,255,0.12);color:#FAF5EC;font-weight:500;}
.nav-icon{font-size:16px;width:20px;text-align:center;flex-shrink:0;}
.sidebar-user{margin-top:auto;padding:16px 20px;border-top:1px solid rgba(255,255,255,0.1);display:flex;align-items:center;gap:10px;}
.user-avatar{width:32px;height:32px;border-radius:50%;background:var(--gold);display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:600;color:var(--text);flex-shrink:0;}
.user-name{font-size:13px;color:rgba(250,245,236,0.8);flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;}
.sign-out-btn{background:none;border:none;color:rgba(250,245,236,0.4);cursor:pointer;font-size:12px;padding:4px;transition:.15s;}
.sign-out-btn:hover{color:rgba(250,245,236,0.8);}

/* ——— MAIN CONTENT ——— */
.main{margin-left:240px;min-height:100vh;padding:32px;padding-bottom:40px;}
.page{display:none;}
.page.active{display:block;}
.page-header{margin-bottom:28px;}
.page-title{font-size:clamp(28px,4vw,38px);font-weight:300;color:var(--text);letter-spacing:-0.5px;}
.page-subtitle{font-size:14px;color:var(--text3);margin-top:4px;font-weight:400;}
.month-pill{display:inline-flex;align-items:center;gap:8px;background:var(--teal);color:#FAF5EC;border:none;border-radius:24px;padding:8px 18px;font-size:13px;font-weight:500;cursor:pointer;font-family:'Jost',sans-serif;transition:.2s;}
.month-pill:hover{background:var(--teal-light);}

/* ——— CARDS ——— */
.grid{display:grid;gap:20px;}
.grid-2{grid-template-columns:repeat(2,1fr);}
.grid-3{grid-template-columns:repeat(3,1fr);}
.grid-4{grid-template-columns:repeat(4,1fr);}
.card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow);}
.card-sm{padding:16px 20px;}
.card-title{font-size:11px;letter-spacing:2px;text-transform:uppercase;color:var(--text3);font-weight:500;margin-bottom:8px;}
.card-value{font-family:'Cormorant Garamond',serif;font-size:clamp(28px,3.5vw,40px);font-weight:400;color:var(--text);}
.card-sub{font-size:12px;color:var(--text3);margin-top:4px;}
.card-accent{border-top:3px solid var(--gold);}
.card-teal{border-top:3px solid var(--teal);}
.card-rose{border-top:3px solid var(--rose);}
.stat-badge{display:inline-flex;align-items:center;gap:4px;background:var(--surface2);border-radius:20px;padding:4px 10px;font-size:11px;color:var(--text2);margin-top:8px;}
.stat-badge.green{background:#E6F4EF;color:#1E7A58;}
.stat-badge.red{background:#FDECEA;color:var(--rose);}
.stat-badge.gold{background:#FDF5E4;color:var(--gold);}

/* ——— PROGRESS BAR ——— */
.progress-wrap{background:var(--surface2);border-radius:99px;height:6px;overflow:hidden;margin:10px 0 4px;}
.progress-bar{height:100%;border-radius:99px;background:var(--gold);transition:.5s;}
.progress-bar.teal{background:var(--teal);}
.progress-bar.rose{background:var(--rose);}
.progress-bar.green{background:#3DAA78;}

/* ——— TABLE ——— */
.table-wrap{overflow-x:auto;border-radius:var(--radius-sm);border:1px solid var(--border);}
table{width:100%;border-collapse:collapse;font-size:13.5px;}
thead th{background:var(--surface2);padding:12px 16px;text-align:left;font-size:10px;letter-spacing:1.5px;text-transform:uppercase;color:var(--text3);font-weight:600;white-space:nowrap;}
tbody tr{border-top:1px solid var(--border);transition:.1s;}
tbody tr:hover{background:var(--surface2);}
tbody td{padding:12px 16px;color:var(--text);}
.status-pill{display:inline-block;border-radius:20px;padding:3px 10px;font-size:11px;font-weight:500;}
.status-ok{background:#E6F4EF;color:#1E7A58;}
.status-warn{background:#FDF5E4;color:#A07020;}
.status-over{background:#FDECEA;color:var(--rose);}
.status-none{background:var(--surface2);color:var(--text3);}

/* ——— FAB ——— */
.fab{position:fixed;bottom:24px;right:24px;background:var(--teal);color:#FAF5EC;border:none;border-radius:50%;width:56px;height:56px;font-size:24px;cursor:pointer;box-shadow:0 4px 20px rgba(43,95,82,0.4);z-index:200;transition:.2s;display:none;}
.fab:hover{background:var(--teal-light);transform:scale(1.05);}
.fab.visible{display:flex;align-items:center;justify-content:center;}

/* ——— MODAL ——— */
.modal-bg{position:fixed;inset:0;background:rgba(28,21,16,0.5);z-index:500;display:none;align-items:center;justify-content:center;padding:20px;backdrop-filter:blur(4px);}
.modal-bg.open{display:flex;}
.modal{background:var(--surface);border-radius:var(--radius);padding:28px;max-width:460px;width:100%;box-shadow:var(--shadow-lg);max-height:90vh;overflow-y:auto;}
.modal-title{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:400;margin-bottom:6px;}
.modal-sub{font-size:13px;color:var(--text3);margin-bottom:24px;}
.form-row{margin-bottom:16px;}
.form-label{display:block;font-size:11px;letter-spacing:1.5px;text-transform:uppercase;color:var(--text2);margin-bottom:6px;font-weight:500;}
.form-input,.form-select{width:100%;background:var(--bg);border:1px solid var(--border);border-radius:8px;padding:11px 14px;font-family:'Jost',sans-serif;font-size:14px;color:var(--text);outline:none;transition:.2s;appearance:none;}
.form-input:focus,.form-select:focus{border-color:var(--teal);background:var(--surface);}
.form-row-2{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
.btn-submit{background:var(--teal);color:#FAF5EC;border:none;border-radius:8px;padding:13px 24px;font-family:'Jost',sans-serif;font-size:14px;font-weight:500;cursor:pointer;width:100%;transition:.2s;margin-top:8px;}
.btn-submit:hover{background:var(--teal-light);}
.btn-cancel{background:transparent;color:var(--text3);border:1px solid var(--border);border-radius:8px;padding:13px 24px;font-family:'Jost',sans-serif;font-size:14px;cursor:pointer;width:100%;transition:.2s;margin-top:8px;}
.btn-cancel:hover{border-color:var(--text2);color:var(--text2);}

/* ——— MOBILE TOP NAV ——— */
.mobile-nav{display:none;position:fixed;bottom:0;left:0;right:0;background:var(--teal);z-index:100;padding:8px 0 12px;}
.mobile-nav-inner{display:flex;justify-content:space-around;}
.mobile-nav-item{display:flex;flex-direction:column;align-items:center;gap:3px;padding:6px 8px;cursor:pointer;color:rgba(250,245,236,0.55);font-size:10px;transition:.15s;min-width:52px;}
.mobile-nav-item.active{color:#FAF5EC;}
.mobile-nav-item .nav-icon{font-size:20px;width:auto;}

/* ——— RULES ——— */
.rule-item{display:flex;gap:16px;padding:16px 0;border-bottom:1px solid var(--border);align-items:flex-start;}
.rule-item:last-child{border-bottom:none;}
.rule-num{font-family:'Cormorant Garamond',serif;font-size:32px;font-weight:300;color:var(--gold);line-height:1;min-width:36px;text-align:right;}
.rule-text{font-size:15px;line-height:1.6;color:var(--text);padding-top:4px;}

/* ——— DAILY RHYTHM ——— */
.rhythm-item{display:flex;gap:20px;padding:12px 0;border-bottom:1px solid var(--border);align-items:flex-start;}
.rhythm-item:last-child{border-bottom:none;}
.rhythm-time{font-size:13px;font-weight:600;color:var(--teal);min-width:72px;padding-top:2px;letter-spacing:-0.2px;}
.rhythm-activity{font-size:14px;line-height:1.55;color:var(--text);}

/* ——— PLAN GRID ——— */
.plan-day{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-sm);padding:14px;transition:.15s;}
.plan-day:hover{border-color:var(--teal);box-shadow:var(--shadow);}
.plan-day-num{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:400;color:var(--gold);line-height:1;}
.plan-day-dow{font-size:10px;letter-spacing:1.5px;color:var(--text3);text-transform:uppercase;font-weight:500;}
.plan-day-content{font-size:12px;color:var(--text2);line-height:1.5;margin-top:8px;}
.plan-day-purchases{font-size:11px;color:var(--teal);font-weight:500;margin-top:6px;line-height:1.5;}
.plan-day-highlight{border-top:2px solid var(--gold-light);}

/* ——— WEALTH GOALS ——— */
.goal-item{padding:16px 0;border-bottom:1px solid var(--border);}
.goal-item:last-child{border-bottom:none;}
.goal-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:8px;}
.goal-name{font-size:14px;font-weight:500;color:var(--text);}
.goal-status{font-size:11px;padding:3px 10px;border-radius:20px;}
.goal-targets{display:flex;gap:16px;font-size:12px;color:var(--text3);margin-bottom:6px;}
.goal-pct{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:400;color:var(--text);margin-top:6px;}

/* ——— ACTIVITY LIST ——— */
.activity-month{margin-bottom:20px;}
.activity-month-title{font-size:12px;letter-spacing:2px;text-transform:uppercase;color:var(--teal);font-weight:600;margin-bottom:10px;padding-bottom:6px;border-bottom:2px solid var(--teal-light);}
.activity-item{display:flex;gap:12px;padding:10px 0;border-bottom:1px solid var(--border);align-items:flex-start;}
.activity-item:last-child{border-bottom:none;}
.activity-icon{font-size:20px;margin-top:1px;}
.activity-content{flex:1;}
.activity-name{font-size:14px;font-weight:500;color:var(--text);}
.activity-detail{font-size:12px;color:var(--text3);margin-top:2px;}
.activity-budget{font-size:12px;font-weight:600;color:var(--teal);margin-left:auto;white-space:nowrap;padding-top:2px;}

/* ——— MEAL PLAN ——— */
.meal-day-card{background:var(--surface);border:1px solid var(--border);border-radius:var(--radius-sm);padding:16px;position:relative;}
.meal-day-name{font-size:13px;font-weight:600;color:var(--teal);text-transform:uppercase;letter-spacing:1px;margin-bottom:10px;}
.meal-slot{margin-bottom:8px;}
.meal-slot-label{font-size:10px;letter-spacing:1.5px;text-transform:uppercase;color:var(--text3);font-weight:500;}
.meal-slot-val{font-size:13px;color:var(--text);line-height:1.4;}
.cook-badge{position:absolute;top:12px;right:12px;background:#E6F4EF;color:#1E7A58;font-size:10px;font-weight:600;padding:3px 8px;border-radius:20px;letter-spacing:0.5px;}

/* ——— BEAUTY CALENDAR ——— */
.beauty-item{display:flex;gap:16px;padding:14px 0;border-bottom:1px solid var(--border);align-items:flex-start;}
.beauty-item:last-child{border-bottom:none;}
.beauty-month{font-size:13px;font-weight:600;color:var(--text);min-width:72px;}
.beauty-service{font-size:14px;color:var(--text);font-weight:500;}
.beauty-detail{font-size:12px;color:var(--text3);line-height:1.5;margin-top:2px;}
.beauty-cost{font-size:13px;font-weight:600;color:var(--gold);margin-left:auto;white-space:nowrap;}

/* ——— LOADING ——— */
.spinner{width:32px;height:32px;border:2px solid var(--border);border-top-color:var(--teal);border-radius:50%;animation:spin .7s linear infinite;margin:auto;}
@keyframes spin{to{transform:rotate(360deg);}}
.loading-msg{text-align:center;padding:40px;color:var(--text3);font-size:14px;}

/* ——— TOAST ——— */
.toast{position:fixed;bottom:80px;left:50%;transform:translateX(-50%) translateY(20px);background:var(--text);color:#FAF5EC;padding:12px 24px;border-radius:24px;font-size:14px;z-index:999;opacity:0;transition:.3s;pointer-events:none;}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0);}

/* ——— SECTION TOGGLE ——— */
.tab-bar{display:flex;gap:4px;background:var(--surface2);border-radius:10px;padding:4px;margin-bottom:24px;overflow-x:auto;}
.tab{flex:1;text-align:center;padding:8px 14px;border-radius:7px;cursor:pointer;font-size:13px;font-weight:500;color:var(--text3);transition:.15s;white-space:nowrap;}
.tab.active{background:var(--white);color:var(--text);box-shadow:0 1px 6px rgba(0,0,0,0.08);}

/* ——— SCROLLBAR ——— */
::-webkit-scrollbar{width:6px;height:6px;}
::-webkit-scrollbar-track{background:transparent;}
::-webkit-scrollbar-thumb{background:var(--border);border-radius:3px;}

/* ——— RESPONSIVE ——— */
@media(max-width:900px){
  .sidebar{transform:translateX(-100%);}
  .sidebar.open{transform:translateX(0);}
  .main{margin-left:0;padding:20px 16px 100px;}
  .mobile-nav{display:block;}
  .grid-4{grid-template-columns:repeat(2,1fr);}
  .grid-3{grid-template-columns:repeat(2,1fr);}
  .fab{bottom:80px;}
  .toast{bottom:100px;}
}
@media(max-width:600px){
  .grid-2,.grid-3,.grid-4{grid-template-columns:1fr;}
}
.hamburger{display:none;position:fixed;top:16px;left:16px;z-index:200;background:var(--teal);color:#FAF5EC;border:none;border-radius:8px;width:42px;height:42px;font-size:18px;cursor:pointer;}
@media(max-width:900px){.hamburger{display:flex;align-items:center;justify-content:center;}}
.sidebar-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,0.4);z-index:99;}
.sidebar-overlay.open{display:block;}

.flex{display:flex;} .flex-between{display:flex;justify-content:space-between;align-items:center;} .gap-8{gap:8px;} .mb-16{margin-bottom:16px;} .mb-24{margin-bottom:24px;} .mt-12{margin-top:12px;} .text-right{text-align:right;} .font-serif{font-family:'Cormorant Garamond',serif;} .text-gold{color:var(--gold);} .text-teal{color:var(--teal);} .text-muted{color:var(--text3);}
</style>
</head>
<body>

<!-- ————— SETUP SCREEN ————— -->
<div class="splash" id="setup-screen">
  <div class="splash-logo">Life OS</div>
  <div class="splash-sub">2026 · Your Personal Operating System</div>
  <div class="splash-divider"></div>
  <div class="splash-card">
    <h2>Connect Google Sheets</h2>
    <p>Your data stays in your own Google Sheet — open from any device, always in sync.</p>
    <label>Google OAuth Client ID</label>
    <input type="text" id="input-client-id" placeholder="xxxx.apps.googleusercontent.com">
    <label>Google Sheet ID</label>
    <input type="text" id="input-sheet-id" placeholder="From your Sheet's URL">
    <button class="btn-primary" onclick="saveConfig()">Continue →</button>
    <button class="btn-ghost" onclick="showHelp()">How do I get these?</button>
  </div>
  <div id="help-text" style="display:none;max-width:420px;margin-top:16px;color:rgba(250,245,236,0.7);font-size:13px;line-height:1.7;text-align:left;">
    <strong style="color:rgba(250,245,236,0.9);">Step 1 · Client ID:</strong><br>
    Go to console.cloud.google.com → New Project → Enable "Google Sheets API" → Credentials → Create OAuth Client ID (Web Application) → Add your site URL to "Authorized JavaScript origins". Copy the Client ID.<br><br>
    <strong style="color:rgba(250,245,236,0.9);">Step 2 · Sheet ID:</strong><br>
    Create a Google Sheet, then copy the long ID from the URL: docs.google.com/spreadsheets/d/<u>THIS-PART</u>/edit
  </div>
</div>

<!-- ————— AUTH SCREEN ————— -->
<div class="splash hidden" id="auth-screen">
  <div class="splash-logo">Life OS</div>
  <div class="splash-sub">2026 · Your Personal Operating System</div>
  <div class="splash-divider"></div>
  <div class="splash-card">
    <h2>Sign in with Google</h2>
    <p>Sign in to access and sync your personal data with Google Sheets.</p>
    <button class="btn-primary" onclick="signIn()">Sign in with Google</button>
    <button class="btn-ghost" onclick="document.getElementById('setup-screen').classList.remove('hidden');document.getElementById('auth-screen').classList.add('hidden');">← Change settings</button>
  </div>
</div>

<!-- ————— MAIN APP ————— -->
<div id="app">
  <button class="hamburger" onclick="toggleSidebar()">☰</button>
  <div class="sidebar-overlay" id="overlay" onclick="toggleSidebar()"></div>
  <div class="layout">
    <nav class="sidebar" id="sidebar">
      <div class="sidebar-header">
        <div class="sidebar-logo">Life OS</div>
        <div class="sidebar-year">2026 · Mar – Dec</div>
      </div>
      <div class="nav-section">
        <div class="nav-section-title">Overview</div>
        <div class="nav-item active" onclick="nav('dashboard')"><span class="nav-icon">🏠</span> Dashboard</div>
        <div class="nav-item" onclick="nav('expenses')"><span class="nav-icon">💳</span> Expenses</div>
        <div class="nav-item" onclick="nav('budget')"><span class="nav-icon">💰</span> Budget</div>
        <div class="nav-item" onclick="nav('wealth')"><span class="nav-icon">📈</span> Wealth</div>
      </div>
      <div class="nav-section">
        <div class="nav-section-title">Planning</div>
        <div class="nav-item" onclick="nav('monthly')"><span class="nav-icon">📅</span> Monthly Plan</div>
        <div class="nav-item" onclick="nav('rhythm')"><span class="nav-icon">🕐</span> Daily Rhythm</div>
        <div class="nav-item" onclick="nav('meals')"><span class="nav-icon">🍽</span> Meal Plan</div>
        <div class="nav-item" onclick="nav('activities')"><span class="nav-icon">🏃</span> Activities</div>
        <div class="nav-item" onclick="nav('beauty')"><span class="nav-icon">💄</span> Beauty</div>
      </div>
      <div class="nav-section">
        <div class="nav-section-title">Rules</div>
        <div class="nav-item" onclick="nav('rules')"><span class="nav-icon">📏</span> My 10 Rules</div>
      </div>
      <div class="sidebar-user">
        <div class="user-avatar" id="user-avatar">?</div>
        <div class="user-name" id="user-name">Loading…</div>
        <button class="sign-out-btn" onclick="signOut()" title="Sign out">↩</button>
      </div>
    </nav>

    <main class="main">
      <!-- DASHBOARD -->
      <div class="page active" id="page-dashboard">
        <div class="flex-between mb-24">
          <div class="page-header" style="margin-bottom:0">
            <h1 class="page-title font-serif">Dashboard</h1>
            <p class="page-subtitle">Your financial pulse at a glance</p>
          </div>
          <button class="month-pill" onclick="changeMonth()">
            📅 <span id="selected-month-label">Mar 2026</span> ▾
          </button>
        </div>
        <div class="grid grid-4 mb-24" id="dashboard-stats"></div>
        <div class="grid grid-2 mb-24">
          <div class="card">
            <div class="card-title">Budget vs Spent · GHS</div>
            <div id="budget-chart-wrap"><canvas id="budget-chart" height="180"></canvas></div>
          </div>
          <div class="card">
            <div class="card-title">Category Breakdown</div>
            <div id="category-list" style="max-height:280px;overflow-y:auto;"></div>
          </div>
        </div>
        <div class="card">
          <div class="card-title" style="margin-bottom:16px;">Year Overview · GHS Budget vs Actual</div>
          <div id="year-overview"></div>
        </div>
      </div>

      <!-- EXPENSES -->
      <div class="page" id="page-expenses">
        <div class="flex-between mb-24">
          <div class="page-header" style="margin-bottom:0">
            <h1 class="page-title font-serif">Expense Tracker</h1>
            <p class="page-subtitle">Log every cedis — same day, 30 seconds</p>
          </div>
          <div style="display:flex;gap:8px;align-items:center;">
            <button class="month-pill" onclick="changeMonth()">📅 <span class="month-ref-label">Mar 2026</span> ▾</button>
            <button class="month-pill" style="background:var(--gold);" onclick="openExpenseModal()">+ Add</button>
          </div>
        </div>
        <div class="grid grid-4 mb-24" id="expense-stats"></div>
        <div class="card">
          <div class="card-title" style="margin-bottom:16px;">Transactions</div>
          <div class="table-wrap">
            <table>
              <thead><tr><th>Date</th><th>Category</th><th>Description</th><th style="text-align:right">Amount</th><th>Method</th></tr></thead>
              <tbody id="expense-table-body"></tbody>
            </table>
          </div>
          <div id="expense-empty" class="loading-msg" style="display:none;">No expenses logged for this month yet.</div>
        </div>
      </div>

      <!-- BUDGET -->
      <div class="page" id="page-budget">
        <div class="flex-between mb-24">
          <div class="page-header" style="margin-bottom:0">
            <h1 class="page-title font-serif">Budget</h1>
            <p class="page-subtitle">GHS · USD · GBP annual view</p>
          </div>
          <button class="month-pill" onclick="changeMonth()">📅 <span class="month-ref-label">Mar 2026</span> ▾</button>
        </div>
        <div class="tab-bar">
          <div class="tab active" onclick="switchBudgetTab('ghs',this)">GHS Budget</div>
          <div class="tab" onclick="switchBudgetTab('usd',this)">USD Budget</div>
          <div class="tab" onclick="switchBudgetTab('payment',this)">Payment Schedule</div>
        </div>
        <div id="budget-ghs"></div>
        <div id="budget-usd" style="display:none;"></div>
        <div id="budget-payment" style="display:none;"></div>
      </div>

      <!-- WEALTH -->
      <div class="page" id="page-wealth">
        <div class="page-header">
          <h1 class="page-title font-serif">Wealth Tracker</h1>
          <p class="page-subtitle">Net worth · savings goals · investments</p>
        </div>
        <div class="grid grid-3 mb-24" id="wealth-summary"></div>
        <div class="card mb-24">
          <div class="flex-between mb-16">
            <div class="card-title">Savings Goals · 2026</div>
            <button class="month-pill" style="font-size:12px;padding:6px 14px;" onclick="openWealthModal()">+ Update Month</button>
          </div>
          <div id="goals-list"></div>
        </div>
        <div class="card">
          <div class="card-title" style="margin-bottom:16px;">Monthly Net Worth</div>
          <div class="table-wrap">
            <table>
              <thead><tr><th>Month</th><th style="text-align:right">Savings (USD)</th><th style="text-align:right">Savings (GBP)</th><th style="text-align:right">Investments (GHS)</th><th style="text-align:right">Debts (USD)</th><th style="text-align:right">Net Worth</th><th>Notes</th></tr></thead>
              <tbody id="wealth-table-body"></tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- MONTHLY PLAN -->
      <div class="page" id="page-monthly">
        <div class="flex-between mb-24">
          <div class="page-header" style="margin-bottom:0">
            <h1 class="page-title font-serif">Monthly Plan</h1>
            <p class="page-subtitle">31-day template — copy and use each month</p>
          </div>
          <button class="month-pill" onclick="changeMonth()">📅 <span class="month-ref-label">Mar 2026</span> ▾</button>
        </div>
        <div id="monthly-grid"></div>
      </div>

      <!-- DAILY RHYTHM -->
      <div class="page" id="page-rhythm">
        <div class="page-header">
          <h1 class="page-title font-serif">Daily Rhythm</h1>
          <p class="page-subtitle">Built around your biology · Active 9am–5pm · Nap 5–9pm · Creative 9pm–4am</p>
        </div>
        <div class="card" style="max-width:640px;" id="rhythm-list"></div>
      </div>

      <!-- MEALS -->
      <div class="page" id="page-meals">
        <div class="page-header">
          <h1 class="page-title font-serif">Meal Plan</h1>
          <p class="page-subtitle">Cook 3×/week · Sunday · Wednesday · Friday · Fresh shop every Saturday</p>
        </div>
        <div class="grid grid-2" id="meals-grid"></div>
      </div>

      <!-- ACTIVITIES -->
      <div class="page" id="page-activities">
        <div class="page-header">
          <h1 class="page-title font-serif">Annual Activities</h1>
          <p class="page-subtitle">Every Saturday is planned · Fun is budgeted, not spontaneous</p>
        </div>
        <div id="activities-list"></div>
      </div>

      <!-- BEAUTY -->
      <div class="page" id="page-beauty">
        <div class="page-header">
          <h1 class="page-title font-serif">Beauty Calendar</h1>
          <p class="page-subtitle">Cornrows ×2/month · Quarterly dye · Annual budget: GHS 3,000</p>
        </div>
        <div class="card"><div id="beauty-list"></div></div>
      </div>

      <!-- RULES -->
      <div class="page" id="page-rules">
        <div class="page-header">
          <h1 class="page-title font-serif">My 10 Rules</h1>
          <p class="page-subtitle">Read on Day 1 of every month · These rules are your operating system</p>
        </div>
        <div class="card" style="max-width:640px;" id="rules-list"></div>
        <div style="margin-top:20px;font-family:'Cormorant Garamond',serif;font-size:20px;color:var(--text3);font-style:italic;max-width:640px;">
          You have 10 months. 10 sets of rules. One life. Make it count.
        </div>
      </div>
    </main>
  </div>

  <button class="fab" id="fab" onclick="openExpenseModal()">+</button>

  <!-- Month Picker Modal -->
  <div class="modal-bg" id="month-modal">
    <div class="modal" style="max-width:320px;">
      <div class="modal-title">Select Month</div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:16px;" id="month-picker"></div>
    </div>
  </div>

  <!-- Add Expense Modal -->
  <div class="modal-bg" id="expense-modal">
    <div class="modal">
      <div class="modal-title">Log Expense</div>
      <div class="modal-sub">Record every spend — even GHS 5 kelewele</div>
      <div class="form-row">
        <label class="form-label">Category</label>
        <select class="form-select" id="exp-category"></select>
      </div>
      <div class="form-row-2">
        <div class="form-row">
          <label class="form-label">Date</label>
          <input type="date" class="form-input" id="exp-date">
        </div>
        <div class="form-row">
          <label class="form-label">Amount (GHS)</label>
          <input type="number" class="form-input" id="exp-amount" placeholder="0.00">
        </div>
      </div>
      <div class="form-row">
        <label class="form-label">Description</label>
        <input type="text" class="form-input" id="exp-desc" placeholder="What was this for?">
      </div>
      <div class="form-row">
        <label class="form-label">Payment Method</label>
        <select class="form-select" id="exp-method">
          <option>Cash</option>
          <option>Mobile Money</option>
          <option>Bank Transfer</option>
          <option>Card</option>
        </select>
      </div>
      <div class="form-row">
        <label class="form-label">Notes (optional)</label>
        <input type="text" class="form-input" id="exp-notes" placeholder="Any extra details?">
      </div>
      <button class="btn-submit" onclick="submitExpense()">Save Expense</button>
      <button class="btn-cancel" onclick="closeModal('expense-modal')">Cancel</button>
    </div>
  </div>

  <!-- Wealth Update Modal -->
  <div class="modal-bg" id="wealth-modal">
    <div class="modal">
      <div class="modal-title">Update Wealth</div>
      <div class="modal-sub">Record your monthly balances</div>
      <div class="form-row">
        <label class="form-label">Month</label>
        <select class="form-select" id="wealth-month"></select>
      </div>
      <div class="form-row-2">
        <div class="form-row">
          <label class="form-label">Savings (USD)</label>
          <input type="number" class="form-input" id="wealth-usd" placeholder="0">
        </div>
        <div class="form-row">
          <label class="form-label">Savings (GBP)</label>
          <input type="number" class="form-input" id="wealth-gbp" placeholder="0">
        </div>
      </div>
      <div class="form-row-2">
        <div class="form-row">
          <label class="form-label">Investments (GHS)</label>
          <input type="number" class="form-input" id="wealth-ghs" placeholder="0">
        </div>
        <div class="form-row">
          <label class="form-label">Debts (USD)</label>
          <input type="number" class="form-input" id="wealth-debts" placeholder="0">
        </div>
      </div>
      <div class="form-row">
        <label class="form-label">Notes</label>
        <input type="text" class="form-input" id="wealth-notes" placeholder="Any notes for this month?">
      </div>
      <button class="btn-submit" onclick="submitWealth()">Save</button>
      <button class="btn-cancel" onclick="closeModal('wealth-modal')">Cancel</button>
    </div>
  </div>

  <!-- Mobile Bottom Nav -->
  <nav class="mobile-nav">
    <div class="mobile-nav-inner">
      <div class="mobile-nav-item active" id="mnav-dashboard" onclick="nav('dashboard')"><span class="nav-icon">🏠</span> Home</div>
      <div class="mobile-nav-item" id="mnav-expenses" onclick="nav('expenses')"><span class="nav-icon">💳</span> Expenses</div>
      <div class="mobile-nav-item" id="mnav-budget" onclick="nav('budget')"><span class="nav-icon">💰</span> Budget</div>
      <div class="mobile-nav-item" id="mnav-wealth" onclick="nav('wealth')"><span class="nav-icon">📈</span> Wealth</div>
      <div class="mobile-nav-item" id="mnav-more" onclick="toggleMoreMenu()"><span class="nav-icon">⋯</span> More</div>
    </div>
  </nav>
</div>

<!-- Toast -->
<div class="toast" id="toast"></div>

<script>
// ————————————————————————————————————————
// STATE
// ————————————————————————————————————————
let CLIENT_ID = '', SHEET_ID = '', accessToken = '';
let currentPage = 'dashboard';
let selectedMonth = 'Mar 2026';
let expenses = [];
let wealthData = [];
let isLoading = false;

const MONTHS = ['Mar 2026','Apr 2026','May 2026','Jun 2026','Jul 2026','Aug 2026','Sep 2026','Oct 2026','Nov 2026','Dec 2026'];
const MONTH_BUDGETS = {'Mar 2026':12600,'Apr 2026':12600,'May 2026':12600,'Jun 2026':14300,'Jul 2026':12600,'Aug 2026':12600,'Sep 2026':14300,'Oct 2026':12600,'Nov 2026':12600,'Dec 2026':14300};

const CATEGORIES = [
  'Rent','Family Expenses & Allowance','Electricity','Drinking Water (delivery)',
  'Water Bill (GWCL)','Fresh Groceries (weekly)','Mall Groceries (monthly)',
  'Data Bundle','Airtime','Phone Charges','Home Care','Toiletries (bulk)',
  'Health & Medication','Cleaner (Saturdays x4)','Beauty — Salon','Car Expenses',
  'Car Maintenance','Dining Out — Fufu','Dining Out — Other','Entertainment',
  'Gifts','Education Fund','Savings'
];
const BUDGETS_GHS = {
  'Rent':3000,'Family Expenses & Allowance':3000,'Electricity':500,
  'Drinking Water (delivery)':500,'Water Bill (GWCL)':100,
  'Fresh Groceries (weekly)':1200,'Mall Groceries (monthly)':500,
  'Data Bundle':250,'Airtime':150,'Phone Charges':100,'Home Care':100,
  'Toiletries (bulk)':200,'Health & Medication':200,'Cleaner (Saturdays x4)':400,
  'Beauty — Salon':300,'Car Expenses':300,'Car Maintenance':0,
  'Dining Out — Fufu':200,'Dining Out — Other':300,'Entertainment':500,
  'Gifts':150,'Education Fund':150,'Savings':500
};

// ————————————————————————————————————————
// INIT
// ————————————————————————————————————————
window.onload = () => {
  CLIENT_ID = localStorage.getItem('gos_client_id') || '';
  SHEET_ID = localStorage.getItem('gos_sheet_id') || '';
  const savedMonth = localStorage.getItem('gos_month');
  if (savedMonth && MONTHS.includes(savedMonth)) selectedMonth = savedMonth;
  
  if (CLIENT_ID && SHEET_ID) {
    document.getElementById('setup-screen').classList.add('hidden');
    document.getElementById('auth-screen').classList.remove('hidden');
  }
  
  populateSelects();
  renderStaticSections();
  initBudgetView();
};

function saveConfig() {
  CLIENT_ID = document.getElementById('input-client-id').value.trim();
  SHEET_ID = document.getElementById('input-sheet-id').value.trim();
  if (!CLIENT_ID || !SHEET_ID) { toast('Please fill in both fields'); return; }
  localStorage.setItem('gos_client_id', CLIENT_ID);
  localStorage.setItem('gos_sheet_id', SHEET_ID);
  document.getElementById('setup-screen').classList.add('hidden');
  document.getElementById('auth-screen').classList.remove('hidden');
}

function showHelp() {
  const h = document.getElementById('help-text');
  h.style.display = h.style.display === 'none' ? 'block' : 'none';
}

function signIn() {
  if (typeof google === 'undefined') {
    toast('Google Identity Services not loaded. Check your internet connection.');
    return;
  }
  const tokenClient = google.accounts.oauth2.initTokenClient({
    client_id: CLIENT_ID,
    scope: 'https://www.googleapis.com/auth/spreadsheets https://www.googleapis.com/auth/userinfo.profile',
    callback: async (resp) => {
      if (resp.error) { toast('Sign in failed: ' + resp.error); return; }
      accessToken = resp.access_token;
      await fetchUserInfo();
      await initSheet();
      document.getElementById('auth-screen').classList.add('hidden');
      document.getElementById('app').style.display = 'block';
      await loadAllData();
    }
  });
  tokenClient.requestAccessToken();
}

function signOut() {
  if (confirm('Sign out?')) {
    accessToken = ''; expenses = []; wealthData = [];
    document.getElementById('app').style.display = 'none';
    document.getElementById('auth-screen').classList.remove('hidden');
  }
}

async function fetchUserInfo() {
  try {
    const r = await fetch('https://www.googleapis.com/oauth2/v2/userinfo', {
      headers: { Authorization: `Bearer ${accessToken}` }
    });
    const u = await r.json();
    const name = u.given_name || u.name || 'User';
    document.getElementById('user-name').textContent = name;
    document.getElementById('user-avatar').textContent = name[0].toUpperCase();
  } catch(e) {}
}

// ————————————————————————————————————————
// GOOGLE SHEETS API
// ————————————————————————————————————————
async function sheetsGet(range) {
  const r = await fetch(
    `https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${encodeURIComponent(range)}`,
    { headers: { Authorization: `Bearer ${accessToken}` } }
  );
  return r.json();
}

async function sheetsUpdate(range, values) {
  await fetch(
    `https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${encodeURIComponent(range)}?valueInputOption=USER_ENTERED`,
    { method: 'PUT', headers: { Authorization: `Bearer ${accessToken}`, 'Content-Type': 'application/json' },
      body: JSON.stringify({ values }) }
  );
}

async function sheetsAppend(sheetName, values) {
  await fetch(
    `https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}/values/${encodeURIComponent(sheetName)}:append?valueInputOption=USER_ENTERED&insertDataOption=INSERT_ROWS`,
    { method: 'POST', headers: { Authorization: `Bearer ${accessToken}`, 'Content-Type': 'application/json' },
      body: JSON.stringify({ values }) }
  );
}

async function getSheetsList() {
  const r = await fetch(
    `https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}?fields=sheets.properties.title`,
    { headers: { Authorization: `Bearer ${accessToken}` } }
  );
  const d = await r.json();
  return (d.sheets || []).map(s => s.properties.title);
}

async function createSheet(title) {
  await fetch(
    `https://sheets.googleapis.com/v4/spreadsheets/${SHEET_ID}:batchUpdate`,
    { method: 'POST', headers: { Authorization: `Bearer ${accessToken}`, 'Content-Type': 'application/json' },
      body: JSON.stringify({ requests: [{ addSheet: { properties: { title } } }] }) }
  );
}

async function initSheet() {
  try {
    const sheets = await getSheetsList();
    if (!sheets.includes('Expenses')) {
      await createSheet('Expenses');
      await sheetsUpdate('Expenses!A1:G1', [['Month','Date','Category','Description','Amount (GHS)','Payment Method','Notes']]);
    }
    if (!sheets.includes('Wealth')) {
      await createSheet('Wealth');
      await sheetsUpdate('Wealth!A1:G1', [['Month','Savings (USD)','Savings (GBP)','Investments (GHS)','Debts (USD)','Net Worth','Notes']]);
    }
  } catch(e) { console.error('Sheet init error:', e); }
}

// ————————————————————————————————————————
// LOAD DATA
// ————————————————————————————————————————
async function loadAllData() {
  await Promise.all([loadExpenses(), loadWealth()]);
  renderDashboard();
  renderExpensePage();
  renderBudgetGHS();
  renderWealthPage();
  document.getElementById('fab').classList.add('visible');
}

async function loadExpenses() {
  try {
    const d = await sheetsGet('Expenses!A2:G500');
    expenses = (d.values || []).filter(r => r[0]).map(r => ({
      month: r[0]||'', date: r[1]||'', category: r[2]||'',
      description: r[3]||'', amount: parseFloat(r[4])||0,
      method: r[5]||'', notes: r[6]||''
    }));
  } catch(e) { expenses = []; }
}

async function loadWealth() {
  try {
    const d = await sheetsGet('Wealth!A2:G20');
    wealthData = (d.values || []).filter(r => r[0]).map(r => ({
      month: r[0], usd: parseFloat(r[1])||0, gbp: parseFloat(r[2])||0,
      ghs: parseFloat(r[3])||0, debts: parseFloat(r[4])||0,
      netWorth: parseFloat(r[5])||0, notes: r[6]||''
    }));
  } catch(e) { wealthData = []; }
}

function getMonthExpenses(month) {
  return expenses.filter(e => e.month === month);
}

function getMonthSpent(month) {
  return getMonthExpenses(month).reduce((s,e) => s+e.amount, 0);
}

function getCategorySpent(month, cat) {
  return getMonthExpenses(month).filter(e => e.category === cat).reduce((s,e) => s+e.amount, 0);
}

// ————————————————————————————————————————
// NAVIGATION
// ————————————————————————————————————————
function nav(page) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
  document.querySelectorAll('.mobile-nav-item').forEach(n => n.classList.remove('active'));
  document.getElementById('page-' + page).classList.add('active');
  
  document.querySelectorAll('.nav-item').forEach(n => {
    if (n.textContent.trim().toLowerCase().includes(page.substring(0,4))) n.classList.add('active');
  });
  const mn = document.getElementById('mnav-' + page);
  if (mn) mn.classList.add('active');
  
  currentPage = page;
  const showFab = ['dashboard','expenses'].includes(page);
  document.getElementById('fab').classList.toggle('visible', showFab);
  
  if (window.innerWidth <= 900) {
    document.getElementById('sidebar').classList.remove('open');
    document.getElementById('overlay').classList.remove('open');
  }
  window.scrollTo(0, 0);
}

function toggleSidebar() {
  document.getElementById('sidebar').classList.toggle('open');
  document.getElementById('overlay').classList.toggle('open');
}

function toggleMoreMenu() {
  // Build a simple overlay with more nav options
  const existing = document.getElementById('more-overlay');
  if (existing) { existing.remove(); return; }
  const div = document.createElement('div');
  div.id = 'more-overlay';
  div.style.cssText = 'position:fixed;bottom:80px;right:0;left:0;background:var(--teal);z-index:150;border-radius:16px 16px 0 0;padding:16px;';
  div.innerHTML = `
    <div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px;">
      ${[['monthly','📅','Monthly'],['rhythm','🕐','Rhythm'],['meals','🍽','Meals'],
         ['activities','🏃','Activities'],['beauty','💄','Beauty'],['rules','📏','Rules']]
        .map(([p,i,l]) => `<div onclick="nav('${p}');document.getElementById('more-overlay').remove();" style="display:flex;flex-direction:column;align-items:center;gap:4px;padding:14px 8px;cursor:pointer;color:rgba(250,245,236,0.85);font-size:12px;background:rgba(255,255,255,0.08);border-radius:10px;"><span style="font-size:22px;">${i}</span>${l}</div>`).join('')}
    </div>`;
  document.body.appendChild(div);
  setTimeout(() => document.addEventListener('click', function handler(e) {
    if (!div.contains(e.target)) { div.remove(); document.removeEventListener('click', handler); }
  }), 100);
}

// ————————————————————————————————————————
// MONTH PICKER
// ————————————————————————————————————————
function changeMonth() {
  document.getElementById('month-modal').classList.add('open');
}

function selectMonth(m) {
  selectedMonth = m;
  localStorage.setItem('gos_month', m);
  document.querySelectorAll('.month-ref-label, #selected-month-label').forEach(el => el.textContent = m);
  closeModal('month-modal');
  renderDashboard();
  renderExpensePage();
  renderBudgetGHS();
  document.querySelectorAll('.month-picker-btn').forEach(b => {
    b.style.background = b.dataset.month === m ? 'var(--gold-light)' : 'var(--surface2)';
    b.style.color = b.dataset.month === m ? 'var(--text)' : 'var(--text2)';
  });
}

document.addEventListener('DOMContentLoaded', () => {
  const mp = document.getElementById('month-picker');
  if (mp) {
    MONTHS.forEach(m => {
      const b = document.createElement('button');
      b.className = 'month-picker-btn';
      b.dataset.month = m;
      b.textContent = m;
      b.style.cssText = `background:var(--surface2);border:1px solid var(--border);border-radius:8px;padding:10px;font-family:'Jost',sans-serif;font-size:13px;cursor:pointer;transition:.15s;color:var(--text2);`;
      if (m === selectedMonth) { b.style.background = 'var(--gold-light)'; b.style.color = 'var(--text)'; }
      b.onclick = () => selectMonth(m);
      mp.appendChild(b);
    });
  }
});

function closeModal(id) {
  document.getElementById(id).classList.remove('open');
}

// ————————————————————————————————————————
// DASHBOARD
// ————————————————————————————————————————
function renderDashboard() {
  const budget = MONTH_BUDGETS[selectedMonth] || 12600;
  const spent = getMonthSpent(selectedMonth);
  const remaining = budget - spent;
  const pct = budget > 0 ? (spent/budget*100).toFixed(1) : 0;
  const ytd = expenses.reduce((s,e) => s+e.amount, 0);

  const foodSpent = ['Fresh Groceries (weekly)','Mall Groceries (monthly)'].reduce((s,c)=>s+getCategorySpent(selectedMonth,c),0);
  const diningSpent = ['Dining Out — Fufu','Dining Out — Other'].reduce((s,c)=>s+getCategorySpent(selectedMonth,c),0);
  const beautySpent = getCategorySpent(selectedMonth,'Beauty — Salon');
  const entertainmentSpent = getCategorySpent(selectedMonth,'Entertainment');

  document.getElementById('dashboard-stats').innerHTML = [
    {label:'Monthly Budget',value:'GHS '+fmt(budget),sub:selectedMonth,cls:'card-accent'},
    {label:'Total Spent',value:'GHS '+fmt(spent),sub:pct+'% of budget',cls: spent>budget ? 'card-rose' : 'card-teal'},
    {label:'Remaining',value:'GHS '+fmt(remaining),sub:remaining<0?'🚨 Over budget':'Looking good',cls:''},
    {label:'YTD Total Spent',value:'GHS '+fmt(ytd),sub:'All months combined',cls:''},
  ].map(s=>`<div class="card ${s.cls}"><div class="card-title">${s.label}</div><div class="card-value">${s.value}</div><div class="card-sub">${s.sub}</div></div>`).join('');

  const wrap = document.getElementById('category-list');
  wrap.innerHTML = CATEGORIES.map(cat => {
    const b = BUDGETS_GHS[cat]||0; const sp = getCategorySpent(selectedMonth, cat);
    if (b===0 && sp===0) return '';
    const p = b>0 ? Math.min(sp/b,1) : (sp>0?1:0);
    const status = sp>b&&b>0?'over':sp>b*0.8&&b>0?'warn':'ok';
    return `<div style="padding:8px 0;border-bottom:1px solid var(--border);">
      <div class="flex-between" style="margin-bottom:4px;">
        <span style="font-size:13px;color:var(--text)">${cat}</span>
        <span style="font-size:12px;font-weight:600;color:${status==='over'?'var(--rose)':status==='warn'?'var(--gold)':'var(--teal)'}">
          ${fmt(sp)} / ${fmt(b)}
        </span>
      </div>
      <div class="progress-wrap"><div class="progress-bar ${status==='over'?'rose':status==='warn'?'':'teal'}" style="width:${p*100}%"></div></div>
    </div>`;
  }).join('');

  const yearOverview = document.getElementById('year-overview');
  yearOverview.innerHTML = `<div class="table-wrap"><table>
    <thead><tr><th>Metric</th>${MONTHS.map(m=>`<th style="text-align:right">${m.split(' ')[0]}</th>`).join('')}<th style="text-align:right">Total</th></tr></thead>
    <tbody>
      <tr><td style="font-weight:500">Budget (GHS)</td>${MONTHS.map(m=>`<td style="text-align:right">${fmt(MONTH_BUDGETS[m])}</td>`).join('')}<td style="text-align:right;font-weight:600">${fmt(Object.values(MONTH_BUDGETS).reduce((a,b)=>a+b,0))}</td></tr>
      <tr><td style="font-weight:500">Spent (GHS)</td>${MONTHS.map(m=>`<td style="text-align:right;color:var(--text2)">${fmt(getMonthSpent(m))}</td>`).join('')}<td style="text-align:right;font-weight:600;color:var(--rose)">${fmt(ytd)}</td></tr>
      <tr><td style="font-weight:500">Remaining</td>${MONTHS.map(m=>{const r=MONTH_BUDGETS[m]-getMonthSpent(m);return`<td style="text-align:right;color:${r<0?'var(--rose)':'var(--teal)'}">${fmt(r)}</td>`;}).join('')}<td style="text-align:right;font-weight:600">${fmt(Object.values(MONTH_BUDGETS).reduce((a,b)=>a+b,0)-ytd)}</td></tr>
    </tbody></table></div>`;

  drawBudgetChart(budget, spent);
}

function drawBudgetChart(budget, spent) {
  const canvas = document.getElementById('budget-chart');
  if (!canvas) return;
  const ctx = canvas.getContext('2d');
  const W = canvas.parentElement.offsetWidth - 48;
  canvas.width = W; canvas.height = 180;
  ctx.clearRect(0, 0, W, 180);
  
  const bars = [
    {label:'Budget',val:budget,color:'#E2D9C8'},
    {label:'Spent',val:spent,color:spent>budget?'#C1544A':'#2B5F52'}
  ];
  const max = Math.max(budget, spent, 1);
  const bw = 60, gap = 40, startX = (W - (bars.length*(bw+gap)))/2;
  bars.forEach((b,i) => {
    const h = Math.max((b.val/max)*130, 2);
    const x = startX + i*(bw+gap);
    ctx.fillStyle = b.color;
    ctx.beginPath();
    ctx.roundRect(x, 160-h, bw, h, [4,4,0,0]);
    ctx.fill();
    ctx.fillStyle = '#1C1510';
    ctx.font = '500 12px Jost,sans-serif';
    ctx.textAlign = 'center';
    ctx.fillText(b.label, x+bw/2, 175);
    ctx.fillStyle = '#6B5E4E';
    ctx.font = '400 11px Jost,sans-serif';
    ctx.fillText('GHS '+fmt(b.val), x+bw/2, 155-h);
  });
}

// ————————————————————————————————————————
// EXPENSES PAGE
// ————————————————————————————————————————
function renderExpensePage() {
  const budget = MONTH_BUDGETS[selectedMonth]||12600;
  const monthExps = getMonthExpenses(selectedMonth);
  const spent = monthExps.reduce((s,e)=>s+e.amount,0);
  const remaining = budget-spent;
  const count = monthExps.length;

  document.getElementById('expense-stats').innerHTML = [
    {l:'Transactions',v:count,s:selectedMonth},
    {l:'Total Spent',v:'GHS '+fmt(spent),s:'this month'},
    {l:'Remaining',v:'GHS '+fmt(remaining),s:`of GHS ${fmt(budget)}`},
    {l:'Daily Average',v:count>0?'GHS '+fmt(Math.round(spent/new Date(selectedMonth.split(' ')[0]+'1 '+selectedMonth.split(' ')[1]).getMonth())):'-',s:'est.'},
  ].map(s=>`<div class="card card-sm"><div class="card-title">${s.l}</div><div class="card-value" style="font-size:clamp(22px,3vw,32px)">${s.v}</div><div class="card-sub">${s.s}</div></div>`).join('');

  const tbody = document.getElementById('expense-table-body');
  const empty = document.getElementById('expense-empty');
  if (monthExps.length === 0) {
    tbody.innerHTML = ''; empty.style.display = 'block';
  } else {
    empty.style.display = 'none';
    tbody.innerHTML = [...monthExps].reverse().map(e => `<tr>
      <td style="color:var(--text3)">${e.date}</td>
      <td><span class="status-pill status-none" style="font-size:11px">${e.category}</span></td>
      <td>${e.description}</td>
      <td style="text-align:right;font-weight:600">GHS ${fmt(e.amount)}</td>
      <td style="color:var(--text3)">${e.method}</td>
    </tr>`).join('');
  }
}

function openExpenseModal() {
  const today = new Date().toISOString().split('T')[0];
  document.getElementById('exp-date').value = today;
  document.getElementById('exp-amount').value = '';
  document.getElementById('exp-desc').value = '';
  document.getElementById('exp-notes').value = '';
  document.getElementById('expense-modal').classList.add('open');
}

async function submitExpense() {
  const cat = document.getElementById('exp-category').value;
  const date = document.getElementById('exp-date').value;
  const amount = parseFloat(document.getElementById('exp-amount').value);
  const desc = document.getElementById('exp-desc').value.trim();
  const method = document.getElementById('exp-method').value;
  const notes = document.getElementById('exp-notes').value.trim();
  if (!cat || !date || !amount || !desc) { toast('Please fill in all required fields'); return; }
  const monthLabel = formatMonthLabel(date);
  try {
    await sheetsAppend('Expenses', [[monthLabel, date, cat, desc, amount, method, notes]]);
    expenses.push({month:monthLabel,date,category:cat,description:desc,amount,method,notes});
    selectedMonth = monthLabel;
    closeModal('expense-modal');
    toast('✓ Expense logged');
    renderDashboard(); renderExpensePage(); renderBudgetGHS();
  } catch(e) { toast('Error saving — check your Sheet ID'); }
}

function formatMonthLabel(dateStr) {
  const d = new Date(dateStr + 'T12:00:00');
  return d.toLocaleString('en-US',{month:'short'})+' '+d.getFullYear();
}

// ————————————————————————————————————————
// BUDGET
// ————————————————————————————————————————
function initBudgetView() {
  renderBudgetGHS();
  renderBudgetUSD();
  renderPaymentSchedule();
}

function switchBudgetTab(tab, el) {
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  el.classList.add('active');
  ['ghs','usd','payment'].forEach(t => document.getElementById('budget-'+t).style.display = t===tab?'block':'none');
}

function renderBudgetGHS() {
  const el = document.getElementById('budget-ghs');
  if (!el) return;
  const rows = CATEGORIES.map(cat => {
    const b = BUDGETS_GHS[cat]||0; const sp = getCategorySpent(selectedMonth, cat);
    const rem = b-sp; const pct = b>0?(sp/b*100).toFixed(0):'-';
    const statusText = sp>b&&b>0?'🚨 Over budget':sp>b*0.8&&b>0?'⚠️ Watch it':sp>0?'✅ On track':'–';
    const cls = sp>b&&b>0?'status-over':sp>b*0.8&&b>0?'status-warn':sp>0?'status-ok':'status-none';
    return `<tr><td>${cat}</td><td style="text-align:right">${fmt(b)}</td><td style="text-align:right;font-weight:500">${fmt(sp)}</td><td style="text-align:right;color:${rem<0?'var(--rose)':'var(--text)'}">${fmt(rem)}</td><td><span class="status-pill ${cls}">${statusText}</span></td></tr>`;
  });
  const total = Object.values(BUDGETS_GHS).reduce((a,b)=>a+b,0);
  const totalSpent = getMonthSpent(selectedMonth);
  el.innerHTML = `<div class="card"><div class="flex-between mb-16"><div class="card-title">GHS MONTHLY BUDGET — ${selectedMonth}</div></div>
  <div class="table-wrap"><table>
    <thead><tr><th>Category</th><th style="text-align:right">Budget (GHS)</th><th style="text-align:right">Spent (GHS)</th><th style="text-align:right">Remaining</th><th>Status</th></tr></thead>
    <tbody>${rows.join('')}
    <tr style="font-weight:700;background:var(--surface2)"><td>TOTAL</td><td style="text-align:right">${fmt(total)}</td><td style="text-align:right;color:${totalSpent>total?'var(--rose)':'inherit'}">${fmt(totalSpent)}</td><td style="text-align:right">${fmt(total-totalSpent)}</td><td></td></tr>
    </tbody></table></div></div>`;
}

function renderBudgetUSD() {
  const el = document.getElementById('budget-usd');
  if (!el) return;
  const income = [
    {cat:'Cadana Income',monthly:2400,annual:32300},
    {cat:'Akuna Income',monthly:925,annual:9448},
    {cat:'iAdjoa Income',monthly:200,annual:2400},
    {cat:'Babe Support',monthly:200,annual:2400},
    {cat:'Family Support',monthly:50,annual:600},
    {cat:'Gifts',monthly:50,annual:600},
    {cat:'Other Income',monthly:50,annual:600},
  ];
  const expenses_usd = [
    {cat:'GHS Expenses',monthly:1260,annual:15630},
    {cat:'Cadana Savings',monthly:1000,annual:11000},
    {cat:'Travel Expenses',monthly:0,annual:2500},
    {cat:'Rent',monthly:300,annual:3600},
    {cat:'Others',monthly:100,annual:1200},
  ];
  const makeRows = (arr) => arr.map(r=>`<tr><td>${r.cat}</td><td style="text-align:right">$${fmt(r.monthly)}</td><td style="text-align:right">$${fmt(r.annual)}</td></tr>`).join('');
  el.innerHTML = `<div class="card"><div class="card-title mb-16">USD ANNUAL BUDGET 2026</div>
    <div class="table-wrap"><table>
      <thead><tr><th>Category</th><th style="text-align:right">Monthly</th><th style="text-align:right">Annual Budget</th></tr></thead>
      <tbody>
        <tr style="background:var(--surface2)"><td colspan="3" style="font-weight:700;font-size:12px;letter-spacing:1.5px;text-transform:uppercase;color:var(--teal);padding:12px 16px;">Income</td></tr>
        ${makeRows(income)}
        <tr style="font-weight:600;background:var(--surface2)"><td>Total Income</td><td style="text-align:right">$${fmt(income.reduce((s,r)=>s+r.monthly,0))}</td><td style="text-align:right">$${fmt(income.reduce((s,r)=>s+r.annual,0))}</td></tr>
        <tr style="background:var(--surface2)"><td colspan="3" style="font-weight:700;font-size:12px;letter-spacing:1.5px;text-transform:uppercase;color:var(--rose);padding:12px 16px;">Expenses</td></tr>
        ${makeRows(expenses_usd)}
        <tr style="font-weight:600;background:var(--surface2)"><td>Total Expenses</td><td style="text-align:right">$${fmt(expenses_usd.reduce((s,r)=>s+r.monthly,0))}</td><td style="text-align:right">$${fmt(expenses_usd.reduce((s,r)=>s+r.annual,0))}</td></tr>
      </tbody></table></div></div>`;
}

function renderPaymentSchedule() {
  const el = document.getElementById('budget-payment');
  if (!el) return;
  const payments = [
    {day:'Day 1','payment':'Rent','amount':'GHS 3,000','notes':'Transfer to landlord'},
    {day:'Day 1','payment':'Family allowance & expenses','amount':'GHS 3,000','notes':'Parents + family obligations'},
    {day:'Day 1','payment':'Electricity (ECG prepaid)','amount':'GHS 500','notes':'Mobile money top-up'},
    {day:'Day 1','payment':'Drinking water delivery','amount':'GHS 500','notes':'Call supplier to deliver'},
    {day:'Day 1','payment':'Data bundle (alternate months)','amount':'GHS 500 or GHS 0','notes':'Mar/May/Jul/Sep/Nov only'},
    {day:'Day 1–2','payment':'Mall grocery shopping','amount':'GHS 500','notes':'Stick to your list!'},
    {day:'Day 3','payment':'Toiletries bulk buy','amount':'GHS 200','notes':'Soap, lotion, toothpaste, sanitary'},
    {day:'Day 5–6','payment':'Salon — cornrows for wig','amount':'GHS 150','notes':'Book appointment in advance'},
    {day:'Day 9','payment':'Home care payment','amount':'GHS 100','notes':''},
    {day:'Day 14–15','payment':'Water bill (GWCL)','amount':'GHS 100','notes':'MUST be paid by Day 15'},
    {day:'Day 20–22','payment':'Salon touch-up (if needed)','amount':'GHS 100–150','notes':'Re-do if cornrows loosening'},
    {day:'Day 24','payment':'Phone charges','amount':'GHS 100','notes':''},
    {day:'Day 24','payment':'Airtime top-up','amount':'GHS 150','notes':''},
    {day:'Day 27','payment':'Final Saturday fresh groceries','amount':'GHS 300','notes':'Last weekly shop of month'},
    {day:'Jun/Sep/Dec','payment':'Car maintenance','amount':'GHS 2,000','notes':'Service + check every 3 months'},
    {day:'Day 30','payment':'Full month budget review','amount':'—','notes':'Tally all Expense Tracker entries'},
    {day:'Day 31','payment':'Transfer savings to account','amount':'Any surplus','notes':'Into savings / investment account'},
  ];
  el.innerHTML = `<div class="card"><div class="card-title mb-16">MONTHLY PAYMENT SCHEDULE</div>
    <div class="table-wrap"><table>
      <thead><tr><th>Day</th><th>Payment / Action</th><th>Amount</th><th>Notes</th></tr></thead>
      <tbody>${payments.map(p=>`<tr><td style="font-weight:600;color:var(--teal)">${p.day}</td><td>${p.payment}</td><td style="font-weight:500">${p.amount}</td><td style="color:var(--text3)">${p.notes}</td></tr>`).join('')}</tbody>
    </table></div></div>`;
}

// ————————————————————————————————————————
// WEALTH
// ————————————————————————————————————————
function renderWealthPage() {
  const goals = [
    {name:'Emergency Fund (6 months)',target:7560,saved:500,date:'Jun 2026'},
    {name:'Treasury Bill & Stocks',target:2400,saved:0,date:'Dec 2026'},
    {name:'Education Fund',target:1000,saved:0,date:'Dec 2026'},
    {name:'GBP Savings',target:5000,saved:931,date:'Dec 2026'},
    {name:'USD Savings',target:10000,saved:0,date:'Dec 2026'},
    {name:'Travel / Personal Treat',target:3000,saved:0,date:'Dec 2026'},
    {name:'Couple Savings (GBP)',target:1500,saved:160,date:'Dec 2026'},
    {name:'2025 Year Savings Close',target:6725,saved:0,date:'Dec 2026'},
    {name:'Other Savings (Loan Collection)',target:1830,saved:0,date:'Dec 2026'},
  ];
  const totalTarget = goals.reduce((s,g)=>s+g.target,0);
  const totalSaved = goals.reduce((s,g)=>s+g.saved,0);
  const latestWealth = wealthData[wealthData.length-1]||{};
  
  document.getElementById('wealth-summary').innerHTML = [
    {l:'Total Goals Target',v:'$'+fmt(totalTarget),s:'USD equiv.',cls:'card-accent'},
    {l:'Total Saved So Far',v:'$'+fmt(totalSaved),s:`${((totalSaved/totalTarget)*100).toFixed(1)}% of target`,cls:'card-teal'},
    {l:'Still Needed',v:'$'+fmt(totalTarget-totalSaved),s:'across all goals',cls:''},
  ].map(s=>`<div class="card ${s.cls}"><div class="card-title">${s.l}</div><div class="card-value">${s.v}</div><div class="card-sub">${s.s}</div></div>`).join('');

  document.getElementById('goals-list').innerHTML = goals.map(g=>{
    const pct = g.target>0?g.saved/g.target:0;
    const pctN = (pct*100).toFixed(1);
    const status = pct>=1?'✅ Complete':pct>=0.5?'🟡 Halfway':pct>0?'🔴 Behind':'🔴 Not started';
    const cls = pct>=1?'status-ok':pct>=0.5?'status-warn':'status-over';
    return `<div class="goal-item">
      <div class="goal-header">
        <div class="goal-name">${g.name}</div>
        <span class="status-pill ${cls}" style="font-size:11px">${status}</span>
      </div>
      <div class="goal-targets"><span>Target: $${fmt(g.target)}</span><span>Saved: $${fmt(g.saved)}</span><span>By: ${g.date}</span></div>
      <div class="progress-wrap"><div class="progress-bar ${pct>=1?'green':pct>=0.5?'':'rose'}" style="width:${Math.min(pct*100,100)}%"></div></div>
      <div class="goal-pct">${pctN}% complete</div>
    </div>`;
  }).join('');

  const tbody = document.getElementById('wealth-table-body');
  if (wealthData.length === 0) {
    tbody.innerHTML = MONTHS.map(m=>`<tr><td style="color:var(--text3)">${m}</td><td style="text-align:right;color:var(--text3)">—</td><td style="text-align:right;color:var(--text3)">—</td><td style="text-align:right;color:var(--text3)">—</td><td style="text-align:right;color:var(--text3)">—</td><td style="text-align:right;color:var(--text3)">—</td><td></td></tr>`).join('');
  } else {
    tbody.innerHTML = wealthData.map(w=>`<tr>
      <td style="font-weight:500">${w.month}</td>
      <td style="text-align:right">$${fmt(w.usd)}</td>
      <td style="text-align:right">£${fmt(w.gbp)}</td>
      <td style="text-align:right">GHS ${fmt(w.ghs)}</td>
      <td style="text-align:right;color:var(--rose)">$${fmt(w.debts)}</td>
      <td style="text-align:right;font-weight:600;color:var(--teal)">$${fmt(w.netWorth)}</td>
      <td style="color:var(--text3)">${w.notes}</td>
    </tr>`).join('');
  }

  // Populate wealth month select
  const sel = document.getElementById('wealth-month');
  if (sel) { sel.innerHTML = MONTHS.map(m=>`<option value="${m}">${m}</option>`).join(''); }
}

function openWealthModal() {
  document.getElementById('wealth-modal').classList.add('open');
}

async function submitWealth() {
  const month = document.getElementById('wealth-month').value;
  const usd = parseFloat(document.getElementById('wealth-usd').value)||0;
  const gbp = parseFloat(document.getElementById('wealth-gbp').value)||0;
  const ghs = parseFloat(document.getElementById('wealth-ghs').value)||0;
  const debts = parseFloat(document.getElementById('wealth-debts').value)||0;
  const notes = document.getElementById('wealth-notes').value;
  const netWorth = (usd + gbp*1.27 - debts); // rough USD equiv
  try {
    await sheetsAppend('Wealth', [[month, usd, gbp, ghs, debts, netWorth.toFixed(2), notes]]);
    wealthData.push({month,usd,gbp,ghs,debts,netWorth,notes});
    closeModal('wealth-modal');
    toast('✓ Wealth data saved');
    renderWealthPage();
  } catch(e) { toast('Error saving — check connection'); }
}

// ————————————————————————————————————————
// STATIC SECTIONS
// ————————————————————————————————————————
function renderStaticSections() {
  renderMonthlyPlan();
  renderDailyRhythm();
  renderMealPlan();
  renderActivities();
  renderBeautyCalendar();
  renderRules();
}

function renderMonthlyPlan() {
  const days = [
    {d:'Day 1',dow:'Mon',morning:'Walk 10:00–10:30am',breakfast:'Oats & milk & honey',lunch:'Waakye (buy)',purchases:'PAY Rent · Family · Electricity · Water order · Data (if data month)',highlight:true},
    {d:'Day 2',dow:'Tue',morning:'Walk 10:00–10:30am',breakfast:'Bread & fried egg',lunch:'Rice & stew (batch)',purchases:'SHOP Mall groceries GHS 500'},
    {d:'Day 3',dow:'Wed',morning:'Walk 10:00–10:30am',breakfast:'Porridge with milk',lunch:'Rice & stew',purchases:'BUY Toiletries bulk GHS 200'},
    {d:'Day 4',dow:'Thu',morning:'Rest morning',breakfast:'Tea & bread & sardines',lunch:'Kontomire & ampesi',purchases:'No spending'},
    {d:'Day 5',dow:'Fri',morning:'Walk 10:00–10:30am',breakfast:'Oats with honey',lunch:'Kontomire (finish batch)',purchases:'BOOK salon appointment'},
    {d:'Day 6',dow:'Sat',morning:'SALON — cornrows for wig',breakfast:'Egg & bread before salon',lunch:'Jollof rice',purchases:'SALON GHS 150 · GROCERIES GHS 300 · CLEANER GHS 100',highlight:true},
    {d:'Day 7',dow:'Sun',morning:'Rest — recharge',breakfast:'Porridge',lunch:'Ampesi & garden egg stew',purchases:'No spending'},
    {d:'Day 8',dow:'Mon',morning:'Walk 10:00–10:30am',breakfast:'Oats with milk',lunch:'Ampesi (Sunday batch)',purchases:'PAY Home care GHS 100'},
    {d:'Day 9',dow:'Tue',morning:'Walk 10:00–10:30am',breakfast:'Bread & sardines',lunch:'Rice & stew',purchases:'No spending'},
    {d:'Day 10',dow:'Wed',morning:'Walk 10:00–10:30am',breakfast:'Tea & bread',lunch:'Waakye (midweek treat)',purchases:'Waakye GHS 40'},
    {d:'Day 11',dow:'Thu',morning:'Rest morning',breakfast:'Oats with honey',lunch:'Kontomire & ampesi',purchases:'No spending'},
    {d:'Day 12',dow:'Fri',morning:'Walk 10:00–10:30am',breakfast:'Egg & bread',lunch:'Kontomire (finish batch)',purchases:'PREP hiking gear'},
    {d:'Day 13',dow:'Sat',morning:'🥾 HIKE 6am → Pool → Fufu',breakfast:'Light snack',lunch:'FUFU & LIGHT SOUP',purchases:'HIKE+POOL GHS 80 · FUFU GHS 120 · GROCERIES GHS 300 · CLEANER GHS 100',highlight:true},
    {d:'Day 14',dow:'Sun',morning:'REST — you earned it!',breakfast:'Tea & bread',lunch:'Banku & tilapia — cook today',purchases:'PAY Water bill GWCL GHS 100'},
    {d:'Day 15',dow:'Mon',morning:'Walk 10:00–10:30am',breakfast:'Oats with milk',lunch:'Banku (Sunday batch)',purchases:'MIDPOINT: check spending vs budget'},
    {d:'Day 16',dow:'Tue',morning:'Walk 10:00–10:30am',breakfast:'Bread & fried egg',lunch:'Rice & stew',purchases:'No spending'},
    {d:'Day 17',dow:'Wed',morning:'Walk 10:00–10:30am',breakfast:'Porridge',lunch:'Ampesi & garden egg stew',purchases:'No spending'},
    {d:'Day 18',dow:'Thu',morning:'Rest morning',breakfast:'Tea & bread',lunch:'Ampesi (Wed batch)',purchases:'No spending'},
    {d:'Day 19',dow:'Fri',morning:'Walk 10:00–10:30am',breakfast:'Oats with honey',lunch:'Fufu (last night)',purchases:'CHECK cornrows — book touch-up?'},
    {d:'Day 20',dow:'Sat',morning:'🏓 PADDLE TENNIS + BUFFET',breakfast:'Egg & bread before paddle',lunch:'POST-PADDLE BUFFET with the girls',purchases:'PADDLE GHS 80 · BUFFET GHS 180 · GROCERIES GHS 300 · CLEANER GHS 100',highlight:true},
    {d:'Day 21',dow:'Sun',morning:'Rest morning',breakfast:'Porridge',lunch:'Waakye (Sunday treat)',purchases:'No spending'},
    {d:'Day 22',dow:'Mon',morning:'Walk 10:00–10:30am',breakfast:'Oats with milk',lunch:'Kontomire (Sunday batch)',purchases:'Final stretch — no new spending'},
    {d:'Day 23',dow:'Tue',morning:'Walk 10:00–10:30am',breakfast:'Bread & sardines',lunch:'Rice & stew',purchases:'CHECK: are you on budget?'},
    {d:'Day 24',dow:'Wed',morning:'Walk 10:00–10:30am',breakfast:'Tea & bread',lunch:'Banku & okro — cook today',purchases:'PAY Phone GHS 100 · TOP-UP Airtime GHS 150'},
    {d:'Day 25',dow:'Thu',morning:'Rest morning',breakfast:'Oats with honey',lunch:'Banku (Wed batch)',purchases:'No spending'},
    {d:'Day 26',dow:'Fri',morning:'Walk 10:00–10:30am',breakfast:'Egg & bread',lunch:'Ampesi (last night)',purchases:'CONFIRM lawn tennis with the girls'},
    {d:'Day 27',dow:'Sat',morning:'🎾 LAWN TENNIS + FUFU',breakfast:'Porridge before tennis',lunch:'FUFU & LIGHT SOUP',purchases:'TENNIS GHS 80 · FUFU GHS 120 · GROCERIES GHS 300 · CLEANER GHS 100',highlight:true},
    {d:'Day 28',dow:'Sun',morning:'Rest morning',breakfast:'Tea & bread',lunch:'Rice & stew — cook today',purchases:'No spending'},
    {d:'Day 29',dow:'Mon',morning:'Walk 10:00–10:30am',breakfast:'Oats with milk',lunch:'Rice & stew (batch)',purchases:'No new spending'},
    {d:'Day 30',dow:'Tue',morning:'Walk 10:00–10:30am',breakfast:'Bread & fried egg',lunch:'Kontomire & ampesi',purchases:'📊 MONTH REVIEW — update Dashboard, log all expenses'},
    {d:'Day 31',dow:'Wed',morning:'Walk — final!',breakfast:'Porridge',lunch:'Waakye (treat)',purchases:'PLAN next month · TRANSFER savings · 🎉'},
  ];
  document.getElementById('monthly-grid').innerHTML = `<div class="grid" style="grid-template-columns:repeat(auto-fill,minmax(200px,1fr));">
    ${days.map(d=>`<div class="plan-day ${d.highlight?'plan-day-highlight':''}">
      <div class="flex-between" style="margin-bottom:6px;">
        <div class="plan-day-num">${d.d.replace('Day ','')}</div>
        <div class="plan-day-dow">${d.dow}</div>
      </div>
      <div class="plan-day-content">
        <div style="margin-bottom:4px"><strong>☀️</strong> ${d.morning}</div>
        <div style="margin-bottom:2px"><span style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:1px">Breakfast</span><br>${d.breakfast}</div>
        <div><span style="font-size:10px;color:var(--text3);text-transform:uppercase;letter-spacing:1px">Lunch</span><br>${d.lunch}</div>
      </div>
      <div class="plan-day-purchases">${d.purchases}</div>
    </div>`).join('')}
  </div>`;
}

function renderDailyRhythm() {
  const schedule = [
    {time:'9:00 AM',activity:'☀️ Wake up. Drink water immediately. Set ONE intention for the day — one thing you want to accomplish.'},
    {time:'9:15 AM',activity:'🪥 Morning freshen up / skincare. Short and consistent. 10 minutes max.'},
    {time:'9:45 AM',activity:'🍳 BREAKFAST — sit down at the table, eat properly. No screens if possible. This sets your energy for the morning.'},
    {time:'10:00 AM',activity:'🚶 MORNING WALK — 30 minutes, non-negotiable on weekdays. Even around the block. This is your movement for the day.'},
    {time:'10:30 AM',activity:'💻 Work session 1 — energised from the walk. Deep work, creative work, best projects go here.'},
    {time:'1:00 PM',activity:'🍛 LUNCH — stop work. Eat at the table, sit down properly. Rushed lunch = afternoon cravings = takeout temptation.'},
    {time:'1:30 PM',activity:'💻 Work session 2 — admin, emails, calls, follow-ups.'},
    {time:'4:00 PM',activity:'📝 Wind down. Save work. Note top 3 tasks for tonight.'},
    {time:'5:00 PM',activity:'😴 NAP — your body\'s natural rhythm. This is not laziness; it is your biology. Honour it.'},
    {time:'9:00 PM',activity:'🌙 Wake from nap. Dinner if not yet eaten. Drink water and rehydrate.'},
    {time:'9:30 PM',activity:'💻 Evening session — often your most creative and productive time. Use it for priority work.'},
    {time:'12:00 AM',activity:'🍽 Light snack if needed — fruit, tea, light bread. Keep it simple.'},
    {time:'2:00 AM',activity:'📋 Begin wrapping up. Write tomorrow\'s top 3 priorities. Review Expense Tracker if any spending today.'},
    {time:'3–4:00 AM',activity:'🛌 SLEEP. You\'ve done well. Rest.'},
  ];
  document.getElementById('rhythm-list').innerHTML = schedule.map(s=>`
    <div class="rhythm-item">
      <div class="rhythm-time">${s.time}</div>
      <div class="rhythm-activity">${s.activity}</div>
    </div>`).join('');
}

function renderMealPlan() {
  const meals = [
    {day:'Monday',cook:false,breakfast:'Oats & milk',lunch:'Marwarko Jollof',dinner:'Kenkey with protein',grocery:'Check fridge'},
    {day:'Tuesday',cook:true,breakfast:'Bread & fried egg',lunch:'Rice & stew',dinner:'Rice & stew / kelewele snack',grocery:''},
    {day:'Wednesday',cook:false,breakfast:'Koko with Koose',lunch:'Waakye with protein',dinner:'Rice & stew / kelewele',grocery:'Tomatoes, rice, chicken/fish'},
    {day:'Thursday',cook:true,breakfast:'Koko with Koose',lunch:'Waakye with protein',dinner:'Banku & okro',grocery:'Cornmeal, okro if batch done'},
    {day:'Friday',cook:false,breakfast:'Koko with Koose',lunch:'Yam and stew',dinner:'Jollof rice',grocery:'Garden eggs, kontomire, yam'},
    {day:'Saturday',cook:'shop',breakfast:'Egg & bread & coffee',lunch:'—',dinner:'Fufu & light soup (post-activity)',grocery:'🛒 WEEKLY FRESH SHOP — GHS 300'},
    {day:'Sunday',cook:true,breakfast:'Oats & milk',lunch:'Fufu with light soup',dinner:'Oat & milk',grocery:''},
  ];
  document.getElementById('meals-grid').innerHTML = meals.map(m=>`
    <div class="meal-day-card">
      <div class="meal-day-name">${m.day}</div>
      ${m.cook===true?'<span class="cook-badge">✅ COOK</span>':m.cook==='shop'?'<span class="cook-badge" style="background:#FDF5E4;color:var(--gold)">🛒 SHOP</span>':''}
      <div class="meal-slot"><div class="meal-slot-label">Breakfast</div><div class="meal-slot-val">${m.breakfast}</div></div>
      <div class="meal-slot"><div class="meal-slot-label">Lunch</div><div class="meal-slot-val">${m.lunch}</div></div>
      <div class="meal-slot"><div class="meal-slot-label">Dinner</div><div class="meal-slot-val">${m.dinner}</div></div>
      ${m.grocery?`<div class="meal-slot" style="margin-top:10px;padding-top:8px;border-top:1px solid var(--border)"><div class="meal-slot-label">Grocery</div><div class="meal-slot-val" style="color:var(--teal)">${m.grocery}</div></div>`:''}
    </div>`).join('');
}

function renderActivities() {
  const activities = {
    'MAR 2026':[
      {icon:'🚶',name:'Daily Walks (Mon–Fri)',detail:'30 min each morning at 10:00am',budget:'FREE'},
      {icon:'🥾',name:'Hike → Pool → Fufu (Sat 2)',detail:'Wake 5:30am. Hike 6–9am. Pool. Fufu lunch.',budget:'~GHS 300'},
      {icon:'🏓',name:'Paddle Tennis + Buffet (Sat 3)',detail:'Morning paddle with girls. Buffet after.',budget:'~GHS 260'},
      {icon:'🎾',name:'Lawn Tennis + Fufu (Sat 4)',detail:'Morning tennis. Fufu & light soup after.',budget:'~GHS 200'},
    ],
    'APR–NOV 2026 (monthly repeat)':[
      {icon:'🚶',name:'Daily Walks (Mon–Fri)',detail:'30 min morning walk — non-negotiable',budget:'FREE'},
      {icon:'🥾',name:'Hike → Pool → Fufu (Sat 2)',detail:'Monthly hike day',budget:'~GHS 300'},
      {icon:'🏓',name:'Paddle Tennis + Buffet (Sat 3)',detail:'Monthly paddle session',budget:'~GHS 260'},
      {icon:'🎾',name:'Lawn Tennis + Fufu (Sat 4)',detail:'Monthly tennis session',budget:'~GHS 200'},
    ],
    'SPECIAL MONTHS':[
      {icon:'🔧',name:'Car Maintenance — Jun, Sep, Dec',detail:'Service + check every 3 months',budget:'~GHS 2,000'},
      {icon:'🎉',name:'Year-End Celebration — Dec Sat 4',detail:'Dinner with partner/girls — celebrate 2026!',budget:'~GHS 400'},
      {icon:'📊',name:'YEAR-END REVIEW — Dec 31',detail:'Full 2026 wealth & budget review',budget:'FREE'},
    ]
  };
  document.getElementById('activities-list').innerHTML = Object.entries(activities).map(([month, items])=>`
    <div class="card activity-month" style="margin-bottom:20px;">
      <div class="activity-month-title">${month}</div>
      ${items.map(a=>`<div class="activity-item">
        <div class="activity-icon">${a.icon}</div>
        <div class="activity-content">
          <div class="activity-name">${a.name}</div>
          <div class="activity-detail">${a.detail}</div>
        </div>
        <div class="activity-budget">${a.budget}</div>
      </div>`).join('')}
    </div>`).join('');
}

function renderBeautyCalendar() {
  const beauty = [
    {month:'Mar 2026',service:'Rasta braids',detail:'Day 5–6: cornrows GHS 150. Day 20–22: touch-up GHS 150. Day 3: toiletries bulk GHS 200.',cost:'GHS 500'},
    {month:'Apr 2026',service:'Cornrows',detail:'Day 5–6 and Day 20–22. Same routine.',cost:'GHS 300'},
    {month:'May 2026',service:'Cornrows (×2) + Toiletries restock',detail:'Day 5–6 and Day 20–22. Toiletries restock if running low.',cost:'GHS 400'},
    {month:'Jun 2026',service:'Cornrows + Quarterly Dye 🎨',detail:'Day 5–6: dye + cornrows (treat yourself!). Day 20–22: touch-up.',cost:'GHS 500–600'},
    {month:'Jul 2026',service:'Braids',detail:'Day 5–6 and Day 20–22. Toiletries bulk restock.',cost:'GHS 500'},
    {month:'Aug 2026',service:'Cornrows',detail:'Standard month. Day 5–6 and Day 20–22.',cost:'GHS 300'},
    {month:'Sep 2026',service:'Cornrows + Quarterly Dye 🎨',detail:'Quarterly dye month. Day 5–6: dye + style. Day 20–22: touch-up.',cost:'GHS 500–600'},
    {month:'Oct 2026',service:'Braids',detail:'Day 5–6 and Day 20–22. Toiletries restock.',cost:'GHS 500'},
    {month:'Nov 2026',service:'Cornrows (×2)',detail:'Day 5–6 and Day 20–22. Standard month.',cost:'GHS 300'},
    {month:'Dec 2026',service:'Wave on ✨ + Festive Dye 🎨',detail:'December: dye + style for festive season. Treat yourself for year-end!',cost:'GHS 600–700'},
  ];
  document.getElementById('beauty-list').innerHTML = beauty.map(b=>`
    <div class="beauty-item">
      <div>
        <div class="beauty-month">${b.month}</div>
        <div class="beauty-service">${b.service}</div>
        <div class="beauty-detail">${b.detail}</div>
      </div>
      <div class="beauty-cost">${b.cost}</div>
    </div>`).join('');
}

function renderRules() {
  const rules = [
    'Pay ALL bills on Day 1 every month. The month starts clean or it does not start at all.',
    'Cook 3 times a week. If you did not cook, eat from what you cooked — not from a delivery app.',
    'Walk every weekday morning at 10am. Even 20 minutes counts. Movement is non-negotiable.',
    'Shop only on Saturdays for fresh produce. No mid-week quick runs — they kill the budget.',
    'Your Big 3 Saturday activities are already planned. No unplanned outings. Enjoy what is scheduled.',
    'Three meals a day. Every day. Skipping meals leads to takeout cravings and budget blowouts.',
    'No impulse buying. If it is not on your list, wait 48 hours. Most impulses disappear.',
    'Log every expense in the Expense Tracker — same day. Even GHS 5 kelewele. 30 seconds.',
    'On Day 30, review the month on the Dashboard. No guilt — just data. What improves next month?',
    'On Day 31, transfer savings and celebrate. You planned it. You did it. That is a win.',
  ];
  document.getElementById('rules-list').innerHTML = rules.map((r,i)=>`
    <div class="rule-item">
      <div class="rule-num">${i+1}</div>
      <div class="rule-text">${r}</div>
    </div>`).join('');
}

// ————————————————————————————————————————
// HELPERS
// ————————————————————————————————————————
function fmt(n) {
  if (n === undefined || n === null || isNaN(n)) return '0';
  return Math.abs(n).toLocaleString('en-US', {minimumFractionDigits:0, maximumFractionDigits:0});
}

function populateSelects() {
  const catSel = document.getElementById('exp-category');
  if (catSel) catSel.innerHTML = CATEGORIES.map(c=>`<option value="${c}">${c}</option>`).join('');
  const wm = document.getElementById('wealth-month');
  if (wm) wm.innerHTML = MONTHS.map(m=>`<option value="${m}">${m}</option>`).join('');
  document.querySelectorAll('.month-ref-label, #selected-month-label').forEach(el => el.textContent = selectedMonth);
}

function toast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2800);
}

// Close modals on bg click
document.querySelectorAll('.modal-bg').forEach(bg => {
  bg.addEventListener('click', e => { if (e.target === bg) bg.classList.remove('open'); });
});
</script>
</body>
</html>
