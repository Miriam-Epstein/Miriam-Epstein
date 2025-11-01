<!doctype html>
<html lang="he">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Miryam Epstein — Logo</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600;800&family=Monoton&display=swap" rel="stylesheet">

  <style>
    :root{
      --badge-blue: #0077FF;   /* labelColor */
      --badge-orange: #FF9900; /* color */
      --badge-green: #21C07A;  /* left green */
      --bg: #0f1220;
      --inner-bg: #141521;
      --glass: rgba(255,255,255,0.03);
      --accent-glow: rgba(33,192,122,0.15);
      --accent-glow-2: rgba(0,119,255,0.14);
      --text-light: #f5f7fb;
    }

    /* 기본 דף */
    html,body{
      height:100%;
      margin:0;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(33,192,122,0.05), transparent 6%),
                  radial-gradient(1000px 500px at 90% 90%, rgba(0,119,255,0.04), transparent 8%),
                  var(--bg);
      font-family: "Poppins", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:36px;
      box-sizing:border-box;
      direction: rtl; /* רקע RTL לפי הנחיה */
    }

    /* קופסה מרכזית */
    .card {
      width: min(920px, 96vw);
      max-width: 920px;
      aspect-ratio: 1.05 / 1; /* כמעט ריבוע */
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius: 28px;
      padding: 40px;
      box-sizing:border-box;
      display:grid;
      grid-template-columns: 1fr 420px;
      gap: 28px;
      align-items:center;
      box-shadow: 0 10px 40px rgba(2,6,23,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
    }

    /* צד שמאל - כיתוב גדול */
    .content {
      padding: 24px 26px;
      display:flex;
      flex-direction:column;
      gap:18px;
      align-items:flex-start;
    }

    .title {
      font-weight:800;
      font-size: clamp(40px, 7.5vw, 78px);
      line-height:0.95;
      letter-spacing: -1px;
      background: linear-gradient(90deg, var(--badge-green) 0%, var(--badge-blue) 45%, var(--badge-orange) 100%);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-transform: none;
      filter: drop-shadow(0 8px 20px rgba(0,0,0,0.6));
      display:inline-block;
      padding:4px 2px;
    }

    .subtitle {
      font-weight:600;
      font-size: clamp(12px, 2.2vw, 16px);
      color: #bfc7d7;
      background: linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      padding:8px 12px;
      border-radius: 999px;
      display:inline-flex;
      gap:10px;
      align-items:center;
      box-shadow: 0 6px 20px rgba(0,0,0,0.45), inset 0 1px 0 rgba(255,255,255,0.02);
    }

    .subtitle .pill {
      width:10px;
      height:10px;
      border-radius:50%;
      background: linear-gradient(180deg, var(--badge-green), #1aa46b);
      box-shadow: 0 0 12px rgba(33,192,122,0.6);
      flex:0 0 auto;
    }

    .desc {
      color: #9aa4be;
      font-size: 14px;
      max-width: 56ch;
    }

    /* צד ימין - עיגול לוגו */
    .logo-wrap {
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
      min-height: 360px;
    }

    .logo {
      width: 100%;
      max-width: 420px;
      aspect-ratio: 1 / 1;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 25%, rgba(255,255,255,0.02), transparent 8%),
                  linear-gradient(180deg, #0e1020 0%, #10111a 100%);
      position:relative;
      display:flex;
      align-items:center;
      justify-content:center;
      overflow:hidden;
      box-shadow: 0 30px 60px rgba(2,6,23,0.65), inset 0 1px 0 rgba(255,255,255,0.02);
    }

    /* טבעת זוהרת */
    .logo::before{
      content:'';
      position:absolute;
      inset: -6px;
      border-radius:999px;
      padding:6px;
      background: conic-gradient(from 150deg, var(--badge-green), var(--badge-green) 20%, transparent 21%, transparent 60%, var(--badge-blue) 62%, var(--badge-orange) 92%, var(--badge-green) 100%);
      -webkit-mask:
        linear-gradient(#000,#000) content-box,
        linear-gradient(#000,#000);
      -webkit-mask-composite: xor;
      mask-composite: exclude;
      filter: blur(6px) saturate(110%);
      opacity:0.95;
    }

    /* עוד טבעת פנימית דקה */
    .logo::after {
      content:'';
      position:absolute;
      inset: 22px;
      border-radius:999px;
      box-shadow: 0 0 40px var(--accent-glow), 0 0 24px var(--accent-glow-2);
      pointer-events:none;
    }

    .logo-inner {
      width: calc(100% - 60px);
      height: calc(100% - 60px);
      border-radius:50%;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(0,0,0,0.12));
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
      overflow:hidden;
    }

    /* הטקסט בתוך הלוגו (קטן יותר, כמו במסך שסיפקת) */
    .logo-text {
      text-align:center;
      color: var(--text-light);
      font-weight:800;
      font-size: clamp(16px, 3.4vw, 28px);
      letter-spacing: 0.6px;
      background: linear-gradient(90deg, rgba(255,255,255,0.9), rgba(255,255,255,0.6));
      -webkit-background-clip:text;
      background-clip:text;
      color:transparent;
      text-shadow: 0 6px 18px rgba(0,0,0,0.6);
    }

    /* אייקון פינה (כמו ביטוי לוגו) */
    .badge-row{
      display:flex;
      gap:8px;
      align-items:center;
      margin-top:6px;
    }

    .tiny-badge{
      display:inline-flex;
      gap:8px;
      align-items:center;
      padding:6px 10px;
      border-radius:999px;
      font-weight:600;
      font-size:13px;
      color:white;
      background: linear-gradient(90deg, var(--badge-blue), var(--badge-orange));
      box-shadow: 0 8px 30px rgba(0,119,255,0.12), 0 2px 8px rgba(0,0,0,0.45);
    }

    /* רספונסיב */
    @media (max-width:880px){
      .card{grid-template-columns:1fr; gap:18px; padding:22px;}
      .logo-wrap{order:-1}
      .card{aspect-ratio: auto}
      .content{align-items:center;text-align:center}
      .subtitle{justify-content:center}
    }

  </style>
</head>
<body>
  <div class="card" role="region" aria-label="Miryam Epstein logo card">
    <div class="content">
      <div class="subtitle" aria-hidden="true">
        <span class="pill" title="accent"></span>
        <span>Banner / Personal Brand</span>
      </div>

      <h1 class="title">Miryam Epstein</h1>

      <p class="desc">
        מעיצוב לוגו מודרני ועד פרופיל מקצועי — הטיפוגרפיה והצבעים כאן מיועדים לתת נוכחות נקייה ובולטת, בהשראת השילוב של כחול, ירוק וכתום בלוגו שהבאת.
      </p>

      <div class="badge-row" aria-hidden="true">
        <div class="tiny-badge">GitHub</div>
        <div class="tiny-badge" style="background:linear-gradient(90deg,#21C07A,#00B07A);">Designer</div>
      </div>
    </div>

    <div class="logo-wrap" aria-hidden="true">
      <div class="logo" role="img" aria-label="Logo circle">
        <div class="logo-inner">
          <div>
            <div class="logo-text" style="font-family: 'Monoton', cursive; font-size: clamp(18px, 3.6vw, 44px);">
              Miryam<br><span style="font-size:0.62em; font-weight:600; letter-spacing:0.6px;">Epstein</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</body>
</html>
