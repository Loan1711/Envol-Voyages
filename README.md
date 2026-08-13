[index.html](https://github.com/user-attachments/files/31029779/index.html)
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ENVOL. — Vos vacances, sans la charge mentale</title>
<meta name="description" content="Décrivez votre voyage de rêve, je m'occupe des recherches — vols, hôtels, activités. Un service de conseil voyage sur mesure en Suisse romande, honoraires clairs, aucune commission sur vos réservations.">
<meta property="og:title" content="ENVOL. — Vos vacances, sans la charge mentale">
<meta property="og:description" content="Décrivez votre voyage de rêve, je m'occupe des recherches — vols, hôtels, activités. Honoraires clairs, aucune commission cachée.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://envol-voyages.netlify.app/">
<meta name="twitter:card" content="summary">
<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Ccircle cx='32' cy='32' r='32' fill='%2314213D'/%3E%3Cpath d='M46 20 L20 30 L28 33 L30 42 L34 34 L46 20Z' fill='%232F6F57'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,500&family=Work+Sans:wght@300;400;500;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#14213D;
    --ink-soft:#3A4A6B;
    --paper:#FBFBF8;
    --paper-2:#F0F1EC;
    --gold:#2F6F57;
    --gold-soft:#8FC3AC;
    --teal:#1F5C56;
    --stamp:#A63D33;
    --line: rgba(20,33,61,0.14);
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--paper);
    background-image:
      radial-gradient(ellipse 60% 50% at 15% 10%, rgba(47,111,87,0.10), transparent),
      radial-gradient(ellipse 55% 45% at 85% 30%, rgba(20,33,61,0.07), transparent),
      radial-gradient(ellipse 50% 40% at 50% 90%, rgba(47,111,87,0.08), transparent);
    background-attachment:fixed;
    background-size:200% 200%;
    animation:driftBg 26s ease-in-out infinite;
    color:var(--ink);
    font-family:'Work Sans', sans-serif;
    font-weight:400;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  @keyframes driftBg{
    0%   { background-position: 0% 0%, 100% 0%, 50% 100%; }
    50%  { background-position: 20% 30%, 80% 20%, 40% 80%; }
    100% { background-position: 0% 0%, 100% 0%, 50% 100%; }
  }
  @media (prefers-reduced-motion: reduce){
    body{ animation:none; }
  }
  a{color:inherit; text-decoration:none;}
  img{max-width:100%; display:block;}
  .wrap{max-width:1100px; margin:0 auto; padding:0 28px;}

  h1,h2,h3{
    font-family:'Fraunces', serif;
    font-weight:600;
    line-height:1.08;
    letter-spacing:-0.01em;
  }

  .eyebrow{
    font-family:'Space Mono', monospace;
    font-size:12px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--gold);
    display:flex;
    align-items:center;
    gap:10px;
  }
  .eyebrow::before{
    content:"";
    width:22px; height:1px; background:var(--gold);
    display:inline-block;
  }

  /* perforation divider - boarding pass motif */
  .perf{
    position:relative;
    height:1px;
    background:repeating-linear-gradient(to right, var(--line) 0 6px, transparent 6px 14px);
    margin: 0;
  }
  .perf::before, .perf::after{
    content:"";
    position:absolute; top:50%; transform:translateY(-50%);
    width:22px; height:22px; border-radius:50%;
    background:var(--paper);
    border:1px solid var(--line);
  }
  .perf::before{left:-11px;}
  .perf::after{right:-11px;}

  /* NAV */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(247,243,232,0.92);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 0;
  }
  .logo{
    font-family:'Fraunces', serif;
    font-weight:700; font-size:22px;
    letter-spacing:0.01em;
    display:flex; align-items:center; gap:10px;
  }
  .logo .dot{color:var(--stamp);}
  .navlinks{
    display:flex; gap:30px;
    font-size:14px; font-weight:500;
  }
  .navlinks a{ position:relative; padding-bottom:2px;}
  .navlinks a:hover{color:var(--teal);}
  .btn{
    font-family:'Work Sans', sans-serif;
    font-weight:600; font-size:14px;
    padding:11px 22px;
    background:var(--ink);
    color:var(--paper);
    border-radius:2px;
    border:1px solid var(--ink);
    display:inline-flex; align-items:center; gap:8px;
    transition:all .2s ease;
    cursor:pointer;
  }
  .btn:hover{ background:transparent; color:var(--ink); }
  .btn-outline{
    background:transparent; color:var(--ink); border:1px solid var(--ink);
  }
  .btn-outline:hover{ background:var(--ink); color:var(--paper); }
  .btn-gold{ background:var(--gold); border-color:var(--gold); color:var(--paper);}
  .btn-gold:hover{ background:transparent; color:var(--gold);}

  @media (max-width:760px){ .navlinks{display:none;} .trust-grid{grid-template-columns:1fr !important;} }
  .split-2col{ display:grid; grid-template-columns:1fr 1fr; }
  @media (max-width:760px){ .split-2col{ grid-template-columns:1fr; } }

  /* HERO — boarding pass concept */
  .hero{
    padding:70px 0 40px;
  }
  .ticket{
    background:var(--ink);
    color:var(--paper);
    border-radius:6px;
    overflow:hidden;
    display:grid;
    grid-template-columns: 1fr 220px;
    box-shadow: 0 30px 60px -20px rgba(20,33,61,0.35);
  }
  @media (max-width:760px){ .ticket{grid-template-columns:1fr;} }
  .ticket-main{
    padding:48px 44px 40px;
  }
  .route-row{
    display:flex; align-items:center; gap:18px;
    font-family:'Space Mono', monospace;
    font-size:13px; letter-spacing:0.08em;
    color:var(--gold-soft);
    margin-bottom:26px;
  }
  .route-row .code{
    font-size:20px; font-weight:700; color:var(--paper);
  }
  .route-line{
    flex:1; height:1px; background:var(--gold-soft); position:relative; opacity:.5;
    overflow:visible;
  }
  .route-line::before{
    content:"";
    position:absolute; top:0; left:0; height:1px; width:100%;
    background:var(--gold-soft);
    transform-origin:left;
    animation:drawLine 3s ease-in-out infinite;
  }
  @keyframes drawLine{
    0%   { transform:scaleX(0); opacity:0; }
    15%  { opacity:1; }
    55%  { transform:scaleX(1); opacity:1; }
    80%  { opacity:0; }
    100% { transform:scaleX(1); opacity:0; }
  }
  .route-line svg{
    position:absolute; right:-2px; top:-7px;
    animation:flyIcon 3s ease-in-out infinite;
  }
  @keyframes flyIcon{
    0%   { transform:translateX(-100%); opacity:0; }
    15%  { opacity:1; }
    55%  { transform:translateX(0); opacity:1; }
    80%  { opacity:0; }
    100% { transform:translateX(0); opacity:0; }
  }
  @media (prefers-reduced-motion: reduce){
    .route-line::before, .route-line svg{ animation:none; transform:none; opacity:1; }
  }
  .ticket-main h1{
    font-size:44px; color:var(--paper); max-width:520px; margin-bottom:18px;
  }
  .ticket-main h1 em{ color:var(--gold); font-style:italic; }
  .ticket-main p{
    font-size:17px; color:#C9D1E3; max-width:480px; margin-bottom:30px;
  }
  .hero-actions{ display:flex; gap:14px; flex-wrap:wrap; }
  .ticket-stub{
    background:var(--gold);
    color:var(--paper);
    padding:36px 26px;
    display:flex; flex-direction:column; justify-content:space-between;
    position:relative;
  }
  .ticket-stub::before{
    content:"";
    position:absolute; left:0; top:0; bottom:0; width:0;
    border-left:2px dashed rgba(251,251,248,0.35);
  }
  .stub-label{
    font-family:'Space Mono', monospace; font-size:11px; letter-spacing:0.1em; text-transform:uppercase; opacity:.75;
  }
  .stub-value{
    font-family:'Fraunces', serif; font-weight:600; font-size:20px; margin-top:4px; margin-bottom:22px;
  }
  .stamp-badge{
    width:78px; height:78px; border-radius:50%;
    border:2px solid var(--paper);
    display:flex; align-items:center; justify-content:center;
    transform:rotate(-12deg);
    align-self:flex-start;
    font-family:'Space Mono', monospace;
    font-size:11px; text-align:center; line-height:1.3;
    letter-spacing:0.05em;
  }

  /* SECTION generic */
  section{ padding:88px 0; }
  .section-head{ max-width:640px; margin-bottom:52px; }
  .section-head h2{ font-size:34px; margin-top:14px; }
  .section-head p{ margin-top:14px; font-size:16px; color:var(--ink-soft); }

  /* HOW IT WORKS */
  .steps{
    display:grid; grid-template-columns:repeat(4,1fr); gap:0;
    border:1px solid var(--line); border-radius:6px; overflow:hidden;
  }
  @media (max-width:900px){ .steps{grid-template-columns:1fr 1fr;} }
  @media (max-width:560px){ .steps{grid-template-columns:1fr;} }
  .step{
    padding:34px 28px;
    border-right:1px solid var(--line);
    background:var(--paper);
  }
  .step:last-child{border-right:none;}
  .step .num{
    font-family:'Space Mono', monospace; color:var(--gold); font-size:13px; margin-bottom:16px; display:block;
  }
  .step h3{ font-size:19px; margin-bottom:10px; }
  .step p{ font-size:14.5px; color:var(--ink-soft); }

  /* WHY ME */
  .why{
    background:var(--ink); color:var(--paper);
    border-radius:6px;
    padding:56px 50px;
    display:grid; grid-template-columns: 1.1fr 1fr; gap:50px; align-items:center;
  }
  @media (max-width:800px){ .why{grid-template-columns:1fr;} }
  .why h2{ color:var(--paper); font-size:30px; margin-bottom:18px;}
  .why p{ color:#C9D1E3; font-size:15.5px; margin-bottom:14px; }
  .why-list{ list-style:none; }
  .why-list li{
    display:flex; gap:14px; padding:16px 0; border-top:1px solid rgba(247,243,232,0.15);
    font-size:14.5px; color:#DCE2F0;
  }
  .why-list li:last-child{padding-bottom:0;}
  .why-list .ico{
    font-family:'Space Mono', monospace; color:var(--gold); flex-shrink:0;
  }
  .signature-note{
    margin-top:22px; font-family:'Fraunces', serif; font-style:italic; font-size:16px; color:var(--gold-soft);
  }

  /* DESTINATIONS */
  .dest-grid{
    display:grid; grid-template-columns:repeat(3,1fr); gap:22px;
  }
  @media (max-width:860px){ .dest-grid{grid-template-columns:repeat(2,1fr);} }
  @media (max-width:560px){ .dest-grid{grid-template-columns:1fr;} }
  .dest-card{
    position:relative;
    border-radius:6px;
    overflow:hidden;
    aspect-ratio:4/5;
    padding:22px;
    display:flex; flex-direction:column; justify-content:flex-end;
    color:var(--paper);
    isolation:isolate;
  }
  .dest-card::before{
    content:""; position:absolute; inset:0; z-index:-1;
  }
  .dest-card::after{
    content:""; position:absolute; inset:0; z-index:-1;
    background:linear-gradient(180deg, rgba(20,33,61,0) 35%, rgba(20,33,61,0.75) 100%);
  }
  .d1::before{ background:linear-gradient(155deg,#E7A65C,#D9724A 45%,#8A3B4E); }
  .d2::before{ background:linear-gradient(155deg,#F6C7D0,#E58AA0 45%,#5B3A66); }
  .d3::before{ background:linear-gradient(155deg,#7FC8C4,#2E8C86 45%,#123D4D); }
  .d4::before{ background:linear-gradient(155deg,#F0D08A,#D9A441 45%,#7A4A26); }
  .d5::before{ background:linear-gradient(155deg,#A9D4C6,#4F8E7A 45%,#1B4B3E); }
  .d6::before{ background:linear-gradient(155deg,#F3B08A,#C9603F 45%,#4A2A3E); }
  .has-photo::before{ background-size:cover; background-position:center; }
  .photo-bali::before{ background-image:url('https://images.pexels.com/photos/36828569/pexels-photo-36828569.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-japon::before{ background-image:url('https://images.pexels.com/photos/29537651/pexels-photo-29537651.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-maldives::before{ background-image:url('https://images.pexels.com/photos/1287455/pexels-photo-1287455.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-maroc::before{ background-image:url('https://images.pexels.com/photos/28902520/pexels-photo-28902520.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-costarica::before{ background-image:url('https://images.pexels.com/photos/10614098/pexels-photo-10614098.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-grece::before{ background-image:url('https://images.pexels.com/photos/6306940/pexels-photo-6306940.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-thailande::before{ background-image:url('https://images.pexels.com/photos/37292541/pexels-photo-37292541.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-portugal::before{ background-image:url('https://images.pexels.com/photos/19627783/pexels-photo-19627783.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-mexique::before{ background-image:url('https://images.pexels.com/photos/6563919/pexels-photo-6563919.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-italie::before{ background-image:url('https://images.pexels.com/photos/19900430/pexels-photo-19900430.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-croatie::before{ background-image:url('https://images.pexels.com/photos/30160278/pexels-photo-30160278.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-lunedemiel::before{ background-image:url('https://images.pexels.com/photos/30716714/pexels-photo-30716714.jpeg?auto=compress&cs=tinysrgb&w=1200&h=750&fit=crop'); }
  .photo-puntacana::before{ background-image:url('https://images.pexels.com/photos/247447/pexels-photo-247447.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-maurice::before{ background-image:url('https://images.pexels.com/photos/31154925/pexels-photo-31154925.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-surf::before{ background-image:url('https://images.pexels.com/photos/34151366/pexels-photo-34151366.jpeg?auto=compress&cs=tinysrgb&w=1200&h=750&fit=crop'); }
  .photo-turquie::before{ background-image:url('https://images.pexels.com/photos/5700576/pexels-photo-5700576.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-egypte::before{ background-image:url('https://images.pexels.com/photos/18608913/pexels-photo-18608913.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-jordanie::before{ background-image:url('https://images.pexels.com/photos/19718009/pexels-photo-19718009.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-afriquedusud::before{ background-image:url('https://images.pexels.com/photos/4064211/pexels-photo-4064211.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-espagne::before{ background-image:url('https://images.pexels.com/photos/1884417/pexels-photo-1884417.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-malte::before{ background-image:url('https://images.pexels.com/photos/30388466/pexels-photo-30388466.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-seychelles::before{ background-image:url('https://images.pexels.com/photos/31386176/pexels-photo-31386176.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .photo-corse::before{ background-image:url('https://images.pexels.com/photos/33797052/pexels-photo-33797052.jpeg?auto=compress&cs=tinysrgb&w=800&h=1000&fit=crop'); }
  .dest-country{
    font-family:'Space Mono', monospace; font-size:11px; letter-spacing:0.1em; text-transform:uppercase; opacity:.9;
  }
  .dest-card h3{ color:var(--paper); font-size:23px; margin:6px 0 10px; }
  .dest-when{
    font-size:13px; display:inline-flex; align-items:center; gap:6px;
    border-top:1px solid rgba(247,243,232,0.4); padding-top:12px; margin-top:4px;
    font-weight:500;
  }
  .dest-when:hover{ color:var(--gold-soft); }

  /* PRICING */
  .price-wrap{
    display:grid; grid-template-columns: 1fr 1.1fr; gap:50px; align-items:start;
  }
  @media (max-width:820px){ .price-wrap{grid-template-columns:1fr;} }
  .price-card{
    border:1px solid var(--line); border-radius:6px; background:var(--paper-2);
    padding:40px 36px;
  }
  .price-row{
    display:flex; justify-content:space-between; align-items:baseline;
    padding:18px 0; border-bottom:1px dashed var(--line);
  }
  .price-row:last-of-type{ border-bottom:none; }
  .price-row .label{ font-size:15px; font-weight:500; }
  .price-row .label small{ display:block; font-size:12.5px; color:var(--ink-soft); font-weight:400; margin-top:3px;}
  .price-row .value{
    font-family:'Fraunces', serif; font-weight:600; font-size:22px; color:var(--teal); white-space:nowrap;
  }
  .price-note{ margin-top:26px; font-size:13.5px; color:var(--ink-soft); }
  .price-justif h3{ font-size:22px; margin-bottom:16px; }
  .price-justif p{ font-size:15px; color:var(--ink-soft); margin-bottom:14px; }
  .price-justif p strong{ color:var(--ink); }

  /* FAQ */
  .faq-item{
    border-bottom:1px solid var(--line);
    padding:24px 0;
  }
  .faq-item h3{ font-size:17px; font-weight:600; font-family:'Work Sans',sans-serif; margin-bottom:8px; }
  .faq-item p{ font-size:14.5px; color:var(--ink-soft); max-width:640px; }

  /* CONTACT FORM — flight request slip */
  .contact-section{ background:var(--ink); color:var(--paper); border-radius:6px; padding:56px 44px; }
  .contact-grid{ display:grid; grid-template-columns:0.9fr 1.1fr; gap:50px; }
  @media (max-width:860px){ .contact-grid{grid-template-columns:1fr;} }
  .contact-section h2{ color:var(--paper); font-size:32px; margin-bottom:16px;}
  .contact-section > .contact-grid > div:first-child p{ color:#C9D1E3; font-size:15px; margin-bottom:22px;}
  .contact-direct{ font-family:'Space Mono', monospace; font-size:14px; line-height:2; }
  .contact-direct a{ color:var(--gold-soft); }

  form{ background:var(--paper); color:var(--ink); border-radius:6px; padding:30px; }
  .form-row{ display:grid; grid-template-columns:1fr 1fr; gap:16px; margin-bottom:16px; }
  @media (max-width:500px){ .form-row{grid-template-columns:1fr;} }
  .field{ display:flex; flex-direction:column; gap:6px; margin-bottom:16px; }
  .field label{ font-size:12.5px; font-weight:600; text-transform:uppercase; letter-spacing:0.04em; color:var(--ink-soft); }
  .field input, .field select, .field textarea{
    border:1px solid var(--line); border-radius:3px; padding:10px 12px;
    font-family:'Work Sans', sans-serif; font-size:14px; background:#fff; color:var(--ink);
  }
  .field textarea{ resize:vertical; min-height:70px; }
  fieldset{ border:1px solid var(--line); border-radius:3px; padding:14px; margin-bottom:16px; }
  legend{ font-size:12.5px; font-weight:600; text-transform:uppercase; letter-spacing:0.04em; color:var(--ink-soft); padding:0 6px; }
  .checks{ display:flex; flex-wrap:wrap; gap:10px 18px; }
  .checks label{ display:flex; align-items:center; gap:7px; font-size:13.5px; font-weight:400; text-transform:none; letter-spacing:0; }
  .checks input{ width:auto; }
  .form-submit{ width:100%; justify-content:center; margin-top:6px; }

  /* FOOTER */
  footer{ padding:50px 0 60px; }
  .footer-inner{
    display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:20px;
    padding-top:34px; font-size:13px; color:var(--ink-soft);
  }
  footer .logo{ margin-bottom:6px; }

  .reveal{ opacity:0; transform:translateY(16px); transition:opacity .6s ease, transform .6s ease; }
  .reveal.in{ opacity:1; transform:none; }

  @media (prefers-reduced-motion: reduce){
    .reveal{ opacity:1; transform:none; transition:none; }
    html{scroll-behavior:auto;}
  }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav>
      <div class="logo">ENVOL<span class="dot">.</span></div>
      <div class="navlinks">
        <a href="#octobre">Octobre</a>
        <a href="#noel">Noël</a>
        <a href="#paques">Pâques</a>
        <a href="#ete">Été</a>
        <a href="#tarifs">Tarifs</a>
      </div>
      <a href="#demande" class="btn">Faire une demande</a>
    </nav>
  </div>
</header>

<main>
  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div class="ticket reveal">
        <div class="ticket-main">
          <div class="route-row">
            <span class="code">GVA / ZRH / BSL</span>
            <span class="route-line"><svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M2 12h16m0 0-5-5m5 5-5 5" stroke="#DCC98A" stroke-width="1.6"/></svg></span>
            <span class="code">N'IMPORTE OÙ</span>
          </div>
          <h1>Vos vacances de rêve, <em>sans y passer vos soirées.</em></h1>
          <p>Vous connaissez ce moment où l'envie de partir est là, mais où l'idée de tout comparer — vols, hôtels, avis, options — vous fatigue déjà ? C'est exactement là que j'interviens. Vous me dites votre envie, je fais le travail de recherche, et vous récupérez juste le meilleur : votre temps et votre énergie, gardés pour l'essentiel.</p>
          <div class="hero-actions">
            <a href="#demande" class="btn btn-gold">Décrire mon voyage →</a>
            <a href="#concept" class="btn btn-outline" style="border-color:#4A5A80; color:#C9D1E3;">Comment ça marche</a>
          </div>
        </div>
        <div class="ticket-stub">
          <div>
            <div class="stub-label">Conseiller</div>
            <div class="stub-value">Loan S.</div>
            <div class="stub-label">Formé chez</div>
            <div class="stub-value" style="font-size:16px;">Kuoni Voyages</div>
          </div>
          <div class="stamp-badge">ENVOL<br>É. 2026</div>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- VACANCES D'AUTOMNE OCTOBRE -->
  <section id="octobre" style="padding-top:60px; padding-bottom:60px;">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow" style="color:var(--stamp);">◉ Dernier moment</span>
        <h2>Les vacances d'automne arrivent vite.</h2>
        <p>Deux petites semaines pour souffler avant l'hiver — encore le temps de trouver quelque chose de bien si vous vous y prenez maintenant.</p>
      </div>
      <div class="dest-grid reveal">
        <a class="dest-card d4 has-photo photo-turquie" href="https://www.partir.com/Turquie/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Méditerranée orientale</span>
          <h3>Turquie</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Cappadoce, côtes et lumière d'automne.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d6 has-photo photo-egypte" href="https://www.partir.com/Egypte/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Afrique du Nord</span>
          <h3>Égypte</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Pyramides et mer Rouge, chaleur garantie.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d5 has-photo photo-jordanie" href="https://www.partir.com/Jordanie/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Moyen-Orient</span>
          <h3>Jordanie</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Petra sous un climat doux, la meilleure saison.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
      </div>
      <p style="margin-top:20px;"><a href="#demande" class="btn btn-outline" style="border-color:var(--ink);">Réserver mes vacances d'octobre →</a></p>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- CONCEPT -->
  <section id="concept">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Le concept</span>
        <h2>Vous rêvez du voyage. Je fais les recherches.</h2>
        <p>Trouver un vol pas cher, comparer quinze hôtels, vérifier les pensions, caler les activités : ça prend un temps fou. ENVOL. s'occupe de cette partie, vous n'avez plus qu'à faire vos valises.</p>
        <p style="margin-top:10px; font-size:14.5px;">Week-end en ville, séjour balnéaire, voyage en famille, lune de miel, ou même un déplacement pour un match de foot entre potes — peu importe le genre de voyage, ça m'intéresse.</p>
      </div>
      <div class="steps reveal">
        <div class="step">
          <span class="num">01</span>
          <h3>Vous me racontez l'envie</h3>
          <p>Dates, budget, nombre de personnes, style de voyage — par le formulaire, ou juste un message.</p>
        </div>
        <div class="step">
          <span class="num">02</span>
          <h3>Je cherche pour vous</h3>
          <p>Vols, hôtels, pensions, activités. Je compare avec les mêmes outils qu'une agence de voyage.</p>
        </div>
        <div class="step">
          <span class="num">03</span>
          <h3>Vous recevez le résultat</h3>
          <p>Un dossier clair, les meilleures options expliquées simplement, sans jargon inutile.</p>
        </div>
        <div class="step">
          <span class="num">04</span>
          <h3>Vous réservez, comme vous voulez</h3>
          <p>Directement chez le prestataire, au prix réel. Je ne touche rien sur votre réservation.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- WHY ME -->
  <section>
    <div class="wrap">
      <div class="why reveal">
        <div>
          <span class="eyebrow" style="color:var(--gold-soft);">Pourquoi moi</span>
          <h2>Deux ans en agence de voyage, à apprendre comment bien préparer un départ.</h2>
          <p>J'ai fait ma formation d'employé de commerce chez Kuoni Voyages pendant deux ans : conseil client, dossiers de réservation, coordination avec des prestataires partout dans le monde. Je connais les bons outils et les pièges à éviter — et surtout, j'aime vraiment faire ça.</p>
          <p>J'ai aussi eu la chance de pas mal voyager moi-même, en famille et seul, ce qui aide beaucoup pour tout ce qui touche à l'organisation : je sais ce qui compte vraiment sur place, et ce qui n'est qu'un détail sur le papier.</p>
          <p class="signature-note">« Je prépare aussi mon propre grand départ, donc je sais ce que ça fait d'avoir hâte. »</p>
        </div>
        <ul class="why-list">
          <li><span class="ico">→</span> 2 ans de formation en agence de voyage (Kuoni)</li>
          <li><span class="ico">→</span> Les mêmes outils de recherche que les pros du secteur</li>
          <li><span class="ico">→</span> Zéro marge sur vos vols et hôtels, juste des honoraires clairs</li>
          <li><span class="ico">→</span> Un humain qui répond, pas un chatbot</li>
          <li><span class="ico">→</span> Français, anglais, allemand, espagnol</li>
        </ul>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- DESTINATIONS -->
  <section id="destinations">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Inspiration</span>
        <h2>Quelques destinations qui reviennent souvent.</h2>
        <p>Cliquez sur une carte pour voir la meilleure période pour y aller.</p>
      </div>
      <div class="dest-grid reveal">

        <a class="dest-card d1 has-photo photo-bali" href="https://www.partir.com/Bali/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Indonésie</span>
          <h3>Bali</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Rizières en terrasses et mer, l'île qui ralentit le temps.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d2 has-photo photo-japon" href="https://www.partir.com/Japon/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Asie de l'Est</span>
          <h3>Japon</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Tradition et modernité, à chaque coin de rue.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d3 has-photo photo-maldives" href="https://www.partir.com/Maldives/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Océan Indien</span>
          <h3>Maldives</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Lagons turquoise et farniente absolu.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d4 has-photo photo-maroc" href="https://www.partir.com/Maroc/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Afrique du Nord</span>
          <h3>Maroc</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Désert, médinas et lumière dorée.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d5 has-photo photo-costarica" href="https://www.partir.com/Costa-rica/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Amérique centrale</span>
          <h3>Costa Rica</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Jungle, volcans et biodiversité pure.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d6 has-photo photo-grece" href="https://www.partir.com/Grece/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Méditerranée</span>
          <h3>Grèce</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Îles blanches et bleues, à l'infini.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d1 has-photo photo-thailande" href="https://www.partir.com/Thailande/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Asie du Sud-Est</span>
          <h3>Thaïlande</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Plages, temples et street food légendaire.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d4 has-photo photo-portugal" href="https://www.partir.com/Portugal/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Europe</span>
          <h3>Portugal</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Villes pastel et côte sauvage, à deux pas de la Suisse.</p>
          <span class="dest-when">Quand partir →</span>
        </a>

      </div>
      <p style="margin-top:20px; font-size:13px; color:var(--ink-soft);">Rien de tout ça ne vous parle ? Pas grave, dites-moi juste ce que vous avez en tête dans le formulaire, je pars de zéro.</p>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- NOEL AU CHAUD -->
  <section id="noel">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Envie de saison</span>
        <h2>Passer Noël au chaud, loin du gris de décembre.</h2>
        <p>Pendant qu'on s'emmitoufle en Suisse, ces destinations vivent leur plus belle saison — chaleur et plages garanties.</p>
      </div>
      <div class="dest-grid reveal">
        <a class="dest-card d3 has-photo photo-maurice" href="https://www.partir.com/Ile-maurice/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Océan Indien</span>
          <h3>Île Maurice</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Lagons, sable fin et douceur mauricienne.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d5 has-photo photo-mexique" href="https://www.partir.com/Mexique/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Amérique du Nord</span>
          <h3>Mexique</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Cénotes, culture maya et plages caraïbes.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d6 has-photo photo-puntacana" href="https://www.partir.com/Republique-dominicaine/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Caraïbes</span>
          <h3>Punta Cana</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Eaux turquoise et cocotiers à perte de vue.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d4 has-photo photo-afriquedusud" href="https://www.partir.com/Afrique-du-sud/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Afrique australe</span>
          <h3>Afrique du Sud</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Décembre, c'est leur été — Cape Town au meilleur moment.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- WEEKEND FOOT -->
  <section>
    <div class="wrap">
      <div style="gap:40px; align-items:center;" class="reveal split-2col">
        <div>
          <span class="eyebrow">Une envie parmi d'autres</span>
          <h2 style="font-size:30px; margin-top:14px;">Un déplacement entre potes pour voir votre équipe jouer ?</h2>
          <p style="margin-top:14px; font-size:15px; color:var(--ink-soft);">Vol ou train, hôtel proche du stade, logistique de groupe : un déplacement se prépare comme n'importe quel voyage, avec en plus les horaires de match à respecter. Je cale tout, pour que le seul stress de la journée soit celui du coup d'envoi.</p>
        </div>
        <div style="background:var(--ink); border-radius:6px; padding:34px; color:var(--paper);">
          <div class="route-row" style="margin-bottom:16px;">
            <span class="code">DOMICILE</span>
            <span class="route-line"><svg width="14" height="14" viewBox="0 0 24 24" fill="none"><path d="M2 12h16m0 0-5-5m5 5-5 5" stroke="#8FC3AC" stroke-width="1.6"/></svg></span>
            <span class="code">STADE</span>
          </div>
          <p style="font-size:14.5px; color:#C9D1E3;">Vol ou train + hôtel à distance de marche du stade, groupé pour toute la bande.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- SURF -->
  <section>
    <div class="wrap">
      <div style="gap:40px; align-items:center;" class="reveal split-2col">
        <div>
          <span class="eyebrow">Une envie parmi d'autres</span>
          <h2 style="font-size:30px; margin-top:14px;">Un surf trip, ça se prépare avec quelqu'un qui connaît les spots.</h2>
          <p style="margin-top:14px; font-size:15px; color:var(--ink-soft);">Le surf, c'est une vraie passion chez moi — même si, entre nous, je passe encore plus de temps dans l'eau que debout sur les vagues. Mais j'ai de bonnes connaissances sur les spots, les saisons de houle et les endroits adaptés à chaque niveau, et j'aime particulièrement préparer ce genre de voyage.</p>
          <p style="margin-top:10px;"><a href="https://oupartirsurfer.com/" target="_blank" rel="noopener" class="btn btn-outline" style="border-color:var(--ink);">Guide des spots surf →</a></p>
        </div>
        <a href="https://oupartirsurfer.com/" target="_blank" rel="noopener" class="dest-card has-photo photo-surf" style="aspect-ratio:16/10;">
          <span class="dest-country">Surf trip</span>
          <h3 style="font-size:26px;">Où surfer ?</h3>
          <p style="font-size:13px; opacity:.9;">Spots, saisons et niveaux — le guide complet.</p>
        </a>
      </div>
    </div>
  </section>
  <section>
    <div class="wrap">
      <div style="gap:40px; align-items:center;" class="reveal split-2col">
        <div class="dest-card d2 has-photo photo-lunedemiel" style="aspect-ratio:16/10;">
          <span class="dest-country">Pour deux</span>
          <h3 style="font-size:28px;">Lune de miel</h3>
          <p style="font-size:13px; opacity:.9;">Un voyage qui ne ressemble qu'à vous deux.</p>
        </div>
        <div>
          <span class="eyebrow">Une envie parmi d'autres</span>
          <h2 style="font-size:30px; margin-top:14px;">Le premier voyage en tant que mariés mérite d'être réussi.</h2>
          <p style="margin-top:14px; font-size:15px; color:var(--ink-soft);">Villa privée, hôtel avec vue, dîners au coucher du soleil — dites-moi le genre de voyage qui vous ressemble, je construis une sélection pensée juste pour vous deux.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- VACANCES DE PAQUES -->
  <section id="paques">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">À prévoir</span>
        <h2>Pâques 2027, ça se prépare déjà.</h2>
        <p>Les vacances de Pâques tombent du 26 mars au 16 avril 2027 selon les cantons. Ça paraît loin, mais les bons prix et les bonnes dispos partent tôt — autant s'y prendre à l'avance.</p>
      </div>
      <div class="dest-grid reveal">
        <a class="dest-card d6 has-photo photo-espagne" href="https://www.partir.com/Espagne/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Europe</span>
          <h3>Espagne</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Andalousie et douceur de printemps, vol court.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d1 has-photo photo-italie" href="https://www.partir.com/Italie/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Europe</span>
          <h3>Italie</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Entre côte, culture et cuisine, à deux pas de chez nous.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d4 has-photo photo-malte" href="https://www.partir.com/Malte/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Méditerranée</span>
          <h3>Malte</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Petite île, grand charme, climat déjà doux.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- VACANCES D'ETE -->
  <section id="ete">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">À prévoir</span>
        <h2>L'été 2027, ça arrive plus vite qu'on ne le pense.</h2>
        <p>Entre fin juin et mi-juillet selon les cantons, avec une rentrée courant août. La haute saison se réserve tôt — les meilleures adresses et les vols corrects partent en premier.</p>
      </div>
      <div class="dest-grid reveal">
        <a class="dest-card d6 has-photo photo-seychelles" href="https://www.partir.com/Seychelles/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Océan Indien</span>
          <h3>Seychelles</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Rochers de granit et plages de rêve, l'excellence tropicale.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d3 has-photo photo-croatie" href="https://www.partir.com/Croatie/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Adriatique</span>
          <h3>Croatie</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Eaux cristallines, vol court, très bon rapport qualité-prix.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
        <a class="dest-card d1 has-photo photo-corse" href="https://www.partir.com/Corse/quand-partir.html" target="_blank" rel="noopener">
          <span class="dest-country">Méditerranée</span>
          <h3>Corse</h3>
          <p style="font-size:12.5px; opacity:.85; margin-bottom:6px;">Criques sauvages et mer turquoise, sans quitter la France.</p>
          <span class="dest-when">Quand partir →</span>
        </a>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <section id="tarifs">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Honoraires</span>
        <h2>Un prix fixe, clair, annoncé avant de commencer.</h2>
      </div>
      <div class="price-wrap reveal">
        <div class="price-card">
          <div class="price-row">
            <div class="label">Escapade simple<br><small>1 destination, jusqu'à 2 personnes</small></div>
            <div class="value">150.-</div>
          </div>
          <div class="price-row">
            <div class="label">Voyage groupe / famille<br><small>1 destination, jusqu'à 6 personnes</small></div>
            <div class="value">200.-</div>
          </div>
          <div class="price-row">
            <div class="label">Sur-mesure complexe<br><small>Multi-destinations, +6 personnes</small></div>
            <div class="value">300.-</div>
          </div>
          <p class="price-note">Montant communiqué et validé avec vous avant toute recherche. Aucun frais caché, aucune commission sur vos réservations.</p>
          <p class="price-note" style="margin-top:10px;">Paiement accepté par <strong style="color:var(--ink);">Twint</strong> ou en <strong style="color:var(--ink);">espèces</strong>, une fois le dossier de voyage livré.</p>
        </div>
        <div class="price-justif">
          <h3>Pourquoi des honoraires, et pas une commission ?</h3>
          <p>Je ne touche <strong>aucune marge</strong> sur vos vols ou votre hôtel : vous réservez vous-même, directement, au prix réel du marché.</p>
          <p>Ce que vous payez, c'est simplement <strong>mon temps</strong> — et ça en prend beaucoup : rechercher, comparer, mettre en forme un dossier de voyage clair et personnalisé, comme le ferait une agence, mais sans la structure ni les frais d'une agence.</p>
          <p>C'est gagnant-gagnant : vous passez de meilleures vacances sans y perdre vos soirées, et ces honoraires m'aident à financer un projet qui me tient à cœur — partir moi-même travailler à l'étranger.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- FAQ -->
  <section id="faq">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Questions fréquentes</span>
        <h2>Avant de vous lancer.</h2>
      </div>
      <div class="reveal" style="max-width:760px;">
        <div class="faq-item">
          <h3>Dois-je payer avant que vous ne commenciez les recherches ?</h3>
          <p>Non. On échange d'abord sur votre projet et le montant des honoraires, et le règlement n'intervient qu'une fois le dossier de voyage livré et validé par vous.</p>
        </div>
        <div class="faq-item">
          <h3>Et si aucune proposition ne me convient ?</h3>
          <p>On en rediscute ensemble et j'ajuste les recherches selon vos retours. L'objectif, c'est que vous soyez vraiment emballé·e avant de réserver quoi que ce soit.</p>
        </div>
        <div class="faq-item">
          <h3>Réservez-vous le voyage à ma place ?</h3>
          <p>Non — je vous fournis tous les liens et informations pour réserver vous-même, directement chez la compagnie aérienne ou l'hôtel. Vous gardez le contrôle total sur votre paiement.</p>
        </div>
        <div class="faq-item">
          <h3>Sous combien de temps recevrai-je ma proposition ?</h3>
          <p>En général sous 48 à 72h après réception de toutes vos informations, selon la complexité de la demande.</p>
        </div>
        <div class="faq-item">
          <h3>Comment puis-je vous payer ?</h3>
          <p>Par Twint ou en espèces, une fois le dossier de voyage livré et validé par vous. Aucun paiement n'est demandé avant.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="wrap"><div class="perf"></div></div>

  <!-- CONFIANCE / LEGAL -->
  <section style="padding:56px 0;">
    <div class="wrap">
      <div class="section-head reveal">
        <span class="eyebrow">Bon à savoir</span>
        <h2 style="font-size:26px;">Transparence et confiance.</h2>
      </div>
      <div class="reveal trust-grid" style="display:grid; grid-template-columns:repeat(3,1fr); gap:24px;">
        <div style="border:1px solid var(--line); border-radius:6px; padding:24px; background:var(--paper-2);">
          <h3 style="font-family:'Work Sans',sans-serif; font-size:15px; font-weight:600; margin-bottom:8px;">Vos données</h3>
          <p style="font-size:13.5px; color:var(--ink-soft);">Les informations transmises dans le formulaire (dates, nombre de voyageurs, préférences) ne servent qu'à préparer votre dossier de voyage. Elles ne sont ni revendues, ni partagées avec des tiers, ni utilisées à d'autres fins.</p>
        </div>
        <div style="border:1px solid var(--line); border-radius:6px; padding:24px; background:var(--paper-2);">
          <h3 style="font-family:'Work Sans',sans-serif; font-size:15px; font-weight:600; margin-bottom:8px;">Annulation</h3>
          <p style="font-size:13.5px; color:var(--ink-soft);">Le paiement des honoraires intervient une fois le dossier de voyage livré et validé. Le travail de recherche étant alors effectué, aucun remboursement n'est possible après livraison, même si vous renoncez ensuite à votre voyage.</p>
        </div>
        <div style="border:1px solid var(--line); border-radius:6px; padding:24px; background:var(--paper-2);">
          <h3 style="font-family:'Work Sans',sans-serif; font-size:15px; font-weight:600; margin-bottom:8px;">Mentions légales</h3>
          <p style="font-size:13.5px; color:var(--ink-soft);">ENVOL. est une activité indépendante à titre accessoire exercée par un particulier (Loan Stillavato, Route de la Préla 198, 1609 Fiaugères, Suisse). Ce service n'est pas une agence de voyage : aucune réservation n'est effectuée en votre nom.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT / FORM -->
  <section id="demande">
    <div class="wrap">
      <div class="contact-section reveal">
        <div class="contact-grid">
          <div>
            <span class="eyebrow" style="color:var(--gold-soft);">Demande de voyage</span>
            <h2>Racontez-moi votre projet.</h2>
            <p>Plus vous donnez de détails, plus la sélection que je vous prépare sera juste. Vous pouvez aussi simplement m'écrire ou m'appeler directement.</p>
            <div class="contact-direct">
              <div>✉ <a href="mailto:loan.stillavato17@gmail.com">loan.stillavato17@gmail.com</a></div>
              <div>☎ <a href="tel:+41798400065">+41 79 840 00 65</a></div>
            </div>
          </div>

          <form action="https://formsubmit.co/loan.stillavato17@gmail.com" method="POST">
            <input type="hidden" name="_subject" value="Nouvelle demande de voyage — ENVOL.">
            <input type="hidden" name="_template" value="table">
            <input type="hidden" name="_autoresponse" value="Bonjour,

Merci beaucoup d'avoir fait confiance à ENVOL. pour préparer votre voyage ! Votre demande vient de m'arriver, et je m'attelle déjà aux recherches : vols, hôtels, et tout ce qu'il faut pour que votre séjour soit à la hauteur de vos envies.

Vous recevrez une première sélection personnalisée sous 48 à 72h, directement par email. Si jamais vous avez oublié un détail important ou une envie particulière, n'hésitez pas à me le faire savoir en répondant simplement à cet email.

À très bientôt,
Loan — ENVOL.">

            <div class="form-row">
              <div class="field">
                <label>Prénom Nom *</label>
                <input type="text" name="Nom" required>
              </div>
              <div class="field">
                <label>Email *</label>
                <input type="email" name="email" required>
              </div>
            </div>

            <div class="field">
              <label>Téléphone *</label>
              <input type="tel" name="Telephone" required>
            </div>

            <div class="field">
              <label>Destination souhaitée (ou "je suis ouvert aux idées") *</label>
              <input type="text" name="Destination souhaitee" placeholder="Ex : Bali, Grèce, je ne sais pas encore..." required>
            </div>

            <div class="form-row">
              <div class="field">
                <label>Départ au plus tôt *</label>
                <input type="date" name="Date de depart au plus tot" required>
              </div>
              <div class="field">
                <label>Retour au plus tard *</label>
                <input type="date" name="Date de retour au plus tard" required>
              </div>
            </div>

            <div class="form-row">
              <div class="field">
                <label>Adultes *</label>
                <input type="number" name="Nombre d'adultes" min="1" value="2" required>
              </div>
              <div class="field">
                <label>Enfants (+ dates de naissance en commentaire)</label>
                <input type="number" name="Nombre d'enfants" min="0" value="0">
              </div>
            </div>

            <fieldset>
              <legend>Aéroport(s) de départ possibles</legend>
              <div class="checks">
                <label><input type="checkbox" name="Aeroport" value="GVA – Genève"> GVA – Genève</label>
                <label><input type="checkbox" name="Aeroport" value="ZRH – Zurich"> ZRH – Zurich</label>
                <label><input type="checkbox" name="Aeroport" value="BSL – Bâle"> BSL – Bâle</label>
              </div>
            </fieldset>

            <div class="form-row">
              <div class="field">
                <label>Formule repas</label>
                <select name="Formule repas">
                  <option>Room only</option>
                  <option>Petit-déjeuner (B&B)</option>
                  <option>Demi-pension</option>
                  <option>Pension complète</option>
                  <option>All inclusive</option>
                  <option>Pas de préférence</option>
                </select>
              </div>
              <div class="field">
                <label>Type d'hôtel souhaité</label>
                <input type="text" name="Type d'hotel" placeholder="Ex : boutique hôtel, resort familial, 4-5 étoiles...">
              </div>
            </div>

            <fieldset>
              <legend>Envies sur place (cochez ce qui vous parle)</legend>
              <div class="checks">
                <label><input type="checkbox" name="Envies" value="Piscine"> Piscine</label>
                <label><input type="checkbox" name="Envies" value="Bord de mer"> Bord de mer</label>
                <label><input type="checkbox" name="Envies" value="Toboggans / parc aquatique"> Toboggans / parc aquatique</label>
                <label><input type="checkbox" name="Envies" value="Spa / bien-être"> Spa / bien-être</label>
                <label><input type="checkbox" name="Envies" value="Vie nocturne"> Vie nocturne</label>
                <label><input type="checkbox" name="Envies" value="Excursions / activités"> Excursions / activités</label>
                <label><input type="checkbox" name="Envies" value="Calme et déconnexion"> Calme et déconnexion</label>
              </div>
            </fieldset>

            <div class="field">
              <label>Voiture de location *</label>
              <select name="Voiture de location" required>
                <option value="" disabled selected>-- Choisissez --</option>
                <option>Non</option>
                <option>Oui — boîte manuelle</option>
                <option>Oui — boîte automatique</option>
                <option>Pas de préférence</option>
              </select>
            </div>

            <div class="field">
              <label>Autres précisions (budget, envies particulières, âges des enfants...) *</label>
              <textarea name="Commentaires" required></textarea>
            </div>

            <button type="submit" class="btn btn-gold form-submit">Envoyer ma demande</button>
          </form>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">
    <div class="perf" style="margin-bottom:40px;"></div>
    <div class="logo">ENVOL<span class="dot">.</span></div>
    <div class="footer-inner">
      <div>Conseil voyage sur mesure — préparé avec soin, sans commission cachée.</div>
      <div>loan.stillavato17@gmail.com — +41 79 840 00 65</div>
    </div>
  </div>
</footer>

<script>
  const els = document.querySelectorAll('.reveal');
  const io = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
  }, {threshold:0.12});
  els.forEach(el=>io.observe(el));
</script>

</body>
</html>
