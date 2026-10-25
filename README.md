# مهدی قورچی — رزومه وب

> سورس کامل HTML/CSS در این فایل قرار دارد تا ساختار، استایل‌ها، رنگ‌ها، چیدمان و تمام المان‌ها بدون حذف حفظ شوند. برای مشاهده طراحی نهایی در مرورگر، فایل `Mahdi-Ghourchi-Resume.html` را باز کنید؛ Markdown خالص به‌تنهایی نمی‌تواند استایل‌های سفارشی HTML/CSS را در همه نمایشگرها عیناً رندر کند.

```html
<!doctype html>

<html lang="fa" dir="rtl">

<head>

<meta charset="utf-8">

<meta name="viewport" content="width=device-width, initial-scale=1">

<meta name="color-scheme" content="dark">

<title>مهدی قورچی — توسعه‌دهنده بک‌اند و هوش مصنوعی</title>

<meta name="description" content="مهدی قورچی؛ دانشجوی مهندسی برق و توسعه‌دهنده بک‌اند با تمرکز بر Python، Flask، FastAPI، Docker و یکپارچه‌سازی هوش مصنوعی.">

<!-- TODO: دامنه واقعی را جایگزین کنید -->

<link rel="canonical" href="https://example.com/">

<meta property="og:type" content="website">

<meta property="og:title" content="مهدی قورچی — توسعه‌دهنده بک‌اند و هوش مصنوعی">

<meta property="og:description" content="توسعه بک‌اند، طراحی API و یکپارچه‌سازی هوش مصنوعی.">

<meta name="twitter:card" content="summary">

<script type="application/ld+json">{"@context":"https://schema.org","@type":"Person","name":"Mahdi Ghourchi","alternateName":"مهدی قورچی","jobTitle":"Backend & AI Developer","sameAs":["https://github.com/Mahdi-ghourchi","https://www.linkedin.com/in/mahdi-ghourchi/"],"knowsAbout":["Python","FastAPI","Flask","Docker","Linux","LLM integration"]}</script>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Geist:wght@400;500;600;700;800&family=Geist+Mono:wght@400;500&family=Vazirmatn:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>

:root{color-scheme:dark;--bg:#0a0a0a;--s1:#0f0f10;--s2:#151516;--ln:#232325;--ln2:#343437;--tx:#ededed;--soft:#cfcfd3;--mu:#a1a1a6;--fa:#7d7d83;--ac:#ef302a;--r:8px;--w:1120px;--sans:'Geist','Vazirmatn',Tahoma,sans-serif;--mono:'Geist Mono',ui-monospace,Menlo,monospace}

*,*::before,*::after{box-sizing:border-box}

html{scroll-behavior:smooth;background:var(--bg)}

body{margin:0;background:var(--bg);color:var(--tx);font:400 15px/1.95 var(--sans);-webkit-font-smoothing:antialiased;overflow-wrap:anywhere}

::selection{background:var(--ac);color:#fff}

a{color:inherit;text-decoration:none}

a:focus-visible{outline:2px solid var(--ac);outline-offset:4px;border-radius:4px}

h1,h2,h3,h4,p{margin:0}

.container{width:min(calc(100% - 64px),var(--w));margin-inline:auto}

.print-page{display:contents}

.ltr{direction:ltr;unicode-bidi:isolate;text-align:right}

.topbar{border-bottom:1px solid var(--ln)}

.nav-inner{min-height:72px;display:flex;align-items:center;justify-content:space-between;gap:24px}

.brand{display:inline-flex;align-items:center;gap:12px}

.brand-mark{position:relative;width:34px;height:34px;display:grid;place-items:center;border:1px solid var(--ln2);border-radius:var(--r);background:var(--s1);font:500 12px var(--mono)}

.brand-mark::after{content:'';position:absolute;top:-2px;inset-inline-end:-2px;width:6px;height:6px;border-radius:50%;background:var(--ac)}

.brand-copy{display:flex;flex-direction:column;line-height:1.5}

.brand-copy strong{font-size:14px;font-weight:600}

.brand-copy span{color:var(--fa);font:400 10px var(--mono);letter-spacing:.12em;direction:ltr}

.nav-links{list-style:none;display:flex;flex-wrap:wrap;gap:4px;margin:0;padding:0}

.nav-links a{display:block;padding:5px 12px;border-radius:6px;color:var(--mu);font-size:13px;transition:color .15s,background .15s}

.nav-links a:hover{color:var(--tx);background:var(--s2)}

/* Hero */

.hero{position:relative;isolation:isolate;overflow:hidden;display:flex;align-items:center;min-height:560px;padding:96px 0 80px;border-bottom:1px solid var(--ln);background:radial-gradient(ellipse 42rem 26rem at 0% 100%,rgba(239,48,42,.12),transparent 70%),var(--bg)}

.hero-portrait-image{position:absolute;z-index:0;left:0;bottom:0;height:100%;width:auto;max-width:56%;object-fit:contain;object-position:left bottom;pointer-events:none;-webkit-mask-image:linear-gradient(90deg,#000 45%,transparent 100%);mask-image:linear-gradient(90deg,#000 45%,transparent 100%)}

.hero-grid{position:relative;z-index:1}

.hero-copy{max-width:640px}

.hero h1{font-size:clamp(52px,7.4vw,92px);font-weight:800;line-height:1.2;text-wrap:balance}

.hero-name-en{display:block;margin-top:10px;color:var(--mu);font:500 15px/1.6 var(--mono);letter-spacing:.2em;direction:ltr;text-align:right}

.hero-role{display:flex;flex-wrap:wrap;align-items:center;gap:12px;margin-top:28px;color:var(--soft);font-size:19px;font-weight:500}

.hero-role .sep{width:1px;height:16px;background:var(--ln2)}

.hero-role .ltr{color:var(--mu);font:400 14px var(--mono)}

.hero-description{max-width:60ch;margin-top:18px;color:var(--mu);font-size:15px;line-height:2.15}

.hero-description strong{color:var(--tx);font-weight:500}

.hero-meta{display:flex;flex-wrap:wrap;gap:8px;margin-top:28px}

.meta-pill{display:inline-flex;align-items:center;gap:8px;padding:3px 12px;border:1px solid var(--ln2);border-radius:6px;background:rgba(10,10,10,.6);color:var(--soft);font:400 12px/1.9 var(--mono);direction:ltr}

.meta-pill::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--ac)}

.hero-links{display:flex;flex-wrap:wrap;gap:8px 24px;margin-top:22px}

.hero-links a{padding-bottom:2px;border-bottom:1px solid var(--ln2);color:var(--mu);font:400 12.5px var(--mono);direction:ltr;transition:color .15s,border-color .15s}

.hero-links a:hover{color:var(--tx);border-color:var(--ac)}

.quickfacts-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;margin-block:40px;overflow:hidden;background:var(--ln);border:1px solid var(--ln);border-radius:var(--r)}

.quickfact{display:flex;flex-direction:column;gap:2px;padding:18px 20px;background:var(--s1)}

.quickfact-label{color:var(--fa);font-size:12px}

.quickfact-value{color:var(--soft);font-size:14px;font-weight:500;line-height:1.8}

/* Sections */

.section{padding-block:76px;border-top:1px solid var(--ln)}

.section>.container{display:grid;grid-template-columns:minmax(0,250px) minmax(0,1fr);column-gap:64px;align-items:start}

.section>.container>*{grid-column:2}

.section>.container>.section-head{grid-column:1;grid-row:1/span 6}

.section-title{font-size:clamp(24px,3vw,32px);font-weight:700;line-height:1.5}

.section-lede{margin-top:12px;color:var(--mu);font-size:13px;line-height:2.05}

.focus-list{display:grid;grid-template-columns:repeat(2,1fr);column-gap:40px;border-top:1px solid var(--ln)}

.focus-item{padding:20px 0;border-bottom:1px solid var(--ln)}

.focus-item h3{display:flex;align-items:center;gap:10px;margin-bottom:6px;font-size:15px;font-weight:600}

.focus-item h3::before{content:'';flex:none;width:6px;height:6px;border-radius:1px;background:var(--ac)}

.focus-item p{color:var(--mu);font-size:13px;line-height:2}

.experience-list{border-top:1px solid var(--ln)}

.experience-item{display:grid;grid-template-columns:minmax(150px,.75fr) 1.5fr;gap:36px;padding:26px 0;border-bottom:1px solid var(--ln)}

.experience-type{display:inline-flex;align-items:center;gap:8px;margin-bottom:8px;color:var(--ac);font-size:12px}

.experience-type::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--ac)}

.experience-role{font-size:18px;font-weight:650;line-height:1.7}

.experience-org{color:var(--soft);font-size:13px}

.experience-date{margin-top:8px;color:var(--fa);font-size:12px}

.experience-copy p{color:var(--mu);font-size:13.5px;line-height:2.05}

.experience-copy p+p{margin-top:8px}

.tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:14px}

.tag{padding:1px 9px;border:1px solid var(--ln2);border-radius:6px;color:var(--soft);font:400 11.5px/1.9 var(--mono);direction:ltr;unicode-bidi:isolate}

.project-status{display:inline-flex;align-items:center;gap:7px;padding:0 10px;border:1px solid rgba(239,48,42,.38);border-radius:999px;color:#ff9b97;font-size:12px}

.project-status::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--ac)}

.projects-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}

.project-card{display:flex;flex-direction:column;gap:10px;padding:22px;background:var(--s1);border:1px solid var(--ln);border-radius:var(--r);transition:border-color .2s}

.project-card:hover{border-color:var(--ln2)}

.project-top{display:flex;align-items:center;justify-content:space-between;gap:10px}

.project-title{font:600 19px/1.5 var(--sans)}

.project-description{color:var(--mu);font-size:13px;line-height:2.05}

.project-card .tags{margin-top:auto;padding-top:6px}

.subheading{margin-bottom:14px;font-size:15px;font-weight:600}

.more{margin-top:44px}

.more-list{list-style:none;margin:0;padding:0;border-top:1px solid var(--ln)}

.more-list li{display:grid;grid-template-columns:120px 1fr;gap:20px;padding:16px 0;border-bottom:1px solid var(--ln)}

.more-name{font:500 14px/1.9 var(--mono)}

.more-list p{display:inline;color:var(--mu);font-size:13px;line-height:2}

.more-list .project-status{margin-inline-start:8px}

.more-list .tags{margin-top:8px}

.skills-grid{border-top:1px solid var(--ln)}

.skill-card{display:grid;grid-template-columns:190px 1fr;gap:28px;padding:18px 0;border-bottom:1px solid var(--ln)}

.skill-card h3{font-size:14px;font-weight:600}

.skill-card p{color:var(--mu);font-size:13px;line-height:2}

.skill-card .tags{margin-top:10px}

.skill-level-note{margin-top:20px;color:var(--fa);font-size:12px;line-height:2}

.closing-grid{display:grid;grid-template-columns:1fr 1fr;gap:40px}

.education-card{padding:20px;background:var(--s1);border:1px solid var(--ln);border-radius:var(--r)}

.education-kicker{margin-bottom:6px;color:var(--ac);font-size:12px}

.education-title{font-size:16px;font-weight:600}

.education-detail{margin-top:6px;color:var(--mu);font-size:13px}

.knowledge-list{border-top:1px solid var(--ln)}

.knowledge-row{display:flex;justify-content:space-between;align-items:baseline;gap:16px;padding:12px 0;border-bottom:1px solid var(--ln)}

.knowledge-row strong{font-size:13px;font-weight:500}

.knowledge-row span{color:var(--mu);font-size:12px}

.contact-section>.container{display:block}

.contact-intro{max-width:760px;margin-bottom:32px}

.eyebrow{display:flex;align-items:center;gap:10px;margin-bottom:14px;color:var(--mu);font-size:12px}

.eyebrow::before{content:'';width:20px;height:1px;background:var(--ac)}

.contact-title{font-size:clamp(34px,5vw,56px);font-weight:800;line-height:1.4}

.contact-description{max-width:60ch;margin-top:12px;color:var(--mu);font-size:14px;line-height:2.1}

.contact-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}

.contact-card{display:flex;align-items:center;gap:14px;min-height:76px;padding:14px 16px;background:var(--s1);border:1px solid var(--ln);border-radius:var(--r);transition:border-color .2s}

.contact-card:hover{border-color:var(--ln2)}

.contact-icon{display:grid;place-items:center;flex:none;width:34px;height:34px;border:1px solid var(--ln2);border-radius:6px;color:var(--soft);font:500 10px var(--mono);direction:ltr}

.contact-card-copy{display:flex;flex-direction:column;min-width:0}

.contact-card-copy strong{font-size:13px;font-weight:600}

.contact-value{color:var(--mu);font:400 12px/1.7 var(--mono);direction:ltr;text-align:right}

.footer{display:flex;justify-content:space-between;gap:16px;padding-block:22px;border-top:1px solid var(--ln);color:var(--fa);font-size:12px}

.footer-right{font-family:var(--mono);direction:ltr}

@media(max-width:960px){.container{width:min(calc(100% - 40px),var(--w))}.section>.container{grid-template-columns:1fr;row-gap:28px}.section>.container>*,.section>.container>.section-head{grid-column:1;grid-row:auto}.quickfacts-grid,.contact-grid{grid-template-columns:repeat(2,1fr)}.nav-inner{flex-direction:column;align-items:flex-start;padding-block:14px;gap:10px}.hero-portrait-image{max-width:100%;opacity:.25}}

@media(max-width:640px){.focus-list,.projects-grid,.closing-grid,.contact-grid,.quickfacts-grid{grid-template-columns:1fr}.experience-item,.skill-card,.more-list li{grid-template-columns:1fr;gap:10px}.hero{min-height:0;padding:64px 0 56px}.footer{flex-direction:column}}

@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto}*{transition:none!important}}

/* Print / PDF: A4, backgrounds kept, natural flow with no clipped content */

@page{size:A4;margin:9mm}

@media print{

html,body{background:#0a0a0a!important;-webkit-print-color-adjust:exact;print-color-adjust:exact}

body{font-size:10.5px;line-height:1.8}

.topbar{display:none}

.container{width:100%;padding-inline:3mm}

.print-page-work,.print-page-capabilities{break-before:page}

.hero{min-height:0;padding:12mm 0 10mm}

.hero h1{font-size:44pt}

.quickfacts-grid{margin-block:6mm}

.section{padding-block:7mm}

.section>.container{grid-template-columns:42mm 1fr;column-gap:8mm}

.section-title{font-size:19pt}

.project-card,.focus-item,.experience-item,.skill-card,.more-list li,.contact-card,.education-card,.knowledge-row{break-inside:avoid}

.project-card{padding:4mm}.experience-item{padding:4mm 0}.skill-card{padding:3mm 0}

a{text-decoration:none!important}

}



/* ===== v3: design scales + component craft ===== */

:root{--fs-xs:12px;--fs-sm:13px;--fs-md:15px;--fs-lg:18px;--fs-xl:clamp(24px,3vw,32px);--fs-2xl:clamp(34px,5vw,56px);--sp-1:4px;--sp-2:8px;--sp-3:12px;--sp-4:16px;--sp-5:24px;--sp-6:32px;--sp-7:48px;--sp-8:72px;--r2:12px}

.section{padding-block:var(--sp-8)}

.section-title{font-size:var(--fs-xl)}

.section-lede,.focus-item p,.project-description,.skill-card p{font-size:var(--fs-sm)}

.head-meta{display:grid;gap:var(--sp-2);margin-top:var(--sp-5);padding-top:var(--sp-4);border-top:1px solid var(--ln);color:var(--mu);font-size:var(--fs-xs);line-height:1.8}

.head-meta b{color:var(--tx);font:600 var(--fs-lg) var(--sans);margin-inline-end:4px}

.lg{display:flex;align-items:center;gap:var(--sp-3)}

/* Hero signal trace: analog burst, digital pulse, spike */

.hero-signal{position:absolute;inset-inline:0;bottom:40px;width:100%;height:150px;z-index:0;opacity:.55;pointer-events:none;-webkit-mask-image:linear-gradient(90deg,transparent,#000 22%,#000 78%,transparent);mask-image:linear-gradient(90deg,transparent,#000 22%,#000 78%,transparent)}

.hero-signal path{fill:none;stroke:var(--ac);stroke-width:1.5;stroke-linejoin:round;vector-effect:non-scaling-stroke}

.hero-signal .base{stroke:var(--ln2);stroke-width:1;stroke-dasharray:2 7}

.quickfact:first-child .quickfact-value{display:flex;align-items:baseline;gap:var(--sp-2)}

.metric{font:700 clamp(34px,4vw,46px)/1 var(--sans);color:var(--tx)}

/* Skill level scale */

.tag,.lv{--c2:var(--ln2);--c3:var(--ln2);--glyph:linear-gradient(270deg,var(--ac) 0 4px,transparent 4px 5px,var(--c2) 5px 9px,transparent 9px 10px,var(--c3) 10px 14px)}

[data-l="2"]{--c2:var(--ac)}

[data-l="3"]{--c2:var(--ac);--c3:var(--ac)}

.lv{display:inline-block;flex:none;width:14px;height:7px;border-radius:1px;background:var(--glyph)}

.tag[data-l]{display:inline-flex;align-items:center;gap:7px}

.tag[data-l]::before{content:'';flex:none;width:14px;height:7px;border-radius:1px;background:var(--glyph)}

/* Experience: timeline rail + tenure chart */

.tenure{margin-bottom:var(--sp-6);padding:var(--sp-4) var(--sp-5);background:var(--s1);border:1px solid var(--ln);border-radius:var(--r2)}

.tn-row{display:grid;grid-template-columns:130px 1fr;gap:var(--sp-4);align-items:center;padding-block:5px;font-size:var(--fs-xs);color:var(--soft)}

.tn-row span{direction:ltr;unicode-bidi:isolate;text-align:right;font-family:var(--mono)}

.tn-track{position:relative;height:8px;background:repeating-linear-gradient(270deg,var(--ln) 0 1px,transparent 1px 8.333%)}

.tn-track i{position:absolute;inset-block:0;inset-inline-start:calc(var(--s)*1%);width:calc(var(--w)*1%);min-width:6px;border-radius:2px;background:var(--ac)}

.tn-axis{display:flex;justify-content:space-between;margin-top:var(--sp-2);padding-inline-start:calc(130px + var(--sp-4));color:var(--fa);font-size:11px}

.experience-list{border-top:0;border-inline-start:1px solid var(--ln2)}

.experience-item{position:relative;padding-inline-start:var(--sp-6)}

.experience-item::before{content:'';position:absolute;top:36px;inset-inline-start:-4px;width:7px;height:7px;border-radius:50%;background:var(--ac);box-shadow:0 0 0 4px var(--bg)}

.live{display:inline-block;margin-inline-start:var(--sp-2);padding:0 8px;border:1px solid rgba(239,48,42,.38);border-radius:999px;color:#ff9b97;font-size:11px}

/* Projects & contact */

.project-card{padding:var(--sp-5);border-radius:var(--r2)}

.project-card::before{content:'';position:absolute;top:-1px;inset-inline-start:var(--sp-5);width:28px;height:2px;background:var(--ac)}

.project-title{font-size:22px}

.quickfacts-grid{border-radius:var(--r2)}

.contact-card{border-radius:var(--r2)}

.contact-card.wide{grid-column:span 2}

.contact-card.wide .contact-value{font-size:var(--fs-sm);color:var(--soft)}

@media(max-width:640px){.contact-card.wide{grid-column:auto}.tn-row{grid-template-columns:96px 1fr}.tn-axis{padding-inline-start:calc(96px + var(--sp-4))}}

@media print{.tenure,.head-meta{break-inside:avoid}.hero-signal{opacity:.45}.experience-item::before{top:5mm}}

</style>

</head>

<body>

<header class="topbar">

  <div class="container nav-inner">

    <a class="brand" href="#top" aria-label="مهدی قورچی، ابتدای صفحه">

      <span class="brand-copy"><strong>مهدی قورچی</strong><span>SOFTWARE · AI · ENGINEERING</span></span>

    </a>

    <nav aria-label="بخش‌های رزومه">

      <ul class="nav-links">

        <li><a href="#about">درباره من</a></li>

        <li><a href="#experience">تجربه</a></li>

        <li><a href="#projects">پروژه‌ها</a></li>

        <li><a href="#skills">مهارت‌ها</a></li>

        <li><a href="#education">تحصیلات</a></li>

        <li><a href="#contact">ارتباط</a></li>

      </ul>

    </nav>

  </div>

</header>

<main id="top">

  <div class="print-page print-page-intro">

  <section class="hero" aria-labelledby="hero-title">

    <svg class="hero-signal" viewBox="0 0 1200 150" preserveAspectRatio="none" aria-hidden="true" focusable="false"><path class="base" d="M0 75H1200"/><path d="M0 75H180C200 75 205 25 230 25S260 125 285 125S315 25 340 25S370 75 390 75H470V35H520V115H570V35H620V75H760L780 75L800 5L825 135L845 75H1000C1030 75 1040 45 1065 45S1100 105 1125 105S1150 75 1175 75H1200"/></svg>

    <!-- تصویر پرترهٔ شفاف در کنار همین فایل قرار دارد. -->

    <!-- TODO: mahdi-photo.png (PNG شفاف) را کنار این فایل قرار دهید؛ اگر نباشد، هیرو بدون عکس نمایش داده می‌شود -->

    <img class="hero-portrait-image" src="mahdi-photo.png" alt="" aria-hidden="true" fetchpriority="high" onerror="this.remove()">

    <div class="container hero-grid">

      <div class="hero-copy">

        <h1 id="hero-title">مهدی قورچی<span class="hero-name-en">MAHDI GHOURCHI</span></h1>

        <p class="hero-role"><span>توسعه‌دهنده بک‌اند و هوش مصنوعی</span><span class="sep"></span><span class="ltr">Backend &amp; AI Engineering</span></p>

        <p class="hero-description">دانشجوی کارشناسی مهندسی برق با بیش از شش سال تجربه در حوزه کامپیوتر و توسعه نرم‌افزار. تمرکز اصلی من بر <strong>توسعه سرویس‌های بک‌اند، طراحی API و یکپارچه‌سازی قابلیت‌های هوش مصنوعی</strong> در محصولات نرم‌افزاری است؛ در کنار آن، به سیستم‌های نهفته و کاربردهای بین‌رشته‌ای مهندسی نیز می‌پردازم.</p>

        <div class="hero-meta"><span class="meta-pill">Python · API</span><span class="meta-pill">LLM Integration</span><span class="meta-pill">مهندسی برق</span></div>

        <div class="hero-links"><a href="https://github.com/Mahdi-ghourchi">github.com/Mahdi-ghourchi</a><a href="https://www.linkedin.com/in/mahdi-ghourchi/">linkedin.com/in/mahdi-ghourchi</a><a href="https://t.me/meti0010001">t.me/meti0010001</a></div>

      </div>

    </div>

  </section>

<section class="section" id="about" aria-labelledby="about-title">

  <div class="container">

    <header class="section-head">

      <div class="section-title-wrap">

        <h2 class="section-title" id="about-title">

          حوزه‌های تخصصی

        </h2>

      </div>

    </header>



    <div class="focus-list" aria-label="حوزه‌های تخصصی و مکمل">

      <article class="focus-item">

        <div>

          <h3>مهندسی برق و سیستم‌های نهفته</h3>

          <p>

            الکترونیک، میکروکنترلرها و ارتباط میان نرم‌افزار و سخت‌افزار؛

            با تمرکز بر پلتفرم‌هایی مانند Arduino، ESP32 و STM32.

          </p>

        </div>

      </article>



      <article class="focus-item">

        <div>

          <h3>هوش مصنوعی و سیستم‌های هوشمند</h3>

          <p>

            یکپارچه‌سازی مدل‌های زبانی و APIهای هوش مصنوعی و بررسی

            کاربرد عامل‌های هوشمند در فرایندها و محصولات نرم‌افزاری.

          </p>

        </div>

      </article>



      <article class="focus-item">

        <div>

          <h3>توسعه بک‌اند و معماری API</h3>

          <p>

            پیاده‌سازی سرویس‌های Python، طراحی و مستندسازی API و

            یکپارچه‌سازی اجزای نرم‌افزاری با استفاده از Flask و FastAPI.

          </p>

        </div>

      </article>



      <article class="focus-item">

        <div>

          <h3>زیرساخت و مهندسی نرم‌افزار</h3>

          <p>

            کار با Linux، Git و Docker در کنار آشنایی با مفاهیم

            استقرار، مدیریت محیط اجرا و فرایندهای DevOps.

          </p>

        </div>

      </article>



      <article class="focus-item">

        <div>

          <h3>بیوانفورماتیک و علوم زیستی</h3>

          <p>

            علاقه‌مندی میان‌رشته‌ای به زیست‌شناسی سلولی، ژنتیک و

            کاربرد محاسبات و هوش مصنوعی در مسائل علوم زیستی؛

            همسو با جهت‌گیری پژوهشی SYNAPSE.

          </p>

        </div>

      </article>



      <article class="focus-item">

        <div>

          <h3>طراحی و ابزارهای مهندسی</h3>

          <p>

            کار با SolidWorks و Altium Designer در زمینه طراحی

            مکانیکی و الکترونیکی و توسعه طرح‌های مهندسی.

          </p>

        </div>

      </article>

    </div>

  </div>

</section>

  </div>

  <div class="print-page print-page-work">

  <section class="section" id="experience" aria-labelledby="experience-title">

    <div class="container">

      <header class="section-head"><div class="section-title-wrap"><h2 class="section-title" id="experience-title">تجربه و همکاری‌ها</h2><p class="section-lede">فعالیت در تیم نرم‌افزاری، پیشبرد کارهای تحقیقاتی و شکل‌دهی مسیر فنی یک تیم مهندسی.</p><div class="head-meta"><span><b>۳</b>نقش فعال</span><span>هر سه نقش هم‌اکنون ادامه دارند.</span><span style="color: #ef302a;">فعالیت های فعلی به صورت تیمی و یا پاره وقت هستند.</span></div></div></header>

      <div class="tenure" role="img" aria-label="نمودار زمانی نقش‌ها از آذر ۱۴۰۳ تا اکنون"><div class="tn-row"><span>SYNAPSE</span><div class="tn-track"><i style="--s:95.5;--w:4.5"></i></div></div><div class="tn-row"><span>Research Team</span><div class="tn-track"><i style="--s:47.8;--w:52.2"></i></div></div><div class="tn-row"><span>Rasta Game</span><div class="tn-track"><i style="--s:0;--w:100"></i></div></div><div class="tn-axis"><span>آذر ۱۴۰۳</span><span>اکنون</span></div></div>

      <div class="experience-list">

        <article class="experience-item">

          <div class="experience-meta"><span class="experience-type">بنیان‌گذاری و مهندس داده</span><h3 class="experience-role">بنیان‌گذار و مدیر فنی</h3><p class="experience-org ltr">SYNAPSE</p><p class="experience-date">مهر ۱۴۰۵ — اکنون<span class="live">فعال</span></p></div>

          <div class="experience-copy"><p>SYNAPSE تیمی مهندسی در تقاطع بیوانفورماتیک و هوش مصنوعی است. تمرکز نقش من بر جهت‌گیری فنی، طراحی API، معماری سیستم و توسعه بک‌اند قرار دارد.</p><div class="tags"><span class="tag">AI</span><span class="tag">Bioinformatics</span><span class="tag">Backend</span><span class="tag">System Architecture</span></div></div>

        </article>

        <article class="experience-item">

          <div class="experience-meta"><span class="experience-type">تحقیق و توسعه</span><h3 class="experience-role">مدیر پروژه</h3><p class="experience-org">تیم تحقیقاتی دانشگاهی</p><p class="experience-date">آبان ۱۴۰۴ — اکنون<span class="live">فعال</span></p></div>

          <div class="experience-copy"><p>هماهنگی فعالیت‌های تحقیق‌وتوسعه درباره فناوری‌های نوین هوش مصنوعی و بررسی کاربردهای صنعتی آن‌ها.</p><div class="tags"><span class="tag">R&amp;D</span><span class="tag">AI</span><span class="tag">Project Coordination</span></div></div>

        </article>

        <article class="experience-item">

          <div class="experience-meta"><span class="experience-type">توسعه نرم‌افزار</span><h3 class="experience-role">توسعه‌دهنده بک‌اند</h3><p class="experience-org ltr">Rasta Game</p><p class="experience-date">آذر ۱۴۰۳ — اکنون<span class="live">فعال</span></p></div>

          <div class="experience-copy"><p>توسعه و نگهداری سرویس‌های بک‌اند با Flask و FastAPI، طراحی و مستندسازی APIها، یکپارچه‌سازی سرویس‌ها و اتصال مدل‌ها و APIهای هوش مصنوعی به محصولات نرم‌افزاری. همچنین مشارکت در فرایند استقرار با Docker و Linux.</p><p>رستا گیم یک تیم و استارتاپ گیمینگ است که روی پلتفرم معرفی بازی‌ها، کتابخانه بازی‌های آنلاین و اطلاعات گیم‌سرورها کار می‌کند.</p><div class="tags"><span class="tag">Python</span><span class="tag">Flask</span><span class="tag">FastAPI</span><span class="tag">Docker</span><span class="tag">Linux</span></div></div>

        </article>

      </div>

    </div>

  </section>

  </div>

  <div class="print-page print-page-projects">

  <section class="section" id="projects" aria-labelledby="projects-title">

    <div class="container">

      <header class="section-head"><div class="section-title-wrap"><h2 class="section-title" id="projects-title">پروژه‌ها و فعالیت‌های مهندسی</h2><p class="section-lede">چند مسیر منتخب در توسعه نرم‌افزار و مهندسی. وضعیت پروژه‌ها عمداً واقع‌بینانه بیان شده و نتیجه یا قابلیت اندازه‌گیری‌نشده‌ای ادعا نشده است.</p><div class="head-meta"><span><b>۱۲</b>پروژه</span><span>شش مورد برجسته و شش مورد در فهرست فشرده</span></div></div></header>

      <div class="projects-grid"><article class="project-card"><div class="project-top"><h3 class="project-title ltr">Chatloom</h3></div><p class="project-description">عامل مکالمه‌محور مبتنی بر هوش مصنوعی با تمرکز بر یکپارچه‌سازی مدل‌های زبانی و پیاده‌سازی تعامل متنی هوشمند.</p><div class="tags"><span class="tag">LLM Integration</span><span class="tag">AI Agent</span><span class="tag">Chatbot</span></div></article><article class="project-card"><div class="project-top"><h3 class="project-title ltr">ApiBeacon</h3></div><p class="project-description">سامانه پایش API برای بررسی وضعیت سرویس‌ها و نمایش اطلاعات نظارتی در قالب یک داشبورد متمرکز.</p><div class="tags"><span class="tag">API Monitoring</span><span class="tag">Backend</span><span class="tag">Observability</span></div></article><article class="project-card"><div class="project-top"><h3 class="project-title ltr">TraceCLI</h3></div><p class="project-description">عامل خط فرمان برای تحلیل ساختار پروژه‌های نرم‌افزاری و بررسی کدبیس با بهره‌گیری از قابلیت‌های مدل‌های زبانی.</p><div class="tags"><span class="tag">CLI</span><span class="tag">Codebase Analysis</span><span class="tag">LLM</span></div></article><article class="project-card"><div class="project-top"><h3 class="project-title ltr">TeleDash</h3></div><p class="project-description">داشبورد مدیریتی ربات‌های تلگرام با هدف متمرکزسازی کنترل، مدیریت قابلیت‌ها و یکپارچه‌سازی عملیات ربات‌ها.</p><div class="tags"><span class="tag">Telegram Bot API</span><span class="tag">API Integration</span><span class="tag">Dashboard</span></div></article><article class="project-card"><div class="project-top"><h3 class="project-title ltr">Handwave</h3></div><p class="project-description">سامانه احراز تعامل انسانی مبتنی بر تشخیص حرکات دست از طریق وب‌کم، با تمرکز بر تعامل بدون تماس و حفظ حریم خصوصی کاربران.</p><div class="tags"><span class="tag">Computer Vision</span><span class="tag">Gesture Recognition</span><span class="tag">Privacy-Aware</span></div></article><article class="project-card"><div class="project-top"><h3 class="project-title ltr">DataCanvas</h3></div><p class="project-description">داشبورد تعاملی تحلیل و نمایش داده با قابلیت مرتب‌سازی، سازمان‌دهی مجموعه‌داده‌ها و بررسی بصری اطلاعات.</p><div class="tags"><span class="tag">Data Visualization</span><span class="tag">Data Processing</span><span class="tag">Interactive Dashboard</span></div></article></div><div class="more"><h3 class="subheading">پروژه‌های دیگر</h3><ul class="more-list"><li><h4 class="more-name ltr">DirPilot</h4><div><p>عامل هوشمند مدیریت فایل و پوشه با هدف خودکارسازی عملیات فایل‌سیستم و تسهیل تعامل با ساختارهای محلی.</p><div class="tags"><span class="tag">AI Agent</span><span class="tag">Filesystem</span><span class="tag">Automation</span></div></div></li><li><h4 class="more-name ltr">FetchFox</h4><div><p>ربات دانلود با هدف ساده‌سازی فرایند دریافت محتوا و اجرای گردش‌کارهای دانلود از طریق رابط مبتنی بر پیام‌رسان.</p><div class="tags"><span class="tag">Bot Development</span><span class="tag">Automation</span><span class="tag">Download Workflow</span></div></div></li><li><h4 class="more-name ltr">Stayform</h4><div><p>وب‌سایت رزرو اتاق هتل با تمرکز بر فرایند ثبت درخواست، دریافت اطلاعات کاربر و مدیریت جریان رزرو.</p><div class="tags"><span class="tag">Web Development</span><span class="tag">Booking Workflow</span><span class="tag">Web Forms</span></div></div></li><li><h4 class="more-name ltr">ShroomRun</h4><div><p>بازی دوبعدی تحت وب با الهام از سبک سکوبازی کلاسیک، شامل منطق حرکت، تعامل با محیط و مدیریت وضعیت بازی.</p><div class="tags"><span class="tag">Browser Game</span><span class="tag">Game Logic</span><span class="tag">Interactive UI</span></div></div></li><li><h4 class="more-name ltr">Driftline</h4><div><p>بازی رانندگی تحت وب با تمرکز بر کنترل حرکت، تشخیص برخورد و پیاده‌سازی مکانیزم‌های تعامل و موانع.</p><div class="tags"><span class="tag">Browser Game</span><span class="tag">Collision Detection</span><span class="tag">Game Mechanics</span></div></div></li><li><h4 class="more-name ltr">TextDock</h4><div><p>طرح اولیه محیط کار با متن با رویکرد Local-first؛ با بررسی معماری رابط React و سرویس پشتیبان FastAPI.</p><span class="project-status">طرح اولیه</span><div class="tags"><span class="tag">Local-first</span><span class="tag">React</span><span class="tag">FastAPI</span></div></div></li></ul></div>

    </div>

  </section>

  </div>

  <div class="print-page print-page-capabilities">

  <section class="section" id="skills" aria-labelledby="skills-title">

    <div class="container">

      <header class="section-head"><div class="section-title-wrap"><h2 class="section-title" id="skills-title">مهارت‌ها در چند حوزه</h2><p class="section-lede">فناوری‌ها و زمینه‌های دانشی بر اساس کاربرد دسته‌بندی شده‌اند؛ بدون رتبه‌بندی عددی یا ادعای تسلط یکسان بر همه موارد.</p><div class="head-meta"><span class="lg"><i class="lv" data-l="3"></i>کاربرد روزمره</span><span class="lg"><i class="lv" data-l="2"></i>کاربرد در پروژه‌ها</span><span class="lg"><i class="lv" data-l="1"></i>در حال یادگیری یا آشنایی</span><span>سطح‌بندی کیفی است، نه عددی.</span></div></div></header>

      <div class="skills-grid"><article class="skill-card"><h3>بک‌اند و طراحی API</h3><div><p>Python، Flask، FastAPI، Django، طراحی و مستندسازی API و یکپارچه‌سازی سرویس‌ها.</p><div class="tags"><span class="tag" data-l="3">Python</span><span class="tag" data-l="3">Flask</span><span class="tag" data-l="3">FastAPI</span><span class="tag" data-l="2">Django</span><span class="tag" data-l="2">REST</span></div></div></article><article class="skill-card"><h3>هوش مصنوعی و LLM</h3><div><p>یکپارچه‌سازی LLM و AI API، کار با مدل‌های آماده، AI Agent و توسعه نرم‌افزار با کمک هوش مصنوعی؛ آشنایی و فعالیت در حوزه ML / Deep Learning.</p><div class="tags"><span class="tag" data-l="2">LLM</span><span class="tag" data-l="2">AI Agents</span><span class="tag" data-l="1">ML / DL</span></div></div></article><article class="skill-card"><h3>ابزارهای توسعه و DevOps</h3><div><p>Linux، Git، Docker و مفاهیم توسعه، دیباگ، استقرار و نگهداری سرویس‌ها.</p><div class="tags"><span class="tag" data-l="3">Linux</span><span class="tag" data-l="3">Git</span><span class="tag" data-l="3">Docker</span></div></div></article><article class="skill-card"><h3>سیستم‌های نهفته و IoT</h3><div><p>Arduino، ESP32، STM32 و مفاهیم اتصال سخت‌افزار به نرم‌افزار.</p><div class="tags"><span class="tag" data-l="2">Arduino</span><span class="tag" data-l="2">ESP32</span><span class="tag" data-l="2">STM32</span></div></div></article><article class="skill-card"><h3>طراحی مهندسی</h3><div><p>SolidWorks و Altium Designer؛ طراحی مکانیکی و طراحی مدار در چارچوب فعالیت‌های مهندسی.</p><div class="tags"><span class="tag" data-l="1">SolidWorks</span><span class="tag" data-l="1">Altium Designer</span></div></div></article><article class="skill-card"><h3>علوم زیستی و بیوانفورماتیک</h3><div><p>آشنایی با مفاهیم بیوانفورماتیک، زیست‌شناسی سلولی و ژنتیک؛ زمینه‌های مکمل فعالیت بین‌رشته‌ای.</p><div class="tags"><span class="tag" data-l="1">Bioinformatics</span><span class="tag" data-l="1">Genetics</span></div></div></article></div>

      <div class="skill-level-note">حوزه‌های فنی و دانشی بر اساس کاربرد دسته‌بندی شده‌اند؛ نوع و میزان استفاده از هر ابزار به پروژه و نیاز آن بستگی دارد.</div>

    </div>

  </section>



  <section class="section" id="education" aria-labelledby="education-title-section">

    <div class="container">

      <header class="section-head"><div class="section-title-wrap"><h2 class="section-title" id="education-title-section">تحصیلات و زمینه‌های علمی</h2><p class="section-lede">پایه مهندسی در کنار علاقه به نرم‌افزار و موضوعات علمی بین‌رشته‌ای.</p></div></header>

      <div class="closing-grid">

        <div><h3 class="subheading">تحصیلات</h3><article class="education-card"><p class="education-kicker">در حال تحصیل</p><h4 class="education-title">کارشناسی مهندسی برق</h4><p class="education-detail">دانشگاه تفرش؛ در حال تحصیل در مقطع کارشناسی.</p></article></div>

        <div><h3 class="subheading">زمینه‌های مکمل</h3><div class="knowledge-list"><div class="knowledge-row"><strong>الکترونیک و سیستم‌های فیزیکی</strong><span>هم‌راستا با مهندسی برق</span></div><div class="knowledge-row"><strong>سیستم‌های نهفته و IoT</strong><span class="ltr">Arduino · ESP32 · STM32</span></div><div class="knowledge-row"><strong>علوم زیستی و محاسباتی</strong><span>بیوانفورماتیک · سلولی · ژنتیک</span></div></div></div>

      </div>

    </div>

  </section>



  <section class="section contact-section" id="contact" aria-labelledby="contact-title">

    <div class="container">

      <div class="contact-intro">

        <p class="eyebrow">ارتباط حرفه‌ای</p>

        <h2 class="contact-title" id="contact-title">گفت‌وگو درباره ساختن</h2>

        <p class="contact-description">برای همکاری یا گفت‌وگو درباره توسعه بک‌اند، یکپارچه‌سازی هوش مصنوعی، پروژه‌های مهندسی و فعالیت‌های تحقیق‌وتوسعه.</p>

      </div>

      <div class="contact-grid" aria-label="شبکه‌های اجتماعی و راه‌های ارتباطی">

        <!-- اطلاعات نمونه را با اطلاعات واقعی خود جایگزین کنید. -->

        <a class="contact-card wide" href="mailto:mahdi.ghourchi.me@gmail.com"><span class="contact-icon">@</span><span class="contact-card-copy"><strong>ایمیل</strong><span class="contact-value">Mahdi.Ghourchi.me@example.com</span></span></a>

        <a class="contact-card" href="tel:+989982401191"><span class="contact-icon">TEL</span><span class="contact-card-copy"><strong>شماره تماس</strong><span class="contact-value">+989982401191</span></span></a>

        <a class="contact-card" href="https://t.me/meti0010001"><span class="contact-icon">TG</span><span class="contact-card-copy"><strong>تلگرام</strong><span class="contact-value">@meti0010001</span></span></a>

        <!-- TODO: wa.me معمولاً شماره تلفن می‌خواهد (فقط ارقام)، نه username؛ بررسی کنید -->

        <a class="contact-card" href="https://wa.me/meti0010001"><span class="contact-icon">WA</span><span class="contact-card-copy"><strong>واتساپ</strong><span class="contact-value">@meti0010001</span></span></a>

        <a class="contact-card" href="https://www.linkedin.com/in/mahdi-ghourchi/"><span class="contact-icon">in</span><span class="contact-card-copy"><strong>لینکدین</strong><span class="contact-value">linkedin.com/in/mahdi-ghourchi</span></span></a>

        <a class="contact-card" href="https://github.com/Mahdi-ghourchi"><span class="contact-icon">GH</span><span class="contact-card-copy"><strong>گیت‌هاب</strong><span class="contact-value">github.com/Mahdi-ghourchi</span></span></a>

      </div>

    </div>

  </section>

  </div>

</main>

<footer class="container footer"><span>مهدی قورچی</span><span class="footer-right" aria-hidden="true">BACKEND / AI / ENGINEERING</span></footer>

</body>

</html>
```
