<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>مواهب — اكتشف موهبتك، طوّرها، وخلّ العالم يشوفها</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Alexandria:wght@400;500;600;700;800;900&family=IBM+Plex+Sans+Arabic:wght@400;500;600;700&family=Amiri:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">
<style>
  :root{
    /* نظام «مواهب لَكْس»: أوبسيديان زمردي × ذهب */
    --bg:#0B0F0D; --bg2:#0E1411;
    --surface:#131A17; --surface2:#1A2320; --surface3:#202B27;
    --line:rgba(217,180,90,.16); --line2:rgba(255,255,255,.07);
    --gold:#D9B45A; --gold2:#F2DD9B; --gold-d:#A8843A;
    --ink:#F4F1E6; --muted:#9AAB A3;
    --muted:#98A9A1;
    --good:#3DDBB4;
    /* توافق خلفي مع الأسماء القديمة */
    --deep:#12352D; --deep2:#0B211C;
    --teal:#1FBF9C; --teal-bright:#2BD9B4;
    --warm:#D9B45A; --warm-d:#A8843A; --warm-soft:rgba(217,180,90,.13);
    --shadow:0 24px 60px -20px rgba(0,0,0,.65);
    --shadow-sm:0 12px 30px -14px rgba(0,0,0,.55);
    --glow-gold:0 0 0 1px rgba(217,180,90,.35),0 14px 40px -12px rgba(217,180,90,.28);
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{font-family:'IBM Plex Sans Arabic',sans-serif;background:var(--bg);color:var(--ink);-webkit-font-smoothing:antialiased;line-height:1.65;
    background-image:radial-gradient(1100px 500px at 85% -10%,rgba(31,191,156,.07),transparent 60%),radial-gradient(900px 480px at 0% 8%,rgba(217,180,90,.05),transparent 55%)}
  h1,h2,h3,h4,.dsp{font-family:'Alexandria',sans-serif}
  ::selection{background:rgba(217,180,90,.35)}
  @media (prefers-reduced-motion:reduce){*{transition:none!important;animation:none!important}html{scroll-behavior:auto}}

  /* ===== شريط التنقّل ===== */
  .nav{position:sticky;top:0;z-index:50;background:rgba(10,13,12,.82);backdrop-filter:blur(16px);color:#fff;border-bottom:1px solid var(--line)}
  .nav-in{max-width:1220px;margin:0 auto;padding:14px 24px;display:flex;align-items:center;gap:22px}
  .brand{display:flex;align-items:center;gap:11px;font-family:'Alexandria';font-weight:900;font-size:20px;flex-shrink:0;letter-spacing:.01em}
  .brand .m{width:38px;height:38px;border-radius:12px;background:linear-gradient(135deg,var(--gold2),var(--gold) 55%,var(--gold-d));color:#141109;display:flex;align-items:center;justify-content:center;font-size:19px;box-shadow:0 6px 18px -4px rgba(217,180,90,.55)}
  .links{display:flex;gap:2px;margin-right:auto;flex-wrap:wrap}
  .links button{background:none;border:none;color:#AEBDB6;font-family:'IBM Plex Sans Arabic';font-size:14.5px;font-weight:500;cursor:pointer;padding:9px 15px;border-radius:10px;transition:all .2s}
  .links button:hover{color:var(--gold2);background:rgba(217,180,90,.07)}
  .links button.on{color:var(--gold2);background:rgba(217,180,90,.12);box-shadow:inset 0 0 0 1px rgba(217,180,90,.3)}
  .links button:focus-visible{outline:2px solid var(--gold);outline-offset:2px}
  .nav-badge{font-size:11.5px;color:var(--gold);border:1px solid var(--line);padding:7px 14px;border-radius:999px;flex-shrink:0;white-space:nowrap;letter-spacing:.06em;background:rgba(217,180,90,.05)}
  @media(max-width:880px){.nav-badge{display:none}.nav-in{gap:10px}.links button{padding:8px 11px;font-size:13.5px}}

  .view{display:none;animation:fade .5s ease}
  .view.active{display:block}
  @keyframes fade{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
  .wrap{max-width:1220px;margin:0 auto;padding:0 24px}
  .section{padding:60px 0}
  .eyebrow{display:inline-flex;align-items:center;gap:9px;font-size:12.5px;letter-spacing:.14em;color:var(--gold);border:1px solid var(--line);padding:8px 18px;border-radius:999px;font-weight:600;background:rgba(217,180,90,.05)}
  .eyebrow::before{content:"✦";font-size:11px;color:var(--gold)}

  /* أزرار */
  .btn{border:none;cursor:pointer;font-family:'Alexandria';font-weight:700;font-size:15.5px;padding:15px 28px;border-radius:14px;transition:transform .15s,box-shadow .25s,filter .2s;display:inline-flex;align-items:center;gap:9px;text-decoration:none}
  .btn:active{transform:scale(.97)}
  .btn-primary{background:linear-gradient(135deg,var(--gold2),var(--gold) 55%,var(--gold-d));color:#161207;box-shadow:0 14px 34px -10px rgba(217,180,90,.5)}
  .btn-primary:hover{box-shadow:0 20px 44px -10px rgba(217,180,90,.6);transform:translateY(-2px);filter:brightness(1.05)}
  .btn-ghost{background:transparent;color:var(--gold2);border:1px solid var(--line)}
  .btn-ghost:hover{border-color:var(--gold);background:rgba(217,180,90,.07)}
  .btn:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .btn-sm{padding:11px 19px;font-size:14px;border-radius:12px}

  /* ===== الرئيسية ===== */
  .hero{position:relative;overflow:hidden;border-bottom:1px solid var(--line)}
  .hero::before{content:"";position:absolute;width:760px;height:760px;border-radius:50%;background:radial-gradient(circle,rgba(217,180,90,.16),transparent 62%);top:-320px;left:-160px;pointer-events:none}
  .hero::after{content:"";position:absolute;width:520px;height:520px;border-radius:50%;background:radial-gradient(circle,rgba(31,191,156,.12),transparent 65%);bottom:-220px;right:-120px;pointer-events:none}
  .hero-in{position:relative;z-index:2;display:grid;grid-template-columns:1.15fr .85fr;gap:48px;align-items:center;padding:84px 0 92px}
  .hero h1{font-size:52px;font-weight:900;line-height:1.24;margin:26px 0 20px;letter-spacing:-.01em}
  .hero h1 .hl{background:linear-gradient(100deg,var(--gold-d),var(--gold) 30%,var(--gold2) 50%,var(--gold) 70%,var(--gold-d));background-size:220% auto;-webkit-background-clip:text;background-clip:text;color:transparent;animation:shimmer 5.5s linear infinite}
  @keyframes shimmer{to{background-position:-220% center}}
  .hero p.lead{font-size:17.5px;color:#C3CFC8;line-height:1.95;margin-bottom:18px;max-width:540px}
  .quote{border-right:2px solid var(--gold);padding:8px 18px;margin:26px 0 30px;color:#E8E2CF;font-size:16px;max-width:520px;font-family:'Amiri',serif;line-height:1.9}
  .quote span{display:block;color:var(--gold);font-size:12.5px;margin-top:8px;font-family:'IBM Plex Sans Arabic';letter-spacing:.04em}
  .hero-cta{display:flex;gap:14px;flex-wrap:wrap}
  .hero-art{position:relative;height:380px;display:flex;align-items:center;justify-content:center}
  .ring{position:absolute;border:1px solid rgba(217,180,90,.4);border-radius:50%;animation:rip 3.8s ease-out infinite}
  .ring:nth-child(2){animation-delay:1.25s}.ring:nth-child(3){animation-delay:2.5s}
  @keyframes rip{0%{width:100px;height:100px;opacity:.95}100%{width:380px;height:380px;opacity:0}}
  .core{width:104px;height:104px;border-radius:50%;background:radial-gradient(circle at 32% 30%,var(--gold2),var(--gold) 45%,var(--gold-d));box-shadow:0 0 90px rgba(217,180,90,.45),inset 0 2px 10px rgba(255,255,255,.35);z-index:2;display:flex;align-items:center;justify-content:center;font-size:44px;color:#171204}
  @media(max-width:860px){.hero-in{grid-template-columns:1fr;gap:22px;padding:52px 0}.hero h1{font-size:36px}.hero-art{height:230px}}

  /* رؤوس الأقسام والأعمدة */
  .sec-head{text-align:center;max-width:700px;margin:0 auto 44px}
  .sec-head h2{font-size:33px;font-weight:800;margin:16px 0 14px;line-height:1.35}
  .sec-head p{color:var(--muted);font-size:16px}
  .pillars{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
  .pcard{background:linear-gradient(170deg,var(--surface2),var(--surface));border:1px solid var(--line2);border-radius:22px;padding:30px 26px;box-shadow:var(--shadow-sm);transition:transform .25s,border-color .25s,box-shadow .25s;position:relative;overflow:hidden}
  .pcard::before{content:"";position:absolute;inset:0 0 auto 0;height:1px;background:linear-gradient(90deg,transparent,rgba(217,180,90,.55),transparent)}
  .pcard:hover{transform:translateY(-5px);border-color:var(--line);box-shadow:var(--shadow)}
  .pcard .pic{width:56px;height:56px;border-radius:16px;display:flex;align-items:center;justify-content:center;font-size:26px;margin-bottom:18px;background:rgba(217,180,90,.1);border:1px solid var(--line)}
  .pcard h3{font-size:19px;font-weight:800;margin-bottom:9px;color:var(--gold2)}
  .pcard p{color:var(--muted);font-size:14.5px;line-height:1.85}
  @media(max-width:780px){.pillars{grid-template-columns:1fr}}

  /* شريط المسارين */
  .paths{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:8px}
  .pathcard{border-radius:24px;padding:34px 30px;color:#fff;position:relative;overflow:hidden;cursor:pointer;transition:transform .25s,box-shadow .25s;border:1px solid var(--line2)}
  .pathcard::after{content:"";position:absolute;width:280px;height:280px;border-radius:50%;left:-90px;bottom:-140px;background:radial-gradient(circle,rgba(255,255,255,.08),transparent 70%)}
  .pathcard:hover{transform:translateY(-5px);box-shadow:var(--shadow)}
  .pathcard.acad{background:linear-gradient(150deg,#153B33,#0C211C)}
  .pathcard.tal{background:linear-gradient(150deg,#3A2F14,#211A08);border-color:var(--line)}
  .pathcard .tag{font-size:12px;font-weight:600;margin-bottom:12px;letter-spacing:.08em;color:var(--gold);display:inline-block;border:1px solid var(--line);padding:5px 12px;border-radius:999px}
  .pathcard h3{font-size:23px;font-weight:800;margin-bottom:10px}
  .pathcard p{font-size:14.5px;opacity:.85;line-height:1.85;margin-bottom:20px}
  .pathcard .go{display:inline-flex;align-items:center;gap:7px;font-family:'Alexandria';font-weight:700;font-size:14.5px;background:rgba(217,180,90,.14);color:var(--gold2);padding:10px 20px;border-radius:12px;border:1px solid var(--line)}
  @media(max-width:780px){.paths{grid-template-columns:1fr}}

  /* ===== العنوان الداخلي ===== */
  .page-head{background:linear-gradient(165deg,#101915,var(--bg2));color:#fff;padding:46px 0 50px;border-bottom:1px solid var(--line);position:relative;overflow:hidden}
  .page-head::before{content:"";position:absolute;width:480px;height:480px;border-radius:50%;background:radial-gradient(circle,rgba(217,180,90,.1),transparent 65%);top:-220px;left:-100px}
  .page-head .wrap{display:flex;align-items:center;gap:18px;flex-wrap:wrap;position:relative;z-index:1}
  .page-head .ic{width:64px;height:64px;border-radius:18px;display:flex;align-items:center;justify-content:center;font-size:31px;flex-shrink:0;background:rgba(217,180,90,.1);border:1px solid var(--line)}
  .page-head h2{font-size:28px;font-weight:800}
  .page-head p{color:#A9BAB2;font-size:15px;margin-top:5px}

  .grid-2{display:grid;grid-template-columns:1.4fr .9fr;gap:24px;align-items:start}
  @media(max-width:880px){.grid-2{grid-template-columns:1fr}}
  .card{background:var(--surface);border:1px solid var(--line2);border-radius:20px;padding:24px;box-shadow:var(--shadow-sm);margin-bottom:20px}
  .card-h{display:flex;align-items:flex-start;justify-content:space-between;gap:12px;margin-bottom:16px}
  .card-h h3{font-size:17px;font-weight:800;color:var(--gold2)}
  .card-h .csub{color:var(--muted);font-size:13px;margin-top:4px}
  .card-h a{color:var(--teal-bright);font-size:13px;font-weight:600;cursor:pointer;text-decoration:none}

  .care{background:linear-gradient(120deg,#15332B,#0D1F1A);border:1px solid rgba(31,191,156,.25);border-radius:18px;padding:19px 22px;color:#DDEBE5;display:flex;gap:14px;align-items:center;margin-bottom:22px}
  .care .e{font-size:24px}
  .care p{font-size:14px;line-height:1.8}
  .care b{color:var(--gold2);font-family:'Alexandria'}

  .members{display:flex;align-items:center;flex-wrap:wrap;gap:6px}
  .av{width:42px;height:42px;border-radius:50%;display:flex;align-items:center;justify-content:center;color:#fff;font-family:'Alexandria';font-weight:700;font-size:14px;margin-left:-8px;border:3px solid var(--surface);flex-shrink:0}
  .members .more{width:42px;height:42px;border-radius:50%;background:var(--surface3);color:var(--gold2);font-weight:700;font-size:13px;display:flex;align-items:center;justify-content:center;margin-left:-8px;border:3px solid var(--surface);font-family:'Alexandria'}

  .res{display:flex;gap:13px;align-items:center;padding:14px;border:1px solid var(--line2);border-radius:14px;margin-bottom:10px;transition:transform .15s,border-color .2s;cursor:pointer;background:var(--surface2)}
  .res:hover{transform:translateX(-4px);border-color:var(--line)}
  .res .ric{width:40px;height:40px;border-radius:11px;display:flex;align-items:center;justify-content:center;font-size:17px;flex-shrink:0;background:rgba(217,180,90,.1);color:var(--gold2)}
  .res.vid .ric{background:rgba(31,191,156,.12);color:var(--teal-bright)}
  .res.note .ric{background:rgba(255,255,255,.06);color:#CFE0DA}
  .res .rm{flex:1;min-width:0}
  .res .rm b{display:block;font-family:'Alexandria';font-weight:600;font-size:14px}
  .res .rm small{color:var(--muted);font-size:12px}
  .res .free{font-size:11px;font-weight:700;color:var(--good);background:rgba(61,219,180,.1);padding:5px 11px;border-radius:8px;flex-shrink:0}

  .q{border:1px solid var(--line2);border-radius:16px;padding:18px;margin-bottom:12px;background:var(--surface2)}
  .q .who{display:flex;gap:10px;align-items:center;margin-bottom:10px}
  .q .who .av{margin:0;width:38px;height:38px;border:none}
  .q .who b{font-family:'Alexandria';font-size:14px;display:block}
  .q .who small{color:var(--muted);font-size:12px}
  .q .qt{font-size:14.5px;line-height:1.8;margin-bottom:12px}
  .q .qf{display:flex;gap:16px;align-items:center;font-size:12.5px;color:var(--muted)}
  .q .qf .ans{color:var(--good);font-weight:600}
  .q .qf .rep{margin-right:auto;color:var(--gold);font-weight:600;cursor:pointer}

  .side .sbox h4{font-size:15px;font-weight:700;margin-bottom:16px}
  .clarity .cl-h{display:flex;justify-content:space-between;align-items:baseline;margin-bottom:12px}
  .clarity .cl-h span{font-family:'Alexandria';font-weight:800;font-size:26px;color:var(--gold2)}
  .bar{height:9px;background:rgba(255,255,255,.1);border-radius:999px;overflow:hidden}
  .bar i{display:block;height:100%;background:linear-gradient(90deg,var(--gold-d),var(--gold2));border-radius:999px}
  .goalbox{background:var(--surface);border:1px dashed var(--line);border-radius:18px;padding:19px;display:flex;gap:14px;align-items:center}
  .goalbox .ring2{width:56px;height:56px;flex-shrink:0;border-radius:50%;background:conic-gradient(var(--gold) 72%,var(--surface3) 0);display:flex;align-items:center;justify-content:center}
  .goalbox .ring2 i{width:42px;height:42px;border-radius:50%;background:var(--surface);display:flex;align-items:center;justify-content:center;font-family:'Alexandria';font-weight:800;font-size:12.5px;color:var(--gold2);font-style:normal}
  .goalbox b{display:block;font-family:'Alexandria';font-weight:700;font-size:14px;margin-bottom:3px}
  .goalbox small{color:var(--muted);font-size:12.5px}

  /* ===== الفئات ===== */
  .note-bar{background:rgba(217,180,90,.07);border:1px solid var(--line);border-radius:16px;padding:17px 19px;font-size:13.5px;color:#D8CDA9;line-height:1.8;margin-bottom:28px;display:flex;gap:12px;align-items:flex-start}
  .note-bar b{font-family:'Alexandria';color:var(--gold2)}
  .cats{display:grid;grid-template-columns:repeat(4,1fr);gap:16px}
  @media(max-width:880px){.cats{grid-template-columns:repeat(2,1fr)}}
  @media(max-width:480px){.cats{grid-template-columns:1fr}}
  .cat{background:linear-gradient(170deg,var(--surface2),var(--surface));border:1px solid var(--line2);border-radius:20px;padding:24px 20px;cursor:pointer;text-align:center;transition:transform .2s,border-color .25s,box-shadow .25s;font-family:inherit;position:relative;overflow:hidden}
  .cat::before{content:"";position:absolute;inset:0 0 auto 0;height:1px;background:linear-gradient(90deg,transparent,rgba(217,180,90,.4),transparent);opacity:0;transition:opacity .25s}
  .cat:hover{transform:translateY(-5px);border-color:var(--line);box-shadow:var(--glow-gold)}
  .cat:hover::before{opacity:1}
  .cat:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .cat .ce{width:62px;height:62px;border-radius:18px;margin:0 auto 15px;display:flex;align-items:center;justify-content:center;font-size:29px;background:rgba(217,180,90,.08);border:1px solid var(--line2)}
  .cat b{display:block;font-family:'Alexandria';font-weight:700;font-size:16px;color:var(--ink);margin-bottom:5px}
  .cat small{color:var(--muted);font-size:12.5px}
  .cat .ctag{display:inline-block;margin-top:11px;font-size:11px;font-weight:700;padding:5px 12px;border-radius:8px}
  .cat .ctag.free{color:var(--good);background:rgba(61,219,180,.1)}
  .cat .ctag.paid{color:var(--gold);background:rgba(217,180,90,.1)}
  .cat.locked{opacity:.85}
  .cat.other{border-style:dashed;border-color:var(--line)}
  .cat.other .ce{background:rgba(217,180,90,.06)}

  .discover-cta{margin-top:30px;background:linear-gradient(120deg,var(--surface2),var(--surface));border:1px solid var(--line);border-radius:20px;padding:26px;display:flex;align-items:center;gap:18px;flex-wrap:wrap;box-shadow:var(--shadow-sm)}
  .discover-cta .dic{width:56px;height:56px;border-radius:16px;background:rgba(217,180,90,.1);border:1px solid var(--line);display:flex;align-items:center;justify-content:center;font-size:26px;flex-shrink:0}
  .discover-cta .dt{flex:1;min-width:200px}
  .discover-cta .dt b{font-family:'Alexandria';font-weight:800;font-size:18px;display:block;margin-bottom:5px;color:var(--gold2)}
  .discover-cta .dt p{color:var(--muted);font-size:14px}

  /* مودالات */
  .modal{display:none;position:fixed;inset:0;z-index:100;background:rgba(5,8,7,.75);backdrop-filter:blur(8px);align-items:center;justify-content:center;padding:20px}
  .modal.show{display:flex}
  .modal-box{background:linear-gradient(170deg,var(--surface2),var(--surface));border:1px solid var(--line);border-radius:24px;padding:32px;max-width:440px;width:100%;box-shadow:var(--shadow);animation:pop .3s ease}
  @keyframes pop{from{transform:scale(.94);opacity:0}to{transform:scale(1);opacity:1}}
  .modal-box .mi{width:58px;height:58px;border-radius:17px;background:rgba(217,180,90,.1);border:1px solid var(--line);display:flex;align-items:center;justify-content:center;font-size:28px;margin-bottom:18px}
  .modal-box h3{font-size:21px;font-weight:800;margin-bottom:8px;color:var(--gold2)}
  .modal-box p{color:var(--muted);font-size:14px;margin-bottom:18px;line-height:1.8}
  .modal-box input{width:100%;padding:14px;border:1px solid var(--line2);border-radius:13px;font-family:inherit;font-size:15px;margin-bottom:16px;background:var(--bg2);color:var(--ink)}
  .modal-box input:focus{outline:none;border-color:var(--gold)}
  .modal-box .mrow{display:flex;gap:10px}
  #otherDone{display:none}
  #otherDone .ok{width:58px;height:58px;border-radius:50%;background:rgba(61,219,180,.12);color:var(--good);display:flex;align-items:center;justify-content:center;font-size:30px;margin-bottom:16px}

  /* ===== الاكتشاف ===== */
  .disc-wrap{max-width:700px;margin:0 auto}
  .method-cards{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-top:8px}
  @media(max-width:620px){.method-cards{grid-template-columns:1fr}}
  .method{background:linear-gradient(170deg,var(--surface2),var(--surface));border:1px solid var(--line2);border-radius:22px;padding:28px;cursor:pointer;text-align:center;transition:transform .2s,border-color .25s,box-shadow .25s;font-family:inherit}
  .method:hover{transform:translateY(-5px);border-color:var(--line);box-shadow:var(--glow-gold)}
  .method:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .method .mie{width:66px;height:66px;border-radius:19px;margin:0 auto 17px;display:flex;align-items:center;justify-content:center;font-size:32px;background:rgba(31,191,156,.1);border:1px solid rgba(31,191,156,.25)}
  .method.g .mie{background:rgba(217,180,90,.1);border-color:var(--line)}
  .method b{display:block;font-family:'Alexandria';font-weight:800;font-size:18px;margin-bottom:9px;color:var(--gold2)}
  .method p{color:var(--muted);font-size:13.5px;line-height:1.8;margin-bottom:15px}
  .method .mtag{display:inline-block;font-size:11.5px;font-weight:600;color:var(--teal-bright);background:rgba(31,191,156,.1);padding:6px 14px;border-radius:999px}
  .method.g .mtag{color:var(--gold);background:rgba(217,180,90,.1)}
  .ai-analyzing{text-align:center;padding:34px 0;display:none}
  .ai-analyzing.show{display:block;animation:fade .4s ease}
  .ai-spin{width:66px;height:66px;border-radius:19px;margin:0 auto 20px;background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;display:flex;align-items:center;justify-content:center;font-size:30px;animation:spin 1.4s linear infinite}
  @keyframes spin{to{transform:rotate(360deg)}}
  .ai-analyzing h3{font-size:21px;font-weight:800;margin-bottom:8px;color:var(--gold2)}
  .ai-analyzing p{color:var(--muted);font-size:14px}
  .progress{display:flex;gap:7px;margin-bottom:30px}
  .progress i{flex:1;height:5px;border-radius:999px;background:var(--surface3);transition:background .3s;min-width:8px}
  .progress i.on{background:linear-gradient(90deg,var(--gold-d),var(--gold))}
  .qstep{display:none}.qstep.active{display:block;animation:fade .4s ease}
  .qstep .qn{font-size:12.5px;color:var(--gold);font-weight:600;margin-bottom:12px;letter-spacing:.06em}
  .qstep h3{font-size:25px;font-weight:800;margin-bottom:9px;line-height:1.45}
  .qstep .qhint{color:var(--muted);font-size:14.5px;margin-bottom:24px}
  .choices{display:flex;flex-direction:column;gap:12px}
  .choice{background:var(--surface2);border:1px solid var(--line2);border-radius:16px;padding:17px 19px;cursor:pointer;text-align:right;font-family:inherit;font-size:15px;display:flex;align-items:center;gap:14px;transition:transform .15s,border-color .2s;color:var(--ink)}
  .choice:hover{transform:translateX(-5px);border-color:var(--gold)}
  .choice:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .choice .che{font-size:23px}
  .choice b{font-family:'Alexandria';font-weight:600}

  .disc-result{display:none;text-align:center;animation:fade .5s ease}
  .disc-result.show{display:block}
  .disc-result .rok{width:72px;height:72px;border-radius:22px;margin:0 auto 20px;background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;display:flex;align-items:center;justify-content:center;font-size:34px;box-shadow:0 14px 34px -8px rgba(217,180,90,.45)}
  .disc-result h3{font-size:27px;font-weight:800;margin-bottom:11px;color:var(--gold2)}
  .disc-result>p{color:var(--muted);font-size:15.5px;margin-bottom:28px;max-width:480px;margin-inline:auto}
  .matches{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-bottom:28px}
  @media(max-width:620px){.matches{grid-template-columns:1fr}}
  .match{background:var(--surface2);border:1px solid var(--line2);border-radius:18px;padding:22px;box-shadow:var(--shadow-sm)}
  .match .me{font-size:32px;margin-bottom:9px}
  .match b{display:block;font-family:'Alexandria';font-weight:700;font-size:15.5px;margin-bottom:8px}
  .match .pct{font-size:12px;color:var(--gold2);font-weight:700;background:rgba(217,180,90,.1);display:inline-block;padding:5px 12px;border-radius:8px}

  /* ===== لوحتي ===== */
  .dash-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-bottom:24px}
  @media(max-width:880px){.dash-grid{grid-template-columns:repeat(2,1fr)}}
  .metric{background:var(--surface);border:1px solid var(--line2);border-radius:18px;padding:22px;box-shadow:var(--shadow-sm)}
  .metric .mt{display:flex;align-items:center;gap:9px;margin-bottom:13px}
  .metric .mt .e{width:38px;height:38px;border-radius:11px;display:flex;align-items:center;justify-content:center;font-size:18px;border:1px solid var(--line2)}
  .metric .mt b{font-family:'Alexandria';font-weight:600;font-size:13px;color:var(--muted)}
  .metric .big{font-family:'Alexandria';font-weight:800;font-size:31px;color:var(--gold2)}
  .metric .big small{font-size:15px;color:var(--muted);font-weight:500}
  .metric .tr{font-size:12px;color:var(--good);margin-top:5px}
  .mood{background:var(--surface);border:1px solid var(--line2);border-radius:20px;padding:26px;box-shadow:var(--shadow-sm)}
  .mood b{font-family:'Alexandria';font-weight:700;font-size:16px;display:block;margin-bottom:5px;color:var(--gold2)}
  .mood .msub{color:var(--muted);font-size:13.5px;margin-bottom:18px}
  .faces{display:flex;gap:12px;flex-wrap:wrap}
  .face{width:58px;height:58px;border-radius:16px;border:1px solid var(--line2);background:var(--surface2);font-size:27px;cursor:pointer;display:flex;align-items:center;justify-content:center;transition:transform .15s,border-color .2s}
  .face:hover{transform:scale(1.1)}
  .face.sel{border-color:var(--gold);background:rgba(217,180,90,.1);transform:scale(1.06)}
  .face:focus-visible{outline:3px solid var(--gold);outline-offset:2px}

  /* ===== تبويبات ===== */
  .tabs{display:flex;gap:6px;background:var(--surface);border:1px solid var(--line2);border-radius:15px;padding:6px;margin-bottom:24px;box-shadow:var(--shadow-sm)}
  .tabs button{flex:1;background:none;border:none;cursor:pointer;font-family:'Alexandria';font-weight:700;font-size:14px;color:var(--muted);padding:12px;border-radius:11px;transition:all .2s;display:flex;align-items:center;justify-content:center;gap:7px}
  .tabs button.on{background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;box-shadow:0 8px 20px -8px rgba(217,180,90,.45)}
  .tabs button:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .tabpane{display:none;animation:fade .35s ease}.tabpane.on{display:block}

  .topic{margin-bottom:24px}
  .topic-h{display:flex;align-items:center;gap:10px;margin-bottom:12px}
  .topic-h .tn{width:30px;height:30px;border-radius:9px;background:rgba(217,180,90,.12);color:var(--gold2);display:flex;align-items:center;justify-content:center;font-family:'Alexandria';font-weight:800;font-size:13px;border:1px solid var(--line)}
  .topic-h b{font-family:'Alexandria';font-weight:700;font-size:16px}
  .topic-h .cnt{margin-right:auto;font-size:11.5px;color:var(--muted);background:var(--surface2);padding:5px 12px;border-radius:999px;border:1px solid var(--line2)}

  /* ===== الشات ===== */
  .chat-wrap{background:var(--surface);border:1px solid var(--line2);border-radius:20px;overflow:hidden;box-shadow:var(--shadow-sm)}
  .chat-top{padding:14px 18px;border-bottom:1px solid var(--line2);display:flex;align-items:center;gap:10px;background:var(--surface2)}
  .chat-top .live{display:flex;align-items:center;gap:7px;font-size:12.5px;color:var(--good);font-weight:600}
  .chat-top .live i{width:7px;height:7px;border-radius:50%;background:var(--good);animation:pulse 1.6s infinite}
  @keyframes pulse{0%,100%{opacity:1}50%{opacity:.3}}
  .chat-top .mod{margin-right:auto;font-size:11.5px;color:var(--muted);display:flex;align-items:center;gap:5px}
  .chat-body{padding:20px;max-height:420px;overflow-y:auto;display:flex;flex-direction:column;gap:15px;background:var(--bg2)}
  .msg{display:flex;gap:11px;align-items:flex-start}
  .msg .av{margin:0;width:38px;height:38px;border:none;font-size:13px}
  .msg .bub{background:var(--surface2);border:1px solid var(--line2);border-radius:5px 16px 16px 16px;padding:11px 15px;max-width:80%}
  .msg .nm{font-family:'Alexandria';font-weight:700;font-size:12.5px;color:var(--gold2);margin-bottom:4px}
  .msg .nm .uni{color:var(--muted);font-weight:500;font-family:'IBM Plex Sans Arabic';font-size:11px}
  .msg .tx{font-size:13.5px;line-height:1.75;color:#DEE7E2}
  .msg.me{flex-direction:row-reverse}
  .msg.me .bub{background:rgba(217,180,90,.1);border-color:var(--line);border-radius:16px 5px 16px 16px}
  .modbadge{font-size:10px;color:var(--good);background:rgba(61,219,180,.12);padding:2px 8px;border-radius:6px;font-weight:700}
  .chat-input{display:flex;gap:10px;padding:14px 16px;border-top:1px solid var(--line2);background:var(--surface2)}
  .chat-input input{flex:1;padding:13px 16px;border:1px solid var(--line2);border-radius:12px;font-family:inherit;font-size:14px;background:var(--bg2);color:var(--ink)}
  .chat-input input:focus{outline:none;border-color:var(--gold)}
  .chat-input button{width:48px;border:none;border-radius:12px;background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;font-size:17px;cursor:pointer;transition:filter .2s}
  .chat-input button:hover{filter:brightness(1.08)}
  .chat-rooms{display:flex;gap:8px;padding:12px 16px;border-top:1px solid var(--line2);flex-wrap:wrap;background:var(--surface)}
  .room{font-size:12.5px;font-weight:600;color:var(--muted);background:var(--surface2);border:1px solid var(--line2);padding:7px 14px;border-radius:999px;cursor:pointer;transition:all .2s}
  .room:hover{color:var(--gold2);border-color:var(--line)}
  .room.on{color:var(--gold2);background:rgba(217,180,90,.1);border-color:var(--line)}

  /* أيام الأسبوع */
  .week-days{display:flex;gap:8px;margin:14px 0 4px;flex-wrap:wrap}
  .wday{flex:1;min-width:74px;border:1px solid var(--line2);border-radius:13px;padding:11px 8px;text-align:center;background:var(--surface2)}
  .wday b{display:block;font-family:'Alexandria';font-weight:700;font-size:12.5px;margin-bottom:3px}
  .wday small{font-size:11px;color:var(--muted)}
  .wday.done{border-color:rgba(61,219,180,.35);background:rgba(61,219,180,.07)}
  .wday.done small{color:var(--good)}
  .wday.on{border-color:var(--gold);background:rgba(217,180,90,.09)}
  .wday.on small{color:var(--gold)}

  /* بطاقة المستكشفين */
  .scout{background:linear-gradient(140deg,#3A2F14 0%,#211A08 70%);border:1px solid var(--line);border-radius:22px;padding:28px;color:#fff;position:relative;overflow:hidden}
  .scout::after{content:"🏆";position:absolute;left:-14px;bottom:-26px;font-size:120px;opacity:.08}
  .scout .stag{display:inline-block;font-size:11.5px;font-weight:700;color:var(--gold2);border:1px solid var(--line);background:rgba(217,180,90,.1);padding:6px 14px;border-radius:999px;margin-bottom:14px;letter-spacing:.05em}
  .scout h3{font-size:21px;font-weight:800;margin-bottom:9px;color:var(--gold2)}
  .scout p{font-size:14px;opacity:.85;line-height:1.85;margin-bottom:18px;position:relative;z-index:2}
  .reqs{display:flex;flex-direction:column;gap:10px;margin-bottom:20px;position:relative;z-index:2}
  .req{display:flex;gap:11px;align-items:center;font-size:13.5px}
  .req .c{width:26px;height:26px;border-radius:8px;background:rgba(217,180,90,.15);border:1px solid var(--line);color:var(--gold2);display:flex;align-items:center;justify-content:center;font-family:'Alexandria';font-weight:800;font-size:12px;flex-shrink:0}

  /* تنقّل المجتمعات */
  .pillnav{display:flex;gap:8px;background:var(--surface);border:1px solid var(--line2);border-radius:15px;padding:7px;margin-bottom:28px;box-shadow:var(--shadow-sm);overflow-x:auto}
  .pillnav button{flex:1;white-space:nowrap;background:none;border:none;cursor:pointer;font-family:'Alexandria';font-weight:700;font-size:14px;color:var(--muted);padding:11px 14px;border-radius:11px;transition:all .2s;display:flex;align-items:center;justify-content:center;gap:6px}
  .pillnav button.on{background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;box-shadow:0 8px 20px -8px rgba(217,180,90,.45)}
  .pillnav button:focus-visible{outline:3px solid var(--gold);outline-offset:2px}
  .commpane{display:none;animation:fade .35s ease}.commpane.on{display:block}
  @media(max-width:680px){.pillnav button{flex:0 0 auto;font-size:13px;padding:10px 12px}}

  /* فلاتر الصدارة */
  .fpills{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:20px}
  .fp{font-size:13px;font-weight:700;font-family:'Alexandria';color:var(--muted);background:var(--surface2);border:1px solid var(--line2);padding:8px 16px;border-radius:999px;cursor:pointer;transition:all .2s}
  .fp:hover{color:var(--gold2);border-color:var(--line)}
  .fp.on{color:#171204;background:linear-gradient(135deg,var(--gold2),var(--gold-d));border-color:transparent}

  /* الصدارة */
  .lb{display:flex;flex-direction:column;gap:10px}
  .lb .row{display:flex;gap:13px;align-items:center;background:var(--surface);border:1px solid var(--line2);border-radius:16px;padding:13px 17px;transition:transform .15s,border-color .2s}
  .lb .row:hover{transform:translateX(-4px);border-color:var(--line)}
  .lb .rk{width:32px;height:32px;border-radius:10px;background:var(--surface3);color:var(--muted);display:flex;align-items:center;justify-content:center;font-family:'Alexandria';font-weight:800;font-size:13.5px;flex-shrink:0}
  .lb .row.top1{border-color:rgba(217,180,90,.55);background:linear-gradient(120deg,rgba(217,180,90,.1),var(--surface))}
  .lb .row.top1 .rk{background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204}
  .lb .row.top2 .rk{background:#8E9CA6;color:#10151A}
  .lb .row.top3 .rk{background:#8A6A45;color:#1B130A}
  .lb .nm{flex:1;min-width:0}
  .lb .nm b{font-family:'Alexandria';font-weight:700;font-size:14.5px;display:block}
  .lb .nm small{color:var(--muted);font-size:12px}
  .lb .stk{font-family:'Alexandria';font-weight:800;font-size:15px;color:var(--gold2);flex-shrink:0}

  /* المؤثرون */
  .inf-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}
  @media(max-width:720px){.inf-grid{grid-template-columns:1fr}}
  .inf{display:flex;gap:14px;align-items:center;background:var(--surface);border:1px solid var(--line2);border-radius:18px;padding:17px 19px;transition:transform .18s,border-color .25s,box-shadow .25s}
  .inf:hover{transform:translateY(-3px);border-color:var(--line);box-shadow:var(--glow-gold)}
  .inf .ia{width:52px;height:52px;border-radius:15px;color:#fff;display:flex;align-items:center;justify-content:center;font-family:'Alexandria';font-weight:800;font-size:16px;flex-shrink:0}
  .inf .im{min-width:0}
  .inf .im b{font-family:'Alexandria';font-weight:700;font-size:15px;display:block}
  .inf .im .fld{color:var(--teal-bright);font-size:12px;font-weight:600;display:block;margin:3px 0 7px}
  .inf .hd{display:flex;gap:6px;flex-wrap:wrap}
  .inf .hd span{font-size:11px;font-weight:700;color:var(--gold2);background:rgba(217,180,90,.1);border:1px solid var(--line);padding:4px 10px;border-radius:8px}

  /* المستكشفون */
  .scout-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin-bottom:26px}
  @media(max-width:720px){.scout-grid{grid-template-columns:1fr}}
  .scard{background:var(--surface);border:1px solid var(--line2);border-radius:18px;padding:21px;transition:transform .18s,border-color .25s}
  .scard:hover{transform:translateY(-3px);border-color:var(--line)}
  .scard .sh{display:flex;gap:11px;align-items:center;margin-bottom:10px}
  .scard .sh .se{width:42px;height:42px;border-radius:12px;background:rgba(217,180,90,.08);border:1px solid var(--line2);display:flex;align-items:center;justify-content:center;font-size:20px}
  .scard .sh b{font-family:'Alexandria';font-weight:700;font-size:15px}
  .scard p{color:var(--muted);font-size:13.5px;line-height:1.75;margin-bottom:10px}
  .scard .slk{font-size:12px;color:var(--teal-bright);font-weight:600}

  /* الباقات */
  .trial{background:linear-gradient(135deg,#15332B,#0D1F1A);border:1px solid rgba(31,191,156,.3);border-radius:18px;padding:19px 21px;display:flex;align-items:center;gap:16px;color:#fff;margin-bottom:24px;position:relative;overflow:hidden;flex-wrap:wrap}
  .trial::after{content:"✨";position:absolute;left:-6px;bottom:-18px;font-size:78px;opacity:.08}
  .trial .te{font-size:26px}
  .trial .tt{flex:1;min-width:200px}
  .trial .tt b{font-family:'Alexandria';font-weight:700;font-size:15.5px;display:block;color:var(--gold2)}
  .trial .tt span{font-size:13px;color:#A9BAB2;display:block;margin-top:3px}
  .prices{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin:8px 0}
  @media(max-width:620px){.prices{grid-template-columns:1fr}}
  .price{background:var(--surface2);border:1px solid var(--line2);border-radius:18px;padding:20px 17px;cursor:pointer;transition:transform .15s,border-color .2s;text-align:center}
  .price:hover{transform:translateY(-3px);border-color:var(--line)}
  .price.best{border-color:var(--gold);background:linear-gradient(170deg,rgba(217,180,90,.1),var(--surface2));box-shadow:var(--glow-gold)}
  .price .pname{font-family:'Alexandria';font-weight:700;font-size:14px;color:var(--gold2);margin-bottom:9px}
  .price .pamt{font-family:'Alexandria';font-weight:800;font-size:27px;margin-bottom:9px}
  .price .pamt small{font-size:12.5px;color:var(--muted);font-weight:500}
  .price .pdesc{font-size:12px;color:var(--muted);line-height:1.7}
  .price-note{font-size:12.5px;color:var(--muted);line-height:1.8;background:var(--surface2);border:1px solid var(--line2);border-radius:12px;padding:12px 15px}
  .price-note b{color:var(--gold2)}

  /* ===== مجتمع المجال (نمط ديسكورد) ===== */
  .chan-row{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:15px}
  .chan{font-size:13px;font-weight:700;font-family:'Alexandria';color:var(--muted);background:var(--surface);border:1px solid var(--line2);padding:9px 16px;border-radius:999px;cursor:pointer;transition:all .2s}
  .chan:hover{color:var(--gold2);border-color:var(--line);transform:translateY(-1px)}
  .chan.on{background:linear-gradient(135deg,var(--gold2),var(--gold-d));color:#171204;border-color:transparent;box-shadow:0 8px 20px -8px rgba(217,180,90,.45)}
  .tip{display:flex;gap:12px;align-items:flex-start;padding:13px 0;border-bottom:1px dashed var(--line2);font-size:14px;line-height:1.85;color:#DEE7E2}
  .tip:last-child{border-bottom:none;padding-bottom:2px}
  .tip .tn2{width:27px;height:27px;border-radius:9px;background:rgba(217,180,90,.12);border:1px solid var(--line);color:var(--gold2);display:flex;align-items:center;justify-content:center;font-size:12.5px;flex-shrink:0;font-weight:800;font-family:'Alexandria'}
  .star{display:flex;gap:11px;align-items:center;padding:12px 0;border-bottom:1px solid var(--line2)}
  .star:last-child{border-bottom:none;padding-bottom:2px}
  .star .sa{width:40px;height:40px;border-radius:12px;color:#fff;display:flex;align-items:center;justify-content:center;font-weight:800;font-family:'Alexandria';font-size:13px;flex-shrink:0}
  .star .sm2{min-width:0}
  .star .sm2 b{font-size:13.5px;font-family:'Alexandria';display:block;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
  .star .sm2 small{color:var(--muted);font-size:11.5px;display:block}
  .star .fw{margin-right:auto;font-size:10.5px;font-weight:700;color:var(--gold2);background:rgba(217,180,90,.1);border:1px solid var(--line);padding:5px 9px;border-radius:8px;white-space:nowrap;flex-shrink:0}

  .foot{background:var(--bg2);border-top:1px solid var(--line);color:#7E8F87;text-align:center;padding:32px 24px;font-size:13px;margin-top:28px;line-height:2}
  .foot b{color:var(--gold2);font-family:'Alexandria'}
  .foot a{color:var(--gold);font-weight:600;text-decoration:none}
  .foot a:hover{text-decoration:underline}
</style>
</head>
<body>

<!-- شريط التنقّل -->
<header class="nav">
  <div class="nav-in">
    <div class="brand"><span class="m">م</span> مواهب</div>
    <div class="links">
      <button class="on" id="n-home" onclick="show('home',this)">الرئيسية</button>
      <button id="n-academic" onclick="show('academic',this)">المسار الأكاديمي</button>
      <button id="n-talents" onclick="show('talents',this)">المواهب</button>
      <button id="n-communities" onclick="show('communities',this)">مجتمعات</button>
      <button id="n-discover" onclick="show('discover',this)">اكتشف موهبتك</button>
      <button id="n-dashboard" onclick="show('dashboard',this)">لوحتي</button>
    </div>
    <span class="nav-badge">اكتشف ✦ طوّر ✦ انطلق</span>
  </div>
</header>

<!-- ============ الرئيسية ============ -->
<div class="view active" id="v-home">
  <section class="hero">
    <div class="wrap hero-in">
      <div>
        <span class="eyebrow">بوابتك من الموهبة إلى النجومية</span>
        <h1>اكتشف موهبتك. طوّرها.<br><span class="hl">وخلّ العالم يشوفها.</span></h1>
        <p class="lead">داخل كل شاب موهبة تنتظر من يكتشفها. «مواهب» تاخذك من سؤال «وش موهبتي؟» إلى مجتمع يصقلك، ومرشد باسمه يتابعك، ومستكشفين يفتحون لك أبواب الاحتراف.</p>
        <div class="quote">الشباب هم القوة والطاقة الحقيقية لتحقيق رؤية 2030.<span>— ولي العهد الأمير محمد بن سلمان</span></div>
        <div class="hero-cta">
          <button class="btn btn-primary" onclick="show('talents',document.getElementById('n-talents'))">اكتشف موهبتك الآن ›</button>
          <button class="btn btn-ghost" onclick="document.getElementById('problem').scrollIntoView()">شوف كيف تشتغل المنصة</button>
        </div>
      </div>
      <div class="hero-art">
        <div class="ring"></div><div class="ring"></div><div class="ring"></div>
        <div class="core">✦</div>
      </div>
    </div>
  </section>

  <section class="section" id="problem">
    <div class="wrap">
      <div class="sec-head">
        <span class="eyebrow">لماذا مواهب</span>
        <h2>الموهبة وحدها ما تكفي — تحتاج نظاماً يطلقها</h2>
        <p>الفرق بين موهوب وصل وموهوب توقّف مو الحظ — ثلاث ركائز، جمعناها لك في مكان واحد.</p>
      </div>
      <div class="pillars">
        <div class="pcard">
          <div class="pic">🧭</div>
          <h3>اكتشاف علمي</h3>
          <p>نختصر عليك سنوات من التخبّط: اختبار الذكاءات المتعددة ورحلة تجاربك يحددان مجالك الأقرب — فتستثمر وقتك في المكان الصح من أول يوم.</p>
        </div>
        <div class="pcard">
          <div class="pic">🤝</div>
          <h3>مجتمع يدفعك للأمام</h3>
          <p>لكل مجال مجتمع حي: قنوات نقاش يومية، أبطال تنافسهم على الصدارة، ومرشد باسمه يضع خطتك ويتابع تقدّمك خطوة بخطوة.</p>
        </div>
        <div class="pcard">
          <div class="pic">🚀</div>
          <h3>فرص حقيقية</h3>
          <p>تطوّرك ما يضيع: نوثّقه يوماً بيوم، ونعرض الأبرز على الأندية والكشّافين ودور النشر والحاضنات — من الهواية إلى الاحتراف.</p>
        </div>
      </div>
    </div>
  </section>

  <section class="section" style="background:var(--surface2);border-top:1px solid var(--line);border-bottom:1px solid var(--line)">
    <div class="wrap">
      <div class="sec-head">
        <span class="eyebrow">مساراك نحو التميّز</span>
        <h2>مساران يصنعان شاباً يرفع نفسه ومجتمعه</h2>
      </div>
      <div class="paths">
        <div class="pathcard acad" onclick="show('academic',document.getElementById('n-academic'))">
          <div class="tag">للطالب اللي يبي يتفوّق</div>
          <h3>📚 المسار الأكاديمي</h3>
          <p>تفوقك الدراسي أساس انطلاقتك. مجتمع لكل مادة: مصادر مرتبة، طلاب متفوقون يدرسون معك، وأسئلة محلولة — فترتفع درجاتك وثقتك.</p>
          <span class="go">ادخل المسار ›</span>
        </div>
        <div class="pathcard tal" onclick="show('talents',document.getElementById('n-talents'))">
          <div class="tag">لصاحب الموهبة والطموح</div>
          <h3>🎯 مسار المواهب</h3>
          <p>موهبتك تستحق أكثر من وقت الفراغ. اختر مجالك أو اكتشفه، وادخل نظاماً كاملاً: خطة، مرشد، مجتمع نابض، وفرص عرض حقيقية.</p>
          <span class="go">اكتشف مجالك ›</span>
        </div>
      </div>
    </div>
  </section>
</div>

<!-- ============ المسار الأكاديمي ============ -->
<div class="view" id="v-academic">
  <div class="page-head">
    <div class="wrap">
      <div class="ic">📚</div>
      <div>
        <h2>المسار الأكاديمي</h2>
        <p>اختر مادتك، وادخل مجتمعها: مصادر منظّمة + طلاب يدرسونها معك</p>
      </div>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="trial">
      <div class="te">✨</div>
      <div class="tt"><b>ابدأ بتجربة مجانية 7 أيام</b><span>الإرشاد الأكاديمي مع مرشد مؤهل — جلسة تعريفية ومتابعة، بدون أي رسوم.</span></div>
      <button class="btn btn-primary btn-sm tbtn" onclick="openPlans('أكاديمي')">ابدأ مجاناً ›</button>
    </div>
    <div class="note-bar">
      <span>💡</span>
      <span><b>أول 3 مجتمعات دراسية مجانية بالكامل</b> (مصادر + شات + أسئلة). كل مجتمع إضافي بـ <b>50 ريال</b> لمرة واحدة. وخانة «أخرى» تجمع طلبكم — فلما يتجمّع طلب كافٍ على مادة، نفتح لها مجتمعاً.</span>
    </div>
    <div class="cats">
      <button class="cat" onclick="openSubject('تفاضل وتكامل 1','Math 101','∫')"><div class="ce">∫</div><b>تفاضل وتكامل 1</b><small>Math 101 · 52 طالب</small><span class="ctag free">✓ مجاني</span></button>
      <button class="cat" onclick="openSubject('فيزياء عامة','Phys 101','⚛️')"><div class="ce">⚛️</div><b>فيزياء عامة</b><small>Phys 101 · 41 طالب</small><span class="ctag free">✓ مجاني</span></button>
      <button class="cat" onclick="openSubject('كيمياء عامة','Chem 101','🧪')"><div class="ce">🧪</div><b>كيمياء عامة</b><small>Chem 101 · 29 طالب</small><span class="ctag free">✓ مجاني</span></button>
      <button class="cat locked" onclick="openStudyUnlock('مقدمة برمجة','CS 101','💻')"><div class="ce">💻</div><b>مقدمة برمجة</b><small>CS 101 · 63 طالب</small><span class="ctag paid">🔒 50 ريال</span></button>
      <button class="cat locked" onclick="openStudyUnlock('إحصاء','Stat 201','📊')"><div class="ce">📊</div><b>إحصاء</b><small>Stat 201 · 38 طالب</small><span class="ctag paid">🔒 50 ريال</span></button>
      <button class="cat locked" onclick="openStudyUnlock('هياكل بيانات','CS 211','🗂️')"><div class="ce">🗂️</div><b>هياكل بيانات</b><small>CS 211 · 34 طالب</small><span class="ctag paid">🔒 50 ريال</span></button>
      <button class="cat locked" onclick="openStudyUnlock('لغة إنجليزية','Eng 101','🔤')"><div class="ce">🔤</div><b>لغة إنجليزية</b><small>Eng 101 · 47 طالب</small><span class="ctag paid">🔒 50 ريال</span></button>
      <button class="cat other" onclick="openOther()"><div class="ce">➕</div><b>أخرى</b><small>اطلب مادتك</small></button>
    </div>
  </div></section>
</div>

<!-- ============ صفحة المادة (مصادر + شات + أسئلة) ============ -->
<div class="view" id="v-subject">
  <div class="page-head">
    <div class="wrap">
      <div class="ic" id="sub-ic">∫</div>
      <div>
        <h2 id="sub-title">مجتمع: تفاضل وتكامل 1</h2>
        <p id="sub-sub">Math 101 · 52 طالب من 7 جامعات · <span style="color:#7FE0D3">14 متّصل الآن</span></p>
      </div>
      <button class="btn btn-ghost btn-sm" style="margin-right:auto" onclick="show('academic',document.getElementById('n-academic'))">‹ كل المواد</button>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="care" style="cursor:pointer" onclick="openPlans('توجيه')">
      <span class="e">🤝</span>
      <p>قربت الاختبارات وحاس بضغط؟ اطلب <b>جلسة توجيه وإرشاد</b> مع مرشد مؤهل، بسرّية تامة — <b>اضغط لعرض الباقات</b>. <span style="opacity:.8">(توجيه — لا يُغني عن الاستشارة الطبية عند الحاجة)</span></p>
    </div>

    <!-- التبويبات -->
    <div class="tabs">
      <button class="on" id="tab-res" onclick="subTab('res')">📚 المصادر</button>
      <button id="tab-chat" onclick="subTab('chat')">💬 الشات التفاعلي</button>
      <button id="tab-q" onclick="subTab('q')">❓ الأسئلة</button>
    </div>

    <!-- تبويب المصادر -->
    <div class="tabpane on" id="pane-res">
      <div class="grid-2">
        <div>
          <div class="topic">
            <div class="topic-h"><span class="tn">1</span><b>النهايات والاتصال</b><span class="cnt">4 مصادر</span></div>
            <div class="res pdf"><span class="ric">📄</span><span class="rm"><b>ملخص النهايات الشامل</b><small>12 صفحة · PDF · ⭐ 4.8</small></span><span class="free">مجاني</span></div>
            <div class="res vid"><span class="ric">▶</span><span class="rm"><b>شرح الاتصال من الصفر</b><small>فيديو · 18 دقيقة</small></span><span class="free">مجاني</span></div>
          </div>
          <div class="topic">
            <div class="topic-h"><span class="tn">2</span><b>المشتقات</b><span class="cnt">5 مصادر</span></div>
            <div class="res vid"><span class="ric">▶</span><span class="rm"><b>قواعد الاشتقاق + أمثلة</b><small>فيديو · 24 دقيقة</small></span><span class="free">مجاني</span></div>
            <div class="res note"><span class="ric">✦</span><span class="rm"><b>أخطاء شائعة في الاشتقاق</b><small>جمعها طلاب سابقون</small></span><span class="free">مجاني</span></div>
          </div>
          <div class="topic">
            <div class="topic-h"><span class="tn">3</span><b>التكامل</b><span class="cnt">6 مصادر</span></div>
            <div class="res pdf"><span class="ric">📄</span><span class="rm"><b>جدول التكاملات الأساسية</b><small>3 صفحات · PDF · ⭐ 4.9</small></span><span class="free">مجاني</span></div>
            <div class="res note"><span class="ric">✦</span><span class="rm"><b>أسئلة الاختبارات السابقة محلولة</b><small>تجميعة الفصول الماضية</small></span><span class="free">مجاني</span></div>
          </div>
        </div>
        <div class="side">
          <div class="card" style="margin-bottom:20px">
            <div class="card-h"><h3>طلاب المادة</h3></div>
            <div class="members">
              <span class="av" style="background:#0EA5A0">سا</span>
              <span class="av" style="background:#F4A261">عب</span>
              <span class="av" style="background:#5B7FE0">نو</span>
              <span class="av" style="background:#C065C0">رغ</span>
              <span class="more">+48</span>
            </div>
            <div style="color:var(--muted);font-size:13px;margin-top:12px;line-height:1.6"><b style="font-family:'Tajawal';color:var(--ink)">52 طالب</b> من 7 جامعات يدرسون المادة معك</div>
          </div>
          <div class="goalbox">
            <div class="ring2"><i>72%</i></div>
            <div><b>هدف الأسبوع: 5 جلسات مذاكرة</b><small>خلّصت 4 — باقي وحدة 🔥</small></div>
          </div>
        </div>
      </div>
    </div>

    <!-- تبويب الشات -->
    <div class="tabpane" id="pane-chat">
      <div class="chat-wrap">
        <div class="chat-top">
          <span class="live"><i></i>14 متّصل الآن</span>
          <span class="mod">🛡️ مُدار بإشراف — بيئة آمنة ومحترمة</span>
        </div>
        <div class="chat-body" id="chatBody">
          <div class="msg">
            <span class="av" style="background:#5B7FE0">نو</span>
            <div class="bub"><div class="nm">نورة ا. <span class="uni">· جامعة طيبة</span></div><div class="tx">السلام عليكم، أي أحد فهم درس التكامل بالتجزئة؟ 😅</div></div>
          </div>
          <div class="msg">
            <span class="av" style="background:#2FB39A">في<span class="modbadge"></span></span>
            <div class="bub"><div class="nm">فيصل (مشرف) <span class="modbadge">🛡️ مرشد</span></div><div class="tx">عليكم السلام نورة! أكيد، فيه ملخص ممتاز له في تبويب المصادر، وأقدر أشرحه لك خطوة خطوة. ابدئي بقاعدة LIATE لاختيار u.</div></div>
          </div>
          <div class="msg">
            <span class="av" style="background:#F4A261">عب</span>
            <div class="bub"><div class="nm">عبدالله ر. <span class="uni">· جامعة الأمير مقرن</span></div><div class="tx">أنا بعد كنت متعثّر فيه، الفيديو اللي بالمصادر طلّع لي الزبدة 👌</div></div>
          </div>
          <div class="msg me">
            <span class="av" style="background:linear-gradient(135deg,#14B8A6,#0F4C46)">أنا</span>
            <div class="bub"><div class="tx">تمام، بشوف الملخص وأرجع لكم لو احتجت 🙏</div></div>
          </div>
        </div>
        <div class="chat-input">
          <input type="text" id="chatInput" placeholder="اكتب رسالتك للمجتمع..." onkeydown="if(event.key==='Enter')sendMsg()">
          <button onclick="sendMsg()" aria-label="إرسال">➤</button>
        </div>
        <div class="chat-rooms">
          <span class="room on">💬 عام</span>
          <span class="room">📝 قبل الاختبار</span>
          <span class="room">🎧 غرفة مذاكرة مباشرة</span>
        </div>
      </div>
    </div>

    <!-- تبويب الأسئلة -->
    <div class="tabpane" id="pane-q">
      <div class="card-h" style="margin-bottom:16px"><h3 style="font-family:'Tajawal';font-size:18px">أسئلة وأجوبة محفوظة</h3><a style="color:var(--teal);font-weight:600;cursor:pointer">اطرح سؤال +</a></div>
      <div class="q">
        <div class="who"><span class="av" style="background:#5B7FE0">نو</span><div><b>نورة ا.</b><small>قبل 8 دقائق · جامعة طيبة</small></div></div>
        <div class="qt">في مسألة الـ limit لما أعوّض ويطلع 0/0 — متى أستخدم لوبيتال ومتى أبسّط بالعامل المشترك؟ 🤔</div>
        <div class="qf"><span class="ans">✓ 3 إجابات</span><span>♡ 12</span><span class="rep">شارك بإجابة</span></div>
      </div>
      <div class="q">
        <div class="who"><span class="av" style="background:#0EA5A0">سا</span><div><b>سارة م.</b><small>قبل ساعة · جامعة الأمير مقرن</small></div></div>
        <div class="qt">خلّصت تمارين 14.7، أي أحد يبي نراجع نقاط الـ saddle مع بعض المغرب؟ 📈</div>
        <div class="qf"><span class="ans">✓ 5 إجابات</span><span>♡ 27</span><span class="rep">انضم</span></div>
      </div>
      <div class="q">
        <div class="who"><span class="av" style="background:#C065C0">رغ</span><div><b>رغد ع.</b><small>أمس · جامعة القصيم</small></div></div>
        <div class="qt">وش أفضل ترتيب أذاكر فيه المادة للنهائي؟ حاسة إني متشتتة وما أعرف من وين أبدأ 😞</div>
        <div class="qf"><span class="ans">✓ 7 إجابات</span><span>♡ 41</span><span class="rep">شارك بإجابة</span></div>
      </div>
    </div>

  </div></section>
</div>

<!-- ============ المواهب (الفئات) ============ -->
<div class="view" id="v-talents">
  <div class="page-head">
    <div class="wrap">
      <div class="ic">🎯</div>
      <div>
        <h2>مسار المواهب</h2>
        <p>اختر مجال موهبتك، وندخلك مجتمعاً يصقلك ويدعمك</p>
      </div>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="note-bar">
      <span>💡</span>
      <span><b>كيف تتوسّع المجالات؟</b> نبدأ بالأكثر طلباً. وخانة «أخرى» تجمع اهتماماتكم — فلما يتجمّع طلب كافٍ على مجال جديد، نفتحه رسمياً. المنصة تنمو ببياناتكم، لا بتخميننا.</span>
    </div>
    <div class="cats">
      <button class="cat" onclick="openCommunity('الرياضة','🏅')"><div class="ce">🏅</div><b>رياضة</b><small>بمختلف أنواعها</small></button>
      <button class="cat" onclick="openCommunity('الرياضات الإلكترونية','🎮')"><div class="ce">🎮</div><b>eSports</b><small>رياضات إلكترونية</small></button>
      <button class="cat" onclick="openCommunity('ريادة الأعمال','💡')"><div class="ce">💡</div><b>ريادة الأعمال</b><small>مشاريع وابتكار</small></button>
      <button class="cat" onclick="openCommunity('الكتابة','✍️')"><div class="ce">✍️</div><b>الكتابة</b><small>قصص ومقالات</small></button>
      <button class="cat" onclick="openCommunity('الرسم','🎨')"><div class="ce">🎨</div><b>الرسم</b><small>فنون بصرية</small></button>
      <button class="cat" onclick="openCommunity('الخط','🖋️')"><div class="ce">🖋️</div><b>الخط</b><small>خط عربي وزخرفة</small></button>
      <button class="cat" onclick="openCommunity('الصوت','🎤')"><div class="ce">🎤</div><b>صوت جميل</b><small>إلقاء وإنشاد</small></button>
      <button class="cat" onclick="openCommunity('الشطرنج','♟️')"><div class="ce">♟️</div><b>الشطرنج</b><small>تكتيك وتفكير استراتيجي</small></button>
      <button class="cat other" onclick="openOther()"><div class="ce">➕</div><b>أخرى</b><small>اذكر موهبتك</small></button>
    </div>

    <div class="discover-cta">
      <div class="dic">🧭</div>
      <div class="dt"><b>ما تعرف موهبتك؟ هذا طبيعي.</b><p>كثير عندهم طاقة بس ما اكتشفوا مجالهم. جاوب 3 أسئلة قصيرة ونرشّح لك مسارك.</p></div>
      <button class="btn btn-primary btn-sm" onclick="show('discover',document.getElementById('n-discover'))">اكتشف موهبتك ›</button>
    </div>
  </div></section>
</div>

<!-- ============ مجتمع الموهبة (نمط ديسكورد — يظهر بعد اختيار تخصص) ============ -->
<div class="view" id="v-talent-community">
  <div class="page-head">
    <div class="wrap">
      <div class="ic" id="tc-ic">🎯</div>
      <div>
        <h2 id="tc-title">مجتمع الموهبة</h2>
        <p id="tc-sub">رحلتك في صقل موهبتك تبدأ هنا</p>
      </div>
      <button class="btn btn-ghost btn-sm" style="margin-right:auto" onclick="show('talents',document.getElementById('n-talents'))">‹ كل المجالات</button>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="care">
      <span class="e">🔥</span>
      <p><b>الأبطال ما انبنوا بيوم — انبنوا بستريك.</b> كل يوم تتمرّن وتوثّق، تقترب خطوة من مستوى يستحق العرض على المستكشفين.</p>
    </div>
    <div class="grid-2">
      <div>
        <!-- قنوات المجتمع (نمط ديسكورد) -->
        <div class="chan-row" id="tcChans"></div>
        <div class="chat-wrap" style="margin-bottom:22px">
          <div class="chat-top">
            <span class="live"><i></i><span id="tcOnline">37</span> متّصل الآن</span>
            <span class="mod">🛡️ مُدار بإشراف — بيئة محترمة</span>
          </div>
          <div class="chat-body" id="tcChat"></div>
          <div class="chat-input">
            <input type="text" id="tcInput" placeholder="شارك مجتمعك..." onkeydown="if(event.key==='Enter')sendTcMsg()">
            <button onclick="sendTcMsg()" aria-label="إرسال">➤</button>
          </div>
        </div>

        <!-- نصائح ذكية -->
        <div class="card">
          <div class="card-h"><div><h3>💡 نصائح ذكية — طبّقها اليوم</h3><div class="csub" id="tcTipsSub">حيل عملية مجرّبة تشوف أثرها بسرعة</div></div></div>
          <div id="tcTips"></div>
        </div>

        <div class="scout">
          <span class="stag">🏆 فرصتك الحقيقية</span>
          <h3>اعرض موهبتك لمستكشفي الأداء</h3>
          <p>وصلت لمستوى متقدّم؟ ارفع ملف أدائك بمواصفات احترافية مع توصية مرشدك — ونعرضه على الجهات الباحثة عن المواهب في مجالك.</p>
          <div class="reqs">
            <div class="req"><span class="c">1</span> عيّنة أو فيديو واضح (دقيقة–دقيقتين) يبرز مهارتك</div>
            <div class="req"><span class="c">2</span> نص تعريفي بمستواك وإنجازاتك</div>
            <div class="req"><span class="c">3</span> توصية موثّقة من مرشدك في المنصة</div>
          </div>
          <button class="btn btn-primary btn-sm" style="background:linear-gradient(135deg,var(--warm),var(--warm-d));position:relative;z-index:2">جهّز ملف العرض ›</button>
        </div>
      </div>

      <div class="side">
        <div class="sbox" style="background:linear-gradient(160deg,var(--deep),var(--deep2));color:#fff;border-radius:18px;padding:22px;margin-bottom:20px;text-align:center">
          <div style="font-size:40px;line-height:1">🔥</div>
          <div style="font-family:'Tajawal';font-weight:800;font-size:34px;margin:6px 0">90 <span style="font-size:18px;font-weight:600">يوم</span></div>
          <div style="font-size:13px;color:#BFDAD5">تحدّي الـ 90 يوم — التزامك المتواصل في صقل موهبتك</div>
          <div class="bar" style="margin-top:14px"><i style="width:46%"></i></div>
          <div style="font-size:12px;color:#9FD8CF;margin-top:8px">اليوم 41 من 90 — نص الطريق تقريباً 💪</div>
        </div>

        <div class="card" style="margin-bottom:20px">
          <div class="card-h"><h3 id="tc-mentor-h">مرشدك في المجال</h3></div>
          <div style="display:flex;gap:13px;align-items:center">
            <span class="av" id="tc-mentor-av" style="background:linear-gradient(135deg,var(--teal),var(--warm));margin:0;width:50px;height:50px;border:none">م</span>
            <div><b style="font-family:'Tajawal';font-size:15px" id="tc-mentor-name">مرشد مؤهل</b><div style="color:var(--muted);font-size:13px" id="tc-mentor-role">يضع خطتك ويتابع تقدّمك بالـ Feedback</div></div>
          </div>
          <button class="btn btn-primary btn-sm" style="width:100%;margin-top:16px;justify-content:center" onclick="openPlans(window.curCommunity||'تدريب وإرشاد')">ابدأ معه مجاناً 7 أيام ›</button>
        </div>

        <div class="card" style="margin-bottom:20px">
          <div class="card-h"><div><h3 id="tc-h">خطتك التدريبية</h3><div class="csub" id="tc-plan-sub">برنامج 3 أيام بالأسبوع مع متابعة مرشدك</div></div></div>
          <div class="week-days">
            <div class="wday done"><b>السبت</b><small>تمرين ✓</small></div>
            <div class="wday done"><b>الإثنين</b><small>تمرين ✓</small></div>
            <div class="wday on"><b>الأربعاء</b><small>اليوم</small></div>
            <div class="wday"><b>باقي</b><small>راحة</small></div>
          </div>
          <div style="font-size:12.5px;color:var(--muted);margin-top:10px">التزامك هالأسبوع: <b style="color:var(--good);font-family:'Tajawal'">يومين من 3</b> — باقي تمرين اليوم 💪</div>
        </div>

        <div class="card">
          <div class="card-h"><div><h3>⭐ نجوم المجال</h3><div class="csub">بملايين المتابعين — تعلّم من الأفضل</div></div></div>
          <div id="tcStars"></div>
        </div>
      </div>
    </div>
  </div></section>
</div>

<!-- ============ مجتمعات (الواجهة الرئيسية للمجتمعات) ============ -->
<div class="view" id="v-communities">
  <div class="page-head">
    <div class="wrap">
      <div class="ic">🌐</div>
      <div>
        <h2>مجتمعات</h2>
        <p>اختر مجالك، وانضم لمجتمعه — تخصصات، أبطال، مؤثرون، ومستكشفون</p>
      </div>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="pillnav">
      <button class="on" id="ct-comm" onclick="commTab('comm')">🧩 المجتمعات</button>
      <button id="ct-gchat" onclick="commTab('gchat')">💬 الشات العام</button>
      <button id="ct-board" onclick="commTab('board')">🔥 الصدارة</button>
      <button id="ct-infl" onclick="commTab('infl')">⭐ مؤثرون</button>
      <button id="ct-scouts" onclick="commTab('scouts')">🔍 المستكشفون</button>
    </div>

    <!-- 1) المجتمعات -->
    <div class="commpane on" id="cp-comm">
      <div class="note-bar">
        <span>💡</span>
        <span><b>لكل اهتمام مجتمع، ولكل مجتمع تخصصاته.</b> اختر مجالك وندخلك على تخصصاته — كل تخصص له مجتمعه الخاص ومرشده المتخصص وأبطاله. الانضمام والشات مجاناً.</span>
      </div>
      <div class="cats">
        <button class="cat" onclick="openCommunity('الرياضة','🏅')"><div class="ce">🏅</div><b>رياضة</b><small>8 تخصصات · كرة قدم، سلة…</small></button>
        <button class="cat" onclick="openCommunity('الرياضات الإلكترونية','🎮')"><div class="ce">🎮</div><b>eSports</b><small>8 ألعاب تنافسية</small></button>
        <button class="cat" onclick="openCommunity('ريادة الأعمال','💡')"><div class="ce">💡</div><b>ريادة الأعمال</b><small>7 مهارات أساسية</small></button>
        <button class="cat" onclick="openCommunity('الكتابة','✍️')"><div class="ce">✍️</div><b>الكتابة</b><small>7 أنواع كتابية</small></button>
        <button class="cat" onclick="openCommunity('الرسم','🎨')"><div class="ce">🎨</div><b>الرسم</b><small>8 أساليب وأنواع</small></button>
        <button class="cat" onclick="openCommunity('الخط','🖋️')"><div class="ce">🖋️</div><b>الخط</b><small>7 أنواع خطوط</small></button>
        <button class="cat" onclick="openCommunity('الصوت','🎤')"><div class="ce">🎤</div><b>صوت جميل</b><small>6 مجالات صوتية</small></button>
        <button class="cat" onclick="openCommunity('الشطرنج','♟️')"><div class="ce">♟️</div><b>الشطرنج</b><small>7 تخصصات · افتتاحيات، بليتز…</small></button>
        <button class="cat other" onclick="openOther()"><div class="ce">➕</div><b>أخرى</b><small>اقترح مجتمعاً</small></button>
      </div>
    </div>

    <!-- 2) الشات العام -->
    <div class="commpane" id="cp-gchat">
      <div class="note-bar">
        <span>💬</span>
        <span><b>الشات العام لكل المجالات.</b> دردشة مفتوحة بين كل الشباب — بدّل بين الغرف حسب اهتمامك. 🛡️ مُدار بإشراف لبيئة آمنة ومحترمة.</span>
      </div>
      <div class="chat-wrap">
        <div class="chat-top">
          <span class="live"><i></i>312 متّصل الآن</span>
          <span class="mod">🛡️ مُدار بإشراف</span>
        </div>
        <div class="chat-body" id="gchatBody">
          <div class="msg">
            <span class="av" style="background:#0EA5A0">سا</span>
            <div class="bub"><div class="nm">سارة م. <span class="uni">· مجتمع الرسم</span></div><div class="tx">أحد جرّب تحدّي الرسم اليومي؟ حسّيت إنه رفع التزامي بشكل كبير 🎨</div></div>
          </div>
          <div class="msg">
            <span class="av" style="background:#5B7FE0">في</span>
            <div class="bub"><div class="nm">فيصل د. <span class="uni">· مجتمع eSports</span></div><div class="tx">أنا بعد! الستريك حقي وصل 27 يوم 🔥 الإصرار شي ثاني</div></div>
          </div>
          <div class="msg">
            <span class="av" style="background:#2FB39A">مر<span class="modbadge"></span></span>
            <div class="bub"><div class="nm">مرشد (مشرف) <span class="modbadge">🛡️ مشرف</span></div><div class="tx">أبطال 👏 خلوا نشاطكم متوازن مع الراحة والمذاكرة. لو حد حاس بضغط، تجربة الإرشاد متاحة مجاناً 7 أيام.</div></div>
          </div>
          <div class="msg me">
            <span class="av" style="background:linear-gradient(135deg,#14B8A6,#0F4C46)">أنا</span>
            <div class="bub"><div class="tx">حلو! أنا أبدأ من اليوم وأشارككم تقدّمي 💪</div></div>
          </div>
        </div>
        <div class="chat-input">
          <input type="text" id="gchatInput" placeholder="اكتب رسالتك للمجتمع العام..." onkeydown="if(event.key==='Enter')sendGMsg()">
          <button onclick="sendGMsg()" aria-label="إرسال">➤</button>
        </div>
        <div class="chat-rooms">
          <span class="room on">🌐 عام</span>
          <span class="room">🏅 رياضة</span>
          <span class="room">🎮 eSports</span>
          <span class="room">💡 ريادة</span>
          <span class="room">✍️ كتابة</span>
          <span class="room">🎨 رسم</span>
          <span class="room">🖋️ خط</span>
          <span class="room">🎤 صوت</span>
          <span class="room">♟️ شطرنج</span>
          <span class="room">📚 أكاديمي</span>
        </div>
      </div>
    </div>

    <!-- 3) الصدارة -->
    <div class="commpane" id="cp-board">
      <div class="note-bar">
        <span>🔥</span>
        <span><b>أطول ستريك في كل مجال.</b> الستريك = أيام التزامك المتواصلة (تمرين، توثيق، أو مشاركة). فلتر حسب المجال وشوف أبطال كل مجتمع.</span>
      </div>
      <div class="fpills">
        <span class="fp on" data-f="all" onclick="renderBoard('all')">الكل</span>
        <span class="fp" data-f="رياضة" onclick="renderBoard('رياضة')">🏅 رياضة</span>
        <span class="fp" data-f="esports" onclick="renderBoard('esports')">🎮 eSports</span>
        <span class="fp" data-f="ريادة" onclick="renderBoard('ريادة')">💡 ريادة</span>
        <span class="fp" data-f="كتابة" onclick="renderBoard('كتابة')">✍️ كتابة</span>
        <span class="fp" data-f="رسم" onclick="renderBoard('رسم')">🎨 رسم</span>
        <span class="fp" data-f="خط" onclick="renderBoard('خط')">🖋️ خط</span>
        <span class="fp" data-f="صوت" onclick="renderBoard('صوت')">🎤 صوت</span>
        <span class="fp" data-f="شطرنج" onclick="renderBoard('شطرنج')">♟️ شطرنج</span>
        <span class="fp" data-f="أكاديمي" onclick="renderBoard('أكاديمي')">📚 أكاديمي</span>
      </div>
      <div class="lb" id="lbList"></div>
    </div>

    <!-- 4) مؤثرون -->
    <div class="commpane" id="cp-infl">
      <div class="note-bar">
        <span>⭐</span>
        <span><b>تعلّم من الأفضل في العالم.</b> نجوم حقيقيون بملايين المتابعين في كل مجال — تابعهم، حلّل أسلوبهم، واستلهم رحلتهم. <span style="opacity:.85">(أرقام المتابعين تقريبية وقت الإعداد)</span></span>
      </div>
      <div class="inf-grid" id="infGrid"></div>
    </div>

    <!-- 5) المستكشفون -->
    <div class="commpane" id="cp-scouts">
      <div class="note-bar">
        <span>🔍</span>
        <span><b>مستكشفو الأداء.</b> جهات تبحث عن المواهب في كل مجال — طوّر مستواك ووثّقه، ونعرض الأبرز منكم عليهم.</span>
      </div>
      <div class="scout-grid">
        <div class="scard"><div class="sh"><span class="se">⚽</span><b>الأندية الرياضية وكشّافوها</b></div><p>تبحث عن لاعبين واعدين في كرة القدم والسلة والطائرة وغيرها.</p><div class="slk">↳ تتابع المتصدّرين في مجتمع الرياضة</div></div>
        <div class="scard"><div class="sh"><span class="se">🎮</span><b>فرق eSports المحترفة</b></div><p>تستقطب لاعبين بأداء عالٍ في الألعاب التنافسية للانضمام لفرقها.</p><div class="slk">↳ تتابع المتصدّرين في مجتمع eSports</div></div>
        <div class="scard"><div class="sh"><span class="se">🚀</span><b>حاضنات ومسرّعات الأعمال</b></div><p>تبحث عن مؤسّسين ومشاريع ناشئة واعدة لدعمها واحتضانها.</p><div class="slk">↳ تتابع المتميّزين في مجتمع ريادة الأعمال</div></div>
        <div class="scard"><div class="sh"><span class="se">🎨</span><b>استوديوهات التصميم والإعلان</b></div><p>تبحث عن رسّامين ومصمّمين بأسلوب مميّز لمشاريع حقيقية.</p><div class="slk">↳ تتابع المتميّزين في مجتمعي الرسم والخط</div></div>
        <div class="scard"><div class="sh"><span class="se">📚</span><b>دور النشر والمجلات</b></div><p>تبحث عن كتّاب وأقلام واعدة لنشر أعمالهم وإبداعاتهم.</p><div class="slk">↳ تتابع المتميّزين في مجتمع الكتابة</div></div>
        <div class="scard"><div class="sh"><span class="se">🎤</span><b>شركات الإنتاج والتعليق الصوتي</b></div><p>تبحث عن أصوات مميّزة للتعليق والإنشاد والأداء الصوتي.</p><div class="slk">↳ تتابع المتميّزين في مجتمع الصوت</div></div>
        <div class="scard"><div class="sh"><span class="se">♟️</span><b>أندية واتحادات الشطرنج</b></div><p>تبحث عن لاعبين بتصنيفات صاعدة لضمّهم للأندية وتمثيلها في البطولات.</p><div class="slk">↳ تتابع المتصدّرين في مجتمع الشطرنج</div></div>
      </div>
      <div class="scout">
        <span class="stag">🏆 فرصتك الحقيقية</span>
        <h3>اعرض موهبتك لمستكشفي الأداء</h3>
        <p>وصلت لمستوى متقدّم في تخصصك؟ ارفع ملف أدائك بمواصفات احترافية مع توصية مرشدك — ونعرضه على الجهات الباحثة عن المواهب أعلاه.</p>
        <div class="reqs">
          <div class="req"><span class="c">1</span> عيّنة أو فيديو واضح يبرز مهارتك</div>
          <div class="req"><span class="c">2</span> نص تعريفي بمستواك وإنجازاتك</div>
          <div class="req"><span class="c">3</span> توصية موثّقة من مرشدك في المنصة</div>
        </div>
        <button class="btn btn-primary btn-sm" style="background:linear-gradient(135deg,var(--warm),var(--warm-d));position:relative;z-index:2">جهّز ملف العرض ›</button>
      </div>
    </div>

  </div></section>
</div>

<!-- ============ تخصصات المجتمع (يظهر بعد اختيار مجتمع) ============ -->
<div class="view" id="v-community-branches">
  <div class="page-head">
    <div class="wrap">
      <div class="ic" id="cb-ic">🏅</div>
      <div>
        <h2 id="cb-title">مجتمع</h2>
        <p id="cb-sub">اختر تخصصك</p>
      </div>
      <button class="btn btn-ghost btn-sm" style="margin-right:auto" onclick="show('communities',document.getElementById('n-communities'))">‹ كل المجتمعات</button>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="note-bar" id="branchNote"><span>💡</span><span>اختر تخصصك داخل هذا المجتمع.</span></div>
    <div class="cats" id="branchGrid"></div>
  </div></section>
</div>

<!-- ============ اكتشف موهبتك ============ -->
<div class="view" id="v-discover">
  <div class="page-head">
    <div class="wrap">
      <div class="ic">🧭</div>
      <div>
        <h2>اكتشف موهبتك</h2>
        <p>الوضوح يبدأ بمعرفة نفسك — اختر طريقة الاكتشاف</p>
      </div>
    </div>
  </div>
  <section class="section"><div class="wrap"><div class="disc-wrap">

    <!-- اختيار الطريقة -->
    <div id="discMethod">
      <div class="method-cards">
        <button class="method" onclick="startMethod('exp')">
          <div class="mie">🌱</div>
          <b>رحلة تجاربك</b>
          <p>أسئلة عن طفولتك، تجاربك السابقة، واللي تستمتع فيه. ميولك الحقيقية مدفونة في ماضيك.</p>
          <span class="mtag">4 أسئلة · ~3 دقائق</span>
        </button>
        <button class="method g" onclick="startMethod('gardner')">
          <div class="mie">🧠</div>
          <b>اختبار الذكاءات المتعددة</b>
          <p>30 سؤال مبني على نظرية جاردنر (Gardner) للذكاءات المتعددة، يحلّلها الذكاء الاصطناعي ويحدّد مسارك بدقة.</p>
          <span class="mtag">30 سؤال · تحليل AI 🤖</span>
        </button>
      </div>
    </div>

    <!-- طريقة 1: رحلة التجارب -->
    <div id="discExp" style="display:none">
      <div class="progress"><i class="on" id="ep1"></i><i id="ep2"></i><i id="ep3"></i><i id="ep4"></i></div>
      <div class="qstep active" id="eqs1">
        <div class="qn">السؤال 1 من 4</div>
        <h3>وش كنت تحب تسويه وأنت صغير وتستمتع فيه؟</h3>
        <div class="qhint">ميول الطفولة غالباً أصدق إشارة لموهبتك الفطرية.</div>
        <div class="choices">
          <button class="choice" onclick="ans2('exp',1,'physical')"><span class="che">🏃</span><b>ألعب وأتحرّك وأتنافس</b></button>
          <button class="choice" onclick="ans2('exp',1,'digital')"><span class="che">🎮</span><b>ألعب ألعاب أو أفكّك الأجهزة</b></button>
          <button class="choice" onclick="ans2('exp',1,'creative')"><span class="che">🎨</span><b>أرسم، ألوّن، أو أبني أشياء</b></button>
          <button class="choice" onclick="ans2('exp',1,'social')"><span class="che">🗣️</span><b>أقود ألعاب الجماعة وأنظّمهم</b></button>
        </div>
      </div>
      <div class="qstep" id="eqs2">
        <div class="qn">السؤال 2 من 4</div>
        <h3>وش النشاط اللي تنسى الوقت وأنت تسويه؟</h3>
        <div class="qhint">حالة "التدفّق" (Flow) — تنغمس وتنسى كل شي — أقوى مؤشر موهبة.</div>
        <div class="choices">
          <button class="choice" onclick="ans2('exp',2,'physical')"><span class="che">⚽</span><b>الرياضة والحركة</b></button>
          <button class="choice" onclick="ans2('exp',2,'digital')"><span class="che">💻</span><b>التقنية والألعاب</b></button>
          <button class="choice" onclick="ans2('exp',2,'creative')"><span class="che">🖌️</span><b>الرسم والكتابة والإبداع</b></button>
          <button class="choice" onclick="ans2('exp',2,'social')"><span class="che">🤝</span><b>التنظيم والتعامل مع الناس</b></button>
        </div>
      </div>
      <div class="qstep" id="eqs3">
        <div class="qn">السؤال 3 من 4</div>
        <h3>وش أكثر تجربة بحياتك حسّيت فيها بالفخر والإنجاز؟</h3>
        <div class="qhint">لحظات الفخر تكشف وين تتألّق طاقتك فعلاً.</div>
        <div class="choices">
          <button class="choice" onclick="ans2('exp',3,'physical')"><span class="che">🏅</span><b>فزت بمنافسة أو تحدّي بدني</b></button>
          <button class="choice" onclick="ans2('exp',3,'digital')"><span class="che">🖥️</span><b>بنيت/حليت شي تقني صعب</b></button>
          <button class="choice" onclick="ans2('exp',3,'creative')"><span class="che">✍️</span><b>أنتجت عملاً إبداعياً أعجب الناس</b></button>
          <button class="choice" onclick="ans2('exp',3,'social')"><span class="che">🎤</span><b>قدت فريقاً أو ألقيت/أقنعت</b></button>
        </div>
      </div>
      <div class="qstep" id="eqs4">
        <div class="qn">السؤال 4 من 4</div>
        <h3>الناس يجونك ويطلبون مساعدتك في أي شي؟</h3>
        <div class="qhint">اللي يراه الناس فيك، أحياناً تكون أنت آخر من ينتبه له.</div>
        <div class="choices">
          <button class="choice" onclick="ans2('exp',4,'physical')"><span class="che">💪</span><b>التمارين والرياضة</b></button>
          <button class="choice" onclick="ans2('exp',4,'digital')"><span class="che">⚙️</span><b>التقنية والأجهزة</b></button>
          <button class="choice" onclick="ans2('exp',4,'creative')"><span class="che">🎨</span><b>التصميم والكتابة والفن</b></button>
          <button class="choice" onclick="ans2('exp',4,'social')"><span class="che">🗣️</span><b>التنظيم والإقناع والكلام</b></button>
        </div>
      </div>
    </div>

    <!-- طريقة 2: اختبار جاردنر -->
    <div id="discGardner" style="display:none">
      <div class="progress" id="gprog"></div>
      <div class="qstep active" id="gqs1">
        <div class="qn">السؤال <span class="gnum">1</span> من 30 · ذكاء منطقي–رياضي</div>
        <h3>أستمتع بحل المسائل المنطقية والألغاز وأكتشف الأنماط بسهولة.</h3>
        <div class="qhint">جاوب بصدق حسب ما ينطبق عليك.</div>
        <div class="choices">
          <button class="choice" onclick="ansG(1,'digital')"><span class="che">✅</span><b>ينطبق عليّ تماماً</b></button>
          <button class="choice" onclick="ansG(1,'digital')"><span class="che">🔵</span><b>ينطبق أحياناً</b></button>
          <button class="choice" onclick="ansG(1,'social')"><span class="che">⚪</span><b>لا ينطبق عليّ</b></button>
        </div>
      </div>
      <div class="qstep" id="gqs2">
        <div class="qn">السؤال <span class="gnum">2</span> من 30 · ذكاء لغوي</div>
        <h3>أعبّر عن أفكاري بسهولة بالكلمات، وأحب القراءة والكتابة.</h3>
        <div class="qhint">جاوب بصدق حسب ما ينطبق عليك.</div>
        <div class="choices">
          <button class="choice" onclick="ansG(2,'creative')"><span class="che">✅</span><b>ينطبق عليّ تماماً</b></button>
          <button class="choice" onclick="ansG(2,'creative')"><span class="che">🔵</span><b>ينطبق أحياناً</b></button>
          <button class="choice" onclick="ansG(2,'physical')"><span class="che">⚪</span><b>لا ينطبق عليّ</b></button>
        </div>
      </div>
      <div class="qstep" id="gqs3">
        <div class="qn">السؤال <span class="gnum">3</span> من 30 · ذكاء حركي–جسدي</div>
        <h3>أتعلّم أسرع لما أتحرّك وأمارس بيدي، وأجيد الأنشطة البدنية.</h3>
        <div class="qhint">جاوب بصدق حسب ما ينطبق عليك.</div>
        <div class="choices">
          <button class="choice" onclick="ansG(3,'physical')"><span class="che">✅</span><b>ينطبق عليّ تماماً</b></button>
          <button class="choice" onclick="ansG(3,'physical')"><span class="che">🔵</span><b>ينطبق أحياناً</b></button>
          <button class="choice" onclick="ansG(3,'digital')"><span class="che">⚪</span><b>لا ينطبق عليّ</b></button>
        </div>
      </div>
      <div class="qstep" id="gqs4">
        <div class="qn">السؤال <span class="gnum">4</span> من 30 · ذكاء اجتماعي</div>
        <h3>أفهم مشاعر الناس بسهولة، وأقدر أقودهم وأنظّمهم وأقنعهم.</h3>
        <div class="qhint">جاوب بصدق حسب ما ينطبق عليك.</div>
        <div class="choices">
          <button class="choice" onclick="ansG(4,'social')"><span class="che">✅</span><b>ينطبق عليّ تماماً</b></button>
          <button class="choice" onclick="ansG(4,'social')"><span class="che">🔵</span><b>ينطبق أحياناً</b></button>
          <button class="choice" onclick="ansG(4,'digital')"><span class="che">⚪</span><b>لا ينطبق عليّ</b></button>
        </div>
      </div>
      <div class="qstep" id="gqs5">
        <div class="qn">السؤال <span class="gnum">5</span> من 30 · ذكاء بصري–مكاني</div>
        <h3>أتخيّل الأشكال والتصاميم بسهولة، وعندي حس فني وبصري.</h3>
        <div class="qhint">باقي الأسئلة تقيس بقية الذكاءات — ويحلّلها الـ AI.</div>
        <div class="choices">
          <button class="choice" onclick="ansG(5,'creative')"><span class="che">✅</span><b>ينطبق عليّ تماماً</b></button>
          <button class="choice" onclick="ansG(5,'creative')"><span class="che">🔵</span><b>ينطبق أحياناً</b></button>
          <button class="choice" onclick="ansG(5,'physical')"><span class="che">⚪</span><b>لا ينطبق عليّ</b></button>
        </div>
      </div>
    </div>

    <!-- تحليل AI -->
    <div class="ai-analyzing" id="aiAnalyzing">
      <div class="ai-spin">🤖</div>
      <h3>الذكاء الاصطناعي يحلّل إجاباتك...</h3>
      <p>نطابق نمط ذكاءاتك المتعددة مع المجالات الأنسب لك</p>
    </div>

    <!-- النتيجة -->
    <div class="disc-result" id="discResult">
      <div class="rok">✨</div>
      <h3>رشّحنا لك مسارك</h3>
      <p id="resultDesc">بناءً على إجاباتك، هذي المجالات الأقرب لميولك. جرّبها — الموهبة تتأكد بالتجربة مو بالتفكير.</p>
      <div class="matches" id="matches"></div>
      <button class="btn btn-primary" onclick="show('communities',document.getElementById('n-communities'))">ادخل مجتمع المجال المقترح ›</button>
      <div style="margin-top:14px"><button class="btn btn-ghost btn-sm" onclick="restartDiscover()">اختر طريقة ثانية</button></div>
    </div>

  </div></div></section>
</div>

<!-- ============ لوحتي ============ -->
<div class="view" id="v-dashboard">
  <div class="page-head">
    <div class="wrap">
      <div class="ic">🌙</div>
      <div>
        <h2>رحلتك في مواهب</h2>
        <p>مساء الخير، محمد — هنا يظهر نموّك يوماً بيوم</p>
      </div>
    </div>
  </div>
  <section class="section"><div class="wrap">
    <div class="sbox clarity" style="background:linear-gradient(160deg,var(--deep),var(--deep2));color:#fff;border-radius:18px;padding:26px;margin-bottom:24px">
      <div class="cl-h"><h4 style="font-size:16px">مؤشر النمو</h4><span>68%</span></div>
      <div class="bar"><i style="width:68%"></i></div>
      <small>ارتفع 12% هذا الأسبوع — كل تمرين توثّقه ومشاركة في مجتمعك ترفع المؤشر. استمر على نفس الإيقاع.</small>
    </div>
    <div class="dash-grid">
      <div class="metric"><div class="mt"><span class="e" style="background:rgba(217,180,90,.12)">🔥</span><b>الاستمرارية</b></div><div class="big">9 <small>أيام</small></div><div class="tr">أطول ستريك لك</div></div>
      <div class="metric"><div class="mt"><span class="e" style="background:rgba(31,191,156,.12)">👥</span><b>مجتمعاتك</b></div><div class="big">3</div><div class="tr">تفاضل · رسم · ريادة</div></div>
      <div class="metric"><div class="mt"><span class="e" style="background:rgba(255,255,255,.06)">💬</span><b>ساعدت</b></div><div class="big">11 <small>شخص</small></div><div class="tr">دعمك يرجع لك دعم</div></div>
      <div class="metric"><div class="mt"><span class="e" style="background:rgba(61,219,180,.12)">✓</span><b>أنجزت</b></div><div class="big">24 <small>مهمة</small></div><div class="tr">هذا الشهر</div></div>
    </div>
    <div class="mood">
      <b>وش مستوى حماسك اليوم؟</b>
      <div class="msub">نضبط خطة أسبوعك على قد طاقتك — يوم حماسك عالي نرفع التحدي، ويوم أقل نثبّت المكاسب.</div>
      <div class="faces" role="group" aria-label="تقييم المزاج">
        <button class="face" onclick="pickMood(this)" aria-label="متضايق">😔</button>
        <button class="face" onclick="pickMood(this)" aria-label="تعبان">😕</button>
        <button class="face sel" onclick="pickMood(this)" aria-label="عادي">🙂</button>
        <button class="face" onclick="pickMood(this)" aria-label="منشرح">😃</button>
        <button class="face" onclick="pickMood(this)" aria-label="متحمّس">🤩</button>
      </div>
    </div>
  </div></section>
</div>

<div class="foot">منصة <b>مواهب</b> · نموذج أولي تفاعلي — منصة الشباب لاكتشاف المواهب وتطويرها: من الهواية إلى الاحتراف<br>للتواصل: <a href="mailto:mawaaheb11@gmail.com">mawaaheb11@gmail.com</a></div>

<!-- مودال "أخرى" -->
<div class="modal" id="otherModal">
  <div class="modal-box">
    <div id="otherForm">
      <div class="mi">➕</div>
      <h3>اذكر موهبتك أو اهتمامك</h3>
      <p>ما لقيت مجالك في القائمة؟ اكتبه هنا. كل طلب نسجّله — ولما يتجمّع طلب كافٍ على مجالك، نفتح له مجتمعاً رسمياً.</p>
      <input type="text" id="otherInput" placeholder="مثال: التصوير، الطبخ، البرمجة، الفلك...">
      <div class="mrow">
        <button class="btn btn-primary" style="flex:1;justify-content:center" onclick="submitOther()">سجّل اهتمامي</button>
        <button class="btn btn-ghost" onclick="closeOther()">إلغاء</button>
      </div>
    </div>
    <div id="otherDone" style="text-align:center">
      <div class="ok" style="margin-inline:auto">✓</div>
      <h3>سجّلنا اهتمامك!</h3>
      <p id="otherMsg"></p>
      <button class="btn btn-primary" style="width:100%;justify-content:center" onclick="closeOther()">تمام</button>
    </div>
  </div>
</div>

<!-- مودال باقات الإرشاد/المتابعة -->
<div class="modal" id="plansModal">
  <div class="modal-box" style="max-width:640px">
    <div class="mi">🗓️</div>
    <h3 id="plansTitle">باقات الإرشاد الأكاديمي</h3>
    <p id="plansDesc">جلسات فردية مع مرشد مؤهل + متابعة وتوثيق لتطوّرك. اختر ما يناسبك:</p>
    <div class="trial" style="margin-bottom:18px">
      <div class="te">✨</div>
      <div class="tt"><b id="trialText">تجربة مجانية 7 أيام للإرشاد الأكاديمي</b><span>جرّب قبل ما تدفع — بدون أي التزام.</span></div>
      <button class="btn btn-primary btn-sm tbtn" onclick="closePlans()">ابدأ التجربة</button>
    </div>
    <div class="prices">
      <div class="price" onclick="pickPlan(this)">
        <div class="pname">استشارة واحدة</div>
        <div class="pamt">49 <small>ريال</small></div>
        <div class="pdesc">جلسة فردية واحدة — تشخيص وضعك ووضع خطة بداية</div>
      </div>
      <div class="price best" onclick="pickPlan(this)">
        <div class="pname">اشتراك شهري</div>
        <div class="pamt">199 <small>ريال/شهر</small></div>
        <div class="pdesc">4 جلسات إرشادية (جلسة أسبوعياً) + Feedback يومي لتوثيقك ومتابعة تطوّرك</div>
      </div>
      <div class="price" onclick="pickPlan(this)">
        <div class="pname">مكثّف</div>
        <div class="pamt">399 <small>ريال/شهر</small></div>
        <div class="pdesc">8 جلسات إرشادية (جلستين أسبوعياً) + Feedback يومي + أولوية للمستكشفين</div>
      </div>
    </div>
    <div class="price-note">💡 الخدمة الأساسية (المجتمعات والمصادر والشات) مجانية دائماً. الباقات للإرشاد الفردي والمتابعة فقط.<br><b>إرشاد وتوجيه — لا يُغني عن الاستشارة الطبية المتخصصة عند الحاجة.</b></div>
    <div style="display:flex;gap:10px;margin-top:18px">
      <button class="btn btn-primary" style="flex:1;justify-content:center" onclick="closePlans()">تأكيد الاشتراك</button>
      <button class="btn btn-ghost" onclick="closePlans()">لاحقاً</button>
    </div>
  </div>
</div>

<!-- مودال فتح مجتمع دراسي إضافي -->
<div class="modal" id="studyModal">
  <div class="modal-box">
    <div class="mi">🔓</div>
    <h3>افتح مجتمع <span id="studyName"></span></h3>
    <p>استخدمت مجتمعاتك الثلاثة المجانية. افتح هذا المجتمع الدراسي بـ <b>50 ريال</b> لمرة واحدة — يشمل كل مصادره وشاته وأسئلته بشكل دائم.</p>
    <div class="price-note" style="margin-bottom:16px">💡 أول 3 مجتمعات دراسية مجانية بالكامل. كل مجتمع إضافي بـ 50 ريال لمرة واحدة.</div>
    <div class="mrow">
      <button class="btn btn-primary" style="flex:1;justify-content:center" onclick="confirmStudy()">افتح بـ 50 ريال</button>
      <button class="btn btn-ghost" onclick="closeStudy()">لاحقاً</button>
    </div>
  </div>
</div>

<script>
  function show(id, btn){
    document.querySelectorAll('.view').forEach(v=>v.classList.remove('active'));
    document.getElementById('v-'+id).classList.add('active');
    document.querySelectorAll('.links button').forEach(b=>b.classList.remove('on'));
    if(btn && btn.id && btn.id.startsWith('n-')) btn.classList.add('on');
    window.scrollTo({top:0,behavior:'smooth'});
  }

  // صفحة المادة
  function openSubject(name, code, emoji){
    document.getElementById('sub-title').textContent = 'مجتمع: ' + name;
    document.getElementById('sub-ic').textContent = emoji;
    document.getElementById('sub-sub').innerHTML = code + ' · طلاب من جامعات المملكة · <span style="color:#7FE0D3">متّصلون الآن</span>';
    subTab('res');
    show('subject', document.getElementById('n-academic'));
  }
  function subTab(t){
    ['res','chat','q'].forEach(x=>{
      document.getElementById('tab-'+x).classList.toggle('on', x===t);
      document.getElementById('pane-'+x).classList.toggle('on', x===t);
    });
    if(t==='chat'){ const b=document.getElementById('chatBody'); b.scrollTop=b.scrollHeight; }
  }
  function sendMsg(){
    const inp=document.getElementById('chatInput'); const v=inp.value.trim(); if(!v)return;
    const body=document.getElementById('chatBody');
    const m=document.createElement('div'); m.className='msg me';
    m.innerHTML='<span class="av" style="background:linear-gradient(135deg,#14B8A6,#0F4C46)">أنا</span><div class="bub"><div class="tx"></div></div>';
    m.querySelector('.tx').textContent=v;
    body.appendChild(m); inp.value=''; body.scrollTop=body.scrollHeight;
  }

  // مودال أخرى
  function openOther(){ document.getElementById('otherModal').classList.add('show'); document.getElementById('otherForm').style.display='block'; document.getElementById('otherDone').style.display='none'; document.getElementById('otherInput').value=''; setTimeout(()=>document.getElementById('otherInput').focus(),100); }
  function closeOther(){ document.getElementById('otherModal').classList.remove('show'); }
  function submitOther(){
    const v = document.getElementById('otherInput').value.trim();
    if(!v){ document.getElementById('otherInput').focus(); return; }
    document.getElementById('otherMsg').textContent = 'بنخبرك أول ما نفتح مجتمع «'+v+'». كل ما زاد عدد المهتمين بنفس المجال، أسرعنا في فتحه.';
    document.getElementById('otherForm').style.display='none';
    document.getElementById('otherDone').style.display='block';
  }

  // طاقة اليوم
  function pickMood(btn){ document.querySelectorAll('.face').forEach(f=>f.classList.remove('sel')); btn.classList.add('sel'); }

  // باقات التوجيه — متأقلمة حسب المجال
  function openPlans(ctx){
    var academic = (ctx==='أكاديمي' || ctx==='توجيه');
    var cfg = MENTOR[ctx] || (academic ? MENTOR['أكاديمي'] : {m:'مرشدك', mr:'مرشد مؤهل'});
    document.getElementById('plansTitle').textContent = academic ? 'باقات الإرشاد الأكاديمي' : ('باقات الإرشاد مع ' + cfg.m);
    document.getElementById('plansDesc').textContent = academic
      ? 'جلسات فردية مع مرشد أكاديمي مؤهل، مع متابعة يومية (feedback) لتوثيق تطوّرك أسبوعاً بأسبوع.'
      : ('جلسات فردية مع ' + cfg.mr + '، مع متابعة يومية (feedback) لتوثيق تطوّرك أسبوعاً بأسبوع.');
    document.getElementById('trialText').textContent = academic
      ? 'ابدأها بتجربة مجانية 7 أيام للإرشاد الأكاديمي — بدون أي رسوم.'
      : ('ابدأها بتجربة مجانية 7 أيام مع ' + cfg.m + ' — بدون أي رسوم.');
    document.getElementById('plansModal').classList.add('show');
  }
  function closePlans(){ document.getElementById('plansModal').classList.remove('show'); }
  function pickPlan(el){ document.querySelectorAll('.price').forEach(p=>p.classList.remove('best')); el.classList.add('best'); }

  // الاكتشاف — طريقتان
  const ans = {}; let curMethod='exp';
  const TALENTS = {
    physical:{e:'🏅',n:'الرياضة'}, digital:{e:'🎮',n:'الرياضات الإلكترونية / الشطرنج'},
    creative:{e:'🎨',n:'الفنون والكتابة'}, social:{e:'💡',n:'ريادة الأعمال والإلقاء'}
  };

  function startMethod(m){
    curMethod=m; for(let k in ans) delete ans[k];
    document.getElementById('discMethod').style.display='none';
    if(m==='exp'){
      document.getElementById('discExp').style.display='block';
    } else {
      let prog=''; for(let i=0;i<30;i++) prog+='<i'+(i===0?' class="on"':'')+' id="gp'+(i+1)+'"></i>';
      document.getElementById('gprog').innerHTML=prog;
      document.getElementById('gprog').style.flexWrap='wrap';
      document.getElementById('discGardner').style.display='block';
    }
  }

  function ans2(method, step, val){
    ans[step]=val;
    document.getElementById('ep'+step).classList.add('on');
    if(step<4){
      document.getElementById('eqs'+step).classList.remove('active');
      document.getElementById('eqs'+(step+1)).classList.add('active');
    } else { finishDiscover(false); }
  }

  function ansG(step, val){
    ans[step]=val;
    for(let i=0;i<6;i++){ const idx=(step-1)*6+i+1; const el=document.getElementById('gp'+idx); if(el)el.classList.add('on'); }
    if(step<5){
      document.getElementById('gqs'+step).classList.remove('active');
      document.getElementById('gqs'+(step+1)).classList.add('active');
    } else {
      document.getElementById('discGardner').style.display='none';
      const ai=document.getElementById('aiAnalyzing'); ai.classList.add('show');
      setTimeout(()=>{ ai.classList.remove('show'); finishDiscover(true); }, 2200);
    }
  }

  function finishDiscover(isAI){
    const tally={}; Object.values(ans).forEach(v=>tally[v]=(tally[v]||0)+1);
    const sorted = Object.keys(tally).sort((a,b)=>tally[b]-tally[a]);
    const all=['physical','digital','creative','social'];
    const ordered=[...sorted, ...all.filter(x=>!sorted.includes(x))].slice(0,3);
    const pcts=['تطابق 92%','تطابق 74%','تطابق 58%'];
    const box=document.getElementById('matches'); box.innerHTML='';
    ordered.forEach((k,i)=>{
      const t=TALENTS[k];
      box.innerHTML += '<div class="match"><div class="me">'+t.e+'</div><b>'+t.n+'</b><span class="pct">'+pcts[i]+'</span></div>';
    });
    document.getElementById('resultDesc').textContent = isAI
      ? 'حلّل الذكاء الاصطناعي نمط ذكاءاتك المتعددة (جاردنر)، وهذي المجالات الأقرب لمسارك. جرّبها — الموهبة تتأكد بالتجربة.'
      : 'بناءً على تجاربك وميولك، هذي المجالات الأقرب لك. جرّبها — الموهبة تتأكد بالتجربة مو بالتفكير.';
    document.getElementById('discResult').classList.add('show');
  }

  function restartDiscover(){
    for(let k in ans) delete ans[k];
    document.getElementById('discResult').classList.remove('show');
    document.getElementById('aiAnalyzing').classList.remove('show');
    document.getElementById('discExp').style.display='none';
    document.getElementById('discGardner').style.display='none';
    document.querySelectorAll('#discExp .qstep').forEach((q,i)=>q.classList.toggle('active',i===0));
    document.querySelectorAll('#discExp .progress i').forEach((p,i)=>p.classList.toggle('on',i===0));
    document.querySelectorAll('#discGardner .qstep').forEach((q,i)=>q.classList.toggle('active',i===0));
    document.getElementById('discMethod').style.display='block';
  }

  /* ============ مرشدو المجالات (أسماء افتراضية لمرشدين مؤهلين) ============ */
  const MENTOR = {
    'الرياضة':              {n:'كابتن بدر العنزي',      m:'مدرّبك',          mr:'مدرّب معتمد — سابقاً لاعب دوري الدرجة الأولى', plan:'خطتك التدريبية',    planSub:'تمارين مهارية أسبوعية + متابعة أدائك ولياقتك'},
    'الرياضات الإلكترونية': {n:'كوتش طلال «TLL»',       m:'كوتشك',           mr:'كوتش محترف — خبرة بطولات إقليمية',            plan:'خطتك التدريبية',    planSub:'تحليل Gameplay + تمارين ميكانيكية أسبوعية'},
    'ريادة الأعمال':        {n:'أ. سلمان الحربي',       m:'مرشدك الريادي',   mr:'مؤسس متمرّس — خرّج مشاريع من حاضنات محلية',    plan:'خطة نموك الريادي',  planSub:'مهارة أسبوعية: تسويق، مبيعات، عرض وإقناع'},
    'الكتابة':              {n:'أ. وضحى القحطاني',      m:'محرّرتك',         mr:'كاتبة ومحرّرة — إشراف على إصدارات منشورة',     plan:'خطتك الإبداعية',    planSub:'تمارين كتابة أسبوعية + تحرير نصوصك'},
    'الرسم':                {n:'أ. مشعل الزهراني',      m:'مرشدك الفني',     mr:'فنان محترف — أعمال في معارض محلية',            plan:'خطتك الإبداعية',    planSub:'تمارين رسم أسبوعية + نقد بنّاء لأعمالك'},
    'الخط':                 {n:'الخطّاط إبراهيم النجدي', m:'أستاذك',          mr:'خطّاط مجاز بالسند في النسخ والثلث',            plan:'خطتك في المشق',     planSub:'مشق أسبوعي + تصحيح مساراتك حرفاً حرفاً'},
    'الصوت':                {n:'أ. ماجد السلمي',        m:'مدرّب صوتك',      mr:'مدرّب صوت وأداء — خلفية إذاعية',               plan:'خطتك التدريبية',    planSub:'تمارين تنفس وإلقاء أسبوعية + تقييم تسجيلاتك'},
    'الشطرنج':              {n:'م. حاتم الشمري',        m:'مدرّبك',          mr:'مدرّب شطرنج معتمد (FIDE) — تصنيف 2100+',       plan:'خطتك التدريبية',    planSub:'ألغاز يومية + تحليل مبارياتك أسبوعياً'},
    'أكاديمي':              {n:'أ. عبدالعزيز الدوسري',  m:'مرشدك الأكاديمي', mr:'مرشد أكاديمي مؤهل',                            plan:'خطتك الدراسية',     planSub:'جلسات أسبوعية + متابعة يومية لتوثيق تطوّرك'}
  };

  /* تفرّعات كل مجتمع (خاصة بمجاله) */
  const BRANCHES = {
    'الرياضة':[
      {e:'⚽',n:'كرة القدم',meta:'لاعبون ومواهب الميدان'},{e:'🏀',n:'كرة السلة',meta:'مهارات وتمرير وتسديد'},
      {e:'🏐',n:'الكرة الطائرة',meta:'إرسال واستقبال وهجوم'},{e:'🏓',n:'تنس الطاولة',meta:'سرعة ودوران وردود'},
      {e:'🏊',n:'السباحة',meta:'سرعة وتحمّل'},{e:'🏃',n:'ألعاب القوى',meta:'جري وقفز ورمي'},
      {e:'🤾',n:'كرة اليد',meta:'سرعة وتكتيك'},{e:'🥋',n:'الفنون القتالية',meta:'كاراتيه وتايكوندو وجودو'}
    ],
    'الرياضات الإلكترونية':[
      {e:'⚽',n:'EA FC',meta:'كرة قدم تنافسية'},{e:'🎯',n:'Valorant',meta:'تكتيكي 5v5'},
      {e:'⚔️',n:'League of Legends',meta:'MOBA تنافسي'},{e:'🔫',n:'PUBG',meta:'باتل رويال'},
      {e:'🚗',n:'Rocket League',meta:'سيارات وكرة'},{e:'🛡️',n:'Fortnite',meta:'بناء وقتال'},
      {e:'🥊',n:'Street Fighter',meta:'قتال فردي'},{e:'🎮',n:'Call of Duty',meta:'تصويب وسرعة'}
    ],
    'ريادة الأعمال':[
      {e:'📣',n:'التسويق الرقمي',meta:'محتوى وإعلانات ونمو'},{e:'🤝',n:'المبيعات والإقناع',meta:'إغلاق الصفقات'},
      {e:'🧩',n:'بناء المنتج',meta:'من الفكرة للإطلاق'},{e:'🎤',n:'العرض والإلقاء (Pitching)',meta:'عرض مشروعك بثقة'},
      {e:'💰',n:'التمويل والتسعير',meta:'أرقام ونماذج ربح'},{e:'⚙️',n:'إدارة العمليات',meta:'تنظيم وكفاءة'},
      {e:'✨',n:'بناء العلامة',meta:'هوية وقصة تجارية'}
    ],
    'الكتابة':[
      {e:'📖',n:'القصة القصيرة',meta:'حبكة في صفحات'},{e:'📚',n:'الرواية',meta:'بناء عوالم وشخصيات'},
      {e:'🪶',n:'الشعر',meta:'وزن وصورة وإحساس'},{e:'📝',n:'المقال',meta:'رأي وإقناع'},
      {e:'✍️',n:'كتابة المحتوى',meta:'محتوى رقمي وتسويقي'},{e:'🎬',n:'السيناريو',meta:'حوار ومشاهد'},
      {e:'🌙',n:'الكتابة الإبداعية',meta:'أسلوب وخيال'}
    ],
    'الرسم':[
      {e:'🖌️',n:'الرسم الرقمي',meta:'Procreate وPhotoshop'},{e:'✏️',n:'الرسم بالرصاص',meta:'ظل ونور وتفاصيل'},
      {e:'💧',n:'الألوان المائية',meta:'شفافية وتدرّج'},{e:'🎨',n:'الرسم الزيتي',meta:'لون وعمق'},
      {e:'🌸',n:'الأنمي والمانجا',meta:'أسلوب ياباني'},{e:'👤',n:'البورتريه',meta:'ملامح وتعبير'},
      {e:'🖼️',n:'الرسم الواقعي',meta:'دقة ومحاكاة'},{e:'😄',n:'الكاريكاتير',meta:'مبالغة ساخرة'}
    ],
    'الخط':[
      {e:'✒️',n:'خط الرقعة',meta:'سريع وعملي'},{e:'📜',n:'خط النسخ',meta:'واضح للقراءة'},
      {e:'🕌',n:'خط الثلث',meta:'فخم وزخرفي'},{e:'🖋️',n:'الخط الديواني',meta:'متشابك وأنيق'},
      {e:'🔷',n:'الخط الكوفي',meta:'هندسي وقديم'},{e:'🌹',n:'الخط الفارسي',meta:'انسيابي ورشيق'},
      {e:'🎴',n:'الخط الحر',meta:'تكوينات فنية'}
    ],
    'الصوت':[
      {e:'📿',n:'تلاوة القرآن',meta:'تجويد ومقامات'},{e:'🎵',n:'الإنشاد',meta:'أداء وطبقات'},
      {e:'🎙️',n:'الإلقاء والخطابة',meta:'ثقة وتأثير'},{e:'🎧',n:'التعليق الصوتي',meta:'إعلانات ووثائقي'},
      {e:'🎤',n:'الأداء الصوتي',meta:'تمثيل بالصوت'},{e:'🎬',n:'الدوبلاج',meta:'مزامنة وشخصيات'}
    ],
    'الشطرنج':[
      {e:'📖',n:'الافتتاحيات',meta:'إيطالية، إسبانية، صقلية'},
      {e:'⚡',n:'التكتيكات',meta:'شوكة، تثبيت، كشف'},
      {e:'👑',n:'النهايات',meta:'ملك وبيادق وقلاع'},
      {e:'⏱️',n:'البليتز والرابيد',meta:'قرارات تحت الضغط'},
      {e:'🏛️',n:'الشطرنج الكلاسيكي',meta:'مباريات طويلة وعمق'},
      {e:'🧩',n:'حل الألغاز',meta:'رفع التصنيف بالتكتيك'},
      {e:'🌐',n:'الشطرنج أونلاين',meta:'Chess.com وLichess'}
    ]
  };

  /* ============ حزمة كل مجال: قنوات + شات حي + نصائح + نجوم ============ */
  const AV_COLORS=['#0EA5A0','#F4A261','#5B7FE0','#C065C0','#2FB39A','#7C3AED','#E07B43','#EC4899'];
  const FIELDPACK = {
    'الرسم':{
      online:44,
      chans:['# عام','# أعمالكم','# نقد-وتطوير','# أدوات-وخامات','# تحدي-الأسبوع'],
      chat:[
        {n:'نورة ع.',t:'خلصت تحدي الأسبوع 🎨 أول تجربة لي مع الألوان المائية Wet-on-Wet والنتيجة فاجأتني!'},
        {n:'زياد م.',t:'أحد يعرف فرش Procreate قوية للبورتريه؟ أحس فرشي الحالية تطلع الجلد بلاستيك 😅'},
        {n:'ريم س.',t:'جرّب فرش Max Ulichney (MaxPacks) — غيّرت شغلي بالكامل، خصوصاً الـ Gouache 👌'},
        {mod:1,n:'أ. مشعل (مرشدك الفني)',t:'ملاحظة اليوم: أغلب أعمالكم قوية بالخط وضعيفة بالقيم الضوئية (Values). تمرين الأسبوع: نفس الرسمة بثلاث درجات رمادي فقط.'},
        {n:'سلمان ب.',t:'يوم 23 من الستريك 🔥 رسمة يومية مهما كانت بسيطة — الفرق واضح من أول أسبوعين'}
      ],
      tips:[
        'ارسم 5 اسكتشات سريعة (30 ثانية للواحد) قبل أي رسمة — تفكّ يدك وتقوّي ملاحظتك',
        'اقلب الصورة المرجعية رأساً على عقب وارسمها — تجبر عينك ترى الأشكال الحقيقية بدل الافتراضات',
        'ابدأ بالأشكال الأساسية (دائرة، مكعب، أسطوانة) قبل التفاصيل — هذا سر التناسب الصحيح'
      ],
      stars:[
        {n:'Devon Rodriguez',d:'بورتريه واقعي في مترو نيويورك',f:'TikTok · ‎+30M'},
        {n:'ZHC',d:'رسم وتحديات فنية ضخمة',f:'YouTube · ‎+25M'},
        {n:'مصطفى سعدي',d:'تعليم الرسم بالعربي خطوة بخطوة',f:'YouTube · ‎+7M'}
      ]
    },
    'الشطرنج':{
      online:31,
      chans:['# عام','# تحليل-مباريات','# ألغاز-اليوم','# بحث-عن-خصم','# بطولات'],
      chat:[
        {n:'فهد ر.',t:'وصلت 1400 تصنيف اليوم على Chess.com 🔥 الألغاز اليومية فرقت معي أكثر من أي شي'},
        {n:'سارة ن.',t:'سؤال: متى أبادل الفيل بالحصان؟ دايم أتردد وأخسر التمبو ⏱️'},
        {n:'عمر ح.',t:'قاعدة عامة: بالمراكز المفتوحة الفيل أقوى، وبالمغلقة الحصان يتفوق ♞ بس حلل كل مركز بحاله'},
        {mod:1,n:'م. حاتم (مدرّبك)',t:'لغز اليوم منشور في # ألغاز-اليوم — أبيض يلعب ويكسب قطعة بثلاث نقلات. أول 5 حلول صحيحة لهم نقاط بالصدارة 🏆'},
        {n:'يزيد ق.',t:'أحد فاضي لمباراة رابيد 15|10؟ تصنيفي 1250 وأبي أجرب افتتاحية لندن'}
      ],
      tips:[
        'حلّ 10 ألغاز تكتيكية يومياً — أسرع طريقة مثبتة لرفع تصنيفك تحت 1800',
        'بأول 10 نقلات: سيطر على المركز وطوّر قطعك وبيّت ملكك — قبل أي هجوم',
        'راجع كل خسارة 5 دقائق فقط وحدّد النقلة اللي انقلبت فيها المباراة — خسارة محلّلة = درس مجاني'
      ],
      stars:[
        {n:'GothamChess',d:'ليفي روزمان — أمتع شروحات الشطرنج',f:'YouTube · ‎+6M'},
        {n:'Magnus Carlsen',d:'بطل العالم السابق وأعلى تصنيف تاريخياً',f:'ملايين المتابعين'},
        {n:'Hikaru Nakamura',d:'أسطورة البليتز والبث المباشر',f:'YouTube+Twitch · ‎+5M'}
      ]
    },
    'الرياضة':{
      online:58,
      chans:['# عام','# تمارين-اليوم','# مقاطع-أداء','# تغذية-ولياقة','# فعاليات'],
      chat:[
        {n:'سلطان ق.',t:'نزلت مقطع تسديداتي في # مقاطع-أداء — أبي رأيكم بوضعية القدم الثابتة ⚽'},
        {n:'ريان د.',t:'شفته 👀 التسديد قوي بس جسمك يميل ورا — خل صدرك فوق الكرة تنزل التسديدة'},
        {mod:1,n:'كابتن بدر (مدرّبك)',t:'ريان قالها صح 👏 سلطان: أضفت لخطتك تمرين التصويب من لمسة واحدة — 3 جولات × 10 تسديدات، وصوّر الأخيرة'},
        {n:'لينا م.',t:'يوم 31 من الستريك 🏊 حسّيت زمن الـ 50 متر نزل ثانيتين هالشهر'},
        {n:'ناصر ع.',t:'أحد جرب تمارين البلايومتركس للانطلاقة؟ سمعت إنها ترفع السرعة بشكل ملحوظ'}
      ],
      tips:[
        'تمرّن على المهارة أول التمرين وأنت «طازج» — واترك اللياقة للنهاية، الدماغ يتعلم أفضل قبل التعب',
        'صوّر أداءك مرة بالأسبوع وقارنه بالشهر الماضي — الكاميرا تشوف اللي ما تحسّه',
        'النوم 8 ساعات جزء من التمرين مو راحة منه — فيه يثبت جسمك المهارة ويبني العضلة'
      ],
      stars:[
        {n:'IShowSpeed',d:'كرة قدم وترفيه — ظاهرة عالمية',f:'YouTube · ‎+35M'},
        {n:'Celine Dept',d:'تحديات كرة قدم مع النجوم',f:'TikTok · ‎+30M'},
        {n:'Chris Heria',d:'لياقة وكاليسثينكس من الصفر',f:'YouTube · ‎+6M'}
      ]
    },
    'الرياضات الإلكترونية':{
      online:73,
      chans:['# عام','# تشكيل-فرق','# كليبات','# تحليل-جيمبلاي','# بطولات'],
      chat:[
        {n:'فيصل د.',t:'رفعت كليب كلتش 1v3 في # كليبات 🎯 وصلت Diamond أخيراً بعد شهرين قريند'},
        {n:'نواف ش.',t:'مبروك 🔥 وش سيتنقس الحساسية عندك؟ أحس إيمي يهتز بالمواجهات'},
        {mod:1,n:'كوتش طلال «TLL»',t:'نواف: انزل DPI وارفع تركيزك على الكروس-هير بليسمنت — 15 دقيقة Aim Lab قبل الرانك، أسبوع وتشوف الفرق'},
        {n:'مشعل ت.',t:'نبي خامس لفريق البطولة الشهرية، رانك Plat فما فوق — الرول: كنترولر 🛡️'},
        {n:'جود س.',t:'راجعت ريبلاي خساراتي أمس زي ما قال الكوتش… طلعت أموت بنفس الزاوية كل مرة 😅 درس مجاني'}
      ],
      tips:[
        'راجع ريبلاي خسائرك مو انتصاراتك — أخطاؤك المتكررة هي منجم تطورك',
        '15 دقيقة تمارين Aim/ميكانيكس قبل الرانكد ترفع مستوى جلستك كاملة',
        '3 مباريات بتركيز كامل أفضل من 10 وأنت مشتت — الجودة تبني الذاكرة العضلية، مو الكمية'
      ],
      stars:[
        {n:'أبو فلة AboFlah',d:'أكبر صانع محتوى قيمنق عربي',f:'YouTube · ‎+30M'},
        {n:'بندريتا BanderitaX',d:'قيمنق سعودي — من روّاد المجال',f:'YouTube · ‎+10M'},
        {n:'شونق ShoNgxBoNg',d:'قيمنق وترفيه',f:'YouTube · ‎+7M'}
      ]
    },
    'ريادة الأعمال':{
      online:39,
      chans:['# عام','# اعرض-فكرتك','# تسويق-ومبيعات','# ابحث-عن-شريك','# فرص-وتمويل'],
      chat:[
        {n:'لمى ز.',t:'وصلت أول 100 عميل لمتجري 🎉 السر؟ كلمت 20 عميل بنفسي وسألتهم ليش اشتروا وليش شبه يتركون'},
        {n:'عبدالله غ.',t:'ما شاء الله 👏 كيف تسوّقين؟ إعلانات مدفوعة ولا Organic؟'},
        {n:'لمى ز.',t:'أول 50: محتوى تيك توك مجاني. بعدها جربت إعلانات بميزانية صغيرة والـ ROAS طلع 3.2'},
        {mod:1,n:'أ. سلمان (مرشدك الريادي)',t:'درس الأسبوع من قصة لمى: العميل الأول يجي بالكلام المباشر مو بالإعلان. تحديكم: 5 محادثات مع عملاء محتملين قبل الخميس — وانشروا الخلاصة هنا'},
        {n:'تركي ف.',t:'أدور شريك تقني لفكرة SaaS بقطاع اللوجستيات — عندي Validation مبدئي و3 عملاء مهتمين. التفاصيل في # ابحث-عن-شريك'}
      ],
      tips:[
        'كلّم 5 عملاء محتملين قبل ما تبني أي شيء — السوق يوجّهك أفضل من خيالك',
        'جهّز عرض 30 ثانية لفكرتك (Elevator Pitch) واحفظه — الفرص ما تستأذن قبل ما تمر',
        'ابدأ بنسخة يدوية من خدمتك وبِعها اليوم — أول ريال ربح يعلّمك أكثر من 100 كتاب'
      ],
      stars:[
        {n:'Gary Vee',d:'ريادة وتسويق — غاري فاينرتشوك',f:'المنصات مجتمعة · ‎+30M'},
        {n:'Alex Hormozi',d:'نمو الأعمال والمبيعات بلا حشو',f:'YouTube · ‎+3M'},
        {n:'Ali Abdaal',d:'بناء المشاريع والإنتاجية',f:'YouTube · ‎+6M'}
      ]
    },
    'الكتابة':{
      online:27,
      chans:['# عام','# نصوصكم','# نقد-أدبي','# تحدي-الكتابة','# فرص-نشر'],
      chat:[
        {n:'جود س.',t:'خلصت الفصل الثالث من روايتي 📚 60 يوم كتابة متواصلة — قاعدة الـ 200 كلمة اليومية صادقة'},
        {n:'مازن ح.',t:'نشرت قصيدة جديدة في # نصوصكم — جربت البحر الكامل أول مرة، أبي رأيكم بالقافية 🪶'},
        {mod:1,n:'أ. وضحى (محرّرتك)',t:'مازن: الصور الشعرية قوية 👏 عندك كسر بالبيت الخامس — راجع تفعيلة «متفاعلن» الثانية. جود: أرسلي الفصل وأرجعه لك بملاحظات التحرير خلال يومين'},
        {n:'أفنان ر.',t:'تحدي الأسبوع: قصة قصيرة كاملة في 500 كلمة بالضبط ✍️ مين معي؟'},
        {n:'خالد ب.',t:'فرصة: مجلة أدبية تستقبل قصص الشباب حتى نهاية الشهر — الرابط في # فرص-نشر'}
      ],
      tips:[
        'اكتب 200 كلمة يومياً بنفس الوقت — الاستمرارية تغلب الإلهام، والعادة تصنع الكاتب',
        'اقرأ نصك بصوت عالٍ قبل النشر — أذنك تكشف الركاكة اللي تفوتها عينك',
        'أنشئ «بنك أفكار» في جوالك — سجّل كل خاطرة لحظتها، أفكار منتصف الليل ما ترجع'
      ],
      stars:[
        {n:'أسامة المسلم',d:'الروائي الأكثر مبيعاً عربياً',f:'ملايين القرّاء والمتابعين'},
        {n:'أثير عبدالله النشمي',d:'روائية سعودية بأعمال الأكثر مبيعاً',f:'Instagram · ملايين'},
        {n:'Brandon Sanderson',d:'محاضرات مجانية في بناء الرواية',f:'YouTube · ‎+1M'}
      ]
    },
    'الخط':{
      online:19,
      chans:['# عام','# مشقكم','# نقد-وتصحيح','# أدوات-وأحبار','# معارض'],
      chat:[
        {n:'عمر ر.',t:'نزلت مشق اليوم في # مشقكم — «الرحمن علم القرآن» بالثلث 🕌 حاولت أضبط تشابك الألف واللام'},
        {n:'هاجر ف.',t:'ما شاء الله التكوين جميل! عندي سؤال: وش أفضل قصبة للديواني، والحبر ينشف عندي بسرعة'},
        {mod:1,n:'الخطّاط إبراهيم (أستاذك)',t:'عمر: النسبة ممتازة، انتبه لعرض القلم في رأس الألف — يجب يكون نقطتين كاملة. هاجر: قصبة جاوية متوسطة، وأضيفي قطرات ماء ورد للحبر يبقى رطباً'},
        {n:'نايف س.',t:'يوم 40 من مشق حرف الواو 🖋️ صدق أستاذنا: الإتقان حرفاً حرفاً مو صفحة صفحة'},
        {n:'شهد ع.',t:'معرض الخط العربي بالرياض فتح التسجيل لركن المواهب الشابة — التفاصيل في # معارض'}
      ],
      tips:[
        'تمرّن على حرف واحد 15 دقيقة حتى يثبت — الإتقان حرفاً حرفاً، مو صفحة صفحة',
        'تتبّع مشق الخطاطين الكبار بورق شفاف — هكذا تعلّم أساتذة الخط عبر القرون',
        'ثبّت زاوية القلم ولا تديرها مع الحرف — الزاوية الثابتة سر انتظام خطك'
      ],
      stars:[
        {n:'Seb Lester',d:'كاليغرافي عالمي — يحاكي الشعارات يدوياً',f:'Instagram · ‎+2M'},
        {n:'عثمان طه',d:'خطّاط مصحف المدينة النبوية',f:'أشهر خطاط معاصر'},
        {n:'وسام شوكت',d:'خطاط عربي بأسلوب معاصر عالمي',f:'أعمال في متاحف عالمية'}
      ]
    },
    'الصوت':{
      online:22,
      chans:['# عام','# تسجيلاتكم','# تقييم-الأداء','# تمارين-تنفس','# فرص-تسجيل'],
      chat:[
        {n:'يوسف م.',t:'رفعت تلاوة جديدة بمقام النهاوند في # تسجيلاتكم 📿 اشتغلت على القرار والجواب أسبوعين'},
        {n:'ندى ق.',t:'صوتك ثابت ما شاء الله! أنا أتدرب على الإلقاء — أحس نفَسي ينقطع بالجمل الطويلة 🎙️'},
        {mod:1,n:'أ. ماجد (مدرّب صوتك)',t:'ندى: هذي مشكلة تنفس صدري — تمرين اليوم في # تمارين-تنفس: شهيق 4 ثواني من البطن، حبس 4، زفير 8 على حرف «س». أسبوعين وتقرين فقرة كاملة بنفَس واحد'},
        {n:'راكان ع.',t:'سجلت أول تعليق صوتي تجريبي لإعلان 🎧 استخدمت مايك الجوال مع لحاف فوق راسي كعازل 😅 والنتيجة نظيفة'},
        {n:'أريج س.',t:'فرصة: بودكاست محلي يدور أصوات شابة لقراءة المقدمات — التفاصيل في # فرص-تسجيل'}
      ],
      tips:[
        '5 دقائق تنفس حجابي (من البطن) يومياً — أساس ثبات الصوت وقوته',
        'سجّل صوتك واسمعه يومياً — ما راح تطوّر صوتاً ما تعرفه',
        'اقرأ صفحة بصوت عالٍ يومياً بسرعات مختلفة — تبني تحكماً كاملاً بمخارجك ونبرتك'
      ],
      stars:[
        {n:'مشاري العفاسي',d:'تلاوة وإنشاد — الأشهر عربياً',f:'YouTube · ‎+12M'},
        {n:'إسلام صبحي',d:'تلاوات هزّت تيك توك',f:'TikTok+YouTube · ملايين'},
        {n:'ياسر الدوسري',d:'إمام الحرم المكي',f:'ملايين المتابعين'}
      ]
    }
  };
  const FIELDPACK_DEFAULT = {
    online:18,
    chans:['# عام','# شاركنا-تقدمك','# اسأل-مرشدك','# فعاليات'],
    chat:[
      {n:'سارة م.',t:'أول يوم لي هنا — متحمسة أبدأ رحلتي 🌟'},
      {mod:1,n:'مرشد المجتمع',t:'حياك الله! ابدئي بخطة الأسبوع الأول من مرشدك، وشاركينا أول توثيق لك هنا 👏'},
      {n:'فهد ع.',t:'يوم 12 من الستريك 🔥 الالتزام اليومي أسهل مما توقعت مع المجتمع'}
    ],
    tips:[
      'ابدأ بـ 15 دقيقة يومياً فقط — الاستمرارية الصغيرة تغلب الحماس الكبير المتقطع',
      'وثّق تقدمك من اليوم الأول — بعد شهر بتنصدم من الفرق',
      'شارك أعمالك بالمجتمع مبكراً — النقد البنّاء يختصر عليك شهوراً'
    ],
    stars:[]
  };

  /* فتح مجتمع → عرض التفرّعات */
  function openCommunity(name, emoji){
    window.curCommunity = name;
    var cfg = MENTOR[name] || MENTOR['أكاديمي'];
    document.getElementById('cb-ic').textContent = emoji;
    document.getElementById('cb-title').textContent = 'مجتمع: ' + name;
    document.getElementById('cb-sub').innerHTML = 'اختر تخصصك داخل ' + name + ' · <span style="color:#7FE0D3">انضم لمن يطوّرون موهبتهم الآن</span>';
    document.getElementById('branchNote').innerHTML = '<span style="font-size:17px">🧭</span> كل تخصص له مجتمعه الخاص و' + cfg.m + ' المختص. اختر تخصصك لتبدأ بخطة مخصّصة.';
    var grid = document.getElementById('branchGrid'); grid.innerHTML = '';
    (BRANCHES[name] || []).forEach(function(b){
      var btn = document.createElement('button'); btn.className = 'cat';
      btn.innerHTML = '<div class="ce">'+b.e+'</div><b>'+b.n+'</b><small>'+b.meta+'</small>';
      btn.addEventListener('click', function(){ openBranch(name, b.n, b.e); });
      grid.appendChild(btn);
    });
    show('community-branches', null);
  }

  function initials(name){ return name.trim().split(/\s+/).slice(0,2).map(function(w){return w.charAt(0);}).join(''); }

  /* فتح تخصّص → صفحة المجتمع بنمط ديسكورد، بمحتوى خاص بالمجال */
  function openBranch(community, branch, emoji){
    var cfg = MENTOR[community] || MENTOR['أكاديمي'];
    var pack = FIELDPACK[community] || FIELDPACK_DEFAULT;
    window.curCommunity = community;

    document.getElementById('tc-title').textContent = 'مجتمع: ' + branch;
    document.getElementById('tc-ic').textContent = emoji;
    document.getElementById('tc-sub').innerHTML = community + ' · ' + branch + ' · <span style="color:#7FE0D3">' + pack.online + ' متّصل الآن</span>';
    document.getElementById('tcOnline').textContent = pack.online;

    // القنوات
    var ch = document.getElementById('tcChans'); ch.innerHTML='';
    pack.chans.forEach(function(c,i){
      var b=document.createElement('button'); b.className='chan'+(i===0?' on':''); b.textContent=c;
      b.addEventListener('click',function(){ document.querySelectorAll('#tcChans .chan').forEach(x=>x.classList.remove('on')); b.classList.add('on'); });
      ch.appendChild(b);
    });

    // الشات الحي الخاص بالمجال
    var body = document.getElementById('tcChat'); body.innerHTML='';
    pack.chat.forEach(function(m,i){
      var div=document.createElement('div'); div.className='msg';
      var col = m.mod ? '#2FB39A' : AV_COLORS[i % AV_COLORS.length];
      var badge = m.mod ? ' <span class="modbadge">🛡️ مرشد</span>' : '';
      div.innerHTML = '<span class="av" style="background:'+col+'">'+initials(m.n)+'</span>'+
        '<div class="bub"><div class="nm">'+m.n+badge+'</div><div class="tx"></div></div>';
      div.querySelector('.tx').textContent = m.t;
      body.appendChild(div);
    });
    setTimeout(function(){ body.scrollTop = body.scrollHeight; }, 50);

    // النصائح الذكية
    var tips = document.getElementById('tcTips'); tips.innerHTML='';
    pack.tips.forEach(function(t,i){
      var d=document.createElement('div'); d.className='tip';
      d.innerHTML='<span class="tn2">'+(i+1)+'</span><span></span>';
      d.querySelector('span:last-child').textContent=t;
      tips.appendChild(d);
    });

    // نجوم المجال
    var stars = document.getElementById('tcStars'); stars.innerHTML='';
    if(pack.stars.length){
      pack.stars.forEach(function(st,i){
        var d=document.createElement('div'); d.className='star';
        d.innerHTML='<span class="sa" style="background:'+AV_COLORS[(i+2)%AV_COLORS.length]+'">'+initials(st.n)+'</span>'+
          '<span class="sm2"><b>'+st.n+'</b><small>'+st.d+'</small></span>'+
          '<span class="fw">'+st.f+'</span>';
        stars.appendChild(d);
      });
    } else {
      stars.innerHTML='<div style="color:var(--muted);font-size:13px;padding:8px 0">قريباً — نرشّح لك نجوم هذا المجال.</div>';
    }

    // المرشد والخطة
    document.getElementById('tc-h').textContent = cfg.plan;
    document.getElementById('tc-plan-sub').textContent = cfg.planSub;
    document.getElementById('tc-mentor-h').textContent = cfg.m + ' في هذا التخصص';
    document.getElementById('tc-mentor-name').textContent = cfg.n;
    document.getElementById('tc-mentor-role').textContent = cfg.mr;
    document.getElementById('tc-mentor-av').textContent = cfg.n.replace(/^(أ\.|م\.|كابتن|كوتش|الخطّاط)\s*/,'').charAt(0);

    show('talent-community', null);
  }

  /* شات مجتمع التخصص */
  function sendTcMsg(){
    var inp=document.getElementById('tcInput'); var v=inp.value.trim(); if(!v)return;
    var body=document.getElementById('tcChat');
    var m=document.createElement('div'); m.className='msg me';
    m.innerHTML='<span class="av" style="background:linear-gradient(135deg,#14B8A6,#0F4C46)">أنا</span><div class="bub"><div class="tx"></div></div>';
    m.querySelector('.tx').textContent=v;
    body.appendChild(m); inp.value=''; body.scrollTop=body.scrollHeight;
  }

  /* تبويبات صفحة المجتمعات */
  function commTab(t){
    ['comm','gchat','board','infl','scouts'].forEach(function(x){
      var tab=document.getElementById('ct-'+x), pane=document.getElementById('cp-'+x);
      if(tab) tab.classList.toggle('on', x===t);
      if(pane) pane.classList.toggle('on', x===t);
    });
    if(t==='board') renderBoard(boardFilter);
    if(t==='gchat'){ var b=document.getElementById('gchatBody'); if(b) b.scrollTop=b.scrollHeight; }
  }

  /* الشات العام */
  function sendGMsg(){
    var inp=document.getElementById('gchatInput'); var v=inp.value.trim(); if(!v)return;
    var body=document.getElementById('gchatBody');
    var m=document.createElement('div'); m.className='msg me';
    m.innerHTML='<span class="av" style="background:linear-gradient(135deg,#14B8A6,#0F4C46)">أنا</span><div class="bub"><div class="tx"></div></div>';
    m.querySelector('.tx').textContent=v;
    body.appendChild(m); inp.value=''; body.scrollTop=body.scrollHeight;
  }

  /* قائمة الصدارة — أطول ستريك بكل مجال (أمثلة توضيحية) */
  function catLabel(c){
    var map={'رياضة':'الرياضة','esports':'eSports','ريادة':'ريادة الأعمال','كتابة':'الكتابة','رسم':'الرسم','خط':'الخط','صوت':'الصوت','شطرنج':'الشطرنج','أكاديمي':'أكاديمي'};
    return map[c]||c;
  }
  const LB_DATA=[
    {n:'محمد الأحمدي', f:'تفاضل وتكامل', cat:'أكاديمي', s:401, c:'#0F4C46'},
    {n:'سلطان القحطاني', f:'كرة القدم',   cat:'رياضة',   s:388, c:'#2FB39A'},
    {n:'دانة المالكي', f:'الرسم الرقمي',  cat:'رسم',     s:376, c:'#EC4899'},
    {n:'حسام العمري',  f:'التكتيكات',     cat:'شطرنج',   s:359, c:'#7C3AED'},
    {n:'فيصل العتيبي', f:'EA FC',          cat:'esports', s:347, c:'#8B5CF6'},
    {n:'يوسف المطيري', f:'تلاوة القرآن',   cat:'صوت',     s:334, c:'#0EA5A0'},
    {n:'لمى الزهراني', f:'التسويق الرقمي', cat:'ريادة',   s:312, c:'#F4A261'},
    {n:'عمر الراشد',   f:'خط الثلث',       cat:'خط',      s:298, c:'#0B342F'},
    {n:'جود السبيعي',  f:'الرواية',        cat:'كتابة',   s:289, c:'#14B8A6'},
    {n:'ريان الدوسري', f:'كرة السلة',      cat:'رياضة',   s:256, c:'#2FB39A'},
    {n:'أريج الشهراني',f:'البليتز',        cat:'شطرنج',   s:243, c:'#5B7FE0'},
    {n:'تركي العنزي',  f:'الأنمي والمانجا',cat:'رسم',     s:221, c:'#F472B6'},
    {n:'سارة باوزير',  f:'فيزياء عامة',    cat:'أكاديمي', s:213, c:'#0F4C46'},
    {n:'نواف الشهري',  f:'Valorant',        cat:'esports', s:198, c:'#8B5CF6'},
    {n:'ندى القرني',   f:'الإلقاء',         cat:'صوت',     s:187, c:'#14B8A6'},
    {n:'عبدالله الغامدي',f:'المبيعات',       cat:'ريادة',  s:174, c:'#E07B43'},
    {n:'هاجر الفيفي',  f:'الخط الديواني',  cat:'خط',      s:167, c:'#0EA5A0'},
    {n:'مازن الحربي',  f:'الشعر',          cat:'كتابة',   s:143, c:'#14B8A6'}
  ];
  let boardFilter='all';
  function renderBoard(filter){
    boardFilter=filter;
    document.querySelectorAll('.fpills .fp').forEach(function(p){ p.classList.toggle('on', p.getAttribute('data-f')===filter); });
    var list=LB_DATA.filter(function(x){ return filter==='all' || x.cat===filter; });
    list.sort(function(a,b){ return b.s-a.s; });
    var box=document.getElementById('lbList'); box.innerHTML='';
    if(!list.length){ box.innerHTML='<div style="text-align:center;color:var(--muted);padding:26px 12px;font-size:13.5px">لا توجد بيانات لهذا المجال بعد — كن أول من يبدأ ستريك هنا 🔥</div>'; return; }
    list.forEach(function(x,i){
      var rank=i+1; var topClass = rank<=3 ? ' top'+rank : '';
      var row=document.createElement('div'); row.className='row'+topClass;
      row.innerHTML =
        '<span class="rk">'+rank+'</span>'+
        '<span style="width:36px;height:36px;border-radius:50%;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-family:Tajawal;font-weight:700;color:#fff;font-size:13px;background:'+x.c+'">'+initials(x.n)+'</span>'+
        '<span class="nm"><b>'+x.n+'</b><small>'+x.f+' · '+catLabel(x.cat)+'</small></span>'+
        '<span class="stk">🔥 '+x.s+'</span>';
      box.appendChild(row);
    });
  }

  /* نجوم حقيقيون بملايين المتابعين — لكل مجال (أرقام تقريبية) */
  const INF=[
    {n:'IShowSpeed',        f:'كرة قدم وترفيه · الرياضة',        h:['YouTube · ‎+35M'],            c:'#2FB39A'},
    {n:'Celine Dept',       f:'تحديات كرة قدم · الرياضة',        h:['TikTok · ‎+30M'],             c:'#0EA5A0'},
    {n:'Chris Heria',       f:'لياقة وكاليسثينكس · الرياضة',     h:['YouTube · ‎+6M'],             c:'#14B8A6'},
    {n:'أبو فلة AboFlah',   f:'قيمنق وتحديات · eSports',         h:['YouTube · ‎+30M'],            c:'#7C3AED'},
    {n:'بندريتا BanderitaX',f:'قيمنق سعودي · eSports',           h:['YouTube · ‎+10M'],            c:'#8B5CF6'},
    {n:'Gary Vee',          f:'ريادة وتسويق · ريادة الأعمال',    h:['المنصات مجتمعة · ‎+30M'],     c:'#F4A261'},
    {n:'Alex Hormozi',      f:'نمو الأعمال · ريادة الأعمال',     h:['YouTube · ‎+3M'],             c:'#E07B43'},
    {n:'Ali Abdaal',        f:'إنتاجية ومشاريع · ريادة الأعمال', h:['YouTube · ‎+6M'],             c:'#D97706'},
    {n:'أسامة المسلم',      f:'رواية · الكتابة',                 h:['الأكثر مبيعاً عربياً · ملايين'],c:'#0F4C46'},
    {n:'أثير عبدالله النشمي',f:'رواية · الكتابة',                h:['Instagram · ملايين'],          c:'#14B8A6'},
    {n:'Devon Rodriguez',   f:'بورتريه واقعي · الرسم',           h:['TikTok · ‎+30M'],             c:'#EC4899'},
    {n:'ZHC',               f:'رسم وتحديات · الرسم',             h:['YouTube · ‎+25M'],            c:'#F472B6'},
    {n:'مصطفى سعدي',        f:'تعليم الرسم بالعربي · الرسم',     h:['YouTube · ‎+7M'],             c:'#DB2777'},
    {n:'Seb Lester',        f:'كاليغرافي · الخط',                h:['Instagram · ‎+2M'],           c:'#0B342F'},
    {n:'عثمان طه',          f:'خطّاط مصحف المدينة · الخط',       h:['أشهر خطاط معاصر'],            c:'#0EA5A0'},
    {n:'مشاري العفاسي',     f:'تلاوة وإنشاد · الصوت',            h:['YouTube · ‎+12M'],            c:'#2FB39A'},
    {n:'إسلام صبحي',        f:'تلاوات · الصوت',                  h:['TikTok+YouTube · ملايين'],    c:'#14B8A6'},
    {n:'GothamChess',       f:'شروحات · الشطرنج',               h:['YouTube · ‎+6M'],             c:'#7C3AED'},
    {n:'Magnus Carlsen',    f:'بطل العالم السابق · الشطرنج',     h:['ملايين المتابعين'],           c:'#5B7FE0'},
    {n:'Hikaru Nakamura',   f:'بليتز وبث مباشر · الشطرنج',      h:['YouTube+Twitch · ‎+5M'],      c:'#8B5CF6'}
  ];
  function renderInfluencers(){
    var box=document.getElementById('infGrid'); box.innerHTML='';
    INF.forEach(function(p){
      var hd=p.h.map(function(x){return '<span>'+x+'</span>';}).join('');
      var c=document.createElement('div'); c.className='inf';
      c.innerHTML='<div class="ia" style="background:'+p.c+'">'+initials(p.n)+'</div>'+
        '<div class="im"><b>'+p.n+'</b><span class="fld">'+p.f+'</span><div class="hd">'+hd+'</div></div>';
      box.appendChild(c);
    });
  }

  /* فتح مجتمع دراسي مدفوع */
  let pendingSubject=null;
  function openStudyUnlock(name, code, emoji){
    pendingSubject={name:name, code:code, emoji:emoji};
    document.getElementById('studyName').textContent=name;
    document.getElementById('studyModal').classList.add('show');
  }
  function closeStudy(){ document.getElementById('studyModal').classList.remove('show'); }
  function confirmStudy(){
    closeStudy();
    if(pendingSubject) openSubject(pendingSubject.name, pendingSubject.code, pendingSubject.emoji);
    pendingSubject=null;
  }

  /* تهيئة */
  renderInfluencers();
  renderBoard('all');
</script>
</body>
</html>
