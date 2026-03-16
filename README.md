<!DOCTYPE html>
<html lang="en" data-theme="light">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Musaddilal Jewellers Pvt. Ltd. — Crafted Since 1952</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400;1,600&family=Jost:wght@300;400;500&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
:root{
  --gold:#C9A84C;--gold2:#E8C97A;--gold3:#8B6914;
  --gold-glow:rgba(201,168,76,0.14);
  --bg:#FAF7F2;--bg2:#F2EDE4;--bg3:#EAE3D6;--bg4:#DDD5C3;
  --text:#1A1410;--text2:#5C4A2A;--text3:#9C8660;--text4:#C0AA88;
  --border:rgba(201,168,76,0.18);--shadow:rgba(0,0,0,0.07);--shadow2:rgba(0,0,0,0.14);
  --card-r:16px;--tr:0.42s cubic-bezier(.25,.46,.45,.94);
}
[data-theme="dark"]{
  --bg:#0C0A08;--bg2:#161410;--bg3:#201C15;--bg4:#2A2419;
  --text:#F5EDD8;--text2:#D4B47A;--text3:#8A7050;--text4:#5A4830;
  --border:rgba(201,168,76,0.13);--shadow:rgba(0,0,0,0.5);--shadow2:rgba(0,0,0,0.72);
}
body{font-family:'Jost',sans-serif;background:var(--bg);color:var(--text);transition:background var(--tr),color var(--tr);overflow-x:hidden}
::-webkit-scrollbar{width:5px}::-webkit-scrollbar-track{background:var(--bg2)}::-webkit-scrollbar-thumb{background:var(--gold3);border-radius:3px}
.page-wrap{max-width:1160px;margin:0 auto;padding:0 52px}

/* CURSOR */
.cursor{width:9px;height:9px;background:var(--gold);border-radius:50%;position:fixed;pointer-events:none;z-index:9999;transform:translate(-50%,-50%);transition:width .3s,height .3s;mix-blend-mode:difference}
.cursor-ring{width:34px;height:34px;border:1.5px solid var(--gold);border-radius:50%;position:fixed;pointer-events:none;z-index:9998;transform:translate(-50%,-50%);opacity:.45;transition:width .3s,height .3s}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:500;background:rgba(250,247,242,.92);backdrop-filter:blur(22px);border-bottom:1px solid var(--border);transition:background var(--tr)}
[data-theme="dark"] nav{background:rgba(12,10,8,.92)}
.nav-topbar{background:var(--gold);color:#1A1410;text-align:center;padding:6px;font-size:11px;letter-spacing:.18em;text-transform:uppercase;font-weight:500}
.nav-inner{max-width:1160px;margin:0 auto;padding:0 52px;display:grid;grid-template-columns:1fr auto 1fr;align-items:center;height:66px;gap:12px}
.nav-left{display:flex;gap:24px;align-items:center}
.nav-left a{font-size:12px;letter-spacing:.12em;text-transform:uppercase;color:var(--text2);text-decoration:none;transition:color .3s;font-weight:400;position:relative}
.nav-left a::after{content:'';position:absolute;bottom:-3px;left:0;right:0;height:1px;background:var(--gold);transform:scaleX(0);transition:transform .3s;transform-origin:left}
.nav-left a:hover{color:var(--gold)}
.nav-left a:hover::after{transform:scaleX(1)}
.nav-logo{text-align:center;text-decoration:none;display:block}
.nav-logo-main{font-family:'Cormorant Garamond',serif;font-size:21px;font-weight:600;color:var(--gold);letter-spacing:.05em;line-height:1.1;display:block}
.nav-logo-sub{font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--text3);font-family:'Jost',sans-serif;font-weight:300;display:block;margin-top:2px}
.nav-right{display:flex;gap:12px;align-items:center;justify-content:flex-end}
.icon-btn{width:38px;height:38px;border-radius:9px;border:1px solid var(--border);background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--text2);transition:all .3s;position:relative;text-decoration:none}
.icon-btn:hover{border-color:var(--gold);color:var(--gold);background:var(--gold-glow)}
.cart-badge{position:absolute;top:-5px;right:-5px;width:17px;height:17px;border-radius:50%;background:var(--gold);color:#1A1410;font-size:10px;font-weight:600;display:flex;align-items:center;justify-content:center}
/* 3-DOT */
.dot-wrap{position:relative}
.dot-btn{width:38px;height:38px;border-radius:9px;border:1px solid var(--border);background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;gap:3px;color:var(--text2);transition:all .3s}
.dot-btn:hover{border-color:var(--gold);color:var(--gold);background:var(--gold-glow)}
.dot-btn span{width:4px;height:4px;border-radius:50%;background:currentColor;display:block}
.dot-dd{position:absolute;top:calc(100% + 10px);right:0;background:var(--bg);border:1px solid var(--border);border-radius:14px;padding:8px;width:225px;box-shadow:0 16px 48px var(--shadow2);opacity:0;pointer-events:none;transform:translateY(8px);transition:opacity .3s,transform .3s;z-index:600}
.dot-dd.open{opacity:1;pointer-events:all;transform:translateY(0)}
.dd-item{display:flex;align-items:center;gap:12px;padding:11px 14px;border-radius:9px;font-size:13px;color:var(--text2);cursor:pointer;transition:all .3s;text-decoration:none;border:none;background:none;width:100%;font-family:'Jost',sans-serif}
.dd-item:hover{background:var(--gold-glow);color:var(--gold)}
.dd-ico{width:32px;height:32px;border-radius:8px;background:var(--bg3);display:flex;align-items:center;justify-content:center;flex-shrink:0;color:var(--gold);transition:background .3s}
.dd-item:hover .dd-ico{background:var(--gold-glow)}
.dd-sep{height:1px;background:var(--border);margin:6px 8px}
.theme-row{display:flex;align-items:center;justify-content:space-between;padding:10px 14px}
.theme-lbl{font-size:12px;color:var(--text3)}
.tog{width:44px;height:24px;border-radius:12px;border:1.5px solid var(--gold);background:transparent;cursor:pointer;position:relative;transition:background .3s;flex-shrink:0}
.tog::after{content:'';position:absolute;top:3px;left:3px;width:14px;height:14px;border-radius:50%;background:var(--gold);transition:transform .3s}
[data-theme="dark"] .tog::after{transform:translateX(20px)}

/* UTIL */
section{padding:80px 0}
.eyebrow{font-size:11px;letter-spacing:.4em;text-transform:uppercase;color:var(--gold);margin-bottom:13px;display:block}
.sec-title{font-family:'Cormorant Garamond',serif;font-size:44px;font-weight:300;line-height:1.15;color:var(--text);margin-bottom:14px}
.sec-title em{font-style:italic;color:var(--gold)}
.sec-sub{font-size:14px;line-height:1.85;color:var(--text3);max-width:520px}
.btn{display:inline-flex;align-items:center;gap:8px;padding:13px 30px;border-radius:7px;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:.18em;text-transform:uppercase;font-weight:500;cursor:pointer;text-decoration:none;transition:all .3s;border:none}
.btn-gold{background:var(--gold);color:#1A1410}
.btn-gold:hover{background:var(--gold2);transform:translateY(-2px);box-shadow:0 10px 28px rgba(201,168,76,.35)}
.btn-ghost{background:transparent;color:var(--gold);border:1.5px solid var(--gold)}
.btn-ghost:hover{background:rgba(201,168,76,.08);transform:translateY(-2px)}

/* HERO */
.hero{min-height:100vh;padding-top:110px;display:flex;align-items:center;position:relative;overflow:hidden}
.hero-orb{position:absolute;border-radius:50%;pointer-events:none}
.hero-orb:nth-child(1){width:650px;height:650px;top:-15%;right:-10%;background:radial-gradient(circle,rgba(201,168,76,.07) 0%,transparent 65%)}
.hero-orb:nth-child(2){width:480px;height:480px;bottom:-12%;left:-8%;background:radial-gradient(circle,rgba(201,168,76,.05) 0%,transparent 65%)}
.hero-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:center;width:100%}
.hero-tag{display:inline-flex;align-items:center;gap:8px;border:1px solid var(--border);border-radius:20px;padding:6px 16px;font-size:11px;letter-spacing:.25em;text-transform:uppercase;color:var(--gold);margin-bottom:26px;opacity:0;animation:fadeUp .9s .1s forwards}
.hero-tag::before{content:'✦';font-size:9px}
.hero-h1{font-family:'Cormorant Garamond',serif;font-size:62px;line-height:1.05;font-weight:300;color:var(--text);margin-bottom:22px;opacity:0;animation:fadeUp .9s .25s forwards}
.hero-h1 em{font-style:italic;color:var(--gold)}
.hero-desc{font-size:15px;line-height:1.85;color:var(--text3);max-width:400px;margin-bottom:38px;opacity:0;animation:fadeUp .9s .4s forwards}
.hero-btns{display:flex;gap:14px;flex-wrap:wrap;opacity:0;animation:fadeUp .9s .55s forwards}
.hero-stats{display:flex;gap:34px;margin-top:46px;opacity:0;animation:fadeUp .9s .7s forwards}
.stat-n{font-family:'Cormorant Garamond',serif;font-size:30px;font-weight:600;color:var(--gold);line-height:1}
.stat-l{font-size:11px;letter-spacing:.1em;color:var(--text3);margin-top:3px;text-transform:uppercase}
/* MOSAIC */
.hero-mosaic{display:grid;grid-template-columns:1.1fr .9fr;gap:13px;opacity:0;animation:fadeIn 1.2s .4s forwards}
.mos{border-radius:var(--card-r);overflow:hidden;position:relative;transition:transform .4s,box-shadow .4s}
.mos:hover{transform:scale(1.02);box-shadow:0 20px 50px var(--shadow2)}
.mos:nth-child(1){grid-row:span 2}
.mos img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .6s}
.mos:hover img{transform:scale(1.06)}
.mos:nth-child(1),.mos:nth-child(1) img{height:360px}
.mos:not(:nth-child(1)),.mos:not(:nth-child(1)) img{height:172px}
.mos-lbl{position:absolute;bottom:12px;left:12px;background:rgba(12,10,8,.72);backdrop-filter:blur(8px);color:#F5EDD8;padding:5px 12px;border-radius:5px;font-size:11px;letter-spacing:.08em}
.mos-badge{position:absolute;top:12px;right:12px;background:var(--gold);color:#1A1410;padding:4px 10px;border-radius:4px;font-size:10px;letter-spacing:.15em;text-transform:uppercase;font-weight:500}

/* MARQUEE */
.mq-wrap{padding:20px 0;border-top:1px solid var(--border);border-bottom:1px solid var(--border);background:var(--bg2);overflow:hidden;transition:background var(--tr)}
.mq-track{display:flex;white-space:nowrap;animation:marquee 26s linear infinite}
.mq-track:hover{animation-play-state:paused}
.mq-item{font-family:'Cormorant Garamond',serif;font-size:17px;font-style:italic;color:var(--text3);padding:0 34px;flex-shrink:0}
.mq-item span{color:var(--gold);margin:0 4px}

/* RECOMMENDED */
.rec-top{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:48px}
.view-all{font-size:12px;letter-spacing:.15em;text-transform:uppercase;color:var(--gold);text-decoration:none;display:flex;align-items:center;gap:6px;transition:gap .3s}
.view-all:hover{gap:10px}
.rec-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:20px}
.rec-card{background:var(--bg2);border-radius:var(--card-r);overflow:hidden;cursor:pointer;border:1px solid var(--border);transition:transform .4s,box-shadow .4s,background var(--tr)}
.rec-card:hover{transform:translateY(-6px);box-shadow:0 20px 56px var(--shadow2)}
.rec-img{height:200px;position:relative;overflow:hidden}
.rec-img img{width:100%;height:100%;object-fit:cover;transition:transform .6s}
.rec-card:hover .rec-img img{transform:scale(1.07)}
.rec-ov{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.38),transparent 55%);opacity:0;transition:opacity .3s}
.rec-card:hover .rec-ov{opacity:1}
.rec-tag{position:absolute;top:10px;left:10px;background:var(--gold);color:#1A1410;padding:3px 9px;border-radius:4px;font-size:10px;letter-spacing:.12em;text-transform:uppercase;font-weight:500}
.rec-add{position:absolute;bottom:12px;right:12px;width:36px;height:36px;border-radius:50%;background:var(--gold);border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;opacity:0;transform:translateY(8px);transition:all .3s}
.rec-card:hover .rec-add{opacity:1;transform:translateY(0)}
.rec-body{padding:16px 18px 18px}
.rec-name{font-family:'Cormorant Garamond',serif;font-size:19px;font-weight:400;color:var(--text);margin-bottom:3px}
.rec-sub{font-size:12px;color:var(--text3);margin-bottom:10px}
.rec-foot{display:flex;justify-content:space-between;align-items:center}
.rec-price{font-size:14px;color:var(--gold);font-weight:500}
.rec-stars{font-size:11px;color:var(--gold);letter-spacing:2px}

/* COLLECTIONS */
.coll-top{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:48px}
.coll-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.coll-card{background:var(--bg2);border-radius:var(--card-r);overflow:hidden;cursor:pointer;border:1px solid var(--border);transition:transform .4s,box-shadow .4s,background var(--tr)}
.coll-card:hover{transform:translateY(-6px);box-shadow:0 22px 60px var(--shadow2)}
.coll-img{height:230px;position:relative;overflow:hidden}
.coll-img img{width:100%;height:100%;object-fit:cover;transition:transform .6s}
.coll-card:hover .coll-img img{transform:scale(1.07)}
.coll-ov{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.38),transparent 55%);opacity:0;transition:opacity .3s}
.coll-card:hover .coll-ov{opacity:1}
.coll-tag{position:absolute;top:12px;right:12px;background:var(--gold);color:#1A1410;padding:4px 11px;border-radius:4px;font-size:10px;letter-spacing:.15em;text-transform:uppercase;font-weight:500}
.coll-body{padding:20px 22px}
.coll-name{font-family:'Cormorant Garamond',serif;font-size:22px;font-weight:400;color:var(--text);margin-bottom:3px}
.coll-sub{font-size:12px;color:var(--text3);margin-bottom:12px}
.coll-foot{display:flex;justify-content:space-between;align-items:center}
.coll-price{font-size:14px;color:var(--gold);font-weight:500}
.coll-arr{width:32px;height:32px;border-radius:50%;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--text3);font-size:15px;transition:all .3s;cursor:pointer;user-select:none}
.coll-card:hover .coll-arr{background:var(--gold);color:#1A1410;border-color:var(--gold)}

/* CUSTOM ORDER */
.custom-box{background:var(--bg2);border-radius:24px;padding:60px;position:relative;overflow:hidden;border:1px solid var(--border);transition:background var(--tr)}
.custom-box::before{content:'';position:absolute;top:-80px;right:-80px;width:360px;height:360px;border-radius:50%;background:radial-gradient(circle,rgba(201,168,76,.07),transparent 65%);pointer-events:none}
.custom-grid{display:grid;grid-template-columns:1fr 1.1fr;gap:60px;align-items:start;position:relative;z-index:1}
.proc-list{display:flex;flex-direction:column;gap:22px;margin-top:30px}
.proc-step{display:flex;gap:16px;align-items:flex-start}
.proc-num{width:38px;height:38px;border-radius:50%;border:1.5px solid var(--gold);flex-shrink:0;display:flex;align-items:center;justify-content:center;font-family:'Cormorant Garamond',serif;font-size:17px;color:var(--gold)}
.proc-h{font-size:14px;font-weight:500;color:var(--text);margin-bottom:3px}
.proc-p{font-size:13px;color:var(--text3);line-height:1.65}
.cform{display:flex;flex-direction:column;gap:14px}
.frow{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.fg{display:flex;flex-direction:column;gap:6px}
.fg label{font-size:10.5px;letter-spacing:.22em;text-transform:uppercase;color:var(--text3)}
.fg input,.fg select,.fg textarea{background:var(--bg);border:1px solid var(--border);border-radius:9px;padding:12px 16px;font-family:'Jost',sans-serif;font-size:14px;color:var(--text);outline:none;transition:border-color .3s,background var(--tr);width:100%}
.fg input::placeholder,.fg textarea::placeholder{color:var(--text4)}
.fg input:focus,.fg select:focus,.fg textarea:focus{border-color:var(--gold)}
.fg select{appearance:none;cursor:pointer;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='14' height='14' viewBox='0 0 24 24' fill='none' stroke='%239C8660' stroke-width='2'%3E%3Cpath d='M6 9l6 6 6-6'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 14px center;padding-right:40px}
.fg textarea{height:108px;resize:none;line-height:1.6}
.price-note{background:rgba(201,168,76,.07);border:1px solid rgba(201,168,76,.22);border-radius:10px;padding:14px 18px;font-size:13px;color:var(--text2);line-height:1.7}
.price-note strong{color:var(--gold)}
.wa-row{background:rgba(37,211,102,.07);border:1px solid rgba(37,211,102,.22);border-radius:10px;padding:12px 16px;display:flex;align-items:center;gap:12px;font-size:13px;color:var(--text2)}
.wa-ico{width:34px;height:34px;border-radius:50%;background:#25D366;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.wa-btn{display:inline-flex;align-items:center;gap:7px;background:#25D366;color:#fff;padding:9px 16px;border-radius:7px;font-size:11px;letter-spacing:.12em;text-transform:uppercase;text-decoration:none;font-weight:500;transition:all .3s;border:none;cursor:pointer;font-family:'Jost',sans-serif;margin-left:auto;flex-shrink:0}
.wa-btn:hover{background:#1EAD55;transform:translateY(-1px)}
.sub-btn{background:var(--gold);color:#1A1410;padding:15px;border-radius:9px;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:.2em;text-transform:uppercase;font-weight:500;border:none;cursor:pointer;transition:all .3s}
.sub-btn:hover{background:var(--gold2);transform:translateY(-2px);box-shadow:0 10px 24px rgba(201,168,76,.3)}

/* FEATURES */
.features-bg{background:var(--bg2);padding:50px 0;border-top:1px solid var(--border);border-bottom:1px solid var(--border);transition:background var(--tr)}
.feat-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:28px}
.feat{text-align:center}
.feat-icon{width:50px;height:50px;border-radius:50%;background:var(--gold-glow);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;margin:0 auto 13px;color:var(--gold)}
.feat-t{font-size:14px;font-weight:500;color:var(--text);margin-bottom:5px}
.feat-d{font-size:12px;color:var(--text3);line-height:1.65}

/* TESTIMONIALS */
.testi-hdr{text-align:center;margin-bottom:52px}
.testi-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.testi-card{background:var(--bg2);border-radius:var(--card-r);padding:28px;border:1px solid var(--border);transition:background var(--tr),transform .4s}
.testi-card:hover{transform:translateY(-4px)}
.stars{color:var(--gold);font-size:12px;letter-spacing:3px;margin-bottom:13px}
.testi-txt{font-family:'Cormorant Garamond',serif;font-size:17px;font-style:italic;line-height:1.75;color:var(--text);margin-bottom:18px}
.testi-auth{display:flex;align-items:center;gap:12px}
.auth-av{width:38px;height:38px;border-radius:50%;background:var(--gold-glow);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-family:'Cormorant Garamond',serif;font-size:15px;color:var(--gold);flex-shrink:0}
.auth-name{font-size:13px;font-weight:500;color:var(--text)}
.auth-loc{font-size:11px;color:var(--text3)}

/* ABOUT */
.about-bg{background:var(--bg2);padding:80px 0;border-top:1px solid var(--border);border-bottom:1px solid var(--border);transition:background var(--tr)}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:70px;align-items:center}
.about-img-wrap{position:relative}
.about-img{border-radius:var(--card-r);height:380px;overflow:hidden}
.about-img img{width:100%;height:100%;object-fit:cover}
.about-badge{position:absolute;bottom:-16px;right:-16px;background:var(--gold);color:#1A1410;padding:18px 20px;border-radius:14px;text-align:center;box-shadow:0 8px 28px rgba(201,168,76,.3)}
.about-badge-n{font-family:'Cormorant Garamond',serif;font-size:34px;font-weight:600;line-height:1}
.about-badge-t{font-size:10px;letter-spacing:.12em;text-transform:uppercase;margin-top:2px}
.cert-row{display:flex;flex-wrap:wrap;gap:9px;margin-top:26px}
.cert{border:1px solid var(--border);border-radius:6px;padding:7px 14px;font-size:11px;letter-spacing:.12em;text-transform:uppercase;color:var(--text3);display:flex;align-items:center;gap:6px}
.cert::before{content:'✦';color:var(--gold);font-size:9px}

/* CART */
.cart-ov{position:fixed;inset:0;background:rgba(0,0,0,.55);backdrop-filter:blur(4px);z-index:700;opacity:0;pointer-events:none;transition:opacity .35s}
.cart-ov.open{opacity:1;pointer-events:all}
.cart-panel{position:fixed;top:0;right:0;bottom:0;width:400px;background:var(--bg);z-index:701;transform:translateX(100%);transition:transform .4s cubic-bezier(.25,.46,.45,.94);display:flex;flex-direction:column;box-shadow:-20px 0 60px var(--shadow2)}
.cart-panel.open{transform:translateX(0)}
.cart-hdr{padding:22px 26px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center}
.cart-title{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:400;color:var(--text)}
.cart-cls{width:36px;height:36px;border-radius:8px;border:1px solid var(--border);background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--text3);transition:all .3s}
.cart-cls:hover{border-color:var(--gold);color:var(--gold)}
.cart-items{flex:1;overflow-y:auto;padding:18px 26px}
.cart-empty{text-align:center;padding:60px 0;color:var(--text3)}
.cart-empty svg{opacity:.25;margin-bottom:12px}
.cart-empty p{font-family:'Cormorant Garamond',serif;font-size:20px;font-style:italic;margin-bottom:6px}
.cart-empty span{font-size:13px}
.c-item{display:flex;gap:13px;align-items:flex-start;padding:15px 0;border-bottom:1px solid var(--border)}
.c-item-img{width:68px;height:68px;border-radius:10px;overflow:hidden;flex-shrink:0}
.c-item-img img{width:100%;height:100%;object-fit:cover}
.c-item-info{flex:1}
.c-item-name{font-size:14px;font-weight:500;color:var(--text);margin-bottom:3px}
.c-item-sub{font-size:12px;color:var(--text3);margin-bottom:7px}
.c-item-price{font-size:14px;color:var(--gold);font-weight:500}
.c-item-del{width:28px;height:28px;border-radius:6px;border:1px solid var(--border);background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--text4);transition:all .3s;flex-shrink:0}
.c-item-del:hover{border-color:#e24b4a;color:#e24b4a;background:rgba(226,75,74,.06)}
.cart-ftr{padding:18px 26px;border-top:1px solid var(--border)}
.cart-total-row{display:flex;justify-content:space-between;align-items:center;margin-bottom:14px}
.ct-lbl{font-size:12px;color:var(--text3);letter-spacing:.08em;text-transform:uppercase}
.ct-val{font-family:'Cormorant Garamond',serif;font-size:26px;color:var(--gold);font-weight:600}
.checkout-btn{width:100%;background:var(--gold);color:#1A1410;padding:14px;border-radius:9px;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:.2em;text-transform:uppercase;font-weight:500;border:none;cursor:pointer;transition:all .3s;margin-bottom:10px}
.checkout-btn:hover{background:var(--gold2);transform:translateY(-1px);box-shadow:0 8px 22px rgba(201,168,76,.3)}
.inv-dl-btn{width:100%;background:transparent;color:var(--gold);padding:11px;border-radius:9px;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:.15em;text-transform:uppercase;font-weight:500;border:1.5px solid var(--gold);cursor:pointer;transition:all .3s;display:flex;align-items:center;justify-content:center;gap:8px}
.inv-dl-btn:hover{background:var(--gold-glow)}

/* MODALS */
.mod-ov{position:fixed;inset:0;z-index:800;background:rgba(0,0,0,.65);backdrop-filter:blur(6px);display:flex;align-items:center;justify-content:center;opacity:0;pointer-events:none;transition:opacity .35s;padding:20px}
.mod-ov.open{opacity:1;pointer-events:all}
.mod-box{background:var(--bg);border-radius:22px;max-width:540px;width:100%;transform:scale(.92) translateY(16px);transition:transform .35s,background var(--tr);border:1px solid var(--border);overflow:hidden}
.mod-ov.open .mod-box{transform:scale(1) translateY(0)}
.mod-top{padding:24px 30px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center}
.mod-title{font-family:'Cormorant Garamond',serif;font-size:23px;font-weight:400;color:var(--text)}
.mod-x{width:34px;height:34px;border-radius:7px;border:1px solid var(--border);background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--text3);transition:all .3s}
.mod-x:hover{border-color:var(--gold);color:var(--gold)}
/* INVOICE */
.inv-wrap{padding:28px 30px}
.inv-logo{font-family:'Cormorant Garamond',serif;font-size:21px;font-weight:600;color:var(--gold);text-align:center;margin-bottom:3px}
.inv-sublogo{font-size:9.5px;letter-spacing:.3em;text-transform:uppercase;color:var(--text3);text-align:center;margin-bottom:22px}
.inv-row{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:18px}
.inv-lbl{font-size:10.5px;letter-spacing:.15em;text-transform:uppercase;color:var(--text3);margin-bottom:3px}
.inv-val{font-size:14px;color:var(--text);font-weight:500}
.inv-tbl{width:100%;border-collapse:collapse;font-size:13px;margin:18px 0}
.inv-tbl th{text-align:left;padding:7px 0;font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:var(--text3);border-bottom:1px solid var(--border);font-weight:400}
.inv-tbl td{padding:9px 0;border-bottom:1px solid var(--border);color:var(--text2)}
.inv-tbl td:last-child{text-align:right;color:var(--gold);font-weight:500}
.inv-totals{display:flex;flex-direction:column;gap:5px;margin-bottom:4px}
.inv-trow{display:flex;justify-content:space-between;font-size:13px;color:var(--text3)}
.inv-grand{display:flex;justify-content:space-between;padding:13px 0;border-top:2px solid var(--border);margin-top:4px}
.inv-grand-lbl{font-size:13px;text-transform:uppercase;font-weight:500;color:var(--text)}
.inv-grand-val{font-family:'Cormorant Garamond',serif;font-size:22px;color:var(--gold);font-weight:600}
.inv-note{font-size:11.5px;color:var(--text3);text-align:center;margin-top:14px;line-height:1.7;padding-top:14px;border-top:1px solid var(--border)}
.dl-inv-btn{display:none}
/* SUCCESS */
.suc-wrap{padding:48px 38px;text-align:center}
.suc-ico{width:64px;height:64px;border-radius:50%;background:var(--gold-glow);border:1.5px solid rgba(201,168,76,.3);display:flex;align-items:center;justify-content:center;margin:0 auto 20px}
.suc-title{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:400;color:var(--text);margin-bottom:12px}
.suc-desc{font-size:14px;color:var(--text3);line-height:1.75;margin-bottom:24px}
.suc-close{background:var(--gold);color:#1A1410;padding:12px 34px;border-radius:7px;font-family:'Jost',sans-serif;font-size:12px;letter-spacing:.15em;text-transform:uppercase;border:none;cursor:pointer;font-weight:500;transition:all .3s}
.suc-close:hover{background:var(--gold2)}

/* FOOTER */
footer{background:var(--bg2);border-top:1px solid var(--border);padding:56px 0 26px;transition:background var(--tr)}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1.2fr;gap:44px;margin-bottom:48px}
.f-logo{font-family:'Cormorant Garamond',serif;font-size:21px;font-weight:600;color:var(--gold);letter-spacing:.04em;display:block;margin-bottom:12px}
.f-brand p{font-size:13px;color:var(--text3);line-height:1.8;max-width:270px;margin-bottom:18px}
.f-contact{display:flex;align-items:flex-start;gap:9px;font-size:13px;color:var(--text3);margin-bottom:9px;line-height:1.55}
.f-contact svg{flex-shrink:0;margin-top:2px;color:var(--gold)}
.f-social{display:flex;gap:10px;margin-top:14px}
.soc-btn{width:34px;height:34px;border-radius:7px;border:1px solid var(--border);background:transparent;display:flex;align-items:center;justify-content:center;color:var(--text3);cursor:pointer;text-decoration:none;transition:all .3s;font-size:12px;font-weight:500}
.soc-btn:hover{border-color:var(--gold);color:var(--gold);background:var(--gold-glow)}
.f-col h4{font-size:10.5px;letter-spacing:.3em;text-transform:uppercase;color:var(--gold);margin-bottom:16px}
.f-col a{display:block;font-size:13px;color:var(--text3);text-decoration:none;margin-bottom:10px;transition:color .3s}
.f-col a:hover{color:var(--gold)}
.f-bottom{border-top:1px solid var(--border);padding-top:20px;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px}
.f-bottom p{font-size:12px;color:var(--text4)}
.f-bottom a{color:var(--text3);text-decoration:none;transition:color .3s}
.f-bottom a:hover{color:var(--gold)}
.f-certs{display:flex;gap:14px}
.f-cert{font-size:11px;color:var(--text4);display:flex;align-items:center;gap:5px}
.f-cert::before{content:'✦';color:var(--gold);font-size:9px}

/* SCROLL TOP */
.scrolltop{position:fixed;bottom:30px;right:30px;z-index:400;width:44px;height:44px;border-radius:50%;background:var(--gold);border:none;cursor:pointer;display:flex;align-items:center;justify-content:center;opacity:0;transform:translateY(12px);transition:all .35s;box-shadow:0 6px 18px rgba(201,168,76,.35)}
.scrolltop.show{opacity:1;transform:translateY(0)}
.scrolltop:hover{background:var(--gold2);transform:translateY(-3px)}

/* ANIMATIONS */
@keyframes fadeUp{from{opacity:0;transform:translateY(22px)}to{opacity:1;transform:translateY(0)}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes marquee{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.reveal{opacity:0;transform:translateY(24px);transition:opacity .72s ease,transform .72s ease}
.reveal.in{opacity:1;transform:translateY(0)}

/* RESPONSIVE */
@media(max-width:980px){
  .page-wrap,.nav-inner{padding:0 24px}
  .nav-inner{grid-template-columns:1fr auto}
  .nav-left{display:none}
  .hero-grid,.custom-grid,.about-grid,.footer-grid{grid-template-columns:1fr;gap:36px}
  .hero-mosaic{display:none}
  .hero-h1{font-size:44px}
  .rec-grid,.coll-grid,.testi-grid{grid-template-columns:repeat(2,1fr)}
  .feat-grid{grid-template-columns:repeat(2,1fr)}
  .cart-panel{width:340px}
}
@media(max-width:600px){
  .rec-grid,.coll-grid,.testi-grid{grid-template-columns:1fr}
  .hero-h1{font-size:34px}
  .sec-title{font-size:32px}
  .custom-box{padding:30px 22px}
  .cart-panel{width:100%}
  .footer-grid{grid-template-columns:1fr 1fr}
}
</style>
</head>
<body>

<div class="cursor" id="cur"></div>
<div class="cursor-ring" id="curRing"></div>

<!-- ===== NAV ===== -->
<nav id="navbar">
  <div class="nav-topbar">✦ Free home delivery across Delhi NCR · BIS Hallmark Certified · Est. 1952 ✦</div>
  <div class="nav-inner">
    <div class="nav-left">
      <a href="#home">Home</a>
      <a href="#collections">Collections</a>
      <a href="#custom-page">Custom Order</a>
      <a href="#recommended">Recommended</a>
    </div>
    <a href="#home" class="nav-logo">
      <span class="nav-logo-main">Musaddilal Jewellers</span>
      <span class="nav-logo-sub">Pvt. Ltd. &nbsp;·&nbsp; Est. 1952</span>
    </a>
    <div class="nav-right">
      <a href="#" class="icon-btn" onclick="openCart(event)" title="Cart">
        <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 01-8 0"/></svg>
        <span class="cart-badge" id="cartCount">0</span>
      </a>
      <a href="#" class="icon-btn" onclick="openInvoice(event)" title="Download Invoice">
        <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="12" y1="18" x2="12" y2="12"/><polyline points="9 15 12 18 15 15"/></svg>
      </a>
      <div class="dot-wrap">
        <button class="dot-btn" id="dotBtn" onclick="toggleDot()">
          <span></span><span></span><span></span>
        </button>
        <div class="dot-dd" id="dotDd">
          <a class="dd-item" href="#home"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/></svg></div>Home</a>
          <a class="dd-item" href="#recommended"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/></svg></div>Recommended</a>
          <a class="dd-item" href="#collections"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg></div>Collections</a>
          <a class="dd-item" href="#custom-page"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="12" cy="12" r="3"/><path d="M19.07 4.93a10 10 0 010 14.14"/><path d="M4.93 4.93a10 10 0 000 14.14"/></svg></div>Custom Jewellery</a>
          <a class="dd-item" onclick="openCart(event);toggleDot()"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/></svg></div>My Cart</a>
          <a class="dd-item" onclick="openInvoice(event);toggleDot()"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/></svg></div>Download Invoice</a>
          <div class="dd-sep"></div>
          <a class="dd-item" href="#about"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg></div>About Us</a>
          <a class="dd-item" href="#contact"><div class="dd-ico"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M22 16.92v3a2 2 0 01-2.18 2A19.79 19.79 0 013.07 9.81 19.79 19.79 0 012 2.22 2 2 0 014 .01H7a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L8.09 7.91a16 16 0 006.18 6.18l1.27-.83a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z"/></svg></div>Contact</a>
          <div class="dd-sep"></div>
          <div class="theme-row">
            <span class="theme-lbl">Dark Mode</span>
            <button class="tog" onclick="toggleTheme()"></button>
          </div>
        </div>
      </div>
    </div>
  </div>
</nav>

<!-- ===== HERO ===== -->
<section style="padding-top:110px;min-height:100vh;display:flex;align-items:center;position:relative;overflow:hidden" id="home">
  <div class="hero-orb"></div><div class="hero-orb"></div>
  <div class="page-wrap" style="width:100%">
    <div class="hero-grid">
      <div>
        <div class="hero-tag">Since 1952 · Handcrafted Excellence</div>
        <h1 class="hero-h1">Where Gold<br>Meets <em>Artistry</em><br>& Soul</h1>
        <p class="hero-desc">Every piece we craft carries the warmth of generations. Musaddilal Jewellers creates heirloom jewellery that transcends time — handmade with precision, worn with pride.</p>
        <div class="hero-btns">
          <a href="#collections" class="btn btn-gold">Explore Collections →</a>
          <a href="#custom-page" class="btn btn-ghost">Order Custom Piece</a>
        </div>
        <div class="hero-stats">
          <div><div class="stat-n">70+</div><div class="stat-l">Years of Craft</div></div>
          <div><div class="stat-n">50K+</div><div class="stat-l">Happy Families</div></div>
          <div><div class="stat-n">BIS</div><div class="stat-l">Hallmark Certified</div></div>
        </div>
      </div>
      <div class="hero-mosaic">
        <div class="mos">
          <img src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=600&q=80" alt="Gold Necklace">
          <span class="mos-lbl">✦ Rani Haar Collection</span>
          <span class="mos-badge">Bestseller</span>
        </div>
        <div class="mos">
          <img src="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=400&q=80" alt="Diamond Ring">
          <span class="mos-lbl">✦ Solitaire Series</span>
        </div>
        <div class="mos">
          <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=400&q=80" alt="Gold Bangles">
          <span class="mos-lbl">✦ Jadau Bangles</span>
          <span class="mos-badge">New</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== MARQUEE ===== -->
<div class="mq-wrap">
  <div class="mq-track">
    <span class="mq-item">Gold Jewellery<span>✦</span></span><span class="mq-item">Diamond Rings<span>✦</span></span><span class="mq-item">Bridal Collections<span>✦</span></span><span class="mq-item">Custom Jewellery<span>✦</span></span><span class="mq-item">Silver Ornaments<span>✦</span></span><span class="mq-item">Antique Pieces<span>✦</span></span><span class="mq-item">Temple Jewellery<span>✦</span></span><span class="mq-item">Kundan Work<span>✦</span></span><span class="mq-item">Jadau Sets<span>✦</span></span><span class="mq-item">Meenakari<span>✦</span></span>
    <span class="mq-item">Gold Jewellery<span>✦</span></span><span class="mq-item">Diamond Rings<span>✦</span></span><span class="mq-item">Bridal Collections<span>✦</span></span><span class="mq-item">Custom Jewellery<span>✦</span></span><span class="mq-item">Silver Ornaments<span>✦</span></span><span class="mq-item">Antique Pieces<span>✦</span></span><span class="mq-item">Temple Jewellery<span>✦</span></span><span class="mq-item">Kundan Work<span>✦</span></span><span class="mq-item">Jadau Sets<span>✦</span></span><span class="mq-item">Meenakari<span>✦</span></span>
  </div>
</div>

<!-- ===== RECOMMENDED ===== -->
<section id="recommended">
  <div class="page-wrap">
    <div class="rec-top reveal">
      <div><span class="eyebrow">Recommended For You</span><h2 class="sec-title">Our <em>Most Loved</em> Pieces</h2></div>
      <a href="#collections" class="view-all">See All Collections →</a>
    </div>
    <div class="rec-grid">
      <div class="rec-card reveal" data-id="r1" data-name="Diamond Solitaire Ring" data-price="45000" data-img="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=400&q=80">
        <div class="rec-img">
          <img src="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=400&q=80" alt="Diamond Ring" loading="lazy">
          <div class="rec-ov"></div><span class="rec-tag">Top Rated</span>
          <button class="rec-add" onclick="addToCart(this)"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#1A1410" stroke-width="2"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg></button>
        </div>
        <div class="rec-body"><p class="rec-name">Diamond Solitaire Ring</p><p class="rec-sub">18K Gold · IGI Certified Diamond</p><div class="rec-foot"><span class="rec-price">₹45,000</span><span class="rec-stars">★★★★★</span></div></div>
      </div>
      <div class="rec-card reveal" data-id="r2" data-name="Rani Haar Necklace" data-price="78000" data-img="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=400&q=80">
        <div class="rec-img">
          <img src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=400&q=80" alt="Necklace" loading="lazy">
          <div class="rec-ov"></div><span class="rec-tag">Bestseller</span>
          <button class="rec-add" onclick="addToCart(this)"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#1A1410" stroke-width="2"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg></button>
        </div>
        <div class="rec-body"><p class="rec-name">Rani Haar Necklace</p><p class="rec-sub">22K Gold · Handcrafted Kundan</p><div class="rec-foot"><span class="rec-price">₹78,000</span><span class="rec-stars">★★★★★</span></div></div>
      </div>
      <div class="rec-card reveal" data-id="r3" data-name="Jadau Gold Bangles" data-price="32000" data-img="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=400&q=80">
        <div class="rec-img">
          <img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=400&q=80" alt="Bangles" loading="lazy">
          <div class="rec-ov"></div><span class="rec-tag">New Arrival</span>
          <button class="rec-add" onclick="addToCart(this)"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#1A1410" stroke-width="2"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg></button>
        </div>
        <div class="rec-body"><p class="rec-name">Jadau Gold Bangles</p><p class="rec-sub">22K Gold · Meenakari Work</p><div class="rec-foot"><span class="rec-price">₹32,000</span><span class="rec-stars">★★★★☆</span></div></div>
      </div>
      <div class="rec-card reveal" data-id="r4" data-name="Gold Jhumka Earrings" data-price="18500" data-img="https://images.unsplash.com/photo-1630019852942-f89202989a59?w=400&q=80">
        <div class="rec-img">
          <img src="https://images.unsplash.com/photo-1630019852942-f89202989a59?w=400&q=80" alt="Earrings" loading="lazy">
          <div class="rec-ov"></div>
          <button class="rec-add" onclick="addToCart(this)"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#1A1410" stroke-width="2"><line x1="12" y1="5" x2="12" y2="19"/><line x1="5" y1="12" x2="19" y2="12"/></svg></button>
        </div>
        <div class="rec-body"><p class="rec-name">Gold Jhumka Earrings</p><p class="rec-sub">22K Gold · Traditional Enamel</p><div class="rec-foot"><span class="rec-price">₹18,500</span><span class="rec-stars">★★★★★</span></div></div>
      </div>
    </div>
  </div>
</section>

<!-- ===== COLLECTIONS ===== -->
<section id="collections" style="background:var(--bg2);padding:80px 0;border-top:1px solid var(--border);transition:background var(--tr)">
  <div class="page-wrap">
    <div class="coll-top reveal">
      <div><span class="eyebrow">Our Collections</span><h2 class="sec-title">Crafted for <em>Every Occasion</em></h2></div>
      <a href="#" class="view-all">View All →</a>
    </div>
    <div class="coll-grid">
      <div class="coll-card reveal" data-id="c1" data-name="Rani Haar Collection" data-price="45000" data-img="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=600&q=80" alt="Necklace" loading="lazy"><div class="coll-ov"></div><span class="coll-tag">New</span></div>
        <div class="coll-body"><p class="coll-name">Rani Haar Collection</p><p class="coll-sub">22K Gold · Handcrafted · Kundan</p><div class="coll-foot"><span class="coll-price">Starting ₹45,000</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
      <div class="coll-card reveal" data-id="c2" data-name="Diamond Solitaire Ring" data-price="28000" data-img="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1602173574767-37ac01994b2a?w=600&q=80" alt="Ring" loading="lazy"><div class="coll-ov"></div><span class="coll-tag">Trending</span></div>
        <div class="coll-body"><p class="coll-name">Diamond Solitaire</p><p class="coll-sub">18K Gold · Diamond · IGI Certified</p><div class="coll-foot"><span class="coll-price">Starting ₹28,000</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
      <div class="coll-card reveal" data-id="c3" data-name="Jadau Bangles Set" data-price="32000" data-img="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1599643478518-a784e5dc4c8f?w=600&q=80" alt="Bangles" loading="lazy"><div class="coll-ov"></div></div>
        <div class="coll-body"><p class="coll-name">Jadau Bangles Set</p><p class="coll-sub">22K Gold · Kundan · Meenakari</p><div class="coll-foot"><span class="coll-price">Starting ₹32,000</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
      <div class="coll-card reveal" data-id="c4" data-name="Gold Jhumka Earrings" data-price="12000" data-img="https://images.unsplash.com/photo-1630019852942-f89202989a59?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1630019852942-f89202989a59?w=600&q=80" alt="Earrings" loading="lazy"><div class="coll-ov"></div><span class="coll-tag">Classic</span></div>
        <div class="coll-body"><p class="coll-name">Jhumka Collection</p><p class="coll-sub">22K Gold · Enamel · Traditional</p><div class="coll-foot"><span class="coll-price">Starting ₹12,000</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
      <div class="coll-card reveal" data-id="c5" data-name="Bridal Full Set" data-price="180000" data-img="https://images.unsplash.com/photo-1611085583191-a3b181a88401?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1611085583191-a3b181a88401?w=600&q=80" alt="Bridal" loading="lazy"><div class="coll-ov"></div><span class="coll-tag">Bridal</span></div>
        <div class="coll-body"><p class="coll-name">Shaadi Special Set</p><p class="coll-sub">22K Gold · Complete Bridal Set</p><div class="coll-foot"><span class="coll-price">Starting ₹1,80,000</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
      <div class="coll-card reveal" data-id="c6" data-name="Pure Silver Payal" data-price="3500" data-img="https://images.unsplash.com/photo-1571945153237-4929e783af4a?w=600&q=80">
        <div class="coll-img"><img src="https://images.unsplash.com/photo-1571945153237-4929e783af4a?w=600&q=80" alt="Payal" loading="lazy"><div class="coll-ov"></div></div>
        <div class="coll-body"><p class="coll-name">Pure Silver Payal</p><p class="coll-sub">925 Sterling Silver · Hallmarked</p><div class="coll-foot"><span class="coll-price">Starting ₹3,500</span><span class="coll-arr" onclick="addToCartById(this.closest('.coll-card'))">+</span></div></div>
      </div>
    </div>
  </div>
</section>

<!-- ===== FEATURES ===== -->
<div class="features-bg">
  <div class="page-wrap">
    <div class="feat-grid reveal">
      <div class="feat"><div class="feat-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div><p class="feat-t">BIS Hallmark Certified</p><p class="feat-d">Every piece certified under Government of India standards for purity.</p></div>
      <div class="feat"><div class="feat-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/></svg></div><p class="feat-t">Master Craftsmen</p><p class="feat-d">Karigars with 30+ years experience handcraft each piece with love.</p></div>
      <div class="feat"><div class="feat-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg></div><p class="feat-t">Free Home Delivery</p><p class="feat-d">Secure, insured delivery across India in our signature gift box.</p></div>
      <div class="feat"><div class="feat-icon"><svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M4 12V6a2 2 0 012-2h12a2 2 0 012 2v6M2 12h20M12 12v8m-4-4h8"/></svg></div><p class="feat-t">Lifetime Exchange</p><p class="feat-d">Full exchange and buy-back policy on all gold jewellery pieces.</p></div>
    </div>
  </div>
</div>

<!-- ===== CUSTOM ORDER ===== -->
<section id="custom-page">
  <div class="page-wrap">
    <div class="custom-box reveal">
      <div class="custom-grid">
        <div>
          <span class="eyebrow">Custom Jewellery</span>
          <h2 class="sec-title" style="font-size:38px">Design Your <em>Dream Piece</em></h2>
          <p class="sec-sub">Tell us your vision — our master craftsmen will bring it to life. Share your requirements and we will suggest the best price for you.</p>
          <div class="proc-list">
            <div class="proc-step"><div class="proc-num">1</div><div><p class="proc-h">Submit Your Request</p><p class="proc-p">Describe your design, metal preference, gemstones, and occasion</p></div></div>
            <div class="proc-step"><div class="proc-num">2</div><div><p class="proc-h">We Suggest a Price</p><p class="proc-p">Our experts send you a fair custom quote within 24 hours</p></div></div>
            <div class="proc-step"><div class="proc-num">3</div><div><p class="proc-h">Crafting Begins</p><p class="proc-p">Once approved, our karigars handcraft your unique piece</p></div></div>
            <div class="proc-step"><div class="proc-num">4</div><div><p class="proc-h">Delivered with Love</p><p class="proc-p">Your jewel arrives in our signature Musaddilal gift box</p></div></div>
          </div>
          <div style="display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:28px">
            <div style="border-radius:12px;overflow:hidden;height:130px"><img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?w=400&q=80" alt="Custom jewel" style="width:100%;height:100%;object-fit:cover" loading="lazy"></div>
            <div style="border-radius:12px;overflow:hidden;height:130px"><img src="https://images.unsplash.com/photo-1506630448388-4e683c67ddb0?w=400&q=80" alt="Custom jewel 2" style="width:100%;height:100%;object-fit:cover" loading="lazy"></div>
          </div>
        </div>
        <div>
          <div class="cform">
            <div class="frow">
              <div class="fg"><label>Full Name *</label><input type="text" id="fname" placeholder="Your full name"></div>
              <div class="fg"><label>Phone Number *</label><input type="tel" id="fphone" placeholder="+91 00000 00000"></div>
            </div>
            <div class="fg"><label>Email Address</label><input type="email" id="femail" placeholder="your@email.com"></div>
            <div class="frow">
              <div class="fg"><label>Jewellery Type *</label><select id="fjtype"><option value="">Select type</option><option>Necklace / Haar</option><option>Ring / Solitaire</option><option>Bangles / Kada</option><option>Earrings / Jhumka</option><option>Bridal Full Set</option><option>Bracelet</option><option>Pendant / Locket</option><option>Anklet / Payal</option><option>Maang Tikka</option><option>Nose Ring / Nath</option><option>Other</option></select></div>
              <div class="fg"><label>Metal Preference *</label><select id="fmetal"><option value="">Select metal</option><option>22K Yellow Gold</option><option>18K Yellow Gold</option><option>18K White Gold</option><option>18K Rose Gold</option><option>Sterling Silver (925)</option><option>Platinum</option><option>Mixed / Suggest me</option></select></div>
            </div>
            <div class="frow">
              <div class="fg"><label>Gemstone (Optional)</label><select id="fgem"><option value="">No gemstone</option><option>Diamond</option><option>Ruby</option><option>Emerald</option><option>Sapphire</option><option>Pearl</option><option>Polki / Kundan</option><option>Coral</option><option>Other</option></select></div>
              <div class="fg"><label>Your Budget (Optional)</label><input type="text" id="fbudget" placeholder="e.g. ₹50,000 – ₹80,000"></div>
            </div>
            <div class="fg"><label>Occasion</label><select id="focc"><option value="">Select occasion</option><option>Wedding / Shaadi</option><option>Engagement</option><option>Anniversary Gift</option><option>Birthday Gift</option><option>Festival</option><option>Daily Wear</option><option>Investment</option><option>Other</option></select></div>
            <div class="fg"><label>Describe Your Design *</label><textarea id="fdesc" placeholder="Design details, size, style, special requirements, any inspiration..."></textarea></div>
            <div class="price-note"><strong>✦ Seller Price Suggestion:</strong> After reviewing your request, our team will personally contact you within <strong>24 hours</strong> with a custom price quote tailored to your design and budget.</div>
            <div class="wa-row">
              <div class="wa-ico"><svg width="18" height="18" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M11.999 2C6.477 2 2 6.477 2 12c0 1.89.525 3.66 1.438 5.168L2 22l4.978-1.306A9.951 9.951 0 0012 22c5.523 0 10-4.477 10-10S17.523 2 12 2z"/></svg></div>
              <div style="flex:1"><strong style="color:var(--text);font-size:13px">Quick Order via WhatsApp</strong><br><span style="font-size:12px">Chat directly for instant quotes</span></div>
              <a href="https://wa.me/919873465000?text=Hi!%20I%20want%20to%20order%20custom%20jewellery." target="_blank" class="wa-btn">WhatsApp →</a>
            </div>
            <button class="sub-btn" onclick="submitOrder()">Submit Custom Order Request ✦</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== TESTIMONIALS ===== -->
<section style="padding:80px 0;background:var(--bg2);border-top:1px solid var(--border);transition:background var(--tr)">
  <div class="page-wrap">
    <div class="testi-hdr reveal"><span class="eyebrow">Customer Stories</span><h2 class="sec-title">Loved by <em>Generations</em></h2></div>
    <div class="testi-grid reveal">
      <div class="testi-card"><div class="stars">★★★★★</div><p class="testi-txt">"My bridal set was exactly what I dreamed of. The craftsmanship is extraordinary and the team guided me through every step."</p><div class="testi-auth"><div class="auth-av">P</div><div><p class="auth-name">Priya Sharma</p><p class="auth-loc">New Delhi</p></div></div></div>
      <div class="testi-card"><div class="stars">★★★★★</div><p class="testi-txt">"I ordered a custom kada for my father's birthday. They suggested the perfect design within our budget and delivered on time!"</p><div class="testi-auth"><div class="auth-av">R</div><div><p class="auth-name">Rahul Mehta</p><p class="auth-loc">Mumbai</p></div></div></div>
      <div class="testi-card"><div class="stars">★★★★★</div><p class="testi-txt">"Three generations of my family shop here. The quality and trust Musaddilal offers is unmatched. Our family jeweller, forever."</p><div class="testi-auth"><div class="auth-av">S</div><div><p class="auth-name">Sunita Agarwal</p><p class="auth-loc">Jaipur</p></div></div></div>
    </div>
  </div>
</section>

<!-- ===== ABOUT ===== -->
<div class="about-bg" id="about">
  <div class="page-wrap">
    <div class="about-grid reveal">
      <div class="about-img-wrap">
        <div class="about-img"><img src="https://images.unsplash.com/photo-1584302179602-e4c3d3fd629d?w=700&q=80" alt="Jewellery crafting" loading="lazy"></div>
        <div class="about-badge"><div class="about-badge-n">1952</div><div class="about-badge-t">Est. in Delhi</div></div>
      </div>
      <div>
        <span class="eyebrow">Our Story</span>
        <h2 class="sec-title" style="font-size:38px">Seven Decades of <em>Golden Legacy</em></h2>
        <p style="font-size:14px;color:var(--text3);line-height:1.9;margin-bottom:14px">Founded in 1952 in the heart of Old Delhi, Musaddilal Jewellers began as a small workshop run by master craftsman Late Shri Musaddilal Ji. What started with a hammer, a flame, and a dream — has grown into one of Delhi's most trusted jewellery names.</p>
        <p style="font-size:14px;color:var(--text3);line-height:1.9;margin-bottom:14px">Today, the third generation of our family continues the tradition, blending age-old techniques with modern designs. Every piece we make carries our legacy of trust, purity, and love.</p>
        <div class="cert-row"><span class="cert">BIS Hallmark</span><span class="cert">22K Certified</span><span class="cert">IGI Diamond</span><span class="cert">GST Registered</span></div>
      </div>
    </div>
  </div>
</div>

<!-- ===== FOOTER ===== -->
<footer id="contact">
  <div class="page-wrap">
    <div class="footer-grid">
      <div class="f-brand">
        <span class="f-logo">Musaddilal Jewellers</span>
        <p>Crafting timeless jewellery since 1952. Every piece is a work of art, made with love and precision by our master karigars in Old Delhi.</p>
        <div class="f-contact"><svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg><a href="https://share.google/tpfEQKuUCXW9uog0m" target="_blank" style="color:inherit;text-decoration:none">View on Google Maps →</a></div>
        <div class="f-contact"><svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M22 16.92v3a2 2 0 01-2.18 2A19.79 19.79 0 013.07 9.81 19.79 19.79 0 012 2.22 2 2 0 014 .01H7a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L8.09 7.91a16 16 0 006.18 6.18l1.27-.83a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z"/></svg>+91 98734 65000</div>
        <div class="f-contact"><svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4821262e2708253d3b292c2c21242924222d3f2d24242d3a3b662b2725">[email&#160;protected]</a></div>
        <div class="f-social"><a href="#" class="soc-btn">f</a><a href="#" class="soc-btn">in</a><a href="#" class="soc-btn">yt</a><a href="https://wa.me/919873465000" target="_blank" class="soc-btn">wa</a></div>
      </div>
      <div class="f-col"><h4>Collections</h4><a href="#">Gold Jewellery</a><a href="#">Diamond Rings</a><a href="#">Bridal Sets</a><a href="#">Silver Ornaments</a><a href="#">Antique Pieces</a><a href="#">Temple Jewellery</a></div>
      <div class="f-col"><h4>Quick Links</h4><a href="#custom-page">Custom Order</a><a href="#about">Our Story</a><a href="#">Hallmark Certified</a><a href="#">Exchange Policy</a><a href="#">Jewellery Care Guide</a><a href="#">Book Appointment</a></div>
      <div class="f-col">
        <h4>Shop Timing</h4>
        <a style="cursor:default">Mon – Sat: 10 AM – 8 PM</a>
        <a style="cursor:default">Sunday: 11 AM – 6 PM</a>
        <a href="#custom-page" style="color:var(--gold);margin-top:8px">✦ Book a Private Visit</a>
        <a href="https://wa.me/919873465000" target="_blank" class="wa-btn" style="margin-top:16px;font-size:11px;padding:9px 14px"><svg width="13" height="13" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M11.999 2C6.477 2 2 6.477 2 12c0 1.89.525 3.66 1.438 5.168L2 22l4.978-1.306A9.951 9.951 0 0012 22c5.523 0 10-4.477 10-10S17.523 2 12 2z"/></svg>WhatsApp Us</a>
      </div>
    </div>
    <div class="f-bottom">
      <p>© 2025 Musaddilal Jewellers Pvt. Ltd. All rights reserved. &nbsp;·&nbsp; <a href="#">Privacy</a> &nbsp;·&nbsp; <a href="#">Terms</a></p>
      <div class="f-certs"><span class="f-cert">BIS Hallmark</span><span class="f-cert">GST Registered</span><span class="f-cert">Since 1952</span></div>
    </div>
  </div>
</footer>

<!-- ===== CART PANEL ===== -->
<div class="cart-ov" id="cartOv" onclick="closeCart()"></div>
<div class="cart-panel" id="cartPanel">
  <div class="cart-hdr">
    <h2 class="cart-title">My Cart ✦</h2>
    <button class="cart-cls" onclick="closeCart()"><svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg></button>
  </div>
  <div class="cart-items" id="cartItems">
    <div class="cart-empty" id="cartEmpty">
      <svg width="46" height="46" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 01-8 0"/></svg>
      <p>Your cart is empty</p><span>Add some beautiful jewellery!</span>
    </div>
  </div>
  <div class="cart-ftr">
    <div class="cart-total-row"><span class="ct-lbl">Total Amount</span><span class="ct-val" id="cartTotal">₹0</span></div>
    <button class="checkout-btn" onclick="checkout()">Proceed to Checkout →</button>
    <button class="inv-dl-btn" onclick="closeCart();openInvoice(null)">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="12" y1="18" x2="12" y2="12"/><polyline points="9 15 12 18 15 15"/></svg>
      Download Invoice
    </button>
  </div>
</div>

<!-- ===== INVOICE MODAL ===== -->
<div class="mod-ov" id="invoiceMod" onclick="closeMod(event,'invoiceMod')">
  <div class="mod-box">
    <div class="mod-top">
      <span class="mod-title">Invoice &amp; Receipt</span>
      <button class="mod-x" onclick="document.getElementById('invoiceMod').classList.remove('open')"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg></button>
    </div>
    <div class="inv-wrap" id="invContent">
      <p class="inv-logo">Musaddilal Jewellers</p>
      <p class="inv-sublogo">Pvt. Ltd. · Dariba Kalan, Old Delhi · GST: 07AXXXX1234X1ZX</p>
      <div class="inv-row">
        <div><p class="inv-lbl">Invoice No.</p><p class="inv-val" id="invNo">ML-2025-0001</p></div>
        <div style="text-align:right"><p class="inv-lbl">Date</p><p class="inv-val" id="invDate">—</p></div>
      </div>
      <div class="inv-row">
        <div><p class="inv-lbl">Billed To</p><p class="inv-val">Valued Customer</p><p style="font-size:12px;color:var(--text3)">+91 98734 65000</p></div>
        <div style="text-align:right"><p class="inv-lbl">Payment Status</p><p style="color:#1E9B56;font-weight:500;font-size:14px">✓ Confirmed</p></div>
      </div>
      <table class="inv-tbl"><thead><tr><th>Item</th><th>Metal</th><th>Qty</th><th>Amount</th></tr></thead><tbody id="invBody"></tbody></table>
      <div class="inv-totals">
        <div class="inv-trow"><span>Subtotal</span><span id="invSub">₹0</span></div>
        <div class="inv-trow"><span>GST (3%)</span><span id="invGst">₹0</span></div>
        <div class="inv-trow"><span>Making Charges</span><span>Included</span></div>
      </div>
      <div class="inv-grand"><span class="inv-grand-lbl">Grand Total</span><span class="inv-grand-val" id="invGrand">₹0</span></div>
      <p class="inv-note">Thank you for your trust in Musaddilal Jewellers. This invoice is system-generated and valid without signature. All jewellery is BIS Hallmark certified. For queries call +91 98734 65000.</p>
      <button class="dl-inv-btn" onclick="downloadInvoice()"><svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 01-2 2H5a2 2 0 01-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>Download Invoice / Print</button>
    </div>
  </div>
</div>

<!-- ===== SUCCESS MODAL ===== -->
<div class="mod-ov" id="successMod" onclick="closeMod(event,'successMod')">
  <div class="mod-box">
    <div class="suc-wrap">
      <div class="suc-ico"><svg width="30" height="30" viewBox="0 0 24 24" fill="none" stroke="#C9A84C" stroke-width="1.3"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg></div>
      <h3 class="suc-title">Order Received! ✦</h3>
      <p class="suc-desc">Thank you for your custom jewellery request. Our team will review your design and contact you within <strong style="color:var(--gold)">24 hours</strong> with a personalized price quote.<br><br>You will receive a confirmation on your WhatsApp shortly.</p>
      <button class="suc-close" onclick="document.getElementById('successMod').classList.remove('open')">Close</button>
    </div>
  </div>
</div>

<button class="scrolltop" id="stBtn" onclick="window.scrollTo({top:0,behavior:'smooth'})">
  <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="#1A1410" stroke-width="2.5" stroke-linecap="round"><path d="M18 15l-6-6-6 6"/></svg>
</button>

<!-- ===== SCRIPTS ===== -->
<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
/* CURSOR */
const cur=document.getElementById('cur'),ring=document.getElementById('curRing');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{mx=e.clientX;my=e.clientY;cur.style.left=mx+'px';cur.style.top=my+'px'});
(function a(){rx+=(mx-rx)*.12;ry+=(my-ry)*.12;ring.style.left=rx+'px';ring.style.top=ry+'px';requestAnimationFrame(a)})();
document.querySelectorAll('a,button,.coll-card,.rec-card,.mos').forEach(el=>{
  el.addEventListener('mouseenter',()=>{cur.style.width='18px';cur.style.height='18px';ring.style.width='46px';ring.style.height='46px'});
  el.addEventListener('mouseleave',()=>{cur.style.width='9px';cur.style.height='9px';ring.style.width='34px';ring.style.height='34px'});
});

/* THEME */
function toggleTheme(){const h=document.documentElement;const d=h.getAttribute('data-theme')==='dark';h.setAttribute('data-theme',d?'light':'dark');localStorage.setItem('mlT',d?'light':'dark')}
(()=>{const s=localStorage.getItem('mlT');if(s)document.documentElement.setAttribute('data-theme',s)})();

/* NAV SCROLL */
window.addEventListener('scroll',()=>{
  document.getElementById('stBtn').classList.toggle('show',window.scrollY>500);
});

/* DOT MENU */
let dotOpen=false;
function toggleDot(){dotOpen=!dotOpen;document.getElementById('dotDd').classList.toggle('open',dotOpen)}
document.addEventListener('click',e=>{if(dotOpen&&!e.target.closest('.dot-wrap')){dotOpen=false;document.getElementById('dotDd').classList.remove('open')}});

/* SMOOTH SCROLL */
document.querySelectorAll('a[href^="#"]').forEach(a=>{
  a.addEventListener('click',e=>{const id=a.getAttribute('href').slice(1);const el=document.getElementById(id);if(el){e.preventDefault();el.scrollIntoView({behavior:'smooth',block:'start'})}});
});

/* REVEAL */
const rvEls=document.querySelectorAll('.reveal');
const obs=new IntersectionObserver((ents)=>{ents.forEach((e,i)=>{if(e.isIntersecting)setTimeout(()=>e.target.classList.add('in'),i*80)});},{threshold:0.07});
rvEls.forEach(el=>obs.observe(el));

/* CART */
let cart=[];
function fmt(n){return '₹'+n.toLocaleString('en-IN')}
function cartSum(){return cart.reduce((s,i)=>s+i.price,0)}
function updateCart(){
  document.getElementById('cartCount').textContent=cart.length;
  document.getElementById('cartTotal').textContent=fmt(cartSum());
  const el=document.getElementById('cartItems');
  const emp=document.getElementById('cartEmpty');
  el.querySelectorAll('.c-item').forEach(i=>i.remove());
  if(!cart.length){emp.style.display='block';return;}
  emp.style.display='none';
  cart.forEach((item,idx)=>{
    const d=document.createElement('div');d.className='c-item';
    d.innerHTML=`<div class="c-item-img"><img src="${item.img}" alt="${item.name}"></div><div class="c-item-info"><p class="c-item-name">${item.name}</p><p class="c-item-sub">${item.metal}</p><p class="c-item-price">${fmt(item.price)}</p></div><button class="c-item-del" onclick="removeItem(${idx})"><svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="3 6 5 6 21 6"/><path d="M19 6v14a2 2 0 01-2 2H7a2 2 0 01-2-2V6m3 0V4a1 1 0 011-1h4a1 1 0 011 1v2"/></svg></button>`;
    el.appendChild(d);
  });
}
function addToCart(btn){
  const card=btn.closest('[data-id]');
  cart.push({id:card.dataset.id,name:card.dataset.name,price:parseInt(card.dataset.price)||0,img:card.dataset.img,metal:'22K Gold'});
  updateCart();btn.style.background='#1E9B56';setTimeout(()=>{btn.style.background=''},800);openCart(null);
}
function addToCartById(card){
  cart.push({id:card.dataset.id,name:card.dataset.name,price:parseInt(card.dataset.price)||0,img:card.dataset.img,metal:'22K Gold'});
  updateCart();openCart(null);
}
function removeItem(idx){cart.splice(idx,1);updateCart()}
function openCart(e){if(e)e.preventDefault();document.getElementById('cartPanel').classList.add('open');document.getElementById('cartOv').classList.add('open')}
function closeCart(){document.getElementById('cartPanel').classList.remove('open');document.getElementById('cartOv').classList.remove('open')}
function checkout(){if(!cart.length){alert('Your cart is empty!');return;}alert('Redirecting to payment gateway...\n\nIn a live site this opens your payment system.')}

/* INVOICE */
function openInvoice(e){
  if(e)e.preventDefault();
  const d=new Date();
  document.getElementById('invDate').textContent=d.toLocaleDateString('en-IN',{day:'2-digit',month:'long',year:'numeric'});
  document.getElementById('invNo').textContent='ML-'+d.getFullYear()+'-'+String(Math.floor(Math.random()*9000)+1000);
  const tbody=document.getElementById('invBody');tbody.innerHTML='';
  const items=cart.length?cart:[{name:'Custom Jewellery Enquiry',metal:'22K Gold',price:0}];
  let sub=0;
  items.forEach(item=>{sub+=item.price;const tr=document.createElement('tr');tr.innerHTML=`<td>${item.name}</td><td>${item.metal}</td><td>1</td><td>${fmt(item.price)}</td>`;tbody.appendChild(tr)});
  const gst=Math.round(sub*.03);
  document.getElementById('invSub').textContent=fmt(sub);
  document.getElementById('invGst').textContent=fmt(gst);
  document.getElementById('invGrand').textContent=fmt(sub+gst);
  document.getElementById('invoiceMod').classList.add('open');
}
function downloadInvoice(){
  const c=document.getElementById('invContent').innerHTML;
  const w=window.open('','_blank');
  w.document.write(`<!DOCTYPE html><html><head><title>Invoice — Musaddilal Jewellers</title><link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=Jost:wght@400;500&display=swap" rel="stylesheet"><style>body{font-family:'Jost',sans-serif;max-width:580px;margin:40px auto;padding:24px;color:#1A1410}p{margin:0}.inv-logo{font-family:'Cormorant+Garamond',serif;font-size:22px;font-weight:600;color:#C9A84C;text-align:center;margin-bottom:3px}.inv-sublogo{font-size:10px;letter-spacing:.28em;text-transform:uppercase;color:#9C8660;text-align:center;margin-bottom:22px}.inv-row{display:flex;justify-content:space-between;margin-bottom:18px}.inv-lbl{font-size:10.5px;letter-spacing:.15em;text-transform:uppercase;color:#9C8660;margin-bottom:3px}.inv-val{font-size:14px;font-weight:500}.inv-tbl{width:100%;border-collapse:collapse;font-size:13px;margin:18px 0}.inv-tbl th{text-align:left;padding:7px 0;font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:#9C8660;border-bottom:1px solid #EAE3D6;font-weight:400}.inv-tbl td{padding:9px 0;border-bottom:1px solid #EAE3D6;color:#5C4A2A}.inv-tbl td:last-child{text-align:right;color:#C9A84C;font-weight:500}.inv-totals{display:flex;flex-direction:column;gap:5px}.inv-trow{display:flex;justify-content:space-between;font-size:13px;color:#9C8660}.inv-grand{display:flex;justify-content:space-between;padding:13px 0;border-top:2px solid #EAE3D6;margin-top:4px}.inv-grand-lbl{font-size:13px;text-transform:uppercase;font-weight:500}.inv-grand-val{font-family:'Cormorant+Garamond',serif;font-size:22px;color:#C9A84C;font-weight:600}.inv-note{font-size:11.5px;color:#9C8660;text-align:center;margin-top:14px;line-height:1.7;padding-top:14px;border-top:1px solid #EAE3D6}.dl-inv-btn{display:none}</style></head><body>${c}</body></html>`);
  w.document.close();setTimeout(()=>w.print(),500);
}
function closeMod(e,id){if(e.target.id===id)document.getElementById(id).classList.remove('open')}

/* CUSTOM ORDER */
function submitOrder(){
  const name=document.getElementById('fname').value.trim();
  const phone=document.getElementById('fphone').value.trim();
  const jtype=document.getElementById('fjtype').value;
  const desc=document.getElementById('fdesc').value.trim();
  if(!name){alert('Please enter your full name.');document.getElementById('fname').focus();return}
  if(!phone){alert('Please enter your phone number.');document.getElementById('fphone').focus();return}
  if(!jtype){alert('Please select a jewellery type.');document.getElementById('fjtype').focus();return}
  if(!desc){alert('Please describe your design.');document.getElementById('fdesc').focus();return}
  // Clear form
  document.getElementById('fname').value='';document.getElementById('fphone').value='';document.getElementById('femail').value='';document.getElementById('fjtype').selectedIndex=0;document.getElementById('fmetal').selectedIndex=0;document.getElementById('fgem').selectedIndex=0;document.getElementById('fbudget').value='';document.getElementById('focc').selectedIndex=0;document.getElementById('fdesc').value='';
  // Show success modal
  document.getElementById('successMod').classList.add('open');
} 
</script>
</body>
</html>
