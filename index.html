!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no, viewport-fit=cover">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="theme-color" content="#121212">
    <title>YACHA</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/galmuri@2.40.3/dist/galmuri.css">
    <style>
        :root {
            --px: "Press Start 2P", "Galmuri11", monospace;   /* 영문 픽셀 폰트 */
            --ko: "Galmuri11", "Press Start 2P", monospace;   /* 한글 픽셀 폰트 */
            box-sizing: border-box;
            padding-top: env(safe-area-inset-top, 0px);
            padding-bottom: env(safe-area-inset-bottom, 0px);
        }
        * { border-radius: 0 !important; }

        body {
            background-color: #121212;
            background-image:
                linear-gradient(45deg, #1a1a1a 25%, transparent 25%, transparent 75%, #1a1a1a 75%),
                linear-gradient(45deg, #1a1a1a 25%, transparent 25%, transparent 75%, #1a1a1a 75%);
            background-size: 16px 16px;
            background-position: 0 0, 8px 8px;
            color: #fff;
            text-align: center;
            font-family: var(--ko);
            font-weight: normal;
            margin: 0;
            padding: 20px;
            user-select: none;
        }
        b { font-weight: normal; }

        h1 {
            font-family: var(--px);
            font-weight: normal;
            font-size: 32px;
            letter-spacing: 0.15em;
            margin: 8px 0 20px 0;
            text-shadow: 4px 4px 0 #000;
        }
        .r { color: #ff4757; }
        .b { color: #1e90ff; }

        #ui-container {
            width: 100%;
            max-width: 1100px;
            margin: 0 auto 20px auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 10px;
        }
        .hp-box { width: 45%; }
        .hp-box > div:first-child {
            font-family: var(--px);
            font-weight: normal !important;
            font-size: 12px;
            margin-bottom: 8px !important;
        }
        #ui-container > div:nth-child(2) {
            font-family: var(--px) !important;
            font-weight: normal !important;
            font-size: 20px !important;
            text-shadow: 3px 3px 0 #000;
        }
        .hp-bar-bg {
            position: relative;
            width: 62%;            /* 기본 체력(100) 기준. 최대 체력이 늘면 JS가 길이를 늘림 */
            --seg: 10%;
            height: 28px;
            background: #2b2b33;
            border: 4px solid #fff;
            box-shadow: 4px 4px 0 #000;
            overflow: hidden;
            box-sizing: border-box;
        }
        .hp-bar-fill {
            height: 100%;
            width: 100%;
            transition: width 0.15s steps(4, end);
        }
        /* 체력바를 10칸 블록으로 나눔 */
        .hp-bar-bg::after {
            content: "";
            position: absolute;
            inset: 0;
            pointer-events: none;
            background-image: linear-gradient(90deg, transparent calc(100% - 3px), #000 calc(100% - 3px));
            background-size: var(--seg) 100%;
        }
        #p2-hp-bg { margin-left: auto; }
        #p1-hp { background: #ff4757; }
        #p2-hp { background: #1e90ff; float: right; }

        #p2-st-bg { margin-left: auto; }
        .st-bar-bg {
            width: 62%;
            height: 14px;
            margin-top: 8px;
            background: #2b2b33;
            border: 3px solid #fff;
            box-shadow: 3px 3px 0 #000;
            overflow: hidden;
            box-sizing: border-box;
        }
        .st-bar-fill { height: 100%; width: 100%; background: #f1c40f; }
        .st-bar-fill.low { background: #8a6d0b; }   /* 공격할 만큼 안 찼을 때 어둡게 */
        #p2-st { float: right; }

        #game-container {
            display: flex;
            justify-content: center;
            flex-wrap: nowrap;
            gap: 28px;
        }
        /* 고른 카드 아이콘: 1P는 왼쪽 화면 바깥(왼쪽), 2P는 오른쪽 화면 바깥(오른쪽) */
        .card-col { width: 40px; flex: none; display: flex; flex-direction: column; gap: 8px; align-items: flex-start; }
        .cicon {
            position: relative; width: 38px; height: 38px; flex: none;
            display: flex; align-items: center; justify-content: center;
            font-family: var(--px); font-size: 7px; color: #f1c40f;
            background: #121216; border: 3px solid #f1c40f; box-shadow: 3px 3px 0 #000;
        }
        .cicon.skill { color: #a55eea; border-color: #a55eea; }
        .cicon .n { position: absolute; right: -3px; bottom: -3px; padding: 1px 2px; font-size: 7px; color: #fff; background: #000; }

        canvas {
            background: #000;
            border: 4px solid #fff;
            box-shadow: 8px 8px 0 #000;
            width: min(540px, calc((100vw - 240px) / 2));
            height: auto;
            image-rendering: pixelated;
        }

        #start-screen {
            position: fixed;
            inset: 0;
            z-index: 10;
            background-color: #121216;
            background-image:
                linear-gradient(45deg, #1a1a20 25%, transparent 25%, transparent 75%, #1a1a20 75%),
                linear-gradient(45deg, #1a1a20 25%, transparent 25%, transparent 75%, #1a1a20 75%);
            background-size: 16px 16px;
            background-position: 0 0, 8px 8px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 22px;
        }
        #start-screen.hidden { display: none; }
        .logo {
            font-family: var(--px);
            font-size: clamp(32px, 9vw, 96px);
            letter-spacing: 0.08em;
            text-shadow: 4px 4px 0 #000, 8px 8px 0 #333;
        }
        .tagline { font-family: var(--px); color: #aaa; letter-spacing: 0.2em; font-size: 10px; }
        #startArt { image-rendering: pixelated; }
        .how { display: flex; gap: 40px; color: #ccc; font-size: 14px; line-height: 1.9; }
        .how b.p1 { color: #ff4757; font-family: var(--px); font-size: 12px; }
        .how b.p2 { color: #1e90ff; font-family: var(--px); font-size: 12px; }
        #startBtn {
            margin-top: 6px;
            padding: 14px 28px;
            font-family: var(--px);
            font-size: 16px;
            color: #fff;
            background: #121216;
            border: 4px solid #fff;
            box-shadow: 6px 6px 0 #000;
            cursor: pointer;
            animation: blink 1.1s steps(2, start) infinite;
        }
        .kr { opacity: 0.55; }   /* 메뉴 버튼의 한글 번역은 살짝 투명하게 */
        #startBtn:hover { background: #fff; color: #121216; }
        #startBtn:active { transform: translate(4px, 4px); box-shadow: 2px 2px 0 #000; }
        @keyframes blink { 50% { opacity: 0.35; } }

        .pips { display: flex; gap: 8px; margin-top: 12px; }
        .pips.r { justify-content: flex-end; }
        .pip {
            width: 18px;
            height: 18px;
            border: 3px solid #fff;
            box-shadow: 3px 3px 0 #000;
            box-sizing: border-box;
        }
        #p1-pips .pip.on { background: #ff4757; }
        #p2-pips .pip.on { background: #1e90ff; }
        #round-timer { font-size: 18px; color: #fff; margin-top: 8px; text-shadow: 3px 3px 0 #000; }
        #round-timer.dbl { color: #f1c40f; }
        #round-timer.low { color: #ff4757; }
        #round-label { font-size: 8px; color: #aaa; margin-top: 8px; text-shadow: none; white-space: nowrap; }

        #pause-screen {
            position: fixed;
            inset: 0;
            z-index: 9;
            background: rgba(0, 0, 0, 0.7);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 20px;
        }
        #pause-screen.hidden { display: none; }
        #level-screen, #match-screen { position: fixed; inset: 0; z-index: 12; background: rgba(0, 0, 0, 0.82);
            display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 22px; }
        #level-screen.hidden, #match-screen.hidden { display: none; }
        #match-rows { display: flex; flex-direction: column; gap: 10px; width: min(440px, 92vw); }
        #match-maps { display: flex; gap: 6px; padding: 4px; border: 3px solid #444; background: #121216; }
        #match-maps.sel { border-color: #f1c40f; }
        #match-maps .mtab { padding: 6px 14px; font-family: var(--ko); font-size: 16px; color: #ccc; background: #1a1a20; border: 3px solid #666; cursor: pointer; }
        #match-maps .mtab:hover { border-color: #fff; }
        #match-maps .mtab.on { color: #121216; background: #f1c40f; border-color: #f1c40f; }
        #match-view { position: relative; width: 200px; height: 120px; }
        #match-map-name { position: absolute; left: 0; right: 0; top: 0; padding: 3px 0; text-align: center; font-family: var(--ko); font-size: 15px; color: #f1c40f; background: rgba(0, 0, 0, 0.6); pointer-events: none; }
        #match-map-desc { width: min(440px, 92vw); text-align: center; font-family: var(--ko); font-size: 12px; color: #bbb; }
        #match-preview { width: 200px; height: 120px; border: 3px solid #444; background: #121216; image-rendering: pixelated; }
        .mrow { display: flex; align-items: center; gap: 8px; padding: 8px 10px; background: #121216; border: 3px solid #444; font-family: var(--ko); font-size: 16px; color: #fff; }
        .mrow.sel { border-color: #f1c40f; }
        .mrow .mnm { flex: 1; text-align: left; }
        .mrow .mnm small { display: block; font-size: 11px; color: #999; }
        .mrow .mval { min-width: 96px; text-align: center; color: #f1c40f; }
        .mrow .mbtn { padding: 4px 12px; font-family: var(--ko); font-size: 16px; color: #fff; background: #1a1a20; border: 3px solid #666; cursor: pointer; }
        .mrow .mbtn:hover { border-color: #fff; }
        #match-btns { display: flex; gap: 12px; flex-wrap: wrap; justify-content: center; max-width: 92vw; }
        #match-hint { color: #aaa; font-size: 12px; }
        /* 연습 모드: ESC 능력/설정 패널 */
        #practice-screen { position: fixed; inset: 0; z-index: 11; background: rgba(0,0,0,.85); display: flex; justify-content: center; align-items: center; padding: 12px; box-sizing: border-box; }
        #practice-screen.hidden { display: none; }
        #pr-panel { width: min(680px, 96vw); max-height: calc(100dvh - 24px); display: flex; flex-direction: column; gap: 8px; box-sizing: border-box;
            padding: 12px 14px; background: #121216; border: 4px solid #fff; box-shadow: 6px 6px 0 #000; text-align: left; }
        #pr-opts, #pr-target, #pr-foot { display: flex; flex-wrap: wrap; gap: 6px; }
        .pr-btn { padding: 7px 10px; font-family: var(--ko); font-size: 13px; color: #fff; background: #1a1a20; border: 3px solid #666; cursor: pointer; }
        .pr-btn:hover { border-color: #fff; }
        .pr-btn.on { background: #f1c40f; color: #121216; border-color: #f1c40f; }
        #pr-body { flex: 1; min-height: 0; overflow-y: auto; touch-action: pan-y; }
        .pr-item { display: flex; gap: 10px; align-items: center; padding: 7px 10px; font-size: 13px; line-height: 1.45; border-bottom: 1px solid #2a2a30; cursor: pointer; }
        .pr-item:hover { background: #1c1c24; }
        .pr-item.has { background: #1d2a1d; }
        .pr-item.dis { opacity: .4; cursor: not-allowed; }
        .pr-item .pr-nm { flex: 0 0 96px; font-weight: 700; color: var(--c); }
        .pr-item .pr-ds { flex: 1; color: #ccc; }
        .pr-item .pr-st { flex: 0 0 auto; font-size: 12px; color: #f1c40f; white-space: nowrap; }
        .pr-minus { padding: 2px 9px; font-size: 14px; color: #fff; background: #3a1a1a; border: 2px solid #ff4757; cursor: pointer; }
        #practice-hint { position: fixed; top: 6px; left: 50%; transform: translateX(-50%); z-index: 5; padding: 3px 10px; font-size: 11px; color: #f1c40f; background: rgba(0,0,0,.55); pointer-events: none; white-space: nowrap; }
        #practice-hint.hidden { display: none; }
        /* 한글을 영어 픽셀 폰트처럼 각지게: 도트가 더 큰 Galmuri9 를 9의 배수 크기로, 안티앨리어싱 없이 */
        #level-screen .pause-title, #level-screen .menu-btn, #match-screen .pause-title, #match-screen .menu-btn { font-family: "Galmuri9", "Galmuri11", monospace; -webkit-font-smoothing: none; font-smooth: never; text-rendering: optimizeSpeed; }
        #level-screen .pause-title, #match-screen .pause-title { font-size: 36px; letter-spacing: 0.1em; }
        #level-screen .menu-btn, #match-screen .menu-btn { font-size: 18px; letter-spacing: 0.05em; padding: 14px 22px; }
        #level-btns { display: flex; gap: 12px; flex-wrap: wrap; justify-content: center; max-width: 92vw; }
        .pause-title { font-family: var(--px); font-size: clamp(28px, 7vw, 64px); text-shadow: 4px 4px 0 #000; }
        .pause-sub { color: #ccc; font-size: 14px; }
        .menu-btn {
            padding: 12px 24px;
            font-family: var(--ko);
            font-size: 16px;
            color: #fff;
            background: #121216;
            border: 4px solid #fff;
            box-shadow: 6px 6px 0 #000;
            cursor: pointer;
        }
        .menu-btn:hover { background: #fff; color: #121216; }
        .menu-btn:active { transform: translate(4px, 4px); box-shadow: 2px 2px 0 #000; }

        #card-screen {
            position: fixed; inset: 0; z-index: 8;
            background: rgba(0, 0, 0, 0.78);
            display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 22px;
        }
        #card-screen.hidden { display: none; }
        #card-title { font-family: var(--px); font-size: clamp(14px, 3vw, 26px); text-shadow: 4px 4px 0 #000; }
        #card-sub { color: #ccc; font-size: 13px; }
        #card-list { display: flex; gap: 22px; flex-wrap: wrap; justify-content: center; }
        .card {
            width: 170px; padding: 18px 12px; text-align: center; cursor: pointer;
            font-family: var(--ko); color: #fff; background: #121216;
            border: 4px solid #777; box-shadow: 6px 6px 0 #000;
        }
        #card-dev { display: none; font-family: var(--px); font-size: clamp(10px, 2vw, 14px); color: #ff4d4d; text-shadow: 3px 3px 0 #000; margin-top: -10px; }
        #card-screen.dev { gap: 14px; }
        #card-screen.dev #card-list { gap: 12px; max-width: 94vw; max-height: 62vh; overflow-y: auto; padding: 8px 12px 14px; }
        #card-screen.dev .card { width: 150px; padding: 12px 8px; }
        #card-screen.dev .card .ds { font-size: 11px; line-height: 1.5; }
        .card.stat { border-color: #7a6510; }
        .card.stat .ic, .card.stat.sel { color: #f1c40f; }
        .card.skill { border-color: #5b3a8a; }
        .card.skill .ic { color: #a55eea; }
        .card.sel { transform: translate(-3px, -3px); box-shadow: 9px 9px 0 #000; outline: 3px solid #fff; outline-offset: 3px; }
        .card .ic { font-family: var(--px); font-size: 18px; margin-bottom: 12px; }
        .card .nm { font-size: 15px; margin-bottom: 8px; }
        .card .ds { font-size: 12px; color: #bbb; line-height: 1.6; }
        /* ===== 카드 등급: 똥 < 노말 < 희귀 < 레전더리 (뒤로 갈수록 화려함) ===== */
        .card { position: relative; overflow: hidden; }
        .card .rar { display: inline-block; font-family: var(--px); font-size: 9px; letter-spacing: 1px; padding: 4px 7px; margin-bottom: 10px; }
        .card.r-dung { background: #2a1d12; border: 4px dashed #7a5230; }
        .card.r-dung .rar { color: #c08a55; background: #1a110a; }
        .card.r-dung .ic { color: #8a6540; }
        .card.r-dung .nm { color: #c9a07a; }
        .card.r-dung .ds { color: #a58b70; }
        .card.r-normal { border-color: #9aa0a6; }
        .card.r-normal .rar { color: #d5d8db; background: #26262c; }
        .card.r-rare { border-color: #3498db; background: linear-gradient(160deg, #11213a, #121216 62%); box-shadow: 6px 6px 0 #000, 0 0 14px rgba(52,152,219,.55); }
        .card.r-rare .rar { color: #74b9ff; background: #0e2236; }
        .card.r-rare .ic { color: #74b9ff; }
        .card.r-rare .nm { color: #cfe8ff; }
        .card.r-epic { border-color: #b455ff; background: linear-gradient(160deg, #2a1245, #121216 62%); box-shadow: 6px 6px 0 #000, 0 0 14px rgba(180,85,255,.55); }
        .card.r-epic .rar { color: #dcb8ff; background: #230f3a; }
        .card.r-epic .ic { color: #dcb8ff; }
        .card.r-epic .nm { color: #f0e0ff; }
        .card.r-legend { border-color: #ffd700; background: linear-gradient(160deg, #3d2c00, #16120a 45%, #33200a); animation: legendPulse 1.6s ease-in-out infinite; }
        .card.r-legend .rar { color: #1a1200; background: linear-gradient(90deg, #ffd700, #fff6b0, #ffd700); background-size: 200% 100%; animation: lgShimmer 2s linear infinite; }
        .card.r-legend .ic { color: #ffd700; text-shadow: 0 0 8px #ffb300; }
        .card.r-legend .nm { font-weight: 700; color: transparent; background: linear-gradient(90deg, #ffd700, #fff, #ff9f43, #ffd700); background-size: 200% 100%; -webkit-background-clip: text; background-clip: text; animation: lgShimmer 2.4s linear infinite; }
        .card.r-legend .ds { color: #f3e3b0; }
        .card.r-legend::after { content: ''; position: absolute; top: 0; bottom: 0; left: -60%; width: 40%; background: linear-gradient(100deg, transparent, rgba(255,255,255,.4), transparent); transform: skewX(-20deg); animation: lgShine 2.6s ease-in-out infinite; pointer-events: none; }
        .card .sp { position: absolute; width: 6px; height: 6px; background: #fff3a0; box-shadow: 0 0 6px #ffd700; animation: lgTwinkle 1.4s ease-in-out infinite; pointer-events: none; }
        .card .sp.s1 { left: 10px; top: 12px; } .card .sp.s2 { right: 12px; top: 40%; animation-delay: .5s; } .card .sp.s3 { left: 22%; bottom: 10px; animation-delay: .9s; }
        @keyframes legendPulse { 0%, 100% { box-shadow: 6px 6px 0 #000, 0 0 14px rgba(255,200,0,.55), inset 0 0 14px rgba(255,200,0,.18); } 50% { box-shadow: 6px 6px 0 #000, 0 0 30px rgba(255,200,0,.95), inset 0 0 22px rgba(255,200,0,.35); } }
        @keyframes lgShimmer { to { background-position: -200% 0; } }
        @keyframes lgShine { 0% { left: -60%; } 55%, 100% { left: 130%; } }
        @keyframes lgTwinkle { 0%, 100% { opacity: .15; transform: scale(.6); } 50% { opacity: 1; transform: scale(1.2); } }
        .card.r-fusion { border-color: #9b30ff; background: linear-gradient(160deg, #2e0a52, #14081f 45%, #3d0a45); animation: fusionPulse 1.8s ease-in-out infinite; }
        .card.r-fusion .rar { color: #fff; background: linear-gradient(90deg, #7b2ff7, #e056fd, #7b2ff7); background-size: 200% 100%; animation: lgShimmer 2s linear infinite; }
        .card.r-fusion .ic { color: #d6a4ff; text-shadow: 0 0 8px #a020f0; }
        .card.r-fusion .nm { font-weight: 700; color: transparent; background: linear-gradient(90deg, #c77dff, #fff, #ff7bf5, #c77dff); background-size: 200% 100%; -webkit-background-clip: text; background-clip: text; animation: lgShimmer 2.4s linear infinite; }
        .card.r-fusion .ds { color: #e8d4ff; }
        .card.r-fusion::after { content: ''; position: absolute; top: 0; bottom: 0; left: -60%; width: 40%; background: linear-gradient(100deg, transparent, rgba(224,176,255,.4), transparent); transform: skewX(-20deg); animation: lgShine 2.6s ease-in-out infinite; pointer-events: none; }
        @keyframes fusionPulse { 0%, 100% { box-shadow: 6px 6px 0 #000, 0 0 14px rgba(155,48,255,.55), inset 0 0 14px rgba(224,86,253,.18); } 50% { box-shadow: 6px 6px 0 #000, 0 0 30px rgba(190,70,255,.95), inset 0 0 22px rgba(224,86,253,.35); } }
        .cicon.r-fusion { color: #e0b0ff; border-color: #9b30ff; box-shadow: 3px 3px 0 #000, 0 0 8px #9b30ff; }
        .cicon.r-dung { color: #c08a55; border-color: #7a5230; }
        .cicon.r-normal { color: #d5d8db; border-color: #9aa0a6; }
        .cicon.r-rare { color: #74b9ff; border-color: #3498db; }
        .cicon.r-epic { color: #dcb8ff; border-color: #b455ff; }
        .cicon.r-legend { color: #ffd700; border-color: #ffd700; box-shadow: 3px 3px 0 #000, 0 0 8px #ffd700; }
        body.touch .card .rar { font-size: 7px; padding: 3px 5px; margin-bottom: 6px; }
        .buffs { margin-top: 6px; font-size: 10px; color: #f1c40f; min-height: 12px; }
        #p2-buffs { text-align: right; }

        #skill-container { display: flex; justify-content: center; flex-wrap: nowrap; gap: 28px; margin-top: 18px; }
        .skill-box { width: min(540px, calc((100vw - 240px) / 2)); padding: 0 4px; display: flex; justify-content: center; gap: 18px; }
        .skill { display: flex; flex-direction: column; align-items: center; gap: 8px; font-family: var(--px); font-size: 10px; color: #fff; }
        .skill { cursor: pointer; touch-action: manipulation; }
        .skill canvas { width: 48px; height: 48px; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; }

        #tutBtn { margin-top: -6px; font-family: var(--px); font-size: 12px; }

        /* 튜토리얼: 설명하는 부분만 밝게, 나머지는 살짝 어둡게 */
        #tut-spot { position: fixed; z-index: 30; pointer-events: none; border: 3px solid #f1c40f;
            box-shadow: 0 0 0 9999px rgba(0, 0, 0, 0.62);
            transition: left 0.2s steps(4), top 0.2s steps(4), width 0.2s steps(4), height 0.2s steps(4); }
        #tut-box { position: fixed; z-index: 31; width: 330px; max-width: calc(100vw - 24px); box-sizing: border-box;
            padding: 16px; text-align: left; background: #121216; border: 4px solid #f1c40f; box-shadow: 6px 6px 0 #000; }
        #tut-spot.hidden, #tut-box.hidden { display: none; }
        #tut-step { font-family: var(--px); font-size: 9px; color: #888; margin-bottom: 8px; }
        #tut-title { font-family: var(--px); font-size: 13px; color: #f1c40f; margin-bottom: 10px; line-height: 1.5; }
        #tut-text { font-size: 13px; color: #ddd; line-height: 1.7; }
        #tut-keys { margin-top: 10px; }
        .tk { font-size: 13px; color: #fff; margin: 6px 0; display: flex; align-items: center; gap: 10px; }
        .kc { font-family: var(--px); font-size: 11px; min-width: 22px; padding: 6px 8px; text-align: center;
            color: #121216; background: #fff; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; }
        #tut-nav { display: flex; gap: 8px; margin-top: 14px; }
        #tut-nav .menu-btn { padding: 8px 12px; font-size: 13px; border-width: 3px; box-shadow: 4px 4px 0 #000; }
        #tut-hint { margin-top: 10px; font-size: 11px; color: #777; }

        /* 융합 연출: 재료 카드 둘이 가운데로 모여 부딪히며 번쩍 → 융합 카드가 나타남 */
        #fuse-screen { position: fixed; inset: 0; z-index: 20; background: rgba(0, 0, 0, 0.9); display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 18px; }
        #fuse-screen.hidden { display: none; }
        #fuse-title { font-family: var(--px); font-size: clamp(16px, 3vw, 26px); color: #e056fd; text-shadow: 3px 3px 0 #000; opacity: 0; animation: fuseTitle .5s steps(5) 1s forwards; }
        #fuse-stage { position: relative; width: 300px; height: 390px; }
        #fuse-stage .card { position: absolute; left: 50%; top: 50%; width: 170px; box-sizing: border-box; margin: 0; }
        #fuse-stage .fa { animation: fuseL 1.05s ease-in forwards; }
        #fuse-stage .fb { animation: fuseR 1.05s ease-in forwards; }
        #fuse-stage .fc { opacity: 0; animation: fuseIn .7s ease-out 1s forwards; }
        #fuse-flash { position: fixed; inset: 0; background: #fff; opacity: 0; pointer-events: none; animation: fuseFlash .5s ease-out 1s forwards; }
        @keyframes fuseL { 0% { transform: translate(-50%, -50%) translateX(-190px); opacity: 1; } 85% { transform: translate(-50%, -50%) translateX(-10px) scale(1.05); opacity: 1; } 100% { transform: translate(-50%, -50%) scale(.6); opacity: 0; } }
        @keyframes fuseR { 0% { transform: translate(-50%, -50%) translateX(190px); opacity: 1; } 85% { transform: translate(-50%, -50%) translateX(10px) scale(1.05); opacity: 1; } 100% { transform: translate(-50%, -50%) scale(.6); opacity: 0; } }
        @keyframes fuseIn { 0% { transform: translate(-50%, -50%) scale(.2); opacity: 0; } 60% { transform: translate(-50%, -50%) scale(1.15); opacity: 1; } 100% { transform: translate(-50%, -50%) scale(1); opacity: 1; } }
        @keyframes fuseFlash { 0% { opacity: .95; } 100% { opacity: 0; } }
        @keyframes fuseTitle { to { opacity: 1; } }

        .controls { margin-top: 24px; color: #aaa; font-size: 14px; line-height: 1.9; }
        .controls b { color: #fff; font-family: var(--px); font-size: 11px; }

        #bgmBtn.off { color: #777; border-color: #777; }
        /* ===== 모바일 / 화면 조작키 ===== */
        .vhide { display: none !important; }
        .touch-only { display: none; } body.touch .touch-only { display: inline-block; }
        body.touch .kbd-only { display: none; }
        #pause-btns { display: flex; gap: 12px; flex-wrap: wrap; justify-content: center; max-width: 92vw; }
        #pause-btns .menu-btn[data-key]::before { content: '[' attr(data-key) '] '; color: #f1c40f; }   /* 단축키 표시 */
        body.touch #pause-btns .menu-btn::before { display: none; }
        #fsHint { display: none; color: #aaa; font-size: 12px; max-width: 80vw; } #fsHint.show { display: block; }
        #pauseBtn { position: fixed; top: calc(env(safe-area-inset-top, 0px) + 8px); left: calc(env(safe-area-inset-left, 0px) + 8px); z-index: 50;
            font-family: var(--px); font-size: 10px; color: #fff; background: #121216; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; padding: 8px 10px; cursor: pointer; }
        #rematchBtn { position: fixed; left: 50%; bottom: calc(env(safe-area-inset-bottom, 0px) + 14px); transform: translateX(-50%); z-index: 7; }
        #rotate-hint { display: none; position: fixed; inset: 0; z-index: 60; background: #121216; color: #fff; align-items: center; justify-content: center; text-align: center; font-size: 18px; padding: 20px; }
        @media (orientation: landscape) { body.touch.playing:not(.focus) #rotate-hint { display: flex; } }   /* 모바일 전투는 세로 화면만 ('내 화면만 크게'를 켜면 가로도 가능) */

        #ctrl-screen { position: fixed; inset: 0; z-index: 11; background: rgba(0,0,0,.55); display: flex; justify-content: center; align-items: flex-start;
            padding-top: calc(env(safe-area-inset-top, 0px) + 8px); box-sizing: border-box; }
        #ctrl-panel { width: min(480px, 92vw); max-height: calc(100dvh - 24px); overflow-y: auto; touch-action: pan-y; box-sizing: border-box;
            padding: 12px 14px; background: #121216; border: 4px solid #fff; box-shadow: 6px 6px 0 #000; text-align: left; }
        .ct { font-family: var(--px); font-size: 13px; margin-bottom: 10px; text-align: center; }
        #cardlist-screen { position: fixed; inset: 0; z-index: 11; background: rgba(0,0,0,.88); display: flex; justify-content: center; align-items: center; padding: 12px; box-sizing: border-box; }
        #cl-panel { width: min(560px, 94vw); max-height: calc(100dvh - 24px); display: flex; flex-direction: column; gap: 10px; box-sizing: border-box;
            padding: 12px 14px; background: #121216; border: 4px solid #fff; box-shadow: 6px 6px 0 #000; text-align: left; }
        #cl-body { flex: 1; min-height: 0; overflow-y: auto; touch-action: pan-y; }
        .cl-group { margin-bottom: 12px; }
        .cl-head { padding: 6px 10px; font-size: 14px; font-weight: 700; color: var(--c); background: #1a1a20; border-left: 6px solid var(--c); }
        .cl-item { display: flex; gap: 12px; padding: 8px 10px; font-size: 13px; line-height: 1.5; border-bottom: 1px solid #2a2a30; }
        .cl-nm { flex: 0 0 96px; font-weight: 700; color: var(--c); }
        .cl-ds { color: #ccc; }
        .cl-dung { --c: #c08a55; } .cl-normal { --c: #d5d8db; } .cl-rare { --c: #74b9ff; } .cl-epic { --c: #dcb8ff; } .cl-legend { --c: #ffd700; } .cl-fusion { --c: #c77dff; }
        .cr { display: flex; align-items: center; gap: 10px; margin: 8px 0; font-size: 13px; }
        .cr > span { flex: 0 0 84px; color: #ccc; }
        .cr input[type=range] { flex: 1; min-width: 0; accent-color: #f1c40f; }
        .cr em { font-style: normal; font-family: var(--px); font-size: 9px; width: 40px; text-align: right; }
        .cr .menu-btn { flex: 1; padding: 6px 12px; font-size: 13px; border-width: 3px; box-shadow: 3px 3px 0 #000; }
        .cr .menu-btn:disabled { color: #777; border-color: #777; cursor: default; }
        .cr.cb { justify-content: center; margin-top: 12px; }
        #key-screen { position: fixed; inset: 0; z-index: 12; background: rgba(0,0,0,.6); display: flex; justify-content: center; align-items: flex-start;
            padding-top: calc(env(safe-area-inset-top, 0px) + 8px); box-sizing: border-box; }
        #key-panel { width: min(480px, 92vw); max-height: calc(100dvh - 24px); overflow-y: auto; box-sizing: border-box;
            padding: 12px 14px; background: #121216; border: 4px solid #fff; box-shadow: 6px 6px 0 #000; text-align: left; }
        #key-grid { display: grid; grid-template-columns: 1.3fr 1fr 1fr; gap: 6px; align-items: center; }
        .kg-h { font-family: var(--px); font-size: 12px; text-align: center; } .kg-h.p1 { color: #ff4757; } .kg-h.p2 { color: #1e90ff; }
        .kg-n { font-size: 13px; color: #ccc; } .kg-n small { display: block; font-size: 10px; color: #888; }
        .kg-b { font-family: var(--px); font-size: 11px; padding: 8px 4px; color: #fff; background: #1a1a20; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; cursor: pointer; min-height: 34px; }
        .kg-b:hover { background: #fff; color: #121216; }
        .kg-b.cap { background: #f1c40f; color: #121216; border-color: #f1c40f; font-family: var(--ko); font-size: 11px; }
        #key-hint { margin: 10px 0 0; font-size: 12px; color: #f1c40f; text-align: center; min-height: 16px; }
        #rot-hint { display: none; position: fixed; left: 50%; bottom: calc(env(safe-area-inset-bottom, 0px) + 10px); transform: translateX(-50%); z-index: 8; pointer-events: none;
            padding: 6px 12px; font-size: 12px; color: #fff; background: rgba(0,0,0,.7); border: 2px solid #f1c40f; }
        #rot-hint.show { display: block; }
        body.rot-ptr canvas { touch-action: none; }   /* 마우스 · 터치 회전: 화면을 밀어도 페이지가 스크롤되지 않게 */

        .vpad { position: fixed; inset: 0; z-index: 6; pointer-events: none; opacity: var(--vo, .7); }
        body.ctrl-open .vpad { z-index: 12; }
        .vp-move, .vp-act { position: absolute; bottom: calc(env(safe-area-inset-bottom, 0px) + 12px); transform: scale(var(--vs, 1)); }
        .vp-move { left: calc(env(safe-area-inset-left, 0px) + 16px); width: 140px; height: 140px; transform-origin: left bottom; }
        .vp-act { right: calc(env(safe-area-inset-right, 0px) + 16px); width: 190px; height: 160px; transform-origin: right bottom; }
        .vpad.swap .vp-move { left: auto; right: calc(env(safe-area-inset-right, 0px) + 16px); transform-origin: right bottom; }
        .vpad.swap .vp-act { right: auto; left: calc(env(safe-area-inset-left, 0px) + 16px); transform-origin: left bottom; }
        .vp-pad { position: relative; width: 140px; height: 140px; box-sizing: border-box; border: 4px solid #fff; background: rgba(18,18,22,.55);
            box-shadow: 4px 4px 0 #000; pointer-events: auto; touch-action: none; }
        .vp-pad .a { position: absolute; width: 46px; height: 46px; display: flex; align-items: center; justify-content: center; font-style: normal; font-family: var(--px); font-size: 18px; color: #888; }
        .a.u { left: 47px; top: 4px; } .a.d { left: 47px; bottom: 4px; } .a.l { left: 4px; top: 47px; } .a.r { right: 4px; top: 47px; }
        .vp-pad.u .a.u, .vp-pad.d .a.d, .vp-pad.l .a.l, .vp-pad.r .a.r { color: #f1c40f; background: rgba(241,196,15,.25); }
        .vb { position: absolute; pointer-events: auto; touch-action: none; padding: 0; font-family: var(--ko); font-size: 13px; color: #fff;
            background: rgba(18,18,22,.6); border: 3px solid #fff; box-shadow: 3px 3px 0 #000; -webkit-user-select: none; }
        .vb.on { background: #fff; color: #121216; transform: translate(2px, 2px); box-shadow: 1px 1px 0 #000; }
        .vb[data-act=attack] { right: 6px; bottom: 6px; width: 72px; height: 72px; font-size: 15px; }
        .vb[data-act=guard] { right: 88px; bottom: 0; width: 56px; height: 56px; }
        .vb[data-act=kick] { right: 0; bottom: 84px; width: 56px; height: 56px; }
        .vb[data-act=jump] { right: 70px; bottom: 80px; width: 52px; height: 52px; }
        .vb[data-act=ink] { right: 134px; bottom: 62px; width: 46px; height: 46px; font-size: 11px; }

        .vp-pad { border-radius: 50% !important; }
        .vp-knob { position: absolute; left: 38px; top: 38px; width: 56px; height: 56px; box-sizing: border-box; border-radius: 50% !important;
            background: rgba(255,255,255,.75); border: 3px solid #fff; box-shadow: 3px 3px 0 #000; pointer-events: none;
            transform: translate(var(--kx, 0px), var(--ky, 0px)); }
        /* 모바일(가로) 전체화면 레이아웃 */
        body.touch { --cw: min(calc((100vw - 110px) / 2), calc((100dvh - 160px) * 1.357));
            height: 100dvh; overflow: hidden; box-sizing: border-box; touch-action: none; overscroll-behavior: none;
            -webkit-touch-callout: none; -webkit-tap-highlight-color: transparent;
            padding: calc(env(safe-area-inset-top, 0px) + 34px) calc(env(safe-area-inset-right, 0px) + 6px) 4px calc(env(safe-area-inset-left, 0px) + 6px); }
        body.touch h1 { position: fixed; top: calc(env(safe-area-inset-top, 0px) + 8px); left: 0; right: 0; margin: 0; font-size: 14px; text-shadow: 2px 2px 0 #000; pointer-events: none; }
        body.touch .controls { display: none; }
        body.touch #ui-container { margin-bottom: 4px; gap: 6px; }
        body.touch .hp-box > div:first-child { font-size: 8px; margin-bottom: 3px !important; }
        body.touch .hp-bar-bg { height: 14px; border-width: 3px; box-shadow: 2px 2px 0 #000; }
        body.touch .st-bar-bg { height: 8px; margin-top: 4px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.touch .pips { margin-top: 5px; gap: 5px; }
        body.touch .pip { width: 10px; height: 10px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.touch .buffs { font-size: 8px; min-height: 0; margin-top: 2px; }
        body.touch #ui-container > div:nth-child(2) { font-size: 14px !important; }
        body.touch #round-timer { font-size: 12px; margin-top: 3px; }
        body.touch #round-label { font-size: 6px; margin-top: 3px; }
        body.touch #game-container { gap: 10px; }
        body.touch .card-col { width: 22px; gap: 4px; }
        body.touch .cicon { width: 22px; height: 22px; font-size: 5px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.touch #p1Canvas, body.touch #p2Canvas { width: var(--cw); border-width: 3px; box-shadow: 4px 4px 0 #000; }
        body.touch #skill-container { gap: 10px; margin-top: 8px; }
        body.touch .skill-box { width: var(--cw); gap: 12px; }
        body.touch .skill { font-size: 7px; gap: 3px; }
        body.touch .skill canvas { width: 28px; height: 28px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.touch #start-screen { gap: 8px; }
        body.touch .logo { font-size: 36px; }
        body.touch .how, body.touch .tagline { display: none; }
        body.touch #startArt { width: 150px; height: auto; }
        body.touch #startBtn { padding: 8px 18px; font-size: 13px; margin-top: 0; }
        body.touch .menu-btn { padding: 8px 16px; font-size: 14px; border-width: 3px; box-shadow: 4px 4px 0 #000; }
        body.touch #pause-screen { gap: 10px; }
        body.touch .pause-title { font-size: 30px; }
        body.touch #card-screen { gap: 10px; }
        body.touch #card-list { gap: 10px; }
        body.touch .card { width: 128px; padding: 10px 8px; }
        body.touch .card .ic { font-size: 14px; margin-bottom: 6px; }
        body.touch .card .nm { font-size: 13px; margin-bottom: 4px; }
        body.touch .card .ds { font-size: 10px; line-height: 1.4; }
        /* ===== 모바일 모드 + 2P: 폰을 가운데 두고 마주 보기 (1P는 위쪽에서 180도 돌려서) ===== */
        .vpad.rot { transform: rotate(180deg); }
        body.f2f { display: grid; grid-template-columns: 24px minmax(0, 1fr) 24px; align-content: center; gap: 4px; height: 100dvh; overflow: hidden; box-sizing: border-box;
            padding: calc(max(env(safe-area-inset-top, 0px), env(safe-area-inset-bottom, 0px)) + 4px) calc(env(safe-area-inset-right, 0px) + 6px) calc(max(env(safe-area-inset-top, 0px), env(safe-area-inset-bottom, 0px)) + 4px) calc(env(safe-area-inset-left, 0px) + 6px);
            margin-top: calc(-1 * env(safe-area-inset-top, 0px)); margin-bottom: calc(-1 * env(safe-area-inset-bottom, 0px)); }   /* :root 가 이미 안전영역 패딩을 줬으므로 겹치지 않게 상쇄하고, 위·아래 여백을 같게 해서 1P/2P 가 화면 가운데 기준으로 대칭이 되게 함 */
        body.f2f h1, body.f2f .controls { display: none; }
        body.f2f #ui-container, body.f2f #game-container, body.f2f #skill-container { display: contents; }
        body.f2f .skill-box { width: auto; }
        body.f2f .hp-box { width: auto; }
        body.f2f .card-col { width: 24px; align-self: center; }
        body.f2f .cicon { width: 22px; height: 22px; font-size: 5px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.f2f #p1-skills { grid-area: 1 / 2; transform: rotate(180deg); }
        body.f2f #p1-cards { grid-area: 2 / 1; transform: rotate(180deg); }
        body.f2f #p1Canvas { grid-area: 2 / 2; transform: rotate(180deg); }
        body.f2f #ui-container > .hp-box:nth-child(1) { grid-area: 3 / 1 / 4 / 4; transform: rotate(180deg); }
        body.f2f #ui-container > div:nth-child(2) { grid-area: 4 / 1 / 5 / 4; display: flex; justify-content: center; align-items: center; gap: 12px; }
        body.f2f #ui-container > .hp-box:nth-child(3) { grid-area: 5 / 1 / 6 / 4; }
        body.f2f #p2Canvas { grid-area: 6 / 2; }
        body.f2f #p2-cards { grid-area: 6 / 3; }
        body.f2f #p2-skills { grid-area: 7 / 2; }
        body.f2f #p1Canvas, body.f2f #p2Canvas { width: min(100%, calc((100dvh - 300px) / 2 * 1.357)); height: auto; justify-self: center; }
        body.f2f #pauseBtn { top: 50%; transform: translateY(-50%); }
        body.f2f #pauseBtn { left: calc(env(safe-area-inset-left, 0px) + 8px); }
        body.f2f #rematchBtn { top: 50%; bottom: auto; transform: translate(-50%, -50%); }
        /* 모바일 1인용: 세로 화면에 위(1P) · 아래(2P)로 쌓기 */
        body.ptsolo { display: grid; grid-template-columns: 24px minmax(0, 1fr) 24px; align-content: center; gap: 4px; height: 100dvh; overflow: hidden; box-sizing: border-box;
            padding: calc(max(env(safe-area-inset-top, 0px), env(safe-area-inset-bottom, 0px)) + 4px) calc(env(safe-area-inset-right, 0px) + 6px) calc(max(env(safe-area-inset-top, 0px), env(safe-area-inset-bottom, 0px)) + 4px) calc(env(safe-area-inset-left, 0px) + 6px);
            margin-top: calc(-1 * env(safe-area-inset-top, 0px)); margin-bottom: calc(-1 * env(safe-area-inset-bottom, 0px)); }   /* :root 가 이미 안전영역 패딩을 줬으므로 겹치지 않게 상쇄하고, 위·아래 여백을 같게 해서 1P/2P 가 화면 가운데 기준으로 대칭이 되게 함 */
        body.ptsolo h1, body.ptsolo .controls { display: none; }
        body.ptsolo #ui-container, body.ptsolo #game-container, body.ptsolo #skill-container { display: contents; }
        body.ptsolo .skill-box { width: auto; }
        body.ptsolo .hp-box { width: auto; }
        body.ptsolo .card-col { width: 24px; align-self: center; }
        body.ptsolo .cicon { width: 22px; height: 22px; font-size: 5px; border-width: 2px; box-shadow: 2px 2px 0 #000; }
        body.ptsolo #p1-skills { grid-area: 1 / 2; }
        body.ptsolo #p1-cards { grid-area: 2 / 1; }
        body.ptsolo #p1Canvas { grid-area: 2 / 2; }
        body.ptsolo #ui-container > .hp-box:nth-child(1) { grid-area: 3 / 1 / 4 / 4; }
        body.ptsolo #ui-container > div:nth-child(2) { grid-area: 4 / 1 / 5 / 4; display: flex; justify-content: center; align-items: center; gap: 12px; }
        body.ptsolo #ui-container > .hp-box:nth-child(3) { grid-area: 5 / 1 / 6 / 4; }
        body.ptsolo #p2Canvas { grid-area: 6 / 2; }
        body.ptsolo #p2-cards { grid-area: 6 / 3; }
        body.ptsolo #p2-skills { grid-area: 7 / 2; }
        body.ptsolo #p1Canvas, body.ptsolo #p2Canvas { width: min(100%, calc((100dvh - 300px) / 2 * 1.357)); height: auto; justify-self: center; }
        body.ptsolo #pauseBtn { top: 50%; transform: translateY(-50%); }
        body.ptsolo #pauseBtn { left: calc(env(safe-area-inset-left, 0px) + 8px); }
        body.ptsolo #rematchBtn { top: 50%; bottom: auto; transform: translate(-50%, -50%); }
        /* 모바일 혼자 할 때: 내가 1P이면 1P/2P 자리를 맞바꿔서 내 화면이 아래로 옴 */
        body.ptsolo.me1 #p1-skills { grid-area: 7 / 2; }
        body.ptsolo.me1 #p1-cards { grid-area: 6 / 1; }
        body.ptsolo.me1 #p1Canvas { grid-area: 6 / 2; }
        body.ptsolo.me1 #ui-container > .hp-box:nth-child(1) { grid-area: 5 / 1 / 6 / 4; }
        body.ptsolo.me1 #ui-container > .hp-box:nth-child(3) { grid-area: 3 / 1 / 4 / 4; }
        body.ptsolo.me1 #p2Canvas { grid-area: 2 / 2; }
        body.ptsolo.me1 #p2-cards { grid-area: 2 / 3; }
        body.ptsolo.me1 #p2-skills { grid-area: 1 / 2; }
        body.f2f.pick1 #card-screen { transform: rotate(180deg); }
        /* 모바일 세로: 카드를 고르는 동안 조작키(방향키 · 공격)와 일시정지 버튼에 카드가 가려지지 않게, 카드를 한 줄로 줄여 조작키 위쪽에 둠 */
        @media (orientation: portrait) {
            body.touch.picking-pad:not(.f2f) #card-screen { padding-bottom: calc(env(safe-area-inset-bottom, 0px) + 28px + 160px * var(--vs, 1)); box-sizing: border-box; }
            body.touch.picking-pad:not(.f2f) #card-list { flex-wrap: nowrap; gap: 6px; width: 100%; padding: 0 6px; box-sizing: border-box; }
            body.touch.picking-pad:not(.f2f) .card { flex: 0 1 calc((100vw - 24px) / 3); min-width: 0; width: auto; box-sizing: border-box; padding: 10px 4px; }
            body.touch.picking-pad:not(.f2f) #pauseBtn { top: calc(env(safe-area-inset-top, 0px) + 8px); transform: none; }
        }

        /* 조작키 설정창 · 카드 목록: 화면 조작키(버튼)에 안 가리게 남는 공간의 가운데에 배치 */
        body.pad-on #ctrl-screen { align-items: center; padding: calc(env(safe-area-inset-top, 0px) + 8px) 8px calc(env(safe-area-inset-bottom, 0px) + 28px + 160px * var(--vs, 1)); }
        body.pad-on.f2f #ctrl-screen { padding-top: calc(env(safe-area-inset-top, 0px) + 28px + 160px * var(--vs, 1)); }
        body.pad-on #ctrl-panel { max-height: 100%; }
        body.pad-on.cl-open #cardlist-screen { padding: calc(env(safe-area-inset-top, 0px) + 8px) 8px calc(env(safe-area-inset-bottom, 0px) + 28px + 160px * var(--vs, 1)); }
        body.pad-on.cl-open #cl-panel { max-height: 100%; }
        body.pr-open .vpad { opacity: calc(var(--vo, .7) * .55); }
        body.pr-open .vp-move { bottom: calc(env(safe-area-inset-bottom, 0px) + 72px); }   /* 맨 아래 '계속하기' 줄을 가리지 않게 방향키를 위로 */   /* 연습 능력 목록: 목록은 원래 크기 그대로 두고 방향키만 더 투명하게 */
        body.cl-open .vpad, body.pr-open .vpad, body.picking-pad .vpad { z-index: 12; }
        body.picking-pad .vb:not([data-act=attack]) { display: none; }   /* 카드 고를 땐 방향키 + 공격(선택)만 */
        body.cl-open .vp-act, body.pr-open .vp-act { display: none; }   /* 카드 목록 · 연습 능력 목록에선 방향키만 */
        /* 방향키: 십자(+) 모양 */
        .vpad .vp-pad { border: 0; background: transparent; box-shadow: none; border-radius: 0 !important; }
        .vpad .vp-pad .a, .vpad .vp-pad .vp-knob { position: absolute; width: 46px; height: 46px; box-sizing: border-box; border: 3px solid #fff; background: rgba(18,18,22,.6);
            box-shadow: 3px 3px 0 #000; color: #aaa; font-size: 16px; transform: none; border-radius: 0 !important; }
        .vpad .vp-pad .vp-knob { left: 47px; top: 47px; }
        .vpad .vp-pad .a.u { left: 47px; top: 0; bottom: auto; } .vpad .vp-pad .a.d { left: 47px; top: 94px; bottom: auto; }
        .vpad .vp-pad .a.l { left: 0; top: 47px; right: auto; } .vpad .vp-pad .a.r { left: 94px; top: 47px; right: auto; }
        .vpad .vp-pad.u .a.u, .vpad .vp-pad.d .a.d, .vpad .vp-pad.l .a.l, .vpad .vp-pad.r .a.r { color: #121216; background: #f1c40f; border-color: #f1c40f; }
        /* ===== 멀티플레이: 플레이어 찾는 중 화면 ===== */
        #mm-screen { position: fixed; inset: 0; z-index: 80; background: rgba(0,0,0,.88); display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 22px; padding: 20px; box-sizing: border-box; }
        #mm-screen.hidden { display: none; }
        #mm-title { font-family: var(--ko); font-size: 30px; letter-spacing: 0.08em; text-shadow: 4px 4px 0 #000; }
        #mm-sub { max-width: min(460px, 90vw); color: #bbb; font-size: 13px; line-height: 1.7; white-space: pre-line; }
        #mm-dots { display: flex; gap: 12px; }
        #mm-dots i { width: 16px; height: 16px; background: #f1c40f; box-shadow: 3px 3px 0 #000; animation: mmdot 1.2s steps(2, start) infinite; }
        #mm-dots i:nth-child(2) { animation-delay: .2s; } #mm-dots i:nth-child(3) { animation-delay: .4s; }
        #mm-dots.off { display: none; }
        #gearBtn { position: fixed; top: calc(env(safe-area-inset-top, 0px) + 8px); right: calc(env(safe-area-inset-right, 0px) + 8px); z-index: 50; width: 44px; height: 44px; padding: 0; font-size: 26px; line-height: 1; color: #fff; background: #121216; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; cursor: pointer; }
        #gearBtn:hover { background: #fff; color: #121216; }
        #pause-screen.startmenu { z-index: 11; }
        #pause-screen.startmenu .menu-btn::before { display: none; }   /* 처음 화면 설정 메뉴에서는 숫자 단축키 없음 */
        /* 고른 카드만 크게 */
        #card-screen.showpick #card-sub, #card-screen.showpick #card-dev { visibility: hidden; }
        .card.picked { animation: pickpop .35s ease-out forwards; z-index: 2; }
        @keyframes pickpop { from { transform: scale(1); } to { transform: scale(1.8); } }
        body.touch .card.picked { animation-name: pickpop2; } @keyframes pickpop2 { from { transform: scale(1); } to { transform: scale(1.5); } }
        /* 시작 화면 버튼이 하나 늘어서 낮은 화면에서 로고가 잘리지 않게: 넘치면 스크롤, 간격은 살짝 좁힘 */
        #start-screen { justify-content: flex-start; overflow-y: auto; }
        #start-screen > :first-child { margin-top: auto; }
        #start-screen > :last-child { margin-bottom: auto; }
        @media (max-height: 960px) { #start-screen { gap: 12px; } }
        /* ===== 채팅 (온라인 대전) ===== */
        #chat-log, #chatBtn, #chat-box { display: none; }
        body.online #chat-log { display: block; }
        body.online #chatBtn { display: block; }
        body.online #chat-box:not(.hidden) { display: flex; }
        #chat-log { position: fixed; left: calc(env(safe-area-inset-left, 0px) + 10px); bottom: calc(env(safe-area-inset-bottom, 0px) + 10px); z-index: 70; width: min(640px, 92vw); text-align: left; font-family: var(--ko); font-size: clamp(20px, 2.4vw, 30px); line-height: 1.4; pointer-events: none; }
        #chat-log > div { margin-top: 4px; padding: 4px 12px; background: rgba(0,0,0,.65); word-break: break-all; user-select: text; }
        body.touch #chat-log { bottom: calc(env(safe-area-inset-bottom, 0px) + 190px); }
        #chatBtn { position: fixed; top: calc(env(safe-area-inset-top, 0px) + 8px); right: calc(env(safe-area-inset-right, 0px) + 8px); z-index: 50; font-size: 16px; background: #121216; border: 3px solid #fff; box-shadow: 3px 3px 0 #000; padding: 4px 8px; cursor: pointer; }
        #chat-box { position: fixed; left: 50%; bottom: calc(env(safe-area-inset-bottom, 0px) + 60px); transform: translateX(-50%); z-index: 90; gap: 8px; width: min(520px, 94vw); }
        body.touch #chat-box { bottom: auto; top: calc(env(safe-area-inset-top, 0px) + 50px); }
        #chat-input { flex: 1; min-width: 0; padding: 10px 12px; font-family: var(--ko); font-size: 22px; color: #fff; background: #121216; border: 4px solid #fff; box-shadow: 4px 4px 0 #000; outline: none; user-select: text; -webkit-user-select: text; }
        #chat-input:focus { border-color: #f1c40f; }
        #chat-send { padding: 8px 14px; font-size: 14px; }
        /* ===== 내 화면만 크게 ===== */
        body.focus-p1 #p2Canvas, body.focus-p2 #p1Canvas, body.focus-p1 #p2-skills, body.focus-p2 #p1-skills { display: none; }
        body.focus #p1Canvas, body.focus #p2Canvas { width: min(980px, calc(100vw - 240px), calc((100vh - 340px) * 1.357)); }
        body.focus .skill-box { width: auto; }
        body.ptsolo.focus #p1Canvas, body.ptsolo.focus #p2Canvas { width: min(100%, calc((100dvh - 230px) * 1.357)); }
        /* 모바일 가로: 내 화면을 가운데에 높이 가득 크게, 체력바·카드·기술 아이콘은 양옆 빈 곳에 (조작키는 양옆 아래 모서리) */
        @media (orientation: landscape) {
            body.touch.ptsolo.focus { grid-template-columns: minmax(0, 1fr) auto minmax(0, 1fr); grid-template-rows: auto auto 1fr; align-content: stretch; column-gap: 8px; row-gap: 4px; }
            body.touch.ptsolo.focus #p1Canvas, body.touch.ptsolo.focus #p2Canvas { grid-area: 1 / 2 / 4 / 3; align-self: center; width: min(calc((100dvh - 12px) * 1.357), calc(100vw - 280px)); }
            body.touch.ptsolo.focus #ui-container > .hp-box:nth-child(1) { grid-area: 1 / 1; margin-top: 40px; }
            body.touch.ptsolo.focus #ui-container > .hp-box:nth-child(3) { grid-area: 1 / 3; margin-top: 40px; }
            body.touch.ptsolo.focus #ui-container > div:nth-child(2) { grid-area: 1 / 2; align-self: start; justify-self: center; z-index: 2; padding: 0 8px; background: rgba(0, 0, 0, .5); pointer-events: none; }
            body.touch.ptsolo.focus #p1-cards { grid-area: 2 / 1; width: auto; flex-direction: row; flex-wrap: wrap; align-self: start; justify-self: start; }
            body.touch.ptsolo.focus #p2-cards { grid-area: 2 / 3; width: auto; flex-direction: row; flex-wrap: wrap; justify-content: flex-end; align-self: start; justify-self: end; }
            body.touch.ptsolo.focus #p1-skills { grid-area: 3 / 1; align-self: start; justify-self: start; }
            body.touch.ptsolo.focus #p2-skills { grid-area: 3 / 3; align-self: start; justify-self: end; }
            body.touch.ptsolo.focus #pauseBtn { top: calc(env(safe-area-inset-top, 0px) + 4px); transform: none; }
        }
        @keyframes mmdot { 0%, 100% { opacity: 1; } 50% { opacity: .2; } }
    </style>
</head>
<body>
    <div id="pause-screen" class="hidden">
        <div class="pause-title">PAUSED</div>
        <div class="pause-sub kbd-only">ESC 를 눌러 계속하기</div>
        <div id="pause-btns">
            <button id="resumeBtn" class="menu-btn" data-key="1">계속하기</button>
            <button id="cardsBtn" class="menu-btn" data-key="2">카드 목록</button>
            <button id="ctrlBtn" class="menu-btn" data-key="3">조작키 설정</button>
            <button id="fsBtn" class="menu-btn touch-only">전체화면</button>
            <button id="viewBtn" class="menu-btn" style="display:none">내 화면만 크게: OFF</button>
            <button id="bgmBtn" class="menu-btn" data-key="4">♪ SOUND ON</button>
            <button id="homeBtn" class="menu-btn" data-key="5">처음 화면으로</button>
        </div>
        <div id="fsHint">iPhone: 공유 버튼 → "홈 화면에 추가"로 실행하면 전체화면이 돼요</div>
    </div>

    <div id="cardlist-screen" class="vhide">
        <div id="cl-panel">
            <div class="ct">카드 목록</div>
            <div id="cl-body"></div>
            <button id="clClose" class="menu-btn">닫기</button>
        </div>
    </div>

    <div id="card-screen" class="hidden">
        <div id="card-title"></div>
        <div id="card-dev">★ 개발자 모드 ★</div>
        <div id="card-sub"></div>
        <div id="card-list"></div>
    </div>
    <div id="fuse-screen" class="hidden"></div>

    <div id="start-screen">
        <div class="logo"><span class="r">YA</span><span class="b">CHA</span></div>
        <div class="tagline">2P FIRST-PERSON BRAWL</div>
        <canvas id="startArt" width="360" height="192"></canvas>
        <div class="how">
            <div><b class="p1">1P</b><br><span id="how1">WASD 이동/회전<br>Z 공격 · X 가드 · C 발차기</span></div>
            <div><b class="p2">2P</b><br><span id="how2">방향키 이동/회전<br>. 공격 · / 가드 · ' 발차기</span></div>
        </div>
        <button id="startBtn">START<span class="kr">(2플레이어)</span> [ENTER]</button>
        <button id="soloBtn" class="menu-btn">SINGLE PLAY<span class="kr">(1인 대전)</span> [1]</button>
        <button id="multiBtn" class="menu-btn">MULTIPLAY<span class="kr">(온라인 대전)</span> [3]</button>
        <button id="practiceBtn" class="menu-btn">PRACTICE<span class="kr">(연습)</span> [2]</button>
        <button id="tutBtn" class="menu-btn">TUTORIAL<span class="kr">(튜토리얼)</span> [T]</button>
    </div>

    <div id="chat-log"></div>
    <div id="chat-box" class="hidden"><input id="chat-input" maxlength="80" autocomplete="off" placeholder="메시지 입력 · Enter 전송 · ESC 취소"><button id="chat-send" class="menu-btn">전송</button></div>
    <button id="chatBtn" title="채팅 (T)">💬</button>
    <button id="gearBtn" class="vhide" title="설정 (ESC)">⚙</button>
    <div id="mm-screen" class="hidden">
        <div class="pause-title" id="mm-title"></div>
        <div id="mm-dots"><i></i><i></i><i></i></div>
        <div id="mm-sub"></div>
        <button id="mm-cancel" class="menu-btn">취소 [ESC]</button>
    </div>
    <div id="practice-hint" class="hidden">PRACTICE · ESC 능력/설정 · R 위치 초기화</div>
    <div id="practice-screen" class="hidden">
        <div id="pr-panel">
            <div class="ct">PRACTICE · 연습 모드</div>
            <div id="pr-opts"></div>
            <div id="pr-target"></div>
            <div id="pr-body"></div>
            <div id="pr-foot"></div>
        </div>
    </div>

    <div id="level-screen" class="hidden">
        <div class="pause-title">난이도 선택</div>
        <div id="level-btns">
            <button class="menu-btn solo-btn" data-level="easy">애기모드 [1]</button>
            <button class="menu-btn solo-btn" data-level="normal">노멀모드 [2]</button>
            <button class="menu-btn solo-btn" data-level="hard">하드모드 [3]</button>
        </div>
        <button id="levelBack" class="menu-btn">뒤로 [ESC]</button>
    </div>

    <div id="match-screen" class="hidden">
        <div class="pause-title">경기 설정</div>
        <div id="match-maps"></div>
        <div id="match-view"><canvas id="match-preview" width="200" height="120"></canvas><div id="match-map-name"></div></div>
        <div id="match-map-desc"></div>
        <div id="match-rows"></div>
        <div id="match-hint" class="kbd-only">↑↓ 항목 선택 · ←→ 값 변경 · ENTER 시작</div>
        <div id="match-btns">
            <button id="matchGo" class="menu-btn">시작 [ENTER]</button>
            <button id="matchReset" class="menu-btn">기본값</button>
            <button id="matchBack" class="menu-btn">뒤로 [ESC]</button>
        </div>
    </div>

    <h1><span class="r">YA</span><span class="b">CHA</span></h1>

    <div id="ui-container">
        <div class="hp-box">
            <div style="text-align: left; font-weight: bold; color: #ff4757; margin-bottom: 4px;">PLAYER 1</div>
            <div class="hp-bar-bg" id="p1-hp-bg"><div id="p1-hp" class="hp-bar-fill"></div></div>
            <div class="st-bar-bg" id="p1-st-bg"><div id="p1-st" class="st-bar-fill"></div></div>
            <div class="pips" id="p1-pips"><span class="pip"></span><span class="pip"></span><span class="pip"></span></div>
            <div class="buffs" id="p1-buffs"></div>
        </div>
        <div style="font-size: 24px; font-weight: bold; color: #f1c40f;">VS<div id="round-label">ROUND 1</div><div id="round-timer">40</div></div>
        <div class="hp-box">
            <div style="text-align: right; font-weight: bold; color: #1e90ff; margin-bottom: 4px;">PLAYER 2</div>
            <div class="hp-bar-bg" id="p2-hp-bg"><div id="p2-hp" class="hp-bar-fill"></div></div>
            <div class="st-bar-bg" id="p2-st-bg"><div id="p2-st" class="st-bar-fill"></div></div>
            <div class="pips r" id="p2-pips"><span class="pip"></span><span class="pip"></span><span class="pip"></span></div>
            <div class="buffs" id="p2-buffs"></div>
        </div>
    </div>

    <div id="game-container">
        <div class="card-col" id="p1-cards"></div>
        <canvas id="p1Canvas" width="380" height="280"></canvas>
        <canvas id="p2Canvas" width="380" height="280"></canvas>
        <div class="card-col r" id="p2-cards"></div>
    </div>

    <div id="skill-container">
        <div class="skill-box" id="p1-skills"></div>
        <div class="skill-box" id="p2-skills"></div>
    </div>

    <div class="controls">
        <span id="ft1"><b>1P:</b> WASD (이동/회전) | <b>Z</b> (공격) | <b>X</b> (가드) | <b>C</b> (발차기) | <b>V</b> (특수)</span> &nbsp;&nbsp;&nbsp;&nbsp;
        <span id="ft2"><b>2P:</b> 방향키 (이동/회전) | <b>.</b> (공격) | <b>/</b> (가드) | <b>'</b> (발차기) | <b>;</b> (특수)</span><br>
        <b>ESC</b>: 일시정지 &nbsp;&nbsp;&nbsp;&nbsp; <b>M</b>: 사운드 켜기/끄기 &nbsp;&nbsp;&nbsp;&nbsp; KO 후 3초 뒤 자동으로 다음 라운드 · 3라운드 먼저 이기면 승리
    </div>

    <div id="tut-spot" class="hidden"></div>
    <div id="tut-box" class="hidden">
        <div id="tut-step"></div>
        <div id="tut-title"></div>
        <div id="tut-text"></div>
        <div id="tut-keys"></div>
        <div id="tut-nav">
            <button id="tutPrev" class="menu-btn">이전</button>
            <button id="tutNext" class="menu-btn">다음</button>
            <button id="tutExit" class="menu-btn">종료</button>
        </div>
        <div id="tut-hint">Enter 다음 · Backspace 이전 · ESC 종료</div>
    </div>

    <button id="pauseBtn" class="vhide">II</button>
    <button id="rematchBtn" class="menu-btn vhide">▶ 새 경기</button>
    <div id="rotate-hint">세로 화면으로 돌려주세요 ↻</div>

    <div id="vpad" class="vpad vhide">
        <div class="vp-move"><div class="vp-pad"><i class="a u">▲</i><i class="a d">▼</i><i class="a l">◀</i><i class="a r">▶</i><i class="vp-knob"></i></div></div>
        <div class="vp-act">
            <button class="vb" data-act="attack">공격</button>
            <button class="vb" data-act="guard">가드</button>
            <button class="vb" data-act="kick">킥</button>
            <button class="vb vb-jump vhide" data-act="jump">점프</button>
            <button class="vb vb-ink vhide" data-act="ink">먹물</button>
        </div>
    </div>

    <div id="ctrl-screen" class="vhide">
        <div id="ctrl-panel">
            <div class="ct">조작키 설정</div>
            <div class="cr"><span>모바일 모드</span><button id="cOn" class="menu-btn"></button></div>
            <div class="cr"><span>크기</span><input id="cScale" type="range" min="50" max="150" step="5"><em id="cScaleV"></em></div>
            <div class="cr"><span>투명도</span><input id="cOpa" type="range" min="20" max="100" step="5"><em id="cOpaV"></em></div>
            <div class="cr"><span>방향키 위치</span><button id="cSwap" class="menu-btn"></button></div>
            <div class="cr"><span>조작 대상</span><button id="cPlayer" class="menu-btn"></button></div>
            <div class="cr"><span>회전 (1인용)</span><button id="cRot" class="menu-btn"></button></div>
            <div class="cr kbd-only"><span>키보드</span><button id="cKeys" class="menu-btn">키 설정</button></div>
            <div class="cr cb"><button id="cReset" class="menu-btn">초기화</button><button id="cClose" class="menu-btn">닫기</button></div>
        </div>
    </div>

    <div id="key-screen" class="vhide">
        <div id="key-panel">
            <div class="ct">키보드 설정</div>
            <div id="key-grid"></div>
            <div id="key-hint"></div>
            <div class="cr cb"><button id="kReset" class="menu-btn">초기화</button><button id="kClose" class="menu-btn">닫기</button></div>
        </div>
    </div>
    <div id="rot-hint">화면을 클릭하면 마우스로 회전해요 · ESC: 일시정지</div>

    <script>
        // ===== 키보드 키 설정 + 1인용 마우스 · 터치 회전 =====
        // 키 설정: 진짜 키보드 입력을 게임이 원래 쓰는 키(P1_KEYS / P2_KEYS)로 바꿔서 다시 보냄 → 게임 · 온라인 중계 코드는 그대로.
        // (NET 리스너보다 먼저 등록돼야 해서 이 스크립트가 맨 앞에 있음)
        const YK = (() => {
            const $ = id => document.getElementById(id);
            const ACTS = ['up', 'down', 'left', 'right', 'attack', 'guard', 'kick', 'ink'];
            const NAMES = { up: '앞으로', down: '뒤로', left: '왼쪽 회전', right: '오른쪽 회전', attack: '공격', guard: '가드', kick: '발차기', ink: '특수공격' };
            const KEY_OK = /^(Key[A-Z]|Arrow(Up|Down|Left|Right)|Period|Comma|Slash|Backslash|Semicolon|Quote|BracketLeft|BracketRight|Minus|Equal|Backquote)$/;
            const KEY_BAN = new Set(['KeyT', 'KeyM', 'KeyR']);   // T 채팅 · 튜토리얼 / M 음소거 / R 다시하기 에 이미 쓰임
            const SHOW = { Period: '.', Comma: ',', Slash: '/', Backslash: '\\', Semicolon: ';', Quote: "'", BracketLeft: '[', BracketRight: ']', Minus: '-', Equal: '=', Backquote: '`', ArrowUp: '↑', ArrowDown: '↓', ArrowLeft: '←', ArrowRight: '→' };
            const label = c => SHOW[c] || c.replace(/^Key/, '');
            const okKey = c => KEY_OK.test(c) && !KEY_BAN.has(c);
            const SAVE_KEYS = 'yacha-keys', SAVE_ROT = 'yacha-rot';
            let DEF = null, U = null, toCanon = {}, defCodes = new Set();
            let rotMode = 'key', pending = 0, lockOwn = false, touchId = null, lastX = 0, cap = null;
            try { if (localStorage.getItem(SAVE_ROT) === 'pointer') rotMode = 'pointer'; } catch (_) {}

            function rebuild() {
                toCanon = {};
                for (const s of [1, 2]) for (const a of ACTS) toCanon[U[s][a]] = DEF[s][a];
            }
            function loadKeys() {
                U = { 1: { ...DEF[1] }, 2: { ...DEF[2] } };
                try {
                    const o = JSON.parse(localStorage.getItem(SAVE_KEYS) || 'null');
                    if (o) {
                        const T = { 1: { ...DEF[1] }, 2: { ...DEF[2] } }, seen = new Set();
                        let good = true;
                        for (const s of [1, 2]) for (const a of ACTS) {
                            const c = o[s] && o[s][a];
                            if (!okKey(c) || seen.has(c)) { good = false; break; }   // 깨졌거나 겹치면 통째로 기본값
                            seen.add(c); T[s][a] = c;
                        }
                        if (good) U = T;
                    }
                } catch (_) {}
                rebuild();
            }
            const saveKeys = () => { try { localStorage.setItem(SAVE_KEYS, JSON.stringify(U)); } catch (_) {} };
            const inPlay = () => { try { return started && !paused; } catch (_) { return false; } };

            // ----- 키 입력 바꿔 보내기 -----
            let redisp = false;
            function onKey(e) {
                if (redisp || !e.isTrusted || !DEF) return;   // 화면 조작키 · 온라인 중계가 만든 가짜 이벤트는 그대로 통과
                if (cap) {   // 키 설정창: 새 키 입력 받는 중
                    e.preventDefault(); e.stopImmediatePropagation();
                    if (e.type !== 'keydown' || e.repeat) return;
                    if (e.code === 'Escape') { cap = null; render('취소했어요'); return; }
                    if (!okKey(e.code)) { render(KEY_BAN.has(e.code) ? '이미 다른 기능에 쓰는 키예요 (T · M · R)' : '글자 · 방향키 · 기호 키만 쓸 수 있어요'); return; }
                    assign(cap.s, cap.a, e.code); cap = null; render('바꿨어요'); return;
                }
                if (keyOpen()) {   // 설정창이 열려 있는 동안: ESC = 설정창만 닫기, 나머지 키는 막음 (일시정지 메뉴 숫자 단축키 방지)
                    e.preventDefault(); e.stopImmediatePropagation();
                    if (e.type === 'keydown' && e.code === 'Escape') closeKeys();
                    return;
                }
                const t = e.target;
                if (t && t.closest && t.closest('input,textarea,select,[contenteditable]')) return;   // 채팅 입력 중
                const c = toCanon[e.code], down = e.type === 'keydown';
                if (c === undefined) {   // 어디에도 지정되지 않은 키: 게임 중이면 원래 기본 키도 더는 동작하지 않게 막음
                    if (down && inPlay() && defCodes.has(e.code)) { e.preventDefault(); e.stopImmediatePropagation(); }
                    return;
                }
                if (c === e.code || (down && !inPlay())) return;   // 기본 키 그대로이거나, 메뉴 화면에선 원래 키 그대로
                e.preventDefault(); e.stopImmediatePropagation();
                redisp = true;
                try { window.dispatchEvent(new KeyboardEvent(e.type, { code: c, key: c, repeat: e.repeat, bubbles: true, cancelable: true })); }
                finally { redisp = false; }
            }
            for (const t of ['keydown', 'keyup']) window.addEventListener(t, onKey, true);

            // ----- 키 설정창 -----
            const keyOpen = () => { const el = $('key-screen'); return !!el && !el.classList.contains('vhide'); };
            function assign(s, a, code) {
                let hs = 0, ha = '';
                for (const s2 of [1, 2]) for (const a2 of ACTS) if (U[s2][a2] === code) { hs = s2; ha = a2; }
                if (hs) U[hs][ha] = U[s][a];   // 이미 쓰고 있던 칸과는 서로 맞바꿈
                U[s][a] = code;
                rebuild(); saveKeys(); texts();
            }
            function render(msg) {
                const g = $('key-grid'); if (!g) return;
                let h = '<div></div><div class="kg-h p1">1P</div><div class="kg-h p2">2P</div>';
                for (const a of ACTS) {
                    let nm = NAMES[a];
                    if ((a === 'left' || a === 'right') && rotMode === 'pointer') nm += '<small>(1인용은 이동)</small>';
                    h += '<div class="kg-n">' + nm + '</div>';
                    for (const s of [1, 2]) {
                        const on = cap && cap.s === s && cap.a === a;
                        h += '<button class="kg-b' + (on ? ' cap' : '') + '" data-s="' + s + '" data-a="' + a + '">' + (on ? '키를 누르세요' : label(U[s][a])) + '</button>';
                    }
                }
                g.innerHTML = h;
                $('key-hint').textContent = msg || '바꿀 칸을 누른 뒤 새 키를 누르세요 (ESC: 취소)';
            }
            function openKeys() { cap = null; render(); $('key-screen').classList.remove('vhide'); }
            function closeKeys() { cap = null; $('key-screen').classList.add('vhide'); }

            // 시작 화면 · 하단 안내 문구를 지금 키에 맞춰 다시 씀
            function texts() {
                const mv = s => { const u = U[s]; const four = [u.up, u.left, u.down, u.right]; return four.every(c => c.startsWith('Arrow')) && new Set(four).size === 4 ? '방향키' : four.map(label).join(''); };
                const how = s => { const u = U[s]; return mv(s) + ' 이동/회전<br>' + label(u.attack) + ' 공격 · ' + label(u.guard) + ' 가드 · ' + label(u.kick) + ' 발차기'; };
                const ft = s => { const u = U[s]; return '<b>' + s + 'P:</b> ' + mv(s) + ' (이동/회전) | <b>' + label(u.attack) + '</b> (공격) | <b>' + label(u.guard) + '</b> (가드) | <b>' + label(u.kick) + '</b> (발차기) | <b>' + label(u.ink) + '</b> (특수)'; };
                for (const s of [1, 2]) { if ($('how' + s)) $('how' + s).innerHTML = how(s); if ($('ft' + s)) $('ft' + s).innerHTML = ft(s); }
            }

            // ----- 회전 방식: 키(기본) / 마우스 · 터치 (1인용만) -----
            const solo = () => { try { return aiMode && started && !tutorial && !(window.NET && NET.on); } catch (_) { return false; } };
            const live = () => { try { return rotMode === 'pointer' && solo() && !paused && !picking && !gameOver; } catch (_) { return false; } };
            const IS_COARSE = matchMedia('(pointer: coarse)').matches;
            const MOUSE_SENS = 0.0035, TOUCH_SENS = 0.006;   // 픽셀당 회전(rad)
            const add = v => { pending = Math.max(-1.5, Math.min(1.5, pending + v)); };
            function ptrRot(player) {   // 이 플레이어를 포인터로 돌리는가: 1인용에서 AI가 아닌 쪽
                try { return rotMode === 'pointer' && aiMode && !tutorial && !(window.NET && NET.on) && player !== aiSelf; } catch (_) { return false; }
            }
            function takeRot() { const v = pending; pending = 0; return v; }
            function refreshRot() { const b = $('cRot'); if (b) b.textContent = rotMode === 'pointer' ? '마우스 · 터치' : '키 (기본)'; }
            function setRot(m) {
                rotMode = m; pending = 0; refreshRot(); render();
                try { localStorage.setItem(SAVE_ROT, m); } catch (_) {}
            }

            window.addEventListener('mousemove', e => {   // 마우스: 화면을 클릭해 포인터를 잠근 동안(또는 버튼을 누른 채) 좌우로 움직이면 회전
                if (!live() || !(document.pointerLockElement || (e.buttons & 1))) return;
                add(e.movementX * MOUSE_SENS);
            }, true);
            window.addEventListener('pointerdown', e => {
                if (e.pointerType === 'mouse') {
                    if (e.button !== 0 || !live() || document.pointerLockElement || !e.target.requestPointerLock || e.target.tagName !== 'CANVAS') return;
                    lockOwn = true;
                    try { const r = e.target.requestPointerLock(); if (r && r.catch) r.catch(() => { lockOwn = false; }); } catch (_) { lockOwn = false; }
                } else if (live() && touchId === null && e.target.tagName === 'CANVAS') {   // 터치: 화면(조작키 밖)을 좌우로 밀면 회전
                    touchId = e.pointerId; lastX = e.clientX;
                }
            }, true);
            window.addEventListener('pointermove', e => {
                if (e.pointerId !== touchId) return;
                if (live()) add((e.clientX - lastX) * TOUCH_SENS);
                lastX = e.clientX;
            }, true);
            for (const t of ['pointerup', 'pointercancel']) window.addEventListener(t, e => { if (e.pointerId === touchId) touchId = null; }, true);
            document.addEventListener('pointerlockchange', () => {
                if (document.pointerLockElement || !lockOwn) return;
                lockOwn = false;   // ESC 로 잠금이 풀림 → 일시정지 (ESC 키 자체가 전달되는 브라우저와 겹치지 않게 살짝 늦게 확인)
                setTimeout(() => { try { if (started && !paused && !picking && solo()) togglePause(); } catch (_) {} }, 60);
            });
            setInterval(() => {   // 일시정지 · 카드 선택 · 경기 끝에서는 잠금을 풀고, 안내 문구 / 화면 터치 설정을 맞춤
                let want = false, on = false;
                try { on = rotMode === 'pointer' && solo(); want = on && !paused && !picking && !(gameOver && matchOver); } catch (_) {}
                if (document.pointerLockElement && !want) { lockOwn = false; try { document.exitPointerLock(); } catch (_) {} }
                if (!live()) { pending = 0; }
                document.body.classList.toggle('rot-ptr', on);
                const h = $('rot-hint'); if (h) h.classList.toggle('show', want && !IS_COARSE && !document.pointerLockElement);
            }, 150);

            function init() {
                DEF = { 1: {}, 2: {} };
                for (const a of ACTS) { DEF[1][a] = P1_KEYS[a]; DEF[2][a] = P2_KEYS[a]; }
                for (const s of [1, 2]) for (const a of ACTS) defCodes.add(DEF[s][a]);
                loadKeys(); texts(); refreshRot();
                $('cRot').addEventListener('click', () => setRot(rotMode === 'pointer' ? 'key' : 'pointer'));
                $('cKeys').addEventListener('click', openKeys);
                $('kClose').addEventListener('click', closeKeys);
                $('kReset').addEventListener('click', () => { cap = null; U = { 1: { ...DEF[1] }, 2: { ...DEF[2] } }; rebuild(); saveKeys(); texts(); render('기본 키로 되돌렸어요'); });
                $('key-grid').addEventListener('click', e => {
                    const b = e.target.closest('.kg-b'); if (!b) return;
                    cap = { s: +b.dataset.s, a: b.dataset.a }; render('새 키를 누르세요 (ESC: 취소)');
                    if (document.activeElement) document.activeElement.blur();
                });
            }
            window.addEventListener('DOMContentLoaded', init);
            return { ptrRot, takeRot };
        })();
    </script>
    <script>
        for (const t of ['keydown', 'keyup']) window.addEventListener(t, e => { if (window.NET) NET.onKey(e); }, true);   // 멀티플레이 입력 중계 (아래 NET 스크립트)
    </script>
    <script>
        // ===== 상수 =====
        const MAP_SIZE = 64;           // 타일 한 칸 크기(px)
        const FOV = Math.PI / 3;
        const PILLAR_R = 9;            // 기둥 반지름(px). 칸(64)보다 훨씬 가늘게
        const PLAYER_RADIUS = 10;      // 벽 충돌 반경
        const MIN_PLAYER_DIST = 28;    // 플레이어 간 최소 거리
        const JUMP_VEL = 300;          // 점프 카드: 뛰어오르는 초기 속도 (높이 = v²/(2g) 약 69px, 체공 약 0.92초)
        const JUMP_COST = 25;          // 점프 카드: 스테미나 소모
        const JUMP_CD = 3;             // 점프 카드: 재사용 대기(초)
        const STOMP_DAMAGE = 10;       // 점프로 내려오면서 상대 머리를 밟으면 주는 피해
        const STOMP_H = 24;            // 상대보다 이 높이 안쪽까지 내려오면 머리를 밟은 것 (이만큼 높이 차이가 나면 서로 겹쳐 지나감)
        const STOMP_BOUNCE = 0.6;      // 밟은 뒤 위로 튀어 오르는 세기 (점프 속도 배율)
        const JUMP_HOLD_MIN = 0.2;     // 점프: 발차기 키를 이 시간(초) 안에 떼면(톡) 평소 발차기, 더 누르면(꾹) 점프
        const JUMP_HOLD_MAX = 0.8;     // 점프: 발차기 키를 이만큼(초) 누르면 최대 높이
        const JUMP_MIN_MUL = 0.55;     // 점프: 가장 짧게 눌렀을 때 점프 속도 배율 (높이는 제곱이라 약 30%)
        const FLURRY_HOLD = 0.4;       // 백열권: 공격 키를 이만큼(초) 누르고 있으면 발동 (그전에 떼면 평소 주먹)
        const CEIL_H = 96;             // 천장(벽) 높이. 눈높이는 MAP_SIZE/2 라 클수록 천장이 높아 보임 (기존 64)
        const MOVE_SPEED = 160;        // px/초
        const GIANT_EYE = 14;          // 거대화 카드: 본인 시점(눈높이)이 올라가는 양 (기본 눈높이 32)
        const GIANT_VIEW_SHRINK = 0.88; // 거대화 카드: 내 화면에서 상대가 작게 보이는 배율
        const GIANT_MOVE_MUL = 0.75;   // 거대화 카드: 이동 속도 배율
        const GIANT_LOOK_MUL = 0.6;    // 거대화 카드: 상대를 내려다보는 정도 (1 = 서 있을 때와 같은 높이에 상대가 보이도록 완전히 보정)
        const GIANT_UP_MUL = 0.4;      // 상대가 거대화했을 때 올려다보는 정도 (클수록 더 올려다봄)
        const GIANT_UP_MAX = 0.08;     // 상대가 거대화했을 때 시선이 올라가는 최대 양 (화면 높이 비율)
        const GIANT_LOOK_MAX = 0.12;   // 거대화 카드: 시선이 내려가는 최대 양 (화면 높이 비율)
        const ROT_SPEED = 2.0;         // rad/초
        const GUN_ROT_MUL = 0.6;       // 총 카드: 회전 속도 배율 (작을수록 느리게 돌아감)
        const AI_GUN_ROT_MUL = 0.5;    // AI가 총을 가졌을 때 회전 속도에 추가로 곱하는 배율 (총 카드 0.6과 합쳐 0.3배)
        const ATTACK_REACH = 85;
        const ATTACK_ANGLE = 0.4;      // rad (약 23도)
        const ATTACK_DURATION = 0.35;  // 공격 모션 전체 시간
        const ATTACK_HIT_TIME = 0.12;  // 모션 중 타격 판정 시점
        const ATTACK_COOLDOWN = 0.25;  // 후딜
        const DAMAGE = 10;
        const KNOCKBACK = 18;
        const SHAKE_DURATION = 0.3;    // 피격 시 화면 흔들림 시간(초)
        const SHAKE_POWER = 6;         // 최대 흔들림 크기(px), 7 이하 권장
        const PUNCH_LAUNCH_VEL = 220;  // 주먹에 맞았을 때 뜨는 속도 (발차기는 LAUNCH_VEL 기준)
        const LAUNCH_VEL = 260;        // 맞았을 때 위로 뜨는 초기 속도 (높이 = v²/(2g))
        const TAUNT_TIME = 1.5;        // 도발 말풍선이 떠 있는 시간
        const TAUNT_CD = 2;            // 도발 재사용 대기
        const DASH_COST = 25;          // 대쉬 카드: 스테미나 소모
        const DASH_TIME = 0.22;        // 대쉬 지속 시간(초) - 이 동안 무적
        const DASH_SPEED = 900;        // 대쉬 속도(px/초) - 걷기(160)의 약 5.6배
        const DASH_DAMAGE = 5;         // 대쉬로 상대와 부딪히면 주는 피해
        const DASH_TAP_MS = 280;       // 앞 방향키를 이 시간 안에 두 번 누르면 대쉬
        const DASH_CD = 1.0;           // 대쉬 재사용 대기(초)
        const DASH_HIT_DIST = MIN_PLAYER_DIST + 6;   // 이 거리 안으로 붙으면 부딪힌 것
        const SLASH_COST = 60;         // 돌진베기(대쉬 + 칼 융합): 스테미나 소모
        const SLASH_CD = 8;            // 돌진베기: 재사용 대기(초)
        const SLASH_DAMAGE = 10;       // 돌진베기: 부딪힌 상대에게 주는 피해 (그냥 대쉬는 5)
        const SLASH_STUN = 1.5;        // 돌진베기: 맞은 상대 기절 시간(초)
        const GRAVITY = 650;           // 중력 (공중 체공 시간 = 2v/g)
        const ROUND_TIME = 40;         // 라운드 제한시간(초). 끝나면 체력이 더 많은 쪽이 승리
        const ROUND1_BONUS_TIME = 10;  // 1라운드에만 추가되는 제한시간(초)
        const DOUBLE_DMG_TIME = 10;    // 남은 시간이 이 값 이하가 되면 Burning Time: 모든 피해량 2배
        const CARD_DELAY = 1.5;        // KO 후 카드 선택 창이 뜨기까지(초)
        const ROUND_END_DELAY = 3;     // 라운드 종료 후 다음 라운드까지 대기(초)
        const WINS_TO_WIN = 3;         // 먼저 이 라운드 수를 이기면 경기 승리
        const GUARD_TIME = 0.3;        // 가드 유지 시간(초)
        const GUARD_COOLDOWN = 0.5;    // 가드가 끝난 뒤 다시 쓰기까지 대기(초)
        const GUARD_BREAK_STUN = 0.5;  // 가드한 상대를 때렸을 때 내가 기절하는 시간(초)
        const STRONG_MUL = 2;          // 힘조절: 이 배율 이상으로 때리면 상대가 기절
        const STRONG_STUN = 1.0;       // 강공격에 맞았을 때 기절 시간(초)
        const STRONG_STUN_MAX = 1.5;   // 끝까지 충전한 강공격(최대 배율)에 맞았을 때 기절 시간(초)
        const GUARD_START = 10;        // 가드: 누르기 시작하려면 필요한 스테미나
        const GUARD_DRAIN = 25;        // 가드: 누르고 있는 동안 초당 스테미나 소모
        const GUARD_HOLD_TICK = 0.1;   // 가드를 누르고 있는 동안 매 프레임 이 값으로 유지
        const CHARGE_TIME = 1.2;       // 힘조절 카드: 최대 충전까지 걸리는 시간(초)
        const CHARGE_MIN = 1;          // 힘조절: 살짝 눌렀다 뗐을 때 데미지 배율
        const CHARGE_MAXMUL = 3;       // 힘조절: 끝까지 충전했을 때 데미지 배율
        const HIT_GUARD_CD = 0.2;      // 맞았을 때 가드 쿨타임이 이 시간(초) 이하로 줄어듦
        const STUN_TIME = 0.2;         // 맞은 뒤 공격 불가 시간(초)
        const CAM_RISE = 0.35;         // 공중에 뜬 본인 시점이 올라가는 비율
        const JUMP_CAM_RISE = 0.8;     // 점프로 뛴 본인 시점이 올라가는 비율 (맞아서 뜰 때보다 크게)
        const JUMP_LOOK_MAX = 0.3;     // 점프로 올라갔을 때 상대를 내려다보려 시선이 내려가는 최대 양 (화면 높이 비율)
        const STAMINA_MAX = 100;
        const DEF_CFG = { wins: WINS_TO_WIN, time: ROUND_TIME, hp: 1, sta: 1, side: 1, map: 'gym' };   // 경기 설정 기본값: 먼저 N승 / 라운드 시간(초) / 체력 배율 / 스테미나 배율 / 1인 대전에서 내가 맡는 쪽(1P · 2P)
        let matchCfg = { ...DEF_CFG };   // 지금 진행 중인 경기의 설정
        const ATTACK_COST = 15;          // 공격: 조금
        const GUARD_COST = 15;           // 가드: 공격과 같게
        const STAMINA_REGEN = 22;        // 초당 회복량
        const KICK_RECHARGE = 4;       // 발차기 전용 재사용 대기(초) - 찬 순간부터 계산
        const KICK_COST = 30;          // 발차기 스테미나 소모 (공격 15, 가드 25)
        const AIR_MOVE_MULT = 0.4;     // 공중에서 이동 속도 배율 (1 = 지상과 같음)
        const AIR_HIT_MAX_Z = 60;      // 상대가 이 높이보다 높이 떠 있으면 공격이 닿지 않음 (주먹에 맞아 뜨는 최대 높이는 약 52)
        const COMBO_WINDOW = 2.0;      // 이 시간(초) 안에 또 맞히면 콤보가 이어짐
        const COMBO_FADE = 1.0;        // 콤보 표시가 사라지기 전 이 시간(초) 동안 서서히 투명해짐
        const KICK_REACH = 90;
        const KICK_DURATION = 0.5;
        const KICK_HIT_TIME = 0.2;
        const KICK_COOLDOWN = 0.4;
        const KICK_DAMAGE = 10;
        const KICK_SLIDE_TIME = 0.5;   // 밀려나는 시간(초)
        const KICK_SLIDE_SPEED = 640;  // 초기 속도(px/초), 약 160px(타일 2.5칸) 밀려남
        const KICK_WALL_STUN = 2;      // 벽에 부딪혔을 때 기절 시간(초)
        const GUN_COST = 25;           // 총: 스테미나 소모
        const GUN_COOLDOWN = 1.5;      // 총: 재사용 대기(초)
        const GUN_DAMAGE = 20;         // 총: 데미지 (맞는 즉시 적용)
        const GUN_RANGE = 600;         // 총: 사거리
        const GUN_ANGLE = 0.06;        // 총: 최소 조준 허용 각도(rad). 가까우면 몸 크기만큼 더 넓게 판정
        const GUN_FX_TIME = 0.25;      // 총: 발사 연출 시간
        const GUN_RECOIL = 0.22;       // 총: 반동으로 시점이 위로 튀는 크기 (화면 높이 비율)
        const GUN_MAG = 4;            // 총: 탄창 크기 (이만큼 쏘면 장전)
        const GUN_RELOAD_TIME = 2;    // 총: 장전 시간(초)
        const INK_COST = 30;           // 오징어 먹물: 스테미나 소모
        const INK_COOLDOWN = 7;        // 오징어 먹물: 재사용 대기(초)
        const INK_RANGE = 400;         // 오징어 먹물: 사거리
        const INK_ANGLE = 0.5;         // 오징어 먹물: 조준 허용 각도(rad). 먹물은 넓게 퍼짐
        const INK_FX_TIME = 0.6;       // 오징어 먹물: 오징어를 들고 뿌리는 연출 시간
        const INK_TIME = 4;            // 오징어 먹물: 맞은 상대 화면이 가려지는 시간
        const LACK_TIME = 1;           // 스테미나 부족: 기술을 못 쓰고 화면이 흐려지며 안내가 뜨는 시간
        const KI_COST = 25;            // 장풍: 스테미나 소모 (발사할 때)
        const KI_COOLDOWN = 5;         // 장풍: 재사용 대기(초)
        const KI_TIME = 1.2;           // 장풍: 최대 충전까지 걸리는 시간(초)
        const KI_MIN = 0.5;            // 장풍: 이 비율 이상 모아야 발사됨 (중간), 못 모으면 불발
        const KI_DAMAGE = 10;          // 장풍: 데미지 (중간 · 최대 충전 동일)
        const KI_STUN = 0.6;           // 장풍: 중간 충전에 맞았을 때 기절 시간(초)
        const KI_STUN_MAX = 1.5;       // 장풍: 최대 충전에 맞았을 때 기절 시간(초) + 넉백
        const KI_SLIDE_MUL = 0.7;      // 장풍: 최대 충전 넉백 거리 배율 (1 = 발차기와 같음)
        const KI_SPEED = 360;          // 장풍: 기 덩어리 속도(px/초)
        let aiShoryuCd = 0;                // AI 승룡권 재사용 대기 (이 시간이 지나야 다시 한 바퀴 돌기 시작함)
        const SHORYU_SPIN = Math.PI * 2;   // 승룡권(히든): 방향키로 이만큼(한 바퀴) 돌면 준비됨
        const SHORYU_SPIN_GAP = 0.5;       // 승룡권: 돌다가 이 시간(초) 이상 멈추면 회전 기록이 초기화
        const SHORYU_READY_TIME = 3;       // 승룡권: 한 바퀴 돈 뒤 특수공격 키를 눌러야 하는 제한 시간(초)
        const SHORYU_TIME = 1.2;           // 승룡권: 돌면서 어퍼컷하는 전체 시간(초)
        const SHORYU_HIT_TIMES = [0.3, 0.54, 0.78, 1.02];   // 승룡권: 다단히트 타격 시점(초) - 첫 타만 판정, 이후는 붙잡은 상대에게 연속 적중
        const SHORYU_HITS = SHORYU_HIT_TIMES.length;
        const SHORYU_RISE = 390;           // 승룡권: 쓰는 쪽이 솟구치는 속도 (상대보다 살짝 낮게)
        const SHORYU_DAMAGE = 40;          // 승룡권: 총 데미지 (다단히트로 나눠서 들어감)
        const SHORYU_LAUNCH_VEL = 470;     // 승룡권: 맞은 상대가 뜨는 속도 (주먹 220 / 발차기 338) - 쓴 쪽보다 살짝 높게
        const SHORYU_COST = 0.65;          // 승룡권: 최대 스테미나의 이 비율만큼 소모
        const SHORYU_FIRE_TIME = 1.0;      // 승룡권: 쓰면 화면 위아래에 불꽃이 타오르는 시간(초)
        const SHORYU_STUN = 1.4;           // 승룡권: 맞은 상대 기절 시간(초)
        const BLINK_DIST = 240;        // 순간이동: 빨간 원이 멀어질 수 있는 최대 거리(px). 벽 · 기둥 · 상대 앞에서 멈춤
        const BLINK_SPEED = 180;       // 순간이동: 키를 누르고 있는 동안 빨간 원이 멀어지는 속도(px/초)
        const BLINK_MIN = 24;          // 순간이동: 이보다 가까울 때 떼면 취소 (스테미나 · 쿨타임 소모 없음)
        const BLINK_R = 10;            // 순간이동: 바닥에 보이는 빨간 원 반지름(월드 단위)
        const BLINK_COST = 35;         // 순간이동: 최대 거리로 갈 때 스테미나 소모 (거리에 비례)
        const BLINK_COST_MIN = 10;     // 순간이동: 최소 스테미나 소모 (시작 조건)
        const BLINK_CD = 5;            // 순간이동: 최대 거리로 갈 때 재사용 대기(초) (거리에 비례)
        const BLINK_GHOST_T = 1.4;     // 순간이동: 떠난 자리에 남는 잔상이 깜빡이며 유지되는 시간(초)
        const BLINK_CD_MIN = 1;        // 순간이동: 최소 재사용 대기(초)
        const FLURRY_MOVE_MUL = 0.3;   // 백열권: 쓰는 동안 이동 속도 배율 (느리게 움직일 수 있음)
        const FLURRY_TIME = 1;         // 백열권: 주먹을 연타하는 시간(초)
        const FLURRY_GAP = 0.1;        // 백열권: 한 대씩 때리는 간격(초)
        const FLURRY_HITS = Math.round(FLURRY_TIME / FLURRY_GAP);   // 백열권: 최대 타수
        const FLURRY_DAMAGE = 3;       // 백열권: 한 대 피해 (전부 맞으면 체력 3칸)
        const FLURRY_COST = 35;        // 백열권: 스테미나 소모
        const FLURRY_CD = 8;           // 백열권: 재사용 대기(초)
        const FLURRY_END_LAG = 0.15;   // 백열권: 다 때린 뒤 후딜(초)
        const FLURRY_RATE = 7;         // 백열권: 연출용, 한 손이 1초에 주먹을 내지르는 횟수
        const FLURRY_GHOSTS = 5;       // 백열권: 1인칭에서 한 손당 동시에 보이는 주먹 수
        const KI_SPEED_MAX = 230;      // 장풍: 최대 충전 기 덩어리 속도(px/초) - 더 느림
        const KI_RANGE = 600;          // 장풍: 사거리
        const KI_HIT_R = 22;           // 장풍: 맞는 판정 반경
        const KI_R = 14;               // 장풍: 기 덩어리 크기(월드 단위)
        const kiBalls = [];            // 날아가는 중인 기 덩어리 { x, y, dx, dy, d, max, owner, full }
        const clones = [];             // 분신: 주인(owner)을 프로토타입으로 삼아 모습 · 무기를 그대로 쓰는 개체 (isClone)
        const obstacles = [];          // 설치한 장애물 박스 { x, y, t: 남은 시간 }
        // 도시 맵 자동차: 십자 도로(가로 큰길 · 세로 큰길) 중 한 길을 한 대가 지나감 { x, y, dx, dy, ci, hit: [1P, 2P] }
        const CAR_INTERVAL = 10;       // 몇 초마다 자동차가 나올지 굴림
        const CAR_CHANCE = 0.5;        // 그때 실제로 나올 확률
        const CAR_WARN = 3;            // 차가 출발하기 이 시간(초) 전부터 지나갈 길이 서서히 빨개짐
        const CAR_SPEED = 420;         // 속도(px/초)
        const CAR_LEN = 110, CAR_WID = 56, CAR_H = 26;   // 길이 · 폭 · 높이
        const CAR_DAMAGE = 20;         // 맞으면 체력 2칸 (10당 1칸)
        const CAR_FLAT = 2;            // 자동차에 치이면 납작해져 못 움직이는 시간(초)
        const CAR_COLORS = ['#d9534f', '#2e86c1', '#e1a02b', '#27ae60', '#ecf0f1'];
        // 버스: 자동차가 나올 때 이 확률로 버스가 나옴. 길 폭을 가득 채워서 옆으로 비킬 수 없음 (점프로 위를 넘거나 대쉬 무적으로만 피함)
        const BUS_CHANCE = 0.5;
        const BUS_LEN = 230, BUS_H = 70, BUS_SPEED = 300, BUS_COLOR = '#2b79d6';
        const BUS_FLAT = 4;            // 버스에 치이면 납작해져 못 움직이는 시간(초)
        const FLAT_IN = 0.1, FLAT_OUT = 0.4;   // 납작해지는 데 / 다시 펴지는 데 걸리는 시간(초)
        const FLAT_SQUASH = 0.12, FLAT_WIDEN = 1.35, FLAT_EYE = 8;   // 납작할 때: 상대 눈에 보이는 키 배율 · 폭 배율 / 본인 눈높이 (기본 눈높이 32)
        const BUS_ROAD_H = 3, BUS_ROAD_V = 4;   // CITY_MAP 큰길 폭(칸): 가로길 3칸 · 세로길 4칸
        // 차량 그림 (도시 맵 버스 · 자동차): front 앞 · back 뒤 · R 진행 방향이 보는 사람 오른쪽인 옆면 · L 왼쪽인 옆면
        const VEH_B64 = {'bus': {'front': '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', 'back': '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', 'R': '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', 'L': 'iVBORw0KGgoAAAANSUhEUgAAAKoAAABcCAMAAADJY960AAAAwFBMVEUmlvYfOFtWWF0QTpoVHCcMYtLi5OskS3FVtO1y0vlXWFiYn61Wb5FqibCltMqjzebm5eXu7+8HO4zmiCfw8fGkoqMrKyvjdR3Nll+ykV9fYGA2ga+Yd2b226WQXiW8kDu6vbr3z3wYh/gOGSrP1uQEBQgvV4YAAAAXIzcRd+wnRm43YZEWKkcjN1YcNFYNZdYAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAABRyiEtAAAAMHRSTlP///7//v/+////qfz/////hEb//ymKnP///1X//////1X///////8A//////////97LX8+AAANAklEQVR42s2bC3ujKhOARTGkG5P0utfz3UK1aMT8/3/3zQUQ1KRpu6dn5znbYxCH12EYQMfs5c1yl18hm5c7rv2Uv03Ot5u9HfWpvkLk3d0jVn7M67fJ429D/SllXav1a1IQLtatTXa+2s0oXKDhovx3oSKD2u9vLgmc1sFMw821ApetFXbI6u4s6lt8CUB/rff7C4aCf/ubQnkp1tcK4mbK1Euez6irp7d50y9Um4EcFoTL4Y831XIVupj/jGXwP9Csljz/9hFR79DxpbIgw2CtOid4epBG6sKjBokIfEnrUbOW8em/VwVMW/Szpuv66RZRv1zjfaNkp4mU9CcS/t06SU6Vp4uCVwHuzIPrGn0gu3sj6k1bTqQgmZYyKJ0OdRIpF+TUlodFVIB9yR6/YPcXHC18zLgo7dwYC+YKVp1UdKBnrXrIkuCGg3SNLpCzA1R78v6szeYueEZmXjY5dZiUnnfPVOm8CTjA2OdQt4x6OF3WdJ74cLW8Sb9HvbmRHrWgK6CzxkqHNwH8vQLeG6NifAGf/iMF4AJqQ5aGMfDno+brP9aqaD6AC8Mq3zDq6Y8zLAQ9GlyEeudRW0I9/HGo5JzSoyrgxLgshBhnE7cugoOorFgUdaa8mK8kWIu/IC51v9JrkAgn2+CrCjq/1yBS6iBylLGI1suxYEG4LK1Nv93KCGrVMq7mjvzKSScqa7cw54oJapeVpdB/k6T0s5MONalOoKEkRS2awpgeDIt/ZyIElWo9WC9DP1gh+Bi0DfgLBNeJFg+7rtd918HRgItHLKEKBktBoEI3DJ3gpScCcbEQfT+gEmiNG5+gWtV1oAR9wBiiFXQRc4peGL6RgRSjJkBFMqRiVCYUfBbJAJXgsKjnG4lQCWoQEaro+GawRbxkAfULrKzxRpDSWdwsClxkxWhVMiIpZ6t6VMtHIyoWkp2RxThb48V9z9cIbFv7mhdQayAbuEEt04EVxKO6FrHznHFQ4BaBsKOTYvB8HhUJoafdhUYbj0pQwpdqEW5g4MsTVIqrtfHWBHfWup6jGmfmBNUkqIKdsetsjIrW7BjVC2jzpF0fihHA+cjAhltGhfEGJhkQsS4K7VF70QfWQjHqiNcbG6N2zlSAyh1tLdyg9ai+C7DvjB9iOKxGDdI7A6OC/xjy+yFG3dT1sSiamlCzYEtRiJptqvus0IRK2mggmDDoBY45HvskXAVrGDfYwFt4/PEAos0mnhjYL+Af6naX94YRAZXHqExRq+rIqGVm2PBGelQdUKVz2iVPTn7N/VyfGwDOtRZrsAPIcVgpcIBqXQGq0XW27jV1y6CLEvhwOPeyz44a6eUUaxFmAfXVaWKpimHviVArE1ANoA6ManXRFuCviKoZtdfRUIoF+qxT81IdgkR0Ui8qMezuSZGvqPuAmmtA3VYNGNyQVa2z6gFQcToZGBVGmWm84ErCYTQNNNTEohT+pXtWcalDbUKhP63QpokGvFOo2MFFjEq+2k1Q+WYAFRx0QKdnVIHW9aqOx2OkGEzCZUmpNUPji8cThpSkZQE1LvWtqRnq9hwqHpJVGVX55kMz2PzHUNW1qGqGij01SELlQ49qsOMnqFDkey9ldaiTezCOIC5UNFthYaTCo8YOYBPUrDcCXQVQDzGqgRUHowLsxFKAquZQQ4Lqyz1qbFjVxVZ1pUtWtVOrWqXmVmVUJp2gKo+a3gAMq3eiNtejUrBiVDSw1QnqrPmAmhYDqmpmWCYZm1wYUOPCJVQBqHkcAQBVKVsjqq2OARWDFYAmqMfUAd6BSsXqSlQjEXVm1XOozRzVhKA4QW2uRMXIfA0qbm2qiVUDKvaOQ+2juJrChnaS9u2IGtGaRIkv7mcqAHW4FtX5auOsqi+imoXiZdRFJYSqpqijVQ8O9askVBVQhVsDULDCYSWNQx2S+dM3f4xNMsLaheozqzquIUZN42oTodKDIECtp7PVwc1WttZgYJwCFlGPy6iNXay+jEpWVedQD9ehKkZtIFjZc6jpWuMSarOI2kxRj5dQYWm96ADstpri6qxtzzUGq7j9herOAdS0sHETa2rVwU2sur2MGjuAm616dN1JN/m4umC/YQkVrGoWdPRmhjpg+MFRHe2t6LXFtvBrABOvVxG1Edqjkm/MG5qi8iy7gNqQAygV7hhXvRFqeKgGrcC6+RihyglqT6i88huXK4L2VvrVbceljckV157dB8n97nkVoR4jVNzTDDVuWAKqetsTtdBwjBAdmzNbwoUyRN2vIlT0VeNRcSfsUHmEDdnRqvzTBF/3jj9UvkpQi2b0VXoSN9QKt4Ee9XkL1f8peX6eoeLm2qFaQC0LfuqEqKvtLr72LY28i23/HGT1nKDigyB69gOo7vmLVCecoiyhrvfb3fNnyj79GaG64X1/wg3LQM90dECFqLNerXd4wWeRTluKUGtNj+rvW0ZFVnq60vPTT7Aqoj5/Hup5qx59agRNAYjaO1Syag+om28Pn0Y6Q43i6q915l+yIyo9iHMPggBVIuqPb98+EXV1FrVgVGdVfmZIVrX8zAqG1eb79+fnP8BXC/9CM6CCr55i1PVu9fzJqCsPjMFRp/kAhNrHqPzQkoPVP4d6lVUD6u5z4+qFCPCqA+zWu2jy+O1kU60w60/Om0uoNAWIFHW/2wTZ7X8H5G63pHA1G1ejVd3L9RhVBFTYBZScgKPj5DeTuWwq+OuzqtqQX9WeSspFGvOtSq7HmU70oyxFrFBzqkdZUmbTeCEmr4xvrk/lZVRoA+NuiuozqQJw245Ja4jajjWSXLFTQElQ6/bgrzwFPaQlTgjZbGcRYETVIjsAaiH6NKdQFKcsZCvOpD21Z1OrOMujLQqTKCwK9sT2cAh3SYcR6mb1fR6sxikAUE9tqce34f6lfe8TExcSY9rTa5kwBXc7qdPcYdqhZiH5wWHpCWrLqHYaARC1cP7kXzXxz76E2fhMfszpdBm0ZzrJGxXjMhYEnIJ7DKgtZ4+OqP/6wSbHlZVNFoH8MuggNINKWGphcoEA/cRK3bWMetmqrFAaUOf3Vc5hUaPLIOQsmwlq61F1hGoCKqsx9KISUaHcuB47h1qerkFFIVTvVB7VD0L2J/bVvK5//O8/rStLhpXBpTWiZs6rSKNDtWTXsm2XadvyVatK7SFZSCHHjdEB2nFY3cLpfz/8Vboy497LjqhW92VwU51vcJe11wRLlinOWbV8zaZkztryhkojMvVUUU5RyxNUZlSbF4uouMzGvdWIavLNhlExjlGXFcvJWeVFB9Cc8gMKbe5RjUcFwxYuI5axyiKgDpj62lKaK+0C0GC4Y+Vj2LEGVFnRHFjl4GXi3ajtgYwqAFVvt6hwt4Huj1AdpJtGqkp71C3IugJzI6p7kYy7AEywwMyUkkDBCjmQKm1yUG01ZqIwapyf549ptopLx1otokp8Na0tqMqlAdZdXkN8QY04r45pzm17L7Y7E6NujxhwAbXAnLEe9oQnn5HRF777oVqeW1VVm10OJqfwWvhJZUQKqO1oRz/3eNQaUeVmU1XQHPWUxFBIqOUEtRmt6t9sF+1B9DSXF/reOTQEf0SFvpLGbja5yiv8pgBQMb9iRM3G6Z8KynENEE2TLaVJOlRwof0Ob11tt9BdFmOhpmFVurzxEyq/F12zgNr2PXlzASAuthVCFM4BYARYDaAdHG1oHpDeAaqHhyphjZcrozw8/EU3xlaVMPp701WV1Xr/nAfUcdXz/eFHeT90Si6gClijkL2M9rlr8B/ZwApAlTpXcCWiGulRQXX17aFM7Hoq5qhl+e3bFFXoPEKVjNqOqA+I2o3BynJ+Dzj0PVi+gX/HphkTJo+MimNAUVQQFboWjGBJowBXbUWRZtyXxUIGPnYsmVuSRil3u46+87CCHQBR709R8j46gRgsfhtCqNpwmhGZfv6txjpjBxB2u6ksxkLwLAhXzgHKkj5SmH/YsPCNAhRS+zT5weWgEDXaHLyVAiuiurW3+6qhvBe4PJB32S0FR9MPglHL6POD0Jm0+gPWDoOVMRVY16IJKFgFzPgbkNOZ7ykI41S6yUrmarOzOLHsKpfLxb5KrK5P72kBDg7wspHRnsHlaE5T2NwCUOIUABPrfoOTFQfsOiSc1kny6RWfGIE1IaooULjbVuC6brXm2k8/DZK4XHn8cuXHS7AGFiKnqaUywgqj648JupQwAjaA4AY4V5mzN/iVv7e6XV2LCn4PwxUFFzLGfBAV52aLwXqzAU+9BvXl7uvrH1DmclxaY2Id682/vF9QIy8CUSttBpB+qerXrz/f8G3g3VPt5m1aWwt89QGu/nL78i55vHvBNb3kJTDdPw/zu49/HHr7NO4DpF9Z5i8fEP7QC3uHVBoe5re/4TvWx00++STVfV34bnnayKnCi/eevftbW/q08GNym978z8u13/Qdax5/EZC/fFzSsfvfy5X/D+dG9ojSFhaeAAAAAElFTkSuQmCC'}, 'car': {'front': 'iVBORw0KGgoAAAANSUhEUgAAAGAAAABLCAMAAAC4LXL/AAAAwFBMVEVaICr4YGUhGSDTLjeUIy4fL0kzUnjvPEPe3+VZVl2ZTVGXl5ZnZ2c1WIGalp/l5eXw8fGyt8hRNkioO0Tt0aTu7+4rLCv60FuEeoTrnZF0dYr0e4K+wc9/gX/qtXA/QT89Q0FAQT9lZWV/iKO/v8HBv7/BucgAAAAGBQb3Q0gRGSkpRmuwJTElNlEXJDgdM1IAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAB8NjvkAAAAMHRSTlP///////////77/5+a//mHSv////8thP///////6r/gID/cf+AgP8A///////////bA2hRAAAGpUlEQVR42rWZC3urKBCGESFqYtUmTU/TnrP33SpB+///3c4MoGDQXM7u9/RpLui8MAPMYNhnVFVV1fXur91uVxag33lM2FKWJVy0+xuuLn6NWWKxL48Nbx8QPza3AJrjZ/MgoKnr+ngVULQweriaM6vtmtgo26fdNUBhu7NN7tDHR5IIc1/RNKuAIwCoz4vGuqUGJgQDQl6vAUoc6MfpBF3qui4z6pzofQYvXTZ9M7UDHCPBqxXAK44yOZ1MX0PzEfntWWYAbXsFsD2A7cN+fzjAkG8TXgrKslQIcMHrOgCcnGVsQKlbZC+EqSdSEFsHQIjJyUwZwtlXL/GrwUrSx0HiH5FuAZQtAjKu5HmzeXp62oB8BHzCr6nhHLRIKQdYOgQolgG/GYACwHljdQ4JBvAUfm30pVhGgHoJUIGHOMwHpfoFAPadAOeYAJABgL9WCwDaULpMKHUeAWH3N2YIm/MCgFwUOGkO4NCJxwEcAXwVkCRwDXqI7IXut+ENzEsUvNAsU0prnepFwBFD3CEg0rvJvO///gtFHAfQy4CKAFozaXvXozzA3GtSGgBchQMBABME4HEAJ4CgSWqtg74898+CYswbBrEkhjkFM3UUUJgRrAOCie+JYBMgbzzArjTiNEkNwNqnu3zAeQlAkgMzu0VRYTlQ7ghQeAmY4SoY5NR9Eob20n7fxwA6TcWUpXcAqPwEL2iZ9ZNw6AvLmpppmk6EGQASKGtwezCJnQCCKenZxzkY3zUkmh+77l45E7gQWnHYCqwdClZDFWGTKkcAbNR9oCUA4e0gJ2cNGGaaLJhzuQPADpqmuE8BYFgCnOf2e/k1jlTOAGAvNQAoI3iX4gLEbKf9EZB7/XB4cUd3YOMXRQH/DfSGAJAYaEkLdBHOfmHUIoDDLMWwSSMvGp59aodUhu+kJ0xuBODOogHY3I0AyGZGOLe4uk8cb8Atm7fOogGM0zaBjPSzgsysvXnKPutpHQgAdK4eWi2IXC3kajN6k9Ifhnc0WdTM7hSvphzNUpxdsGVD7TKVbtnMqim4JuvmEugcVXcwH6k8MnuF3exqLNih1dpCgGdvvbTLbIGH85IKzjTDMfC8rqfdtAZH8QkAL0my6JYA0I3jQwB9Bz7KuNuyDQD3i5bBYk4zspvgWJPuDoFnqOw2JNpReTMBdpxCDFf9BCCZAUziZC7VwC5FAbKXd90VQDYHZNZ8lmoEwFrgAWCL9QSU0+6Yka4RvBOCORjAveZwAikX1oIWNIY5gNZJgnU+roXuHh9h8EjC1vyXgEOXsOLt7W2Ppz48S3T3HNIS7E9yOMChsKjeCsZ1BNCxf/I8//O9gA7cSzAxY2z/Xj3n+cs2CkhYbmRcdQeAgqLROQUZAICIA15eXqC9qmCUezxO6Nv2N9r790UBN6L5l9My4Nu36hnGmD9XkqVasOEm4bThBd2Yfwcbv2yZiMZgAuQVVDhhfRHKS0U9lYwW8N0CokEWrDqdzDDzHLIeuz3VjIBnFEzFy2kqACC2VeUAAxOMPwKo3mEephEAZAqIKYTqHRjvBdzDlLopBFIpmEGFEy2zS4DGbQiqCy/3iUGZ0oLy+WAPrdN/863EGHjzjQ6zaCgGsFtcQnnPBHntQE4tAwGsMpMyFwB4gd2mzVU4TaVfJc2F38LRXGgcvU1rZF1HAfR9Gkg5gFwQx0F4N5iCCxQdgQVoq5RKKE7PIeCfeTGPJYL5xb17tCNcAHAHpxOWp7FbqQhkOynI7oVxyDVY2UUA1LmQ4u4WUek0Zp1GhQA+A2g3Yh+grwFCgrD1o0IXRQD9ZjOYJzNzn1b5hbZzj2pOKxNmxOIIEDD8XwBs73FhmRFqu6gxyYJnowBoEJSEhQgAMOGigJQP0s4/dLDg43zk7dsloGi9qeoAtL7x/BEFpOMGTTPZPQSHuLVFDIBNHkC4D0xHALQHev5k/mKiR82cHjnbkwTaboOzB3NLhGJGj5pnlR0L9gnGr0tNbylY40YAAOxLEwBw9XnLazblMaDBOSZY11oE3afFbB+JMO+JOJ+euDPe7/d973KIOcdGUvOemvco/2bry0uAfwkfZH+r8Gr/bhupOUC1/5WUigIG5XbkRw1z4whnYQpyaZrH3PiofXdWVgN+8g4gx7ohgMu/8KH8A3+C+kFPqnaL+mGfZeGvVd7BfRjGn4zcIRAf2E3JHf0X+0lpWXVTku89wOyZ3bhYaWfgvP68UyW3UXC/ss0fCha+N8u77dujqtNr3VwA/B2g/HxAlbeLjD38F2ugAtHkGIrxAAAAAElFTkSuQmCC', 'back': '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', 'R': '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', 'L': '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'}};
        const VEH_SHADES = [1, 0.8, 0.62, 0.46, 0.32], VEH_IMG = { bus: {}, car: {} };   // VEH_IMG[종류][면] = 밝기별 캔버스
        for (const k in VEH_B64) for (const f in VEH_B64[k]) {
            const im = new Image();
            im.onload = () => { VEH_IMG[k][f] = VEH_SHADES.map(s => { const c = document.createElement('canvas'); c.width = im.width; c.height = im.height; const g = c.getContext('2d'); g.drawImage(im, 0, 0); if (s < 1) { g.globalCompositeOperation = 'source-atop'; g.fillStyle = 'rgba(0,0,0,' + (1 - s) + ')'; g.fillRect(0, 0, c.width, c.height); } return c; }); };
            im.src = 'data:image/png;base64,' + VEH_B64[k][f];
        }
        let car = null, carT = 0;
        let rayExcludeBox = null;      // 총알: 맞힐 상대가 올라서 있는 박스는 시야를 막지 않음 (높은 곳 사람은 총으로는 맞힐 수 있음)
        let rayIgnoreBoxes = false;    // 화면 그릴 때만 true: 박스는 낮아서 따로 그림 (시야 · 공격 판정에서는 박스도 막음)
        const KNIFE_BONUS = 5;         // 칼: 주먹 공격 추가 데미지
        const KNIFE_REACH = 6;         // 칼: 주먹 공격 추가 사거리
        const KNIFE_COST = 5;          // 칼: 주먹 공격 추가 스테미나 소모
        const CLONE_COST = 40;         // 분신(특수): 스테미나 소모
        const CLONE_CD = 15;           // 분신: 재사용 대기(초)
        const CLONE_HP = 20;           // 분신: 체력 (2칸)
        const CLONE_LIFE = 10;         // 분신: 사라지기까지 시간(초)
        const CLONE_DMG_MUL = 0.5;     // 분신: 주먹 피해 배율 (기본 1칸 → 0.5칸)
        // 분신 AI = 애기모드: 느리게 걷고, 천천히 돌고, 때릴 수 있어도 머뭇거리다가 가끔 때림
        const CLONE_SPEED = 60;        // 분신: 이동 속도(px/초)
        const CLONE_ATK_CD = 2;        // 분신: 공격 사이 대기(초)
        const CLONE_TURN = 0.5;        // 분신: 상대 쪽으로 도는 속도 (플레이어 회전 속도 배율)
        const CLONE_ATK_RATE = 1.5;    // 분신: 때릴 수 있는 상태일 때 초당 공격을 시작할 확률 (낮을수록 머뭇거림)
        const INVIS_COST = 25;         // 투명(특수): 스테미나 소모
        const INVIS_CD = 12;           // 투명: 재사용 대기(초)
        const INVIS_TIME = 3;          // 투명: 상대 화면에서 사라지는 시간(초) (공격하면 바로 풀림)
        const HEAL_COST = 20;          // 힐(특수): 스테미나 소모
        const HEAL_CD = 10;            // 힐: 재사용 대기(초)
        const HEAL_HOLD = 3;           // 힐: 특수키를 누르고 있는 동안 서서히 회복, 최대 이 시간(초)
        const HEAL_AMOUNT = 20;        // 힐: 끝까지 마셨을 때 회복량 (2칸)
        const OBST_COST = 15;          // 장애물 설치(특수): 스테미나 소모
        const OBST_CD = 8;             // 장애물 설치: 재사용 대기(초)
        const OBST_LIFE = Infinity;    // 장애물 설치: 박스가 서 있는 시간(초). 무한 = 시간으로는 안 사라지고 라운드가 끝나거나 부서질 때만 사라짐
        const OBST_HALF = 16;          // 장애물 설치: 박스 한 변의 절반(px)
        const OBST_HP = 50;            // 장애물 설치: 박스 체력 (5칸). 주먹 · 발차기 · 총으로 부술 수 있음
        const OBST_RISE_VEL = 260;     // 장애물 설치: 시전자가 박스 위로 솟는 초기 속도 (최고 약 52px, 박스 높이 OBST_H 보다 조금 높게)
        const OBST_KICK_V = 260;       // 장애물 설치: 발차기로 맞은 박스가 밀려나는 처음 속도 (px/초)
        const OBST_KICK_DECEL = 1100;  // 장애물 설치: 밀려나는 박스가 느려지는 정도 (px/초²). 처음 속도 260 이면 약 30px(박스 한 칸) 밀림
        const OBST_PUSH_REACH = 26;    // 장애물 설치: 발차기로 박스를 밀려면 박스 모서리까지 이 거리(px) 안이어야 함 (더 멀리서 차면 피해만 줌)
        const OBST_H = 40;             // 장애물 설치: 박스 높이. 점프(최고 약 69)로 넘거나 위에 올라설 수 있음
        const HIT_FX_TIME = 0.5;   // 피격 이펙트 시간(초)
        const STAMINA_REGEN_DELAY = 0.6; // 사용 후 회복 시작까지 대기(초)

        // 픽셀 주먹 스프라이트 크기 (createPlayer보다 먼저 선언되어야 함)
        const FIST_W = 24;
        const FIST_H = 32;
        const FIST_ANCHOR_X = 12;
        const FIST_ANCHOR_Y = 14;
        const HUD_PX = 2.5;   // 스프라이트 1픽셀 = 화면 몇 px

        const GYM_MAP = [
            [1,1,1,1,1,1,1,1,1,1,1,1],
            [1,0,0,0,0,0,0,0,0,0,0,1],
            [1,0,0,2,0,0,0,0,2,0,0,1],   // 2 = 기둥 (장애물: 이동·시야·총알을 막음)
            [1,0,0,0,0,2,0,0,0,0,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,1],   // 가운데 줄은 비워서 시작할 때 서로 보임
            [1,0,0,0,0,0,2,0,0,0,0,1],
            [1,0,0,2,0,0,0,0,2,0,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,1],
            [1,1,1,1,1,1,1,1,1,1,1,1]
        ];
        // 콜로세움 맵: 둘레가 벽인 빈 방 안에 지름 ARENA_R 의 원형 바닥만 있고, 그 밖은 바다 (경기 설정에서 선택)
        const WINDOW_CELLS = new Set(['0,4', '11,4', '5,0', '6,8']);   // 건물 맵 창문 4개: 칸 'x,y' (서쪽 · 동쪽 · 북쪽 · 남쪽 벽 가운데)
        const COLO_N = 15;
        const COLO_MAP = Array.from({ length: COLO_N }, (_, r) => Array.from({ length: COLO_N }, (_, c) => (r === 0 || c === 0 || r === COLO_N - 1 || c === COLO_N - 1) ? 1 : 0));
        // 도시 맵: 건물 블록(1) 사이로 도로가 나 있음 (기둥 없음). 가운데 도로 줄은 비워서 시작할 때 서로 보임
        const CITY_MAP = [
            [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1],
            [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,1,1,1,1,1,1,1,1,0,0,0,0,1,1,1,1,1,1,1,1,0,1],
            [1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1],
            [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1]
        ];
        const CITY_START = [[406, 480], [1130, 480]];   // 도시 맵 시작 위치 (1P · 2P): 가운데 큰길 위, 서로 724px 떨어진 곳
        const ARENA_C = COLO_N * MAP_SIZE / 2;   // 원형 바닥 중심
        const ARENA_R = 288;     // 원형 바닥 반지름: 이보다 멀리 나가면 바다에 빠짐
        const WALL_R = 400;      // 콜로세움 바깥 둥근 벽 반지름 (네모 방 안쪽 끝 416보다 작아서 방 모서리는 안 보임)
        const RING_R = 268;      // 가장자리 기둥이 서 있는 반지름
        const RING_N = 10;       // 가장자리 기둥 개수 (기둥 사이로 지나갈 수 있음)
        const SEA_DROP = 28;     // 바다가 바닥보다 낮은 높이
        const SEA_EYE_DROP = 26; // 바다에 빠지면 본인 시점(눈높이)이 내려가는 양 (기본 눈높이 32 → 6. 0 이하로는 안 내려가게 아래에서 막음)
        const SEA_DAMAGE = 20;   // 바다에 빠졌을 때 체력 피해
        const SEA_TIME = 2;      // 빠져 있다가 시작 위치로 돌아오기까지(초)
        let map = GYM_MAP;
        let MAP_H = map.length;
        let MAP_W = map[0].length;
        let arena = false;       // true: 콜로세움 맵
        let city = false;        // true: 도시 맵
        const RING = [];         // 콜로세움 가장자리 기둥 좌표

        // ===== 캐릭터 스프라이트 (12x23): 직접 그린 앞/뒤/옆 외곽선에 색과 광택을 입힘 =====
        const SPRITE_W = 12;
        const SPRITE_H = 23;

        // # 외곽선 (왼쪽을 보는 모습은 옆모습을 좌우 반전해서 사용)
const VIEW_OUT = {
            front: [
                "...######...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "..###..###..",
                "..#......#..",
                ".##.......#.",
                ".#........#.",
                ".####.###.#.",
                ".#..#.#.#.#.",
                ".#..#.#.#.#.",
                ".####.#####.",
                "...##....#..",
                "...#.....#..",
                "...#.....#..",
                "...#..#..#..",
                "...#..#..#..",
                "...#..#..#..",
                "...#..#..#..",
                ".###..#..###",
                ".#....#....#",
                ".###########"
            ],
            back: [
                "...######...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "..###..###..",
                "..#......#..",
                ".##.......#.",
                ".#........#.",
                ".#........#.",
                ".#..#.....#.",
                ".#.#....#.#.",
                ".###.....##.",
                "...#.....#..",
                "...#.....#..",
                "...#.....#..",
                "...#..#..#..",
                "...#..#..#..",
                "...#..#..#..",
                "...#..#..#..",
                ".###..#..###",
                ".#....#....#",
                ".###########"
            ],
            side: [
                "...######...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "...#....#...",
                "...##..##...",
                "...#...#....",
                "...#....#...",
                "...#....####",
                "...#...##..#",
                "..#........#",
                "..#...#..###",
                "..#....###..",
                "..#.....#...",
                "..#.....#...",
                "..#.....#...",
                "..#..#..#...",
                "..#..#..#...",
                "..#..#..#...",
                "..#..#..#...",
                "###..#..###.",
                "#....#....#.",
                "###########."
            ],
        };

        // 외곽선 그림 → 칸 종류: 0 비움, 1 외곽선, 2 몸, 3 주먹, 4 광택, 5 반짝임
        function classifyView(rows, fistCells) {
            const H = rows.length, W = rows[0].length;
            const t = rows.map(r => Array.from(r, ch => ch === '#' ? 1 : -1));   // -1: 아직 모름
            const nb = [[1, 0], [-1, 0], [0, 1], [0, -1]];
            const flood = (sr, sc, v) => {
                const st = [[sr, sc]];
                t[sr][sc] = v;
                let n = 0;
                while (st.length) {
                    const [r, c] = st.pop();
                    n++;
                    for (const [dr, dc] of nb) {
                        const nr = r + dr, nc = c + dc;
                        if (nr >= 0 && nr < H && nc >= 0 && nc < W && t[nr][nc] === -1) { t[nr][nc] = v; st.push([nr, nc]); }
                    }
                }
                return n;
            };
            // 바깥: 테두리에서 퍼지는 빈 칸
            for (let r = 0; r < H; r++) for (let c = 0; c < W; c++) {
                if ((r === 0 || c === 0 || r === H - 1 || c === W - 1) && t[r][c] === -1) flood(r, c, 0);
            }
            // 안쪽: 가장 큰 덩어리는 몸, 나머지 작은 닫힌 칸은 주먹
            const comps = [];
            let label = 10;
            for (let r = 0; r < H; r++) for (let c = 0; c < W; c++) {
                if (t[r][c] === -1) comps.push([label, flood(r, c, label++)]);
            }
            comps.sort((a, b) => b[1] - a[1]);
            const mainLabel = comps.length ? comps[0][0] : -1;
            for (let r = 0; r < H; r++) for (let c = 0; c < W; c++) {
                if (t[r][c] >= 10) t[r][c] = t[r][c] === mainLabel ? 2 : 3;
            }
            for (const [r, c] of fistCells) if (t[r][c] === 2) t[r][c] = 3;
            // 광택: 왼쪽 위에서 빛이 들어오는 느낌 (몸 칸의 왼쪽이 외곽선이면 밝게)
            let spark = false;
            for (let r = 0; r < H; r++) for (let c = 1; c < W; c++) {
                if (t[r][c] === 2 && t[r][c - 1] === 1) {
                    t[r][c] = spark ? 4 : 5;
                    spark = true;
                }
            }
            return t;
        }

        const VIEW_CODES = {
            front: classifyView(VIEW_OUT.front, []),
            back: classifyView(VIEW_OUT.back, []),
            side: classifyView(VIEW_OUT.side, [[9, 9], [9, 10], [10, 9], [10, 10]])   // 옆모습 주먹 칸
        };

        // 칸 배열을 편집하는 도구
        function gridTools(g) {
            const H = g.length, W = g[0].length;
            const put = (r, c, v) => { if (r >= 0 && r < H && c >= 0 && c < W) g[r][c] = v; };
            const fill = (r0, c0, r1, c1, v) => {
                for (let r = r0; r <= r1; r++) for (let c = c0; c <= c1; c++) put(r, c, v);
            };
            const box = (r0, c0, r1, c1, inner) => {
                for (let r = r0; r <= r1; r++) for (let c = c0; c <= c1; c++) {
                    put(r, c, (r === r0 || r === r1 || c === c0 || c === c1) ? 1 : inner);
                }
            };
            const shiftUp = (r0, c0, r1, c1, d) => {   // 영역을 d칸 위로 올림 (발을 들어 걷는 모습)
                for (let r = r0; r <= r1; r++) for (let c = c0; c <= c1; c++) put(r - d, c, g[r][c]);
                fill(r1 - d + 1, c0, r1, c1, 0);
            };
            return { put, fill, box, shiftUp };
        }

        function codesToCanvas(g, color) {
            const canvas = document.createElement('canvas');
            canvas.width = SPRITE_W;
            canvas.height = SPRITE_H;
            const ctx = canvas.getContext('2d');
            const colors = {
                1: '#000000',
                2: color,
                3: shade(color, 0.25),
                4: shade(color, 0.45),
                5: shade(color, 0.85)
            };
            for (let r = 0; r < SPRITE_H; r++) {
                for (let c = 0; c < SPRITE_W; c++) {
                    const v = g[r][c];
                    if (v === 0) continue;
                    ctx.fillStyle = colors[v];
                    ctx.fillRect(c, r, 1, 1);
                }
            }
            return canvas;
        }

        // 플레이어 색으로 모든 방향/동작 프레임을 만듦. 정면 프레임마다 .side(옆), .back(뒤)을 연결
        // strike 의 hand: 0 = 오른팔, 1 = 왼팔
        function buildSpriteSet(color) {
            const mk = (view, edit) => {
                const g = VIEW_CODES[view].map(r => r.slice());
                if (edit) edit(gridTools(g));
                return codesToCanvas(g, color);
            };

            // 정면
            const strikeFront = hand => t => {
                const [c0, c1] = hand === 1 ? [1, 8] : [3, 10];
                t.box(6, c0, 13, c1, 3);                       // 정면으로 날아오는 큰 주먹
                t.put(7, c0 + 1, 5); t.put(7, c0 + 2, 4); t.put(8, c0 + 1, 4);
                t.put(10, c0 + 2, 1); t.put(10, c0 + 4, 1);    // 손가락 접힌 선
            };
            const F = {
                base: mk('front'),
                walkA: mk('front', t => t.shiftUp(20, 1, 22, 5, 2)),
                walkB: mk('front', t => t.shiftUp(20, 7, 22, 11, 2)),
                strike: [mk('front', strikeFront(0)), mk('front', strikeFront(1))],
                guard: mk('front', t => {                      // 양 주먹을 얼굴 양옆(턱 높이)으로 올림 — 얼굴은 그대로 보임
                    t.fill(10, 2, 11, 3, 2); t.put(10, 7, 2); t.put(11, 7, 2);   // 내려뜨렸던 주먹 자리는 팔꿈치로
                    t.box(3, 0, 6, 3, 3);
                    t.box(3, 8, 6, 11, 3);
                    t.put(4, 1, 5); t.put(4, 9, 4); t.put(5, 1, 4);
                }),
                kick: mk('front', t => {                       // 오른다리를 앞으로 뻗음
                    t.fill(18, 7, 22, 11, 0);
                    t.box(11, 4, 17, 10, 3);
                    t.put(12, 5, 5); t.put(12, 6, 4); t.put(13, 5, 4);
                })
            };

            // 뒷모습 (동작이 달라도 기본/걷기만 사용)
            const B = {
                base: mk('back'),
                walkA: mk('back', t => t.shiftUp(20, 1, 22, 5, 2)),
                walkB: mk('back', t => t.shiftUp(20, 7, 22, 11, 2))
            };

            // 옆모습 (오른쪽을 봄)
            const S = {
                base: mk('side'),
                walkA: mk('side', t => t.shiftUp(20, 6, 22, 10, 2)),
                walkB: mk('side', t => t.shiftUp(20, 0, 22, 5, 2)),
                strike: mk('side', t => {
                    t.box(7, 7, 12, 11, 3);
                    t.put(8, 8, 5); t.put(8, 9, 4);
                }),
                guard: mk('side', t => {                       // 주먹을 얼굴 앞으로 올리고 아래팔을 세움
                    t.fill(8, 8, 10, 11, 0); t.fill(11, 10, 11, 11, 0);   // 앞으로 뻗은 팔은 지움
                    t.box(2, 8, 5, 11, 3);
                    t.put(3, 9, 5); t.put(3, 10, 4); t.put(4, 9, 4);
                    t.fill(6, 8, 9, 9, 2); t.fill(6, 10, 9, 10, 1);
                    t.put(10, 8, 1); t.put(10, 9, 1);
                }),
                kick: mk('side', t => {
                    t.fill(14, 6, 22, 11, 0);
                    t.box(13, 5, 17, 11, 2);
                    t.fill(14, 9, 16, 10, 3);
                })
            };

            F.base.side = S.base;       F.base.back = B.base;
            F.walkA.side = S.walkA;     F.walkA.back = B.walkA;
            F.walkB.side = S.walkB;     F.walkB.back = B.walkB;
            F.strike[0].side = F.strike[1].side = S.strike;
            F.guard.side = S.guard;
            F.kick.side = S.kick;
            F.strike[0].back = F.strike[1].back = F.guard.back = F.kick.back = B.base;

            return {
                sprite: F.base,
                poseSprites: {
                    wind: [F.base, F.base],       // 와인드업은 순간적이라 기본 자세 그대로
                    strike: F.strike,
                    guard: F.guard,
                    kick: F.kick,
                    walk: [F.walkA, F.walkB]
                }
            };
        }

        function createPlayer(x, y, angle, color) {
            return {
                startX: x, startY: y, startAngle: angle,
                x, y, angle,
                color,
                ...buildSpriteSet(color),   // sprite, poseSprites
                fistSprite: generateFistSprite(color),
                hp: 100,
                maxHp: 100,
                atkCdMul: 1, kickCdMul: 1, guardCdMul: 1,   // 카드로 줄어드는 쿨타임 배율
                cards: [],
                canJump: false,   // 점프 카드
                canTaunt: false, tauntT: 0, tauntCd: 0,   // 도발 카드 / 말풍선 남은 시간 / 대기
                canDash: false, canSlash: false, dashT: 0, dashCd: 0, jumpCd: 0, stompDone: false, dashAngle: 0, dashHit: false, jumping: false, gun: false, knife: false, gunCd: 0, gunT: 0, gunAmmo: GUN_MAG, gunReload: 0, canInk: false, inkCd: 0, inkT: 0, inked: 0, inkSeed: 0, lackT: 0, canKi: false, kiOn: false, kiT: 0, kiCd: 0, canShoryu: false, spinAcc: 0, spinDir: 1, spinIdle: 0, shoryuReady: 0, shoryuOn: false, shoryuT: 0, shoryuHits: 0, shoryuTarget: null, shoryuAngle: 0, noGuard: false, canBlink: false, blinkCd: 0, blinkOn: false, blinkD: 0, ghostT: 0, ghostX: 0, ghostY: 0, ghostA: 0, canFlurry: false, healOn: false, healT: 0, flurryOn: false, flurryT: 0, flurryHits: 0, flurryCd: 0, canClone: false, cloneCd: 0, canInvis: false, invisCd: 0, invisT: 0, canHeal: false, healCd: 0, canObst: false, obstCd: 0,   // 점프 카드 보유 / 스스로 뛰어 공중에 있는 중
                attacking: false,
                attackT: 0,
                hitDone: false,
                cooldown: 0,
                punchHand: 0,   // 0: 오른손, 1: 왼손 (번갈아 사용)
                hitFlash: 0,
                shake: 0,
                stun: 0,   // 공격 불가 남은 시간
                wins: 0,   // 이긴 라운드 수
                guard: 0,  // 가드 남은 시간
                guardCd: 0,
                blockFlash: 0,
                canCharge: false, charging: '', chargeT: 0, chargeSrc: '', dmgMul: 1, hold: '', holdT: 0, holdSrc: '',   // hold: 점프('kick') · 백열권('punch') 키를 누르는 중인 기술 / 누른 시간 / 누른 입력   // 힘조절 카드: 충전 중인 기술('punch'|'kick') / 충전 시간 / 누른 입력(키 코드 또는 'ptr') / 데미지 배율
                z: 0,    // 지면에서 뜬 높이
                vz: 0,   // 수직 속도
                maxStamina: STAMINA_MAX, reachMul: 1,   // 카드로 늘어나는 최대 스테미나 / 사정거리 배율
                stamina: STAMINA_MAX,
                staminaDelay: 0,
                combo: 0,        // 연속 적중 수
                comboT: 99,      // 마지막 적중 후 경과 시간
                punchLanded: false,
                kicking: false,
                kickT: 0,
                kickHit: false,
                kickCd: 0,    // 발차기 전용 재사용 대기
                slideT: 0,    // 발차기에 맞아 밀려나는 남은 시간
                slideDX: 0,
                slideDY: 0,
                hitFx: 0,   // 피격 이펙트 남은 시간
                fx: [],     // 파편 방향/속도
                dizzy: 0,   // 가드 브레이크로 기절한 남은 시간 (이동 불가)
                flat: 0, flatMax: 0,   // 자동차 · 버스에 치여 납작해진 남은 시간 / 처음 시간 (이동 · 공격 불가)
                moving: false
            };
        }

        const p1 = createPlayer(150, 280, 0, '#ff4757');
        const p2 = createPlayer(600, 280, Math.PI, '#1e90ff');
        // 1P/2P 스프라이트: 직접 만든 앞/옆/뒤 그림 사용 (옆모습은 오른쪽을 봄)
        // 걷기 그림은 같은 그림에서 한쪽 발을 번갈아 위로 올려서 만듦 (기본 자세는 모든 동작에 같은 그림)
        function useImageSprites(player, img) {
            const w = img.w, h = img.h;
            // 같은 그림에서 색을 뽑아 큰 주먹/뻗은 다리를 그려 공격·발차기 모습을 만듦 (상대 화면에 보이는 모습)
            const pal = g => {
                const d = g.getImageData(0, 0, w, h).data, px = [];
                for (let i = 0; i < d.length; i += 4) if (d[i + 3] > 0) px.push([d[i], d[i + 1], d[i + 2]]);
                px.sort((a, b) => (a[0] * .3 + a[1] * .59 + a[2] * .11) - (b[0] * .3 + b[1] * .59 + b[2] * .11));
                const at = f => 'rgb(' + px[Math.min(px.length - 1, Math.floor(px.length * f))].join(',') + ')';
                return { out: at(0.01), dark: at(0.4), mid: at(0.68), light: at(0.93) };
            };
            const box = (g, x, y, bw, bh, c) => { g.fillStyle = c; g.fillRect(x, y, bw, bh); };
            const skin = g => {   // 그림에서 가장 많이 쓰인 몸 색을 기준으로 밝은/어두운 톤을 만듦 (팔/주먹이 몸과 같은 색으로 보이게)
                const d = g.getImageData(0, 0, w, h).data, cnt = {};
                let best = [128, 128, 128], n = 0;
                for (let i = 0; i < d.length; i += 4) {
                    if (d[i + 3] === 0 || d[i] + d[i + 1] + d[i + 2] < 60) continue;
                    const k = (d[i] >> 3) + ',' + (d[i + 1] >> 3) + ',' + (d[i + 2] >> 3);
                    cnt[k] = (cnt[k] || 0) + 1;
                    if (cnt[k] > n) { n = cnt[k]; best = [d[i], d[i + 1], d[i + 2]]; }
                }
                const mix = (t, a) => 'rgb(' + best.map((v, j) => Math.round(v + (t - v) * a)).join(',') + ')';
                return { out: '#000', light: mix(255, 0.3), mid: mix(0, 0), dark: mix(0, 0.4) };
            };
            // 칸 단위로 찍는 둥근 도형 (안티앨리어싱 없이 도트 느낌 유지). inside = 안쪽 판정, tone = 칸 색, skipEdge = 외곽선을 안 그릴 칸
            const blob = (g, P, inside, tone, skipEdge) => {
                const m = (x, y) => x >= 0 && y >= 0 && x < w && y < h && inside(x + 0.5, y + 0.5);
                for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
                    if (m(x, y) || !(m(x - 1, y) || m(x + 1, y) || m(x, y - 1) || m(x, y + 1))) continue;
                    if (skipEdge && skipEdge(x + 0.5, y + 0.5)) continue;
                    g.fillStyle = P.out; g.fillRect(x, y, 1, 1);
                }
                for (let y = 0; y < h; y++) for (let x = 0; x < w; x++) {
                    if (!m(x, y)) continue;
                    g.fillStyle = P[tone(x + 0.5, y + 0.5)]; g.fillRect(x, y, 1, 1);
                }
            };
            // 어깨(ax,ay)에서 손목(bx,by)까지 굵기가 변하는 팔. 어깨 쪽 끝은 몸 안에 묻혀 외곽선 없이 이어짐
            const arm = (g, P, ax, ay, ar, bx, by, br) => {
                const vx = bx - ax, vy = by - ay, L2 = vx * vx + vy * vy, L = Math.sqrt(L2);
                let nx = -vy / L, ny = vx / L;
                if (nx * -0.5 + ny * -1 < 0) { nx = -nx; ny = -ny; }   // 법선을 빛이 오는 왼쪽 위로
                const q = (x, y) => {
                    const t = ((x - ax) * vx + (y - ay) * vy) / L2, r = ar + (br - ar) * Math.min(1, Math.max(0, t));
                    return { t, r, d: ((x - ax) * nx + (y - ay) * ny) / r, off: Math.hypot(x - ax - vx * t, y - ay - vy * t) };
                };
                blob(g, P, (x, y) => { const o = q(x, y); return o.t >= 0 && o.t <= 1 && o.off <= o.r; },
                     (x, y) => { const d = q(x, y).d; return d > 0.4 ? 'light' : d < -0.44 ? 'dark' : 'mid'; },
                     (x, y) => q(x, y).t < 0.1);
            };
            // 주먹: 중심(cx,cy) 반지름(rx,ry). front = 정면(접힌 손가락 4개 + 주름선 + 엄지), 아니면 옆모습(손가락 가로줄 + 엄지 쪽 주름)
            const fist = (g, P, cx, cy, rx, ry, front, skipEdge) => {
                const u = x => (x - cx) / rx, v = y => (y - cy) / ry;
                blob(g, P, (x, y) => Math.abs(u(x)) ** 2.2 + Math.abs(v(y)) ** 2.2 <= 1,   // 타원에 가까운 둥근 덩어리 (네모지지 않게)
                     (x, y) => { const k = u(x) * 0.5 + v(y) * 0.9; return k < -0.45 ? 'light' : k > 0.45 ? 'dark' : 'mid'; }, skipEdge);
                const dot = (x, y, c) => { g.fillStyle = c; g.fillRect(Math.round(x), Math.round(y), 1, 1); };
                if (front === 'plain') return;   // 손가락 · 주름 없이 매끈한 주먹 (가드)
                if (front) {
                    const top = Math.round(cy - ry * 0.78), crease = Math.round(cy + ry * 0.1);
                    for (const f of [-0.5, 0, 0.5]) for (let y = top + 1; y < crease; y++) dot(cx + f * rx, y, P.dark);          // 손가락 사이 홈
                    for (const f of [-0.75, -0.25, 0.25, 0.75]) { dot(cx + f * rx - 1, top + 1, P.light); dot(cx + f * rx, top + 1, P.light); }   // 손가락 마디 하이라이트
                    for (let x = Math.round(cx - rx * 0.8); x <= Math.round(cx + rx * 0.8); x++) dot(x, crease + (Math.abs(u(x)) > 0.55 ? -1 : 0), P.dark);   // 손가락이 접히는 주름
                    for (let x = Math.round(cx - rx * 0.72); x <= Math.round(cx + rx * 0.28); x++) {   // 엄지: 접힌 손가락 밑을 가로지름
                        dot(x, crease + 1, P.light); dot(x, crease + 2, P.mid); dot(x, crease + 3, P.dark);
                    }
                } else {
                    for (const f of [-0.5, 0, 0.5]) for (let x = Math.round(cx + rx * 0.1); x < Math.round(cx + rx * 0.7); x++) dot(x, cy + f * ry, P.dark);   // 손가락 사이 홈
                    for (let y = Math.round(cy - ry * 0.6); y <= Math.round(cy + ry * 0.6); y++) dot(cx - rx * 0.05, y, P.dark);   // 손가락이 접히는 주름
                }
            };
            const limb = (g, P, x, y, lw, lh) => {   // 뻗은 팔/다리 막대
                box(g, x, y - 1, lw, lh + 2, P.out);
                box(g, x, y, lw, lh, P.mid);
                box(g, x, y, lw, 2, P.light);
                box(g, x, y + lh - 2, lw, 2, P.dark);
            };
            const mk = (src, view) => {
                const mkc = () => { const c = document.createElement('canvas'); c.width = w; c.height = h; return c; };
                const cv = mkc(), wa = mkc(), wb = mkc(), s0 = mkc(), s1 = mkc(), kk = mkc(), gd = mkc();
                const im = new Image();
                im.onload = () => {
                    const half = w >> 1, r0 = h - 11, d = 4;   // 아래 11줄(종아리~발)을 4칸 위로
                    for (const [c, x0, x1] of [[cv], [wa, 0, half], [wb, half, w]]) {
                        const g = c.getContext('2d');
                        g.drawImage(im, 0, 0);
                        if (x1) {
                            g.putImageData(g.getImageData(x0, r0, x1 - x0, h - r0), x0, r0 - d);
                            g.clearRect(x0, h - d, x1 - x0, d);
                        }
                    }
                    const draw = (c, edit) => {
                        const g = c.getContext('2d');
                        g.imageSmoothingEnabled = false;
                        g.drawImage(im, 0, 0);
                        edit(g, pal(g));
                    };
                    if (view === 'front') {
                        const fw = Math.round(0.34 * w), fh = Math.round(0.20 * h);
                        [s0, s1].forEach((c, hand) => draw(c, (g, P0) => {   // 정면으로 날아오는 큰 주먹 (0: 오른손, 1: 왼손)
                            const P = skin(g), fx = (hand ? 0.73 : 0.27) * w, fy = 0.35 * h;   // 가드 주먹 자리에서 앞으로 나오며 커짐 (어깨는 뒤에 그대로 보임)
                            g.clearRect(hand ? Math.round(0.70 * w) : 0, Math.round(0.34 * h), Math.round(0.30 * w), Math.round(0.21 * h));   // 어깨 옆 가드 주먹은 지움
                            fist(g, P, fx, fy, 0.16 * w, 0.11 * h, true);
                        }));
                        draw(gd, g => {   // 가드: 양팔을 접어 두 주먹을 얼굴 앞에 모음 (상대 화면에 팔이 올라간 모습)
                            const P = skin(g);
                            g.clearRect(0, Math.round(0.34 * h), Math.round(0.30 * w), Math.round(0.21 * h));                 // 어깨 옆 주먹은 지움
                            g.clearRect(Math.round(0.70 * w), Math.round(0.34 * h), Math.round(0.30 * w), Math.round(0.21 * h));
                            for (const m of [1, -1]) {   // 위팔(어깨→팔꿈치) + 아래팔(팔꿈치→주먹) + 둥근 팔꿈치
                                const X = f => (m > 0 ? f : 1 - f) * w, ex = X(0.18), ey = 0.41 * h;
                                arm(g, P, X(0.22), 0.28 * h, 3.4, ex, ey, 3);
                                arm(g, P, ex, ey, 3, X(0.33), 0.20 * h, 2.8);
                                const k = (x, y) => (x - ex) * 0.5 + (y - ey) * 0.9;
                                blob(g, P, (x, y) => Math.hypot(x - ex, y - ey) <= 2.7, (x, y) => k(x, y) < -1.6 ? 'light' : k(x, y) > 1.6 ? 'dark' : 'mid');
                            }
                            fist(g, P, 0.33 * w, 0.18 * h, 0.115 * w, 0.08 * h, 'plain');
                            fist(g, P, 0.67 * w, 0.18 * h, 0.115 * w, 0.08 * h, 'plain');
                        });
                        draw(kk, g => {   // 오른다리를 위로 들어 크게 앞으로 뻗음
                            const lh = 22, a = g.getImageData(0, 0, w, h).data;
                            let gap = half, best = 1e9;   // 두 다리 사이 빈 칸 찾기
                            for (let x = half - 6; x <= half + 6; x++) {
                                let n = 0;
                                for (let y = h - 12; y < h - 1; y++) if (a[(y * w + x) * 4 + 3] > 0) n++;
                                if (n < best || (n === best && Math.abs(x - half) < Math.abs(gap - half))) { best = n; gap = x; }
                            }
                            gap++;
                            g.clearRect(gap, h - lh, w - gap, lh);
                            g.drawImage(im, gap, h - lh, w - gap, lh, gap - 2, Math.round(h - 12 - lh * 1.3), Math.round((w - gap) * 1.3), Math.round(lh * 1.3));
                        });
                    } else if (view === 'side') {
                        draw(s0, (g, P0) => {   // 어깨에서 앞으로 쭉 뻗은 팔 + 주먹
                            const P = skin(g), yc = 0.27 * h, rx = 0.14 * w, ry = 0.085 * h, cx = w - rx - 1.5;
                            arm(g, P, 0.40 * w, 0.29 * h, 4, cx - 0.3 * rx, yc, 3.4);
                            fist(g, P, cx, yc, rx, ry, false, (x, y) => x < cx - rx * 0.4 && Math.abs(y - yc) < 3.2);   // 팔이 들어오는 자리는 외곽선 없이 이어짐
                        });
                        draw(kk, (g, P) => {   // 앞으로 쭉 뻗은 다리 + 발
                            g.clearRect(Math.round(0.36 * w), Math.round(0.70 * h), w, h);
                            const y0 = Math.round(0.60 * h), th = Math.round(0.10 * h), x0 = Math.round(0.45 * w), x1 = Math.round(0.84 * w);
                            limb(g, P, x0, y0, x1 - x0, th);
                            limb(g, P, x1 - 1, y0 - 2, w - x1 + 1, th + 4);
                        });
                    }
                    drawStartArt();
                };
                im.src = 'data:image/png;base64,' + src;
                return { cv, wa, wb, s0, s1, kk, gd };
            };
            const F = mk(img.front, 'front'), S = mk(img.side, 'side'), B = mk(img.back, 'back');
            F.cv.side = S.cv; F.cv.back = B.cv;
            F.wa.side = S.wa; F.wa.back = B.wa;
            F.wb.side = S.wb; F.wb.back = B.wb;
            F.s0.side = F.s1.side = S.s0; F.kk.side = S.kk;
            F.gd.side = S.cv; F.gd.back = B.cv;         // 가드는 정면에서만 팔이 올라가 보임
            F.s0.back = F.s1.back = F.kk.back = B.cv;   // 뒷모습은 기본 그림 그대로
            player.sprite = F.cv;
            player.poseSprites = { wind: [F.cv, F.cv], strike: [F.s0, F.s1], guard: F.gd, kick: F.kk, walk: [F.wa, F.wb] };
        }
        useImageSprites(p1, { w: 43, h: 66,
            front: 'iVBORw0KGgoAAAANSUhEUgAAACsAAABCCAYAAADOpi9SAAANdElEQVR42uWae3Bd1XXGf2vvc67u1cPvNxgwxDIOtgEb87ChBefRgZIJJtNSUvgrk2baIek/Tdsp6UzoQKeTptOZlDaTtCFkAkMgEEgCAyUQEkMNfiA/sGWQZctYlm0ZS9bzPs45e6/+cY6uZCzZepgwncqjsX21dfZ31vnW2uv71hGm/qUTXC+T3UimCvJbs5dQMCECiIKV9JKS3YIFDIaf9R4kUuXlJJr0vsFkgd4/+zJmoDjgz559BNUMf1s7yX98G1RRVSr72nklt5AcoAifCwr8MinpZACbyYY1DyCGr/3oYRRBnUMPtqM7mtIoi2BFqW1cxLq4kz9qWMgCzOQ3nApYK2BEkDAA9dDWDrt2gIsygvlsoSEnnhwFNky/FJGPAawAgiLO4Q8fQ3duR5MKqEc0BapGQGDa5RciQ1yeQmSDqWSXANpxDHlnF4oHVdj2P6MikqkinUpkdagcGAEPUkWi1UctOlzVPAZR+bjAfqi8eqnStPojHRlZnXBBPo+czWLptRo79ck5WD41uJPmrJGMCqopV5veQjVGBcyHMPU2H4FwLtbYKcGdNNg0w4R3H/8xS6N+rHdIdgN+JDU1ZbeqouiUcszwf+jLnCPZx/rmP7vaiNURJw6fuPRjVcQPfwOoVxIJqFDm+cFDRGffY8KNjN5m8+SyZ2pkRA5lq59LStXFG8Na/j4osHTFhRgj+JGPWqHY2sHLZj6P9+ynT5XNLub3jB3eTIbYIryeJqhMCOzzN99CXWDTYKEYMTiB7/z6DQAidbzoh2P0haDAHQ0XU5MVWJ/1Bl6VlkovrxRPsFUTrAh/u2QlN188J908NKgaQHl5SzMP9nWcFeyoCVZXE3Ld+psQ9Wkeecdbmzdz+0WrAHj2/R181uZwKEagIp6WcjfWyPBeIhgEDIgo14nFWsM961ez6DO3ABAfPoxFIE5ofbuN+2vn8VDxxJgd2aicXbv2esTUoAriPRLFrEliAoVAU3IZICeQE8EaCCUr+pL2A5JF2IhQI0JowKJ4V0GDEA3CdPM4QtRTrwYvyl/VzRuzoR81supiXP8pmr7zX1y9fCGEgouVzpOd1Yb6D69ajbXwxfU3AELxsSfoT5QmmYERwQORCINLGvgTcwlPvb0Vr8Ivdrbw5VlvppHatgnvUt7e5LrZjZComVidLf7mRSplz79U+vi3Fk8htBQFfl06BcCtV6zk3nvugVxIuHAhALXFQQrliA3Pv8CrOpf1vptcAIXrPwXeI+8dpQS88O47zO8sAnBL0kWN8eQuWwSq5LyhdJZKPGqCtdXPJhThqCj/NNDDALBEDKvXXg/Avbf/AXrsOCxZgrEhFAdx+1tg307EORIEi2KMoGIQgYGWLt5Sxwlp4MWegwCURflafjqXi5DH86Qp0O4d/zxwbFRso8Y8zpqOOpPHIzjgkIAxgjGCBAFUytDcjI9KEJVhXxNGPWIFawVjJT3JxKOi1C6ZxjVAnXoGUAay86zTQ0WFijFcJpYLg9zEItvcMBtvA5rtLCzw/VMtGGN45nvfTRdsb0J2bUW9H1YEQxf0Wu12NSsO1WxxcHjPMb5a7gbgz/PzqRcBdbh8HfVJiVgTPt3fOSq2D3+gP7j2Br54992gin/qUQb3tfPbKEdiQ5JCPQCfS44TNF6AGFMFqEZGgB3qw2RY5qoB7zm85yj3RSn3f/qn91JTU4PZ/SYIFFuPUtSA3+o07u1+7wx8I2mg/z53OXd/+Uv4N36D/+mjqCr1jYtYhMf4iJ90vcdPut7jNZlFpbUbH/m0QckOA9W0XJX2d+B8eqCkTZmiuPT/I85WW6jDjDjNapcsoi5fz7VxH/847ZIzSthpnDXGpJ1qR1va8RvQQFi2bC4L1FMUpShKRQKaNKDS9gHqQJ3HJx51HnVKWQ2VQ4MpevXgFfVKR2uJisnhUTxKfvUqzNUrUZNRxkJ+cS0FSQglOHvpyuKDl+F/K5DPG1asWoDZdnKozaaLAm9oyLrW9szgkKpI/JXMY0X5FA17eplXm177cFEYNDneKUzDlNN67VWRKk2yYxqYs/wC/LsD566zUu3pdVgNCORU+XYhPdNbEZ7pO0QCPI7yqYaLCUTStFIFA7tyM9PfVZ/2FwXBoTzR3YIZos0Ijqf3qqgK5dYjCDPODva0Dl9T3YSSRVoY0n/7Bo/jMmlzZ91iQueolzJXa4WisbzKLKwRbkXxURcVD6+q4QNv+Ux+Dr+qnBzWZdlFpSruob1kINSz9wYVFBfH+Is/kf5IIfEO75S2d08SARHQp+kDsyLkgEA9K1FCA9PFUaOeW40n+OQC8kYoqKc2A5STAFFBVHjk0SdxzS0IBnWKTzyH9nUxiCXWs4OVr55o5vtffwC75gbM5+/CqRAfPEFLcyd9ccJLHl7y8GoySJJFG41Z4fuY89A3qHvoHwiXXUQN4Conkd17KTz4AACFcBqX5OspS1DlWqQRjzU1YW7bSHygg/f2HqcrTthsari/7+AZpWvUQ+HhGY2EkiZz0XtUoILn73oPVhddaQx1Yrg9P5c/JmJXOJPYWoymTczqShdehLdrZmIzveZF+dfuA3SQHiRHffr3Y7MvJ0ociVFKwF+eah3XoXAuz/U0KXiFtay2eTbWLeIKGzB32QxcuchrbRFrgJlL8+Rv+zwDzz/HKweK9ACP9hxk67BklzH2k4mo2ykaPRP2hse131TUrex1jkiVirGpZgttZh0pBjA5i0ra0PQjVBDETN45CM5XkOK4hxM7umk20wEhcifp3HmS1/c9AS49LPTjcmRGqlMR5cJv/jUILHriR7zUUuKiKy9F8iGL12/g3W99l2256YTGjIQ7Yfd7ymBTxa6UnvwxNbFD3+9AdA69ezoxwOamJ7kU5Ubfyy48V0mBhbm0Cvw8Kk4I8JQdGVVTVbKaN6hCDRUCPwg6SI2PsEaYJ56bRGgQi8103O+SBlrtJZZfiFl6EeIdoXPcuO8ISJpka7UXgnRxiOGahgUc7D/yO+Wsbsw1UGcMD352Awvu3Ej8g4fRSgUEwsbFZ9xXtP8IUdYgWZ1cok2aBjlRDMq8318H6rA+9QVA8Qc7cAfaYcgDEyW87AKMaaAxGmQZOZaRY60NJjT0m5JN7wQknwcs6h1qBAMM+ICSQunoCSrGplXXQP2l9dT5hNAYQmMIgNUTADxpsEYVowI+7cC8d3j1ODG8LtP5Sv8AX+nq59WGeZgv/UUmXzwLaxIaG+bT2DA/bTP1o+WsXhWEbFi7hkKQR5ySbNuM5AK04vAHjrB/MM+A9/ihCU4m0MQYwqUXQWtphHGvHy1nV9gaCjbHHTfegGvei9+5HU0SxFh6SrDJHaeE4gT27tzP9qefg1XXIzUF8AkbbA8bbA+fDhqYZgwrrR0XFSYFtkaEjXfegVwwH7xi8Gjiidq6qBBSUiijlFDK6kicw+Vr0RVrwAiFEAohNNYFrDP1hB9RZKu1lSC1Qofcbdd2nCQq02JCIoUdzrE9SdjU10HbnnbC5ZfDylV4wC6ej108n3ozl+XTF+LGeYhNhLN6nU2tnZuvuRqCArgKfvdWxBj6IqUswoFCPTo42gAktZFSH1UyN9LjhrTe+U6wpRnYjXd9AW3ejQ70Y4wQ7e9gMCjQrHCg/2gKasSj2N3XyZofPsLc6TOYecW1VH7xfOapzcAIqaF8vmkwJNMlCGGgF1ycyhVVduLZFSfEHpIPBbasnrePFPmgvw+XC3DO4ZzDAjnMuFuZiXF2yGjzqaegIqCeYwOePYMRpcSzJelnp3PV1VudoynuJ3bCrkMlcA4xihglR0yijhuklmvGcTgEE0+v02e34tNqabNPZIzf6+w9jhGh47HnWHzlBQCsO3iCAbUE0xexJRWJ55MGMjz9dh7xSQpRwYhBREY9kYbmC9YI04LTh8+14oesmf8fE8azclbUM/L9kXRAc+65bI16QvwZERcZX/EKJknZ6qBZq6MvSTeV0bVPUF0z2jXHp24mBNaeZtr56haSmXoyVhelygkRpqHpS0AjoBoEzbyv80UDXWtzVWD//dwLuEMdsK8Zn/bW6cMd/VnKdu/YEndzyju2hLOrznfshN5E6beCoKw8R/kaD1hdYwMagxBjLMZYnDp2V3rx6tFsGC1koR1jLwfs8H30miAjuTAQK1tjT0Wg1lgKIqwwwcQmjKf1rjbgrtmfwIzgW8fedjoUWrXCHUERU51su7Mmp4rQNeKjH8ZKEdC+Lq4JZmU3pewpdU6Os9fl6rjvgb9BwuGHUNmyCdO0HQgQV4t2H025IBaMydTDh7Bqqi6E4X7861cuArH4T15Nbt16dKCMj4q0f+ObPB0NnJF1wbmTSnjl2WdoNJYFu7ZlLWFCf6L0uzy7g1p83Rx8qa/6gsRYtURJ7dCTe45UpRECNL+Pe/qX9ISz2GVkTKkTnLu0eja9sRnmzGSmJtUBSE/Z00yZiq1FxZAoNEUnx5Qpmv1JNOZUFvm6bEymiaJ4mqWfN0t9Y7aM56oXel9hBgGk4jCbWEtWU4XsnQKE1+IPqjVzm/NneLlrbPrSpBEh9cZHLMiSwWSHgwJPRQPjcr7HayyP13ud7HXOuMb/AqYbXTjdINGhAAAAAElFTkSuQmCC',
            side: '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',
            back: 'iVBORw0KGgoAAAANSUhEUgAAACsAAABCCAYAAADOpi9SAAALgElEQVR42t2aWYxcVxGGvzrndvfM2DPjWZxgO07sRGRFwCP7EhzWYIFEHggvKFJWZVMkHhEiEhJLyGKHkMQQoiiAUIiQAojFcRYcK6AocRwQzuIltuOxY894Znq2Xu45xcM5fbt7NvcsCYKWerp7+t576lb99ddfdVpYnoe2cIwsdRFZDkNvSnpAPYJgsgsLogooinCXH1nymrJUb95kV7Hl0F7UGFQ9cngA/+JLoB5fduy5/Xu8YFbz+sRhjqnjN+nootddrLF6scnxKbuSu3e/gDlvLZwYRg8cxux9lcmtd2MATVMq3vP0qQLDWuHVygkOlco85scWtbZZrFs/TDttgO3Ig3fowbeQfW9AWsJUq0i1ikHJi9BFlRwFLsyv44wlBHPRxiYo3kds7t6H7HkZpiYQVSQa5FEE5SO9HouACNpSLs615mJxIMEk/9ob+CNHqGx7EClPoYARcCgWwYliNHyWaPC7biwaDGbvv6nc/wDgkGlAdGg8DqxAVRVZvGMXD4NgmEfLZdQ7jILPvo1hjwukgKgsAQBLhYERrAqlhx7CNtyB0+hKNHwW4a+DeRxKgrZYPxbmWZ3jWfesBxFhx8m6x0TB1qAgUAWeOekZ8UoFxaliWF7M6gUm4aO0h3qkiorwDOMc8E5rtlhAvecEhr8OGWxkAY2GCkqqnqMq5MXgXIm9pWNs9cVF87vhf+gxq7GX2i5WmDydYlhlDP0Yvmg6m8rsTpmiYgJGJ4FxsZTEICY6TQwihpwIJRyvld5mTx1JiwKvzBAltps7n92O5hPMzucoPfAgz5xQplCeGxsA4B6XiRJuNd2IKBd2nUOfMXyut4KG3KIqsGsQniwe41EdJY/hClZmhSFCouXS34hZvcWu4o5dO5i66iq0UgEjfHvfUS7s3oBFGqgJvmm76cSAplyea+OD/Y6cOkRBNZiTAJ/sg0/0raHtkGVKPd677Bo3mO6suNznRvR0BiczZNSLe6BaRVRRVd7fvZ4D48eZ8BUkVp+7e95Hn63w8R7LmutuQMoVNJdQfvgRtDKJiASDraH9mhvQ1HHbQ9sQl1JGeGowkN3qxJGmyglJuKaoPOhG5zXYTGcsHRsN9V2EkgpVQPMWFTAIBmENhs2rLD0iiEvBGsR78pddCjYJNGstnLkGRJGcoU09bSJ0C6yywiorfKRP+PhqwyoxdNkcm5KueYW8NMOgi+9uWIdFqSI8fSrHzrEj3LHzyXDErl0ATN1/f0b6RP5XgCSh47rrmfzJvbRfdTVePZVf/LzhgFAvpOF97f+/HGrj1eJBxvH8PJ2d3mYk2MM9H+Sr/RVKeH5w4Dg/eOov8M+X0dRR/sm98SidM1gqEr8Pr60SqgK3HxjgFPCQm12gN8JAr7edbOqrgveIj3e+5xVKbx6m9NP7EI1ekXm6L1V2DOZQlfphevrOLSSmj61QC5gtiKF7ZScGxYhHVaE0hn/id4h3qCgqmiVaY2w8gosd1xQWh+IJJVel+dgayXpoYpjTKUjT7BRL/sqvQ0c7k9Zg1VHa9jOMKirgjeBNLKkZ+YeFnxjK88ehNgQw0WVVhD+dKqASz9FGxQZPDlueGs5TA0uHgJ9HQzZRl0SsfWfvAc5A+M7G9agqImHh7SdzAHypr1IPYYSvCT1D5j5VKIhyeX+Fxwfb+UpviVz0Y83Te4pHqEiOYV3P13rLfOvcsxhW6Dh4nHvT4Rk0lsxU1IFfh8WEkNTCrMq/x47Gk9ZyWV8VELYP5RCED/Wm9ONm4FNU2dxb4u+DlnESElE29acAlDUA6Ks9ZUARD20wp0BvLgoSXHJO53pWulLTfXmUKQ2eSZEQutgBAPSLI3RYYU5Q854oFNRzSZ/w/EiCKhSjh/sxnNnei61Rm0AeKCQC7rQSMSC80xi6pIPaGRqbllpNT+I3OVU+01Op31SNN6e7RqAHxxd6HCrC7fuPA/CxzrUUJKZnzCwr8O2zz6B6ULlnGhSS5mzzlLY9wBV9mhkpwI6Twig+u9ldo4cY9mvpFctlfS67mmaTmGlgix+cCjtP1nNahKzL0Pi5MRfmZQMPPDUU01sDfp8ZFIbTSXaPD3BXOsxd6TAI5EhIo+5vDDk1ntSZfBooS7J3z40NcMhNsfOUDaTntX7+LMBtMrasygTKKyMBlxPAIPDP0gh/9hPZcSfx7K8eoyxpc9SFjKZm8KWCwzOljjQ2kZMoe6eGmVJPqSEWUyqnTTC53xd1xdhxkpVnMjhkEAMvjR9ja9o8VHs0Leq12kmlNMBX+tZk8auBx0yTk7UzUxGeHzvKllBO6xEdU7ys49N9ghfhz0OG2Qr19B5Mflw9pVcXU1aokBq4d45BmkcoI/x+KM/m1dWAodgpOpkWMoEnT1iK6hsvlb3Zko6qFGFX1C8KbAkOktM1jLLNFTUD8RySRQAvYDABa1JPms/2lkkaxI4qlDBUxYa2eJbL3ZOO6umGhsk7OLdd9onmortb01DlpwulfOQulQamWAYXLHoiI6oUAK8pRqZPQKZLP7Ciodrpf8FYIxYrni+vruLn0uJaz7vP9aeMoOwuGppqyDs85NBv2G4KhXY62tcAQuHW22YQqyqoMRRuvi3UNQ85hJ7CWq61PVxre1ionxfl2X5VusxqciLQlockgLOm8qtIkLvr1qOmtgUS/uZNnrZ3EwZKkJFVDPkbb6T6ox/WplwosH2wwObv34J3juqddzRVTqWhpL4bxppoWkGV8o9/iKnVK43AEmX8zjsoREkZyq9kxUSWxECLeLQb5awEfjXQ3I8p8Hq5hPUe8VG6iHJc4bdvWy5I0sWOuhZsbJhoWsslidKmjglyjCGUgYrAH457xl3KrwdSKkAJKAk8/nbCJIYVQM4YcsawyXYuKMkWEhG9xXYDsK7jPN5rwzjpjTShmJbD8EIEI8JY6S3ac+9BjM1U2QprKYhwnlX2p3kA3prcTxHHz1xrM9sFYbaWRBfnHGgIykXWQRIG8OMo/yge5lk/xke9pyCWS7vOnpaacH4SerDD6hcEBrMwY+Ptx2GHqGnobCGv4BR2q0eJAwvV7LV+Xl0Dm3c+wbTpEsEW4a2UTFV5CXtgrnHI0dST+KYuY/mNzZSJNCwajN/nLONSH6lMYHDGst/n54ajMO+4aIk8O62bEwH1IHB0cl8cqoVkecSNKg5udVUu7N6In0MMLYR1F+RZG5+idVWtIhz0SegOZHbttc/l5nCssJAUa9VY3Zx0ITZBbNIsWgSmvCcFdvjJGSdWxDOJx4tpWDJAqadtHQVjltVYvcasZIMaets20tu2ccaI88jEAbamRQ6G/YLGuMp9boKjE/ub9IBIqGoF08Z72s7hRtPVUnFoCbOOBIPygZzL5J8RwceNYzNLEzhDLzbgvda5XpRTKiocaxG3pjWsusgEkTcb0kKbWGGutKz1NjaOmOr8a9TXhdD//Q7jbIwlzTUs7H5P99xpBYifpmV9tMAso7FSC3vjgD0aaqR5bD9rLVEqImiNEYwFY7Pq1epPUUxrB03zXbx2iuFfadISV75aNbxerbXuDlVXj5rqcmK2Ph/Q+pYWXpSByQNsmV/iyVY3xvGp/ZRcBZVaOxGfusyYTYxhdfs6mnbpYvga92Lne6TqGSwdmSUZBMkly2Ks3pR0sq5wLnlpr9sqAmKyWtRy3yZmZusphrWF87k5CPt5+51kPsVyY9LN57s21HesskFx2A9biHAOv0TyiJosQVUgJ3BJrsIl3RsxxYMcFXisOvuG82ye1fNsws1JN5d1nt2wwaoZmdNUi1qvPgZmThHVY2IifLpzA+fmLVfa2cvvrJ7dpB1YDeI4VRcbGs30S23cvqd4tOV+L5zjqTbN7TXu9fqsBekoQS/SOgySuJX59Mib8xNE1AitelaBv40cnKVdjltVcTJmFtjdLrSplxadu6Rr/geTjGbSobyvlwAAAABJRU5ErkJggg==' });
        useImageSprites(p2, { w: 38, h: 66,
            front: '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',
            side: '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',
            back: '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' });

        // ===== 피격 자세: 맞아서 뒤로 밀려나는 동안 상대 화면에 보이는 그림 (파란 원본을 플레이어 색으로 바꿔 사용) =====
        const HIT_POSE_B64 = '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';
        function buildHitSprite(player) {
            const c = document.createElement('canvas');
            c.width = 96; c.height = 99;
            const im = new Image();
            im.onload = () => {
                const g = c.getContext('2d');
                c.width = im.width; c.height = im.height;
                g.drawImage(im, 0, 0);
                const d = g.getImageData(0, 0, c.width, c.height), px = d.data;
                const n = parseInt(player.color.slice(1), 16), tc = [(n >> 16) & 255, (n >> 8) & 255, n & 255];
                for (let i = 0; i < px.length; i += 4) {
                    if (px[i + 3] === 0) continue;
                    const L = px[i] * 0.3 + px[i + 1] * 0.59 + px[i + 2] * 0.11;
                    if (L < 45) { px[i] = px[i + 1] = px[i + 2] = 0; continue; }   // 외곽선은 검정 그대로
                    const r = L / 122;   // 원본 파랑의 밝기를 기준으로 밝고 어두운 정도만 가져옴
                    for (let k = 0; k < 3; k++) px[i + k] = Math.round(r <= 1 ? tc[k] * r : tc[k] + (255 - tc[k]) * Math.min(1, (r - 1) / 0.9));
                }
                g.putImageData(d, 0, 0);
            };
            im.src = 'data:image/png;base64,' + HIT_POSE_B64;
            return c;
        }
        p1.hitSprite = buildHitSprite(p1);
        p2.hitSprite = buildHitSprite(p2);

        // ===== 가드 자세: 상대 화면에 보이는 그림 (파란 원본을 플레이어 색으로 바꿔 사용, 어느 방향에서 봐도 같은 그림) =====
        const GUARD_B64 = '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';
        function buildGuardSprite(player) {
            const c = document.createElement('canvas');
            c.width = 81; c.height = 132;
            const im = new Image();
            im.onload = () => {
                const g = c.getContext('2d');
                g.drawImage(im, 0, 0);
                const d = g.getImageData(0, 0, c.width, c.height), px = d.data;
                const n = parseInt(player.color.slice(1), 16), tc = [(n >> 16) & 255, (n >> 8) & 255, n & 255];
                for (let i = 0; i < px.length; i += 4) {
                    if (px[i + 3] === 0) continue;
                    const L = px[i] * 0.3 + px[i + 1] * 0.59 + px[i + 2] * 0.11;
                    if (L < 45) { px[i] = px[i + 1] = px[i + 2] = 0; continue; }
                    const r = L / 122;
                    for (let k = 0; k < 3; k++) px[i + k] = Math.round(r <= 1 ? tc[k] * r : tc[k] + (255 - tc[k]) * Math.min(1, (r - 1) / 0.9));
                }
                g.putImageData(d, 0, 0);
                drawStartArt();
            };
            im.src = 'data:image/png;base64,' + GUARD_B64;
            return c;
        }
        p1.poseSprites.guard = buildGuardSprite(p1);
        p2.poseSprites.guard = buildGuardSprite(p2);

        // ===== 장전 자세: 총을 두 손으로 잡고 탄창을 갈아 끼우는 1인칭 그림 (파란 손은 플레이어 색으로 바꿔 사용) =====
        const RELOAD_B64 = 'iVBORw0KGgoAAAANSUhEUgAAAKAAAACgCAYAAACLz2ctAABgcklEQVR42s29d5il+VXf+TlvuDlVruo4naZnejRJI2lGowBCAUlgWIwk8Bow2GvsNQavzTqswzJi17vGi3eNjR/AK4MXWwvLmmyEAQESIyvMCE3Q5NS5uivefO+bz/7xu1Vd1V1173urqmd9n2emu2940+/8Tvye74FdXiLcttdtPPRtO6/s8Hc5oHPI/0/3LSn+LSmPL2OcZ+iXJOWPZIwb2SrUcoALImM8pIM6j4yxiPImCpSM2CiS8h7HuXZJeU1b117ezJ0kY9zwXoVEbsP97Had4y7oQQubHNC9jdLgsseNL2Nsllt+f5A3J2MK4u3SErfjnsYxX3sV+HGOM2qBxxE2OWBtKAehEWQfD+92+D9pNU/aRUjr/0iKzbYXDSn7WBfZp48qB7i+ssfNbB+IkMruN7IfB3in3+g4Cyvm+3vRwLLf3XyAm1P2aG12fKay/TM9IK2tKTep7scXGtf+78VkjrsjZQzhlgNa9N0+OGh3YpzNLGNq6f0EH3s5956CRtnDe+Oo4rFvVPZvqhhzQQ5iMx1kikf2oTT2uqZ7zYTIGJt3z479fi5U9rER9htF7jdvJWNoGmH8tNUo7T6u0AjpLcZe3JVx/Ow9Bye3wx9Ktdgy4kHIm5OO2e+DlDEXRsZ0T2SMY6bZkJJSeUhKAd+zqZeUJxrHb7ndDvxeFjyt8B10QLKXlFGqKF3251PuVfvuxVfd9aHcjjydjPng95L0HbcycLtSSKMCor24AntJhI+6Z9mjttpLjnQsX0/G1AiS8sHfTg04buQlYy7+uAHQuJFimuve1RxKeq2/3xzkLdcqe98wQxdtmA/yZpnYN9uUj7vxxnVF9qLB9qNI0qRFRvraqXxUSeXH7ysPlraOJ3t4mG9GDVVuw7llDOuwn40iKTfCQeZrx03/pHU/DkQ77De032sAcdA+4+147SUFdDuvf5zS4kFtwgN/9gcZmLxZpneclMVeU05ywJssbfojtUDI8Dqw7GMD3JZc6zh5noNMR9xOrbqX9EwaH+p2+XhpKw3jIlr2LMRjCuCBb9qDBpOOSgXs54YPSiPtt/JwOy1E2mrMfmBWb1bQd+CaYy8+3biqXNg7Xm4vvszt0v636zz7TSUdhNUb+/mPo5n2svP3WktOE+3tBVEzjsYaxzU4KJ9qv6ZuVLJ5r/neUf7qgbhQ45SMbod2POgo8Xb87r+UiHuvboG8CWsit+MGx+n7OAgH9nZGzGlLdPvdfLdoFNl7ALInQZCDAecepADaHLD2eTOc1YOKkndaWB3yXU3x/igBABDLRuwcYruQRDuiicftStwP/lDGfJ8xntuo8zu7PcSd/p1mwdK+t/WlKQVg47s64jhpHoCmPO+oY+uIf8tNHwpw+uxb8Lt1DYKApSVPUB153K1rcPMz0JT3O+rebj6m7PBbHfIc01zDLddyUBHhm1Gr3esuH2Ve9wrVTxttP/zOR5mZmdGpQ2e0WJ1hcnJS/8UvP64f+8HH1LKsA+nBfTOsmKQIZsa1VnKzdhlHg/yX/hql2Q/quDtp6Q2Tu3DsLip5tFwuc/36dY7e+34iv015cp6vfP4P6K9dkCSJUE121xJjXv+o76V1NWQHCzWutRl1bms3szZU88ntE5iDzDnt9iD3m7va6o7IFpiH3mS6soUKZx78RnUch0wmw5EjR3jfR76D4sRRXnj6T7Eti2yxRqEyRa5YA7F2vU7ZRRB2en5p3AlJ4VLoLv/WMYKXnbridoSP7dWO73W3HrQWHaU99uMw6xjadOv3z779I3r49Ftw3AwXn/hVFhYW6Pf7PPRtf4uVpWssLy2ycvU1SpVJWs0G55/+Qwl7TeIk3vNzTPscDnpdZIhg6pib/bab4L38fpjQy007Ww/oPPvS5JbFuUc+qodOvQURCxAufOU/sLCwgO/7fOB7/xGvvf4GmgTYloWIcP7l53n+K79PY/mC7PV607oHaQREhgQfo363H2uzu0QL2wK2/UbBss+bkAMQOtmnqd7tu3fc/wE9edeDuK5Noolpklfl8ld/iyNHjtDr9fiGP/8Yly++hiYRkCBiceX8q7z61ONcO/+s6OBh73Uj7ZZl2O1PbuPG3e1zK01qZPMAOjo1MUwzjTrHODdzc/pgI7G7H+eYFH5WWj+xUp0gigK67SZRGGBbNo7jctd7/xzXrl0jk8nw+C/9OEcOHyaXy+M4GUSEw8dP8cB7v5Ujpx9ERPYlDLqTz7VD2kVH+IjjImnGWU8r7e7REcnVcW3/OLm0tMdQ3dvv2GGxNIWjv9t1G8FR8sUyYtvoBljdEqI45ux7vpulpSWy2Sx//H//L9xx/DiVSo1sNk8mm6U6Mc197/4WPXHuHduCnHHuSYYEZWnSUJoigNkmqDJ+DnVXARxnHdMu+u1O2xxUYJ4mgtQdojy56ZnUV6/R77bIF0o4tk0UhYiab0VRzIMf+n4WFxcREe6/705++1//fV5+5kla6+tkszmOnzjNOz/wZ/XYXW9NlbOUIde5a9JadhdMSZlN0C33LKQ73q73M8x/20sOSnbxQd6MnN+bEVHvfI/C3LGzREmiR+96O/NHTpFEAaoJbia7aTUsy0KBVx7/ZSYnJ+n1ely9epWFO99NbWYW17Hx+x2unH+F5SuviddeS/0c0/q1mwROOl7wN8yHHHm+NK7OuOW0YRe518h2P0HJQXyHFJtnp/cm5u7gxLmHtd+u4/sec8fvpDo5h21b29wWEQvVBMt2eOXxX6JWq9FqtZg9/Qir9TaB18HvtXCcLF6/w+qVl8XvNVNdy0El4GUXt2S3iHpfQciuidYUEq0pfEYZodqV/ePgDlK7aoqAZKd7zOSKGqtQmzuGbSkrl1+l325gO47xDTfNXgIISRJz4pGP02w2qdVq1C/+Kefue4jJ6QXmjp5h/sRdTB06QWX6qOYrs8guV6MjAsGx00gMrz0ro2nXJIVfao1yZPWAFlxHCLeMcHw15TlHgS73nZ8ascPXFs/L2uJ5fK/Hwsn7yWQzLJ5/nsbKIpbtYIm9mRfcCDAsSzjznv+aVqtFqVTiG9/3bmbn5qnUJsgXSuTyRSbm72Dq0J1anj408uJkh2h4VJS6l+etI6JmHXLcjZd9u5z52xlspOVGSXOctGmVnTTxTr+xsmWy+cJjbjaP7bgUq9N4nXUaq4sUimUy+RKgiIIO8kYyiJwnjt3L4itP8vLX/oS//vf+J2Iy9DyfbC5HNpenUKowOXfHY163+cl+pzG2ldgrgGRc5qtxXBx7vw99P4Td4yBtbjeX9E5maytgVFL4yABJ7HHH2YceczI5Os1VbMdlcu4YIsrFV56lUKqSL1UxEmh0wtY0zdyZd3DlxS/ztcd/l4987PtptXvEcUw+l6U2OUOpXKVcm32s12l8st9u7DtTsF+sn+zy67RrZo2bkxuVfB7HVKdNhCIHh2JJ48fpTSmmm5O6Q31kVdaWr1EsV4mjgF63QxhFWJkSmiS89uwXSaIAy7JAZVP4No4VhT1OPvpx6vU6//p/+qs8cN9ZisUiltiQxNi2ML1wlLc8+q1anpzdd4pJR0SmOsJ63HgWesvz0BRrYI3ynxgRKOiYWi+tJtQdco23SwvulFzd7VloivteuvC0XD3/EjOHTxOFHstXX6dYLHL05Fla6ys8/YXfJwojEN1etVAliRXEYvaeb6bVavGL/9uP8o53PMTE1DSJKklibPbE1Czv/jM/oJlcaawnk6ZFM20VSkblGYcIrOwkgLvleNI8+INI/h40OmYcTa277N5R0fmOjrYql178knQay1Qn5uh3Wpx/5etUpg5RzCpLl1/i0qvPYrsulm1hDUpuSaImQFEI/C7W1D3U63V+5V/8Xf70Mz/L1OwClu0Y2JZAoVTl/Z/46+pmS0OM4e4baNeqRsrof5xK124wr9QmeFw/bNQu2ks3lo7pUI/LcadDNL+OyJHdekzlxSf/kwSdVSrlMnHo02zUufe9n6BWzvLyVz/L+vUrWJaLiJjjD5zOXqdJa22F2tQ0Jx/5OKurqxSLRZ7+3Z/l2PETiNgkagQ2X6rw0e/7W3r8rneqDMETphGwtO7WMDLMcdt5hTHV8H4RLAel3ZTbCwtL058CoytHmXyFuePndPrQSVP9SGIqlTLPfeHX6PkR973rzzB95JSJhgerWF9botNscuj4ScLAp99aZ/31LzI3N0e/3+eRP/vfc/niBZIkQMSiVCrQ9zzeeP5pnv7cr4gmMclW32Uf6zQsqb2X/p+bn501LPm6Ux1c2Z3rTcfQZgeRcB7X/5QxHpSmzJONurbQ6xD6PSzLIgwD4jii1+/x0Af+PKV8hhee/EPWrrxughKUKPJJ4ohiuUyuUMLvdwlj5f4Pfj/r6+tkMhm+9Kv/G8dPnKJYrOA4NplMllptknsefAd33HFcv/Uv/G19x4e+V223sImo2Su34yifbljuT1KY46GJ6N1qhKNqh5AOQj6OORhHsNNshHFgV2mQIbueRxNaa9elubZEJlsAIApD1tfXePe3/SBee5VXnvoCa9cumGg/SYgCHxDCICAMQ7K5PK12l1MPfwcrKyvk83n+8//7T5iZmcISizDwePYrjzM5Nc3Mybdx/dLr/MBf+evc/bYPqlg2lu0wf/xuLddmwbL3bC1uFqJhEfSwVk/ZSQAl5e5P46DKkPdkhKN6kD2ossv50yRNxymqj9r9/dYySxdflOb68qaZjaOYq1cXeev7Po6bcek017Etl8Dz8LptHMclCAJEhFyhRJzELC2vcMfbv5OlpSWKxSJf/o1/QS5X4MWnnuCNl5/h0usv8+zXvszXvvC7/NzP/Aydno9l2cwcv08nisJkNa/T88dHNj4Ne+Zpn9du/SM3I3Bk2Mn242P9l9CT8P/nubc9R7HIlWeYPHRaJ2cP4bguaEKr2WDl0vOcOfcQjbXrlGqz1GaP0Wk3mVk4Tre9jiJMzszTrq/h9TpMzx+iub7G5ac/w/Hjx2m321xc9un3e0BC6Hvkc1nuPXuUZ19dQUkQlMOn7iebL3Hpxa9Qv/6aGBT27fXR0/iSFkM0wl4i4HHBqKmjrD3+bi85yLSmX1LkR0WEiYXTOn/iXo0Cj5Urr2OpggjL1xbxe12SKMKrX+aNZ/6Y17/+ZXK5AoViEVQRgThOCMKQbKGMZbtEYciDH/lB3vHR/4ZqtcrJhQLf+0P/I65tE/fWaK5c5Mknn6S3fhGv0yBJlI9/3/ci/gqddh3ZwQwfJEfMqOh563fscQ96EENabtc4r3EF56C03/DPhOmF448VyjUaq1fpri+C5ZDN5Vh85Ss4uTK4OSYOneHO+97Jhef+hNLkHLWZw6wtXyWbzZMAXr9LPl9AgW6rTrk2QbfX57VnHmdqaorFV58g5yTMzc0yPT3Nh7/vf2B1ZZ3A8wg6q3zp936F65dexc6WIAk/mcThbcm1jhvk2Gkz5bfbtMkIod8v4aSk/OK4w5hHad7S9DEW7jj3mJBw/eLLxFGIipAp1igUK4BggAtZojjm1LmHeOFLv0O32ydbqFCbnCYIfCwRMrkc7cY6xUqVXL6AIjzywY9x+cUvc+HCBe5+15/l2N3v4Ni5d3Lizvt457se5eLXP8dErUy5XCaTyXD4zNvxu41P+v3WbWW7TftyDrIqMY7tH+XcjsN9MqwqkeoYurtAyQ6I4bTVIUuE6fljmsnmWF28RqyKAp36dURg7vjd2G4OsW3iJOb65ddJ/Dnue/e3s3TlAknokS+VadZXcTJZbNshDPpMzc6Z41sWlYlJ/tpjP8dj//Af8MLzz9NZPk82X+KOO+/hxJl76PV6AHzsh/4JtWoNr9vkl376BZ1feJu8+OxXU6/VqGeu+xXAvcLnh13EMKFIA/UeS5uOaUOHXdu269KdhVluEs6dF0/I5fKEvkez0cCyXRQhDvu0V6+QyRUo1+axszm6zXU09Gg167jZAiuXvs6R/MOsLl4giWNs2yaOYsAik8mhCplMlpmpGl994gmi0Ke9fo047NNqNVm+vsjLLzyPZU9hORn++DO/yuobT+C6Lq7rcu3SayoioqpDm6yGCaUegGJyxtEY4+6QtJ/pkBtOeyMbTTF77cTbaSMM65LTwf+GLV5t+hDZfJl2c41ep45lOygQ+zFRErJy+VVsJ0/RdvDaa8wcuoMojLh4/hXufNuHeemJz9BpN5g+fJpiuUZjdRnLEsSysMSiVK6ScWwe/9znaK1dp7lyheNnH2ACh36/R7+5TNBdRyyX1solytNHyE8tMDU7T9N/XBqNxljrtFuqSUcolGEoHGuUsEjKi9mvLyZjCu0oQdpLFLwXczKsUnDinrdrNl+k3+8h4iADSJUmJgBIIo9et0noexRrMwS+RxTHJFHEK889yQPf8DHWLr9Ar7VGr90kDEOKpSqIYDk2TrZIFMfEWKxfeYlcaZLFi6/RWLlGFHhk8mWmj97N7B33sHDmrbRXLtLv1BGx0STZU3ZAdqlq7CVIlZ18wLSR8DhUDWnM+kF04o/LDZNG6PbCzrDxp+95LBy7m16/Q2P1OkkS35ICaS1fIpfNky1N0Gys0WmsEEUR2UKNi+cv8Oi3/iBf/I//mvXV6xw5/VYmZuZJkpicm2dhfprA92mtXCGOAs7c8xCNtSWiKCDwfbqtJv12EwQSbPwgIF+sUF9dptdpj+WO7FbxuPlZjtOPomkEUFOo1P2Yvb2mQfabMpF9CGwadgEBXn7i98V1XJ2ZO0p05l4WL79B2GvcdCMJK8EhrLv/NtzzEJpP0K4QNl0uPv8Ujad/nnvf8+18/fHf5Boxd5w+S4KQcV3mZyb48pefMPVeO8Pa+jqqAuKQL+eYOXyCJEkIvA7tZoOgtUi1OsHi+edorl458M3PCHO908Z3xlns/QjQfhucxm39HKYhR/mdssvn45hoBZIk5vKFVylWpzh09AStVpO618bJVYn9Nrzt3yF3H6d4bIb7TszyliNFLFt4cU155go0s/fTqvwNXrr8ac687UO8/rXP8vTjv8mD3/CdiFjEqly6eJE4URCbdmMNN5MBjcFXoijehP3HYYCTrw0ip+QWjPlB9XCPi1Ryhv1oHFIhHWGa91sm0zHeS2PqZYxo/mYKit0i352O111flNb6kpaOn2Vicop6S0iOvxvrxHGK5z5MtlrkjoUMZ2dhrmTArKcnoBvAq1Kg0T/J2vp7yPThxFvexevPPs7rk4d49EPfgSXK6vWr9LttMsUajcWXyGQL5Coz2LZLHEVYlgsieN02hVINy7KJo3Dk+ozDhz0sCBkV4DrDtIGmPPk4angvAcw4Jl/2INBpd63e9MM0COug1+Tq618XENX8EbjzfZTf+Qmm7pglk7MhhkDhjYbS8WEiAxM5uG8WmmFCfz5HkHyQpT9dwmq8xP3v+a+ory7yK//8b3Lip36VbrtOc+USuUKVftih27gGmTLEbQQliX3cTBa/12Vm4TDi5ImiaE9rsBtSfjeZSYMmd0apz3H9vjSa5KBSOcOisnHMyF6TqWktRGP5MprEkjt7RsP7v4WJU/OUHWj6StdL6CcWFx2ounBnDY4r1PLwtkMmnj4fQ3DkHay+cpXC4udZv/QMURTxz370uwisKu21y9QWimRK06b32LaJIg9NQoL2Gs7MCRCP6sQM9eVLdBqre7I+IjtvwGGbd9TzcUYFHjpikcc94SjBHif6HnW+gyRV3BOj/twDWBNH0Bia7S6NXgEpHGNpDeoOeBFoXxCNkYKNl4Eghkjh/iwcLQq9aaXpweqddxP0V7j87J+QCUNyuRyNRoNMyaYyMYfX76IakcsVsYixMlmQvCFEshwTCauydvVl6bVW2ctrp4rQLRteBBlUfNK4a06axdgtx5OGzmwc/23YZhglBGkrMjJmTnOnZ7GhCYZFeczcReWbP6nlt32UXk/pPHeR4I1X0MUWsU7QL1iIRrDUh2wGFQcfpSHCqy3FtYT7ZpQzVaHuw1MhtO96hH74t5BnH8P2X2N6epqFc++nvr5Mp75Ce/0KVuIRej5BmGC5RfLlCTSJ0MjH7/UI/f6eSptpxjWYv2uqNRuJhtnPrLi9vt7MOcT7Pf5Q1LWdxfrWn9ZHv/Xbef9pi3LVYlnL9OoKq+fBKiKehbaBZh1igWwGXKP9wgSCBKpZqGTAFYgtWFObyD1E2F0guvKb5CfvAMtlcmaO6blDHD5xjvnjZ8mVp1Fx6TYbBJ3r9FsraBzS6Hj0Gsuf1CQ6kKHXu8nKKDBvamaEtGO59jog8HYIRprr3HXontz6Pdnht8OpxSzk/f9W8+/8GKWKTd5WjpUEcsLVK18lefY/IMXTaOBD0Ial58G2kcKk+W3WIhKhG0MrErIWHC1C2YWGr9QtF8kfJe4cxXvjF+m0mjTWV1havMTy0nU67RYiFsdOnObk3fdx6MQ9zB07y6FT9+F1m/Q765/UMaBYBzWwW3bRijYpSi5pLyANPGm/N7GXa2LEte2V1m1nARQ4/bHH4vl7aCg0AyHvKoeLFlF8iGvnA+SNX0Lyx8DrQPNVyExAYRpcB2wBUZLEwk+gH8FUDiZyZtCbbwtt20ULp9Bginjxt1AnD4M5I36/Ta/TYHVlmaVrF1levESzUafdatJcviBx0EM12fd6yD7euyUPOCqc3ms0OO53R6VG9lJ7HlWx2Gs0LkOIHSVxSdahl8ClUIlEqGbgkp+DqVPotRh59V/BsT8HzReRbBmtHAJrBrJ5yJiDeyGsBcIrTeWsKCerQsaFbl9YP1JCOx8lufYFvPXfxnKK2LkiliU4bhY7ASVGxCEIugSdCwRyWNVCiFfHSiTvthZpkvqjzmOT0lzJiJJWGi201511O8z0XjZPuhMI1N79GIU7AZckZ9NNoNGFfj2GTgzNC3DlP2A1vgKNZ6BwFKqnwcqCWmBbkDUMqpEKQSIUXZgpCBbQDqDrWgTZMiRn0CtfgPAacdAh9jtEXpuwXyfstYj8FrHXISx/CH3L30P6Fz8p3QvsVgmRFII5LLiTMZWQM2yR0pBd75VQ/M0eVDMK85YmwZ1qZ6uir/wroTir6PuAClHeIdIE6h3oLiHqQdRGu31IYrj4aaQwjVofhGwWehnIKFK0iMKE9UQ47wi1rFLLwKkJWAmhV3Xg3H1I7lMkv/ddqH8RLAeNAlQVKb6V+PB3o6XDMH8GOXUKZv5n5YmCcPnXh+ZCRyWcd3uuaZhbdVgQcrsCAN5kzZbWL7wtvmqwBqE8RvYQYmVNqaPTBs+D7ipW/Vms1jOIkzVJi7AFhTugcgayOchkwXLBVrDBGtR94xgmc1DJCt1IacdCYFkkhRlEDwGTSOsZsIow/51w5gfg3Ptw7n+QI/ccwZkr4NuzqFd4TBJ5jOZznzyIYGNcK8fQKFj2byr3m4oZlzjydgjr3sfVC3LiI8j0ucckVugsI/0G+DG0FmH5CVj+A6y4gZsvG67oJAIVKJ6G3JQRPsmADeIAlmDbgm2BYykFByyBVgQ9BXIO1O6BzCkI20jmENz532E/9E1Mn53g+Kkc9xyxcVyoe0KYLKChwOVf/+RY2n0Mdyvtutn7FSAZsSAHIcRyGzTh7co7Wqc+SOEDj+nEI99HHHaImkvQuATrz0D967DyeazW02QKNXKlCcSySeIAeouQO2Q0YRRC4iKZLJp3UNsQYlmW4MeCa0M5Izi20A4ED9C8Yk1OwdQH0OxJqB3DvqfGe87YPDgtlBxY78N6KHg9oLWMdNY+Sfe1256pGLaW9igzOo5qVtIxiUrK/JzsUajkNgnayPsun4X3/4Qee/e7ODoPc3cdJzN/L1G3SbT0ZVj6I6T5dXLlKYqTC7i5PKIxcRxiZwqoU0NzRyEzBW4e7AzkHCRnDfxLk6WJ1dSNc7bQC5V2AGoLbsWCfJakcAiaLbSS5/CUw0TOBC6vr8NKNyFuJZDUoPrQY7z+qU8ehHLYiVU2jaDao/w5HUO69xNVjjt0L21AKnvcqaPu8db8p8DD/07l3LsIczYTOeHBGeHOBZv+7BlW8u8lboPTfJJCdZZ8sYzrOAO+PyhXZ4jrLxJlppGj3wRTM8h8DgpAomRsIesaGl/AIGeygmMJfiJ0A5O9yReFuGyhTgVdT1jPW7i2sNSD5S50O0rcF4htY8df+KlPjpIBOeDnt2MekBSRbVrUq8j4Y7N0TO2aRui3NirJGJFcmnu85TMRKNfQEDprMS/EDl6snJkQYldgooLMHcN6I4vrOuSyWcTNYTkebsbF0oSuDVqsQXUSpl20BAywo34MEgliKe0QbAcutZVKVshaSsYxJbxcotRywvpRSBZduiFcaipqC81QicKBCtVocPE7P71RUa3u8ixGEUEpYyCix53erUOkadzJmjpG2mcUR9+47aF7TsWsryNX12F6ln6kvBQJLzUUbStxI0J6XSTxcNwsOBnyhTz1lSZT07PEccjq0jJiF1GxBkKiJjgZCHgQKY4FBQc6kRImQi9SRIS8o9R7RrFJrNRcYX1aSURoheBGZjIJMaAJODZE/ZH2atwNO24PuDVu0naUedytVjruQOxhG2KU35e2+jEqD5g24b4xZsH6008If/oT8MIX4Eqb+HJAfAmSxRiurUL9KpaTIZ8vks/n0SRBSMgX8gT9Dt7hH0CPfqfJDbZi6GweHE2UODHVkSA2Jt+PjdaTWCkOsO3NfmJIfwSmCgKJUu8lRArWxmrbFkJsDj5gVRXGozWWFOY6TY7VGWrC0paldnk/bWPzXokj95IMH2fSu6bQsgBqueT+5tOamy6SL1boXi7Q+sKvg51B5u+HfhMaS2jnigGMuhniOCLw+pTKFWqTM6wvXyGOPXAyRkMFAYRZUHtLd7wQCXRCCGPIuxCHkLfNtRRspZsIDR9KrhLFG+6Q0AzZhiNT2zXq5/TfV177CVENUif308K00hQdnF39uDGqHntpbB6HUWEvVLDjmBVN8cB2fU9s7B/8ih696wxvO+QwlYPrR5QvZd7Pta88gz73aVOT9a9hr/8e+Vp1MKhQCIM+x07cg9gOXreFukDoQ2SBnYWuQgbIDJxZy0ITJUwUsSHnCIklm3S81Rz0IoskhnaUYG9EYQJxbMJoVTWlPjPWHTn0NvQN0xqQ1g8cZkHSAn+30bOl0W63q2IhYwjtXvJMuz60IQl3TeFy6ED45L3/ryZH72XFd3huRXmtbrSQfWQKOXs/UpqFlceRpd/FtQJKtTky2TzWYBkKxTKB7+F7HqoRxD0IPUgS8HwDmzbTDQc+oTl5GEMngEQhUkVFsCzIuoomSpJAlOhAeYr5qSqUxAAMVcFy0cLsWBH/ODNf0swSvIUhVbYwWI7VaCxjLP6IC5YUKR5NIbxDE+Ga3qXQITetRz+E9oTmuvLykvDli8qzq7DeFdSdQCunkUwVR1uUJmbJ5PKEgYff71CrTfDs536FwO8ThT4SexB54HuIPxDCbgzBltTCwByrCn4IvUDxEyOIqAlQRM3TUQRN2E5w4wCWDmbGCrgFENkXr2OaUa27vW6h5rh5KExq6l7d/fO0uaRxWQrS0MWO05WXlmh7uxMTw3qENhLClYjGunD1WkJ3OSJZX0PFRZ0iTrZAvlRDFWzHJUE4euIMAK2GGe2qGkPYgbBnAKtJYkxjI4RetEVDyCYhjh9B1zdBc6QmuM1ntl+1JjoQxAFheV6QnA1uzpjjLT0co7TXblTHMsKV27VyNCzKHYb+1ZSabhTtwzCtl3bEvLI/xve9BGKbn4Z9qK/B2ira9KEZwKqPXl2Gxiqy+iRW/zxOJoebyeFms2Y4jSY887lf4aEPfR9BGIA4SOsFkcYrkASgIUSR+c8LoR1DqDemTG9o4AT8CPphghmiJBTzguuY5iADVL3p6eQs1LUgk4E42fHpaQolsdPfJUWguU0Djkpf7Fc1jxLkVBUXGR1RpYWIjUrZjFPmE4ArT0DzOlx/HVp1WFmB5SVoLMH1J+Ha72B3nyeTL+NmcliWjd/rUCxX+Obv+TvEcYzv+URxDCuPQ/1ZiANIjABK5Juo2EugrZiII7mhBAfX0glkIICKjZLPKY4NrmUwhJvDcFAzIswSJJsDS5DKGdM5l8KlYUQZdZjV2UkhWQfJ18IIcyeys5rebYzTKH9tL1M1xyXQERFyWZepSp6Ma9200xP4/LcL/SZ0FuH8Z5HFJ5ClZ2DleeSNTyGNr1IoT1EsVREB3+uRADPzh81gw5XrtNaXUMB1syY/pwpeEwk7A+duELX2QliJBu9tX3VNoOVDFBulZgHTZWGuIkyXhKxtRsQOpBTNWmZcbHEKfeQXlMzEWGU0SSGoO3EK6TATPG55bNzPbi7P7ff4aQYijwJYaIrdXSpX9Zd/8i/rO++s6mZ9edBnC4r9J98quFVYexl95l8gX/yL8MRfwGo8RbE8xeT8MYrVacIwIJvJkM1kee3Jz9BsNli6/DqoUChOILatSdSDMEASRcMe2m9AGA1Kcgn0AyOEst0ykChBJKx2E9b6imWBYwvTOZjOK7NFyOdAbFP+F0fBzRgR0ISNMV+QbkL8buZ3lCWVnSohafn7ZEzTu580jo7w1dIWw3UMYd+oaOSq85qrzOrc0Tt1emZG//lfejvHDlX42X/zs/yDj51V17E2/SrDotqHP/k2obQAx7+TZOJhJDtHtlRh6vBJg3RByOaKNNaWybo2H/6ev0ucQKfXJ04iwtAnwUEufFp44xfRsAexby6834R+C4kH2jDQTSEU1Gi1BDSOUbFQy6IZmA1SyMBkQZgvwh1loZIDsQW1LCSOIJMfcBYmY6fibs6cpFnPmzWlcxDJ5jQLu99EcprdNA57wU6/rc6e0IVjZ7jnwUfJ5Iq8+PWv8eqTv8UXvnaBtWaDb/pQlz9ZmuNnfriqP/hTT4oMDpCoIuojL/0voke+TzVco1QpMDV/DEFxLFP8b7dbFEplVs5/jd+/8nVmTz9K0O+SyeZJohCSyPh3Ud9ou9gDr47kqoOgxENyVTSbAy9BFgN00oUc6KrChMDlCC05yLygqvRjYSEHJ6rC9Y3SnmUqfTphg2cb2JdYYwVuys5zlYfVgHdaF+sgE8x7mak2LuZPRpTx0kReO/mdtp2hmovJ5nN87YnP0+81+dC3fDvlcplPf/kKT79ynWeeeoGf/4fv51t+8DF+/m8/orbjqNzACpD4y+jVT0veblKenMVyHBw3h+/16LXq2JZFqVIlk8kQhiFXL76CCISBh1gWbq6AZbvI8h+KXP8cJAYwoL11NPJRVbRXh+Yq9HpoJLAew7UI/ASuheCHECXEkWJZQhBDPzCb4MwknKnCdAbKebBqYhqOC1V48J8ruUOp13Uvlmwn5eGMu+C7SfUoEMGoeuu4NHBpeGLStGCaCpdFuVzQt334B0CVi6+/xNULr/Lkf/oFHv32v8bFl57m17/2R0zUFsk4X+YtfsA7Hn0XP505xI/8xG9rFIaSDIbK4C9Tmp8jX5qAAdhULBtbbGxbmJqe5YG3/zAvP/80Lz79FTKFMiQJYRhgZwpYfl/Vb4r2roLfMU3rtqJ+fxCM2CCGaVU9QVRQxzVIg9CcSwtmGnvHUyyFwgD651owkVPmixABvQCSgo2WJmDynNGEpKPVSzNDbzdQylY3ykoVPKRMeYxCk4xD2TBKS+6lAX7X0pBYfN/f/N9ZvHKJ1ZUl7r73bVRrUxTm7wGxeOu7v5lz7/kufv6PLvPp336ap7/wh/y3/8dXWch1+a/evoBjDzxChdLEgtam500KxM0gIti2g5vJUixPcOjoSYIgZG1lhTiJcN0cYeCRxIHpDSEx5vD8vxMu/6a5RgEJmtBdG5TpIpOq6XdQr29uIgwhSVDbRkrGLjY9pReCnxjkTJQolRwslGAqDxkXrJoF2TziZBDL3cxU6IhAbqxk/RAMgMNefagxQKfj0qTJiPrhuIytu+HXLAE3W+Cj3/Oj+rk/+l1IEroonXaLB976DuaPHOfVV14mm8ny1rc9Qq1S4Y9/++eYm7jGD733Tr7zxz5LsVjczIooMDF3hFyhZKhx/T624xCFAVEUcvSOE2QLBV54+qssXX2dYmWGfreBk80TRyFxrDjZEkkcgSboG/+XSLaseujDKAkkfQN/QVHLheK0uTvbQpwclIswbw9Ka2aL1j0TtusS3DdjSDAXiuZ6u6HwRqIkCzbqzcIDP6M89UNC5+WxNV7aiPlmgR0LEb1TSmVcWBMjhGw/eUZ20Gy7C6eiYmNlyprEyYBN1Hw/iiKuXL5MEPS4cv5FVq5dpDoxw/TsAuVymV98fIljczXiOEZVsS0x0Cdg6cJzYjsZLdZmyOWLdNsNAq/H5NQ0rz7xO7z6xO9QWrgXy87gZnIkSUwcR4OqhhEuy3Y1iiORxEfe+EUh6CmHvhnN5AaRcQISIa1raGkekgh1XGTOBsf0juiW8mijp1jApaZQcpW8Y+g+7htQvzUnbHpBETpnIVO5ZXXSspKNGkq0kzA6ww48zPfbMcms6TVgmuhqnGjq5uSxksH6ln+t7myBjCuEoemr1QCiNR/76jNUln9Z7n30oyxevWzGqA7yevlcnvr6MvW1ZQKvTxSEeL0e3dY6x+//EDzz+/zEb76xeb4ouXFPQb/D8uVX5GRlUisTU+TzOaIw5NCRo7y09BJ3PvJtPPXlP8G2bfxe03TFRQGKhW1nQCGJQmxXNQlFtL+MXv1dEXtCZfp+sG1ULIQERUwqJVbUGvDK3DQwRVEihaYHl3tgr8PdU5CzYSZniI+SWImnXcJglqTzY8qL/zcs/kchbqUyo+P64LcEIcMg7bsJxi0n1/QXNkwLpuHvG6otJQ8P/D21Zosc/sAnuGM+g2sLa13oxdDtKY31kOD5Mm7zN6hNz7H49JPkclkQwXZc8oUi9dVrtOsrmxcUxxGtVh3P63PvN3w3X/n8ZygWPSqTR+m89MVtz6jfWmN96QpB4OG6GSamZ6lNzhKGIedfewWv3yFfKBOGPqKK7WRJ4ohEZHOUg4gZSJPEgniraP3rSG4KcjOQq6BWBjJlNI6R3joUq+gayKSNWtzo9xhMQvIT4XpHsYHpgjHDGQtOTyjdyMLKwHrkEN77QZQ82j0P618aGWTs171y0iQN90pgvRfC82FR7vDdJMjhb0LmT2v+/X+bw8cc7j7icLwMyx2l3TY4PbcoOK1l6H2dyuSctpt1LGfQ6a2QzeUIAx+v1zPH3MSxJ6AWicKrLz1Hv9MkX51m/dprqCbbrjVJQuqri7SaaziOTdRv8MpXfpv7v+HjvPTsV9EkJk4U282TRAFxHKBxOEDIWwMBtBHLMdrcKYJbQnEGEYkLTg4pVE3gEfmml7iTQXOKFLbUfQcPSFD8WFjtK5da4AgcKikLRVj3lKgp9EuguISnH0Da36U8uyh0L45NwTtOXOCksde7NfnsqWEpRSQ7Ls+zimDNPgjv+6dq3/UWTh51+abDJgJ8taE8u6SsroMfJYgF+uwTzD73axx56N0sXnoDeyB8ikWhVGZ9ZYlmYw3VBMFmI8S1LIuMk6HdWsd2s0SBh9e4tm3e2tbrjrw23V6D+rXXKJQneeFr/5lCeYJYodVYxbZdHDeDiEUigm25qB0TBcE2wkKp3K1U70HdIlg2uCWozMHMYdT3kdYytK6h1mFYzaPzBnS6rfauoJrQ8oULTSGJlbIrVLLK6aqBdanCEkpyuErs/FVoL6q+8vNCsJqq1jsOwOSWrrihFPuyxbFld7b0UQKTVkumZeo3cUYW+eAvKPd/MwsnJ7hnBt4yodgCz60qLzZh1RfCFR/aaszTmodNH419/H6XfKmEIDhuhkymQBLHg5q9PdBoEZblYLsudjZHf+UKtpsxmm8gfDffZ695TQpTRzVnCb3mCr32Or32OtlCjfL0Mabnj5pBhFGAk8mTxDGaqGGwtyxILDQZ4OQLx9DJt5qyma2QryLlmumey2SgNAVrl8FrIfk8upIgh+0dhEJQFRqeAUVnVuDhQyY/eHZK8SOhH0NUsegHLsmDfwc4pLz6TwV/cXf52ENkvKMJ3q1IP4qcOk3zzliJ4y0Rza3CKJugTHn0F5Ujx6k9cA+njpa5cxLm8+BFwlNLymIf1vpK1AONEujUYeUF5NLnCXyfdquF2I5x/JOIQnGKy+dfprm+fCNPMyjUW5Zgu1niwAONcdwczeuvya4dgKpYYqOZKnamRxx0AfB7DeJrfSLvENXpw3Qay/S7dWwng5stYNkOcTRoENIInXyfMvEw5GtQmzcCl4QmEtYYXBsma6ivSPcqZAuQLaG+DXm5ATbdtMZKGEPdN8DVbgg5x0TJJ2sGW5igRGUlnK+Q3P0xWPmMgZhpPJRFay+m2hkFqdlP41BaH+EWgVbd/ff3/1OVQ6exKxYcfy/V6SIPn3E4UjT9O0GsPLMqvNKCbgSRWCSdGFlfRpdfQxb/gFr0LAt3nKPTbpFxXUAIo4hSucqFF79CY+UKTr5muJYH12LZDhrH9D0PVcWyHOLQH5r97zevS2n6uGYLFfobfh4MRqsuEgY9KjNHcTI5Oo1lc1zbxbIsknhwpMopmD4HlRnIFwabwjasWl4XymU0A3KoiC7PmE2WKUI9MqFuIsbt2BYZQ5AIqz48tQyPHBYslGIGClmoJEKvAK1JC/En0Yf+kfLVSFj+o5GVrHEnWKViyWcMf26/YIbd5u5y14+qNTtDcvq74dA8lQmbo9OwUFCOFJSswLoHF1rw9bUEXy3CWNFOgjQD6LWQ5c9jr/0B+ZpgZQrEXhMlIevYlKtTrC1dol1fwvf6FKoL2JZFlERmPKrloKp4vSaO7dJvLY9MvsZBn35zSTL5khZr83idBpFvhgTGkU+vuYIAxYl5CuVJfK9PHHjGtCcJSFE3/b1CFRzLBEM4EMeI1wEStDKF1rIgU3C+B34PNA9rCpOOmR/HwI3aiOoTpR/CtZ7JD86XjDI9WjEA7KoLUUnoTjjo/H1w6i8aTo+1L42NZBr2mZOmgjBM442r4caebC4OHP8uePBvkjk7j51PmJ2yOVKCY2WYy5k83GJHWexZvNYwZD2g0AeuebByBW1eQZovkkuWcbIn6TTXDS+L2oS+T+3IBE9/8T/R67TI5MtYboYkjtBEsQaGNuh3SJII1y3SbLwsg62x6wZUIOjWsW1b8rUFFadA0Fkl6DfN6ARN6DSWcNws+eosSRzR97sgxv9L3CNC7oiSKRjhEwGxER0gohOBfhfaZRMVVxyYnkUba+bkrYJByMgNU7y5bokSBELLglfWlOm8OUUlAwvlhEgFLxLCikUwlSO581sh7ilBXbT90oFVwJxxy2GjzO0wPmFlPHoO7AJafQDe+XPK6RzOtHDnhMU9NWUhbwQvSqARCK804XxT6YaYRptGBCsB2mhB/Qos/jHSeYl8dYpcaYKg1wGNsZ0MIGSyWeLQJ5svka9MEYU+YRhioUihhFgWvW4bEKKgt2ma09CG9FqrJIoUJw6pZc2CCKHXRuMQ1YTGyiXiJKZYmwex6DaukwQ9YeFepXgc6a+jhSIbyGhD3REbP9B2oN4Gy0Zrjin0em3o1iGXRzw1cK1bolfTqtnuK3VbaIeCbZvNdqwsxAmseVAoWsi8hS+QRN8GQVt59aeF7vk9YTpvliNrv2o0baPQWBAep4hUzyCHH4V7/7HKVB5r0iJnK/dOwOGicfJty5A0Pr+mLHZN45hhHE2gYaP1NWT1JWhfQ9afxAkXwc7g9XvYbnbTNNWmpnnt+aeJJUN+7n78zAJtmaDrztBhkl6Yp9tYJUlMKqa59KqMM5YAwGuvsn71JQm9NuWpQxSnjmHnKoP5wUJ77SrdxhKObZMdkI3j5kA9NOpDnBjNBwYRw4A0MNlojPKNddYEjsyaswcBuhSh/fhGO+fgf7JZqhP6ifDsqglOLDE4wqNl5dyUUnGVUgEyUzYyXYQ7vwuOf7ci7ti5v50al5y9AEZ3guuk0XZp/D3sDBz6EHzgUyrzZfSNLlo1mYljJaHsmqZrBbwYXq3DpbbQDhUdtFjp5dgU4/0e2roE1/4A7Z6nUJ7AzWQJ/C6WFMnmC3jdFrZlcen154gS6Mx9G/a93wELs9hZJb7WpfvsL+O99I8plMpokmwLktJQj2wuQBzQq1+RKOhSnTullpOh314l8TtEfpf22hXEdihMzBOFvsZJaNhSgx7SvI7WFgyMPo4hiAbQLAuIIGxAowBTllnVueNw/TxUZmE9BzM2ZIwfuLlKg1xjs6dYAk0fMrZJYdkCZyYMD80rdSUoW8TzRaI4g86+G974LcV7XiB949pO33PGydmkiZbTBCS7p2EE645vg2//98qcQ/JyALNlZCJBE4vTVcEZHLjuC08tw4tNIdCN7kKFdQu6ngFuxjF4a8jaF1B/iah4hDiOsWyLwO8Rhj4kEU/+4a8SF9+BfPRf4Z49y+yc8NYFuKMiPHHN4ckjP0g8fZL2Z79TxM3o1rp3WuHb+gq6dVbf+KrY+SmdOnSSBIvW0utEQR+xHPz2Gl57TZjJKXYWifvQvT7QajWwbfBa4NeR2jFUMiAJ0myhk1VwbGRB0JUstNfBmYHQNgSCIltC4sFcNxHUgq8uK+9agOmC6bCLE7hryvzk5YbSLwnM2Yh+EJUfh899YltqJg2u4GZYnpM2cBhWvdhRgG9KXo90UK0icvYvafIN/xCZcdD1GFywjlogCWerkBElSmDVh6dX4EIb/HhAP6GKICRX23DhGajOQHcZ1p9C4h5OvoxqjN/vmsRv2Mfz+gT9GOs7XiSZd8kcneYDpyxOVJScDUtdxRZhfs5i8fQ74PpPKs/+iOx2U+OkqhSI+uuyeqGFlStraeIQxcoUrZULdOrXRFDk8i9L4paUIx9BiQyNb9BC3DwELcOGH4fgZAdlXw+Wi7BgLDFnF+ClSyZfuBYa4GpONtOssrmYSrMLWhCeXYO3YMjQQbFEODNh2pM1gnrFoh9bcPID0PsF5YnvH9AvpIdmpeIHTDPcT4Z9R8eZPinIkffD2/4ycnjasDE2fGQuh7gwV7S4a0LJOXClA1c7cLVn5qmhYjzZZJDrr7imZ+LqFw3hd+dFNOpgZSqI7ZhIs7VCkDlNfO5H0PkCztkj5KvKO48IRwqmffFqB15rwoon1PsJuHl06vSuGn7UVMjdaCCTOCTpt6SbhHjNa4R+D40NC0ISduDKb4rmZ5SZtwMJEjTQ3jLiNSE3aSQjW4IkQMIe6hUQLRslZwtU5s1IMMuGhiCTDpqxTEp6C52KqglK/NiY4koWMpZ5zwKOVSEWxW4Li74STeaQ0x9E5VPKl/8bGSxAatDJLVHwzXCqm6H2MsLfE8aforlxYjn6CfS+v6ocudMALusJUs5hl03C9XhRWMjDsgeX20YIe+GAX8dS1BGSjqB+AoUMTB2Glz4FpTuRsG4ABSIkcUysOcLqo8RnvxvrLR+kMJ+lXBAemBUW8koQw6WOySc2fKj3laADGgjE/Vui32H+bhoqENNSGRH224YC5ubvds/DhV8SsTKqk/caPGDQM81Kdg71GlAsDSD5AfgeWs8iMzkjhFMuXE+g3wK7hgYgrqCiNyHWFT8ALwNrPszEgiNqGGYEqlnhVM1UTtoFoTXjEidTYH8H4q2oPvuPhCQY6fPtmobZqWc3TTAxTj341vcF5t8PZ75H5fjbIeNAK0RDkHmHbB5KDsznles95ULTcB23gy2VMjGFde0kaDNAQtPgo7WzcO1LWGETK5NHVQkii2Tmnci934fzloepzVrcvyAUHai58PI6eIHSjIXlriGDDNsJuuLByhp0FtnAGo8SrFH+8CjU97bvNp4zQthdVCbfaohg/HXDplWchV4DcmVUQzNvrhtDKTYF35KNTFbReguiADpigpGstXnCjcAkiIR2CFlfuNpWjpWUggvW4I4KjnKkDL4aesv2pIVSRO/6S7DypLL4G4JG6TCbu/mAw4ZLp008pq6GlO5G7/ph5Y53QME1Dy6ykBkLuwi2KLNZAzBdbMP1ntFKyRZiOdUBXYWVmKrA6gqiETL7VnjlZ9CwC06JhCzJ1HvRc38B59zDLBx1OFVRzlWVWIWX1pQX6kLQBd0YJu0putyD1VWT8O1e2zboL22dezcgZ1oroQDrX4PuokhnUclUUb8J7hTM3AuBB4UJBAv6dcjOoe0QJjJG+9fy0I8Qv4/6LvTVcGK4ss0SAfQCoWXDtQ4UbaHgmvMnidGE03mLVgANbwBasEDbJTj7N5Dea2j96aGys2spbthwur1A7hkBclUE5j6qTN0NkzWTPPYSrJqNNWmREZhwhYqjXGkqa31oBVs8jQ2GsQEtBQUHQkUI0dWLSLYI2kVFTXlr7n3Iue9F7n2EwhScnYQ7y8Y/9xUudyFQpeeJ4bcIA1jrmvFafhvxrsPy4wOSx5RIHfY+HHHH7/rX4er/Yx6hlYXJ9yiRB2ELiSfR4jQ0rhmcYBgjRQfyFmoJUsyZBqY4QPuOYUKobIU4GYcwiqDdN3X19UCYisxgHBl8p2Ar8wUjgLEKUdkinHXR7l1o+/uVF39K6JwfCjjZeu/WTiZgGABhr0DEWzRC8Tgc+yaYmjXCF8SQFWTSwhUlg5mLpsCqZwaLJzeYas3zElMIsF2wAoEeUJmG/iqsv4IkEWqV0MIdcO/3I/e+h8KszZEp2ySzBa53lYstc3zPH9ijRogudtBm0+Dq8OD656H9nFA4vWPwNW5zf1rmr121aeIj7a+LdBchUbS9PkivxGh3EHR0BzwySYyWHCgUkMBD+h5E0aCQeAM0qAPMoB8m9CJhzTfPxY/Nbt/Ivk9m4a5JqDlKwQZ7GpiuwsmPw8kfUPJHbrmX3WRnLJLycZrJh31m2Tk49+PK4YdgomjqaWohFQcRw+hUdE29sjkomCc3HdQaZPMThShS4pYPbQ/ttCHx0cu/ZRK1838B3vMLyLl34U4IR6pwbgKSUHluXfjcdeFCS3EFJB4ksnM2FLNQrCGddfTS59Dz/xFd+HOq535CyU7t7q9JOkBmGishI9ZC/SWM8y/gt027ppOF7prpGWn1B892cGGTJdR2DAl6pDeS0jvsJD9W1j14pW7Ge2192RbUssLxqjDlQsYVZNqGqUm46y8Z4ILIyGamHfGA4+zkcREzm/dY/kblyMMwWd7ABiFFBymAJErWEUqu0AmVa/0b5aFtbFADLZgAWgdZakBzEb3yn5FXfx76L6Pf+EfYJx/AuiNLqQp3VpW7J8yog6eX4fmG4nuw2kgMKrMVov0Qel1oXgOvhbYvI+vPoW4JOfQN6KlvRI88pfzmnULi3SpAmh4RPiqwS0U7suED2zZ4TchWIOijrVUoTcJiD5nJo84gUe9koN8GK4LqFJq5wXFjiiPGFPcDk6R2RXi1ZfzxDcCCAK6lHC1DJxRWPLBLQjyTQWUSa+oUiWRBvaE+8NA8YFofRkbkDOUmHJpYDvroj8HErEmZ9COoOFCzcICsBc4ANLnsbQjbjQPITeogqivJ9TpcfQYar0HuBPrB30FmJtCajU5aHF+Ae2sw7ZrreaUBL6yD11F0WU2FYLVvOFka16Hfgf4a4q/ByheQ9vPo0e+FO+7GeahGdKkA7/sT5Y8e3Yz6SBG8iYwW0LEDuWAVPvtNwgf+QJHYCKAm0FlBKjNoHECU25yJJdMlWI/RXs+YluPFbamYreyr3cDQBjo2XGyZa5sviclHAqWMcN8stDxYCqHlCqGTJQn+DFg1lc99h+iIJLWTCqGcUgvuNq3oxh3a6Lt/TSksQCFnirkqiGth24I78Er82IAM9CaVMKA+NnlnhSBRtBFBcw2O3I3c87BxUMQmO+VSs+HcpHJywowwSBReaMKfLkG/jyF9VGB1Hek2UK8FvToEHSOM1z8L639KcuTjyMkPIodPmhP3LQOPR0eWJLd9puOjxlOlMzSCyAfXhd4qkq9Ar4526yZJvdaF6RK4FmqB5HJIlKCBB1rcsqm3EoSbATidvnFPUMg4Qj6jVAZaM1GwUY6UhaBtKII7JUXnC6j1fnTqOeXX7heScNf7dNKahbQI6KGfi0DtGFRKJomXmDZCikaoFEOJHA9It8UyKRhBNwOQjQcUAcmqGobPc8chZ5vuNhJmS8LpSTheVvICWUwJ740OfH0Jur6ggUIzhF4PWstod9XQXvSuI4v/EWl8DZwqOvkIUj0N1cNo6BBfjWD5MrQv7+rZ7ZRFkBHJ2b0iyo0blyBP/hXRd35KSSK0NGOedf0qHDpnNGKjP+DjsKGYMfzTrS6yHMCsu/1ejKnaxBC2PPPpugfTPhRdY4o3BuKcqCndSAyc3wFv0iXMOSTOSXjvbyj/+c8LYWP3Ssiw6djDJo2P9eAKx+Atf1+pzEOpbKKInAV5GYyt0AFQ0tyUDGrJlqgh4E5MZWnriknJolSzsLOQdQ0LqAs8MAtlVym5xn9c6imvt+BCE+o9IeknsB5Cq4F062jrMnRXkCu/ivjLaOd1kqiPVI+itfsgO2UwefUBrKl1GV74MZFBIV5SbNQ0TVbDwK2jgMLauQjXn4Kj7zSlNzAkRkEPdTNm8E2QAydBbTHuT9uHbheo3YjoNhk4Bx04iRKL4EfCel95DXBFmC+zmZLP2nCsrDQ8CGNFbMGyhP6UhZx6D/B/qn7pr4n6K8ODEB1Zsx1/h5rfWZCdgTs+bEyvmFBKCmLSKLIx9OVGSS/rGK3oRVsg7nqDRFJUKefNbsw4MFM08nykJExlb/jm1/vKG03jwzT7EPUiqAdm97eWjckK2nD119GlP0Q0NLg7d8o8nqgHcYi2lwxRZNiA1/8tUv8qys5luVF+3Kh5eKRch21roopc+jR67J1m1INYZg5I0AG7BFYG6XqQyRuCchGknEfrzc0JnIhs+qgb+H0VQRS80EC2OrFw3YN8Rqlmb6xdNQuHy6YieG0ws86tWkRaRJMPw/qPKC//S8FfvjUIGdZmmdY8DxXgzBTMvVvJF03bYJIgWRfJGe03aMvFwghTXoSMs8n+SKBCaHzfTSEt2FC0TfBacoWaC7WcUHGVZmDo8rwEnluFlb6JdWJfkVaIdkLwuqjfgqCNVf8qXP9PkMSIm0djH8vKkcQJsvolCJahMDFw6Htw/tOypUdvqP+2W4Axai7eOIK4EUBo8xmRq59VPfR+Ez1oDH4TyeZRO0F9D7yB/bQttJqFTtbkCwvOlsalW4l/4kQJY9O2eaVj3r9zwigAUdPoPpuHKBbWetBLIJez8KsQ9HLw4A8h8Zrq658WvJUdasFjYvdGYQQ3/+1W4Ni3Kff+d+CYHWVGzBvtt/Fb2xIqLkxklHLGCFAvVLIFWO7q5oyLje/XMkI4mM5i2+b7/Vg434brXfP3hg+NwMxMI1C0GUK9j/Tr0L6OdheR+jPoC/8MLAc7W0YsiHHR3BHUzkP/vFidZ5D+deItxfbdusBknGQ8483jG6kxNUGf+qRw+EM3Bn/4ffC7BthqO6aQnnNMB1KiSCGHXu8hx8uILbtcrDHNXiQ4vgkUr/Yg78CxCuQtA2KtZoR+1qxNPzGcNNmsogs2kVVB3/YPkMhXvfRrQn9pdB5wGDZw2AzYbceonoP7/i4Uq1DImyh21kLsQS4PcCyhloWTJVP7DVFakalLqjWAXbGF7EqUUIW6D5WssOoLq6GiHeh4ZoyVH+kNdoEkgRUP6QQGvt5Zgf460ngBXvhJcw3ZMm62SNyvk+TvhtlvQqqn0dysJkt/DBd/UcS7nhrvlgqytksi++ZUjYwZOdOrQ3HGhHSWjXbWTHrGEhMtkx+MXgedziBL0aAkoTeVLHSTCXvjmvzQFFkSEV5tK3ECxypmZrGDMpkT7qgqEcK1AStXsQjtKYvYr6Jv/3EkU1V96WeFsDHaBxyVahlOFOQg2Vm0NA2lovE7DtmILZu+bsFVDhfhaElZKJk84HJPWWvLgBjeqP7NBR04i8t9U5Nd8wZUa9zoJzapieQGSGwxhFYf9VtIt26adppfR5/7x4PGnixOJodqTBTHyPQjcPyjyIn7wbHQ6buheEr1a391m+kdlWQd18zKTamaUcOhd9akCXzuzwrf/DnDRCQm/SWRj9oD7sD1EA7ZaGKyCHq4jCG83nK1G3PpBnd8AzGjOKGZ3t4P4GpiLHoSGyXiiGIjTOaVugcBZtRstSI0bYfYmUDv/+8hs6B87UfF4YBeO/o/8+9HH/nflawLRQd7XkhUDbGYwkQWTlZMBDWTN+mXugev1YVGYHqLVntyC8g1GQzhEzYHim/+TzdGWYnAaoKutCDomsDFb0JvBW28ARc+O9CqWexcGcvJELaX0GN/Bfvhv86hB45z7KjFlSsJF7pThv5ip/uV3cG3aQf4pdncaVNgJoCN0SgyGWTLMPprexmRechkzSSmZWAuh6xGsOBumtmdLla2+IUiQj8wa1DKQzMWWqFSsKAdQqIG6Fpw4J5peGr1hiBXStA9ahG6JVS+G6Ye1pFjGtIOKrmlVnnoI+jb/4lSm4VqFplS4+QOQvxaFu6ZEk7XDFmiKqx48NzaIEiNDAghGaBddGMaQcLm5MeNz9iYCpmAhDG6GqOv92FxDek1zMwNr4/2POi1of0aNL9i8mduFtvNEUc+sTWHzr+LeG6KwoRFuw/X1xPT4thbTj3ReddB3zJ8lsleN/stwAiN4IvfMzAhlrEMOmBdTYCwj0YB9BM0StBF71ZAs9yojeiWUpZ53uCHStszmYnzLfPzZICy3kS6CDwwbQJNBkNyClklM5tBjtfg6N2bln+kSR3ly9zyu0xZKc9BJQc1w5Ktg2zyREa4awLmC2bSd5yYJOeVjvlz3WOwy2TbSQ2r6QD0sVHs3jAVyQC/txbB9VUkitCMgxbLxu/prphaaeN55NpnkCTAyVZw3BxuJkvUq4sufAgmz2BbOZbrcPmij7+4Cu1FWHt214cjsrt/vM0034Q4lxHAjnEmQenN/+pdNvdtTIY5ud8yCCEwY8D6psGdWG6gXWSLqRnUhuWWmH9QBk3MtM4ogcUuhBs0JhusXgKurZwuQ84eYG8UMhklU7WRhaKZFTdqYOC42D+mH4XDHzZcJgUbqyibBylnDBbvVA1qGRDLBBOvNeFq25jgXmACia3wd93IU6FmM9cj6A0034ZDuQGZcbOoY0EmB9m8mULptaDxIqx8ATqvIXYGK5MjV5okkysYyFLtAYhDotUG65d81i/10fUGXP8iXP892QHPfUuJbdjctJ3ygDePxd3rYJ9bf5fAG//e7G4RkxMMPYgDJElM60OvbxJ3AtqJt/YWbcVnbZuvLJs3LCQJ9D3jTjV8YaU30II3Xc9kHuYKhhBzA02TzQvulGVmxY1Lrbrb+5u4ivkPKEc/CoUcktcNHm1KjnKmBierJtgIYmW5m/B6C651DY2sH95UA2aL9vMUujHSGQzuC0ESAT9BfLPLJWtDqYTIYI6910WCrpnB1vg6uvYEiI2dLeJm8mZITKIkcQz9a9C5Dq0WXL8GS68j178M619G+hdSRbS6gyCmNbWSxrymxWeqwmufEiLPhK0okkQmJbPRjhl6RrBsG9rJINOv24ZGD5o3TZVeBj72ls+TRAbcgspyH3rRoI/Eks0AJgam82IqgWI0pG1DLqfDWfLHrf+qXYTScageQyYmYMJFC4qFUs0Jp8uyCYdKFOq+xatNuNYxyIsg3r5yW4dn4ytaVwxEQyDnIqUBTKtl2rlkIxLecBb7XWgvg9dA+8vQuwhxF8vNkSlUKJRqWJZNv9ccRIfPm1yPdx6NE4gjWPpjuPY7ouhY0Codw3cbVqaTPcDltr2aL0HmLSYHiIDfRHNlcLPGx4tiI4BJYqI+x95CjjmwQGFs0ja2dcsNqUDbA8lB1jUWLGtD1tZtgZo1AC1Yoqz0lHAwjUJIARpM1XjkVmHiG5QHfxROvhVm8sikZTSfpdw1IdxZM8IXqqlOvLQmXOsqQbTN7bhBGqImDUMCcrFvGKNsGylkYM5CQ6CeGMkdoBckjqDTQh0HOutIexG8Ovriz8C1z2I5OZxcmUJ5kkJ1iigIWL/2GnFkizozQA80wkp8iFqoRtuYENJorbTDfdiDRkw7hmxz3ewJ9J0/pUycNsZRFC0fMgIoxsRKcRK1LfNsZ2xwB2W4ASqGax6St4zPZG33RHQwIhbLolZQXNt87WiZG8HHwEMyNX7hSguu9ZSIIdQcafN/Aobp/Y6/qLz1f4CFSWTKMppPlaojnC3D2QkDKghieGpVWO5BvadEGxUO2UDobnmCvsLVELyeidrcrKklTw/qd6uRwQDdsAdou4FogvRb0F0Fv4M2F8FbM/kwy8HNV8gVq2SyOcBCwz468wml+laYOAW4JFd+B7n+K6LhcioEs46puYYBQPZTe79l3ZLm4Gi2aW5PFIn6aCa7GaBorw2ViRu+4wDzJslACaiiS10kjmE6v+3uZAtWrtGDag5awIWmcOfkIFOxzVdOOFy2yNnwcuumWvA2wdqlT/jmJdDqwyrnfhjrzDeTHC5BBcgYbsTpHBwuwURBeKOlrHnCpbbS6yUklrVZyr+R6BxcQz+BJR+6PSNIkW8gRiXjyep6jIQ62H4D2rJuH/G6Jkr2mkh7BfwWKjZy9Veh/RLYGexsgXypQqFSI/D6dOpLJEkMRz+Mde/7yByqEnViotfn4GVL5eWfFsMZujdMpKQUFhnhAqVlpd8RMb36MhSPmBygCPTrSBxAcdowbQ0AGJqArgjWtINmB1dngbguavnoeg9xbIO53ClgESFUwVVoB8ozy8p9s9Y2QVIF21JqOTimw9AwI2b7itjoff+ryvzbSA7fg3V4EikbCc/bymTO1Aa7Eaysw1pPSYC8Kzh56EYG9azJ9vBb+wks+9BoQmMRtSyYOLJZxiPSQd5vkDpIYrTfhzBAkxjxG6jXhbBjBr+8+jPI+lMm+srkcTN5bMsimyvQ77bpNVfQ4kPI1EmoThBKliTsgV1E3VrqBR+nzzdt0nksaP6unytc+JQwfVZxT9yUlIw3k/baaxuYnA4yDFUbsoPPNvzyBOgmkFEoyK1E4pi+ahLTUhMjdAMDWNgAuFoDbZmxhUOlMcAINx64oLV3KMc+Amc/AQtzSMVBi8Y/y9kWeUeJBZoxhIFScIT7ZoQ4hlVP6QrElhB7SiLbyxySgEYb3dKKeGuofcI0GCmmZdKywOsjlqBRiPR7EHSNH9hdR0IPjRV549+jK19ENcZ2c1i2S75QYmruKGEU0musGJbHyXcpSYIuLaLNAuoDay/BylfYOQO2O84vjaZK07g+CuyRpl6/+fKXDdgWeyBFanKEvgeFkomIIx/iAliWAev2xGg7GQA0N5qZej3jIxYKW7TGjZpdsgGhU6WYExa7yt1TMigmDDIiYmiDbWsUQ+rN04/EQs/+DeXQB9AjD0BtCiZcpCi4tmJbCbmMYIuRhZoLhyaELDCZE1b7sNg1FxtGN6GcRVAvQTqhOXG2APky2ryAtJbQsALZrDG5jgN+OODNi9E4QHpNCLto5Jk+3ku/irX0hyRRD3HzWLaDm81TnpzDzeXpLNcJvJ7heY7qaHsRsI1P03wdWfxDaHxNFB2rySgNtC1tzi+NHzhsutQ2u3f5N4TyIaUwNYDwB4i2IF9iY+as9Ltormiebz8xGKuiZSLjwXE0UegFWE0HLbs30MO6JT+Igb/hG6DJ5bap94sYloWt5IrOUL9mO30VcvLPq973IzA9i0zkIG9mpmQyZv5YxjJIn0pGqGaVqYwyVzSwqdfXYckTvMTMr/XCG32+m6mXMEG7A7NgOSZ/FfZh7VXIT0NxwpwwGaQOwr4h5EkCg9Xz2sjSH0HYhiu/jeW6ZCuzhEGPOPTIVCZwXRev28L3fOxMDoiQ5hPopQZSOAK2i9RfQNe/KgSrI6tDOiLIGKXV9orDvCVDIcPm9yksfgZOfMw8x41PE38wiGcgWFEAoWPqxyKmqc3BJLN1C1o6iND1LkgRqhlUZSB2bGncsehHSiFSljrmMLMFwZxON8GvI+nZxC5A6QxkKujb/leYnkKqDtaEII6JrXI25B2DhshbyvHKxkRGoRsqS33hUkdpR0qiQsvXbUVuHSAmiAaYqzgydBOhb1hCu9cGXH9NwwAvlklvim2oN5LARLlhG33pX4mI4BQnNZev4GRyWL06cdjHtoQkSfB7Dfx+azDuPobO80Ln+T0326dNlaRh0EqjZXf0C9NcfOtVKB8zz5TBjJM4RG2XTUhw0DfClyuYDHI3NoiPAZMrG/zUUYI0PBNtZuxbn81gN/QjKGWUq23BtZSpvMF+btyIDN/NglTPoQ/+lDJ3n2k8ngKpCOIKjmUGblczRghPV+BQyXgaG1r59Sa8sAb92MhQvbclyak3GA60ZTjssAbE22tXkDhAgzay/hKqDmTKiFsYRG5qtKRtQeLDC/9SrKXPoZpgZSuarc6TL5RI4pBiuUZlYprVyy+xunieTHGabGkCSXwa116RtJotrYkcVwgP8jVUk4oFD/9LZfahAXID034weeJG6+vGUUpVY4pFzJp0PfB90/AuW3ndBDldM375LpHsdHGQ3xbhrkmlljX6MrF2CEK2PfjJh9B3/ltl+g6YyCOzFlbO9AZYljnQlAsnKibd4m6CGk30+2pduNQ1yOY4gUZ/0GkkN7UzbgzWE9sgeNtrEHkGRyiC4iDdKxDPoMmU+b2dNwNbvvZjIp3X0SQkGRQzE78lveU2fYHc1B0qYuH1WiwcP8fJex/l0stPsXr1ddzixFiabTcTOixISBPFyhhR7m7HlSGwsK2IaZNXkS3/HgQkmewNDmqATgMtVUzqRhUcC4ltEzhvPYsk8HobTg0ArxtcjVv8gdUuzJQFx4aX68LxioHv34x/3X57hz+CPPjjqrMnkckyTNs4OePjFV1Tyz1RhokcTOWUjG062ARDoXa1a0gevVjoBdD1lOTmp7TB8dKI0VYEfQ8aKyaKrdTMh61F5MpXof6SGV219semxU8s0wfhrxlyxt00ju1giYVYFpXZE1qbOUYmmyXyWpx/7ouyOZXoTdJaqeaqyc7TqWA4a20qVyA/Dw//M6V6CtGNCe02TB3f0oppUl3iuAZN5LoQJUi/b7IOlmzmbtVSE7ydqm3fBduSyBa2KLWiUVI5x4ATZoq7+YB3fBx5yw+rHnuLYS0omwA0Z3ClTBfMrNmFgiG1zg7cgwRhZSB4q74hkfRCpR+J6aVXvVWDNGIzR9XrQ7Nu2JsqEwbJ0mlA4Jtv2jmzu6IGG9D4VDQicbSReKC1fEH81ipi26AxSRSkjmz3UxrbKVodGtXq8BSLkm6m3o6C6S2buq9YW6Zax5v1Tx1oRRExzWNRjFr2oPPINqghtrZvGmAD13swM4D6b71aMbnhWIVW30xicmxhzTMwLucmdYHc8XH03F9WPf4QMuFilwU3r1QdJW8bOoZTFahkDJZv683VfdOSt9I3PH5BAv0QomQr1PtGxCaoSTz3fKTThKCNFirg5pDAM6yeUQBODqpnDPfdcD6loTm3OOjTC/oHos32M5QxTW14Ny7BnfCZOg5gQRV545eE8t9XrC1tDt01yE9upiSMbMao3zeEn45tfD9LtlWtZCOF1ouQeCDYluw0PI8wEXqh6d9OYiWIZctqTr8POfld6Lm/qJx4FKpZrKKQzUE5YzrWFopwuKjM5g1n3Ea0o5gZHYttaHiGxjVSEwFFCTdU8hZSbCzQbox4HvQ60G+h2YIZSaViEsuRbxKoImh2AtrPQdRNBRcbNkoi7W/TdLilGUM7Tk1Xhxzj5nsZRQ28M4BV0au/Z2YPY93oDOs1IOhvUb+DElUUgu8Z4bJMLX0DkqWbgorJJnRDA+naiuXaxr6lhLHSCgw/pL+ZhqncDef+rurpR6CSR2oudj7BdQxFbs01bFUnqko1b/y8jWvUAUfLtTYsdYW6b2bPBokQhrrLwggSJrAaQsdDem3UyZg8nyoS9NFeCwmaaPsCkp1A/BX0+meEsDkUDzeKgWAk3bDs3Bg07muc8bVpk9qawl9Mx2ChSOc8Wjp8Y4yXJhD2wMkPYpRBC+0GbtC2IZszhALxDeuqG/k0BV0zDfEykdmsjGzO+tuCtPYiCFxjrS3JTMA3/ppy97uRwxVkxiFTVSolYaYItSxkLeWeaajlQHSAwVNIBjMmLneENxqm0tGJoBsJ/UB33Z5qga6Adn1DrOg4UFsAx4UoMCRBCOq1TPQL6NN/RwjWhzrlw6Y2DdUSsh3dPGr603ANk77qMaoistt4jDTTYYZPMEjQz//XQmiatTZKZOK1kSQ0OcJNHP5gmHevi4Qe2LI5IU9RU8bb+P3m4O8tm1hvXnzzheaA2c7R776gTBSgLNgVJZcT8o5SckyObzIrnJvWLaOebmjAfmL4Vq60DU9cL1aCEOJNDo2b/NGN7W4JtNrQvIYUimixavJ5/Z5pAAp96C4j3jV4+Sdl0zFmd45lYXiz+NBSmg4HA6Quee1By+0U8aYBLKCjE9wj85pib1YuBDEBhteEQm0A5ksGWTVBSdBOx8xXdrODax5Qd2wUE1Sh7iFRbKJUuXWLKsaHjBJYaikWMwWYsrGrFrmsQbIWbVNOmy/CqaoSJ9sNWKymc+21psWVDrRDoe0rnm+Szbc4Xxsu4EZD0Rt9pL0GpRoUK0YXR4Hx95IA6a8gYW8whUe34jpS58x2y73tyDSaIpgYdu5xfMedyrRpfyNDXA+GBCo7ux8KX/xvB6k/64bW8tsGqrXljlXjTV9Ogx7Saw2CwS3Dw7fmGvsRtOIbxDHbxI9tKtKhZpMtm6nZOdv4fJMZOFyBasZ0NclWtiSETgivrMNKX/Ei6AY66AuQ7TZsO3LQ7JZEoNtFC2XIZFFJTFogCsyc29BDIx/pL6Kv/hvZKXWTFmuXliwoDQIlTTAxiq5jnPFnafGHad5nN1+ycxGsHGgwqCwZDaG95oCZMnuLeRDbQS1nO5vbQAtu9mZHCdIPkRkXDW96Elv8GBGw7BLYtpJzhKIrTOSE2SJUXDMjwh606w3o/FjqKpfaSt03gt4PTSNRtDVDfrP7t4HHVoWVrvEv3MyNBphkwEofdCDsGEhQ3IPWS+zWibZTJCh7rGiMo7Ek5XvDolUZU/BH/WbUZ7sHawm88m/M85ctGi0KkDi80WS2YUp1Q4mEiN8buBDWDbmSDT5HUC+Etf72/tOtF2MZobLsrPl7xjYN4gtFZbYwYD3a8oMYoRUKr64L59eFjg/90HTJR/FNRWW2I5w3idgDRVd6mx37mwXjKDQRWOxB5CGRB51Lt6zEqMXXPQqS7sME7sbxJ+PWafeYcxx1/cPSNWgCr35qQPxiOudIBnx4SWIqT1uFcOt6xYGB521Gu7I9hxgmJNf6psf2JjOxlbbZyliKbQsl1wjfTN7AquwBYWE8SBiu9IVnVoTrPnQSw23Y7pts9i2IDLl1C0o/Rq4FkMsMcsmDBGEQIr2G8f/sDGCjzVfg1Z+THbyWPVGapRFW3fmyt/2XpoU1DbpFUmiqYb+7uRE+rS+469GT4EZPtWUZnpj+uvHDN7uJtvzEdlGxb9SSN9s2N6mMNn+nl9sm5bZ5MRtzVgZN7JYIh7PKqbKpbCRbmEgTDN/H02vw1JKy2FH6sdAPhH7INmCh7LbtNj5INjiJNxqlLVPC6a0bny/oQH8dg6WxU1Ne6BhmaVym+pEaZIiGkxT5vbSR8i3Xr+m0dCqNqzH8wUfMiCgxrZubra3tNSQaTLDboCYTMWikJIJO8wad77Ya4pbeYUvQi222dSdtuSJnLmeI0m3LJJQdgV4khJhu9/PrZv7LxpSiTld37x256alujGylF6GLvS1Nz2YuiPqhkXivA2HP7Jz6U8iL/0wSdNcF0hTAgb0kkTUl2iXN70dF7GnJLIcFVmk1/GhkTYKyUR+OzZoMmsYkiTcBpCI3WA/Uskxf0ADbJ7rls412drkBw+dSGw4Vb8x5GPSQWEcLSsbZyEcJXiw0A1NbfqMptGKhFZjSWrd7g2Zk14YI2axrG1nzQljpbsn4boFve20k8g2wdKM4HrZIvLWRke+u3WeS9qHv7C2Mg1wZlXbREbnDncqFu8G7Us1oTpFW2jkPmSDP/qTgDxr0LftGzb3XQMJwe2ebWCYfqGq6FjdYyQYdirL1yQzWVcMYFnsmAbiFccAquXqjEV7M5IRGaAAF7UDxVfHVzBALk51XRTdKipGZWkk0qPUCeIoGg1TLRjhtDXB//eaN4APQ/jK6/FVJndHfyWTqeE0+aXqf0xBQpvZDhZFRPSnBBcPym2ldkE25Wv4CErQQLFTMfyKWGQ3bb5nemy1CtlEkIYmR0B8I7vbSklo3vg9ihLCfmH7jQVLEsgcO5kbHYycSVj1TVvMSk2IJAqHX3+L8bobSuslgILEifYVGYqgPRJAggW5idpRl3QjrEQNACDqmsSiJzTHa55Glz95IWI6pxfYaZY4KBEaBEjRFOU24FSaX1u9LEwXrkPvRFPeo6kF/1eRyN3SYGJCwBh1jisUe4DAH3ZFiGaH0e4MJS5ZhZB0oGREx2MENwbUE7arpukMRUUNOhGVmwK54cLGlLPZM+2c/Nrwfoa+biW8so/GwdZPWVQKFZmJI/QoyGPCnSByjfmguwLHNnDIsQ/7TqyMaDvxVB4l64K3eMhA6jZ+jexS2YceUIT6XjlGR0D3m9tIET6NSPbuZ9p2vRdHn/k/oLA+CkUE+dyP4SELjzxs4vHlfrIHGtNEkMdMQLNsAFwafb0TW2LZJbvuBQSMkxlQ5UQK9WFhqwfU+hGp4meNE6PV1W1CjW3KSJoGssK4GUMpgaEzegoygrRhditicEcXA+YwGY6TiFlgOkiRGKyw9Dq/8rIxjMncql+0l4NAU7+131tvteO0F5jX0WN2nhKiryID6Pk4GiWaF1opZy/Kk4eixTAStikFWN5fRyiyaMak0sQa8PnLT2QeN75IAcw7/H5wUt87SGxFUAAAAAElFTkSuQmCC';
        function buildReloadSprite(player) {
            const c = document.createElement('canvas');
            c.width = 160; c.height = 160;
            const im = new Image();
            im.onload = () => {
                const g = c.getContext('2d');
                g.drawImage(im, 0, 0);
                if (player.color.toLowerCase() === '#1e90ff') return;   // 원본 그림이 이미 이 색
                const d = g.getImageData(0, 0, c.width, c.height), px = d.data;
                const n = parseInt(player.color.slice(1), 16), tc = [(n >> 16) & 255, (n >> 8) & 255, n & 255];
                for (let i = 0; i < px.length; i += 4) {
                    if (px[i + 3] === 0 || px[i + 2] < 100 || !(px[i + 2] > px[i] * 1.5 && px[i + 2] > px[i + 1] * 1.2)) continue;
                    const mx = Math.max(px[i], px[i + 1], px[i + 2]), mn = Math.min(px[i], px[i + 1], px[i + 2]);
                    if ((mx - mn) / mx < 0.7 && px[i + 2] < 200) continue;   // 파란 손만 (채도가 낮고 어두운 푸른 회색 = 총은 그대로)
                    const r = (px[i] * 0.3 + px[i + 1] * 0.59 + px[i + 2] * 0.11) / 105;
                    for (let k = 0; k < 3; k++) px[i + k] = Math.round(r <= 1 ? tc[k] * r : tc[k] + (255 - tc[k]) * Math.min(1, (r - 1) / 0.9));
                }
                g.putImageData(d, 0, 0);
            };
            im.src = 'data:image/png;base64,' + RELOAD_B64;
            return c;
        }
        p1.reloadSprite = buildReloadSprite(p1);
        p2.reloadSprite = buildReloadSprite(p2);

        // ===== 2P 1인칭 주먹: 팔이 아래 모서리에서 대각선으로 올라와 가운데에서 주먹이 마주 보는 그림 (왼손 기준, 오른손은 좌우 반전) =====
        // 그림 좌표(104x104 칸 기준)를 (x+ARM_OX, y-ARM_OY) 픽셀로 옮겨 그림. 팔은 화면 밖까지 이어지도록 크게 만듦
        const ARM_OX = 60, ARM_OY = 40, ARM_W = 112, ARM_H = 132;
        const ARM_SCALE = 0.7;   // 화면에서 차지하는 크기 (작을수록 시야를 덜 가림)
        const ARM_ANCHOR_X = 35 + ARM_OX, ARM_ANCHOR_Y = 55 - ARM_OY;   // 주먹 중심
        function generateArmSprite(color) {
            const c = document.createElement('canvas');
            c.width = ARM_W; c.height = ARM_H;
            const g = c.getContext('2d');
            const base = color, hi = shade(color, 0.35), spark = shade(color, 0.6);
            const mid = shade(color, -0.15), dark = shade(color, -0.35), deep = shade(color, -0.7);
            const FIST = [[19.5, 60], [23, 52], [27, 47], [31, 43], [35, 41.6], [41, 41.6], [44, 44], [48, 46], [48.5, 51],
                          [50, 54], [50, 58], [47, 61], [43, 63], [39, 66], [35, 68], [31, 68], [27, 66], [22, 64]];
            const inPoly = (x, y, P) => {
                let o = false;
                for (let i = 0, j = P.length - 1; i < P.length; j = i++) {
                    const [xi, yi] = P[i], [xj, yj] = P[j];
                    if ((yi > y) !== (yj > y) && x < (xj - xi) * (y - yi) / (yj - yi) + xi) o = !o;
                }
                return o;
            };
            for (let py = 0; py < ARM_H; py++) for (let px = 0; px < ARM_W; px++) {
                const x = px - ARM_OX + 0.5, y = py + ARM_OY + 0.5;
                const rEdge = 31.5 - 0.389 * (y - 68);          // 팔 오른쪽(안쪽 아래) 가장자리
                const inFist = inPoly(x, y, FIST);
                const inArm = y >= 58 && x + y >= 81 && x <= rEdge;   // 위쪽 왼쪽 가장자리는 x+y=81 선
                if (!inFist && !inArm) continue;
                // 밝기 값 t(0 가장 밝음 ~ 1 가장 어두움)를 만들고, 5단계 색으로 바꿈. 경계는 체크무늬로 섞어 부드럽게
                let t;
                let crease = 0;
                if (inFist) {
                    const u = (x - 19.5) / 30.5, v = (y - 41.6) / 26.4;
                    t = 0.2 + 0.5 * (0.9 * u + 1.1 * v) / 2 * 1.6 - 0.05;               // 왼쪽 위에서 오른쪽 아래로 점점 어두워짐
                    t += Math.max(0, v - 0.78) * 1.4 + Math.max(0, u - 0.88) * 1.2;      // 아래·오른쪽 가장자리는 조금 더 어둡게
                    t -= 0.4 * Math.max(0, 1 - Math.hypot(x - 36.5, y - 44.5) / 4.5);    // 윗면 반짝임
                    t -= 0.18 * Math.max(0, 1 - Math.hypot(x - 28, y - 55) / 6);          // 손등 윤기
                    const cdx = x - 43.2, cdy = y - 52;                                   // 손가락이 말려 들어간 틈: 비스듬한 가는 타원
                    const ca = cdx * 0.5 + cdy * 0.866, cb = -cdx * 0.866 + cdy * 0.5;
                    const e = Math.hypot(ca / 3.8, cb / 1.5);
                    if (e < 1) crease = 2; else if (e < 1.6) crease = 1;
                    if (!crease && x > 44 && x < 49.5 && y >= 52.2 && y < 53.4) t += 0.22;   // 손가락 사이 선 (살짝만)
                    if (!crease && x > 43 && x < 49.5 && y >= 57 && y < 58.2) t += 0.2;
                } else {
                    const c2 = (x + y - 81) / Math.max(1, rEdge + y - 81);            // 팔 가로 위치 0(위쪽 왼쪽)~1(아래 오른쪽)
                    t = 0.1 + 0.8 * Math.pow(Math.min(1, Math.max(0, c2)), 1.1);
                    if (c2 < 0.3 && Math.floor(y / 6) % 2 === 0) t -= 0.22;           // 팔을 따라 이어지는 밝은 줄
                    t += 0.28 * Math.max(0, (73 - y) / 15) * Math.min(1, c2 * 3);       // 주먹 바로 아래 손목은 그림자
                }
                const PAL = [spark, hi, base, mid, dark];
                const f = Math.min(4, Math.max(0, t * 4));
                const bayer = [0.125, 0.625, 0.875, 0.375][(py & 1) * 2 + (px & 1)];
                const fr = Math.min(1, Math.max(0, ((f % 1) - 0.3) / 0.4));        // 색이 바뀌는 좁은 구간에서만 섞음
                const k = crease === 2 ? deep : crease === 1 ? dark : PAL[Math.min(4, Math.floor(f) + (fr > bayer ? 1 : 0))];
                g.fillStyle = k;
                g.fillRect(px, py, 1, 1);
            }
            // 검은 테두리: 그림 바로 바깥 한 칸(상하좌우)을 검게
            const src = g.getImageData(0, 0, ARM_W, ARM_H).data;
            const filled = (x, y) => x >= 0 && y >= 0 && x < ARM_W && y < ARM_H && src[(y * ARM_W + x) * 4 + 3] > 0;
            g.fillStyle = '#000';
            for (let py = 0; py < ARM_H; py++) for (let px = 0; px < ARM_W; px++) {
                if (!filled(px, py) && (filled(px - 1, py) || filled(px + 1, py) || filled(px, py - 1) || filled(px, py + 1))) g.fillRect(px, py, 1, 1);
            }
            return c;
        }
        p1.armSprite = generateArmSprite(p1.color);
        p2.armSprite = generateArmSprite(p2.color);

        // 1인칭 단검: 칼 든 오른손 전용 그림. 칼은 기울기를 처음부터 그림에 반영해 그림(회전으로 뭉개지지 않게), 주먹이 원점
        const KNIFE_OX = 16, KNIFE_OY = 54, KNIFE_W = 52, KNIFE_H = 78;
        const KNIFE_TILT = 0.45;
        const KNIFE_DROP = 0.07;   // 칼을 화면 아래로 내리는 정도 (화면 너비 비율, 클수록 더 아래)   // rad (약 31도): 날 끝이 화면 안쪽(가운데)으로 기울어 있음 (팔뚝 방향과 이어지게)
        function generateKnifeSprite(frontOnly) {   // frontOnly: 손가락 아래로 나온 자루 끝(손 앞에 그려질 부분)만
            const c = document.createElement('canvas');
            c.width = KNIFE_W; c.height = KNIFE_H;
            const g = c.getContext('2d');
            const STEEL = ['#f1f5f8', '#c3ccd5', '#98a4af', '#6b7681', '#454e57'];
            const sn = Math.sin(KNIFE_TILT), cs = Math.cos(KNIFE_TILT);
            const BLADE_BASE = -16.5, BLADE_LEN = 36;
            for (let py = 0; py < KNIFE_H; py++) for (let px = 0; px < KNIFE_W; px++) {
                const x0 = px + 0.5 - KNIFE_OX, y0 = py + 0.5 - KNIFE_OY;
                const x = x0 * cs + y0 * sn, y = -x0 * sn + y0 * cs;   // 칼 기준 좌표: y 음수 = 칼끝 쪽, 양수 = 자루 끝 쪽
                if (frontOnly && y < 14.6) continue;
                let k = null;
                const t = (BLADE_BASE - y) / BLADE_LEN;                    // 날 위치: 0 (날밑) ~ 1 (끝)
                if (t >= 0 && t <= 1) {
                    const hw = t < 0.55 ? 4.6 : 4.6 * (1 - Math.pow((t - 0.55) / 0.45, 1.4)) + 0.3;   // 곧은 양날 + 끝이 뾰족한 단검 모양
                    if (Math.abs(x) <= hw) {
                        const u = x / hw;
                        k = u < -0.65 ? STEEL[0] : u < -0.15 ? STEEL[1] : u <= 0.15 ? STEEL[2] : u < 0.65 ? STEEL[3] : STEEL[4];
                    }
                } else if (y >= BLADE_BASE && y <= -13.5 && Math.abs(x) <= 7.5 &&
                           !(Math.abs(x) > 6.5 && (y < -15.5 || y > -14.5))) {   // 십자 날밑
                    k = y < -15.5 ? '#7d8893' : y < -14.5 ? '#4a525b' : '#262b30';
                } else if (y > -13.5 && y <= 17 && Math.abs(x) <= 2.9) {     // 가죽 감은 자루
                    const band = Math.floor((y + 13.5) / 2.5) % 2 === 0;
                    k = x > 1.2 ? '#0e1114' : band ? '#3d444b' : '#272c31';
                } else if (y > 17 && y <= 20.5 && Math.abs(x) <= 4 && !(Math.abs(x) > 3 && y > 19.5)) {   // 고리 포멜
                    k = y < 18 ? '#aab4be' : y < 19.5 ? '#6b7681' : '#2e353c';
                    if (Math.abs(x) < 1 && y > 18 && y < 19.5) k = '#14181b';
                }
                if (k) { g.fillStyle = k; g.fillRect(px, py, 1, 1); }
            }
            // 검은 테두리 (다른 그림과 같은 방식)
            const src = g.getImageData(0, 0, KNIFE_W, KNIFE_H).data;
            const filled = (x, y) => x >= 0 && y >= 0 && x < KNIFE_W && y < KNIFE_H && src[(y * KNIFE_W + x) * 4 + 3] > 0;
            g.fillStyle = '#000';
            for (let py = 0; py < KNIFE_H; py++) for (let px = 0; px < KNIFE_W; px++) {
                if (!filled(px, py) && (filled(px - 1, py) || filled(px + 1, py) || filled(px, py - 1) || filled(px, py + 1))) g.fillRect(px, py, 1, 1);
            }
            return c;
        }
        const KNIFE_SPRITE = generateKnifeSprite(false);   // 손 뒤: 칼날·날밑·자루
        const KNIFE_FRONT = generateKnifeSprite(true);     // 손 앞: 손가락 아래로 나온 자루 끝

        // 1인칭 총: 참고 그림(두 손으로 권총을 잡은 모습)을 도트로 옮긴 것. 플레이어 색으로 칠함
        // 0~4: 손·팔 (0 가장 밝음 ~ 4 가장 어두움) / a~h: 권총 회색 (a 가장 어두움 ~ h 가장 밝음) / . 은 빈칸
        const GUNVIEW_SPLIT = 64;                 // 이 열부터 오른쪽이 권총 든 오른손 (왼쪽 열의 왼손은 쓰지 않음)
        const GUNVIEW_TOP = 0.46;                 // 총구 높이 (화면 높이 비율, 클수록 더 아래)
        const GUNVIEW_MUZZLE = [70.5, 2.5];       // 총구 위치 (그림 칸 좌표)
        const GUNVIEW_PIVOT = [86, 40];           // 오른손 반동의 회전 중심 (그림 칸 좌표)
        const GUNVIEW_GRAY = ["#040d1d", "#071329", "#0d1b32", "#112342", "#1b2c48", "#374559", "#495970", "#8a9cb3"];
        const GUNVIEW_ROWS = [
            '...............................................................................................................................',
            '.....................................................................h.........................................................',
            '.....................................................................f.........................................................',
            '..................................................................fhhdeggc.....................................................',
            '..................................................................ghhhhhhhe....................................................',
            '..................................................................gghhhhhhhg...................................................',
            '..................................................................fffhhhhgggfc.................................................',
            '..................................................................ffgghhhffffec................................................',
            '..................................................................gffgghhhgfgfee...............................................',
            '..................................................................fgffgghhhhggggge.............................................',
            '...................................................................eggggghhhhhhhhgf............................................',
            '...................................................................gcgggggghhhhhhhhge.gg.......................................',
            '...................................................................fg.gggggfhhhhhhbcdae.d......................................',
            '....................................................................fgbggggffhhhgg.ggah.a......................................',
            '....................................................................effdgggfffhhhfbcbbcbde.....................................',
            '.....................................................................egfdggfgfghhhhhhhhhhhe....................................',
            '.....................................................................dfgefgfgfgfhffeeeeeefd....................................',
            '......................................................................effdffgfgfhfeccccccfd....................................',
            '......................................................................cfeeeegfgfhfadddddddd....................................',
            '..............................................43333444................ecddfeffgfhfceeeeeeed....................................',
            '............................................32000001124...............d.ceefefgfhfbedeedddd....................................',
            '..........................................420h001222222d.................cedfdgfhfb.bbb..dd....................................',
            '........................................a20000012333333e.................bedeg.fhfc..a..be214..................................',
            '.......................................2100000012444433c................e4ccceg.heacccccca40024................................',
            '.....................................42000000111344c44e................d12eeeefh...a....a.b30013...............................',
            '....................................42200000011234....................b303cdeeedhfffffffffc310014..............................',
            '...................................42310000111234cb4434b..............b324bbddc..dcccccccbb310003a.............................',
            '..................................423210000111234be432224.............a4344eeeb....aaaaa.b42000124.............................',
            '.................................d233110000111234ad444322b............a310002244a........420001224a............................',
            '................................4233210000011124dabc444444444.........400000001234e....a4310001233c............................',
            '................................32320100001111234..abe44300024........2000000000123444443200001133d............................',
            '...............................233201000001112234.a...e2000023.......a11110000000112233332100002234a...........................',
            '.............................d3332101000011122334acc.c21000124.......322221110000011222222110002223a...........................',
            '.............................42321010000122111234acdd310001234.......223222111000000111111111001223a...........................',
            '............................433210010000222111234abb4200011234.......2344322221100000111122111012233...........................',
            '............................43320011000122211233d.a4200011234e.......3344433222210000011122111112233...........................',
            '...........................a43210110001222221234d431000112344.........444c433222110000111221111122234..........................',
            '...........................d32101110012222222333221000022344..........aedac43322221100011222211122233..........................',
            '..........................a42201110001222222222110000012344d...........b44ae3322222211001222221112233d.........................',
            '..........................b3211110000122222221110000012334d............4234d43222222221011222111112234.........................',
            '..........................4211110000112222222111000111234d.............4113443322222222111121100011233b........................',
            '.........................a3111000001122222222121111122344..............b213e443322222222212211000001234........................',
            '.........................3211000000122222222222122222344................3234b43333222222222111100000123d.......................',
            '.......................43211000000222222222222222222234c................d34e.444333222222222111100001123d......................',
            '......................321110000012222222233332222222344..................abba.444333332323321112100000123d.....................',
            '.....................321110000012222223333332222233344e..................e234a.444333333432211111110001123c....................',
            '....................3211100000122222223333322222333444...................4123da.444444444321111111000000124....................',
            '...................3211100001112222222443322223333444a...................d223dba.44444444322211111100000123c...................',
            '..................42111000011222222222344333333334444....................a434dcbb.c4444443322211111110000122b..................',
            '.................4211100001112222222233444433334444.......................d44bcdbd.c444e443322211111200000123a.................',
            '...............a4211000000112222212233344e4444444da.......................434bcdbea...bb4443322111122100001124a................',
            '..............432110000000112221122334444e44444cb.........................c33dcdbfca....44343322111111100001123b...............',
            '.............4321100000001122211123343344dbaaba............................b4ccdagcbb...443343222111111100001123b..............',
            '............4221100000001222221133343344......................................ccagccba..4443333322111111000001123a.............',
            '...........43210000000011222221233443444......................................deagdcbaa.a4433343222111111000001123.............',
            '..........42210000000011222222233443344........................................dagebbbb.b44432233322111111000001223............',
            '.........32210000000001222222123443344........................................cbbgebbca..a44322333221111110000001223...........',
            '........32100000000011222222123433344a.........................................e.geccab.a.d43322333221111110000001223..........',
            '......b321100000000012222222233333444...........................................efd.......c433332333211121110000001223b........',
            '.....b321100000000012222222223323344b...........................................bfa.....b..4433322333112221100000001223c.......',
            '....c3211000000000122222212233333444.............................................ba........c4333322331122221100000011123d......',
            '...43211100000000112222222233333344b........................................................44433322222222221100000011123c.....',
            '..432111000000001122222221233333344.........................................................a44333222212222221100000011123d....',
            'a321111000000001122222221223333344...........................................................444333222112222211110000011123d...',
            '3211110000000011222222222333333344............................................................4433322221111222111000001111234..',
            '211110000000112222222221233333344.............................................................44433222211111122111100001111224.',
            '111100000000112222222212333333344..............................................................44333222212211222111000000111224',
            '11100000000112222222221333333344...............................................................44333322212221222211100000011112',
            '11000000010122222222223333333344................................................................4433322212232122221110000001111',
            '1000000111122222111123333333344.................................................................4433332222233221111111000000111',
            '0000001111122222221223333333444.................................................................b443333222233322122111100000011',
            '0000001111222222221123333333444.................................................................a443333222233332222211110000001',
            '000000111222212332223333333344a..................................................................c44333322233332212212110000000',
            '000001122222123332123333333444...................................................................b44333332233333222222111000000',
            '00001121221123333222333333444b....................................................................44433332233333321222111100000',
            '00111221111233333223333333444a....................................................................b4443333222333321222211110000',
            '0111122111123333333333333444d......................................................................4443333323333332112211111000',
            '0112222211233333333233333444.......................................................................a443333322333333111221111100',
            '1111222111333333333333334444........................................................................444333332333333221211111111',
            '111222111233333333333334444a........................................................................444433332233333321111111111',
            '121222111333333333333334444..........................................................................44433332233333331111111111',
            '11111211233333333333334444c..........................................................................44433332223333332222111111',
            '11111112333333333333334444...........................................................................a4443333222333333211111111',
            '1122111333333332333334444a............................................................................4443333322333333311111111',
            '1121122333333333333344444.............................................................................b443333332233333332111111',
            '111112333333333333334444..............................................................................a444333333223333332111111',
            '11112333333332333333444c...............................................................................c44333333322333332211111',
            '1112232223333333333444e................................................................................a43333333322222333221111'
        ];
        function generateGunViewSprite(color, c0, c1) {   // 열 c0 ~ c1-1 만 그림 (위·아래·양옆으로 검은 테두리 한 칸 여유)
            const w = c1 - c0, h = GUNVIEW_ROWS.length;
            const c = document.createElement('canvas');
            c.width = w + 2; c.height = h + 2;
            const g = c.getContext('2d');
            const PAL = [shade(color, 0.6), shade(color, 0.35), color, shade(color, -0.15), shade(color, -0.35)];
            GUNVIEW_ROWS.forEach((row, r) => {
                for (let q = c0; q < c1; q++) {
                    const ch = row[q];
                    if (ch === '.') continue;
                    g.fillStyle = ch < 'a' ? PAL[+ch] : GUNVIEW_GRAY[ch.charCodeAt(0) - 97];
                    g.fillRect(q - c0 + 1, r + 1, 1, 1);
                }
            });
            const src = g.getImageData(0, 0, w + 2, h + 2).data;
            const filled = (x, y) => x >= 0 && y >= 0 && x < w + 2 && y < h + 2 && src[(y * (w + 2) + x) * 4 + 3] > 0;
            g.fillStyle = '#000';
            for (let py = 0; py < h + 2; py++) for (let px = 0; px < w + 2; px++) {
                if (!filled(px, py) && (filled(px - 1, py) || filled(px + 1, py) || filled(px, py - 1) || filled(px, py + 1))) g.fillRect(px, py, 1, 1);
            }
            return c;
        }
        [p1, p2].forEach(p => {
            p.gunViewR = generateGunViewSprite(p.color, GUNVIEW_SPLIT, GUNVIEW_ROWS[0].length);
        });

        // 칼 든 손: 원래 팔+주먹 그림 위에 손가락 4개가 자루를 감싸 쥐고, 엄지가 자루를 따라 날밑 쪽으로 뻗은 모양을 덧그림
        function generateKnifeHandSprite(color) {
            const c = document.createElement('canvas');
            c.width = ARM_W; c.height = ARM_H;
            const g = c.getContext('2d');
            g.drawImage(generateArmSprite(color), 0, 0);
            const CUT = 18;                                   // 이 줄 위(원래 주먹 자리)는 지우고 새 손으로 채움, 아래는 원래 팔을 그대로 씀
            g.clearRect(0, 0, ARM_W, CUT);
            const PAL = [shade(color, 0.6), shade(color, 0.35), color, shade(color, -0.15), shade(color, -0.35)];
            const deep = shade(color, -0.7);
            const sn = Math.sin(KNIFE_TILT), cs = Math.cos(KNIFE_TILT);
            const rect = (v, a0, a1, p0, p1, al, pp) => Math.hypot(pp - Math.min(p1, Math.max(p0, pp)), al - Math.min(a1, Math.max(a0, al)));   // 직사각형까지 거리
            // 자루 기준 좌표 (al: 자루 방향, 0 = 주먹 중심 / pp: 자루와 직각, + 쪽이 손가락 쪽)
            const each = fn => { for (let py = 0; py < ARM_H; py++) for (let px = 0; px < ARM_W; px++) {
                const rx = px - ARM_OX + 0.5 - 35, ry = py + ARM_OY + 0.5 - 55;
                fn(px, py, -rx * sn + ry * cs, rx * cs + ry * sn); } };
            const dot = (px, py, col) => { g.fillStyle = col; g.fillRect(px, py, 1, 1); };
            // 둥근 면 조명: (nx, ny) = 표면 기울기(-1~1, nx는 +pp 쪽, ny는 +al 쪽). 왼쪽 위에서 빛이 오는 구/원통처럼 칠함
            const lit = (nx, ny) => {
                nx = Math.max(-1, Math.min(1, nx)); ny = Math.max(-1, Math.min(1, ny));
                const nz = Math.sqrt(Math.max(0, 1 - nx * nx - ny * ny));
                const b = -0.3 * nx - 0.55 * ny + 0.78 * nz;
                return PAL[b > 0.95 ? 0 : b > 0.84 ? 1 : b > 0.5 ? 2 : b > 0.25 ? 3 : 4];
            };

            // 1) 손등: 자루 오른쪽(pp<0)에서 팔로 이어지는 둥근 덩어리 (팔 위쪽 끝 줄 위에만)
            each((px, py, al, pp) => {
                if (py >= CUT) return;
                const d = rect(0, -8.3, 6.8, -6.0, -4.2, al, pp), R = 4.2;
                if (d > R + 0.8) return;
                if (d > R) { dot(px, py, deep); return; }
                dot(px, py, lit((pp + 5.1) / 5.1, Math.min(0, (al + 8.3) / 4.2)));
            });

            // 2) 손가락 4개: 자루 왼쪽(pp>0)으로 감아 쥔 둥근 막대. 검지가 굵고 새끼로 갈수록 작음
            const FP = 5.2, FA = -3.2;
            const FB = [8.8, 9.2, 8.4, 6.8], FR = [2.5, 2.5, 2.4, 2.2];
            const fy = i => -5.9 + FP * i + FR[i] + (i ? 0 : 0.1);
            for (let i = 3; i >= 0; i--) each((px, py, al, pp) => {
                const d = Math.hypot(pp - Math.min(FB[i], Math.max(FA, pp)), al - fy(i));
                if (d > FR[i] + 0.7) return;
                if (d > FR[i]) { dot(px, py, deep); return; }
                const du = pp - Math.min(FB[i], Math.max(FA, pp));            // 양 끝 둥근 부분에서만 0이 아님
                dot(px, py, lit(du / (FR[i] + 0.4), (al - fy(i)) / (FR[i] + 0.4)));
            });

            // 3) 엄지: 검지 위를 가로질러 끝이 왼쪽으로 나오고, 날밑 바로 아래를 누름
            const TA = -4.5, TB = 8.8, TY = -9.3, TR = 2.8;
            each((px, py, al, pp) => {
                const d = Math.hypot(pp - Math.min(TB, Math.max(TA, pp)), al - TY);
                if (d > TR + 0.7) return;
                if (d > TR) { dot(px, py, deep); return; }
                const du = pp - Math.min(TB, Math.max(TA, pp));
                if (Math.abs(pp - 1.6) < 0.5 && Math.abs(al - TY) < TR * 0.6) { dot(px, py, PAL[3]); return; }   // 엄지 마디 주름 (부드럽게)
                dot(px, py, lit(du / (TR + 0.4), (al - TY) / (TR + 0.4)));
            });
            return c;
        }
        p1.armKnifeSprite = generateKnifeHandSprite(p1.color);
        p2.armKnifeSprite = generateKnifeHandSprite(p2.color);

        // 1인칭 발차기: 참고 그림(맨발 + 비스듬히 뻗은 다리)을 5단계 색 번호로 옮긴 도트 (0 가장 밝음 ~ 4 가장 어두움, . 은 빈칸)
        // 플레이어 색으로 칠하고, 발 중심(LEG_OX, LEG_OY)이 기준 (아래로 길게 이어짐)
        const LEG_OX = 13, LEG_OY = 25;
        const LEG_ROWS = [
            '..........2223.....................................................................',
            '.........200002....................................................................',
            '........32000133...................................................................',
            '.....201220012311..................................................................',
            '....20012322234333.................................................................',
            '...2100134222343212................................................................',
            '..411012342223431023...............................................................',
            '.42111234433324212222..............................................................',
            '.32111224443334322223..............................................................',
            '.321222244422343243342.............................................................',
            '.411001222223443344322.............................................................',
            '.310001122223433344322.............................................................',
            '.110001112222223344323.............................................................',
            '21000001112222222433340............................................................',
            '22000001112222222433430............................................................',
            '22100001112222222234421............................................................',
            '22111000111222222223322............................................................',
            '22211000011222222223323............................................................',
            '32222100001122222222234............................................................',
            '32222100001122222222234............................................................',
            '32222210000112222222234............................................................',
            '4322222100011122222224.............................................................',
            '.322222100011112222234.............................................................',
            '.332222100001112222234.............................................................',
            '.432222110000112222334.............................................................',
            '..3222221000011222334..............................................................',
            '..3222121000001223334..............................................................',
            '..4322112200001223344..............................................................',
            '...322111210001123344..............................................................',
            '...322111121001123344..............................................................',
            '...22211012100012344...............................................................',
            '..422111000110011244...............................................................',
            '..322121000110011244...............................................................',
            '..322221000000000144...............................................................',
            '..322211112211112233...............................................................',
            '..322111112211111223...............................................................',
            '..2221122320000001234..............................................................',
            '.32221233200000001223..............................................................',
            '.22222222100000000122..............................................................',
            '.22222321001100000122..............................................................',
            '2122232112211100001123.............................................................',
            '21222321122211000001224............................................................',
            '212224122222110000001234...........................................................',
            '2122342222222110000012234..........................................................',
            '2223342332222110000011233..........................................................',
            '2223343332222211000001222..........................................................',
            '32233433322222110000011223.........................................................',
            '32233443322222110000001222.........................................................',
            '43334443332222111000001122.........................................................',
            '.33334443322222210000001222........................................................',
            '.333344433222222110000001223.......................................................',
            '..434444332222221100000012222......................................................',
            '..4444433322222211000000112224.....................................................',
            '...444433322222211100000112223.....................................................',
            '.....4433322222211100000111222.....................................................',
            '......4333222222211100000011222....................................................',
            '......43332222222111000000112223...................................................',
            '......433322222221110000011112223..................................................',
            '......433322222221110000001112223..................................................',
            '......4333222222212110000000112223.................................................',
            '......3333222222212211000000112222.................................................',
            '.....433332222222222111000001112222................................................',
            '.....43332222222222211100000011122223..............................................',
            '.....33332222222222211100000001122223..............................................',
            '....4333322222222322111100000011122223.............................................',
            '....3232222222233322111100000001112223.............................................',
            '...422322222222333221111000000001122224............................................',
            '...3223222222223322211111000000011122244...........................................',
            '...32232222222333222211111000000011122234..........................................',
            '...22233222223332222211111000000011122233..........................................',
            '...22233322233322222211111111111111122222..........................................',
            '...22333322233322222211111111211111112222..........................................',
            '...333333223332222221111111111111111112223.........................................',
            '...333333223332222211111112211111111111122.........................................',
            '...3333333233322221111112222111111211111222........................................',
            '...43333333333222111111222222211111221011224.......................................',
            '....33333334332221111122222222111112221101233......................................',
            '....333333344322211122232222222111111221111234.....................................',
            '....333333343322111122332222222211111222111123.....................................',
            '....333333343321112233322222222221111133211123.....................................',
            '....4333333432111223332222222111111111232211233....................................',
            '....4333333432112233332222221111111111233222223....................................',
            '.....433334322122344322222211000000111223322223....................................',
            '.....443334322223343322222100000000001223332223....................................',
            '.....4433332222334432232210000000000001223322233...................................',
            '.....4433322223344332332100011111110000011333223...................................',
            '......443322223443333321111111111111100000133322...................................',
            '......4433222344433333111111111111111110000233224..................................',
            '......44321233444333221111111222233332211100124222.................................',
            '.......43222344433322111111112222222233222111123234................................',
            '.......43223344433221111111111111122233332211113333................................',
            '.......32233444332211111111110111111222333332212332................................',
            '......4332344433221111112211100111111222223433222334...............................',
            '......4332344433221111112211000011111122223443322344...............................',
            '......4333444322111112221110000001111112222333443224...............................',
            '......43334443221111222211100000000111112222334433334..............................',
            '......433444322111122221101100000001111111222234443344.............................',
            '......333443222222333211111100000000011111122222234444.............................',
            '......434443222222332211111111000000011111112222233444.............................',
            '......4444322222233322111111101000000111111112222223444............................',
            '.......444222223333322211111101100000110111111122232334............................',
            '.......4432222333332222211111111000000111121111222233334...........................',
            '.......4422222333322222211111111110000111111111112232223...........................',
            '.......33222233332222222211111111111111111111110112233233..........................',
            '......43322333333222222221111111110111111111111111122333334........................',
            '......33222333333222222222111111111111111111111111112233334........................',
            '......332233333332222222221122111111111111111001111112233334.......................',
            '......3222334433222222222221121111111111111111112211112233344......................',
            '......3222334433222222222222112111111111111111112221111233334......................',
            '......3223344433322222222222212211111111111111112222111123334......................',
            '......22333444332223322222222222211111111111111111232211123344.....................',
            '......23333444332223322222222222221111111111111111222221112334.....................',
            '......233344433222333222222222222211111111111111111223221122334....................',
            '......333344433222333222222222222221111111111111111122322222334....................',
            '.....3333444433222333322222222222221111111111111111112222222234....................',
            '.....33344444332233333222222222221221111111111100111112223222244...................',
            '.....33344443332333333222222222222122111111111100001111222333334...................',
            '.....333444433333333333222222222222211111111111100001111222233344..................',
            '.....3344443333333333333222222222222111111111110000011111222233334.................',
            '.....4344443333333333332222222222222211111111110000000111122223334.................',
            '.....43444333333333333322222222222222211111111111000000111122222344................',
            '.....44444333333333333332222222222222221221111111100000111112222233................',
            '.....444443333333333333332222222222222212221111111100001111112222234...............',
            '......444433333333333333322222222222222222221111111100000011112222234..............',
            '......4443333333333333333322222222222222222222111111100001111112222334.............',
            '......44433333333333333333222222222222222222222211111110001111122222234............',
            '......44433333333333333333222222222222222222222221111110000111112222233............',
            '.......44333333333333333333222233222222222222222221111100000111112222224...........',
            '.......333333333333333333333222332222222222222222222111110001111112222233..........',
            '.......3333333333433333333333223332222222222222222222111110001111122222233.........',
            '.......33333333334333333333333233322222222222222222222111100001111122222234........',
            '......4333333334443333333333333333322222222222222222222111110011111122222234.......',
            '......33333333344433333333333333333222222222222222222222111111111111122222234......',
            '......333333333444333333333333333333222222222222222222222111111111111122222234.....',
            '......3333333344443333333333333333333222222222222222222222111111111111122222334....',
            '.....333333333444433333333333333333333222222222222222222222211111111111122222344...',
            '.....3333333344443333333333333333333333222222222222111112222211111111111122222344..',
            '.....3333333344443333333333333333333332222222222222111112222211111111111112222334..',
            '.....3333333444443333333333333333333332222222222222111111111221111000101111222334..',
            '....433333344444433333333333333333333322222222222111111111111111100000011111222334.',
            '....3333333444444333333444333333333332222222222222222222222221111100000000111122234',
            '....3333333444443333334444333333332222222222222222222222222221111110000000011122233',
        ];
        const LEG_W = LEG_ROWS[0].length + 2, LEG_H = LEG_ROWS.length + 2;   // 검은 테두리 한 칸씩 여유
        function generateLegSprite(color) {
            const c = document.createElement('canvas');
            c.width = LEG_W; c.height = LEG_H;
            const g = c.getContext('2d');
            const PAL = [shade(color, 0.6), shade(color, 0.35), color, shade(color, -0.15), shade(color, -0.35)];
            LEG_ROWS.forEach((row, r) => {
                for (let q = 0; q < row.length; q++) {
                    if (row[q] === '.') continue;
                    g.fillStyle = PAL[+row[q]];
                    g.fillRect(q + 1, r + 1, 1, 1);
                }
            });
            // 검은 테두리
            const src = g.getImageData(0, 0, LEG_W, LEG_H).data;
            const filled = (x, y) => x >= 0 && y >= 0 && x < LEG_W && y < LEG_H && src[(y * LEG_W + x) * 4 + 3] > 0;
            g.fillStyle = '#000';
            for (let py = 0; py < LEG_H; py++) for (let px = 0; px < LEG_W; px++) {
                if (!filled(px, py) && (filled(px - 1, py) || filled(px + 1, py) || filled(px, py - 1) || filled(px, py + 1))) g.fillRect(px, py, 1, 1);
            }
            return c;
        }
        p1.legSprite = generateLegSprite(p1.color);
        p2.legSprite = generateLegSprite(p2.color);

        // 2P 전용: 그림 팔+주먹을 drawFist 와 같은 방식(중심 x,y / 크기 / 회전 / 좌우)으로 그림
        // knife: 칼 든 손 — 이때 sprite 는 칼 든 손 그림(armKnifeSprite). 칼날·자루는 손 뒤, 손가락 아래로 나온 자루 끝은 손 앞에 그림
        function drawArmHand(ctx, x, y, scale, rot, side, sprite, alpha, width, knife) {
            const U = width / 104 * ARM_SCALE;        // 그림 한 칸 = 화면 몇 px
            ctx.save();
            ctx.globalAlpha = alpha;
            ctx.imageSmoothingEnabled = false;
            ctx.translate(Math.round(x), Math.round(y + (knife ? width * KNIFE_DROP : 0)));   // 칼은 손 자리보다 화면 아래쪽에 그림
            ctx.rotate(rot);
            const s = 1 + (scale - 1) * 0.5;          // 뻗을 때 너무 커지지 않게 절반만 반영
            ctx.scale(U * s * side, U * s);
            if (knife) ctx.drawImage(KNIFE_SPRITE, -KNIFE_OX, -KNIFE_OY);   // 원점 = 주먹 중심 (손과 같이 움직임)
            if (!knife) ctx.drawImage(sprite, -ARM_ANCHOR_X, -ARM_ANCHOR_Y);   // 칼 든 손은 손·팔을 그리지 않고 칼만 보임
            if (knife) ctx.drawImage(KNIFE_FRONT, -KNIFE_OX, -KNIFE_OY);
            ctx.restore();
        }

        // ===== 시작 화면 =====
        let started = false;
        let aiMode = false;   // 1P 모드: 2P를 AI가 조작
        let aiSelf = p2, aiFoe = p1;   // AI가 조작하는 쪽 / 그 상대(사람). 모바일 연습 모드에서는 사람이 2P(아래 화면) 기준이라 AI가 1P를 맡음
        const aiKeys = () => aiSelf === p2 ? P2_KEYS : P1_KEYS;   // AI 쪽 키 (사람 입력은 무시)
        let practice = false; // 연습 모드: 1인 전용, 시간 · KO 없음, ESC 로 능력 · 설정을 실시간 변경
        // AI 난이도: 초당 행동 확률 (가드 / 공격 / 발차기), 이동 속도 배율
        // aim: 조준 허용 오차(rad, 클수록 허술) / react: 상대가 공격을 시작할 때 가드할 확률 / hitGuard: 맞고 기절이 풀린 뒤 가드할 확률 / delay: 반응 지연(초)
        const AI_LEVELS = {
            easy:   { guard: 0.12, attack: 0.9, kick: 0.1, speed: 0.5,  aim: 0.22, react: 0,    hitGuard: 0,   delay: [0.05, 0.1] },
            normal: { guard: 0.45, attack: 2.4, kick: 0.45, speed: 0.65, aim: 0.1,  react: 0.18, hitGuard: 0.3, delay: [0.05, 0.1] },
            hard:   { guard: 1,    attack: 7,   kick: 1.8, speed: 1.15, aim: 0.04, react: 0.5,  hitGuard: 0.7, delay: [0.03, 0.08] }
        };
        let aiLevel = AI_LEVELS.normal;
        const startScreen = document.getElementById('start-screen');
        function drawStartArt() {
            const c = document.getElementById('startArt');
            const g = c.getContext('2d');
            g.clearRect(0, 0, c.width, c.height);
            g.imageSmoothingEnabled = false;
            const sc = 8;
            const w = SPRITE_W * sc, h = SPRITE_H * sc;
            const w1 = h * p1.poseSprites.guard.width / p1.poseSprites.guard.height;   // 1P도 그림 비율에 맞춤
            g.drawImage(p1.poseSprites.guard, 12, c.height - h, w1, h);
            const w2 = h * p2.sprite.width / p2.sprite.height;   // 2P 그림은 가로세로 비율이 달라서 맞춤
            g.drawImage(p2.sprite, c.width - w2 - 12, c.height - h, w2, h);
            g.fillStyle = '#f1c40f';
            g.font = '32px "Press Start 2P", monospace';
            g.textAlign = 'center';
            g.fillText('VS', c.width / 2, c.height / 2 + 12);
        }
        drawStartArt();
        if (document.fonts && document.fonts.ready) document.fonts.ready.then(drawStartArt);
        const pauseScreen = document.getElementById('pause-screen');
        function togglePause() {
            if (!started) return;
            if (window.NET && NET.on) { NET.menu(); return; }   // 온라인 대전은 멈출 수 없음: 메뉴만 띄움
            paused = !paused;
            if (practice) { document.getElementById('practice-screen').classList.toggle('hidden', !paused); if (paused) renderPractice(); }
            else pauseScreen.classList.toggle('hidden', !paused);
            document.getElementById('practice-hint').classList.toggle('hidden', !practice || paused);
            if (paused) for (const k in keys) keys[k] = false;   // 누른 채 멈추면 키가 남지 않게
        }
        // 일시정지 메뉴 → 처음 화면: 경기 상태를 모두 초기화하고 시작 화면을 다시 띄움
        function goHome() {
            if (window.NET) NET.leave();
            paused = false;
            pauseScreen.classList.add('hidden');
            practice = false;
            document.getElementById('practice-screen').classList.add('hidden');
            document.getElementById('practice-hint').classList.add('hidden');
            started = false;
            p1.wins = 0; p2.wins = 0;
            matchOver = false;
            round = 1;
            closeCards();
            resetBuffs();
            resetGame();
            for (const k in keys) keys[k] = false;
            if (document.activeElement) document.activeElement.blur();
            startScreen.classList.remove('hidden');
        }
        document.getElementById('homeBtn').addEventListener('click', goHome);

        function startGame(solo) {   // 시작 버튼 · 난이도 선택 → 경기 설정 창을 먼저 띄움 (튜토리얼은 기본 설정으로 바로 시작)
            if (started) return;
            if (tutorial) { matchCfg = { ...DEF_CFG }; beginGame(solo, true); return; }
            openMatch(solo);
        }
        function buildPips() {   // 승리 칸을 '먼저 N승' 개수만큼 만듦
            for (const id of ['p1-pips', 'p2-pips']) document.getElementById(id).innerHTML = '<span class="pip"></span>'.repeat(matchCfg.wins);
        }
        function beginGame(solo, noPick) {
            if (started) return;
            started = true;
            buildPips();
            aiMode = !!solo;
            aiSelf = p2; aiFoe = p1;
            if (solo && matchCfg.side === 2) { aiSelf = p1; aiFoe = p2; }   // 1인 대전에서 2P를 고르면 AI가 1P를 맡음
            if (solo) aiLevel = AI_LEVELS[solo];   // solo: 'easy' | 'normal' | 'hard'
            startScreen.classList.add('hidden');
            closeLevel();
            p1.wins = 0; p2.wins = 0;
            matchOver = false;
            round = 1;
            setMap(matchCfg.map);
            resetBuffs();
            resetGame();
            if (!noPick) startIntroPick();   // 시작할 때 각자 능력 하나씩 선택
        }
        document.getElementById('startBtn').addEventListener('click', () => startGame(false));
        function startPractice() {
            if (started) return;
            matchCfg = { ...DEF_CFG };
            beginGame(false, true);   // 기본 상대는 2P(사람): AI 없이 2P 키를 그대로 받음 (시작 능력 선택 없음). ESC 패널에서 AI · 가만히로 바꿀 수 있음
            practice = true;
            if (window.yachaMmOn && window.yachaMmOn()) { aiSelf = p1; aiFoe = p2; }   // 모바일 모드 연습: 2P(아래 화면) 기준으로 내가 하고, 상대(연습 상대)가 1P
            practiceSettings.dummy = 'human';
            practiceSettings.map = matchCfg.map;
            practiceSettings.target = practiceMe() === p1 ? 1 : 2;
            document.getElementById('practice-hint').classList.remove('hidden');
            updateUI();
        }
        document.getElementById('practiceBtn').addEventListener('click', startPractice);
        const levelScreen = document.getElementById('level-screen');
        const levelOpen = () => !levelScreen.classList.contains('hidden');
        const openLevel = () => { levelScreen.classList.remove('hidden'); if (document.activeElement) document.activeElement.blur(); };
        const closeLevel = () => levelScreen.classList.add('hidden');
        document.getElementById('soloBtn').addEventListener('click', openLevel);
        document.getElementById('levelBack').addEventListener('click', closeLevel);
        document.querySelectorAll('.solo-btn').forEach(b => b.addEventListener('click', () => startGame(b.dataset.level)));

        // ===== 경기 설정 창: 시작하면 먼저 뜸 (먼저 N승 · 라운드 시간 · 체력/스테미나 배율) =====
        const matchScreen = document.getElementById('match-screen');
        const matchOpen = () => !matchScreen.classList.contains('hidden');
        const MATCH_OPTS = [
            { key: 'map', nm: '맵', vals: ['gym', 'colo', 'city', 'rand'], fmt: v => v === 'colo' ? '콜로세움' : v === 'city' ? '도시' : v === 'rand' ? '랜덤' : '건물', tab: true },   // 맵 그림 위에 탭으로 보임 (콜로세움: 밖으로 떨어지면 체력이 서서히 -SEA_DAMAGE)
            { key: 'wins', nm: '승리 라운드 수', note: '먼저 이 수만큼 이기면 승리', vals: [1, 2, 3, 4, 5], fmt: v => '먼저 ' + v + '승' },
            { key: 'time', nm: '라운드 시간', note: '1라운드는 +' + ROUND1_BONUS_TIME + '초', vals: [20, 30, 40, 50, 60, 90, 120], fmt: v => v + '초' },
            { key: 'hp', nm: '체력 배율', note: '기본 체력 10칸 기준', vals: [0.5, 0.75, 1, 1.5, 2, 3], fmt: v => '×' + v },
            { key: 'sta', nm: '스테미나 배율', note: '기본 스테미나 100 기준', vals: [0.5, 0.75, 1, 1.5, 2, 3], fmt: v => '×' + v },
            { key: 'side', nm: '내 쪽', note: '1인 대전: 내가 조작할 쪽 (상대는 AI)', vals: [1, 2], fmt: v => v + 'P', soloOnly: true }
        ];
        const matchOpts = () => MATCH_OPTS.filter(o => !o.soloOnly || matchSolo);   // 1인 대전일 때만 '내 쪽' 줄이 보임
        const matchUI = { ...DEF_CFG };   // 창에 보이는 값 (다음 경기에도 그대로 남음)
        let matchSel = 0, matchSolo = false;
        const matchPreview = document.getElementById('match-preview');
        const MAP_INFO = {   // 경기 설정 창에서 그림 위 이름 · 아래 설명 (체력은 체력바 칸 수로: 10 = 1칸)
            gym: ['건물', '창문이 있는 건물 안. 기둥 뒤로 숨을 수 있어요.'],
            colo: ['콜로세움', '바다 위에 뜬 원형 바닥. 밖으로 떨어지면 체력 ' + +(SEA_DAMAGE / 10).toFixed(1) + '칸이 ' + SEA_TIME + '초 동안 서서히 줄어요.'],
            city: ['도시', '건물 사이로 도로가 난 거리. 건물 벽 뒤로 숨을 수 있어요.'],
            rand: ['랜덤', '시작할 때 건물 / 콜로세움 / 도시 중 하나가 정해져요.']
        };
        function drawMatchPreview() {
            document.getElementById('match-map-name').textContent = MAP_INFO[matchUI.map][0];
            document.getElementById('match-map-desc').textContent = MAP_INFO[matchUI.map][1];   // 선택한 맵을 위에서 내려다본 모습: 건물 / 콜로세움(바다 위 원형 바닥)
            const c = matchPreview.getContext('2d'), W = matchPreview.width, H = matchPreview.height;
            if (matchUI.map === 'rand') {   // 랜덤: 시작할 때 건물 / 콜로세움 / 도시 중 하나가 정해짐
                c.clearRect(0, 0, W, H); c.fillStyle = '#2a2a33'; c.fillRect(0, 0, W, H);
                c.fillStyle = '#f1c40f'; c.font = 'bold 64px monospace'; c.textAlign = 'center'; c.textBaseline = 'middle'; c.fillText('?', W / 2, H / 2 + 4);
                c.textAlign = 'start'; c.textBaseline = 'alphabetic';
                return;
            }
            const colo = matchUI.map === 'colo', cty = matchUI.map === 'city', m = colo ? COLO_MAP : cty ? CITY_MAP : GYM_MAP;
            const cs = Math.min(W / m[0].length, H / m.length), ox = (W - cs * m[0].length) / 2, oy = (H - cs * m.length) / 2;
            const px = v => v / MAP_SIZE * cs;   // 월드 좌표 → 미리보기 좌표
            c.clearRect(0, 0, W, H);
            c.fillStyle = colo ? '#d6c293' : cty ? '#55555d' : '#cfc8b8'; c.fillRect(ox, oy, cs * m[0].length, cs * m.length);   // 콜로세움은 벽(돌), 건물은 바닥
            if (colo) {
                c.fillStyle = '#1c6aa8'; c.beginPath(); c.arc(ox + px(ARENA_C), oy + px(ARENA_C), px(WALL_R), 0, Math.PI * 2); c.fill();   // 둥근 벽 안쪽 바다
                c.fillStyle = '#c8b48c'; c.beginPath(); c.arc(ox + px(ARENA_C), oy + px(ARENA_C), px(ARENA_R), 0, Math.PI * 2); c.fill();
                c.strokeStyle = '#786446'; c.lineWidth = 2; c.stroke();
            }
            for (let r = 0; r < m.length; r++) for (let q = 0; q < m[0].length; q++) {
                if (m[r][q] === 1 && !colo) { c.fillStyle = cty ? ['#b5524a', '#8d9aa6', '#c9a66b', '#6f8f72', '#a8a0b8'][(q * 3 + r * 5) % 5] : '#4a3f2c'; c.fillRect(ox + q * cs, oy + r * cs, cs + 0.5, cs + 0.5); }
                else if (m[r][q] === 2) { c.fillStyle = '#555'; c.beginPath(); c.arc(ox + (q + 0.5) * cs, oy + (r + 0.5) * cs, Math.max(2, px(PILLAR_R)), 0, Math.PI * 2); c.fill(); }
            }
            if (colo) for (let i = 0; i < RING_N; i++) { const a = i * Math.PI * 2 / RING_N; c.fillStyle = '#555'; c.beginPath(); c.arc(ox + px(ARENA_C + Math.cos(a) * RING_R), oy + px(ARENA_C + Math.sin(a) * RING_R), Math.max(2, px(PILLAR_R)), 0, Math.PI * 2); c.fill(); }
            const sp = colo ? [[ARENA_C - 150, ARENA_C], [ARENA_C + 150, ARENA_C]] : cty ? CITY_START : [[150, 280], [600, 280]];   // 시작 위치 (1P 빨강 · 2P 파랑)
            sp.forEach(([x, y], i) => { c.fillStyle = i ? '#3498db' : '#e74c3c'; c.beginPath(); c.arc(ox + px(x), oy + px(y), 4, 0, Math.PI * 2); c.fill(); });
        }
        function renderMatch() {
            drawMatchPreview();
            const box = document.getElementById('match-rows');
            box.innerHTML = '';
            const tabs = document.getElementById('match-maps');
            tabs.innerHTML = '';
            matchOpts().forEach((o, i) => {
                if (o.tab) {   // 맵 선택지: 그림 바로 위에 나란히
                    tabs.classList.toggle('sel', i === matchSel);
                    for (const v of o.vals) {
                        const b = document.createElement('button');
                        b.className = 'mtab' + (v === matchUI[o.key] ? ' on' : ''); b.textContent = o.fmt(v);
                        b.addEventListener('click', () => { matchSel = i; matchUI[o.key] = v; renderMatch(); });
                        tabs.appendChild(b);
                    }
                    return;
                }
                const row = document.createElement('div');
                row.className = 'mrow' + (i === matchSel ? ' sel' : '');
                const nm = document.createElement('span'); nm.className = 'mnm'; nm.innerHTML = o.nm + '<small>' + o.note + '</small>';
                const lt = document.createElement('button'); lt.className = 'mbtn'; lt.textContent = '◀';
                const val = document.createElement('span'); val.className = 'mval'; val.textContent = o.fmt(matchUI[o.key]);
                const rt = document.createElement('button'); rt.className = 'mbtn'; rt.textContent = '▶';
                lt.addEventListener('click', () => { matchSel = i; stepMatch(i, -1); });
                rt.addEventListener('click', () => { matchSel = i; stepMatch(i, 1); });
                row.append(nm, lt, val, rt);
                box.appendChild(row);
            });
        }
        function stepMatch(i, d) {
            const o = matchOpts()[i], k = o.vals.indexOf(matchUI[o.key]);
            matchUI[o.key] = o.vals[Math.max(0, Math.min(o.vals.length - 1, k + d))];
            renderMatch();
        }
        function openMatch(solo) { matchSolo = solo; matchSel = 0; renderMatch(); matchScreen.classList.remove('hidden'); if (document.activeElement) document.activeElement.blur(); }
        const closeMatch = () => matchScreen.classList.add('hidden');
        function confirmMatch() { closeMatch(); matchCfg = { ...matchUI }; if (matchCfg.map === 'rand') matchCfg.map = ['gym', 'colo', 'city'][Math.floor(Math.random() * 3)]; beginGame(matchSolo); }
        document.getElementById('matchGo').addEventListener('click', confirmMatch);
        document.getElementById('matchBack').addEventListener('click', closeMatch);
        document.getElementById('matchReset').addEventListener('click', () => { Object.assign(matchUI, DEF_CFG); renderMatch(); });

        const keys = {};
        let gameOver = false;   // 현재 라운드가 끝난 상태
        let matchOver = false;  // 누군가 3라운드를 이겨 경기가 끝난 상태
        let round = 1;
        let paused = false;
        let roundTime = ROUND_TIME;   // 남은 라운드 시간
        let shoryuFxT = 0;            // 승룡권 불꽃 이펙트 남은 시간
        let burnT = 0;                // Burning Time 시작 후 경과 시간
        let timeUp = false;           // 시간 종료로 끝난 라운드
        let roundEndT = 0;      // 라운드 종료 후 경과 시간
        let roundIntroT = 0;    // 라운드 시작 후 경과 시간 (ROUND n 표시용)
        let winner = null;
        let gameTime = 0;

        // ===== 튜토리얼 (1P 기준): 설명하는 부분만 밝게, 나머지는 살짝 어둡게 =====
        // 튜토리얼 중에는 시간이 흐르지 않고 체력이 줄지 않으며, 키를 눌러 연습할 수 있음
        let tutorial = false;
        let tutStep = 0;
        const tutSpot = document.getElementById('tut-spot');
        const tutBox = document.getElementById('tut-box');
        const TUT_STEPS = [
            { sel: '#p1Canvas', title: '1P 화면', keys: [],
              text: '빨간색 1P의 시점이에요.<br>1인칭으로 상대(2P)를 보면서 싸워요.<br>이 튜토리얼은 1P 기준으로 설명해요.' },
            { sel: '#p1Canvas', title: '이동 · 회전', keys: [['W S', '앞 / 뒤로 이동'], ['A D', '왼쪽 / 오른쪽으로 회전']],
              text: '상대를 화면 정면에 두고 싸우세요. 정면에 있어야 공격이 맞아요.<br>직접 눌러서 상대에게 다가가 보세요!' },
            { sel: '#p1-hp-bg', title: '체력 (HP)', keys: [],
              text: '공격을 맞으면 줄어들고, 0이 되면 KO예요.<br>먼저 3라운드를 이기면 경기에서 승리해요.' },
            { sel: '#p1-st-bg', title: '스테미나', keys: [],
              text: '노란 바가 스테미나예요.<br>공격 · 가드 · 발차기를 쓸 때마다 줄고, 잠깐 쉬면 다시 차올라요.<br>모자라면 기술을 쓸 수 없어요.' },
            { sel: '#p1-skills .skill:nth-child(1)', title: '공격', avoid: '#p1Canvas', keys: [['Z', '주먹 공격 (스테미나 15)']],
              text: '왼손 오른손 번갈아 주먹을 날려요. 맞히면 바로 다음 주먹을 이어 칠 수 있어요.<br>아이콘의 어두운 막은 다시 쓸 수 있을 때까지 남은 시간이에요.<br>눌러 보세요!' },
            { sel: '#p1-skills .skill:nth-child(2)', title: '가드', avoid: '#p1Canvas', keys: [['X', '꾹 누르기 (스테미나 계속 소모)']],
              text: '누르고 있는 동안 공격을 막아요. 스테미나가 계속 닳아요.<br>가드 중인 상대를 때리면 때린 쪽이 0.5초 동안 기절해요.' },
            { sel: '#p1-skills .skill:nth-child(3)', title: '발차기', avoid: '#p1Canvas', keys: [['C', '발차기 (스테미나 30)']],
              text: '맞은 상대는 멀리 날아가고, 벽에 부딪히면 2초 동안 기절해요.<br>쿨타임이 4초로 길어요.' },
            { sel: '#ui-container > div:nth-child(2)', title: '라운드 시간', keys: [],
              text: '라운드는 40초예요 (1라운드만 50초). 시간이 끝나면 체력이 더 많은 쪽이 이겨요.<br>남은 시간이 10초 이하가 되면 Burning Time — 모든 피해가 2배!' },
            { sel: '#p1-pips', title: '라운드 승리와 카드', keys: [['V', '특수공격 (카드를 얻으면)']],
              text: '라운드를 이기면 칸이 채워져요.<br>라운드에서 진 사람은 능력 카드를 한 장 골라 강해져요.<br>도발 · 먹물 · 장풍 · 순간이동 · 분신 · 투명 · 힐 · 장애물 설치 카드는 특수공격 키로 사용해요. 점프는 발차기 키, 백열권은 공격 키를 꾹 눌러 사용해요. (장풍과 점프를 둘 다 모으면 승룡권으로 합쳐져요)<br>대쉬는 앞 방향키를 빠르게 두 번 눌러요.' },
            { sel: null, title: '준비 완료!', keys: [],
              text: '이제 자유롭게 연습해 보세요.<br>끝내면 처음 화면으로 돌아가요.' }
        ];

        // 강조할 칸 위치를 재서 밝은 구멍을 옮기고, 설명 상자는 대상을 가리지 않는 쪽에 놓음
        function layoutTut() {
            if (!tutorial) return;
            const step = TUT_STEPS[tutStep];
            const el = step.sel ? document.querySelector(step.sel) : null;
            const vw = window.innerWidth, vh = window.innerHeight, m = 12;
            const bw = tutBox.offsetWidth, bh = tutBox.offsetHeight;
            if (!el) {   // 강조 없이 가운데 안내 (전체를 어둡게)
                tutSpot.style.cssText = 'left:' + vw / 2 + 'px;top:' + vh / 2 + 'px;width:0;height:0;border-width:0;';
                tutBox.style.left = Math.round((vw - bw) / 2) + 'px';
                tutBox.style.top = Math.round((vh - bh) / 2) + 'px';
                return;
            }
            const rc = el.getBoundingClientRect();
            const pad = 6;
            const r = { left: rc.left - pad, top: rc.top - pad, right: rc.right + pad, bottom: rc.bottom + pad };
            tutSpot.style.cssText = 'left:' + r.left + 'px;top:' + r.top + 'px;width:' + (r.right - r.left - 6) + 'px;height:' + (r.bottom - r.top - 6) + 'px;';
            const clampX = x => Math.min(Math.max(m, x), vw - bw - m);
            const clampY = y => Math.min(Math.max(m, y), vh - bh - m);
            const cands = [
                [clampX(r.left), r.bottom + 14],       // 아래
                [clampX(r.left), r.top - bh - 14],     // 위
                [r.left - bw - 14, clampY(r.top)],     // 왼쪽
                [r.right + 14, clampY(r.top)]          // 오른쪽
            ];
            const av = step.avoid ? document.querySelector(step.avoid).getBoundingClientRect() : null;   // 설명 상자가 가리면 안 되는 영역 (내 화면)
            const fits = ([x, y]) => x >= m && y >= m && x + bw <= vw - m && y + bh <= vh - m;
            const clear = ([x, y]) => !av || x + bw <= av.left || x >= av.right || y + bh <= av.top || y >= av.bottom;
            let pos = cands.find(c => fits(c) && clear(c)) || cands.find(fits);
            if (!pos) pos = [Math.round((vw - bw) / 2), vh - bh - m];
            tutBox.style.left = Math.round(pos[0]) + 'px';
            tutBox.style.top = Math.round(pos[1]) + 'px';
        }

        function showTutStep() {
            const step = TUT_STEPS[tutStep];
            document.getElementById('tut-step').textContent = (tutStep + 1) + ' / ' + TUT_STEPS.length;
            document.getElementById('tut-title').textContent = step.title;
            document.getElementById('tut-text').innerHTML = step.text;
            document.getElementById('tut-keys').innerHTML = step.keys.map(([k, d]) =>
                '<div class="tk"><span class="kc">' + k + '</span><span>' + d + '</span></div>').join('');
            document.getElementById('tutPrev').style.visibility = tutStep === 0 ? 'hidden' : 'visible';
            document.getElementById('tutNext').textContent = tutStep === TUT_STEPS.length - 1 ? '처음 화면으로' : '다음';
            const el = step.sel ? document.querySelector(step.sel) : null;
            if (el) el.scrollIntoView({ block: 'center' });
            layoutTut();
        }
        function tutorialNext() {
            if (tutStep >= TUT_STEPS.length - 1) { endTutorial(false); return; }
            tutStep++;
            showTutStep();
        }
        function tutorialPrev() {
            if (tutStep > 0) { tutStep--; showTutStep(); }
        }
        function startTutorial() {
            if (started) return;
            tutorial = true;
            tutStep = 0;
            startGame();
            tutSpot.classList.remove('hidden');
            tutBox.classList.remove('hidden');
            if (document.activeElement) document.activeElement.blur();
            showTutStep();
        }
        function endTutorial(startAfter) {
            tutorial = false;
            tutSpot.classList.add('hidden');
            tutBox.classList.add('hidden');
            goHome();
            window.scrollTo(0, 0);
            if (startAfter) startGame();
        }
        document.getElementById('tutBtn').addEventListener('click', startTutorial);
        document.getElementById('tutNext').addEventListener('click', () => { tutorialNext(); if (document.activeElement) document.activeElement.blur(); });
        document.getElementById('tutPrev').addEventListener('click', () => { tutorialPrev(); if (document.activeElement) document.activeElement.blur(); });
        document.getElementById('tutExit').addEventListener('click', () => endTutorial(false));
        window.addEventListener('resize', layoutTut);
        window.addEventListener('scroll', layoutTut);

        const p1HpEl = document.getElementById('p1-hp');
        const p2HpEl = document.getElementById('p2-hp');
        const p1StEl = document.getElementById('p1-st');
        const p2StEl = document.getElementById('p2-st');

        // 캔버스/컨텍스트 캐싱
        const views = [
            makeView('p1Canvas', p1, p2),
            makeView('p2Canvas', p2, p1)
        ];
        function makeView(id, observer, enemy) {
            const canvas = document.getElementById(id);
            return {
                canvas,
                ctx: canvas.getContext('2d'),
                observer,
                enemy,
                wallDist: new Float32Array(canvas.width)
            };
        }

        // ===== 입력 (e.code 사용: 한글/CapsLock 상태에서도 동작) =====
        const P1_KEYS = { up: 'KeyW', down: 'KeyS', left: 'KeyA', right: 'KeyD', attack: 'KeyZ', guard: 'KeyX', kick: 'KeyC', jump: 'KeyV', ink: 'KeyV' };
        // 2P: 방향키 이동/회전, 공격 . (마침표), 가드 / (슬래시)
        const P2_KEYS = { up: 'ArrowUp', down: 'ArrowDown', left: 'ArrowLeft', right: 'ArrowRight', attack: 'Period', guard: 'Slash', kick: 'Quote', jump: 'Semicolon', ink: 'Semicolon' };
        const GAME_KEYS = new Set([
            ...Object.values(P1_KEYS), ...Object.values(P2_KEYS), 'Space', 'Enter', 'KeyR'
        ]);

        const PAUSE_KEYS = { Digit1: 'resumeBtn', Numpad1: 'resumeBtn', Digit2: 'cardsBtn', Numpad2: 'cardsBtn', Digit3: 'ctrlBtn', Numpad3: 'ctrlBtn',
                             Digit4: 'bgmBtn', Numpad4: 'bgmBtn', Digit5: 'homeBtn', Numpad5: 'homeBtn' };
        window.addEventListener('keydown', e => {
            if (GAME_KEYS.has(e.code)) e.preventDefault();   // 방향키 스크롤 방지
            if (e.repeat) return;
            if (!started) {
                if (matchOpen()) {   // 경기 설정 창
                    if (e.code === 'Enter' || e.code === 'NumpadEnter') confirmMatch();
                    else if (e.code === 'Escape') closeMatch();
                    else if (e.code === 'ArrowUp' || e.code === 'KeyW') { matchSel = (matchSel + matchOpts().length - 1) % matchOpts().length; renderMatch(); }
                    else if (e.code === 'ArrowDown' || e.code === 'KeyS') { matchSel = (matchSel + 1) % matchOpts().length; renderMatch(); }
                    else if (e.code === 'ArrowLeft' || e.code === 'KeyA') stepMatch(matchSel, -1);
                    else if (e.code === 'ArrowRight' || e.code === 'KeyD') stepMatch(matchSel, 1);
                    return;
                }
                if (levelOpen()) {   // 난이도 선택 창
                    if (e.code === 'Digit1' || e.code === 'Numpad1') startGame('easy');
                    else if (e.code === 'Digit2' || e.code === 'Numpad2') startGame('normal');
                    else if (e.code === 'Digit3' || e.code === 'Numpad3') startGame('hard');
                    else if (e.code === 'Escape') closeLevel();
                    return;
                }
                if (e.code === 'Enter' || e.code === 'NumpadEnter' || e.code === 'Space') startGame(false);
                else if (e.code === 'Digit1' || e.code === 'Numpad1') openLevel();
                else if (e.code === 'Digit2' || e.code === 'Numpad2') startPractice();
                else if (e.code === 'KeyT') startTutorial();
                return;
            }
            if (tutorial) {   // 튜토리얼: Enter 다음 / Backspace 이전 / ESC 종료 (나머지 키는 연습용으로 그대로 동작)
                if (e.code === 'Escape') { endTutorial(false); return; }
                if (e.code === 'Enter' || e.code === 'NumpadEnter') { tutorialNext(); return; }
                if (e.code === 'Backspace') { e.preventDefault(); tutorialPrev(); return; }
            }
            if (e.code === 'Escape') { togglePause(); return; }
            if (paused && practice) return;   // 연습 모드 패널은 마우스/터치로 조작 (ESC 로 닫기)
            if (paused && (e.code === 'Enter' || e.code === 'NumpadEnter')) { goHome(); return; }   // 일시정지 중 Enter: 처음 화면으로
            if (paused) {   // 일시정지 메뉴 단축키: 1~5 (카드 목록 · 조작키 설정창이 열려 있을 땐 무시)
                const btn = PAUSE_KEYS[e.code];
                const shown = id => !document.getElementById(id).classList.contains('vhide');
                if (btn && !shown('cardlist-screen') && !shown('ctrl-screen')) document.getElementById(btn).click();
                return;
            }
            if (practice && e.code === 'KeyR') { practiceReset(); return; }   // 연습 모드: R = 위치 · 체력 초기화
            if (aiMode && Object.values(aiKeys()).includes(e.code)) return;   // 1인용에서는 AI 쪽 키 무시
            keys[e.code] = true;
            for (const [pl, K] of [[p1, P1_KEYS], [p2, P2_KEYS]]) {   // 대쉬: 앞 방향키를 빠르게 두 번
                if (!(pl.canDash || pl.canSlash) || e.code !== K.up) continue;
                const now = performance.now();
                if (lastDashTap[e.code] && now - lastDashTap[e.code] < DASH_TAP_MS && tryDash(pl)) lastDashTap[e.code] = 0;
                else lastDashTap[e.code] = now;
            }

            if (gameOver && picking) {
                const K = pickPlayer === p1 ? P1_KEYS : P2_KEYS;
                if (/^(Digit|Numpad)\d$/.test(e.code)) {   // 카드 선택창에서 8015 를 치면 개발자 모드
                    devBuf = (devBuf + e.code.slice(-1)).slice(-4);
                    if (devBuf === '8015' && !devMode) { devMode = true; buildCards(); }
                    return;
                }
                if (e.code === K.up || e.code === K.down) { devKeys = (devKeys + (e.code === K.up ? 'U' : 'D')).slice(-5); return; }   // 앞 뒤 앞 앞 뒤 (모바일 · 키보드 공통)
                if (e.code === K.attack && devKeys === 'UDUUD' && !devMode) { devMode = true; devKeys = ''; buildCards(); return; }   // + 공격 = 개발자 모드
                if (e.code === K.left) { pickIdx = (pickIdx + pickCards.length - 1) % pickCards.length; renderCards(); }
                else if (e.code === K.right) { pickIdx = (pickIdx + 1) % pickCards.length; renderCards(); }
                else if (e.code === K.attack || e.code === 'Enter') confirmCard();
                return;
            }
            if (gameOver) {
                if (matchOver && (e.code === 'Enter' || e.code === 'KeyR')) nextRound();   // 라운드는 자동 진행, 경기 종료 때만 키로 새 경기
                return;
            }
            for (const [pl, K] of [[p1, P1_KEYS], [p2, P2_KEYS]]) {   // 쿨타임이 안 찼는데 누르면 삐익 (AI의 2P는 제외)
                if (aiMode && pl === aiSelf) continue;
                cdBeep(pl, e.code === K.attack ? 'attack' : e.code === K.guard ? 'guard' : e.code === K.kick ? 'kick' : e.code === K.ink ? 'special' : '');
            }
            if (e.code === P1_KEYS.attack) pressAction(p1, 'punch', e.code);
            if (e.code === P2_KEYS.attack) pressAction(p2, 'punch', e.code);
            if (e.code === P1_KEYS.guard) startGuard(p1, e.code);
            if (e.code === P2_KEYS.guard) startGuard(p2, e.code);
            for (const [pl, K] of [[p1, P1_KEYS], [p2, P2_KEYS]]) {   // 도발·먹물·장풍·순간이동 등은 모두 같은 특수공격 키 (하나만 가질 수 있음. 점프는 발차기 키, 백열권은 공격 키라 함께 가질 수 있음)
                if (e.code !== K.ink) continue;
                if (tryShoryu(pl)) continue;   // 한 바퀴 돌았으면 승룡권이 먼저 나감
                startTaunt(pl); startInk(pl); startKi(pl); startBlink(pl); startClone(pl); startInvis(pl); startHeal(pl); startObst(pl);
            }
            if (e.code === P1_KEYS.kick) pressAction(p1, 'kick', e.code);
            if (e.code === P2_KEYS.kick) pressAction(p2, 'kick', e.code);
        });
        // 기술 키를 눌렀는데 안 나가는 경우(쿨타임이 남았거나, 다른 기술을 쓰는 중)면 경고음
        function cdBeep(p, act) {
            if (!act) return;
            const busy = p.attacking || p.kicking || p.guard > 0 || !!p.charging || p.kiOn || p.flurryOn;   // 다른 기술을 쓰는 중
            let no = false;
            if (act === 'attack') no = busy || p.cooldown > 0 || (p.gun && (p.gunCd > 0 || p.gunReload > 0));
            else if (act === 'kick') no = busy || p.cooldown > 0 || p.kickCd > 0;
            else if (act === 'guard') no = p.attacking || p.kicking || p.guard > 0 || p.guardCd > 0;
            else if (p.canShoryu && p.shoryuReady > 0 && !busy && p.z <= 0) no = false;   // 승룡권 발동 가능
            else if (p.canTaunt) no = p.tauntCd > 0;
            else if (p.canInk) no = busy || p.cooldown > 0 || p.inkCd > 0;
            else if (p.canKi) no = busy || p.cooldown > 0 || p.kiCd > 0;
            else if (p.canBlink) no = busy || p.z > 0 || p.cooldown > 0 || p.blinkCd > 0 || p.stamina < BLINK_COST_MIN;
            else if (p.canClone) no = busy || p.z > 0 || p.cooldown > 0 || p.cloneCd > 0 || p.stamina < CLONE_COST;
            else if (p.canInvis) no = busy || p.invisCd > 0 || p.stamina < INVIS_COST;
            else if (p.canHeal) no = busy || p.healCd > 0 || p.hp >= p.maxHp || p.stamina < HEAL_COST;
            else if (p.canObst) no = busy || p.z > 0 || p.cooldown > 0 || p.obstCd > 0 || p.stamina < OBST_COST;
            if (no) {   // 꾹 누르거나 연타해도 소리가 겹치지 않게 간격을 둠
                const now = performance.now();
                if (now - (p.denyAt || 0) < 800) return;
                p.denyAt = now;
                bgm.sfx('deny');
            }
        }
        const lastDashTap = {};   // 대쉬 더블탭 판정
        window.addEventListener('keyup', e => {
            keys[e.code] = false;
            releaseAction(p1, e.code); releaseAction(p2, e.code);
            releaseGuard(p1, e.code); releaseGuard(p2, e.code);
            if (e.code === P1_KEYS.ink) { releaseKi(p1); releaseBlink(p1); releaseHeal(p1); }
            if (e.code === P2_KEYS.ink) { releaseKi(p2); releaseBlink(p2); releaseHeal(p2); }
        });
        // 창 포커스를 잃으면 눌린 키 초기화 (키가 눌린 채로 남는 문제 방지)
        window.addEventListener('blur', () => { if (p1.guardHold) endGuard(p1); if (p2.guardHold) endGuard(p2); p1.charging = ''; p2.charging = ''; p1.hold = ''; p2.hold = ''; p1.kiOn = false; p2.kiOn = false; p1.blinkOn = false; p2.blinkOn = false; p1.healOn = false; p2.healOn = false; for (const k in keys) keys[k] = false; });

        window.addEventListener('pointerup', e => { for (const q of [p1, p2]) if (q.blinkPtr === e.pointerId) { q.blinkPtr = null; releaseBlink(q); }
            for (const q of [p1, p2]) if (q.healPtr === e.pointerId) { q.healPtr = null; releaseHeal(q); }
            for (const q of [p1, p2]) if (q.kiPtr === e.pointerId) { q.kiPtr = null; releaseKi(q); }   // 다른 손가락(방향키 등)을 뗄 때는 장풍 충전이 풀리지 않게
            releaseAction(p1, 'ptr'); releaseAction(p2, 'ptr'); releaseGuard(p1, 'ptr'); releaseGuard(p2, 'ptr'); });
        window.addEventListener('pointercancel', e => { for (const q of [p1, p2]) if (q.blinkPtr === e.pointerId) { q.blinkPtr = null; q.blinkOn = false; q.blinkD = 0; }
            for (const q of [p1, p2]) if (q.healPtr === e.pointerId) { q.healPtr = null; releaseHeal(q); }
            for (const q of [p1, p2]) if (q.kiPtr === e.pointerId) { q.kiPtr = null; q.kiOn = false; q.kiT = 0; }
            p1.charging = ''; p2.charging = ''; p1.hold = ''; p2.hold = ''; releaseGuard(p1, 'ptr'); releaseGuard(p2, 'ptr'); });

        // ===== 충돌 =====
        function isWallAt(x, y) {
            if (arena && Math.hypot(x - ARENA_C, y - ARENA_C) > WALL_R) return true;   // 콜로세움: 둥근 바깥 벽
            const mx = Math.floor(x / MAP_SIZE);
            const my = Math.floor(y / MAP_SIZE);
            if (mx < 0 || my < 0 || mx >= MAP_W || my >= MAP_H) return true;
            return map[my][mx] === 1;   // 기둥(2)은 칸 전체가 아니라 가는 원기둥이라 따로 검사
        }
        let PILLARS = [];
        function setMap(id) {   // 경기 설정의 '맵' 적용: 'gym' 건물 / 'colo' 콜로세움 / 'city' 도시 (기둥 · 시작 위치도 맵에 맞춤)
            arena = id === 'colo';
            city = id === 'city';
            map = arena ? COLO_MAP : city ? CITY_MAP : GYM_MAP;
            MAP_H = map.length; MAP_W = map[0].length;
            RING.length = 0;
            if (arena) for (let i = 0; i < RING_N; i++) { const a = i * Math.PI * 2 / RING_N; RING.push([ARENA_C + Math.cos(a) * RING_R, ARENA_C + Math.sin(a) * RING_R]); }
            PILLARS = RING.slice();
            for (let r = 0; r < MAP_H; r++) for (let c = 0; c < MAP_W; c++) if (map[r][c] === 2) PILLARS.push([(c + 0.5) * MAP_SIZE, (r + 0.5) * MAP_SIZE]);
            p1.startX = arena ? ARENA_C - 150 : city ? CITY_START[0][0] : 150; p1.startY = arena ? ARENA_C : city ? CITY_START[0][1] : 280;
            p2.startX = arena ? ARENA_C + 150 : city ? CITY_START[1][0] : 600; p2.startY = p1.startY;
        }
        setMap('gym');
        function hitsPillar(x, y) {
            const lim = PILLAR_R + PLAYER_RADIUS;
            for (const [cx, cy] of PILLARS) if (Math.hypot(x - cx, y - cy) < lim) return true;
            return false;
        }
        function boxUnder(t) {   // t 가 올라서 있는 박스 (없으면 null)
            if (!(t.z >= OBST_H - 0.5)) return null;
            for (const b of obstacles) if (!(b.vx || b.vy) && Math.abs(t.x - b.x) < OBST_HALF && Math.abs(t.y - b.y) < OBST_HALF) return b;   // 밀리는 중인 박스 위에는 못 섬
            return null;
        }
        function hitsBox(x, y, z) {   // 설치한 박스: 발이 박스 높이보다 낮을 때만 막음 (점프로 넘거나 올라설 수 있음)
            if (z >= OBST_H - 0.5) return false;
            const lim = OBST_HALF + PLAYER_RADIUS;
            for (const b of obstacles) if (Math.abs(x - b.x) < lim && Math.abs(y - b.y) < lim) return true;
            return false;
        }
        function boxFloor(x, y) {   // 이 자리 아래에 박스가 있으면 박스 윗면 높이, 없으면 0
            for (const b of obstacles) if (!(b.vx || b.vy) && Math.abs(x - b.x) < OBST_HALF + PLAYER_RADIUS * 0.5 && Math.abs(y - b.y) < OBST_HALF + PLAYER_RADIUS * 0.5) return OBST_H;
            return 0;
        }
        function flatK(p) {   // 납작한 정도: 0 (서 있음) ~ 1 (완전히 납작). 눌릴 때 FLAT_IN 초 · 펴질 때 FLAT_OUT 초 동안 부드럽게 변함
            if (!(p.flat > 0)) return 0;
            return Math.max(0, Math.min(1, (p.flatMax - p.flat) / FLAT_IN, p.flat / FLAT_OUT));
        }
        function pushOutOfBoxes(p) {   // 박스 가장자리에서 내려오다 박스 몸통 판정 안에 걸리면 가장 가까운 바깥으로 밀어냄 (벽 · 기둥으로는 안 밀림)
            const lim = OBST_HALF + PLAYER_RADIUS;
            for (const b of obstacles) {
                if ((b.vx || b.vy) || !(Math.abs(p.x - b.x) < lim && Math.abs(p.y - b.y) < lim)) continue;   // 밀리는 중에는 건드리지 않음 (멈춘 뒤에 밀어냄)
                const c = [[b.x + lim, p.y], [b.x - lim, p.y], [p.x, b.y + lim], [p.x, b.y - lim]]
                    .filter(([x, y]) => !blockedAt(x, y, OBST_H))   // z 를 박스 높이로 줘서 벽 · 기둥만 검사
                    .sort((u, v) => Math.hypot(u[0] - p.x, u[1] - p.y) - Math.hypot(v[0] - p.x, v[1] - p.y));
                if (c.length) { p.x = c[0][0]; p.y = c[0][1]; }
            }
        }
        function blockedAt(x, y, z = 0) {
            const r = PLAYER_RADIUS;
            return isWallAt(x - r, y - r) || isWallAt(x + r, y - r) ||
                   isWallAt(x - r, y + r) || isWallAt(x + r, y + r) || hitsPillar(x, y) || hitsBox(x, y, z);
        }
        // x, y를 따로 검사 → 벽을 따라 미끄러짐
        function tryMove(p, nx, ny) {
            if (!blockedAt(nx, p.y, p.z)) p.x = nx;
            if (!blockedAt(p.x, ny, p.z)) p.y = ny;
        }
        function separatePlayers() {
            const dx = p2.x - p1.x;
            const dy = p2.y - p1.y;
            const dist = Math.hypot(dx, dy);
            if (dist >= MIN_PLAYER_DIST) return;
            if ((p1.canSlash && p1.dashT > 0) || (p2.canSlash && p2.dashT > 0)) return;   // 돌진베기 중에는 서로 통과
            if ((p1.jumping && p1.z - p2.z > STOMP_H) || (p2.jumping && p2.z - p1.z > STOMP_H)) return;   // 점프로 상대 머리 위에 떠 있으면 겹쳐 지나감
            let nx, ny;
            if (dist < 0.001) { nx = 1; ny = 0; } else { nx = dx / dist; ny = dy / dist; }
            const push = (MIN_PLAYER_DIST - dist) / 2;
            tryMove(p1, p1.x - nx * push, p1.y - ny * push);
            tryMove(p2, p2.x + nx * push, p2.y + ny * push);
        }

        // ===== 레이캐스팅 (DDA) =====
        let rayType = 1;   // 레이가 맞은 칸 종류 (1 벽, 2 박스)
        let rayDist = 0;   // 레이 길이(px)
        let raySide = 0;   // 0: 동서 면, 1: 남북 면
        let rayU = 0;      // 벽 면 위 가로 위치(0~1)
        let rayCellX = 0, rayCellY = 0;   // 레이가 맞은 벽 칸 (건물 맵의 창문 위치 판정용)
        function boxHit(ox, oy, dx, dy) {   // 레이와 가장 가까운 박스가 만나는 { t, side, u } (박스 안에서 쏘면 무시)
            let best = null;
            for (const b of obstacles) {
                const x0 = b.x - OBST_HALF, x1 = b.x + OBST_HALF, y0 = b.y - OBST_HALF, y1 = b.y + OBST_HALF;
                if (b === rayExcludeBox || (ox > x0 && ox < x1 && oy > y0 && oy < y1)) continue;
                let tmin = -Infinity, tmax = Infinity, side = 0;
                if (Math.abs(dx) < 1e-9) { if (ox < x0 || ox > x1) continue; }
                else { let a = (x0 - ox) / dx, c = (x1 - ox) / dx; if (a > c) { const s = a; a = c; c = s; } if (a > tmin) { tmin = a; side = 0; } if (c < tmax) tmax = c; }
                if (Math.abs(dy) < 1e-9) { if (oy < y0 || oy > y1) continue; }
                else { let a = (y0 - oy) / dy, c = (y1 - oy) / dy; if (a > c) { const s = a; a = c; c = s; } if (a > tmin) { tmin = a; side = 1; } if (c < tmax) tmax = c; }
                if (tmax < tmin || tmin <= 0) continue;
                if (!best || tmin < best.t) best = { t: tmin, t2: tmax, side, u: side === 0 ? (oy + dy * tmin - y0) / (OBST_HALF * 2) : (ox + dx * tmin - x0) / (OBST_HALF * 2) };
            }
            return best;
        }
        function castRay(ox, oy, angle) {   // 벽 · 기둥 + 설치한 박스 (화면을 그릴 때는 rayIgnoreBoxes 로 박스를 빼고 따로 그림)
            castRayWorld(ox, oy, angle);
            if (rayIgnoreBoxes || !obstacles.length) return;
            const bh = boxHit(ox, oy, Math.cos(angle), Math.sin(angle));
            if (bh && bh.t < rayDist) { rayDist = bh.t; raySide = bh.side; rayType = 3; rayU = bh.u; }
        }
        function castRayWorld(ox, oy, angle) {
            const dirX = Math.cos(angle);
            const dirY = Math.sin(angle);
            const px = ox / MAP_SIZE;
            const py = oy / MAP_SIZE;
            let mapX = Math.floor(px);
            let mapY = Math.floor(py);

            const deltaX = dirX === 0 ? 1e30 : Math.abs(1 / dirX);
            const deltaY = dirY === 0 ? 1e30 : Math.abs(1 / dirY);
            let stepX, stepY, sideX, sideY;

            if (dirX < 0) { stepX = -1; sideX = (px - mapX) * deltaX; }
            else          { stepX = 1;  sideX = (mapX + 1 - px) * deltaX; }
            if (dirY < 0) { stepY = -1; sideY = (py - mapY) * deltaY; }
            else          { stepY = 1;  sideY = (mapY + 1 - py) * deltaY; }

            // 기둥: 칸 한가운데의 가는 원기둥과 레이가 만나는지 검사, 안 만나면 그냥 통과
            const hitPillar = (cellX, cellY) => {
                const cx = (cellX + 0.5) * MAP_SIZE, cy = (cellY + 0.5) * MAP_SIZE;
                const fx = ox - cx, fy = oy - cy;
                const b = fx * dirX + fy * dirY;
                const disc = b * b - (fx * fx + fy * fy - PILLAR_R * PILLAR_R);
                if (disc < 0) return false;
                const t = -b - Math.sqrt(disc);
                if (t <= 0) return false;
                rayDist = t;
                raySide = 0;
                rayType = 2;
                const hx = fx + dirX * t, hy = fy + dirY * t;
                rayU = ((hx * -dirY + hy * dirX) / PILLAR_R + 1) / 2;   // 0~1: 보이는 폭 위의 위치
                return true;
            };

            // 시작 칸이 기둥 칸이면(기둥 바로 옆에 붙은 경우) 루프가 이 칸을 건너뛰므로 먼저 검사
            if (map[mapY] && map[mapY][mapX] === 2 && hitPillar(mapX, mapY)) return;

            let side = 0;
            for (let i = 0; i < 64; i++) {
                if (sideX < sideY) { sideX += deltaX; mapX += stepX; side = 0; }
                else               { sideY += deltaY; mapY += stepY; side = 1; }

                if (mapX < 0 || mapY < 0 || mapX >= MAP_W || mapY >= MAP_H) break;
                const cell = map[mapY][mapX];
                if (cell === 1) break;
                if (cell === 2 && hitPillar(mapX, mapY)) return;
            }
            rayType = (mapX < 0 || mapY < 0 || mapX >= MAP_W || mapY >= MAP_H) ? 1 : map[mapY][mapX];
            rayCellX = mapX; rayCellY = mapY;
            const d = side === 0 ? sideX - deltaX : sideY - deltaY;
            rayDist = d * MAP_SIZE;
            raySide = side;
            const wx = side === 0 ? py + d * dirY : px + d * dirX;
            rayU = wx - Math.floor(wx);
            if (arena) {   // 콜로세움: 네모 방 벽 앞에 있는 둥근 벽과 만나는 지점으로 바꿈
                const fx = ox - ARENA_C, fy = oy - ARENA_C;
                const b = fx * dirX + fy * dirY, cc = fx * fx + fy * fy - WALL_R * WALL_R;
                const disc = b * b - cc;
                if (cc < 0 && disc >= 0) {
                    const t = -b + Math.sqrt(disc);
                    rayDist = t; raySide = 0; rayType = 1;
                    rayU = (Math.atan2(fy + dirY * t, fx + dirX * t) + Math.PI) * WALL_R / MAP_SIZE;   // 둘레를 따라 늘어나는 가로 위치 (아치 간격은 기존과 비슷)
                }
            }
            if (arena) for (const [cx, cy] of RING) {   // 콜로세움 기둥(칸 가운데가 아닌 원 둘레에 서 있음): 벽보다 가까우면 기둥이 보임
                const fx = ox - cx, fy = oy - cy;
                const b = fx * dirX + fy * dirY;
                const disc = b * b - (fx * fx + fy * fy - PILLAR_R * PILLAR_R);
                if (disc < 0) continue;
                const t = -b - Math.sqrt(disc);
                if (t <= 0 || t >= rayDist) continue;
                rayDist = t; raySide = 0; rayType = 2;
                rayU = (((fx + dirX * t) * -dirY + (fy + dirY * t) * dirX) / PILLAR_R + 1) / 2;
            }
        }

        // ===== 전투 =====
        // ===== 대쉬: 앞 방향키 두 번 → 앞으로 매우 빠르게 돌진. 돌진 중 무적 · 상대와 부딪히면 피해 =====
        function tryDash(p) {
            if (!(p.canDash || p.canSlash) || gameOver || p.dashT > 0 || p.dashCd > 0 || p.attacking || p.kicking || p.kiOn || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.shoryuOn || p.z > 0 || p.cooldown > 0) return false;
            const cost = p.canSlash ? SLASH_COST : DASH_COST;
            if (p.stamina < cost) { p.lackT = LACK_TIME; return true; }
            p.stamina -= cost; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.dashT = DASH_TIME; p.dashCd = p.canSlash ? SLASH_CD : DASH_CD; p.dashAngle = p.angle; p.dashHit = false;
            p.cooldown = DASH_TIME;   // 돌진 중에는 다른 공격 불가
            if (p.canSlash) { p.attacking = true; p.attackT = 0; p.hitDone = true; p.punchLanded = false; p.punchHand = 0; bgm.sfx('knife'); }   // 돌진베기: 칼 휘두르는 모션만 재사용 (타격은 부딪힐 때 dashCollide 가 처리)
            else bgm.sfx('jump');
            return true;
        }
        function dashCollide(a, d) {   // 부딪힘: 피해 + 이펙트, 돌진은 거기서 끝
            a.dashHit = true; if (!a.canSlash) a.dashT = 0;   // 돌진베기는 상대를 통과해 끝까지 돌진
            if (d.guard > 0) { d.blockFlash = 0.2; bgm.sfx('guard'); return; }   // 가드로 막힘: 피해 없음 (돌진한 쪽은 기절하지 않음)
            if (!tutorial) d.hp = Math.max(0, d.hp - (a.canSlash ? SLASH_DAMAGE : DASH_DAMAGE) * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1));
            a.combo = (a.combo > 0 && a.comboT < COMBO_WINDOW) ? a.combo + 1 : 1;
            a.comboT = 0;
            d.combo = 0;
            d.hitFlash = 0.3; d.shake = SHAKE_DURATION; d.hitFx = HIT_FX_TIME;
            if (a.canSlash && !d.giant) { d.stun = SLASH_STUN; d.dizzy = SLASH_STUN; }   // 돌진베기: 1.5초 기절 (거대화: 기절 면역)
            bgm.sfx('hit');
            d.fx = burstFx();
            updateUI();
            if (d.hp <= 0) {
                gameOver = true;
                winner = a;
                a.wins++;
                matchOver = a.wins >= matchCfg.wins;
                updateUI();
            }
        }
        function updateDash(p, d, dt) {
            if (p.dashCd > 0) p.dashCd = Math.max(0, p.dashCd - dt);
            if (p.dashT <= 0) return;
            if (gameOver || p.stun > 0) { p.dashT = 0; return; }
            p.dashT = Math.max(0, p.dashT - dt);
            const total = DASH_SPEED * dt, steps = Math.max(1, Math.ceil(total / 8)), step = total / steps;   // 잘게 나눠 움직여 상대 · 벽을 뚫지 않게
            for (let i = 0; i < steps; i++) {
                const ox = p.x, oy = p.y;
                tryMove(p, p.x + Math.cos(p.dashAngle) * step, p.y + Math.sin(p.dashAngle) * step);
                if (!p.dashHit && d.dashT <= 0 && d.z <= AIR_HIT_MAX_Z && Math.hypot(d.x - p.x, d.y - p.y) <= DASH_HIT_DIST) { dashCollide(p, d); break; }
                if (p.x === ox && p.y === oy) { p.dashT = 0; break; }   // 벽에 막히면 멈춤
            }
        }

        function startTaunt(p) {
            if (!p.canTaunt || gameOver || p.tauntCd > 0 || p.stun > 0 || p.dizzy > 0) return;
            p.tauntT = TAUNT_TIME;
            p.tauntCd = TAUNT_CD;
            bgm.sfx('taunt');
        }

        function tryJump(p, mul = 1) {   // 점프: 바닥에 있을 때만, 공중에서는 이동 · 공격 가능 (p.jumping). mul: 점프 속도 배율 (발차기 키를 누른 시간에 따라 0.55~1)
            if (p.fallT > 0 && p.canJump && !gameOver && p.stamina >= JUMP_COST) {   // 콜로세움: 바다에 빠진 채 점프하면 가장자리 바닥 위로 뛰어올라 나옴
                const a = Math.atan2(p.y - ARENA_C, p.x - ARENA_C);
                p.x = ARENA_C + Math.cos(a) * (ARENA_R - 40); p.y = ARENA_C + Math.sin(a) * (ARENA_R - 40);
                p.fallT = 0; p.stun = 0;
                p.stamina -= JUMP_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
                p.vz = JUMP_VEL * mul; p.z = 0.01; p.jumping = true; p.jumpCd = JUMP_CD;
                bgm.sfx('jump');
                return;
            }
            if (!p.canJump || gameOver || p.z > 0 || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.attacking || p.kicking || p.dashT > 0 || p.shoryuOn || p.kiOn || p.charging || p.jumpCd > 0) return;
            if (p.stamina < JUMP_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= JUMP_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.vz = JUMP_VEL * mul; p.z = 0.01; p.jumping = true; p.jumpCd = JUMP_CD;
            bgm.sfx('jump');
        }

        // 가드: 사람은 키를 누르고 있는 동안 유지(스테미나 계속 소모), AI는 짧게 한 번(src 없음)
        function startGuard(p, src) {
            if (gameOver || p.attacking || p.kicking || p.stun > 0 || p.guard > 0 || p.guardCd > 0 || p.noGuard || p.shoryuOn || p.flurryOn) return;   // 승룡권에 맞아 뜬 동안은 가드 불가
            if (src) {
                if (p.stamina < GUARD_START) { p.lackT = LACK_TIME; return; }
                p.guardHold = src; p.guard = GUARD_HOLD_TICK;
            } else {
                if (p.stamina < GUARD_COST) { p.lackT = LACK_TIME; return; }
                p.stamina -= GUARD_COST;
                p.guard = GUARD_TIME;
            }
            p.staminaDelay = STAMINA_REGEN_DELAY;
            p.charging = ''; p.chargeT = 0; p.hold = ''; p.holdT = 0;   // 가드하면 충전 · 점프 · 백열권 누르기 취소
            bgm.sfx('guard');
        }
        function endGuard(p) { p.guardHold = ''; p.guard = 0; p.guardCd = GUARD_COOLDOWN * p.guardCdMul; }
        function releaseGuard(p, src) { if (p.guardHold && p.guardHold === src) endGuard(p); }

        // 공격/발차기 입력. 힘조절 카드가 있으면 누르는 동안 충전하고 뗄 때 발동 (src: 누른 키 코드 또는 'ptr')
        function pressAction(p, kind, src) {
            if (!p.canCharge && !p.hold && !gameOver && !p.attacking && !p.kicking && p.cooldown <= 0 && p.stun <= 0 && p.dizzy <= 0 && p.guard <= 0 && p.z <= 0 && !p.shoryuOn && !p.kiOn &&
                ((kind === 'kick' && p.canJump && p.jumpCd <= 0 && p.stamina >= JUMP_COST) || (kind === 'punch' && p.canFlurry && !p.flurryOn && p.flurryCd <= 0 && p.stamina >= FLURRY_COST))) {
                p.hold = kind; p.holdT = 0; p.holdSrc = src; return;   // 점프 · 백열권: 키를 꾹 눌러서 발동 (그전에 떼면 평소 발차기 · 주먹)
            }
            if (!p.canCharge || (kind === 'punch' && p.gun)) { kind === 'kick' ? startKick(p) : startAttack(p); return; }
            if (p.charging || gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0) return;
            if (p.z > 0 && !p.jumping) return;
            if (kind === 'kick' && p.kickCd > 0) return;
            p.charging = kind; p.chargeT = 0; p.chargeSrc = src;
        }
        function endHold(p) {   // 점프 · 백열권 키를 뗌: 점프는 누른 만큼 높이, 백열권이 나가기 전에 뗐으면 평소 주먹, 점프를 톡 눌렀으면 평소 발차기
            const kind = p.hold, t = p.holdT;
            p.hold = ''; p.holdT = 0; p.holdSrc = '';
            if (paused) return;
            if (kind === 'punch') startAttack(p);
            else if (t < JUMP_HOLD_MIN) startKick(p);
            else tryJump(p, JUMP_MIN_MUL + (1 - JUMP_MIN_MUL) * Math.min(1, (t - JUMP_HOLD_MIN) / (JUMP_HOLD_MAX - JUMP_HOLD_MIN)));
        }
        function releaseAction(p, src) {
            if (p.hold && p.holdSrc === src) { endHold(p); return; }
            if (!p.charging || p.chargeSrc !== src) return;
            if (paused) { p.charging = ''; p.chargeT = 0; return; }   // 일시정지 중에 뗀 건 취소
            const kind = p.charging;
            p.dmgMul = CHARGE_MIN + (CHARGE_MAXMUL - CHARGE_MIN) * Math.min(1, p.chargeT / CHARGE_TIME);
            p.charging = ''; p.chargeT = 0;
            kind === 'kick' ? startKick(p) : startAttack(p);
            p.freeHit = false;
            if (!p.attacking && !p.kicking) p.dmgMul = 1;   // 스테미나 부족 등으로 안 나갔으면 배율 되돌림
        }

        function startAttack(p) {
            if (p.gun) { startGun(p); return; }   // 총 카드: 주먹 대신 총
            if (gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0) return;
            if (p.z > 0 && !p.jumping) return;   // 맞아서 뜬 상태에서는 가드만 가능
            const cost = p.freeHit ? 0 : ATTACK_COST + (p.knife ? KNIFE_COST : 0);
            if (p.stamina < cost) { p.lackT = LACK_TIME; return; }
            p.stamina -= cost;
            if (cost) p.staminaDelay = STAMINA_REGEN_DELAY;
            p.attacking = true;
            p.attackT = 0;
            p.hitDone = false;
            p.punchLanded = false;
            bgm.sfx(p.knife ? 'knife' : 'punch');
            p.punchHand = p.knife ? 0 : 1 - p.punchHand;   // 단검은 오른손 하나에 들려 있어 항상 그 손으로 공격
        }

        function startKick(p) {
            if (gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0) return;
            if (p.z > 0 && !p.jumping) return;   // 맞아서 뜬 상태에서는 가드만 가능
            const kcost = p.freeHit ? 0 : KICK_COST;
            if (p.kickCd > 0) return;
            if (p.stamina < kcost) { p.lackT = LACK_TIME; return; }
            p.stamina -= kcost;
            p.kickCd = KICK_RECHARGE * p.kickCdMul;
            if (kcost) p.staminaDelay = STAMINA_REGEN_DELAY;
            p.kicking = true;
            p.kickT = 0;
            p.kickHit = false;
            bgm.sfx('kick');
        }

        // ===== 분신 · 투명 · 힐 · 장애물 설치 (특수): 모두 특수공격 키 하나를 씀 =====
        function clearTemp() {   // 라운드가 바뀌면 분신 · 장애물 제거
            obstacles.length = 0;
            clones.length = 0;
            car = null; carT = 0;   // 자동차도 라운드마다 처음부터
        }
        function setObstacles(list) {   // 멀티플레이 손님: 방장이 보낸 장애물 목록으로 통째로 바꿈
            obstacles.length = 0;
            for (const [x, y, hp] of list) obstacles.push({ x, y, t: 0, hp });
        }
        function mkClone(owner, x, y, angle) {   // 분신: 주인을 프로토타입으로 삼아 스프라이트 · 무기 · 사정거리를 그대로 씀 (몸 상태는 따로)
            const c = Object.create(owner);
            return Object.assign(c, {
                isClone: true, owner, x, y, angle, hp: CLONE_HP, maxHp: CLONE_HP, life: CLONE_LIFE,
                giant: true, gun: false, canCharge: false, dmgMul: 1, z: 0, vz: 0, jumping: false, dashT: 0, guard: 0, guardCd: 0, noGuard: false, fallT: 0, slideT: 0,   // 거대화처럼 기절 · 띄움 면역 (피격 때 쓰러지듯 날아가지 않음)
                moving: false, attacking: false, attackT: 0, hitDone: false, punchLanded: false, punchHand: 0, kicking: false, kickT: 0, cooldown: 0, stun: 0, dizzy: 0, flat: 0,
                combo: 0, comboT: 99, hitFlash: 0, shake: 0, hitFx: 0, blockFlash: 0, tauntT: 0, gunT: 0, kiOn: false, flurryOn: false, shoryuOn: false, fx: burstFx()
            });
        }
        function startClone(p) {
            if (!p.canClone || gameOver || p.cloneCd > 0 || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.dizzy > 0 || p.guard > 0 || p.slideT > 0 || p.dashT > 0) return;
            if (p.z > 0 && !p.jumping) return;
            if (p.stamina < CLONE_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= CLONE_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.cloneCd = CLONE_CD; p.cooldown = 0.3;
            for (let i = clones.length - 1; i >= 0; i--) if (clones[i].owner === p) clones.splice(i, 1);   // 분신은 한 명만 (다시 쓰면 이전 분신은 사라짐)
            let x = p.x, y = p.y;
            for (const s of [1, -1]) {   // 내 오른쪽 옆 → 왼쪽 옆, 둘 다 막혀 있으면 내 자리에서 시작
                const nx = p.x + Math.cos(p.angle + s * Math.PI / 2) * MIN_PLAYER_DIST, ny = p.y + Math.sin(p.angle + s * Math.PI / 2) * MIN_PLAYER_DIST;
                if (!blockedAt(nx, ny) && (!arena || Math.hypot(nx - ARENA_C, ny - ARENA_C) < ARENA_R - 12)) { x = nx; y = ny; break; }
            }
            clones.push(mkClone(p, x, y, p.angle));
            bgm.sfx('taunt');
        }
        function startInvis(p) {
            if (!p.canInvis || gameOver || p.invisCd > 0 || p.invisT > 0 || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0) return;
            if (p.stamina < INVIS_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= INVIS_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.invisT = INVIS_TIME; p.invisCd = INVIS_CD;
            bgm.sfx('ink');
        }
        function startHeal(p) {   // 특수키를 누르는 동안 물약을 마시며 서서히 회복 (최대 HEAL_HOLD 초 · 2칸). 떼면 거기까지만 회복하고 쿨타임
            if (!p.canHeal || p.healOn || gameOver || p.healCd > 0 || p.attacking || p.kicking || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0) return;
            if (p.hp >= p.maxHp) { p.lackT = LACK_TIME; p.lackMsg = '체력이 가득 차서 사용할 수 없음'; return; }
            if (p.stamina < HEAL_COST * 0.2) { p.lackT = LACK_TIME; return; }
            p.healOn = true; p.healT = 0;
        }
        function releaseHeal(p) { if (p.healOn && p.healT > 0) p.healCd = HEAL_CD; p.healOn = false; p.healT = 0; }   // 조금이라도 마셨으면 쿨타임
        function updateHeal(dt) {
            for (const p of [p1, p2]) {
                if (!p.healOn) continue;
                if (gameOver || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.attacking || p.kicking || p.stamina <= 0) { releaseHeal(p); continue; }   // 맞거나 다른 행동을 하면 멈춤
                const step = Math.min(dt, HEAL_HOLD - p.healT);
                p.healT += step;
                p.hp = Math.min(p.maxHp, p.hp + HEAL_AMOUNT / HEAL_HOLD * step);
                p.stamina = Math.max(0, p.stamina - HEAL_COST / HEAL_HOLD * step); p.staminaDelay = STAMINA_REGEN_DELAY;
                updateUI();   // 체력바에 바로 반영
                if (p.healT >= HEAL_HOLD || p.hp >= p.maxHp) releaseHeal(p);   // 끝까지 마심 / 체력이 가득 참
            }
        }
        function startObst(p) {   // 시전자 발밑에 박스 (높이 OBST_H) 를 만들고 그 위로 올라섬. 놓을 자리가 막혔거나 상대가 서 있으면 실패 (쿨타임 · 스테미나 안 씀)
            if (!p.canObst || gameOver || p.obstCd > 0 || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.dizzy > 0 || p.guard > 0 || p.slideT > 0) return;
            if (p.z > 0 && !p.jumping) return;
            if (p.stamina < OBST_COST) { p.lackT = LACK_TIME; return; }
            const x = p.x, y = p.y;
            const R = OBST_HALF + PLAYER_RADIUS + 2, H = OBST_HALF;
            const bad = [[-H, -H], [H, -H], [-H, H], [H, H]].some(([dx, dy]) => isWallAt(x + dx, y + dy) || (arena && Math.hypot(x + dx - ARENA_C, y + dy - ARENA_C) > ARENA_R - 12))
                || [p1, p2, ...clones].some(q => q !== p && Math.abs(q.x - x) < R && Math.abs(q.y - y) < R)
                || PILLARS.some(([cx, cy]) => Math.abs(cx - x) < H + PILLAR_R && Math.abs(cy - y) < H + PILLAR_R)
                || obstacles.some(o => Math.abs(o.x - x) < H * 2 && Math.abs(o.y - y) < H * 2);
            if (bad) { bgm.sfx('deny'); return; }
            p.stamina -= OBST_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.obstCd = OBST_CD; p.cooldown = 0.2;
            obstacles.push({ x, y, t: OBST_LIFE, hp: OBST_HP });
            p.vz = Math.max(p.vz, OBST_RISE_VEL); p.z = Math.max(p.z, 0.01); p.jumping = true;   // 박스가 솟으면서 시전자가 위로 튀어 올라 윗면에 착지 (updateAir 가 boxFloor 로 받아 줌)
            bgm.sfx('guard');
        }
        function updateObstacles(dt) {
            if (gameOver) { obstacles.length = 0; return; }   // 라운드가 끝나면 박스도 바로 사라짐
            for (let i = obstacles.length - 1; i >= 0; i--) if ((obstacles[i].t -= dt) <= 0) obstacles.splice(i, 1);
            for (const q of [p1, p2, ...clones]) if (q.boxDropT > 0) q.boxDropT -= dt;
            for (const b of obstacles) {   // 발차기로 밀린 박스: 미끄러지다 서서히 멈춤. 벽 · 기둥 · 다른 박스 · 바닥에 선 사람에 막히면 거기서 멈춤
                if (!b.vx && !b.vy) continue;
                const dx = b.vx * dt, dy = b.vy * dt, nx = b.x + dx, ny = b.y + dy;
                if (!boxFits(b, nx, ny)) { b.vx = b.vy = 0; continue; }
                b.x = nx; b.y = ny;
                const sp = Math.hypot(b.vx, b.vy), k = Math.max(0, sp - OBST_KICK_DECEL * dt) / sp;
                b.vx *= k; b.vy *= k;
                if (k === 0) b.vx = b.vy = 0;
            }
        }
        function boxFits(b, x, y) {   // 박스 b 를 (x, y) 로 옮겨도 되는지
            const H = OBST_HALF;
            return ![[-H, -H], [H, -H], [-H, H], [H, H]].some(([dx, dy]) => isWallAt(x + dx, y + dy) || (arena && Math.hypot(x + dx - ARENA_C, y + dy - ARENA_C) > ARENA_R - 12))
                && !PILLARS.some(([cx, cy]) => Math.abs(cx - x) < H + PILLAR_R && Math.abs(cy - y) < H + PILLAR_R)
                && !obstacles.some(o => o !== b && Math.abs(o.x - x) < H * 2 && Math.abs(o.y - y) < H * 2)
                && ![p1, p2, ...clones].some(q => q.z < OBST_H - 0.5 && !(q.boxDropT > 0) && Math.abs(q.x - x) < H + PLAYER_RADIUS && Math.abs(q.y - y) < H + PLAYER_RADIUS);   // 박스보다 낮은 사람이 막음 (방금 박스에서 떨어지는 사람은 제외)
        }
        // 분신 AI: 주인은 무시하고 상대 쪽으로 돌아서 걸어가 사거리 안에서 주먹을 휘두름 (벽 · 기둥은 막힘, 콜로세움 가장자리 밖으로는 안 나감)
        function updateClones(dt) {
            for (let i = clones.length - 1; i >= 0; i--) {
                const c = clones[i], foe = c.owner === p1 ? p2 : p1;
                if (gameOver || c.hp <= 0 || (c.life -= dt) <= 0) { clones.splice(i, 1); continue; }
                if (c.hitFlash > 0) c.hitFlash = Math.max(0, c.hitFlash - dt);
                if (c.hitFx > 0) c.hitFx = Math.max(0, c.hitFx - dt);
                if (c.shake > 0) c.shake = Math.max(0, c.shake - dt);
                if (c.cooldown > 0) c.cooldown = Math.max(0, c.cooldown - dt);
                c.moving = false;
                if (c.attacking) {
                    c.attackT += dt;
                    if (!c.hitDone && c.attackT >= ATTACK_HIT_TIME) { c.hitDone = true; resolveHit(c, foe); }
                    if (!c.attacking || c.attackT >= ATTACK_DURATION) { c.attacking = false; c.attackT = 0; c.cooldown = CLONE_ATK_CD; }   // 가드에 막혀 끊겨도 같은 대기
                    continue;
                }
                const dx = foe.x - c.x, dy = foe.y - c.y, dist = Math.hypot(dx, dy);
                let da = Math.atan2(dy, dx) - c.angle;
                while (da < -Math.PI) da += Math.PI * 2;
                while (da > Math.PI) da -= Math.PI * 2;
                c.angle += Math.max(-ROT_SPEED * CLONE_TURN * dt, Math.min(ROT_SPEED * CLONE_TURN * dt, da));
                const reach = ATTACK_REACH * c.reachMul;
                if (dist > reach * 0.8 && Math.abs(da) < 1) {
                    const ox = c.x, oy = c.y;
                    tryMove(c, c.x + Math.cos(c.angle) * CLONE_SPEED * dt, c.y + Math.sin(c.angle) * CLONE_SPEED * dt);
                    if (arena && Math.hypot(c.x - ARENA_C, c.y - ARENA_C) > ARENA_R - 12) { c.x = ox; c.y = oy; }
                    c.moving = c.x !== ox || c.y !== oy;
                } else if (dist <= reach && Math.abs(da) < 0.3 && c.cooldown <= 0 && Math.random() < CLONE_ATK_RATE * dt) {
                    c.attacking = true; c.attackT = 0; c.hitDone = false; c.punchLanded = false;
                    c.punchHand = 1 - c.punchHand;
                    bgm.sfx('punch');
                }
            }
        }
        // 상대 분신이 사정거리 · 각도 · 벽 검사를 통과해 본체보다 앞(같거나 더 가까움)에 있으면 분신이 대신 맞음
        function hitReach(a, t, kick, gun) {   // a 가 t 를 맞힐 수 있으면 거리, 아니면 -1 (resolveHit 의 검사와 같음)
            if (t.dashT > 0) return -1;
            const dx = t.x - a.x, dy = t.y - a.y, dist = Math.hypot(dx, dy);
            if (dist > (gun ? GUN_RANGE : (kick ? KICK_REACH : ATTACK_REACH + (a.knife ? KNIFE_REACH : 0)) * a.reachMul)) return -1;
            if (t.z > AIR_HIT_MAX_Z) return -1;
            let ang = Math.atan2(dy, dx) - a.angle;
            while (ang < -Math.PI) ang += Math.PI * 2;
            while (ang > Math.PI) ang -= Math.PI * 2;
            if (Math.abs(ang) > (gun ? Math.max(GUN_ANGLE, Math.atan(14 / Math.max(dist, 1))) : ATTACK_ANGLE)) return -1;
            rayExcludeBox = gun ? boxUnder(t) : null;   // 총은 박스 위 사람도 맞힘 (주먹 · 발차기는 박스에 막힘)
            castRay(a.x, a.y, Math.atan2(dy, dx));
            rayExcludeBox = null;
            return rayDist < dist ? -1 : dist;
        }
        // 박스 때리기: 상대 본체가 박스에 가려 안 닿는데 박스가 사정거리 · 각도 안에 있으면 박스가 대신 맞음 (체력이 다하면 부서짐)
        function hitBox(a, d, kick, gun) {
            if (!obstacles.length || a.isClone || hitReach(a, d, kick, gun) >= 0) return false;
            const reach = (gun ? GUN_RANGE : (kick ? KICK_REACH : ATTACK_REACH + (a.knife ? KNIFE_REACH : 0)) * a.reachMul);
            let best = null, bestD = Infinity;
            for (const b of obstacles) {
                if (Math.abs(a.x - b.x) < OBST_HALF && Math.abs(a.y - b.y) < OBST_HALF) continue;   // 박스 위 · 안에서는 제외
                const dx = b.x - a.x, dy = b.y - a.y, dist = Math.hypot(dx, dy);
                if (dist - OBST_HALF > reach) continue;
                let ang = Math.atan2(dy, dx) - a.angle;
                while (ang < -Math.PI) ang += Math.PI * 2;
                while (ang > Math.PI) ang -= Math.PI * 2;
                if (Math.abs(ang) > (gun ? GUN_ANGLE : ATTACK_ANGLE) + Math.atan(OBST_HALF / Math.max(dist, 1))) continue;
                if (dist < bestD) { best = b; bestD = dist; }
            }
            if (!best) return false;
            const dmg = Math.round(((gun ? GUN_DAMAGE : kick ? KICK_DAMAGE : DAMAGE) + (a.knife && !kick && !gun ? KNIFE_BONUS : 0))
                * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1) * (gun ? 1 : (a.canCharge ? (a.dmgMul || 1) : 1)));
            best.hp -= dmg;
            if (best.hp <= 0) obstacles.splice(obstacles.indexOf(best), 1);
            else if (kick && bestD - OBST_HALF <= OBST_PUSH_REACH) {   // 가까이서 찬 발차기만 박스를 차는 방향으로 밀어냄 (아예 못 움직이는 자리면 안 밀림)
                const ux = Math.cos(a.angle), uy = Math.sin(a.angle);
                if (boxFits(best, best.x + ux * 2, best.y + uy * 2)) {
                    for (const q of [p1, p2, ...clones]) if (boxUnder(q) === best) { q.boxDropT = 0.8; q.vz = 0; }   // 위에 선 사람은 박스가 밀리면 떨어짐 (떨어지는 동안은 밀리는 박스를 막지 않음)
                    best.vx = ux * OBST_KICK_V; best.vy = uy * OBST_KICK_V;
                }
            }
            bgm.sfx('hit');
            return true;
        }
        function cloneInFront(a, d, kick, gun) {
            if (!clones.length) return d;
            let best = d, bestD = hitReach(a, d, kick, gun);
            if (bestD < 0) bestD = Infinity;
            for (const c of clones) {
                if (c.owner !== d) continue;
                const dc = hitReach(a, c, kick, gun);
                if (dc >= 0 && dc <= bestD) { best = c; bestD = dc; }
            }
            return best;
        }

        // 오징어 먹물: 오징어를 들고 앞의 적에게 먹물을 뿌림. 맞은 적의 화면이 INK_TIME 동안 먹물로 가려짐 (가드 중인 적에게는 막힘)
        function inkHits(a, d) {
            const dx = d.x - a.x, dy = d.y - a.y, dist = Math.hypot(dx, dy);
            if (dist > INK_RANGE) return false;
            let ang = Math.atan2(dy, dx) - a.angle;
            while (ang < -Math.PI) ang += Math.PI * 2;
            while (ang > Math.PI) ang -= Math.PI * 2;
            if (Math.abs(ang) > INK_ANGLE) return false;
            castRay(a.x, a.y, Math.atan2(dy, dx));   // 벽 너머로는 안 닿음
            return rayDist >= dist;
        }
        function startInk(p) {
            if (!p.canInk || gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0 || p.inkCd > 0) return;
            if (p.z > 0 && !p.jumping) return;   // 맞아서 뜬 상태에서는 가드만 가능
            if (p.stamina < INK_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= INK_COST;
            p.staminaDelay = STAMINA_REGEN_DELAY;
            p.inkCd = INK_COOLDOWN;
            p.inkT = INK_FX_TIME;
            p.cooldown = 0.3;
            bgm.sfx('ink');
            const d = p === p1 ? p2 : p1;
            if (d.dashT <= 0 && inkHits(p, d)) {   // 대쉬 중에는 무적
                if (d.guard > 0) d.blockFlash = 0.2;   // 가드로 막힘 (쏜 쪽은 기절하지 않음)
                else { d.inked = INK_TIME; d.inkSeed = Math.random(); if (aiMode && d === aiSelf) aiFreezeT = AI_INK_FREEZE; }   // AI는 먹물을 맞으면 잠시 멈춤
            }
        }

        // 장풍: 특수공격 키를 누르고 있으면 기를 모으고, 떼면 기 덩어리가 앞으로 날아감 (KI_MIN 이상 모았을 때만, 못 모으면 불발)
        function startKi(p) {
            if (!p.canKi || p.kiOn || gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0 || p.kiCd > 0) return;
            if (p.z > 0 && !p.jumping) return;   // 맞아서 뜬 상태에서는 가드만 가능
            if (p.stamina < KI_COST) { p.lackT = LACK_TIME; return; }
            p.kiOn = true; p.kiT = 0;
        }
        function releaseKi(p) {
            if (!p.kiOn) return;
            const r = p.kiT / KI_TIME;
            p.kiOn = false; p.kiT = 0;
            if (r < KI_MIN || paused || p.stamina < KI_COST) return;
            p.stamina -= KI_COST;
            p.staminaDelay = STAMINA_REGEN_DELAY;
            p.kiCd = KI_COOLDOWN;
            p.cooldown = 0.3;
            bgm.sfx('gun');
            castRay(p.x, p.y, p.angle);   // 벽 앞에서 사라짐
            kiBalls.push({ x: p.x, y: p.y, dx: Math.cos(p.angle), dy: Math.sin(p.angle), d: 0, max: Math.min(KI_RANGE, rayDist), owner: p, full: r >= 1 });
        }
        function kiHit(b, d) {
            const a = b.owner;
            if (d.guard > 0) {
                if (!b.full) { d.blockFlash = 0.2; return; }   // 가드로 막힘 (쏜 쪽은 기절하지 않음)
                endGuard(d);   // 최대 충전은 가드를 뚫음
            }
            if (!tutorial) d.hp = Math.max(0, d.hp - KI_DAMAGE * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1));
            a.combo = (a.combo > 0 && a.comboT < COMBO_WINDOW) ? a.combo + 1 : 1;
            a.comboT = 0;
            d.combo = 0;
            d.hitFlash = 0.3;
            d.shake = SHAKE_DURATION;
            d.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            d.fx = burstFx();
            d.attacking = false; d.attackT = 0; d.kicking = false; d.kickT = 0; d.charging = ''; d.chargeT = 0; d.kiOn = false; d.kiT = 0;
            d.guardCd = Math.min(d.guardCd, HIT_GUARD_CD);
            if (!d.giant) {   // 거대화: 기절 · 넉백 면역
                d.stun = b.full ? KI_STUN_MAX : KI_STUN;
                if (b.full) { d.dizzy = KI_STUN_MAX; d.slideT = KICK_SLIDE_TIME; d.slideMul = KI_SLIDE_MUL; d.slideDX = b.dx; d.slideDY = b.dy; }
            }
            updateUI();
            if (d.hp <= 0) {
                gameOver = true;
                winner = a;
                a.wins++;
                matchOver = a.wins >= matchCfg.wins;
                updateUI();
            }
        }
        function updateKi(dt) {
            for (const p of [p1, p2]) {
                if (p.kiCd > 0) p.kiCd = Math.max(0, p.kiCd - dt);
                if (!p.kiOn) continue;
                if (gameOver || p.stun > 0 || p.dizzy > 0 || p.guard > 0 || p.attacking || p.kicking) { p.kiOn = false; p.kiT = 0; }   // 맞거나 가드하면 충전 취소
                else p.kiT = Math.min(KI_TIME, p.kiT + dt);
            }
            for (let i = kiBalls.length - 1; i >= 0; i--) {
                const b = kiBalls[i], d = b.owner === p1 ? p2 : p1, step = (b.full ? KI_SPEED_MAX : KI_SPEED) * dt;
                b.x += b.dx * step; b.y += b.dy * step; b.d += step;
                if (gameOver || b.d >= b.max) { kiBalls.splice(i, 1); continue; }
                if (Math.hypot(d.x - b.x, d.y - b.y) <= KI_HIT_R && d.z <= AIR_HIT_MAX_Z && d.dashT <= 0) { kiBalls.splice(i, 1); kiHit(b, d); }   // 대쉬 중에는 무적: 기 덩어리가 통과
            }
        }

        // ===== 도시 맵 자동차: 10초마다 50% 확률로 십자 도로 중 한 길(방향도 무작위)을 지나감. 맞으면 체력 2칸 + 납작해짐 (버스 4초 · 자동차 2초) =====
        function fitCar(c) {   // 종류(자동차 · 버스)에 맞는 크기 · 속도를 붙임
            if (c.bus) { c.len = BUS_LEN; c.wid = (c.dx ? BUS_ROAD_H : BUS_ROAD_V) * MAP_SIZE - 6; c.h = BUS_H; c.speed = BUS_SPEED; }   // 길 폭에서 양옆 3px만 뺌 (건물 벽면과 겹쳐 깜빡이지 않게)
            else { c.len = CAR_LEN; c.wid = CAR_WID; c.h = CAR_H; c.speed = CAR_SPEED; }
            return c;
        }
        function spawnCar() {
            const horiz = Math.random() < 0.5, sg = Math.random() < 0.5 ? 1 : -1, bus = Math.random() < BUS_CHANCE;
            const len = bus ? BUS_LEN : CAR_LEN, far = (horiz ? MAP_W : MAP_H) * MAP_SIZE;   // 도로 끝은 바깥벽: 차가 벽 속에서 나와 반대쪽 벽 속으로 사라짐
            const start = sg > 0 ? MAP_SIZE - len / 2 - 4 : far - MAP_SIZE + len / 2 + 4;
            car = fitCar({ x: horiz ? start : MAP_W * MAP_SIZE / 2, y: horiz ? (MAP_H >> 1) * MAP_SIZE + MAP_SIZE / 2 : start, dx: horiz ? sg : 0, dy: horiz ? 0 : sg, ci: Math.floor(Math.random() * CAR_COLORS.length), bus, warn: CAR_WARN, hit: [false, false] });   // warn > 0 동안은 길만 빨갛게 보이고 차는 아직 출발 전
        }
        function carPath(c) {   // 차가 지나갈 길(바닥 띠): 안쪽 벽 사이 도로 한가운데, 차 폭만큼
            const horiz = c.dx !== 0;
            return horiz ? { x0: MAP_SIZE, x1: (MAP_W - 1) * MAP_SIZE, y0: c.y - c.wid / 2, y1: c.y + c.wid / 2 }
                         : { x0: c.x - c.wid / 2, x1: c.x + c.wid / 2, y0: MAP_SIZE, y1: (MAP_H - 1) * MAP_SIZE };
        }
        function carWarnPath(c) {   // 경고: 차가 나오는 쪽 끝에서부터 출발 직전까지 길이 빨갛게 번져 감 (carPath 중 번진 만큼만)
            const w = carPath(c), f = 1 - c.warn / CAR_WARN;
            if (c.dx) { const len = (w.x1 - w.x0) * f; return c.dx > 0 ? { x0: w.x0, x1: w.x0 + len, y0: w.y0, y1: w.y1 } : { x0: w.x1 - len, x1: w.x1, y0: w.y0, y1: w.y1 }; }
            const len = (w.y1 - w.y0) * f; return c.dy > 0 ? { x0: w.x0, x1: w.x1, y0: w.y0, y1: w.y0 + len } : { x0: w.x0, x1: w.x1, y0: w.y1 - len, y1: w.y1 };
        }
        function carHit(p) {
            if (p.guard > 0) endGuard(p);   // 가드로는 못 막음
            if (!tutorial) p.hp = Math.max(0, p.hp - CAR_DAMAGE);
            p.combo = 0;
            p.hitFlash = 0.3; p.shake = SHAKE_DURATION; p.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            p.fx = burstFx();
            p.attacking = false; p.attackT = 0; p.kicking = false; p.kickT = 0; p.charging = ''; p.chargeT = 0; p.kiOn = false; p.kiT = 0;
            if (!p.giant) {   // 뜨지도 밀려나지도 않고 제자리에서 납작하게 눌림 (거대화: 기절 면역이라 안 납작해짐)
                const t = car.bus ? BUS_FLAT : CAR_FLAT;
                p.flat = p.flatMax = t; p.stun = t; p.dizzy = t;
                if (p.vz > 0) p.vz = 0;
            }
            updateUI();
        }
        function updateCar(dt) {
            if (!city || !started || tutorial) { car = null; carT = 0; return; }
            if (gameOver || picking || fusing) return;
            const was = carT;
            carT += dt;
            if (was < CAR_INTERVAL - CAR_WARN && carT >= CAR_INTERVAL - CAR_WARN && !car && Math.random() < CAR_CHANCE) spawnCar();   // 차가 오기 CAR_WARN 초 전에 굴려서 길부터 빨갛게
            if (carT >= CAR_INTERVAL) carT -= CAR_INTERVAL;
            if (!car) return;
            if (car.warn > 0) { car.warn -= dt; if (car.warn <= 0) { car.warn = 0; bgm.sfx('horn'); } return; }   // 출발하는 순간 경적
            car.x += car.dx * car.speed * dt; car.y += car.dy * car.speed * dt;
            const horiz = car.dx !== 0, along = horiz ? car.x : car.y, dir = horiz ? car.dx : car.dy, far = (horiz ? MAP_W : MAP_H) * MAP_SIZE;
            if (dir > 0 ? along - car.len / 2 > far - MAP_SIZE : along + car.len / 2 < MAP_SIZE) { car = null; return; }   // 반대쪽 벽 속으로 다 들어감
            const hx = horiz ? car.len / 2 : car.wid / 2, hy = horiz ? car.wid / 2 : car.len / 2;
            [p1, p2].forEach((p, i) => {   // 차는 한 사람을 한 번만 침. 점프로 차 위를 넘거나 대쉬(무적) 중이면 피함
                if (car.hit[i] || p.z > car.h || p.dashT > 0 || p.fallT > 0) return;
                if (Math.abs(p.x - car.x) < hx + PLAYER_RADIUS && Math.abs(p.y - car.y) < hy + PLAYER_RADIUS) { car.hit[i] = true; carHit(p); }
            });
            if (!tutorial && !gameOver && (p1.hp <= 0 || p2.hp <= 0)) {   // KO: 같이 쓰러지면 무승부
                gameOver = true;
                if (p1.hp > 0 || p2.hp > 0) {
                    winner = p1.hp > 0 ? p1 : p2;
                    winner.wins++;
                    matchOver = winner.wins >= matchCfg.wins;
                }
                updateUI();
            }
        }

        // ===== 순간이동 (특수): 특수공격 키를 누르고 있으면 바닥의 빨간 원이 앞으로 서서히 멀어지고, 키를 떼면 그 위치로 순간이동. 벽 · 기둥 · 상대 앞에서 원이 멈춤 =====
        function blinkReach(p) {   // 지금 바라보는 방향으로 갈 수 있는 최대 거리
            const d = p === p1 ? p2 : p1, dx = Math.cos(p.angle), dy = Math.sin(p.angle);
            let moved = 0, ok = 0;
            while (moved < BLINK_DIST) {
                const next = Math.min(BLINK_DIST, moved + 8), nx = p.x + dx * next, ny = p.y + dy * next;
                if (blockedAt(nx, ny)) break;   // 벽 · 기둥 (상대는 통과)
                moved = next;
                if (Math.hypot(d.x - nx, d.y - ny) >= MIN_PLAYER_DIST) ok = moved;   // 상대 몸 위에는 착지 불가
            }
            return ok;
        }
        function blinkAfford(p) {   // 지금 스테미나로 갈 수 있는 최대 거리
            return BLINK_DIST * p.stamina / BLINK_COST;
        }
        function startBlink(p) {
            if (!p.canBlink || p.blinkOn || gameOver || p.blinkCd > 0 || p.attacking || p.kicking || p.charging || p.flurryOn || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.dashT > 0 || p.fallT > 0 || p.z > 0 || p.cooldown > 0) return;
            if (p.stamina < BLINK_COST_MIN) { p.lackT = LACK_TIME; return; }
            p.blinkOn = true; p.blinkD = 0;
        }
        function releaseBlink(p) {
            if (!p.blinkOn) return;
            const dist = Math.min(p.blinkD, blinkReach(p), blinkAfford(p));
            p.blinkOn = false; p.blinkD = 0;
            if (paused || gameOver || dist < BLINK_MIN || p.stamina < BLINK_COST_MIN) return;   // 너무 가깝거나 일시정지 중이면 취소
            const ratio = dist / BLINK_DIST;   // 멀리 갈수록 스테미나 · 쿨타임 증가
            p.stamina = Math.max(0, p.stamina - Math.max(BLINK_COST_MIN, Math.round(BLINK_COST * ratio))); p.staminaDelay = STAMINA_REGEN_DELAY;
            p.blinkCd = Math.max(BLINK_CD_MIN, BLINK_CD * ratio);
            p.ghostX = p.x; p.ghostY = p.y; p.ghostA = p.angle; p.ghostT = BLINK_GHOST_T;   // 떠난 자리에 잔상
            p.x += Math.cos(p.angle) * dist; p.y += Math.sin(p.angle) * dist;
            bgm.sfx('jump');
        }
        function updateBlink(p, dt) {
            if (p.ghostT > 0) p.ghostT = Math.max(0, p.ghostT - dt);
            if (!p.blinkOn) return;
            if (gameOver || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.attacking || p.kicking || p.flurryOn || p.dashT > 0 || p.fallT > 0 || p.z > 0) { p.blinkOn = false; p.blinkD = 0; return; }   // 맞거나 다른 행동을 하면 취소
            p.blinkD = Math.min(p.blinkD + BLINK_SPEED * dt, blinkReach(p), blinkAfford(p));
        }

        // ===== 백열권 (특수): 특수공격 키로 FLURRY_TIME 동안 제자리에서 주먹을 연타. 한 대마다 사거리 · 각도 · 벽 · 가드를 따로 판정 =====
        function startFlurry(p) {
            if (!p.canFlurry || p.flurryOn || gameOver || p.flurryCd > 0 || p.attacking || p.kicking || p.charging || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.dashT > 0 || p.fallT > 0 || p.z > 0 || p.cooldown > 0) return;
            if (p.stamina < FLURRY_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= FLURRY_COST; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.flurryOn = true; p.flurryT = 0; p.flurryHits = 0; p.flurryCd = FLURRY_CD;
            p.cooldown = FLURRY_TIME + FLURRY_END_LAG;   // 쓰는 동안 다른 공격 불가
            bgm.sfx('punch');
        }
        function stopFlurry(p) { p.flurryOn = false; p.flurryT = 0; p.flurryHits = 0; p.cooldown = 0; }   // 중간에 끊김 (맞음 · 가드에 막힘 · 라운드 끝)
        function flurryHit(a, d) {
            if (d.dashT > 0 || d.z > AIR_HIT_MAX_Z) return;   // 대쉬 무적 · 너무 높이 떠 있음: 이번 한 대는 빗나감
            const dx = d.x - a.x, dy = d.y - a.y, dist = Math.hypot(dx, dy);
            if (dist > ATTACK_REACH * a.reachMul) return;
            let ang = Math.atan2(dy, dx) - a.angle;
            while (ang < -Math.PI) ang += Math.PI * 2;
            while (ang > Math.PI) ang -= Math.PI * 2;
            if (Math.abs(ang) > ATTACK_ANGLE) return;
            castRay(a.x, a.y, Math.atan2(dy, dx));
            if (rayDist < dist) return;
            if (d.guard > 0) {   // 가드로 막으면 피해 없음, 백열권은 끊김 (쓴 쪽은 기절하지 않음)
                d.blockFlash = 0.2;
                stopFlurry(a);
                return;
            }
            if (!tutorial) d.hp = Math.max(0, d.hp - Math.round(FLURRY_DAMAGE * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1)));
            a.combo = (a.combo > 0 && a.comboT < COMBO_WINDOW) ? a.combo + 1 : 1;
            a.comboT = 0;
            d.combo = 0;
            d.hitFlash = 0.3; d.shake = SHAKE_DURATION; d.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            d.fx = burstFx();
            d.attacking = false; d.attackT = 0; d.kicking = false; d.kickT = 0; d.charging = ''; d.chargeT = 0; d.kiOn = false; d.kiT = 0;
            d.guardCd = Math.min(d.guardCd, HIT_GUARD_CD);
            updateUI();
            if (d.hp <= 0) {
                gameOver = true;
                winner = a;
                a.wins++;
                matchOver = a.wins >= matchCfg.wins;
                updateUI();
            }
        }
        function updateFlurry(p, d, dt) {
            if (!p.flurryOn) return;
            if (gameOver || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.fallT > 0 || p.z > 0) { stopFlurry(p); return; }
            p.flurryT += dt;
            while (p.flurryOn && !gameOver && p.flurryHits < FLURRY_HITS && p.flurryT >= FLURRY_GAP * (p.flurryHits + 1)) {
                p.flurryHits++;
                if (p.flurryHits % 2 === 1) bgm.sfx('punch');
                flurryHit(p, d);
            }
            if (p.flurryOn && p.flurryT >= FLURRY_TIME) { p.flurryOn = false; p.flurryT = 0; p.flurryHits = 0; }   // 다 때림 (후딜은 cooldown 에 남아 있음)
        }

        // ===== 승룡권 (히든 스킬): 방향키로 한 바퀴 돌고 특수공격 키 → 돌면서 어퍼컷 =====
        function tryShoryu(p) {
            if (!p.canShoryu || p.shoryuReady <= 0 || gameOver || p.shoryuOn || p.attacking || p.kicking || p.kiOn || p.stun > 0 || p.dizzy > 0 || p.slideT > 0 || p.guard > 0 || p.z > 0 || p.cooldown > 0) return false;
            const cost = p.maxStamina * SHORYU_COST;
            if (p.stamina < cost) { p.lackT = LACK_TIME; return true; }   // 스테미나 부족 (장풍이 대신 나가지 않게 키 입력은 소비)
            p.stamina -= cost; p.staminaDelay = STAMINA_REGEN_DELAY;
            p.shoryuReady = 0;
            shoryuFxT = SHORYU_FIRE_TIME;
            p.shoryuOn = true; p.shoryuT = 0; p.shoryuHits = 0; p.shoryuTarget = null; p.shoryuAimAng = null;
            p.shoryuAngle = p.angle;
            p.cooldown = SHORYU_TIME;   // 쓰는 동안 다른 공격 불가
            p.vz = SHORYU_RISE; p.z = 0.01; p.shoryuAir = true;   // 누르는 순간부터 위로 솟구침 (맞히면 상대도 같이 뜸)
            bgm.sfx('jump');
            return true;
        }
        function shoryuDamage(a, d) {   // 한 타: 데미지 + 이펙트 (총 데미지를 타수로 나눔)
            if (!tutorial) d.hp = Math.max(0, d.hp - Math.round(SHORYU_DAMAGE / SHORYU_HITS * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1)));
            a.combo = (a.combo > 0 && a.comboT < COMBO_WINDOW) ? a.combo + 1 : 1;   // 타마다 콤보 +1
            a.comboT = 0;
            d.combo = 0;
            d.hitFlash = 0.3; d.shake = SHAKE_DURATION; d.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            d.fx = burstFx();
            if (!d.giant) d.stun = Math.max(d.stun, SHORYU_STUN);
            updateUI();
            if (d.hp <= 0) {
                gameOver = true;
                winner = a;
                a.wins++;
                matchOver = a.wins >= matchCfg.wins;
                updateUI();
            }
        }
        function resolveShoryu(a, d) {   // 첫 타: 사거리 · 각도 · 가드 판정. 맞으면 둘 다 떠오르고 true
            const dx = d.x - a.x, dy = d.y - a.y, dist = Math.hypot(dx, dy);
            if (dist > ATTACK_REACH * a.reachMul || d.z > AIR_HIT_MAX_Z || d.dashT > 0) return false;
            let ang = Math.atan2(dy, dx) - a.shoryuAngle;   // 돌기 시작할 때 보던 방향으로 판정
            while (ang < -Math.PI) ang += Math.PI * 2;
            while (ang > Math.PI) ang -= Math.PI * 2;
            if (Math.abs(ang) > ATTACK_ANGLE) return false;
            castRay(a.x, a.y, Math.atan2(dy, dx));
            if (rayDist < dist) return false;
            if (d.guard > 0) {   // 가드로 막으면 데미지 없음, 쓴 쪽이 기절
                if (!a.giant) { a.stun = GUARD_BREAK_STUN; a.dizzy = GUARD_BREAK_STUN; }
                d.blockFlash = 0.2;
                return false;
            }
            d.attacking = false; d.attackT = 0; d.kicking = false; d.kickT = 0; d.charging = ''; d.chargeT = 0; d.kiOn = false; d.kiT = 0; d.shoryuOn = false;
            d.guardCd = Math.min(d.guardCd, HIT_GUARD_CD);
            d.jumping = false;
            if (!d.giant) {   // 거대화: 기절 · 띄우기 면역
                d.vz = SHORYU_LAUNCH_VEL; d.z = Math.max(d.z, a.z, 0.01);   // 쓴 사람과 같은 높이에서 함께 올라가고, 맞은 사람이 더 높이 뜨고 더 늦게 떨어짐
                d.noGuard = true;   // 착지할 때까지 가드 불가
                a.shoryuOrb = { r: Math.max(dist, MIN_PLAYER_DIST) };   // 쓴 사람 앞에서 같이 돌 때 유지할 거리
            }
            shoryuDamage(a, d);
            return true;
        }
        function updateShoryu(p, d, dt) {
            // 한 바퀴 돌아 준비되면 제한 시간 없이 유지 (쓰거나 라운드가 리셋될 때만 해제)
            if (!p.shoryuOn) return;
            if (gameOver || p.stun > 0) { p.shoryuOn = false; p.angle = p.shoryuAimAng !== null ? p.shoryuAimAng : p.shoryuAngle; return; }   // 맞거나 라운드가 끝나면 중단
            p.shoryuT += dt;
            const T0 = SHORYU_HIT_TIMES[0];
            if (p.shoryuHits === 0) {   // 첫 타 전: 맞힐 수 있는 상대가 앞에 있으면 첫 타 순간 정확히 상대를 바라보도록 몸을 돌림
                const ta = Math.atan2(d.y - p.y, d.x - p.x);
                let df = ta - p.shoryuAngle; while (df < -Math.PI) df += Math.PI * 2; while (df > Math.PI) df -= Math.PI * 2;
                const aim = Math.hypot(d.x - p.x, d.y - p.y) <= ATTACK_REACH * p.reachMul && d.z <= AIR_HIT_MAX_Z && Math.abs(df) <= ATTACK_ANGLE;
                p.shoryuAimAng = aim ? p.shoryuAngle + df : null;
                p.angle = aim ? p.shoryuAngle + df * Math.min(1, p.shoryuT / T0)
                              : p.shoryuAngle + Math.min(1, p.shoryuT / SHORYU_TIME) * Math.PI * 2 * p.spinDir;
            } else if (p.shoryuAimAng !== null) {   // 첫 타 후: 상대를 바라본 방향에서 시작해 정확히 한 바퀴
                p.angle = p.shoryuAimAng + Math.min(1, (p.shoryuT - T0) / (SHORYU_TIME - T0)) * Math.PI * 2 * p.spinDir;
            } else {
                p.angle = p.shoryuAngle + Math.min(1, p.shoryuT / SHORYU_TIME) * Math.PI * 2 * p.spinDir;
            }
            while (!gameOver && p.shoryuHits < SHORYU_HITS && p.shoryuT >= SHORYU_HIT_TIMES[p.shoryuHits]) {   // 다단히트
                if (p.shoryuHits === 0) p.shoryuTarget = resolveShoryu(p, d) ? d : null;
                else if (p.shoryuTarget) shoryuDamage(p, p.shoryuTarget);
                p.shoryuHits++;
            }
            const tg = p.shoryuTarget;
            if (tg && p.shoryuOrb && !tg.giant && !gameOver) {   // 맞은 사람은 쓴 사람을 마주 본 채 쓴 사람 둘레를 같이 돔
                const phi = p.angle;   // 맞은 사람은 쓴 사람 정면에서 서로 마주 본 채 같이 돎 (한 바퀴 돌면 원래 자리)
                tryMove(tg, p.x + Math.cos(phi) * p.shoryuOrb.r, p.y + Math.sin(phi) * p.shoryuOrb.r);
                tg.angle = phi + Math.PI;
            }
            if (p.shoryuT >= SHORYU_TIME) { p.shoryuOn = false; p.angle = p.shoryuAimAng !== null ? p.shoryuAimAng : p.shoryuAngle; p.shoryuTarget = null; }
        }

        function startGun(p) {
            if (!p.gun || gameOver || p.attacking || p.kicking || p.cooldown > 0 || p.stun > 0 || p.guard > 0 || p.gunCd > 0 || p.gunReload > 0) return;
            if (p.z > 0 && !p.jumping) return;   // 맞아서 뜬 상태에서는 가드만 가능
            if (p.stamina < GUN_COST) { p.lackT = LACK_TIME; return; }
            p.stamina -= GUN_COST;
            p.staminaDelay = STAMINA_REGEN_DELAY;
            p.gunCd = GUN_COOLDOWN;
            p.gunT = GUN_FX_TIME;
            if (--p.gunAmmo <= 0) { p.gunAmmo = 0; p.gunReload = GUN_RELOAD_TIME; }   // 마지막 탄: 발사 연출이 끝나면 장전 시작
            bgm.sfx('gun');
            p.cooldown = 0.3;   // 쏜 직후 잠깐 다른 공격 불가
            resolveHit(p, p === p1 ? p2 : p1, false, true);   // 총알은 즉시 도달
        }

        function resolveHit(attacker, defender, kick, gun) {
            if (!attacker.isClone) defender = cloneInFront(attacker, defender, kick, gun);   // 상대 분신이 앞을 막고 있으면 분신이 대신 맞음
            if (!defender.isClone && hitBox(attacker, defender, kick, gun)) return;   // 박스가 막고 있으면 박스가 대신 맞음
            if (defender.dashT > 0) return;   // 대쉬 중에는 무적
            const chargeMul = attacker.canCharge ? (attacker.dmgMul || 1) : 1;   // 힘조절 카드가 없으면 남아 있는 충전 배율은 무시
            const dx = defender.x - attacker.x;
            const dy = defender.y - attacker.y;
            const distance = Math.hypot(dx, dy);
            if (distance > (gun ? GUN_RANGE : (kick ? KICK_REACH : ATTACK_REACH + (attacker.knife ? KNIFE_REACH : 0)) * attacker.reachMul)) return;
            if (defender.z > AIR_HIT_MAX_Z) return;   // 너무 높이 떠 있음

            let a = Math.atan2(dy, dx) - attacker.angle;
            while (a < -Math.PI) a += Math.PI * 2;
            while (a > Math.PI) a -= Math.PI * 2;
            if (Math.abs(a) > (gun ? Math.max(GUN_ANGLE, Math.atan(14 / Math.max(distance, 1))) : ATTACK_ANGLE)) return;

            // 벽 너머는 맞지 않음 (총은 박스 위에 선 사람도 맞힘)
            rayExcludeBox = gun ? boxUnder(defender) : null;
            castRay(attacker.x, attacker.y, Math.atan2(dy, dx));
            rayExcludeBox = null;
            if (rayDist < distance) return;

            // 상대가 가드 중이면 데미지 없음, 때린 쪽이 기절
            if (defender.guard > 0) {
                if (gun) { defender.blockFlash = 0.2; return; }   // 총알은 가드로 막히고, 쏜 쪽은 기절하지 않음
                if (!attacker.giant) { attacker.stun = GUARD_BREAK_STUN; attacker.dizzy = GUARD_BREAK_STUN; }   // 거대화: 기절 면역
                attacker.kicking = false;
                attacker.kickT = 0;
                attacker.attacking = false;
                attacker.attackT = 0;
                defender.blockFlash = 0.2;
                return;
            }

            const dmg = Math.round(((gun ? GUN_DAMAGE : kick ? KICK_DAMAGE : DAMAGE) + (attacker.knife && !kick && !gun ? KNIFE_BONUS : 0))
                * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1)   // 남은 시간이 적으면 피해 2배
                * (gun ? 1 : chargeMul) * (attacker.isClone ? CLONE_DMG_MUL : 1));   // 힘조절 카드 충전 배율 (총 제외), 소수점은 반올림
            if (!tutorial) defender.hp = Math.max(0, defender.hp - dmg);   // 튜토리얼에서는 체력이 줄지 않음
            // 콤보: 마지막으로 맞힌 지 1초 안에 또 맞히면 +1, 아니면 1부터 다시
            attacker.combo = (attacker.combo > 0 && attacker.comboT < COMBO_WINDOW) ? attacker.combo + 1 : 1;
            attacker.comboT = 0;
            defender.combo = 0;   // 맞은 쪽의 콤보는 끊김
            if (!kick && !gun) attacker.punchLanded = true;   // 주먹이 맞으면 후딜(쿨타임) 없이 바로 다음 주먹
            defender.hitFlash = 0.3;
            defender.shake = SHAKE_DURATION;
            defender.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            defender.fx = burstFx();
            if (!defender.giant) defender.stun = STUN_TIME;   // 거대화: 기절 면역
            defender.guardCd = Math.min(defender.guardCd, HIT_GUARD_CD);   // 맞으면 가드 쿨타임이 빨리 참
            defender.attacking = false;   // 하던 공격도 끊김
            defender.attackT = 0;
            defender.kicking = false;
            defender.kickT = 0;
            const kbMul = gun ? 1 : Math.max(1, chargeMul);   // 힘조절 강공격일수록 더 세게 밀려남 (약공격은 기본)
            if (!gun && !defender.giant) { defender.vz = PUNCH_LAUNCH_VEL * (1 + 0.25 * (kbMul - 1)); defender.z = Math.max(defender.z, 0.01); }   // 총알은 띄우지 않음
            defender.jumping = false;
            if (kick && !defender.giant) {   // 발차기: 멀리 밀려남 (벽에 부딪히면 updateSlide에서 기절)
                defender.slideT = KICK_SLIDE_TIME;
                defender.slideMul = Math.min(2, kbMul);
                defender.slideDX = Math.cos(attacker.angle);
                defender.slideDY = Math.sin(attacker.angle);
                defender.stun = KICK_SLIDE_TIME;
                defender.vz = LAUNCH_VEL * 1.3; defender.jumping = false;
            } else {
                tryMove(defender,
                    defender.x + Math.cos(attacker.angle) * KNOCKBACK * kbMul,
                    defender.y + Math.sin(attacker.angle) * KNOCKBACK * kbMul);
            }
            if (!gun && !defender.giant && chargeMul >= STRONG_MUL) { const st = chargeMul >= CHARGE_MAXMUL ? STRONG_STUN_MAX : STRONG_STUN; defender.stun = st; defender.dizzy = st; }   // 강공격 스턴
            updateUI();

            if (attacker.invisT > 0) attacker.invisT = 0;   // 투명: 맞히면 모습이 드러남
            if (defender.hp <= 0 && !defender.isClone) {   // 분신이 쓰러진 건 라운드 종료가 아님 / 분신이 쓰러뜨려도 승리는 주인 몫
                const win = attacker.owner || attacker;
                gameOver = true;
                winner = win;
                win.wins++;
                matchOver = win.wins >= matchCfg.wins;
                updateUI();
            }
        }

        function updateAttack(attacker, defender, dt) {
            if (attacker.cooldown > 0) attacker.cooldown = Math.max(0, attacker.cooldown - dt);
            if (attacker.hitFlash > 0) attacker.hitFlash = Math.max(0, attacker.hitFlash - dt);
            if (attacker.hitFx > 0) attacker.hitFx = Math.max(0, attacker.hitFx - dt);
            attacker.comboT += dt;
            if (attacker.tauntT > 0) attacker.tauntT = Math.max(0, attacker.tauntT - dt);
            if (attacker.tauntCd > 0) attacker.tauntCd = Math.max(0, attacker.tauntCd - dt);
            if (attacker.kickCd > 0) attacker.kickCd = Math.max(0, attacker.kickCd - dt);
            if (attacker.gunCd > 0) attacker.gunCd = Math.max(0, attacker.gunCd - dt);
            if (attacker.gunT > 0) attacker.gunT = Math.max(0, attacker.gunT - dt);
            if (attacker.gunReload > 0 && attacker.gunT <= 0) { attacker.gunReload = Math.max(0, attacker.gunReload - dt); if (attacker.gunReload === 0) attacker.gunAmmo = GUN_MAG; }
            if (attacker.inkCd > 0) attacker.inkCd = Math.max(0, attacker.inkCd - dt);
            if (attacker.blinkCd > 0) attacker.blinkCd = Math.max(0, attacker.blinkCd - dt);
            if (attacker.flurryCd > 0) attacker.flurryCd = Math.max(0, attacker.flurryCd - dt);
            if (attacker.cloneCd > 0) attacker.cloneCd = Math.max(0, attacker.cloneCd - dt);
            if (attacker.invisCd > 0) attacker.invisCd = Math.max(0, attacker.invisCd - dt);
            if (attacker.healCd > 0) attacker.healCd = Math.max(0, attacker.healCd - dt);
            if (attacker.obstCd > 0) attacker.obstCd = Math.max(0, attacker.obstCd - dt);
            if (attacker.invisT > 0) attacker.invisT = (attacker.attacking || attacker.kicking || attacker.gunT > 0) ? 0 : Math.max(0, attacker.invisT - dt);   // 투명: 공격하면 바로 풀림
            if (attacker.inkT > 0) attacker.inkT = Math.max(0, attacker.inkT - dt);
            if (attacker.inked > 0) attacker.inked = Math.max(0, attacker.inked - dt);
            if (attacker.lackT > 0) { attacker.lackT = Math.max(0, attacker.lackT - dt); if (attacker.lackT === 0) attacker.lackMsg = ''; }
            if (attacker.shake > 0) attacker.shake = Math.max(0, attacker.shake - dt);
            if (attacker.stun > 0) attacker.stun = Math.max(0, attacker.stun - dt);
            if (attacker.dizzy > 0) attacker.dizzy = Math.max(0, attacker.dizzy - dt);
            if (attacker.flat > 0) { attacker.flat = Math.max(0, attacker.flat - dt); attacker.stun = Math.max(attacker.stun, attacker.flat); attacker.dizzy = Math.max(attacker.dizzy, attacker.flat); }   // 납작한 동안은 다른 기절에 덮여 짧아져도 못 움직임 · 못 때림
            if (attacker.blockFlash > 0) attacker.blockFlash = Math.max(0, attacker.blockFlash - dt);
            if (attacker.guardCd > 0) attacker.guardCd = Math.max(0, attacker.guardCd - dt);
            if (attacker.guardHold) {   // 가드를 누르고 있는 동안: 스테미나가 계속 닳고, 바닥나거나 기절하면 풀림
                if (gameOver || attacker.stun > 0 || attacker.stamina <= 0) endGuard(attacker);
                else { attacker.guard = GUARD_HOLD_TICK; attacker.stamina = Math.max(0, attacker.stamina - GUARD_DRAIN * dt); attacker.staminaDelay = STAMINA_REGEN_DELAY; }
            }
            if (attacker.guard > 0) {
                attacker.guard = Math.max(0, attacker.guard - dt);
                if (attacker.guard === 0) attacker.guardCd = GUARD_COOLDOWN * attacker.guardCdMul;
            }
            if (attacker.staminaDelay > 0) attacker.staminaDelay = Math.max(0, attacker.staminaDelay - dt);
            else attacker.stamina = Math.min(attacker.maxStamina, attacker.stamina + STAMINA_REGEN * dt);
            if (attacker.charging) {   // 힘조절 충전: 맞거나 기절하거나 가드하면 취소
                if (gameOver || attacker.stun > 0 || attacker.dizzy > 0 || attacker.guard > 0 || attacker.attacking || attacker.kicking) { attacker.charging = ''; attacker.chargeT = 0; }
                else attacker.chargeT = Math.min(CHARGE_TIME, attacker.chargeT + dt);
            }
            if (attacker.hold) {   // 점프 · 백열권 누르는 중: 맞거나 기절하거나 가드하거나 다른 행동을 하면 취소
                if (gameOver || attacker.stun > 0 || attacker.dizzy > 0 || attacker.guard > 0 || attacker.attacking || attacker.kicking || attacker.slideT > 0 || attacker.z > 0) { attacker.hold = ''; attacker.holdT = 0; }
                else {
                    attacker.holdT += dt;
                    if (attacker.hold === 'punch' && attacker.holdT >= FLURRY_HOLD) { attacker.hold = ''; attacker.holdT = 0; startFlurry(attacker); }
                }
            }
            bgm.charge(attacker === p1 ? 1 : 2, attacker.charging ? attacker.chargeT / CHARGE_TIME : -1);
            if (attacker.kicking) {
                attacker.kickT += dt;
                if (!attacker.kickHit && attacker.kickT >= KICK_HIT_TIME) {
                    attacker.kickHit = true;
                    if (!gameOver) resolveHit(attacker, defender, true);
                }
                if (attacker.kickT >= KICK_DURATION) {
                    attacker.kicking = false;
                    attacker.cooldown = KICK_COOLDOWN;
                }
            }
            if (!attacker.attacking) return;

            attacker.attackT += dt;
            if (!attacker.hitDone && attacker.attackT >= ATTACK_HIT_TIME) {
                attacker.hitDone = true;
                if (!gameOver) resolveHit(attacker, defender);
            }
            if (attacker.attackT >= ATTACK_DURATION) {
                attacker.attacking = false;
                attacker.cooldown = attacker.punchLanded ? 0 : ATTACK_COOLDOWN * attacker.atkCdMul;   // 맞혔으면 쿨타임 초기화
                attacker.punchLanded = false;
            }
        }

        function burstFx() {
            // 파편 24개: 색 종류(0 본색, 1 밝은색, 2 흰색)와 크기 배율을 섞어서 튀게
            return Array.from({ length: 24 }, (_, i) => ({
                a: (i / 24) * Math.PI * 2 + Math.random() * 0.5,
                s: 0.35 + Math.random() * 0.9,
                c: i % 3,
                k: 0.8 + Math.random() * 1.2
            }));
        }

        // 발차기에 맞아 밀려나는 중: 점점 느려지며 이동, 벽에 부딪히면 2초 기절
        function updateSlide(p, dt) {
            if (p.slideT <= 0) return;
            const speed = KICK_SLIDE_SPEED * (p.slideMul || 1) * (p.slideT / KICK_SLIDE_TIME);
            const nx = p.x + p.slideDX * speed * dt;
            const ny = p.y + p.slideDY * speed * dt;
            const hitWall = speed > 120 &&
                ((Math.abs(p.slideDX) > 0.3 && blockedAt(nx, p.y)) ||
                 (Math.abs(p.slideDY) > 0.3 && blockedAt(p.x, ny)));
            tryMove(p, nx, ny);
            if (hitWall) {
                p.slideT = 0;
                p.dizzy = KICK_WALL_STUN;
                p.stun = KICK_WALL_STUN;
                p.shake = SHAKE_DURATION;
                p.hitFx = HIT_FX_TIME;
                p.fx = burstFx();
                p.vz = Math.max(p.vz, LAUNCH_VEL * 0.5);
                p.z = Math.max(p.z, 0.01);
            } else {
                p.slideT = Math.max(0, p.slideT - dt);
            }
        }

        function updateAir(p, dt) {
            if (p.jumpCd > 0) p.jumpCd = Math.max(0, p.jumpCd - dt);
            if (obstacles.length && p.vz <= 0 && p.z < OBST_H - 0.5) pushOutOfBoxes(p);   // 박스 위에서 내려올 때 박스에 끼이지 않게 (솟아오르는 중 vz > 0 은 제외)
            const fl = boxFloor(p.x, p.y);   // 박스 위에 있으면 바닥이 박스 윗면 (거기 서 있는 동안은 jumping 으로 취급해 공격 · 이동이 막히지 않게)
            if (p.z <= fl && p.vz <= 0) { if (fl > 0) { p.z = fl; p.jumping = true; } else { p.shoryuAir = false; } return; }   // 승룡권 시전자 공중 표시는 착지하면 해제
            p.vz -= GRAVITY * dt;
            p.z += p.vz * dt;
            if (p.z <= fl) { p.z = fl; p.vz = 0; p.jumping = fl > 0; p.noGuard = false; }
        }
        function updateStomp(a, d) {   // 점프해서 내려오다 상대 머리를 밟으면 피해 + 위로 튀어 오름 (한 번 뛸 때 한 번만)
            if (a.z <= 0) { a.stompDone = false; return; }
            if (gameOver || a.stompDone || !a.jumping || a.vz >= 0) return;
            const gap = a.z - d.z;
            if (gap <= 0 || gap > STOMP_H || d.dashT > 0 || d.z > AIR_HIT_MAX_Z || Math.hypot(d.x - a.x, d.y - a.y) > MIN_PLAYER_DIST) return;
            a.stompDone = true; a.vz = JUMP_VEL * STOMP_BOUNCE;
            if (!tutorial) d.hp = Math.max(0, d.hp - STOMP_DAMAGE * (roundTime <= DOUBLE_DMG_TIME ? 2 : 1));
            a.combo = (a.combo > 0 && a.comboT < COMBO_WINDOW) ? a.combo + 1 : 1;
            a.comboT = 0;
            d.combo = 0;
            d.hitFlash = 0.3; d.shake = SHAKE_DURATION; d.hitFx = HIT_FX_TIME;
            bgm.sfx('hit');
            d.fx = burstFx();
            updateUI();
            if (d.hp <= 0) {
                gameOver = true;
                winner = a;
                a.wins++;
                matchOver = a.wins >= matchCfg.wins;
                updateUI();
            }
        }

        function updateSea(p, dt) {   // 콜로세움: 원형 바닥 밖으로 나가면 바다에 빠져 피해를 받고, 잠시 뒤 시작 위치로 돌아옴
            if (!arena) return;
            if (p.fallT > 0) {
                p.fallT = Math.max(0, p.fallT - dt);
                p.stun = Math.max(p.stun, p.fallT);   // 빠져 있는 동안 공격 · 기술 불가
                if (!tutorial && !gameOver) {   // 빠져 있는 동안 SEA_TIME 에 걸쳐 SEA_DAMAGE 만큼 서서히 피해
                    p.hp = Math.max(0, p.hp - SEA_DAMAGE / SEA_TIME * dt);
                    updateUI();
                    if (p.hp <= 0) {
                        const o = p === p1 ? p2 : p1;
                        gameOver = true;
                        winner = o;
                        o.wins++;
                        matchOver = o.wins >= matchCfg.wins;
                        updateUI();
                        return;
                    }
                }
                if (p.fallT <= 0 && !gameOver) { p.x = p.startX; p.y = p.startY; p.angle = p.startAngle; p.stun = 0; }
                return;
            }
            if (gameOver || p.z > 0.5 || Math.hypot(p.x - ARENA_C, p.y - ARENA_C) <= ARENA_R) return;   // 점프로 떠 있는 동안은 안 빠짐
            p.fallT = SEA_TIME;
            p.attacking = false; p.attackT = 0; p.kicking = false; p.kickT = 0; p.charging = ''; p.slideT = 0; p.dashT = 0; p.guard = 0; p.guardHold = '';
            p.shake = SHAKE_DURATION;
            bgm.sfx('hit');
        }

        function updateUI() {
            p1HpEl.style.width = (p1.hp / p1.maxHp * 100) + '%';
            p2HpEl.style.width = (p2.hp / p2.maxHp * 100) + '%';
            // 최대 체력이 늘면 체력 칸(10당 1칸)이 늘어나 바가 길어짐. 한 줄을 넘으면 칸이 좁아짐
            for (const [id, pl] of [['p1-hp-bg', p1], ['p2-hp-bg', p2]]) {
                const bg = document.getElementById(id);
                bg.style.width = Math.min(100, 62 * pl.maxHp / 100) + '%';
                bg.style.setProperty('--seg', (1000 / pl.maxHp) + '%');
            }
            for (const [id, pl] of [['p1-cards', p1], ['p2-cards', p2]]) {
                const el = document.getElementById(id);
                const key = pl.cards.map(c => c.nm).join(',');
                if (el.dataset.key === key) continue;   // 바뀐 때만 다시 그림
                el.dataset.key = key;
                el.innerHTML = '';
                const groups = [];
                for (const c of pl.cards) {
                    const g = groups.find(x => x.c === c);
                    if (g) g.n++; else groups.push({ c, n: 1 });
                }
                for (const g of groups) {
                    const d = document.createElement('div');
                    d.className = 'cicon' + (g.c.kind === 'skill' ? ' skill' : '') + ' r-' + g.c.r;
                    d.title = RARITY[g.c.r].nm + ' ' + cardName(g.c);
                    d.textContent = g.c.ic;
                    if (g.n > 1) { const n = document.createElement('span'); n.className = 'n'; n.textContent = 'x' + g.n; d.appendChild(n); }
                    el.appendChild(d);
                }
            }
            for (const [id, pl] of [['p1-pips', p1], ['p2-pips', p2]]) {
                const pips = document.getElementById(id).children;
                for (let i = 0; i < pips.length; i++) pips[i].classList.toggle('on', i < pl.wins);
            }
            document.getElementById('round-label').textContent = practice ? 'PRACTICE' : 'ROUND ' + round;
            const tEl = document.getElementById('round-timer');
            const sec = Math.max(0, Math.ceil(roundTime));
            const dbl = roundTime <= DOUBLE_DMG_TIME;
            const label = practice ? '∞' : sec + (dbl ? ' x2' : '');
            if (tEl.textContent !== label) tEl.textContent = label;
            tEl.classList.toggle('low', sec <= 10);
            tEl.classList.toggle('dbl', dbl && sec > 10);
        }

        function updateStamina() {
            p1StEl.style.width = (p1.stamina / p1.maxStamina * 100) + '%';
            p2StEl.style.width = (p2.stamina / p2.maxStamina * 100) + '%';
            for (const [id, pl] of [['p1-st-bg', p1], ['p2-st-bg', p2]]) {   // 최대 스테미나가 늘면 바도 길어짐
                const w = Math.min(100, 62 * pl.maxStamina / 100) + '%';
                const bg = document.getElementById(id);
                if (bg.style.width !== w) bg.style.width = w;
            }
            p1StEl.classList.toggle('low', p1.stamina < (p1.gun ? GUN_COST : ATTACK_COST));
            p2StEl.classList.toggle('low', p2.stamina < (p2.gun ? GUN_COST : ATTACK_COST));
        }

        // ===== 기술 아이콘 (화면 밖, 쿨타임 표시) =====
        // # 외곽선, o 본체색, l 밝은색, w 흰색 (12x12)
        const SKILL_DEFS = [
            { total: ATTACK_DURATION + ATTACK_COOLDOWN, cost: ATTACK_COST, art: [   // 공격
                "............",
                "..########..",
                ".#llooooooo#",
                ".#l#o#o#o#o#",
                ".#ooooooooo#",
                ".#ooooooooo#",
                "..#ooooooo#.",
                "..#oooooo#..",
                "..#oooooo#..",
                "..########..",
                "............",
                "............"
            ] },
            { total: GUARD_TIME + GUARD_COOLDOWN, cost: GUARD_COST, art: [         // 가드
                "............",
                ".##########.",
                ".#wlloooooo#",
                ".#llloooooo#",
                ".#ooooooooo#",
                ".#ooooooooo#",
                ".#ooooooooo#",
                "..#ooooooo#.",
                "...#ooooo#..",
                "....#ooo#...",
                ".....###....",
                "............"
            ] },
            { total: KICK_RECHARGE, cost: KICK_COST, art: [        // 발차기
                "............",
                "..####......",
                "..#oo#..ww..",
                "..#oo#.www..",
                "..#oo#..ww..",
                "..#oo####...",
                "..#ooooooo#.",
                "..#ooooollo#",
                "..##########",
                "............",
                "............",
                "............"
            ] },
            { total: DASH_CD, cost: DASH_COST, art: [                             // 대쉬 (카드를 얻으면 나타남)
                "............",
                ".#.....#....",
                ".##....##...",
                ".#o#...#o#..",
                ".#oo#..#oo#.",
                ".#ooo#.#ooo#",
                ".#oo#..#oo#.",
                ".#o#...#o#..",
                ".##....##...",
                ".#.....#....",
                "............",
                "............"
            ] },
            { total: TAUNT_CD, cost: 0, art: [                                    // 도발 (카드를 얻으면 나타남)
                "............",
                ".##########.",
                ".#wwwwwwww#.",
                ".#wowowowo#.",
                ".#wwwwwwww#.",
                ".##########.",
                "...###......",
                "....##......",
                ".....#......",
                "............",
                "............",
                "............"
            ] },
            { total: GUN_COOLDOWN, cost: GUN_COST, art: [                         // 총 (카드를 얻으면 나타남)
                "............",
                "............",
                ".##########.",
                ".#oooooooo#.",
                ".#llooooooo#",
                ".##########.",
                ".#ooo#......",
                ".#ooo#......",
                ".#ooo#......",
                ".#ooo#......",
                ".#####......",
                "............"
            ] },
            { total: INK_COOLDOWN, cost: INK_COST, art: [                         // 오징어 먹물 (카드를 얻으면 나타남)
                "............",
                ".....##.....",
                "....#oo#....",
                "..#.#ol#.#..",
                ".#o##oo##o#.",
                "..##oooo##..",
                "....#ww#....",
                "...#oooo#...",
                "...#o##o#...",
                "..#o#..#o#..",
                "..#o#..#o#..",
                "...#....#..."
            ] },
            { total: KI_COOLDOWN, cost: KI_COST, art: [                           // 장풍 (카드를 얻으면 나타남)
                "............",
                "....####....",
                "..##wwww##..",
                "..#wwllww#..",
                ".#wwllllww#.",
                ".#wlloolww#.",
                ".#wlloolww#.",
                ".#wwllllww#.",
                "..#wwllww#..",
                "..##wwww##..",
                "....####....",
                "............"
            ] },
            { total: SHORYU_TIME, cost: 0, art: [                                 // 승룡권 (카드를 얻으면 나타남)
                "............",
                ".....##.....",
                "....#ll#....",
                "...#llll#...",
                "..##.oo.##..",
                "....#oo#....",
                "..########..",
                ".#oooooooo#.",
                ".#oooooooo#.",
                ".#oooooooo#.",
                "..########..",
                "............"
            ] },
            { total: JUMP_CD, cost: JUMP_COST, art: [                                   // 점프 (카드를 얻으면 나타남)
                "............",
                ".....##.....",
                "....#oo#....",
                "...#oooo#...",
                "..#oooooo#..",
                "....#oo#....",
                "....#oo#....",
                "............",
                "..########..",
                ".#llllllll#.",
                "..########..",
                "............"
            ] },
            { total: BLINK_CD, cost: BLINK_COST, art: [                                  // 순간이동 (카드를 얻으면 나타남)
                "............",
                ".#...#......",
                ".o#..o#.....",
                ".oo#.oo#....",
                ".ooo#ooo#...",
                ".oooooooo#..",
                ".ooo#ooo#...",
                ".oo#.oo#....",
                ".o#..o#.....",
                ".#...#......",
                "............",
                "............"
            ] },
            { total: FLURRY_CD, cost: FLURRY_COST, art: [                                // 백열권 (카드를 얻으면 나타남)
                "............",
                "............",
                "............",
                "....#######.",
                "l...#ooooo#.",
                "ll..#oloooo#",
                "....#ooooo#.",
                "ll..#ooooo#.",
                "l...#ooooo#.",
                "....#######.",
                "............",
                "............"
            ] },
            { total: CLONE_CD, cost: CLONE_COST, art: [
                "............",
                "..##....##..",
                ".#oo#..#ll#.",
                ".#oo#..#ll#.",
                "..##....##..",
                ".#oo#..#ll#.",
                "#oooo##llll#",
                "#oooo##llll#",
                ".#oo#..#ll#.",
                ".#..#..#..#.",
                "............",
                "............"
            ] },
            { total: INVIS_CD, cost: INVIS_COST, art: [
                "............",
                "....####....",
                "...#llll#...",
                "..#llllll#..",
                "..#l#ll#l#..",
                "..#llllll#..",
                "..#llllll#..",
                "..#llllll#..",
                "..#l#ll#l#..",
                "...#.##.#...",
                "............",
                "............"
            ] },
            { total: HEAL_CD, cost: HEAL_COST, art: [
                "............",
                "....####....",
                "....#oo#....",
                "....#oo#....",
                ".####oo####.",
                ".#oooooooo#.",
                ".#oooooooo#.",
                ".####oo####.",
                "....#oo#....",
                "....#oo#....",
                "....####....",
                "............"
            ] },
            { total: OBST_CD, cost: OBST_COST, art: [
                "............",
                "...######...",
                "..#oooooo#..",
                "..#oloooo#..",
                "..#oloooo#..",
                "..#oloooo#..",
                "..#oloooo#..",
                "..#oloooo#..",
                "..#oloooo#..",
                "..#oooooo#..",
                "...######...",
                "............"
            ] }
        ];
        const SKILL_LABELS = [['[Z]', '[X]', '[C]', '[↑↑]', '[V]', '[Z]', '[V]', '[V]', '[V]', '[C]', '[V]', '[Z]', '[V]', '[V]', '[V]', '[V]'], ['[.]', '[/]', "[']", '[↑↑]', '[;]', '[.]', '[;]', '[;]', '[;]', "[']", '[;]', '[.]', '[;]', '[;]', '[;]', '[;]']];   // 점프(9)는 발차기 키 · 백열권(11)은 공격 키를 씀

        function makeSkillArt(rows, color) {
            const c = document.createElement('canvas');
            c.width = 12; c.height = 12;
            const g = c.getContext('2d');
            const col = { '#': '#000', o: color, l: shade(color, 0.45), w: '#fff' };
            rows.forEach((row, y) => Array.from(row).forEach((ch, x) => {
                if (col[ch]) { g.fillStyle = col[ch]; g.fillRect(x, y, 1, 1); }
            }));
            return c;
        }

        const skillSlots = [];
        [[p1, 'p1-skills', 0], [p2, 'p2-skills', 1]].forEach(([pl, id, pi]) => {
            const box = document.getElementById(id);
            SKILL_DEFS.forEach((def, i) => {
                const slot = document.createElement('div');
                slot.className = 'skill';
                const cv = document.createElement('canvas');
                cv.width = 48; cv.height = 48;
                const lb = document.createElement('div');
                lb.textContent = SKILL_LABELS[pi][i];
                slot.append(cv, lb);
                // 아이콘을 누르면 키보드로 누른 것과 똑같이 기술 발동 (0 공격/총, 1 가드, 2 발차기, 3 대쉬, 4 도발, 9 점프)
                slot.addEventListener('pointerdown', e => {
                    e.preventDefault();
                    if (!started || paused || (aiMode && pl === aiSelf)) return;   // 1인용의 AI 쪽 칸은 무시
                    if (window.NET && NET.on && NET.icon(pl, i, e)) return;   // 온라인: 내 칸만, 손님은 방장에게 전달
                    if (!gameOver) cdBeep(pl, i === 0 ? 'attack' : i === 1 ? 'guard' : i === 2 ? 'kick' : 'special');
                    if (i === 0) pressAction(pl, 'punch', 'ptr');
                    else if (i === 1) startGuard(pl, 'ptr');
                    else if (i === 2) pressAction(pl, 'kick', 'ptr');
                    else if (i === 3) tryDash(pl);
                    else if (i === 4) startTaunt(pl);
                    else if (i === 6) startInk(pl);
                    else if (i === 7) { startKi(pl); pl.kiPtr = e.pointerId; }   // 누르고 있으면 기를 모으고, 그 손가락을 떼면 발사
                    else if (i === 8) tryShoryu(pl);
                    else if (i === 9) tryJump(pl);
                    else if (i === 10) { startBlink(pl); pl.blinkPtr = e.pointerId; }   // 누르고 있으면 빨간 원이 멀어지고, 그 손가락을 떼면 이동
                    else if (i === 11) startFlurry(pl);
                    else if (i === 12) startClone(pl);
                    else if (i === 13) startInvis(pl);
                    else if (i === 14) { startHeal(pl); pl.healPtr = e.pointerId; }   // 누르고 있는 동안 마시고, 그 손가락을 떼면 취소
                    else if (i === 15) startObst(pl);
                });
                box.appendChild(slot);
                if (i >= 3) slot.style.display = 'none';   // 카드를 얻기 전에는 숨김
                skillSlots.push({ el: slot, player: pl, i, def, ctx: cv.getContext('2d'), art: makeSkillArt(def.art, pl.color), gunArt: i === 0 ? makeSkillArt(SKILL_DEFS[5].art, pl.color) : null, last: '' });
            });
        });

        // 다시 쓸 수 있기까지 남은 시간(초). 0 = 사용 가능(스테미나는 별도)
        function skillRemain(p, i) {
            const act = p.attacking ? ATTACK_DURATION - p.attackT : p.kicking ? KICK_DURATION - p.kickT : 0;
            if (i === 1) {   // 가드: 공격/발차기 동작이 끝나야 함, 쓰고 나면 가드 쿨타임
                return Math.max(act, p.stun, p.guardCd, p.guardHold ? 0 : p.guard > 0 ? p.guard + GUARD_COOLDOWN * p.guardCdMul : 0);
            }
            const busy = p.attacking ? act + ATTACK_COOLDOWN * p.atkCdMul : p.kicking ? act + KICK_COOLDOWN : p.cooldown;
            const r = Math.max(busy, p.stun, p.guard);
            if (i === 3) return Math.max(p.dashT, p.dashCd);   // 대쉬 재사용 대기
            if (i === 9) return p.jumpCd;   // 점프 재사용 대기
            if (i === 4) return p.tauntCd;
            if (i === 5) return Math.max(r, p.gunCd, p.gunReload);
            if (i === 6) return Math.max(r, p.inkCd);
            if (i === 7) return Math.max(r, p.kiCd);
            if (i === 8) return Math.max(r, p.cooldown);
            if (i === 10) return Math.max(r, p.blinkCd);
            if (i === 11) return Math.max(r, p.flurryCd);
            if (i === 12) return Math.max(r, p.cloneCd);
            if (i === 13) return Math.max(r, p.invisCd);
            if (i === 14) return Math.max(r, p.healCd);
            if (i === 15) return Math.max(r, p.obstCd);
            return i === 2 ? Math.max(r, p.kickCd) : r;   // 공격/발차기는 후딜 쿨다운 공유, 가드 중에는 불가
        }

        function updateSkills() {
            for (const s of skillSlots) {
                const pl = s.player;
                if (s.i === 5) {   // 총은 따로 칸을 만들지 않고 주먹 아이콘 자리(0번)를 대신함
                    if (s.el.style.display !== 'none') s.el.style.display = 'none';
                    continue;
                }
                if (s.i >= 3) {
                    const has = s.i === 3 ? (pl.canDash || pl.canSlash) : s.i === 6 ? pl.canInk : s.i === 7 ? pl.canKi : s.i === 8 ? pl.canShoryu : s.i === 9 ? pl.canJump : s.i === 10 ? pl.canBlink : s.i === 11 ? pl.canFlurry : s.i === 12 ? pl.canClone : s.i === 13 ? pl.canInvis : s.i === 14 ? pl.canHeal : s.i === 15 ? pl.canObst : pl.canTaunt;
                    const vis = has ? '' : 'none';
                    if (s.el.style.display !== vis) { s.el.style.display = vis; s.last = ''; }
                    if (!has) continue;
                }
                const gunMode = s.i === 0 && pl.gun;   // 총을 얻으면 주먹 아이콘 자리가 총 아이콘으로 바뀜
                const remain = skillRemain(s.player, gunMode ? 5 : s.i);
                const total = gunMode ? (pl.gunReload > 0 ? GUN_RELOAD_TIME : GUN_COOLDOWN) : s.i === 0 ? ATTACK_DURATION + ATTACK_COOLDOWN * pl.atkCdMul
                    : s.i === 1 ? GUARD_TIME + GUARD_COOLDOWN * pl.guardCdMul
                    : s.i === 2 ? KICK_RECHARGE * pl.kickCdMul
                    : s.i === 5 ? GUN_COOLDOWN
                    : s.i === 6 ? INK_COOLDOWN
                    : s.i === 7 ? KI_COOLDOWN
                    : s.i === 8 ? SHORYU_TIME
                    : s.i === 9 ? JUMP_CD
                    : s.i === 10 ? BLINK_CD
                    : s.i === 11 ? FLURRY_CD
                    : s.i === 12 ? CLONE_CD
                    : s.i === 13 ? INVIS_CD
                    : s.i === 14 ? HEAL_CD
                    : s.i === 15 ? OBST_CD
                    : s.i === 3 ? (pl.canSlash ? SLASH_CD : DASH_CD)
                    : TAUNT_CD;
                const lack = s.i === 4 ? false : s.i === 8
                    ? (pl.shoryuReady <= 0 || pl.stamina < pl.maxStamina * SHORYU_COST || pl.z > 0)   // 한 바퀴를 돌아야 준비됨 / 스테미나 부족
                    : s.i === 9
                    ? (pl.stamina < JUMP_COST || pl.z > 0 || pl.stun > 0 || pl.dizzy > 0 || pl.slideT > 0 || pl.guard > 0)   // 스테미나 부족 / 공중 / 점프 불가 상태
                    : s.i === 3
                    ? (pl.stamina < (pl.canSlash ? SLASH_COST : DASH_COST) || pl.z > 0 || pl.stun > 0 || pl.dizzy > 0 || pl.slideT > 0 || pl.guard > 0)   // 스테미나 부족 / 대쉬 불가 상태
                    : (pl.stamina < (gunMode ? GUN_COST : s.i === 0 && pl.knife ? s.def.cost + KNIFE_COST : s.def.cost) || (s.i !== 1 && pl.z > 0 && !pl.jumping));
                // 쿨타임이 0.0이 되면 숫자 0.0 을 0.5초 더 보여 주고 사라짐
                if (remain > 0) { s.hadCd = true; s.zeroT = -1; }
                else if (s.hadCd) { if (s.zeroT < 0) s.zeroT = gameTime; if (gameTime - s.zeroT >= 0.5) s.hadCd = false; }
                const showZero = remain <= 0 && s.hadCd;
                const key = remain.toFixed(1) + (lack ? 'L' : '') + (gunMode ? 'G' : '') + (showZero ? 'Z' : '');
                if (key === s.last) continue;   // 변화 없으면 다시 그리지 않음
                s.last = key;
                const g = s.ctx;
                g.imageSmoothingEnabled = false;
                g.fillStyle = '#2b2b33';
                g.fillRect(0, 0, 48, 48);
                g.drawImage(gunMode ? s.gunArt : s.art, 0, 0, 48, 48);
                if (remain > 0) {
                    const f = Math.min(1, remain / total);
                    g.fillStyle = 'rgba(0,0,0,0.68)';
                    g.fillRect(0, 0, 48, Math.round(48 * f));
                    const t = remain.toFixed(1);
                    g.font = '12px "Press Start 2P", monospace';
                    g.textAlign = 'center';
                    g.fillStyle = '#000'; g.fillText(t, 25, 29);
                    g.fillStyle = '#fff'; g.fillText(t, 24, 28);
                } else {
                    if (lack) {   // 스테미나 부족
                        g.fillStyle = 'rgba(0,0,0,0.55)';
                        g.fillRect(0, 0, 48, 48);
                    }
                    if (showZero) {   // 막 쿨타임이 끝남: 0.0 을 잠깐 더 표시
                        g.font = '12px "Press Start 2P", monospace';
                        g.textAlign = 'center';
                        g.fillStyle = '#000'; g.fillText('0.0', 25, 29);
                        g.fillStyle = '#fff'; g.fillText('0.0', 24, 28);
                    }
                }
            }
        }

        function resetGame() {
            for (const p of [p1, p2]) {
                p.x = p.startX; p.y = p.startY; p.angle = p.startAngle;
                p.hp = p.maxHp;
                p.attacking = false; p.attackT = 0; p.hitDone = false;
                p.cooldown = 0; p.hitFlash = 0; p.shake = 0; p.punchHand = 0;
                p.fallT = 0; p.z = 0; p.vz = 0; p.stun = 0; p.jumping = false; p.tauntT = 0; p.tauntCd = 0;
                p.guard = 0; p.guardCd = 0; p.guardHold = ''; p.blockFlash = 0; p.dizzy = 0; p.flat = 0; p.flatMax = 0; p.hitFx = 0;
                p.kicking = false; p.kickT = 0; p.kickHit = false; p.slideT = 0; p.kickCd = 0; p.gunCd = 0; p.gunT = 0; p.gunAmmo = GUN_MAG; p.gunReload = 0; p.inkCd = 0; p.inkT = 0; p.inked = 0; p.lackT = 0;
                p.stamina = p.maxStamina; p.staminaDelay = 0;
                p.combo = 0; p.comboT = 99; p.punchLanded = false; p.dashT = 0; p.dashCd = 0; p.jumpCd = 0; p.stompDone = false;
                p.charging = ''; p.chargeT = 0; p.hold = ''; p.holdT = 0; p.dmgMul = 1;
                p.kiOn = false; p.kiT = 0; p.healOn = false; p.healT = 0; p.kiCd = 0; p.blinkCd = 0; p.blinkOn = false; p.blinkD = 0; p.ghostT = 0; p.flurryOn = false; p.flurryT = 0; p.flurryHits = 0; p.flurryCd = 0; p.cloneCd = 0; p.invisCd = 0; p.invisT = 0; p.healCd = 0; p.obstCd = 0;
                aiShoryuCd = 3; aiFreezeT = 0; aiDetourT = 0; aiDetourHold = 0; aiSpinOn = false; p.spinAcc = 0; p.spinIdle = 0; p.shoryuReady = 0; p.shoryuOn = false; p.shoryuT = 0; p.noGuard = false;
            }
            kiBalls.length = 0;
            clearTemp();   // 분신 · 장애물도 라운드마다 없앰
            gameOver = false;
            winner = null;
            roundEndT = 0;
            roundIntroT = 0;
            introPick = false;
            roundTime = matchCfg.time + (round === 1 ? ROUND1_BONUS_TIME : 0);
            timeUp = false;
            burnT = 0; shoryuFxT = 0;
            updateUI();
            updateStamina();
        }

        // ===== 라운드 카드: 라운드에서 진 사람이 능력 카드 한 장을 골라 얻음 =====
        const newSp = p => p.canClone || p.canInvis || p.canHeal || p.canObst;   // 분신 · 투명 · 힐 · 장애물 설치도 특수공격 키를 혼자 씀
        const hasSpecial = p => p.canTaunt || p.canInk || p.canKi || p.canShoryu || p.canBlink || newSp(p);   // 도발 · 먹물은 특수공격 키를 혼자 씀 (점프 · 백열권은 발차기 · 공격 키를 써서 특수공격 키와 함께 가질 수 있음. 장풍 + 점프는 합치면 승룡권)
        const CARD_POOL = [
            { ic: 'HP', r: 'rare', kind: 'stat', nm: '튼튼한 몸', ds: '최대 체력 +2.5칸', tag: '체력+2.5칸',
              apply: p => { p.maxHp += 25; } },
            { ic: 'STA', r: 'normal', kind: 'stat', nm: '스테미나 증가', ds: '최대 스테미나 +30', tag: 'ST+30',
              apply: p => { p.maxStamina += 30; } },
            { ic: 'RANGE', r: 'normal', kind: 'stat', nm: '긴 사정거리', ds: '주먹 · 발차기 · 칼 사정거리 +20%', tag: '사거리+20%',
              apply: p => { p.reachMul = Math.min(1.8, p.reachMul * 1.2); } },
            { ic: 'JUMP', r: 'rare', kind: 'skill', blocked: p => p.canShoryu || p.canCharge, nm: '점프', ds: '발차기 키(1P C / 2P \')를 꾹 누르면 누른 만큼 높이 점프 (톡 누르면 평소 발차기)<br>공중에서도 이동 · 공격 가능<br>내려오며 상대 머리를 밟으면 체력 1칸 피해<br>스테미나 25 · 쿨타임 3초 · 장풍과 합치면 승룡권 · 힘조절과 같이 못 씀', tag: '점프', once: true,
              apply: p => { p.canJump = true; } },
            { ic: 'DASH', r: 'normal', kind: 'skill', blocked: p => p.canSlash, nm: '대쉬', ds: '앞 방향키 두 번(1P W / 2P ↑)으로 돌진<br>돌진 중 무적 · 부딪히면 체력 0.5칸 피해<br>스테미나 25 · 쿨타임 1초', tag: '대쉬', once: true,
              apply: p => { p.canDash = true; } },
            { ic: 'TAUNT', r: 'dung', kind: 'skill', nm: '도발', ds: '특수키(1P V / 2P ;)로 도발<br>상대 화면에 EZ 말풍선', tag: '도발', once: true,
              blocked: hasSpecial,
              apply: p => { p.canTaunt = true; } },
            { ic: 'GUN', r: 'legend', kind: 'skill', blocked: p => p.knife || p.canFlurry, nm: '총', ds: '공격이 총으로 바뀜<br>멀리서도 즉시 체력 2칸 피해 · 가드로 막힘<br>스테미나 25 · 쿨타임 1.5초', tag: '총', once: true,
              apply: p => { p.gun = true; } },
            { ic: 'KNIFE', r: 'epic', kind: 'skill', blocked: p => p.gun || p.canSlash || p.canFlurry || p.canCharge, nm: '칼', ds: '단검으로 공격<br>피해 체력 0.5칸 증가 · 사거리 +6<br>대신 스테미나 5 더 듦', tag: '칼', once: true,
              apply: p => { p.knife = true; } },
            { ic: 'INK', r: 'rare', kind: 'skill', blocked: hasSpecial, nm: '오징어 먹물', ds: '특수키(1P V / 2P ;)로 먹물 발사<br>맞은 적은 4초간 화면이 가려짐<br>스테미나 30 · 쿨타임 7초', tag: '먹물', once: true,
              apply: p => { p.canInk = true; } },
            { ic: 'KI', r: 'legend', kind: 'skill', blocked: p => p.canTaunt || p.canInk || p.canShoryu || p.canBlink || newSp(p), nm: '장풍', ds: '특수키(1P V / 2P ;)를 누르면 충전, 떼면 발사<br>절반 이상: 체력 1칸 피해 + 잠깐 기절<br>최대: 넉백 + 긴 기절 (기가 느림) · 가드 불가<br>스테미나 25 · 쿨타임 5초', tag: '장풍', once: true,
              apply: p => { p.canKi = true; } },
            { ic: 'SHORYU', r: 'fusion', kind: 'skill', hidden: true, has: p => p.canShoryu, conflict: p => p.canTaunt || p.canInk || p.canBlink || newSp(p), blocked: p => !(p.canKi && p.canJump) || p.canShoryu, nm: '승룡권', ds: '히든 · 장풍 + 점프가 합쳐짐<br>한 방향으로 한 바퀴 돌고 특수키 → 4단 어퍼컷 (체력 4칸 피해 · 느리게 올라감)<br>착지할 때까지 가드 불가 · 첫 타가 가드되면 실패<br>스테미나 65%', tag: '승룡권', once: true,
              apply: p => { p.canShoryu = true; p.canKi = false; p.kiOn = false; p.canJump = false; } },   // 장풍 + 점프가 합쳐져 승룡권이 됨 (카드는 목록에 남아 있어 다시 못 고름)
            { ic: 'DSLASH', r: 'fusion', kind: 'skill', hidden: true, has: p => p.canSlash, conflict: p => p.gun || p.canFlurry, blocked: p => !(p.canDash && p.knife) || p.canSlash, nm: '돌진베기', ds: '히든 · 대쉬 + 칼이 합쳐짐<br>앞 방향키 두 번으로 베며 돌진 (상대 통과)<br>돌진 중 무적 · 체력 1칸 피해 + 1.5초 기절 · 가드로 막힘<br>스테미나 60 · 쿨타임 8초', tag: '돌진베기', once: true,
              apply: p => { p.canSlash = true; p.canDash = false; p.knife = true; } },   // 대쉬 + 칼이 합쳐져 돌진베기가 됨 (칼은 계속 들고 있음)
            { ic: 'CHARGE', r: 'epic', kind: 'skill', blocked: p => p.cards.some(c => c.ic === 'KNIFE') || p.canJump || p.canFlurry, nm: '힘조절', ds: '공격 · 발차기 키를 누르면 충전, 떼면 발동<br>살짝: ×1 · 최대: ×3<br>×2 이상이면 1초 기절 (최대 충전 1.5초) · 총 · 칼 · 점프 · 백열권 카드와 같이 못 씀', tag: '힘조절', once: true,
              apply: p => { p.canCharge = true; } },
            { ic: 'BLINK', r: 'rare', kind: 'skill', blocked: hasSpecial, nm: '순간이동', ds: '특수키(1P V / 2P ;)를 누르고 있으면 바닥의 빨간 원이 앞으로 멀어짐<br>키를 떼면 그 위치로 순간이동<br>벽 · 기둥 앞에서 원이 멈춤 (상대는 통과)<br>스테미나 10~35 · 쿨타임 1~5초 (멀리 갈수록 증가)', tag: '순간이동', once: true,
              apply: p => { p.canBlink = true; } },
            { ic: 'FLURRY', r: 'epic', kind: 'skill', blocked: p => p.gun || p.knife || p.canCharge, nm: '백열권', ds: '공격 키(1P Z / 2P .)를 꾹 누르면 1초간 주먹을 연타 (짧게 누르면 평소 주먹)<br>맞아도 상대는 기절하지 않아 가드 가능 · 다 맞으면 체력 3칸 피해<br>쓰는 동안 제자리(회전만 가능) · 가드로 막히면 끊기지만 기절은 안 함<br>스테미나 35 · 쿨타임 8초 · 총 · 칼 · 힘조절과 같이 못 씀', tag: '백열권', once: true,
              apply: p => { p.canFlurry = true; } },
            { ic: 'CLONE', r: 'epic', kind: 'skill', blocked: hasSpecial, nm: '분신', ds: '특수키(1P V / 2P ;)로 내 옆에 분신을 소환<br>분신은 나를 무시하고 상대만 쫓아가 주먹 공격 (피해 0.5칸)<br>체력 2칸 · 10초 뒤 사라짐 · 상대 공격이 닿으면 분신이 대신 맞음<br>스테미나 40 · 쿨타임 15초', tag: '분신', once: true,
              apply: p => { p.canClone = true; } },
            { ic: 'INVIS', r: 'rare', kind: 'skill', blocked: hasSpecial, nm: '투명', ds: '특수키(1P V / 2P ;)로 3초간 상대 화면 · 미니맵에서 사라짐<br>공격하면 바로 다시 보임<br>스테미나 25 · 쿨타임 12초', tag: '투명', once: true,
              apply: p => { p.canInvis = true; } },
            { ic: 'HEAL', r: 'rare', kind: 'skill', blocked: hasSpecial, nm: '힐', ds: '특수키(1P V / 2P ;)를 꾹 누르는 동안 서서히 회복 (최대 3초 · 2칸)<br>떼거나 맞으면 거기서 멈춤 · 체력이 가득 차 있으면 못 씀<br>스테미나 20 · 쿨타임 10초', tag: '힐', once: true,
              apply: p => { p.canHeal = true; } },
            { ic: 'BLOCK', r: 'epic', kind: 'skill', blocked: hasSpecial, nm: '장애물 설치', ds: '특수키(1P V / 2P ;)로 내 발밑에 낮은 박스를 설치하고 그 위로 올라섬<br>상대는 걸어서 못 지나가고 점프로 넘거나 위에 올라설 수 있음 (위에서는 주먹 · 발차기에 안 맞고, 총에는 맞음)<br>총알 · 시야는 막음 · 체력 50 (때려서 부수거나 가까이서 발차기로 밀 수 있음 · 밀면 위에 선 사람은 떨어짐)<br>스테미나 15 · 쿨타임 8초', tag: '장애물', once: true,
              apply: p => { p.canObst = true; } },
            // 등급별 능력치 카드 (똥 < 노말 < 희귀 < 레전더리)
            { ic: 'POOP', r: 'dung', kind: 'stat', nm: '똥 밟음', ds: '최대 체력 +0.5칸<br>…냄새가 난다', tag: '체력+0.5칸',
              apply: p => { p.maxHp += 5; } },
            { ic: 'DROP', r: 'dung', kind: 'stat', nm: '푼돈 스테미나', ds: '최대 스테미나 +5<br>없는 것보단 낫다', tag: 'ST+5',
              apply: p => { p.maxStamina += 5; } },
            { ic: 'GIANT', r: 'legend', kind: 'stat', nm: '거대화', ds: '최대 체력 +1칸<br>이동 속도 -25% · 기절 면역<br>몸이 커져서 상대 화면에 더 크게 보임', tag: '체력+1칸 기절면역',
              apply: p => { p.maxHp += 10; p.giant = true; p.bodyScale = 1.35; } },
        ];
        // 장풍 + 점프를 둘 다 가지면 바로 승룡권으로 합쳐짐 (둘을 같이 쓰는 상태는 없음). 승룡권을 가지면 장풍 · 점프 카드는 카드열에서도 사라짐
        function fuseSpecial(p) {
            const sh = CARD_POOL.find(c => c.ic === 'SHORYU'), ds = CARD_POOL.find(c => c.ic === 'DSLASH');
            let fused = null;   // 이번에 새로 융합됐으면 { parts: 재료 카드 둘, result: 융합 카드 } (융합 연출용)
            if (p.canKi && p.canJump) {
                const parts = [p.cards.find(c => c.ic === 'KI'), p.cards.find(c => c.ic === 'JUMP')];
                sh.apply(p); if (!p.cards.includes(sh)) p.cards.push(sh);
                if (parts[0] && parts[1]) fused = { parts, result: sh };
            }
            if (p.canShoryu) p.cards = p.cards.filter(c => c.ic !== 'KI' && c.ic !== 'JUMP');
            if (p.canDash && p.knife) {   // 대쉬 + 칼도 같은 방식: 합쳐지면 둘은 카드열에서 사라짐
                const parts = [p.cards.find(c => c.ic === 'DASH'), p.cards.find(c => c.ic === 'KNIFE')];
                ds.apply(p); if (!p.cards.includes(ds)) p.cards.push(ds);
                if (parts[0] && parts[1]) fused = { parts, result: ds };
            }
            if (p.canSlash) p.cards = p.cards.filter(c => c.ic !== 'DASH' && c.ic !== 'KNIFE');
            return fused;
        }
        function fusionReady(p) {   // 융합 재료가 모였고 아직 융합 카드가 없으면 { parts, result } (적용은 안 함: 융합 카드를 직접 골라야 함)
            const sh = CARD_POOL.find(c => c.ic === 'SHORYU'), ds = CARD_POOL.find(c => c.ic === 'DSLASH');
            if (p.canKi && p.canJump && !p.canShoryu) { const parts = [p.cards.find(c => c.ic === 'KI'), p.cards.find(c => c.ic === 'JUMP')]; if (parts[0] && parts[1]) return { parts, result: sh }; }
            if (p.canDash && p.knife && !p.canSlash) { const parts = [p.cards.find(c => c.ic === 'DASH'), p.cards.find(c => c.ic === 'KNIFE')]; if (parts[0] && parts[1]) return { parts, result: ds }; }
            return null;
        }
        const fuseScreen = document.getElementById('fuse-screen');
        let fusing = false;   // 융합 연출 중 (이 동안은 다음 카드 선택 · 라운드 진행을 멈춤)
        function playFusion(f, done) {   // 융합 연출(약 2.2초) 뒤 done 실행
            const mk = (c, cls, full) => '<div class="card ' + (c.kind === 'skill' ? 'skill' : 'stat') + ' r-' + c.r + ' ' + cls + '">' + (c.r === 'fusion' ? '<i class="sp s1"></i><i class="sp s2"></i><i class="sp s3"></i>' : '') +
                '<div class="rar">' + RARITY[c.r].nm + '</div><div class="ic">' + c.ic + '</div><div class="nm">' + cardName(c) + '</div>' + (full ? '<div class="ds">' + c.ds + '</div>' : '') + '</div>';
            fuseScreen.innerHTML = '<div id="fuse-title">★ 융합! ★</div><div id="fuse-stage">' + mk(f.parts[0], 'fa') + mk(f.parts[1], 'fb') + mk(f.result, 'fc', true) + '</div><div id="fuse-flash"></div>';
            fuseScreen.classList.remove('hidden');
            if (window.NET && NET.on) NET.fuse(f);
            fusing = true;
            setTimeout(() => bgm.sfx('guard'), 1000);
            setTimeout(() => { fuseScreen.classList.add('hidden'); fuseScreen.innerHTML = ''; fusing = false; done(); }, 2400);
        }
        // 특수공격 키를 같이 쓰는 카드끼리는 못 가짐 (개발자 모드 · 연습 모드의 승룡권 포함)
        const keyShared = (c, p) => c.hidden ? !!c.conflict(p) : !!(c.blocked && c.blocked(p));
        // 카드 이름 옆에 붙는 분류: 특수(특수공격 키) / 차지(꾹 누르는 카드, 특수키 꾹 제외) / 무기 / 이동 / 스텟
        const CARD_CAT = { CLONE: '특수', INVIS: '특수', HEAL: '특수', BLOCK: '특수', BLINK: '특수', FLURRY: '차지', JUMP: '차지', CHARGE: '차지', DASH: '이동', TAUNT: '특수', INK: '특수', KI: '특수', SHORYU: '특수', DSLASH: '이동', GUN: '무기', KNIFE: '무기' };
        function cardName(c) { const t = c.kind === 'stat' ? '스텟' : CARD_CAT[c.ic]; return c.nm + (t ? ' (' + t + ')' : ''); }
        // AI(aiControl)가 쓸 줄 아는 기술 카드. 스텟 카드는 항상 OK. 새 기술 카드를 만들면 aiControl 에 쓰는 법을 넣고 여기에도 추가
        const AI_SKILLS = new Set(['JUMP', 'DASH', 'TAUNT', 'GUN', 'KNIFE', 'INK', 'KI', 'SHORYU', 'CHARGE', 'DSLASH', 'CLONE', 'INVIS', 'HEAL', 'BLOCK']);
        const aiCanUse = c => c.kind !== 'skill' || AI_SKILLS.has(c.ic);
        const cardScreen = document.getElementById('card-screen');
        const cardListEl = document.getElementById('card-list');
        let picking = false, pickPlayer = null, pickCards = [], pickIdx = 0;
        let devMode = false, devBuf = '', devKeys = '';   // 개발자 모드: 카드 선택창에서 8015 입력 → 이번 한 번만 모든 카드 중에서 고르기

        function resetBuffs() { for (const p of [p1, p2]) resetPlayerBuffs(p); }
        function resetPlayerBuffs(p) {
            p.maxHp = Math.round(100 * matchCfg.hp); p.canJump = false; p.maxStamina = Math.round(STAMINA_MAX * matchCfg.sta); p.reachMul = 1; p.canDash = false; p.canSlash = false; p.dashT = 0; p.dashCd = 0; p.jumpCd = 0; p.stompDone = false; p.jumping = false; p.canTaunt = false; p.tauntT = 0; p.tauntCd = 0; p.canKi = false; p.canShoryu = false; p.atkCdMul = 1; p.kickCdMul = 1; p.guardCdMul = 1; p.gun = false; p.knife = false; p.canInk = false; p.canCharge = false; p.bodyScale = 1; p.giant = false; p.cards = [];
            p.dmgMul = 1; p.freeHit = false; p.charging = ''; p.chargeT = 0; p.hold = ''; p.holdT = 0; p.kiOn = false; p.kiT = 0; p.canBlink = false; p.canFlurry = false; p.blinkCd = 0; p.blinkOn = false; p.blinkD = 0; p.ghostT = 0; p.flurryOn = false; p.flurryT = 0; p.flurryHits = 0; p.flurryCd = 0; p.canClone = false; p.canInvis = false; p.canHeal = false; p.canObst = false; p.cloneCd = 0; p.invisCd = 0; p.invisT = 0; p.healCd = 0; p.obstCd = 0;   // 힘조절·장풍 상태도 같이 초기화 (연습 모드에서 카드를 빼도 배율이 남지 않게)
        }
        function renderCards() {
            [...cardListEl.children].forEach((el, i) => {
                el.classList.toggle('sel', i === pickIdx);
                if (i === pickIdx && devMode) el.scrollIntoView({ block: 'nearest', inline: 'nearest' });
            });
        }
        const RARITY = { dung: { nm: '💩 똥', w: 15 }, normal: { nm: '노말', w: 28 }, rare: { nm: '희귀', w: 27 }, epic: { nm: '에픽', w: 20 }, legend: { nm: '★ 레전더리', w: 10 }, fusion: { nm: '융합', w: 0 } };   // w: 한 장을 뽑을 때 그 등급이 나올 확률(%)
        const RANK = { dung: 0, normal: 1, rare: 2, epic: 3, legend: 4, fusion: 5 };
        function drawCards(avail, n) {   // 먼저 등급을 확률로 정하고, 그 등급 안에서 무작위로 겹치지 않게 n장 뽑기
            const pool = avail.slice(), out = [];
            while (out.length < n && pool.length) {
                const tiers = Object.keys(RARITY).filter(r => RARITY[r].w > 0 && pool.some(c => c.r === r));   // 융합(w 0)은 확률로 안 나오고 조건을 채우면 자리에 등장
                if (!tiers.length) break;
                let x = Math.random() * tiers.reduce((sum, r) => sum + RARITY[r].w, 0), t = tiers[tiers.length - 1];
                for (const r of tiers) { x -= RARITY[r].w; if (x < 0) { t = r; break; } }
                const cand = pool.filter(c => c.r === t);
                out.push(pool.splice(pool.indexOf(cand[Math.floor(Math.random() * cand.length)]), 1)[0]);
            }
            return out;
        }
        function buildCards(only) {   // only: 융합 기술 선택일 때 그 카드 한 장만 보여 줌
            const dev = !only && devMode && !(aiMode && pickPlayer === aiSelf);   // AI가 고를 때는 평소처럼 무작위 3장
            const avail = CARD_POOL.filter(c => !(c.once && pickPlayer.cards.includes(c)) && !(c.blocked && c.blocked(pickPlayer)) && !(aiMode && pickPlayer === aiSelf && !aiCanUse(c)));   // AI 가 고를 때는 AI 가 쓸 수 있는 카드만 나옴
            const devAvail = dev ? CARD_POOL.filter(c => !(c.once && pickPlayer.cards.includes(c)) && !(c.hidden && c.has(pickPlayer)) && !keyShared(c, pickPlayer)) : null;   // 개발자 모드: 히든 카드(승룡권)도 재료 없이 선택 가능 (단, 같은 키를 쓰는 도발 · 먹물이 있으면 불가)
            const sry = avail.find(c => c.hidden);   // (장풍 + 점프는 가지는 즉시 합쳐져서 보통은 여기 안 나옴)
            pickCards = only ? [only] : (dev ? devAvail : sry ? [sry, ...drawCards(avail.filter(c => c !== sry), 2)] : drawCards(avail, 3)).sort((a, b) => RANK[a.r] - RANK[b.r]);   // 왼쪽 → 오른쪽으로 갈수록 높은 등급
            pickIdx = only || dev ? 0 : 1;
            cardScreen.classList.toggle('dev', dev);
            document.getElementById('card-dev').style.display = dev ? 'block' : 'none';
            cardListEl.innerHTML = '';
            pickCards.forEach((c, i) => {
                const el = document.createElement('div');
                el.className = 'card ' + (c.kind === 'skill' ? 'skill' : 'stat') + ' r-' + c.r;
                el.innerHTML = (c.r === 'legend' || c.r === 'fusion' ? '<i class="sp s1"></i><i class="sp s2"></i><i class="sp s3"></i>' : '') + '<div class="rar">' + RARITY[c.r].nm + '</div><div class="ic">' + c.ic + '</div><div class="nm">' + cardName(c) + '</div><div class="ds">' + c.ds + '</div>';
                el.addEventListener('click', () => { if (window.NET && NET.on && NET.notMyPick()) return; pickIdx = i; confirmCard(); });
                el.addEventListener('mouseenter', () => { if (window.NET && NET.on && NET.notMyPick()) return; pickIdx = i; renderCards(); });
                cardListEl.appendChild(el);
            });
            renderCards();
        }
        let pickQueue = [], pickDraw = false;   // 카드를 고를 사람 순서 / 무승부로 열린 선택인지
        let introPick = false;                  // 경기 시작 직후 각자 능력 하나씩 고르는 중
        function startIntroPick() {             // 경기 시작: 1P → 2P 순서로 능력 카드를 한 장씩 고른 뒤 1라운드 시작
            pickQueue = [p1, p2]; pickDraw = true; introPick = true;
            gameOver = true; winner = null; timeUp = false;   // 선택하는 동안 경기를 멈춤 (선택 키 입력도 이 상태에서 받음)
            openNextPick();
        }
        function openCards() {
            pickQueue = winner ? [winner === p1 ? p2 : p1] : [p1, p2];   // 진 사람 / 무승부면 1P → 2P 순서로 둘 다
            pickDraw = !winner;
            openNextPick();
        }
        function openNextPick(fuse) {   // fuse: 융합 연출 뒤 같은 사람이 융합 카드(한 장)를 고름
            if (!fuse) pickPlayer = pickQueue.shift();
            const isP1 = pickPlayer === p1;
            picking = true;
            devBuf = ''; devKeys = '';
            for (const k in keys) keys[k] = false;
            const title = document.getElementById('card-title');
            title.textContent = (isP1 ? 'PLAYER 1' : 'PLAYER 2') + (fuse ? ' 융합 기술 선택' : introPick ? ' 시작 능력 선택' : ' 카드 선택');
            title.style.color = pickPlayer.color;
            document.getElementById('card-sub').textContent = isP1
                ? 'A / D 로 고르고 Z 로 선택 (클릭도 가능)'
                : '← / → 로 고르고 . 로 선택 (클릭도 가능)';
            buildCards(fuse);
            cardScreen.classList.remove('hidden');
            if (aiMode && pickPlayer === aiSelf) {   // AI는 카드를 잠시 뒤 무작위로 고름
                setTimeout(() => { const hi = pickCards.findIndex(c => c.hidden); pickIdx = hi >= 0 ? hi : Math.floor(Math.random() * pickCards.length); renderCards(); confirmCard(); }, 1200);   // 히든 카드(승룡권)가 나오면 AI는 그걸 고름
            }
        }
        function confirmCard() {
            if (!picking) return;
            const c = pickCards[pickIdx];
            c.apply(pickPlayer);
            pickPlayer.cards.push(c);
            const fused = fusionReady(pickPlayer);   // 재료가 모였으면 바로 합치지 않고, 연출 뒤 융합 카드를 직접 고르게 함
            if (!fused) fuseSpecial(pickPlayer);
            devMode = false;   // 개발자 모드는 한 번 고르면 꺼짐 (다음엔 8015 를 다시 입력해야 함)
            picking = false;
            const next = () => {
                if (pickQueue.length) openNextPick();   // 무승부: 다음 사람도 고름
                else if (pickDraw) resetGame();          // 무승부: 점수·라운드는 그대로 같은 라운드를 다시
                else nextRound();
            };
            showPicked(c, () => { cardScreen.classList.add('hidden'); if (fused) playFusion(fused, () => openNextPick(fused.result)); else next(); });   // 고른 카드를 2초 크게 보여 준 뒤, 융합이 일어나면 연출을 보여주고 이어감
        }
        function showPicked(c, done) {   // 고른 카드만 남기고 크게 (이 동안 라운드 진행은 멈춤: fusing 재사용)
            const idx = pickCards.indexOf(c);
            [...cardListEl.children].forEach((el, k) => { if (k !== idx) el.style.display = 'none'; else el.classList.add('picked'); });
            cardScreen.classList.add('showpick');
            if (window.NET && NET.on) NET.picked(idx);
            fusing = true;
            setTimeout(() => { fusing = false; cardScreen.classList.remove('showpick'); done(); }, 2000);
        }
        function closeCards() {
            picking = false;
            cardScreen.classList.add('hidden');
        }


        // ===== 연습 모드 (1인 전용): 시간 · KO 없음. ESC 를 누르면 능력을 실시간으로 추가/제거하고 편의 설정을 바꿈 =====
        const practiceMe = () => (aiMode && aiSelf === p1) ? p2 : p1;   // 연습 모드에서 내가 조작하는 쪽
        const practiceSettings = { target: 1, dummy: 'idle', map: 'gym', infStamina: true, shoryuAuto: false, slow: false };
        const PR_MAPS = [['gym', '건물'], ['colo', '콜로세움'], ['city', '도시']];
        const PR_DUMMY = [['idle', '가만히'], ['easy', '쉬운 AI'], ['normal', '보통 AI'], ['hard', '어려운 AI'], ['human', '2P (사람)']];
        function practiceTick() {
            const me = practiceMe();
            if (practiceSettings.infStamina) { me.stamina = me.maxStamina; me.staminaDelay = 0; }
            if (practiceSettings.shoryuAuto && me.canShoryu && !me.shoryuOn && me.shoryuReady < 0.5) me.shoryuReady = SHORYU_READY_TIME;   // 방향키로 돌지 않아도 바로 사용
            if (gameOver || p1.hp <= 0 || p2.hp <= 0) {   // KO 없이 계속: 쓰러진 쪽 체력만 회복
                for (const q of [p1, p2]) if (q.hp <= 0) q.hp = q.maxHp;
                p1.wins = 0; p2.wins = 0; matchOver = false; gameOver = false; winner = null; roundEndT = 0;
                updateUI();
            }
        }
        function practiceReset() {   // 위치 · 체력 · 스테미나 초기화 (능력은 유지)
            resetGame();
            p1.wins = 0; p2.wins = 0;
            for (const k in keys) keys[k] = false;
        }
        function practiceCooldowns() {
            for (const q of [p1, p2]) {
                q.gunCd = 0; q.gunAmmo = GUN_MAG; q.gunReload = 0; q.inkCd = 0; q.kiCd = 0; q.blinkCd = 0; q.flurryCd = 0; q.cloneCd = 0; q.invisCd = 0; q.healCd = 0; q.obstCd = 0; q.tauntCd = 0; q.kickCd = 0; q.guardCd = 0; q.dashCd = 0;
                if (!q.shoryuOn) q.cooldown = 0;
            }
        }
        function practiceSync(q) {   // 능력이 바뀌면 체력 · 스테미나를 가득 채움
            q.hp = q.maxHp; q.stamina = q.maxStamina; q.shoryuReady = 0;
            updateUI(); updateStamina();
        }
        function practiceAdd(c, q) { c.apply(q); q.cards.push(c); fuseSpecial(q); practiceSync(q); }
        function practiceRemove(c, q) {   // 카드 한 장을 빼고 나머지 능력으로 다시 계산
            const rest = q.cards.slice(); rest.splice(rest.lastIndexOf(c), 1);
            resetPlayerBuffs(q);
            for (const k of rest) { k.apply(q); q.cards.push(k); }
            fuseSpecial(q);
            practiceSync(q);
        }
        function renderPractice() {
            const q = practiceSettings.target === 1 ? p1 : p2;
            const S = practiceSettings;
            const opt = (id, label, on) => '<button class="pr-btn' + (on ? ' on' : '') + '" data-pr="' + id + '">' + label + '</button>';
            document.getElementById('pr-opts').innerHTML =
                opt('dummy', '상대: ' + PR_DUMMY.find(d => d[0] === S.dummy)[1], S.dummy !== 'idle')
                + opt('map', '맵: ' + PR_MAPS.find(m => m[0] === S.map)[1], S.map !== 'gym')
                + opt('stamina', '스테미나 무한 ' + (S.infStamina ? 'ON' : 'OFF'), S.infStamina)
                + opt('shoryu', '승룡권 바로 사용 ' + (S.shoryuAuto ? 'ON' : 'OFF'), S.shoryuAuto)
                + opt('slow', '슬로우 ' + (S.slow ? 'ON' : 'OFF'), S.slow)
                + opt('cd', '쿨타임 초기화', false)
                + opt('reset', '위치 초기화 [R]', false);
            document.getElementById('pr-target').innerHTML = '<span style="align-self:center;font-size:13px;color:#ccc">능력을 줄 대상:</span>'
                + opt('t1', (practiceMe() === p1 ? '나' : '상대') + ' (1P)', S.target === 1) + opt('t2', (practiceMe() === p2 ? '나' : '상대') + ' (2P)', S.target === 2) + opt('clear', '능력 모두 제거', false);
            const tiers = Object.keys(RARITY).sort((a, b) => RANK[b] - RANK[a]);
            const body = document.getElementById('pr-body');
            const keep = body.scrollTop;
            body.innerHTML = tiers.map(r => '<div class="cl-group cl-' + r + '"><div class="cl-head">' + RARITY[r].nm + '</div>'
                + CARD_POOL.filter(c => c.r === r).map(c => {
                    const n = q.cards.filter(k => k === c).length;
                    const blocked = !n && keyShared(c, q);   // 같은 키를 쓰는 카드와는 같이 못 가짐 (승룡권은 도발·먹물과만)
                    const st = n ? ('보유' + (n > 1 ? ' x' + n : '')) + (c.once ? ' · 클릭하면 제거' : '') : blocked ? '다른 카드와 함께 못 씀' : '';
                    return '<div class="pr-item' + (n ? ' has' : '') + (blocked ? ' dis' : '') + '" data-card="' + CARD_POOL.indexOf(c) + '"><div class="pr-nm">' + cardName(c) + '</div><div class="pr-ds">' + c.ds + '</div><div class="pr-st">' + st + '</div>'
                        + (n && !c.once ? '<button class="pr-minus" data-minus="' + CARD_POOL.indexOf(c) + '">−</button>' : '') + '</div>';
                }).join('') + '</div>').join('');
            body.scrollTop = keep;
            document.getElementById('pr-foot').innerHTML = opt('resume', '계속하기 [ESC]', false) + opt('home', '처음 화면으로', false);
        }
        document.getElementById('practice-screen').addEventListener('click', e => {
            const t = e.target.closest('[data-pr],[data-card],[data-minus]');
            if (!t) return;
            const S = practiceSettings, q = S.target === 1 ? p1 : p2;
            if (t.dataset.minus !== undefined) { practiceRemove(CARD_POOL[+t.dataset.minus], q); }
            else if (t.dataset.card !== undefined) {
                const c = CARD_POOL[+t.dataset.card];
                const n = q.cards.filter(k => k === c).length;
                if (n && c.once) practiceRemove(c, q);
                else if (!n && keyShared(c, q)) return;
                else practiceAdd(c, q);
            } else {
                const id = t.dataset.pr;
                if (id === 'dummy') {
                    const i = PR_DUMMY.findIndex(d => d[0] === S.dummy);
                    S.dummy = PR_DUMMY[(i + 1) % PR_DUMMY.length][0];
                    aiMode = S.dummy !== 'human';   // 2P(사람)이면 2P 키 입력을 받고 AI는 끔
                    if (S.dummy === 'idle' || S.dummy === 'human') { for (const k of Object.values(aiKeys())) keys[k] = false; }
                    else aiLevel = AI_LEVELS[S.dummy];
                }
                else if (id === 'map') {   // 맵 바꾸기: 새 맵의 시작 위치로 옮기고 위치 · 체력 초기화 (능력은 유지)
                    const i = PR_MAPS.findIndex(m => m[0] === S.map);
                    S.map = PR_MAPS[(i + 1) % PR_MAPS.length][0];
                    matchCfg.map = S.map; setMap(S.map); practiceReset();
                }
                else if (id === 'stamina') S.infStamina = !S.infStamina;
                else if (id === 'shoryu') S.shoryuAuto = !S.shoryuAuto;
                else if (id === 'slow') S.slow = !S.slow;
                else if (id === 'cd') practiceCooldowns();
                else if (id === 'reset') { practiceReset(); }
                else if (id === 't1') S.target = 1;
                else if (id === 't2') S.target = 2;
                else if (id === 'clear') { resetPlayerBuffs(q); practiceSync(q); }
                else if (id === 'resume') { togglePause(); if (document.activeElement) document.activeElement.blur(); return; }
                else if (id === 'home') { goHome(); return; }
            }
            renderPractice();
            if (document.activeElement) document.activeElement.blur();
        });

        // KO 뒤 Enter/R: 경기가 끝났으면 새 경기, 아니면 다음 라운드
        function nextRound() {
            const fresh = matchOver;   // 새 경기라면 시작 능력을 다시 고름
            if (matchOver) {
                p1.wins = 0; p2.wins = 0;
                matchOver = false;
                round = 1;
                resetBuffs();
            } else {
                round++;
            }
            resetGame();
            if (fresh && !practice && !tutorial) startIntroPick();
        }

        // ===== 이동 =====
        function movePlayer(player, cfg, dt) {
            let move = 0, rot = 0;
            if (keys[cfg.up]) move += MOVE_SPEED;
            if (keys[cfg.down]) move -= MOVE_SPEED;
            // 1인용 '마우스 · 터치 회전': 좌우 키는 옆으로 이동(대각선도 같은 속도), 회전은 마우스 · 터치 이동량이 맡음
            const ptrRot = YK.ptrRot(player);
            let moveAng = 0;   // 바라보는 방향 기준 이동 각도 (0 = 앞, +90° = 오른쪽)
            if (ptrRot) {
                const st = (keys[cfg.right] ? 1 : 0) - (keys[cfg.left] ? 1 : 0);
                if (st) { move = MOVE_SPEED; moveAng = Math.atan2(st, (keys[cfg.up] ? 1 : 0) - (keys[cfg.down] ? 1 : 0)); }
            }
            if (player.giant) move *= GIANT_MOVE_MUL;   // 거대화: 이동 속도 감소
            if (aiMode && player === aiSelf) move *= aiScaled().speed;   // AI 이동 속도는 난이도에 따라
            if (ptrRot) { if (dt > 0) rot += YK.takeRot() / dt; }   // 포인터가 돌린 만큼 (아래 제한 · 총 감속 · 승룡권 회전 누적에 그대로 적용)
            else {
                if (keys[cfg.left]) rot -= ROT_SPEED;
                if (keys[cfg.right]) rot += ROT_SPEED;
            }
            if (player.dashT > 0) { move = 0; rot = 0; }   // 대쉬 중에는 조작 불가 (돌진은 updateDash 가 처리)
            if (player.dizzy > 0 || player.slideT > 0) { move = 0; rot = 0; }
            if (player.fallT > 0) move *= 0.3;   // 바다에 빠진 동안은 느리게 헤엄칠 수 있음   // 기절 중에는 이동/회전 불가
            if (player.z > 0 && !player.jumping) move *= AIR_MOVE_MULT;   // 공중에서는 느리게

            if (player.gun) rot *= GUN_ROT_MUL;   // 총 카드를 가지면 회전이 느려짐
            if (player.gun && aiMode && player === aiSelf) rot *= AI_GUN_ROT_MUL;   // AI는 총을 들면 훨씬 더 느리게 돌아감
            if (player.shoryuOn) { move = 0; rot = 0; }
            if (player.flurryOn) move *= FLURRY_MOVE_MUL;   // 백열권을 쓰는 동안은 느리게 이동 가능   // 승룡권을 쓰는 동안은 조작 불가
            if (player.canShoryu) {   // 한 방향으로 한 바퀴 돌면 승룡권 준비 (방향을 바꾸거나 잠깐 멈추면 처음부터)
                if (rot !== 0) {
                    if (Math.sign(rot) !== Math.sign(player.spinAcc)) player.spinAcc = 0;
                    player.spinAcc += rot * dt; player.spinIdle = 0;
                    if (Math.abs(player.spinAcc) >= SHORYU_SPIN) { player.shoryuReady = SHORYU_READY_TIME; player.spinDir = Math.sign(player.spinAcc); player.spinAcc = 0; bgm.sfx('guard'); }
                } else if ((player.spinIdle += dt) > SHORYU_SPIN_GAP) player.spinAcc = 0;
            }
            player.angle += rot * dt;
            player.moving = move !== 0;
            if (move !== 0) {
                const ox = player.x, oy = player.y;
                tryMove(player,
                    player.x + Math.cos(player.angle + moveAng) * move * dt,
                    player.y + Math.sin(player.angle + moveAng) * move * dt);
                if (player.fallT > 0 && Math.hypot(player.x - ARENA_C, player.y - ARENA_C) <= ARENA_R) { player.x = ox; player.y = oy; }   // 헤엄쳐서 원형 바닥 위로 올라올 수는 없음
            }
        }

        // 콜로세움 하늘 + 바닥 + 바다: 바닥은 화면 한 점마다 월드 좌표를 구해, 원 안이면 돌바닥 / 밖이면 (한 단계 낮은) 바다를 칠함
        function drawArenaBackdrop(view, observer, half, eye, proj) {
            const { canvas, ctx } = view;
            const width = canvas.width, height = canvas.height;
            for (let y = 0; y < Math.floor(half); y++) {   // 하늘: 위는 진하고 지평선 쪽은 옅게
                const k = Math.max(0, Math.min(1, y / Math.max(1, half)));
                ctx.fillStyle = 'rgb(' + Math.round(70 + 130 * k) + ',' + Math.round(150 + 85 * k) + ',' + Math.round(225 + 20 * k) + ')';
                ctx.fillRect(0, y, width, 1);
            }
            const y0 = Math.max(0, Math.ceil(half));
            if (y0 >= height) return;
            if (!view.fc || view.fc.width !== width || view.fc.height !== height) {
                view.fc = document.createElement('canvas'); view.fc.width = width; view.fc.height = height;
                view.fctx = view.fc.getContext('2d');
                view.fimg = view.fctx.createImageData(width, height);
                for (let i = 3; i < view.fimg.data.length; i += 4) view.fimg.data[i] = 255;
            }
            const data = view.fimg.data, cosA = Math.cos(observer.angle), sinA = Math.sin(observer.angle);
            for (let y = y0; y < height; y++) {
                const d0 = eye * proj / (y + 0.5 - half);               // 이 줄에서 바닥(높이 0)까지의 거리
                const d1 = (eye + SEA_DROP) * proj / (y + 0.5 - half);   // 이 줄에서 바다(더 낮음)까지의 거리
                const fog0 = Math.max(0.2, 1 - d0 / 800), fog1 = Math.max(0.3, 1 - d1 / 900);
                let i = (y * width) * 4;
                for (let x = 0; x < width; x++, i += 4) {
                    const u = (x + 0.5 - width / 2) / proj;
                    const dx = cosA - sinA * u, dy = sinA + cosA * u;
                    const wx = observer.x + dx * d0, wy = observer.y + dy * d0;
                    const rr = Math.sqrt((wx - ARENA_C) * (wx - ARENA_C) + (wy - ARENA_C) * (wy - ARENA_C));
                    let r, g, b, f;
                    if (rr <= ARENA_R) {
                        f = fog0;
                        if (rr > ARENA_R - 7) { r = 120; g = 100; b = 70; }                                   // 가장자리 테두리
                        else if (Math.abs(rr - 150) < 3 || Math.abs(rr - 60) < 3) { r = 150; g = 125; b = 85; }   // 둥근 무늬
                        else { const c = (Math.floor(wx / 48) + Math.floor(wy / 48)) & 1; r = c ? 205 : 192; g = c ? 183 : 171; b = c ? 140 : 130; }
                    } else {
                        f = fog1;
                        const sx = observer.x + dx * d1, sy = observer.y + dy * d1;
                        const w = Math.sin(sx * 0.05 + gameTime * 1.6) + Math.sin(sy * 0.043 - gameTime * 1.2);   // 물결
                        const foam = w > 1.6 ? 45 : 0;
                        r = 28 + w * 8 + foam; g = 102 + w * 10 + foam; b = 170 + w * 8 + foam;
                    }
                    data[i] = r * f; data[i + 1] = g * f; data[i + 2] = b * f;
                }
            }
            view.fctx.putImageData(view.fimg, 0, 0);
            ctx.drawImage(view.fc, 0, y0, width, height - y0, 0, y0, width, height - y0);
        }

        const CITY_WALLS = ['#b5524a', '#8d9aa6', '#c9a66b', '#6f8f72', '#a8a0b8'];   // 도시 건물 색 (칸마다 번갈아)
        const cityHash = (a, b, c) => (Math.imul(a + 7, 73856093) ^ Math.imul(b + 13, 19349663) ^ Math.imul(c + 3, 83492791)) >>> 0;
        // 도시 건물 그림(26369.png): 벽 높이(CEIL_H)와 같은 폭으로 이어 붙이고, 건물마다 색과 좌우를 조금씩 바꿈
        const FACADE_B64 = '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';
        const FACADE_GRAY_B64 = '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';   // 26372.png 왼쪽 회청색 건물
        const FACADE_TAN_B64 = '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';   // 26372.png 오른쪽 갈색 건물
        const FACADE_VARIANTS = [   // [원본 그림(0 첫 그림, 1 회청색, 2 갈색), 벽 색 배율 RGB, 벽돌 색 배율 RGB]: 배율이 없으면 원본 그대로
            [0], [1], [2],
            [0, [0.9, 0.97, 1.06], [0.78, 0.84, 0.95]],
            [0, [0.94, 1.02, 0.92], [0.9, 0.8, 0.78]]
        ];
        const facadeImgs = [];   // 변형마다 그림 (불러오기 전에는 비어 있어서 예전 벽을 그림)
        {
            const srcs = [FACADE_B64, FACADE_GRAY_B64, FACADE_TAN_B64].map(b => { const im = new Image(); im.src = 'data:image/png;base64,' + b; return im; });
            let left = srcs.length;
            srcs.forEach(im => im.onload = () => {
                if (--left) return;
                FACADE_VARIANTS.forEach(([si, wf, bf], v) => {
                    const im0 = srcs[si], c = document.createElement('canvas'); c.width = im0.width; c.height = im0.height;
                    const g = c.getContext('2d'); g.drawImage(im0, 0, 0);
                    if (wf) {
                        const d = g.getImageData(0, 0, c.width, c.height), p = d.data;
                        for (let k = 0; k < p.length; k += 4) {
                            const r = p[k], gr = p[k + 1], b = p[k + 2];
                            const m = (r > 120 && gr > r * 0.8 && r - b > 15) ? wf : (r > 120 && gr < r * 0.65 && b < r * 0.5) ? bf : null;   // 베이지 벽 / 붉은 벽돌만 색을 바꿈
                            if (m) { p[k] = Math.min(255, r * m[0]); p[k + 1] = Math.min(255, gr * m[1]); p[k + 2] = Math.min(255, b * m[2]); }
                        }
                        g.putImageData(d, 0, 0);
                    }
                    facadeImgs[v] = c;
                });
            });
        }
        const CITY_BLD = (() => {   // 칸마다 건물 번호(바깥 둘레는 0)와 건물이 차지한 칸 범위
            const H = CITY_MAP.length, W = CITY_MAP[0].length, id = CITY_MAP.map(r => r.map(() => 0)), box = [null];
            for (let y = 1; y < H - 1; y++) for (let x = 1; x < W - 1; x++) {
                if (CITY_MAP[y][x] !== 1 || id[y][x]) continue;
                const n = box.length, bb = { x0: x, x1: x, y0: y, y1: y }, st = [[x, y]];
                id[y][x] = n;
                while (st.length) {
                    const [cx, cy] = st.pop();
                    bb.x0 = Math.min(bb.x0, cx); bb.x1 = Math.max(bb.x1, cx); bb.y0 = Math.min(bb.y0, cy); bb.y1 = Math.max(bb.y1, cy);
                    for (const [dx, dy] of [[1, 0], [-1, 0], [0, 1], [0, -1]]) {
                        const nx = cx + dx, ny = cy + dy;
                        if (nx < 1 || ny < 1 || nx >= W - 1 || ny >= H - 1 || CITY_MAP[ny][nx] !== 1 || id[ny][nx]) continue;
                        id[ny][nx] = n; st.push([nx, ny]);
                    }
                }
                box.push(bb);
            }
            return { id, box };
        })();
        const TUNNEL_B64 = 'iVBORw0KGgoAAAANSUhEUgAAAKMAAACQCAYAAABkgtuDAABcv0lEQVR42u29ebxkV3Xf+937DDXdeei+PXdrBs0IkBCDQAhjMI4MWBjbsQk84xA7+D3b2DHBNih+BCeObZzkOS8kxthgCNOzgTDIskEDQgjNU6vn8c5zzXWGvff7Y+9zqqo1Yw3douvz6Y9afe+tW1VnnbXX+q3f+v3gBfS47rrrHvVvUko8z+v74/s+W7duNUJg4OT6c8EFF5ixsfH8dWavWUqPF/pDvFDfmJSSc845hwMHDhilFMaYR33P6PgUr3zVq3nZpReitMLzPNI0RSmNkALhPh4hBMYY9xwmf34AbQCjUdoAAk8KMMZ9l8EYQAiEsB+2NmC0wfcEQnoIIRBCcNvtd/G9226h1aziCVA9L9f3JWmq2bVrB0tLK6LRaLwgr5n/Qnozb3jDG7j3gXtJOglbt241c3NzDAwOMTAwwMT4GOVSEWMMSkOaJhQqG7j0siv4+Z97K4ePTCOEQGmN73l4nrRBZAxKG7TWYEBIge97SCFQSpOkGtA2YBH4UqCN+373sJlNoJXBYFxgCvwgAAytdofDM+ucvbJC0UsJfI9WJ0YKiTaKeqNBq9VhcXGZC88/3zz8yCNCKcXFF1/M7bff3ncqvPjFL+b6668/nRmfr8fc3By/9N73mnvuvZvF+UV838cYgzaGf/mrv8U1V1/FxOgQnidRyhAEPp0o5q8/+2U8Ce/+xXdw4z9+DyEEUoDv+0gpbOAg0EZjtM2QLlUibN7LEqX7ftBK22zogk5KiZTS/az7fpd1tTEkSUqnE3Prbd/jissv4+fe8VO02x0ajSalUpFUKWbml3jggd18/I//gDSJUUqD0UxMTnLuuWfzr//1r4l3vOMdp4/p5+vxmte8BqUUAIVymXvvususra0xtWkbP/eu9/GyS85lZLCC8AKMMSwsLVOrNYjjFM+3x+O3b/oeA5UiP/uOt7Jn70HiJEFKQSEMUVojEAhpg1Bgj1OlNAhssGtNEPhorTHGIIQkVQoppA1EYT9iIQQIQRwnBL6tBZVWgCBJElZWq9x1z7289NILufKKl7J332EKhYBCIaQQhgwNDlCplEjTmOXlNW6+7S7+9kt/TW19ldGxMa655hrR6DTw8alUKnz2s589fUw/Fw9jDMVCkUNHDpm5mVkbHMDLX345/+7f/QHNZovx8UnanYhGs0mjsc7KSpUkTfE8iRSQxImt3bB1nlYKKQVh6IOxdV27E+N7kiDwAYPnSVxs5XewQGC0rReNMni+IY5igtCnEIR5nekSpf1dBozRYAwI8KTED2xzEicJcZyglEYpRaPZYr3WZHW9zvjYEIVCgcrAMG+/9sf5yTe9hiAM+Tf/5rf5/Oc/b2xt6bFz5y7K5bJQStPptBFCcN111/HFL37xdDA+k49f+7VfY+vWrcYPfKaPTfPyK17Nq658Bb4n2HXGmUxNbeLY8RnmFxaYW1ih0+kgpUAIiXRHq5TSBqE2LoPZ6DKA73lobejEka0bpf25rPkx7igx2EDKTm0pwHg2A0rpkR3i2rg6EwHC4Hm2kTGANgaZNTnaYJRGAGEY4vsSISUmVXhSYoxmYWGZVGlKpSKTE6OMjgwxOjLCv3jXe1hcmGOt3ubee+7hnrtuZ3BwyIyODnD11VcL4JQIxFMmGC+44AIqlQr/8A83mlazyfDwCGeccQY//7M/z5VXvoIojlheXuXbN9+OVinGgOd7FAoFd4SCERoDKNdESBsugEYrTZoqZOCjtCZNUkqlog3GrPHQBiHJ6748QA15x40xhIGHsOczWpu8DgXyDt1og9ZgXJZVSpMqhZAS33evTGtXHtgaVUqPQPoopZifX2JmboHAD7ngoksZKF9Jq5OyfdsOmvVVarU61WqVw4cPm0suuUR0Oh327Nlz8iMgJ9sL+vCHPwzAVVddhTGGL3zhCxw7dszccccdZvfuR7j2rT/N5/7Xl/iL//kpLr30Qu68+x5u/e732bf/IEoppOcTFkI8z7dQij0X8V2dmHezwkaSVhqDwZMS7SLL9wMajRba2IDQprfE7taAnhQuO9pA1EaTJClKKbQ2SCFsRnbQTgYN2R8XeTC32m3iJMkDODvWpRAI6TKzAM+zzyelh+cC86Hde/jeHfewMD/Da151BX/xF5/iM5/5PFdf/QaOHDnCAw/cb+bm5syf/dmfYYzJu+7scz7dwDyFx9VXX83evXvM0tISxgje9e73cu7ZZ7LrjDMYGBji2PFpmq0OaapcoyFcHSbwPWkRZG07atfHOnjGuMCAW2+7g2Ix5O0/9RMcPjJtA9ZdfK0Nge9hgChK8DyJ73WBZ/u8Ju+Ks09TK+2Oa5kf7ELabJgd6wZBFCWuhDAcm1ngvvse4FWvuIxXXXk5u/ccJPA9hMhwyew5BanSqFQjPYHneRhjO3mAMPAZGCizaWojq6tLHD50hNvvuIevfeV/Efo+Y2NjbNuxQ9x5552nj+mn8rjiiis4cuSIuf/+++lECZe99ArOO/ds3va2t+MJweLyKsdnDtHpdAgD32Ud6QBm42o8bL2GvYBaa7SDZoSwF7evE8mPXIPEQjGedMcjxl7sHhDaHp8GY8QJd7bIYSXhxjv2eTWp0q6eBCGx4HgWnK5+VUoTx0kOHxkHKeECUWkHoqPR2mbJvAgF4jhmaanDymqNjRsmueiSl7Bl206EaVOt1rjv3rvZvXu32bZtG+eff7741re+dToYT3z88i//MslaQnGiyM0332yq1SpKKd587Tv55V96Dzu3TnHg0BEe3neIVFlQOgwCtNEOw+vWZwbsNMTgajwbJJ602cwY93WXpqIoot5o4fuSwPcAC3ynWYYTFuQWNiZI3RHcDUzXVWNA99SFRjsYyN4M7U6HUrFkx3zYzl1rRRQrkiQlSWI6UUyaKjxpO3xjbOaVUrpywwax1tlECPu+svpSSoQwqDTlyNHjlJeKnHPmdn73d3+fmbllfuff/DoHD+xjbXWNIAjMxz72MbG0tMSf/Mlx4Is/2sF42WWXcffddzM6Ospff/Wvzdr6Gp1Oh6GRDfzVJ/4bU1NTTM8ucsOe/aRpgvQ8Qinz8ZpJjbtgtr7qHqHa/r8xaFd7aW0bFZnDNTaLqTRleXWdvQcOu7rRZh2lbO0nHGAtXQbWWuf4ZtaJZ82L6Zm8SCGRnr0blMMhPfdcWiviOMbzPMIwoFypUBkYpFIu4fuug3c3lRTdrO0OfYsCSJCeyI9prQ1pkuQYZ7EYorVi995D7D1whDN2bOEPP/Yxbvn+vXz8j/6Ar3/ta3z7298223fswJiHhRCCD3/4w8/r9OZ5qxmzNx6GIVdccYW57bbbGB8b55fe+z42btzI5ZdfzrHjsywsrdBqtQmD7lTFaN2FYkz3eM6agmy2nOExnhRoIPA84iRmZnaBeqPJnr17UUpx/gUXMT0zRxLHJGlMu1V3kIqhE3VIoogk7pCmict8Wd9n+o97FzQYG6B+4OMHIb4f4ns+QtojuVAsMzQ8kY8cPSmYnZnmrDN3sXXrFprNJrt2bqdYKKCUQmndnd44eEopRRRFFEslWxMbQ5oqDNha11gUQXoeaaqolEtMbZzADwLuufMO5hcW+Oxn/8oNEK7ihhtuENp9ruJHLRgB3vjGN3LLzbeYdqeN5xf4Zz/103z4d/8tS0vLHD0+Tb3ecJnEEEUxYRgiBCitUKkmCH20ysZutpEQQuRNhO/bmXC90WJ2fhGj7Rx4aXkN3w+Ymz3G7PRhNm3ZweryPCpN6URtlpfmCIIiCAt0R1EblSY5OcLzA1sSaIPWynXI0v6REowhTWO0VgjpEwShq+9sAIdhgZHRCYqlCr4fEAQhM8cPsWPXuWzaugulUqY2TBAGNnNu2TxFMQxJtcZoi1emaUqcpJSKRTsLVzpD1vF932VwjefZpkwrjTaG4aEBzty5g2KpyB//6cf56le+hNEpY2OjvO51V4svf/nLXHXVVdx8880/Osf0b/7mb/LlL3/ZbN26lSDwqQxNsHnrTo4cPcqhw8fR2k49AFKtSJUicMHmCQm+DQbjAiGDRaSAQiGg04lYWq6yuLzKwuIKcZySakW7WUOnCa1WnbXVFeamD7EwewSEJCxWKBRKTG0+g0plEGMMSRyxvr5MoVgm8AOkq9GyJiVrzXWWvVwA2+NZkSYJcRwzMjJBWLREjajTotlssLy0iEoTjFGoNEEIQxy1KA8ME3U6Wa/O4aPH2bl9K2Ojo4wMD1j4xwiKhQL5yNsYpLSZMKsnTQ+oLj2BJzzq9Qb7Dx1ifGyE4fHNvOSylxF3GtRrNXY/vNvccsst4jWvec2PRmb8xje+wc0338ynPvUps7CwwGf+5n9xyUUXcXx6ms98/qtUaw1e++pXEHiSVFvcDrCjOkdEyIkJbqSXNS9h4KO1sR339Cyr61XS1JIKmo0qRw/vYXV5EYNkYHCEUqlCvV5lYHCYcnkQY3TOG9TaZpXlpRnSJOa88y91GKBApbaelFLkWVIrRZKmaK3wPJ8gCJDCZtXdD9zJ0Mg44xObMEa532HrUikkzVYNrQxhIaRZr1FdXyEMfcbGN7DzzBdTKpVBCIIgYGrDBJs2bWRyfBStNEma2m67W5XYJi21DVAQ+CRJivQkhdC3NTRww7e/y/r6Or/zG/+Sc84+m6987et88Hd+k3POOoc/+OgfCIDnmnzxnAWjEIJCsciWzZvNoUOHuPjiS/ngBz/EyPAwzXaHZrMNwN9+7QaMEbzqypciECil8jomDH3SNLUZ0JMYrXPybLsTsbi0wvTsAiuraxTCkE67wfGj+1mcnyWKYyoDwwwNj+F7gWXTeB7V9RWCoMDAwBBxGrvxHe7ih1Sry9Rr65Qrw2wYH+DCc3ewZdMGBgfKpKkiTezoMAgCPN8nUZDEMcdmFrj1rkeIooT11SWGRyYYHBpBpal9P67GDYKAWnUVPwgZGBimE3WIozZx1CGOOnTaDUCzafN2zr/o5Whj8DyfSrnApqlJdm7f6jiYylHaFEHg47mbtcvFtJ1+IfT5/p33s7Ze5Z1vezPNVofBwQE2TU2yd+8jfPCDv02n02Hbjp3MzcyIVqvF7//+7z8njc2zHozZkP4Vr3gFrXbL7H54N694xZW87W1v5/Wvv4a9+w9y/PgcnuexY/tm4ijiH276Hqura1x68YUUiwVSpdFKUSyFNju5KYUUtk5cWFhicXmF+cVVlFIsL8wwc/wA62vLlMoDjIxuJAiLBEHogGmFMRrPC2g2aiRpxOjoBpRyWQaBEeB7klp1ldWVBbbseBGvv+Isfu/X3sbQ1PlUBgctqSLp2PGi9BBeAEjiqMnqzG5+9fc+yYP7Zpg7foCR0Q0MDA7nnbj0pMMlAxYXZyiVKpTLA6QuW2b4YbvdoNNuksQdhDD4vs/Z513C0MgEpWLI1IZxNk6MUxmo5JS0QujnY8qszjVG0+5E7N1/iOWVVf7Zm1/P1IZJjk3PUyyGbN2yidGRYT7xiU/wne/8I7Oz05x33jkEQUHce++9z0kd+axz2Xfv3k0QBLRaLXPs2DHK5Qr/7t99jEsuvpQ9e/dz6Mg0ge9jjGZxaRUhPV503lncfPNttKOIbVu34HmSJE2RwgNj8DyPQhhQbzS574HdHDk+S6vVZnV5lt0P3sH87FGE8Bif3MLEhi2EYcFliKzWc92u75MkEbX1VcqVwZwYkU9zEERRm06rwbbtZ/Cic3bxlre8CTlyNloW0f4AFEYhHEH7gyhRRMkysjROseDz3Tse4vjsMkvzRylXhgjDUh4g2RhRa0V1fYXBgWF8P+wOux2IHwQBlYFhBoZGSZOUqNNmZvoI9aq90VarTeYWlgAYHR2iVCygtQ1KA/k8PQh8Ht5zgIOHj/OeX/xpNoxPsOfAERCaOEmZX1ylEPi8/po3YLThwQfvZ3FhESm9j0RxdP3Bgwf58Ic//KwG5LM+m/7CF77AG97wBrO0tMRll72Ur3/9W4yNDnP/gw9zfHqOouMOag2e57O2VmVpaYXf+L/ex8palTvuvAetFGEQutoxpN2JeOiR/Xz/zgeoNTq0mzXuv/sWHrjndrSCqS1nsGHTDsqVQVSa2IznslGX6GrZ3kFQoFgsQT6Hts1IFhLFUgWEoNls0GjUiRpLhF5K4GsCz+BLjS8h8CRhEBAGBl92iOqz1Ot1Ws0GQViiXBnqn4lrG2xR1KFYLFOuDGKM6ju0LHYq0CpFpQnDI+Ns3noWG6e2s762xh23/QN7HvoB7XaL6dklbr/jXh7avY8kUVQq5XxC5Qchd97zIAcPHuYX3nktoyMj7Dt0BN+TOUzlSThw+BiP7NnLNW94A5/+zOcICwXm5ud47Wtfa4wxXH/99Y+5vnFKZEbP89i3Z4/53u23c8kll3LttT/FhRdeyMzcIguLS262ahyIbUdeAuPqywKBJ9mz7wCNZouJ8TEGB8osrqzy8J4DzMwuUltf5vDBhzl6aC+ddofNW89kZGxDTlzATUcyckO202LcHgpAEIbESYQxGt8PHKbXrXONMawuz1MoDlAqlVFpwtLiAtPHj3Hs6FEOH3iIA/sf5tDBQxydXuDg3gfZv/sebr71+9x+zyHm5udI4ojRsUm0Vg68toQJ3/OJOm2USilXBknTtK9+6t2jyZjiWYM0NDJBoVhmdXmJ9dUFmo0q0gtptROktJ99uVwk8AP27jvE8vIKr7ziJZx3zlns3XekC4NlkxxXNlRrdQqFgNGRERCCpcVFHnzwAW655ZaPvO7lr7v+2uuuPTWhnQ9+8IN88i8/ydDQML/0S/+S17z6Nezes4+jx2fxfS+fKviu2NZKWeKDgEOHjvLKV7wM6XncdMvtlAolJibHeHjPQdIkxaiIh+77PlEUMb5hCwODo2A0aRJ3pyMODM4upIvPnI9oHNNGJQlaKQqlAUt8xXIedaoxRhEUSiiVcnRmhT/95A0MlouUywWktO8hSVNH2AAhPFKtqVZrdNot2+D4Qd5ggOlbX0jc602S5ATamMzDMWf1ZjcIBoymWKywefsZNGprHD20l+r6Cpe+7NVMzy0yM7/EuWftpBAGPPLIXl7+sou4/OWXcd8Dj9ij3DjUIE0tXio8yxSSHkePzeFJyS+/91cwGj772U9z1113MfDagVOvgfE8jxdf8GKzZ7fl0H35y3/Hls2bOT49x94DR+w4Lies2g8/SVNbD/qeo3xJ4iRh29YtHDp0hL/53JfYun0XoDi470GOHNrH5MZtDI9MAgalUgc8n/DWTHcOTQ9xIWNhS+lRr9nGZ2Rsg90xSVOiqJXvssRxTBy1u8csIq89yQi6GavbHffGGLKtxMrgCIEfYoymUCy7aYxd+lpdWWBwcIRCsZyXE7jJSZYdM4JHdiuJXjKINni+jwFWlmZZW5nn3Bdfws4zXkSSJBw7dpRfee8vsGvndh7avR8/CBBAmiqCMKATxQ6pCHoII/ZlnLlrG8PDQ9x9z1389m/9Bhs2TLJx45R48MEH4aqr4BmuH5/xYDTG8Ja3vMXc8YM7KBaKvPeX3seP/diPMTM3z8LiMs1WhOzh82lt8HxpO+R8HdR+LUkTjDFMz86zb99BFhdmOH50H416laktZ+XA9GO9q+z5uocdOWyTLVplx3irVafRqLkxW5qza4KwkAPqdsPPBp4nPceqMf2/X3THgVlgagdNgSDqNDEZsxtDEIT2JhgZIyyU8ufT+XhT5hBQxh7PZuHdVQb6PrdGY535mYNs2LiVDVPbGZvYwEXnn8OuHduJHXM8m2r5vkcnijHGuGDsfjbGJYQXnXsWQejz5S9/ib/+q7+kXC6zceNGG5Ana2a86qqraDQafPSjH+Vd73qXWVhY4G1v+xk+/vE/5Qc/uJOjx+eI4yS/qNKzE5Q4SSiEYc43VPlCk2CtWuORvQdJ0pRGdYVbv/NNKoOjbJza5jJSdzYsejKhNqY/UHrrR2F/TxJ3aLebOdSSJjGlypCjdkmk8CwT3PRuBfYuZ2UZknwOLISh797IFrLcNKbL5lE506fTrtsuGvCDgEKhTFgo2kAEO17MXnuW5MUJl87Vodl7TtOU5cUZok6La378rSgtKJcLXHbxBRSLxRxNEAI6nRgQBG7/x1WpeFKSpIowCNiyeSPnnHMW73zH29izdw+bN29mZmZGCPHM5rJnpIH5whe+wH/6T/+JP//zP+cDH/iAOXr0KO/4mZ/jfe/7VxyfnubAoaOOXeI5Xp+98+K0i6llR53SBk8K6o0m9z/0CFrDzLED/OB732Z0fIogDClXBvs+UEm3Jszqqfxj1doyb4A4jmi1GrSaNeI4crvLIaVSGa01fhDgewFGa7RROQ+i91i3GVc7jqS2fzcGg3Zf62Yq03N098I1Qgg83ydNYwyCcmUIEKRpQuxuEu0wzyAMLWPdTZ6y3qxbC3fjMuN2SiHsMRz47H7wDsbGJxgcHGN9fY0NG8ZzzqVSXdqd1toSSky3tAkDj1Qp6vUmvid43dVXMz19nN27H+brX//6RxYXF6/XWj9jkM8zEoxf/OIXectb3sKnPvUpMz19nFe/+ire+c6fZePGjdx5z0NI6XXBVwdWZ5xQKV0X7WheUgparTYP79kPwPzsUR6453bGJzczOr6RdquG5/kUCuWcT9jtUHuP54xXCFGnSavVoNmsobUiCELCQhHfjfKyGs9uCXqAJbs+hZrEBkXfBmAvo9twYqq0R71tTpLYNjfS83IIxvcDhJQW7O600MoSMfwgzI940c8ZskwiIfIsXquugITJjdtQyjB9bD+DQ8OUB0ZYWlxmeGiQQhjajjrDPE13kJARkYzLxtoYms0mLzr3HHzfZ3Z2hr1793L22Wdf/4pXvIJPfOITJ09m/Mu//Evuvfdes3v3boyBj370Y1x04UXce9+DdDqx28jr5xza2ks63qG2Iz4pabc73HXvg2ilmD5+kLt/cAtjk1sZHhl366QlqutLlMqDjyo2TL4oZS96HLVpNNZotRpIKSmXBwiC0MqKQF+9p1RCmqZ4XoAxCqMV2ijWV+Zp1NdoN6u03J9m9veG/W+71f1aq1nNv7edf886UadJGJYc51FhtLE4ZxgiPY9s0SZbWchuljRJaDarJElEoVjOT5L8ppYib2yk55EkkRs/TiKEYGBgCOkFHNhzPyNjk/hhmfmFBSYmxvOmJSN8KKXxPemYPjKPdqueoZiemeOKK15BIQz57ndvJk2Sj1x0wQXXf+h3fzcfcDxvNeN1113Hi1/8Yj7zmc+Y2ZkZRsY28R//48fYODnBkWPzrK6t4weeA1ZtM5GkCt/zHIVeE/h2Iy/DHO+85wGazQ5rqwt8/7s3MrFhG0PDY91jCMHy0gxhWGRsYiNKpfnOilbK7aMYGo112s26ZdsERcdD7LJZLAwj3VGrSOLIddVxXsBnW3rPWIEuZc8HLgjCMkMj426+7rsatNuN20DwUColjjukSczA4IiFsTAYrRCeZ8eX7vNZXVkgCEJGRiasUIAjGK8sz1KvLvHK176Z0dFJPAlXvPzSXKaliwDofDigUm2XwNzx3Wp12Lxxgq1bp3jgwfv5rQ/8BhNjo5x/4UXcdNNN/+Qa8p+UGXfv3s0PfvADjNEfieKYX//1D3D5yy7j+OwCs/NL+eK79OxdlroaRcru/oZwH6JWir0HDlOtNVlfW+SO797I5NQORkYniDptVlcX8DzfZowgpNlYp1As43mBDUhtEFLQ6difB0GpPGjn0Tle0d3sM8bQbtaoVZdoVFdotxsoleQ1Xm8DJJ6pW/yEWlKlMZ1mjWZznThqIaQk8As5uzzf6/E8wrCI9Dzi2BIphJQEYQHjeIpSSvu1TovR8Y1IT9Jq1llemqdQKDI8PI4xMDd9kPHJKYKgRKvVZGhoCN8P8hpUmy7SYDCkSUqcJPnarjKK8dERNm/aRLPV5r7772OwMsiv/OqvXP+8HdN/9md/RqlU4kUvehHHjh3/yObNW/jt3/4tjk/PMTu3mCP6wu1vGGxNGPi+yxIip9f7UjI9O8+xmXnazRrf/+7fMzq2ieHRcXvsrK0QhgVarbo7agvEcUyrVadYLLsLrVlbW6bTalB0vMR+GMeN1nRCs7FObW2RVqtmA5kuBPRcP7K6UqUJUbthWTpCuHm6zI9gW097+H5IksY0G1W0UnmNKYWg0ahSrgxRLJZJkojq+ip+4NOor1MqDzA4NEKtXuP4kT1s23k2tXoLz5OMjQ6Tter5ioW7eTpxQieKKZeKTqtI02p3GBgY4NKLL+WGG76JHwT883/+89ffcccdz+1sOtu3PX78ON///vfNl770JbO4tMbrrvlJBIa5haW8M/M8S91vd2LAUCgE+TpABicWw4CZhUX2HTiCMIrv3XoDxfIQo+MbwBgW5qcpFgtcfNmVCAML89MopSz/0NVdUafF8tIMYBgYHMX3A3u85lo3EqUSVpenWZo/Rr26QpomnGwPY4yr+eZZmD3M6vIsWqdZUWFxWaMoFEpUBobpRE1WVuZc92ynSKVSGaUSZqeP4HseF1xyBZ4fsLw4i9GKjVPbMXjcfvM3CIKAI8dmWV5ZtWsd+SqvcOuvgjAIqJRLOaHX8zzqjRYHDh1hw4YxXvryV7F//z5u+NYN5hd+4Rf+SbPrH/qQf9e73sUXvvB543kFfvEX/w9e+coriFJNvVYnTVUOPCNwhbGXTw56pmEsr67x0O4DKKW4986bWK9W2brtbDwpWFyco1gssnXrdoaHSuw9cJzVpRnGxjfgBwVazTpNB1b7QUgQFCzEki3AC2lZOWuLpGl8Ugbgkz2CsEgQFhkZ3YCQnoV8XBdsx4hxDq4PDY9RKg/QqK/RqNeY2rydc8/YzLG5FWanjyOkZGR0Em0Mc9MHmdywkYsuvRKM5tKLX8zgwIANSNEl6dIDqJue7tvzJBPjoxit+PwXvsjXv/a3bN+2haPHjv3QteMPxdr5zne+kzccZ59zHq993esYGh7h+PQ8caLyKX/WcHgOuM1mwXaiYRW7HtlziDiOObDvARYW5ti67WyklKyvr5KmEQPD47zpmlfwxx9+D7t2bGdgaJS1laWceJskkT3WCkVAIwz4nk+aJlTXFlhZmqbTaT5vgfhPKemFECRxh1ZjnZXFadrNqmMf+XlDWHBz8ziO3Pw7ZWV5nsrgKFe+9Hw+8ae/w+tefQWVwWE67TqdTgtPSjZtPZMjh/ZxcN+DpMqw78BRtyDWDUKRQ2+ZMKobd7px4vzCMls2b+L1b/hxtu86gyiK8gz/nB3TH/rQh8yXv/Ql0+lE/ORb3sTWrVMcOnKUSrmIdKh+6iYbJq/FLAzhOcA7TRWP7D1IuxOxujTP3t33sW3HuXieT626RnVtmampbbz0onN5//vfx/mXv4Xf//XrmNq0BS/wmZ05SJLEDA6NobVyJAMLe7SaVdZX5mjU11AuCJ+vzTPzTzy2s0cUtVhdnqVeXXZz8mx1wb6/gcFR6vV1po/uZ3hknPNfdDa/+5u/yOSul/BbH/hVXn7pBYyMbmBtZZ4oivCkx84zL2D3Q/dQXV+i3Yl5eM+BLnsq06B0L8Hz7SxdOzZ5hs8+uHsfl192EVe96koWFhfZtm2bueCCC34o+ZSn3cDcfPPNjE+Of2R+do63vv2dvPpVr6HR6rC0uOL2kSFNUntHeTKfCGSYip1Fe8zOL3D46Awqjbn3rlsYG9/C4NAocdxhdXmebdt3cf6LzuFj1/8Wm7btwKQNDu7bww3fuZNGvY4UHoWw6Lb0lMXmwiLNxjprK3OWOPECU4kWCOK4TRJ38PyAQqFE1Gm5RX8Pz/Mt61x4TEyM87orzmPDlh0MDI1x/nlncM99D9HqpFTXligPDBGGRZROmTl2gG07zqLdSSgWQwbK5VzzR2aEY9GF2m1S8fA8QZwklIpF0tSwsLTEkcOHkFJe/7//9/9+doPxrLPO4pWvfCUryysfWV5d4WMf/RhTU1McPHgE3YPJhWGY7x2LHjqXdkyXJEnZf/AISikevO92Go0Gk1PbiaMW87NHGJ+cYuOGDfzhv/9dXnTBpWAMSwvz/PqHPs4jux9EKcXA4AgGjRDg+yHtdpNGbYVadfkkDaRn7pm0Tum066TKNjeFYgUhbD1XLg9Sr62yvLrO8YUGb7r6cvxwkA1TWzjnzO3c+J0fkMQdVpbmKJQrlMvDrCzNUa+tsmX7GSwtr7JxcjwXypJS9JBCLFbqeV0ChzaGKIq4+OKLGR8f5x9uvIGzzz77+mvfeC1333/3s3NMG2Oo1+vcesstZu/evfz4m99OsVBg3/5DdOIY6SYqIh9RWeA0zcTdnZJrGPo8su8AzVaHxflpZqePsnnbWWiVsrgwTXlgiPHxDfzbD7yHSy69CKUU1bUl/v1//K/s37+HJI4olQfdXJe8U27WV2k2qidtVjPP+DMZmvU1Ws11eyGlb4knUZvBoTGiVo2773uYj/+XTyJ1nTiJednlL+O3f/U6JjZuJQgLLC9MA7DjjPOZmT7K4twMxgiOz8z34LPdObgT8+hpamx93mp3WF1d4ewzz2TT5p088sgj5u++9XfmqquuenaCUQjBH/3RH1GtVjn3nHP5V+97L9VanUazhVK6CxBny+ruWJYOK7PL5z5z80usr9eJ4w57Hr6XyakdlMsDtFp1CqUKGzbt4s1XX8qbr72WJIpR7QX+/P/9C2789m3UqusMj07mvFOBoN2qU11dIE1inmkWycn8MO79J3GH6voCUdTKV2Cl5zE0Msn66iJ/8+Vv8Rf/868IRZM4injnz7+Nqy8/m7GNO5CeR7OxTmVgkI2bdrJ39z2kKmG9WqPRaOL7dlKmlCKKY4dnyu6ECOyuthCsrlVJleb/+o3fpFAosLS4+LTJE/KpZERjDO9+97v5/Oc/bwaGhtixcxeT46PMzi+RpEku35YFY+/0wvNkPsg3xjA7v0iSKI4d3kejUWNkdAKtNa1WHa0SfN9j/7ElZg8+SODH/PWnv8inP/9Vjh7eS6FYyV+TkHaZqVFfJXLE12dzP+PkzLYW0G83a7QaVQeMS0f4kPhBkeljh/jEp/83N9/494ShYXF2nvWWwZdgjKDdaqDSlOGRCdbWVjl+eB+NRptDR465phC3DtJVO8tEplwFie97NJptavUmL7nkQsYnJimXSrznPe/hoosueuZqxptuuolvfOMb1Ot1/uHGGz/yylddw1t+8q0MlIssLK5YoSTTz3LpDchMm1BKyer6OkeOzRLHbe6961Z2nHmBZR4bOzJcnD9Op1Wno0KOHz5MdeEYf/7X3+T4kYOUysN4vt/TmBiW5o+gevZGfpQfaRKRRC0GBsccvU3l5OC11UX2Hl7Cby/y6S/cyA/uP8jssX1U15bYsGk7vu8jpKRUHmD66F7OOu9COlHM1IYJp0lpAy5NtRMM6C61Kd2v1jY2NkpqCtx15+3s37/3I77vX7+2tvbMBOPRo0fZvXs3F198MQ88+OBH3vrWn+Liiy7i+MwscZzmzOZMBzGr1jMBT7e5gedJDhw+xtpajb0P3430C4yMTloRJ2MolQYplsosLc4jMSxVY265cw/TRw84LeuKXUbyA1Qas7Yyf9KA2CdLeaC1IopalMqDeH6A0Qo/KNCoVVlbX+Ouh2dYXGuzMHuYtdUVNm87k6GhkVyaJQgKRFGbNE0Yn9hIHMds3DCeK3YopfrIxhnUkyWiJFXUajXOPeccjh09zIED+9m4ceP1y8vLz8wxfdddd3Httdeyf/9+g5Bs3bINKSXLy+u5z0kuC5fJFLvZMw5PlBJW16q0WhFRp8HqyiLDIxM9daZtQgaHRpmY3MTC3HHWVuaZnz1GFCcMDg67/RCBShParTpx1D6pxngnQ6ed6fi0W3W7aOU+r6HRCdqtJvXqGvPTh5mfPcro2ASVyqA9WTJZaM9jYHCM2ekjtFpNVlbX6XQ6bqzbQ+p14zOd6Vwak/NSG40WQ4NlduzYCUChXOBNb3rTMxOMl112GQ899JB58MEHed3Vb+KMs86l3mgQhAFSWCX+OI5zWboMrc8gHbvH4XHoyHFa7Q4zxw8QFgeoDAzZXWU3XsqYOyNjE4yMTbCyvEjUaTM4NJrTo6T0qFdXqVdXXlDNinmGs3R1bYFms5qzbzwpGR6ZoFZdYW1tibGJTYyNb7SfuxQIkwndpwwMDdPptKmtr6A0HJtecOC6Iggs8ThVqV3PcNdZaZ3v7Xiex9LSMhe/5Ap27DqHPQ/vMfv27DHPSDBWKhVq1SoDAwP8n+//FVbX1lhYXLGFsptZhkGQb86pVOe8OFtjQCeKrPhlmrK6skKlMuwYzPSJbGYd4sTkZsqVISoDw7YuSRWeF9BorNFu1fI56bOJBT5RrJ/Mt0E2R27W14ijNr4fWhKFNpTKg5TLg4yMbcxxwr435JLJ4NA4hw7sodNp2ZXbTmTHt6myXjrSapJr3XUBwxg3mZHMLSwzNjbKT7/97URRRKvVEf/kYPzwhz/MeeedR6sTMTw6SalUIIoiYjecV1YoG8+JU2aNS5I6ox5j8D3J7NwC7XZEdW2JNNVUBoZcnXKi0KZ9jnptDeOMJY2jTsVxh3aj6vQQn/0M9USxfir07EqlNBvrJHHH7XdbbSGVWky2O4TOZjvdbc2BwRHq9XXqtXVa7Yj1ao3AWdhZRrhdpLPqvr1qvXadRKkU35OMjo4xPrmJWCVm165dP1wwZnPFYrHI9PFjJk0N511gF+qVSknilFq9SRwnjj1tSJWT7MA4+4kUz7eSxbV6gzRNOXJ4D74fUCiWugtuJtd5sEVwHNFs1gkLJUeqsJ14q7FOHHe6HnwvmInKs3NbCSFot2o0G+u5eytY1dx2s279cvpAIsf71JpSuYLnBdSrq0jPY25hgThJMMZOzxKVqZ4pp6dufWyUVnTimEazTbW6jhcUufRlr6XVbLK0tGSe7FN7QkWJZnMdpRSDQ8M0Gk0+/v98kiiKUamjuzsxpZzV4SR/pZD4ziPPUth9kjhhfW2VjVM70crqBRoD2lG+snFTvb5mfZZ9382cLTDbqK9395KfwYAyz0AWfaaf+5k6roUQNOvrFAplCsUMjfCRvpXhG5uYcuq6spsQBBitGBufYm7uOC86/1IajTZfv+HbJE4z3PM8pCfxPd+tkGiSJOmPBa2Joph6o5Yr6F533U8/oVvXEwbjy152JX/S+c+cc84Z/Nx117KyuobBqg+EQYDBEHXsi/CkzO1vkyR1d6Lg8JFj3PLd20jjNpWBESqDw5aTl+07my6zJ00T4iiyWVFZTRk76lvrWfc8ORuHk/Mot6dWo76ary0YrQmCkE6nRZLElimer+SavJYslSvUays88shDlMsDXHP1qykEAcpowjC0bhNuz9167mSyzRmZWdHpRCRpytyR3VTXV5/UNu5xg/Hnfu7n+OIXv0hlYIjLLruMH7vmKo4dn3ZHsmUEh2GQC3f6nk+SxHZPwtmPpYnG83weeHg399+9m8rAsN14y3aNtc7dSxF2tCc9Dz8IUGmKVimtZpU47jxvR/GpPNPJDpGo06LTaVIsD1rTJj8gjiM67SaVwRG64vUi3w0vFssYYN8j9/HyV1zNBS8+jy2bN9Bq22tRLISkqSJJVK6dni26xYk1DY06EZ4XcPN3/p79+/Zy+fnnMTIywle/+tWnV/qcddZZ5vjxY/z4m9/B29/+VkrFgP2HjlqpYqVpd2KCwFqi+b5N3Uop6g2rUROGIY1Gg+MzcxgDt91yI9VqjdGxcYZHJmwhnKYoR6uPO22Wl2bzD0cKSatVZ3VpJseyTpYgPJWCNMMEjTEMj27s2SzUdDpNJjZuw5O941yrCLy2tki73WZycoKXXv5ahgfLvPjcXTRbHeLYYpPFohXOz7x5gtBDayfg5Zxhz9ixhX2Hp/nm17/CfXffxlnnnCseeuCBp9dNt9ttoijm3HN2UC4XWV6x0sRpakXUBwZK1hwoDGzX63ZNMiZNMbRwT5Jq5uamabXanHHOBSitmT5+kDhqu27ZoqlxHOH5gb2jHW6lMyGk5/jSmydpWk6lbGlOwCCFkPn6gDaQulMnEyZN04SlxWn8IGTzlh0sLS5QXVuiHcU0WnYrUXoe5VIxv/7lUgHft4GYZcgwCAjDgOm5RTZPbWDTxgk6nYh2p/PD44xjI0MUCiG1eqNHY8apr8pMGVXkgkWZf7LnO1MeIajX1q1kR5oyOraBoaExFuePU6utEYQFQNDptOzfM8XYdpPa+vJJcfVPxSB8rAlRvbZi98JdwPi+T71uJ2lBELK+tsLy0gzDI+OMj09RKBRR2tBsNqjX6rRakW1gejiNff14pmKmNdKB7Z1OxNBAhXLZqvYWg+DpQztWYk7kRpAZhuR7Es8ZNnpOdSAn0To4qFQICXzbbavUrgQUS2XXpKQMjYwzuXEbtfVlqmuWRh/HHXzPzwPdrhKoky67nFoQzwnYY5qQJokVVTDGMr2VQivF6soCrVadyQ1bKZYHSZIIKT2KhQKZvEoQ+BQKIYVC2PXudvInGc6Is1dWTosIrNqZfR574j7eSoJ8rHHS5z73ObO6usbbr/vnnHnWubRarR64gD7zRGOstmIUx3iezBH6diei3YlpNKoszM8xNDSWF7hpEhMEBSY2bCFNY6rVFbdIDpklxcnK2D4VAfDex9rKXC5QagWfFIsL02it2Ti1FT8I8jWONIkplioc2L+POGqjlbb4sewaLEm3dNfLc7R2cnZWHQaW2LJ959lceOkrmZ2ZMTfddJN5ypmxHbVRaco5Z59LkmpWVtet+aOrB+1fTI4zArnigO+2yWwBa5VkW60GxVLZ7gDn82tNEBQYGpmwAp1Jkg/tlVL5ItVJ2RScwmPxNI3zqZZWCk96+EFoPWqyIzbDCjEMDo/SaNTsSqxLPpn0cteHxw0n3EjYy/irTvOoVm/i+QU2Tm0iimOidvSY3ILHDEbhrGs3brAaN3Ec47uM16sMa53tdZ6abbnXXdK3Jt2SQqFEsVByNafo60mT2L6wYnkAbVLSJHIWvCc/ZHIqPqw/trYWdCqlWBpAq5So03I656JP1sX3fALfYsqFQsGKQuVL/l1h4K4jV9cdSWCJE50oxvM9KpWKZfj48qnXjEopm8E8jzhOiOI4L1B1niHtHeL7HkHgxIfcRbLGORbuyeqJPmvm7A7yfWdXhnOVKhBHbdaWZ04uaOQF9PsMhrWlaeI4IgistHOSJJaJ43mILp3bnWJergxSqZRs1+w4BLg9aulOxcz4KDv9pLSMcGO0FXbogZmedjftuxdhmwqrRCVwxt05Dd0du6IrgI6BQhhQKoZOn9u3bGLnICoz3T9tSNIEz/ddgEqCsGjVs35Ea0LzLEdlpqLr+36e5TJyA91Q7BsPCs8aYxbCwNoguxIsE2Qwps++pq+DF5DbjHQNkp5mMGamPVI6ASds55w4QNO4u6xXQTZ7aKMJAp8wDFBuvuxJvwuq9hjb21mn7yQ77A706ceT3wX/1Fg1ussJ6CpUdG3k7Nkr8Dwfz/MRCCrlkp26mW5wWe3NHrHWzOPG9RW9ekeiZ279Q+GMSjk6GNZsu9Xu0Gi1EK6TOvEuMNmdkB3lmZKs6P+g7fK97nZ2JnvR4nQg/pCxKp7Gz/V+zn4QksSx86ERfXvuWd1v4R0fz9mNWMaO7D6pscGX7z65+tTWoV1V4Sd6yCcDSzOc0XMKpp1Oh1qtQbPVdi+yWytmMneB7yOFRfizOyibX2Z3hZBWlCmKOgRBwXkinzqQzqkOM9VrmRKbwJe+HUo4SKf3ybLrlnEIhLRNSRiGfeiCcHtPWcWWpimJqxPFCUkr/x0nloVPDGGIvqBEKYaHBm3Bm6o8Y2bYo+hpN7PVaeXWHTOtQUugJZcxztZYtdEoZeXtTj+eufrw8QI0jto9AqGuCXHjXJvZTE7ly/beu+xwkSeWbLyYH/lZDaqNC0wnYN+zvvx4x7T/RPhFJmSZF5wCKuUiaRLQaHccZUjmUiZpqsCxduwLM853RPbdFb171ZlgqEuX7nv16Uh6BrDQE/sE0XdMd91Ws0yYXe9sf0lK68+TCf9nI0CtNUlis17sLI67gqw43LlrGoC2NeqTVWDyiTKitdPVXXcmA0mi0EC5VLAFKt1F/9R5ndhu2OTtf9++hbszMuAU+jPqqU3aOrmxUHNisslr/X7h/yz79f57V7zfBlbqlMhazY5rgmQOHWW2c704ZMYIf9rBaEtBkXdKaWop5hnGmDlceVK649V219aGTBAGfp4Bda6lLXOMSTxewWNOh+JzDWga0ytbaC9Engl9vw8tieMktw422NHg8PCAnea4KUz25NKzK/lJLkkonrTFesxgzBWI6eKIuddIT/Bk23yZll/mo2x6POgMIpdODhxUZE64V7vHtHlKHeHpfvuZP9O7PjbO2Eh6+XEupWcnbUL0WNZlOo7dmpG+4Zr9tzS1UKDuQVQer2v2H6+Lzp7by8eAoi8Qeg3Cc+UIYzBakLjmJtNq8TzfofHihKAWvQtqTznMTmfPZ66R6X6guaFwz3HdE6xOmlpKge9J54qLWzF2P2MkSnexZ+j1Vuw59uTTGAf2gte5R57udsC6B3IXTuouM8ip1RvgnA20Nl2ZvNxKrOt8KqAveZ/GGJ8HyKePa2ByZpYQ/cdqFpwi4yf0qkv0JLGs3srs7Hy3uNe71fl4paP/RA0MBrsX63akLQzQ40wqukumSmva7Q5B4OdSydmdYb9X5p4mUnl5/ZmPEXtUrk61DHPq7sqYngPJaSblNnemW4L1ZDmtdW4oBZaDIJ3UST4e7Dbojy7vbDg+zQbGBVheD2Ds0n5uqtPfuSVxQrPVplS0FHQpbGbVWjuMqisgmh0H3Yqxy6U+mYms5nkqG8Sz9jwu+4meJf4e8ybXc+Y3W748B04Etv+puhI3XcKtXUUxLqm5BpineUwbYyxbx4n6CKDdseyd7m5sd8wjPcnQwABJqnIqWZcFbBzPTebafplyVe6jjOkLy3/yRX8BnfjmWXqeLCtmGbCXpGHNNbvmo1prtDK5/GEhDPC8bmBmzH/tnGWTOCFOkvxYzkw4bR/+NDKj7aYFUSchihO7OmAMxULozCfpOf9tpvSk3XmRQtBstYnjFN/L5ppZjeFkMFwjY4yx1LIeXMs8g1fwsUrQ01Xp40Wo6IFx+pDH3G4jA72zRJXBdbm9m+kSJYLAwxOCZrNFHEe5RucTXYHH7aa7Rt92rcDiiB4puIkLSNGVNLHUc2sAbmV3E9od601yIlGiD0419B3Rz2T99aTA72lIp9uYiBN6BtGNhSxzWvUxu58Uxwm+o5YFvsQg86Yl4zamqbLEbF8AupuMnv4xbYfdwi19CyGpNZpYN9AQz/fQxg7Si8UihUKBYrFAHKcEQUCSpLQ7kVthNM5Zvr+YtWxh09P1nw6V5zQh9rGzRbdW7Kkhc4hHWEuVtbUarU7M0NCgI0QkSCdlg1s1CEO7Aej7PhPjo3hS5oD5E9Hk/Ucf0ZozzjgDMHzjxpsZHR0jiiK3gyUIfCuRkaSp5SL6Xi6Jls2nU6VsIev5rK2u5qC3lb1I+8ToxQlty6kajqdcR90zi84q9gyCySAe3/Oc8ahgdWWZz3/5axa2M5ogCPB93znQkmdFYwyBHzhuqv23OE4wwOzMMdtde6JvZPi4wSiEYOfOnRhj2LJpgtGxCbTjrklHH0qdjnZGatBKoYyx4p9C4vs+pVKRZrPN8aMHWF6cJ2q3GJ+colwedIi+ygVAM0/BUxkm+WFKjOfzvZ5YT2dHsz2W7cpIrbZOs1GnWl1nYnKSrVs22lUFbQjCwAamSu10xg1BMvZ4Xp5lRFzfR+oO+x82OVvoSTPju9/9bm699WYGB4d459uvZXLjlN2X8P1cMFIpWxckibJOqQKiOMETkjS1CmNDgxWmZxdZXl6htr5KuTLAsSP7GRoeY2BwhHJlAD8Nc2yq92g4VTOVeZq/25wsKd3Vhr5n10Ma9XXmZtaJk5jJDVOUy2V27jqTX37PL1AsBKyt1TDYmtCTVt4kS1Se5wzlXW8hhaATxXTilAe3buLWW/6eKIp4//vfzwMPPNBnz+GfeHd86xvfMO1OxL/61x8gUXDv/Q8RRTGBn3nVqTwNWE5bt5vOmp5Ox641rqyssbi4QKFYZuu2M9kwtYXq+hory4usrixSKBSdzot8NBv8JIFDfpggP9WOa+lbq7dabY1Wq0GhUGTTlm0MD4+ClBw5uI+1tTWOHpum1eqwsLSM73n5URuGQdeAKjt+heVAWmwaOnHC0kqNV73un3H37TeSpqnZvXu3eMLMWGs0UEqzaWojtUbTHclWIjfT7NZaEScpYY9UhXa7is2W9bILwsDJm0hHtlQkScrI6DiVyiDV9VXq9SqpStBthReEXRr7jwDmdzI8PEf7ajfrJGmM53ls3LiZoZExgiAgTuI8UaRpShTFFupTmtD38ZxXZLaglSUjY4yDA60oWBwnSAmlYkipXKbZatFqtp68mxbCNikjwwPEThg001fJ5E7UCYTLrE5IlSJOEoQUFAKfUqmQd+LZ3kS700YbzdjEBsbGJkiTxOl9JyRx50fOWOh5u6kMRJ02cdQmCAsEfsDE5BSVwRHiOKLVapEmaZcaJrJ1gyC3d7Z9hMMaZZcHaYwdbFjBWM+qlhkYqJSRztg0uxGeMDNmClWlUpFmO1vQ6ToSZJ1ysVBw/9/V8m61O4wOD1mKke90WLTKC1bPKVjFcUwUNYnixLnKD5GmKe12/TmXv/vRxRhBSI9iaYAgCNFKEUcRxgjC0CcshLmiXDZ1ySAbYzTVepvhoQEHZJucr6jpis4Ld1RbrZ0A5UqCx9udftxzMU27i9eeZ0m0SyurqDSTQLaAdyYK5UlBpVTMlQYytF3pbCHLz1cVM5Miz/MwAuI4IkljpPRfcEvzJ/PD9+0qcRS17Uqxl6mLdVdDPM/D97vrqTiV4lKx4ObVqg8WzAzTVapIk9ThjiHS8yw7/Ak+c/+JuivhmDm2ZrCm1/nijjB9MhcgKBYLaKWcla/IjWpEDynT0tB7ZDR611yNfv6W5n8EUe8+vFd0QW+LM2ZNarcMswt29tqWy0Vnr6LATd96H0orBBJfQBC4JlU/MftAPtaLzIPHMbyN25ndsmmjxRmdUWKfgaqTusgsN2zWtKurjtDYNSwSsn/U5NxAn06mOj1jfqZPBnMCaGpyFRAcTAP9bC0hBcr0jIR7Vhl8zwLfSlleq864h0/AzJInIqE5o1tmHDaNVhrccpahS6TtJ8VmWU/koGouCGS6yziiG730eidnH405ndGeU9Db9ISlEDJfF8hR3+x65axtRzFzX7L7TuLRo96e5IM7ZeWJQ/AnOqZ7vy3T3csDTGQG5iLX0zF0Ay+jGdlFLJEj+ieaMOXqVXkVLfI1x17u3OnHc5wZHWtbA76gS4Z21DLDCaQKN8r1pJevl3SPfKdCl9WSSvc1yH13w1NpYHI90FyDz/R1uaZn7SD7ZqVMz0qj665O6JoyvtuJr6dLdT9lz7lTrWR81Bvpozk7hn7vimpWYmUboxkXIWt2tPsZrbuuWZYWKHKdMHNCHD2lYLQUsWzHReSSuRnpoS+SXPrWPVR0HJlS9K2MdfckHh144tSMK3OKZ8SsnHIlWZ87rlOgzVZBhdPyzv2mjbFy18ZgjOhxO6NvV15m/EhzYqZ7kmA0vbTz7I8UyN5Ouy+92+mLUobA94mT1HVXoueIFj3riyavOvppY88/iexHrjwwpqf6664J5IQycUIiccx+bYxjcdsd+azwkl5vR06Pckh2FBoeg8j62MFoTgjK7goiuYRuvhOd/4xb5PFs9sy8YbKVA210v1ml26PpelieLhSftxtP9NZLotsbPMZD500MObastMY4zNgYY70kHcG6Z8erf835CQYa8lFn8wmdlt36ytr2TMi5qx5gMgmU7O4QMn/hmN7awf5EBhlB/xZiX3F7ujR8bqLRdINE9GxpCtEnN5F/vzWvtPRBzylGSCn6pi2ZVXNvTHU5/OIJZfEe55jOOmq7EZatqRptyOvPLOAEPTre9t+SNM0FRYWbRYoeZVtxCh6SL+zE/Tj0vXzXWeSy2RY31D3WGyZf2gsCPw/EfEVZ2rjpVUDOlCueENrJgiUTjheiVzfHyVsIThD16VlNNHaM2CsikBXEWf2p6W679B71T5cLeDJnUHMKvdjemi53MOiZimXNjMGQJsrFRU8je8I7z3qTjEyR6X/3NayPMxOUj1fYWqWwR+cFfWKUuzehlKFaa5KqlMD3+t2T8vqzh9mh+wrRF0wGOmU8BR/jrskW83vFGXK2tqZH3En0BVhvPAjRFQHIyjbhxObJYB54GtYbeTq1aTnTWxSPEbQmE4pPEjpRtpLoZpU9knnZNEg8CsvqT9mnx3zPcRoXPY3oibijc1jtmlHRN6XrXr9uLOTIjekKycq+Dvrxpeb8xyrTewNECCxJNsMH3Znf/WWCOE5otzuMDA9QCMNcd5F8j1Z3X2U+Y+pJ36cj8HnJ4L3NiuhzrTC2Ixb9Wju+56F6CLRRnDofQdEX2Do3C9A5xbD3eZ5SA9M3BTE9qlQ9ssh5N+S+LU2tZ0ylUs45jnZZ0GZDmb9ZQ9/aUraJZkwP3nX68ZyiA9mlyIzoc3xYkm/lZ4EiPcfY6m4PxnHM8dk5azrkeQ5GFI+CcLQxPZM40zPvfoLMaHpNKT2ZE2IzQUnTu3Cvu6uNmfiPrSmzRW4vL3SzOXcmq3sikcicDsTnGbAy+fAimzP3s3ls6ZXtRWeBXCyEjAwPorXFGG3TovvA8kyxNt+H6Tt9n7Bm7H5Lmii00T11gOjrwHIVW6fX57kUr7Wx4pA9+GJf52a6XVo/E+R0xfjcn9Wmh0dgr7/OZ8w9MN8JZZcFvq3ezsTYCJ6UjtfYtd7oCoQZtFJ9jc/jRaP/eNBEkiao1C7rZ8HoSTd/FAK/x//NTltsk5OkqTMy6krndYkWNlMaRa7fmNUrpxUlnq/O3wFrgj7/ln4UxOSKcr24ndIGowxh2F3Mysi52bJ/mig83wl+iafpA5P/Km0XqLLAyv6O6LpqatPfg+WSab0D8RzGMU59wPQxvE+Vg+yF+nvNCeVbns20flSHrbV2JlW6h63T/RlDNq3rSh8mSqE1OcE2H3qIp5AZsxcUx7FbxBYIz8dzUxjRk357Rews3cxmTKVVl/OYy2f0SPSCwzBNP0xgzEmXG80L+veanCfYP4o1Pbrs7poY0/Xwcb1A3mOIrkmW0QaEQvrdaYzWGgX5PtTjPfzHL2mNWyNVeNJ31HKV8xtz7KkngLJNsU4nxpOZG7tjiPfgUP2EC3NqGzg/y9nRPKvPL3qmMF2kJBtJ58e17hpWJklKmmp833cNSf/8WghyjR2MZYJHUYz2JFqlfRO8p5QZLT1cOuUpgwjsWqM9pUW+nGO3Bk1uQplp74RhSDtK6EQJYRDYJicIEB1yN85eKzjRsz9x+vHcZUdzQn2oe2rEbMVEOBKE75b2PZdY0tSKP9l4oQdJsaupqdJ4voeHhzHC8h61saalT7WBkZ5HFCfc/8DDGCOdL3HgHFZF3iXFSYLve7kDVhaU2lGJtNHEiaITdYjjmNr6GmCdD3LD9HwRq4uYnmaTPT91qXWlsDYb9lp7RFGHOI5I05RWq8WDD+5GKU290QKceKznOT1GTRQnxHFCIQxQWufaPVEUE6cprXaHmZlpUif69eTHtBAkScy3vvl1BgeHsMxtD20EqbK+xGmSWCzR85x+twGtMWirneP5YDRKGZaXl+m0m1TX1+wyd6lCWCjh+T5JHKFVSpLGj1roOSkvnuCFZZyUje20XbprNmpEUZs0iUmSmKjTQQiPOIk5cvgAMzNHkRg83yUnYcW/kiRB02V+IwSe65wLhQIqTZ2xZUynE1mo56k0MGmaMDAwwEd/79e4cPhWUjlFW0wSmGWmivv4k68OsVCtUCwIQl8yv2a44twqP/saybH62WA0Q+YAsbeJv7+rzh/+179jy9atbN68nfXqGr4fUKtWWV9bIUk6JHFMkkR4fpB7IJ/EsNwLCGI0RFEbz0tRKkVrhR+1UcqC11ObtjA0NMzo6Bj79+1mvVrjD/7te3nZ9mk69QUa4sWErLKxsI9P3DjE3rmQYmgFwJSBWjPht34qYWBoA8vtKYr6AOnK7Xz7u0v86d/px7TfeIztQIEwCRdNHmZ7uESjtYw2glrb8OlbDAeOKtpJi8AzRCpg+2jMNbtWmJAeXrGDSSKIZ5FyEVUTdBKbLcNCmeFh6aYzPsPD43Q6LRbmj1MuDxLHEVGn+Yypm5w+7p8sy1tF4rBQJgwKtNsNNkxtp1QqWfmaUhHf90lS5WAc2DU4z47KLPXOcerxKkJV+dytPg8e8OikLdbSCIOkEHr8zMvWOXMwRjDPcOEogVmjGqxQa0REiXhMX6JHa+3gIejgtXeztryPdmMFgP/y7a185b5JRiv1XLs71R7veekiZ5XrzBz0COQjaKBSMnznvjU+e2OFcjFACFt/1Oo10FbRCgFxEjvupE3bQVg45SGZU+kRBkXLzNeprfnaLYxWBEGAwZDEMcVS0eKDnk9rdT8r6gCd2jEqFcPf3DbKf75hI8OlaaS0jW+cas7b1OKaM1dI1x0HUiuEhKVl+Nv7R0jSFt6TBaPDzVHG50j9bHaYg4wP1fgft27hhj1TbJ3okKQ+YEh0wH/+xVkumGqz0gwJfdD4FAPN7Lrgr+7YSSrbSJbcHoyw9aQkN79UKs2p6hZQVacj5DnM7qlKCKREG5Gb1Mseoowf+BSLJYuqxB2q0RBNM8hgSXL38Qk+eftWNo52UEoghaEVe5y9WfGff3GdJLXPJf3A9gM65m9+MM56J8bzNEo/yQTGIuMSgWZArjM1kvDfb9nE5+4YY7jYJk7Bk1DreLzl4jUu3NQkVYbQ1wihCfyUtXrKB7+4mbl1SSXUqMwUG8eR7N1ZNL3eh+K0Xdtznt1P2EGiZybt2Ds5hGg0kpiNAwl3HSzy+1+axBdtZ8knaEYeY+WI33jjAoEkPz2NEAwUUv7qe+N86+EhKkGC1nQtWR4vGHsfg0Gdbz0wxFfuHcOTJheCqrUFl+xI+ZVr1tFauQg3eD4UA82f3LiZAwshRT8hSlTXb1r2uG/2BN7p4/T5DfcTZ14ZR1U4sNtobbvnoMRwKeW+I4L/8I2NNGPA2K/HKWwc1bz36jqXbG/TiYxj60DRT/jMbYN8/s4xhssm3x54CqydTLTHUG1F/PfvjNFOBb5nQEgMguGS4ldeN8eAnxAriScNygh8qfjSXaN87+AQw2VFknaDLmd6ZDs07uX0rSacjoynjAk+Y1n3MZSrRZ96hBNvcF6BBdnhcz8Y5NhaSDlQbk0V2jG87bJ1fvbyKusND0+C0vZrc2sBX7hjCBB48onpgo/am5YetCP45E0DtCOFL3XumFXrBHzkpxa4dFubWgs8YUiNZGIw5qv3DfEfvrGRSpigTQ9fx3RNjuRjHsM9vPLTEfncHtk9+9I5W6d3OUZ0F6vSuMFX7/Q4vFRhpGxssAnDUt3n/W9c5Z0vrTK7KvGlQRtBpag5uhLyy5/aTjMJCD1NqniUdN4TZkYJpBrWmhLhxDuF9FBG8u5XLXHRthb1jkBKQ6oF5TDhnqNFPn37BAMFe2xnchee9CmEgcuIort99nh3+umS8XnLtIYeBZBeGzYXs51I8eCMT5wmOYEmUj6vP7/Gmy+oW7cEaSdwnqdZbkg+fdsI622JkM4UFVDG9cyPATQ+zkKWQBunWisFcWq4eFudX716CaOcTRuCYkFzcCnkA5/fyXJNEnhWVNyTgtBXXHlWmzDwcpN0fcIK5PMNJIvn8HtO/qh0KaJHNS53wM3cUkmdfpINui2jKR/6iSUqfkqU2r0ZbQSBp/jjb27gWw8OMlhI0Qp8T+AJwUVbagyWNFH6FDJj7i2swZea5WbA5buqXP+T06zXpSPKgi8NUaz5T9/azHpTUgo0qTIE0jC35vPOy9f58YtqtBIfzxN9VHbTZw322JdVPCfZ4Jk5Hs2zFKDPSZCfwKDq30XqX3BOlUYKTTOSlMOIP/mZYxQ8SLXzmNRQKST86Q2b+O6+CqOVlESBlJp6W1DyE153dtWVfU9D09uT0Ih9Lt/V4hdeuU6pYDNiFrAaw//9tU08cKzAQCFBaXsnNROfd1yxzhsvrJMo+4YyG68n9zd/dvenn8skbE6i1/uYlbp5Cr9FkO++WEs+TSv22Tau+LXXrzJaNijb24IQlELN1+4b4mv3VQh8hVIGTxrqUcCLptq8+5XLDlN+ijVjb6s1Vkn55dfOcdn2Fu1YImT2yw2f/d4kN+4eYbCoSFX3HjpnY8z7rlpm62hMrHyLtJsT3QG7Wjy5h93px3N6Y+TaSfSLLZxwaPettHqez0BB8fOvrPITl7SIHbCdaEkhgDsOVPjDr29CCmWJM+75NgwafvbKGj/5khpaPf5qsnxs7ElQa6X83luO8qKpDisNn8AHZSQTQ4obH67wiZtHGS3FJNpm0UTb3Yc/vG6Giq9odjwH44jHaFh6nFT7bNpOctbOC66J6audTpShyxne2Um51BD8i1ctce1FayxUfXwfNJKhkmb3tM+H/r8pSkGSB7EnYbXp8Vtvmuf159VZrnv4vkVYpHwSRQkhQBlBMdD85htXOGMyQSuLDcappFIw3PLIIJ+4aQOlwEI4EkO1LZkaSfno2+YpyNRmT7foIHpcDvqo7aLH1ziTXP5RhFeez1tL9Adk7wSmb09JgMbjPa9pcdnOmEbbHr+pAs/TzKwF/NENm1FakJmcaSNoxh4fessK5021aXQy+7ZsP/8pTGCMBt+DszeH+MJ6RSsDhVAzvSr5w69PstKQ+J59wUoLtowm/MIrVrnyjDoSg5TGFbzdFdQTdVm696YAXjhL/KfOu+jpnk3/1Xg07d52z+dtEUwM+Y7Vb3/CJ+VPbxjjkdmAUuCWr4CCb7j20io/cfEyg6Hq7l2bbOTxZNCOsV1OqiVzrQ1oadndYWBIUsHv/90WFus+AwWNQRL4gnrH580X1Xj7pess1XynJiEtxCNS2p22U6LQPamlRzD8NDj9/L7aXkUJkY0C+0XXjVMGWWwO0Ijton6iBAPFmL+4dZzv7htktJyQZiWbkoyUUt5/9RKdjqSTWBFSG0ve496w8rFuayEEyhtF45NqQyAUH//7jTwyV2KgaLOhQDNf9fiXVy/yMy+vsVz3KYUG7bqqA3MB//3bI3ikZDu0uVdILl5uXojn36mXx3tLx5w7kKmQdA3Si7QIpCLVktGK5v+7a5hPfXeMSiEhUXYiV+94nLsx4j/89HzOW5TSYpOrDclnfjBBJ5X43lMmSgi0hkQZBgopf/Hdcb523xBDxRgnrYPSkjdfUOUnL2pQ8lI8zyrShz40Y/jzm8Y5uhwgUT2e0o/z23LShPmRaiCe97zYkxTyEjEzDupZYc2SRiQqdNICw0XFnYeL/Jd/nKTgp05M1hArj7FKynUvW+aMDRGB5xzWhCFRhhsfHuT4eoDu8QV6wmPauMLRS9YYK3f4+v2jfPLWSQYKCVrbMWAnlZwxmXD9WxcYDhPasU3sqYJQJHz876f4weFBhkpJbu+VKd/mOmkn9O/ZbMb8yDQQJ1ldIegPTHq3BcHzBKkYoBRoHjru87tfnkKlqWN0CVfewS+9ZpW3XNhkuW5llmMFA2HK3901yCe/t4GhYvY7nywz5giLZKLc4KaHfP7sH6Yo+ir3AmzFko3DMf/+7cdJUzsWlBLiFIp+zO/97STffGCQ0UqKptdB0+QWwSbPlOJRmo2ns99zHYldHo3pky+hh/JnA67kRUyvwIe/MsV6yxB4lhJWCGClGXDNi9d420tWWWn6FHxDogXjA4rP/2Cc//emDYwU2iTOHFXyFGbTFtqJObwY8Wff3k47UfYIBpTxqBTg116/wGhZESe2djRCUCloPnvHKP+4e5CCI1A67TFr+aZP4M5lcif06pifzn3Pfc1opa37dvH7DC7BGIFKE7xknv964wjH1gpUQm0bFmFYaQT82AUt/vXrVml0PASGREkKvuGOA0U+/b1RAh9nLODU6p6sgTEGPAHtSPOVe4u0koCCnxEsDO3I8K4rl7jm3AbtSCClppMKQplw15ESn7hlM2FgU3Yue9FDJs40d7qL471oq+H0LOb5hKFMn6hTploLdj1Zpx2+eY/k2KrHYNGgkYS+pJ1IXrypzr96zQLjZYVdZzL4vqbaFvzRNyZZbVriDMgu2P1UTIl8z9BOQo4t+xjVcmRbaMU+V7+4ynWXLVkk3bOTmoGCYs9swO/97RYKXoInuvIlcWqDm9xdVfTpe3eLaB5XAf80TvhsHtJOPyfvLvuTRZqm1vhcChA+j8yXiOMIpYxjbvkMFA2/8xNLbBtNqXWkI0wISr7iv920gaPrRSqhIkntcysjH/eDfkyLX09C4Nv0LKWh2vK4eGuNf/vmBRLlIaUlShZ8zey6x0e/sYlObJwPu1Um8CVcum09N7GxQlDWoEhpnavgy9xOWDy2bvhzHEA/SplZO4GunD3l5Oy0W+rXxm5yZstahcDaMUthiBON0DF/8o5ZzpxIaUSCwAMjBINhxP+8ZZQbHxpksKDQSDxhaMeaCzfXGSpqtJZPdkyb3IgoTWynVG/7nDvV5Dd/bJ40NcSJyLssg+a/37KJ/QslQi8hURqBYanm86YLFnjj+atEukAQ+Ll7ghCSIAiQUpLEEUmaELWbtFoN2u3mDxUMp4/2HwbWgU6rSbvVoNWs5eoeUnoI6TkDKZGrExtjaHci0jQh1VZp7v2vm2XbSIdG22bVdgK+l3Lr/gH+5o5RAs+iKRJNteNx7lST15y5TuzgwTTtJzX6YKlf0mnmhGFIHMcIYYvQnZNt/s2bl9g+bqi1vdwnpuAn/OkNG/nH3RXGBlKSVOL7gijx+emXr/DPr1jixgfLeFLQbjXptDvEUZQv6zcadZIkwvesdFqpWMYUijSqS6eD67koRwQMDo0ShAVazRpKKZaW5qjW1iiVKgwMDFEqlcl8qKUULnis6f3/8cpVrjk/phnZryVK4EvNQ8cKfOybmwFJ4Ntf1OoYLtjS5P3XVNl3yMdzEt2FQqHrF6M1/v/4H/+D3/u93zMLiwv4nmF1ZRlt4NixoyyvNXjVyxaYPt5i9z6Bhx31BL7hkbkCf3Fbi2JQp7ZiHRGUlmwYTNjqL/DtO1MemhF02oq52WUazaaT0/AoFUtMbtiIlD6Net3eiVoRJ52eg/eph+RT/m7Rj6udbFEvnslM37/K0kcJowfTNUC5Mky5YhgcHCKOIxqNGtX1FZYWZ/GDkHarSbPZYG7mGO005NIti2zy5vnKbQUGStCOBKk2RMrjf353hOX6HKWCb9eUtUZKuOBFq+zZ3+T7eySNtubA/kcohKERnmRoeJg//uM/EWLnzp2mXm8wPrGBkaEKUnokSqFMQBj4bBgRCOGRxDFSSjwvRBlYqyWkRhL40snjeShjKMgOoSfQzi2rk3qsV9eoDI5TKg+gUoXSmiSOadRrrK0t4fshUnoolbA4e/B0ZnyOUuPY+Bb8oOCMKDXDw+N4fkC5XKFSqZCqhOraMmkaM7VhkiRVSD9g12gNT8dMV4v4nsAIidHQiTWN2KMQehgkOrXH9EBJMj4kqLcM6/UYpWKMTqk32jRbLWrrq4yOjtib5bKXXsm/eM/7OOeMzSyt1mm12zSbLcrlooUnta0ly8WClcFIUlQaOzk8y+T2PA/Pk7TaCcbtu4S+ZHx0gIWldb7/g7s5dvQoa2urRFEHrVKUUjSbdcJCEYGgXluh2ahSGRjpmVsb+nR3jcE8TlZ7bMbJo6vLx2I5mx7iRubi1bWI6M0tPT+X/1PP+oR5HLn8XMHMPEE+fPQb632t/SIHP0QezacpPq1mlbBQZnB4HM/zSNOEQrGC7wcEgZWyGxgcYtfOnbzsspewa8dGao2YNI1tT6FF7owQ+LYnSJXCExZlSZVCgPOJ8YhSp3amEybHRqg1WszOLzG3sMzff+NLHD+yHz8Ti6/Va3z2S/fSaLbsjmwYdq+H1ni5PqPdhUAIfCnt1pfDFDOx0Ezv2fd9SqUiIyND7NvzCMsrKxSLhR5rXys+lCYx9aqlpI9PbiEIi7nabb/nXL9HTb84dA9d7XHJkaZfPcF0yQAGk28w0uOT/Sju84lsI3EiSbUbUI9aojBPDLPk+OuJunu9dsg86t580nPfylZ3YRwhJEGhRG1tkWZ9laGRyfxVZPUcwNzsDJ4w7Nq1kwcefhilNHGSOAMjkUN0NrPS9XpxhgMZUmIwKDd5CYMAbayjmgGiKCGOIzwp8DOHglqtQa1W75lHxplTpYVglMk1c4TLBGnGxsmX9G0zpFSKMYIkTYmiGN/30Fh4IPMezASf6rUVonaTUnmQ8ckt9nt6rIalW5vMYZ8THFr7R1fOPMlJmQkh++K3z7k287zOdKmdu7vRuu/3Z1mvzy20V/n5hJVO0/uzpuvT3B9I2Q1jcodabXqzchb47t+cfvbjZ38n4ormRF8/3JQrCxDc8MEPQoqlMo3qCitL0wRBkVJ50Aq/arvpZ0VDJWmaUq+3nEBX9/mFFLlcshC9gg1dIfksPoSwyse94vRKpXSiOL+5fIBWs8XSyipKa9fOS+shLWSOBWbHhEDkmGD25roeMNo5sHpWQFJpjNE0Gk1bc7o7JUk01fUl1lcWqAwMsXnbWZQHhsHhj5huh9/75k2PZLOUnl2pPWG0aPEz7QwUe9OHyN2d7O8QuaWY1grP8x+1AyLzuXpXZrg3u2bIQp9fc3f5OKdenXgQd1nW9l/txZdd2wpzok6l6CkhepNsRkDR3X/TBqTz5cGKd3bfl7tu2s2HpWRwcISV5TnWVxeYPbaP8Q1bGBgazT//ThRRrTVIHeyDW1sVzrQSpziRS6JkcZIboYmc15ApHksh8X3Li4wcXCSFtMGYKk27HZEkaY/ZeaZKJfM3YuGfXmcNkV+IjBKUpm2k5zng1L7pdsfK60ZRRBzHVNcXSJMOZ593CRMbNhOEBdIk7gFghft9Itf9zgOz6zGWu3f2KfPnGUbmR15mQZZ5JmMMUnrW20Qp+8dYhd5ed6dujWlOKBFl96uiy5DuXb3t1qDihNfaLT9OLEMy/2alVM/3ZEc4j/Lgy54jcyPrOlL1OlF05a1dtObX0l6vhInJKdI0ZnH+ODPHD5LEHYZHJ0mShFarSb3RQqnu55C612ePZ/v5auealhncZ65YiOx92c/Z83xSp2psSVyCNLX1piiVS6ZUGmTbjrPpdFokSdpXA5KvqfTcufSrhuWpWQpbG+RSJvbrYRiysDBHo14l7jQBw+YtuxgYGiVNYvuGPItzCvpNMnvVNow76nv/v/eYzq+9u4hdElK/YICQXRtarVV+hInMN+9xLECE6Aqy02O+I/rqONH3HvJs6VwAer2cMy/u7PW7qb49UegGY34qZZmg53UYDNL59uXOEabXR7rHv8LYqYsnPXey9zqgSdI0odmos7J4HCF9/LDEwOAQmzZtJYqj/vLX2JNT9T1ft+7NHdJ6Sxxss6OUyn1mlNIsLxzH94B3vvOdDA4OmEcxFp6FP1IKI6U0nqUBnf5zEv4RAuP7npFSGimFEc/B7xyolM3b3vY2/n+reeKsIZhhIAAAAABJRU5ErkJggg==';   // 26371.png 터널 (흰 배경은 투명)
        const TUNNEL_SIDE = 0.22;   // 그림 왼쪽 · 오른쪽 기둥이 차지하는 비율: 기둥은 늘리지 않고 가운데 어두운 입구만 길 폭에 맞춰 늘림
        let tunnelImg = null;       // 불러오기 전에는 null (터널 없이 건물 벽만 그림)
        {
            const im = new Image();
            im.onload = () => { tunnelImg = im; };
            im.src = 'data:image/png;base64,' + TUNNEL_B64;
        }
        const TUNNEL_X0 = (CITY_MAP[0].length - BUS_ROAD_V) / 2, TUNNEL_Y0 = (CITY_MAP.length - BUS_ROAD_H) / 2;   // 큰길이 바깥벽과 만나는 첫 칸 (spawnCar 와 같은 길: 가로길 3칸 · 세로길 4칸)
        function tunnelU(cx, cy, u) {   // 바깥벽에서 차가 나오고 들어가는 자리면 터널 그림 안 가로 위치(0~1), 아니면 -1
            const W = CITY_MAP[0].length, H = CITY_MAP.length;
            let p, len;
            if ((cx === 0 || cx === W - 1) && cy >= TUNNEL_Y0 && cy < TUNNEL_Y0 + BUS_ROAD_H) { p = cy - TUNNEL_Y0 + u; len = BUS_ROAD_H; }
            else if ((cy === 0 || cy === H - 1) && cx >= TUNNEL_X0 && cx < TUNNEL_X0 + BUS_ROAD_V) { p = cx - TUNNEL_X0 + u; len = BUS_ROAD_V; }
            else return -1;
            const px = p * MAP_SIZE, wpx = len * MAP_SIZE, sw = TUNNEL_SIDE * tunnelImg.width * CEIL_H / tunnelImg.height;   // sw: 기둥 한쪽의 원래 폭(px)
            if (px < sw) return px / sw * TUNNEL_SIDE;
            if (px > wpx - sw) return 1 - TUNNEL_SIDE + (px - (wpx - sw)) / sw * TUNNEL_SIDE;
            return TUNNEL_SIDE + (px - sw) / (wpx - 2 * sw) * (1 - 2 * TUNNEL_SIDE);
        }
        function cityFacade(cx, cy, side, u) {   // 이 벽 면에서 쓸 그림 번호와 그림 안 가로 위치(0~1). 건물 한 면에 그림을 폭에 맞게 몇 장 이어 붙임
            const H = CITY_MAP.length, W = CITY_MAP[0].length;
            cx = Math.max(0, Math.min(W - 1, cx)); cy = Math.max(0, Math.min(H - 1, cy));
            const a = side === 0 ? cy : cx, bid = CITY_BLD.id[cy][cx];
            let s, e, key;   // 면이 이어진 칸 범위 [s, e) 와 건물 구분값
            if (bid) { const bb = CITY_BLD.box[bid]; s = side === 0 ? bb.y0 : bb.x0; e = (side === 0 ? bb.y1 : bb.x1) + 1; key = bid; }
            else { s = Math.floor(a / 8) * 8; e = Math.min(s + 8, side === 0 ? H : W); key = 1000 + (side === 0 ? cx : cy) * 40 + s; }   // 바깥 둘레는 8칸씩 끊어 건물 하나로 침
            const v = bid ? (bid - 1) % FACADE_VARIANTS.length : cityHash(key, 1, 0) % FACADE_VARIANTS.length;   // 건물 4채는 서로 다른 그림
            const fw = facadeImgs[v].width / facadeImgs[v].height * CEIL_H;   // 그림 한 장의 가로 길이 (비율 그대로)
            const t = ((a - s) + u) / (e - s) * Math.max(1, Math.round((e - s) * MAP_SIZE / fw)), fr = t - Math.floor(t);
            return [v, (cityHash(key, side, 9) & 1) ? 1 - fr : fr];
        }
        function drawCityBackdrop(view, observer, half, eye, proj) {   // 도시: 하늘 + 도로(차선 · 횡단보도) + 건물 앞 인도를 줄마다 바닥 좌표로 칠함
            const { canvas, ctx } = view;
            const width = canvas.width, height = canvas.height;
            for (let y = 0; y < Math.floor(half); y++) {
                const k = Math.max(0, Math.min(1, y / Math.max(1, half)));
                ctx.fillStyle = 'rgb(' + Math.round(85 + 120 * k) + ',' + Math.round(160 + 75 * k) + ',' + Math.round(230 + 15 * k) + ')';
                ctx.fillRect(0, y, width, 1);
            }
            const y0 = Math.max(0, Math.ceil(half));
            if (y0 >= height) return;
            if (!view.fc || view.fc.width !== width || view.fc.height !== height) {
                view.fc = document.createElement('canvas'); view.fc.width = width; view.fc.height = height;
                view.fctx = view.fc.getContext('2d');
                view.fimg = view.fctx.createImageData(width, height);
                for (let i = 3; i < view.fimg.data.length; i += 4) view.fimg.data[i] = 255;
            }
            const data = view.fimg.data, cosA = Math.cos(observer.angle), sinA = Math.sin(observer.angle);
            const midY = (MAP_H >> 1) * MAP_SIZE + MAP_SIZE / 2, midX = MAP_W * MAP_SIZE / 2;   // 큰길 가운데 선 (가로 · 세로)
            const isB = (cx, cy) => cx < 0 || cy < 0 || cx >= MAP_W || cy >= MAP_H || map[cy][cx] === 1;
            const warn = car && car.warn > 0 ? carWarnPath(car) : null, wa = warn ? 0.6 : 0;   // 차가 오기 전: 차가 나오는 쪽부터 지나갈 길이 빨갛게 번져 감
            for (let y = y0; y < height; y++) {
                const d0 = eye * proj / (y + 0.5 - half);
                const fog = Math.max(0.25, 1 - d0 / 900);
                let i = (y * width) * 4;
                for (let x = 0; x < width; x++, i += 4) {
                    const u = (x + 0.5 - width / 2) / proj;
                    const wx = observer.x + (cosA - sinA * u) * d0, wy = observer.y + (sinA + cosA * u) * d0;
                    const cx = Math.floor(wx / MAP_SIZE), cy = Math.floor(wy / MAP_SIZE);
                    const fx = wx - cx * MAP_SIZE, fy = wy - cy * MAP_SIZE;
                    let r, g, b;
                    if ((fx < 12 && isB(cx - 1, cy)) || (fx > MAP_SIZE - 12 && isB(cx + 1, cy)) || (fy < 12 && isB(cx, cy - 1)) || (fy > MAP_SIZE - 12 && isB(cx, cy + 1))) {   // 인도: 건물 옆 12px
                        const c = (Math.floor(wx / 16) + Math.floor(wy / 16)) & 1; r = c ? 176 : 166; g = c ? 174 : 164; b = c ? 170 : 160;
                    } else if (Math.abs(wy - midY) < 2 && wx > 96 && wx < MAP_W * MAP_SIZE - 96 && (Math.floor(wx / 32) & 1)) { r = 235; g = 215; b = 90; }   // 가로 중앙선 (노랑 점선)
                    else if (Math.abs(wx - midX) < 2 && wy > 96 && wy < MAP_H * MAP_SIZE - 96 && (Math.floor(wy / 32) & 1)) { r = 235; g = 215; b = 90; }   // 세로 중앙선
                    else if (Math.abs(wy - midY) < 96 && ((wx > 300 && wx < 340) || (wx > midX * 2 - 340 && wx < midX * 2 - 300)) && (Math.floor(wy / 12) & 1)) { r = 215; g = 215; b = 220; }   // 횡단보도 (큰길 양쪽)
                    else { const n = (Math.imul(Math.floor(wx / 4), 31) ^ Math.imul(Math.floor(wy / 4), 17)) & 3; r = 60 + n * 3; g = 60 + n * 3; b = 66 + n * 3; }   // 아스팔트
                    if (warn && wx >= warn.x0 && wx <= warn.x1 && wy >= warn.y0 && wy <= warn.y1) { r += (235 - r) * wa; g += (40 - g) * wa; b += (40 - b) * wa; }
                    data[i] = r * fog; data[i + 1] = g * fog; data[i + 2] = b * fog;
                }
            }
            view.fctx.putImageData(view.fimg, 0, 0);
            ctx.drawImage(view.fc, 0, y0, width, height - y0, 0, y0, width, height - y0);
        }

        function drawSeaOverlay(ctx, width, height, p) {   // 바다에 빠지는 중: 화면이 파랗게 물듦
            if (!(p.fallT > 0)) return;
            const k = Math.min(1, (SEA_TIME - p.fallT) / 0.4, p.fallT / 0.4);
            ctx.save();
            ctx.globalAlpha = k * 0.6;
            ctx.fillStyle = '#1565b5';
            ctx.fillRect(0, 0, width, height);
            ctx.restore();
        }

        // ===== 렌더링 =====
        function renderView(view) {
            const { canvas, ctx, observer, enemy, wallDist } = view;
            const width = canvas.width;
            const height = canvas.height;
            let half = height / 2 + gunRecoil(observer) * height * GUN_RECOIL;   // 총 반동: 지평선이 내려가(시점이 위로 튐) 쿨타임 동안 서서히 복귀
            const proj = (width / 2) / Math.tan(FOV / 2);   // 투영면 거리

            ctx.imageSmoothingEnabled = false;

            // 화면 흔들림: 살짝 확대한 뒤 랜덤하게 이동 (가장자리 빈틈 방지)
            ctx.save();
            if (observer.shake > 0) {
                const power = (observer.shake / SHAKE_DURATION) * SHAKE_POWER;
                const ox = (Math.random() * 2 - 1) * power;
                const oy = (Math.random() * 2 - 1) * power;
                ctx.translate(width / 2 + ox, height / 2 + oy);
                ctx.scale(1.04, 1.04);
                ctx.translate(-width / 2, -height / 2);
            }

            // 카메라(눈) 높이: 공중에 뜨면 시점도 살짝 올라감
            let eye = Math.max(4, Math.min(CEIL_H - 10, MAP_SIZE / 2 + observer.z * (observer.jumping ? JUMP_CAM_RISE : CAM_RISE) + (observer.giant ? GIANT_EYE : 0)) - (observer.fallT > 0 ? Math.min(1, (SEA_TIME - observer.fallT) / 0.5) * SEA_EYE_DROP : 0));   // 천장을 뚫지 않게 제한 · 바다에 빠지는 중엔 시점이 가라앉음
            if (observer.jumping && observer.z > 0) {   // 점프로 높이 올라갈수록 시선이 서서히 아래로: 서 있을 때와 같은 높이에 상대 몸통이 보이도록 지평선을 올림
                const eyeUp = eye - MAP_SIZE / 2 - (observer.giant ? GIANT_EYE : 0);
                half -= Math.min(height * JUMP_LOOK_MAX, eyeUp * proj / Math.max(70, Math.hypot(enemy.x - observer.x, enemy.y - observer.y)));
            }
            { const fk = flatK(observer); if (fk > 0) eye += (FLAT_EYE - eye) * fk; }   // 납작해지면 시점(눈높이)도 바닥 가까이 내려감
            if (enemy.giant) {   // 상대가 거대화: 몸이 커진 만큼 살짝 올려다봄 (둘 다 거대화면 서로 상쇄됨)
                half += Math.min(height * GIANT_UP_MAX, GIANT_EYE * GIANT_UP_MUL * proj / Math.max(70, Math.hypot(enemy.x - observer.x, enemy.y - observer.y)));
            }
            {   // 상대가 높이 있으면(점프 · 박스 위) 올려다보고 낮게 있으면(바다에 빠지는 중) 내려다봄: 시선이 상대 높이 쪽으로 위아래로 부드럽게 움직임
                let zE = enemy.z;
                if (enemy.noGuard && enemy.z > 0) zE = observer.z * CAM_RISE + Math.min(16, Math.max(0, (enemy.z - observer.z) * 0.3));   // 맞아서 뜬 상대는 그리는 높이와 같게
                if (enemy.fallT > 0) zE = -Math.min(1, (SEA_TIME - enemy.fallT) / 0.6) * 24;
                const nowT = performance.now(), lookDt = Math.min(0.1, (nowT - (view.lookT || nowT)) / 1000);
                view.lookT = nowT;
                view.lookZ = view.lookZ === undefined ? zE : view.lookZ + (zE - view.lookZ) * Math.min(1, lookDt * 8);
                const lookMax = height * JUMP_LOOK_MAX;
                half += Math.max(-lookMax, Math.min(lookMax, view.lookZ * proj / Math.max(70, Math.hypot(enemy.x - observer.x, enemy.y - observer.y))));
            }
            if (observer.giant) {   // 거대화: 눈높이가 올라간 만큼 상대를 조금 내려다봄 (가까울수록 더 내려다보고, 완전히 보정하지는 않음)
                half -= Math.min(height * GIANT_LOOK_MAX, GIANT_EYE * GIANT_LOOK_MUL * proj / Math.max(70, Math.hypot(enemy.x - observer.x, enemy.y - observer.y)));
            }

            if (arena) drawArenaBackdrop(view, observer, half, eye, proj);   // 콜로세움: 하늘 + 원형 바닥 + 바다
            else if (city) drawCityBackdrop(view, observer, half, eye, proj);   // 도시: 하늘 + 도로 · 인도
            else {
            // 천장
            // 천장: 바닥처럼 깊이마다 패널 이음새 줄무늬 + 천장 전등
            for (let y = 0; y < Math.floor(half); y++) {
                const dist = (CEIL_H - eye) * proj / (half - y - 0.5);
                ctx.fillStyle = scaleColor(Math.floor(dist / 64) % 2 ? '#3a4650' : '#33404a',
                                           Math.max(0.25, 1 - dist / 700));
                ctx.fillRect(0, y, width, 1);
            }
            drawCeilingLights(ctx, observer, width, half, proj, eye);

            // 바닥: 건물 타일 (깊이마다 이음새 줄무늬)
            for (let y = Math.ceil(half); y < height; y++) {
                const dist = eye * proj / (y + 0.5 - half);
                ctx.fillStyle = scaleColor(Math.floor(dist / 32) % 2 ? '#9b9a96' : '#908f8b',
                                           Math.max(0.2, 1 - dist / 800));
                ctx.fillRect(0, y, width, 1);
            }
            }

            // 1. 벽: 건물 벽 (처마 + 창문 + 아래쪽 패널 + 걸레받이)
            const boxCol = [], wallRaw = [];   // wallRaw: 박스를 뺀 벽까지 거리 (박스 위에 선 상대를 가리지 않게 쓰임)
            for (let i = 0; i < width; i++) {
                const offset = Math.atan((i + 0.5 - width / 2) / proj);
                rayIgnoreBoxes = true;
                castRay(observer.x, observer.y, observer.angle + offset);
                rayIgnoreBoxes = false;
                const perp = Math.max(1, rayDist * Math.cos(offset));   // 어안 보정
                wallDist[i] = perp; wallRaw[i] = perp;
                if (obstacles.length) {   // 박스는 벽 위에 따로 그림 (아래 반복문)
                    const bh = boxHit(observer.x, observer.y, Math.cos(observer.angle + offset), Math.sin(observer.angle + offset));
                    boxCol[i] = bh && bh.t * Math.cos(offset) < perp ? { perp: Math.max(1, bh.t * Math.cos(offset)), perp2: Math.max(1, bh.t2 * Math.cos(offset)), side: bh.side, u: bh.u } : null;
                }

                const wallTop = half - (CEIL_H - eye) * proj / perp;
                const wallBottom = half + (eye + (arena && rayType !== 2 ? SEA_DROP : 0)) * proj / perp;   // 콜로세움 벽은 바다까지 내려옴(기둥은 바닥 위)
                const wallH = wallBottom - wallTop;
                const f = Math.max(0.1, (200 - perp * 0.25) / 200) * (raySide === 1 ? 0.85 : 1);

                // 콜로세움: 원형 바닥이 벽보다 앞에 있으니, 바닥 가장자리가 보이는 줄부터 아래는 벽을 그리지 않음 (바닥이 벽 아랫부분을 가림)
                let clipY = Infinity;
                if (arena && rayType !== 2) {
                    const ra = observer.angle + offset, rdx = Math.cos(ra), rdy = Math.sin(ra);
                    const cx = observer.x - ARENA_C, cy = observer.y - ARENA_C;
                    const bq = cx * rdx + cy * rdy, cq = cx * cx + cy * cy - ARENA_R * ARENA_R;
                    if (cq < 0) clipY = Math.floor(half + eye * proj / Math.max(1, (-bq + Math.sqrt(bq * bq - cq)) * Math.cos(offset)));
                }
                const zone = (t0, t1, color) => {
                    const y0 = Math.floor(wallTop + wallH * t0);
                    const y1 = Math.min(Math.ceil(wallTop + wallH * t1), clipY - 1);
                    if (y1 < y0) return;
                    ctx.fillStyle = color;
                    ctx.fillRect(i, y0, 1, y1 - y0 + 1);
                };
                if (rayType === 2) {   // 기둥: 흰색/회색 무채색, 둥근 음영 + 위아래 받침 (얇은 원기둥)
                    const round = 0.35 + 0.65 * Math.sin(Math.PI * rayU);   // 가운데는 밝고 가장자리는 어둡게
                    const fl = f * round;
                    zone(0, 1, scaleColor('#f0f0f3', fl));
                    zone(0, 0.05, scaleColor('#b9b9bf', fl));                // 윗 받침
                    zone(0.05, 0.07, scaleColor('#7d7d84', fl));
                    zone(0.88, 0.92, scaleColor('#9c9ca3', fl));             // 아래 홈
                    zone(0.92, 1, scaleColor('#6e6e75', fl));                // 아랫 받침
                    continue;
                }
                if (arena) {   // 콜로세움 바깥 벽: 돌벽 + 아치 + 물에 잠긴 아랫부분
                    const floorT = CEIL_H / (CEIL_H + SEA_DROP);   // 벽 높이 중 원형 바닥이 있는 위치
                    const ad = Math.abs((rayU * 5) % 1 - 0.5) / 0.3;   // 아치 한 칸 안의 가로 위치 (0 = 가운데, 1 = 가장자리)
                    zone(0, 1, scaleColor('#d6c293', f));
                    zone(0, 0.06, scaleColor('#8c7b55', f));            // 윗 몰딩
                    if (ad < 1) zone(0.24 + 0.1 * ad * ad, floorT, scaleColor('#4a3f2c', f));   // 아치 구멍
                    zone(floorT, 1, scaleColor('#7a735f', f));          // 물에 젖은 아랫부분
                    zone(0.96, 1, scaleColor('#2b6a9e', f));            // 물
                    continue;
                }
                if (city && facadeImgs.length === FACADE_VARIANTS.length) {   // 도시 건물 그림 벽: 가로 한 줄(1px)을 잘라 벽 높이에 맞춰 늘림
                    const [fv, fu] = cityFacade(rayCellX, rayCellY, raySide, rayU), fi = facadeImgs[fv];
                    const y0 = Math.floor(wallTop), y1 = Math.ceil(wallBottom), dy0 = Math.max(y0, 0), dy1 = Math.min(y1, height);
                    if (dy1 > dy0) {
                        ctx.drawImage(fi, Math.min(fi.width - 1, Math.floor(fu * fi.width)), (dy0 - y0) / (y1 - y0) * fi.height, 1, (dy1 - dy0) / (y1 - y0) * fi.height, i, dy0, 1, dy1 - dy0);
                        const tu = tunnelImg ? tunnelU(rayCellX, rayCellY, rayU) : -1;   // 차가 드나드는 벽 자리: 건물 벽 위에 터널을 겹침
                        if (tu >= 0) ctx.drawImage(tunnelImg, Math.min(tunnelImg.width - 1, Math.floor(tu * tunnelImg.width)), (dy0 - y0) / (y1 - y0) * tunnelImg.height, 1, (dy1 - dy0) / (y1 - y0) * tunnelImg.height, i, dy0, 1, dy1 - dy0);
                        if (f < 1) { ctx.fillStyle = 'rgba(0,0,0,' + (1 - f) + ')'; ctx.fillRect(i, dy0, 1, dy1 - dy0); }   // 멀수록 · 옆면일수록 어둡게
                    }
                    continue;
                }
                if (city) {   // 도시 건물 정면: 칸마다 색이 다르고, 위층 창문(켜진 창 무작위) + 1층 가게 유리 · 차양 · 문
                    const hc = cityHash(rayCellX, rayCellY, 0), base = CITY_WALLS[hc % CITY_WALLS.length];
                    zone(0, 1, scaleColor(base, f));
                    zone(0, 0.06, scaleColor('#3a3a42', f));              // 옥상 테두리
                    zone(0.06, 0.08, scaleColor('#555560', f));
                    const wu = (rayU * 4) % 1, wc = Math.floor(rayU * 4);
                    if (wu > 0.2 && wu < 0.8) for (let r = 0; r < 2; r++) {   // 위층 창문 2줄 (칸 하나에 4개씩)
                        const t0 = 0.14 + r * 0.27, lit = cityHash(rayCellX * 4 + wc, rayCellY * 2 + r, raySide + 1) % 3 === 0;
                        zone(t0 - 0.015, t0 + 0.205, scaleColor('#e8e4dc', f));   // 창틀
                        zone(t0, t0 + 0.19, scaleColor(lit ? '#ffe9a0' : '#3b5570', f));
                        if (!lit) zone(t0, t0 + 0.05, scaleColor('#6f93b5', f));
                    }
                    zone(0.7, 1, scaleColor('#44444c', f));               // 1층
                    if (rayU > 0.08 && rayU < 0.92) {
                        if (hc % 2 === 0 && rayU > 0.4 && rayU < 0.6) zone(0.76, 1, scaleColor('#5a3a22', f));   // 문
                        else if (!(hc % 2 === 0 && rayU > 0.36 && rayU < 0.64)) zone(0.78, 0.94, scaleColor('#9fd0e6', f));   // 가게 유리
                    }
                    zone(0.68, 0.76, scaleColor(['#d9534f', '#2e86c1', '#27ae60', '#e1a02b'][hc % 4], f * ((rayU * 8) % 1 < 0.5 ? 1 : 0.85)));   // 줄무늬 차양
                    zone(0.96, 1, scaleColor('#6f6f75', f));              // 인도 턱
                    continue;
                }
                zone(0, 1, scaleColor('#c8c2b4', f));                    // 벽
                for (let k = 0; k < 8; k++) {                            // 은은한 벽돌 무늬: 줄마다 가로 줄눈 + 엇갈린 세로 줄눈
                    const t0 = 0.07 + k * 0.071;
                    zone(t0, t0 + 0.008, scaleColor('#b6b0a1', f));
                    if ((rayU * 3 + (k % 2) * 0.5) % 1 < 0.05) zone(t0, t0 + 0.071, scaleColor('#b6b0a1', f));
                }
                zone(0, 0.07, scaleColor('#7b7568', f));                 // 처마(윗 몰딩)
                if (rayU > 0.12 && rayU < 0.88 && WINDOW_CELLS.has(rayCellX + ',' + rayCellY)) {   // 창문: 지정한 칸에만
                    zone(0.56, 0.60, scaleColor('#9d978a', f));          // 창턱
                    if (rayU > 0.15 && rayU < 0.85) {
                        zone(0.18, 0.56, scaleColor('#efece4', f));      // 창틀
                        if (rayU > 0.2 && rayU < 0.8) {
                            zone(0.21, 0.53, scaleColor('#7fb4dd', f));  // 유리
                            zone(0.21, 0.30, scaleColor('#9ccbee', f));  // 유리 위쪽 반짝임
                            if (Math.abs(rayU - 0.5) < 0.025) zone(0.21, 0.53, scaleColor('#efece4', f));   // 세로 창살
                            zone(0.365, 0.38, scaleColor('#efece4', f));                                       // 가로 창살
                        }
                    }
                }
                zone(0.64, 1, scaleColor((rayU * 2) % 1 < 0.05 ? '#6f7379' : '#8b8f96', f));   // 아래쪽 패널 (타일 이음새)
                zone(0.64, 0.655, scaleColor('#6c6f75', f));             // 패널 윗선
                zone(0.95, 1, scaleColor('#2b2b30', f));                 // 바닥 걸레받이
            }

            const boxBars = [];   // 이번 화면에 그린 박스 체력바: 상대보다 가까운 것은 상대를 그린 뒤 다시 그려서 상대가 바 뒤에 보이게 함
            const drawBoxBar = br => {
                ctx.fillStyle = '#000'; ctx.fillRect(br.bx - br.bw / 2 - 1, br.by - 1, br.bw + 2, br.bh + 2);
                ctx.fillStyle = br.bk > 0.5 ? '#3ddc5a' : '#e74c3c'; ctx.fillRect(br.bx - br.bw / 2, br.by, br.bw * br.bk, br.bh);
            };
            if (obstacles.length) for (const b of obstacles) {   // 박스 체력 바: 박스 위에 떠 있음 (벽에 가려짐, 더 가까운 박스에 가려짐, 더 먼 상대는 가림)
                const bdx = b.x - observer.x, bdy = b.y - observer.y, bca = Math.cos(observer.angle), bsa = Math.sin(observer.angle);
                const bf = bdx * bca + bdy * bsa;
                if (bf < 20) continue;
                const bx = width / 2 + ((-bdx * bsa + bdy * bca) / bf) * proj;
                if (bx < 0 || bx >= width || bf >= wallDist[Math.floor(bx)]) continue;
                const bw = Math.max(10, OBST_HALF * 2 * proj / bf), bh = Math.max(3, bw * 0.12), by = half + (eye - OBST_H - 8) * proj / bf - bh;
                const bk = Math.max(0, Math.min(1, (b.hp ?? OBST_HP) / OBST_HP));
                const br = { bf, bx, bw, bh, by, bk };
                boxBars.push(br); drawBoxBar(br);
            }

            if (obstacles.length) for (let i = 0; i < width; i++) {   // 설치한 박스: 나무 상자 (높이 OBST_H). 뒤에 선 상대는 가려짐
                const bc = boxCol[i];
                if (!bc) continue;
                const top = Math.floor(half + (eye - OBST_H) * proj / bc.perp), bot = Math.ceil(half + eye * proj / bc.perp);
                const f = Math.max(0.1, (200 - bc.perp * 0.25) / 200) * (bc.side === 1 ? 0.8 : 1);
                const hh = bot - top, edge = bc.u < 0.07 || bc.u > 0.93;
                ctx.fillStyle = scaleColor(edge ? '#5a3a1a' : '#b07a3c', f); ctx.fillRect(i, top, 1, hh);
                if (!edge) {
                    ctx.fillStyle = scaleColor('#8a5a28', f);   // 널빤지 이음새
                    ctx.fillRect(i, top + Math.floor(hh / 3), 1, Math.max(1, Math.round(hh * 0.04)));
                    ctx.fillRect(i, top + Math.floor(hh * 2 / 3), 1, Math.max(1, Math.round(hh * 0.04)));
                }
                ctx.fillStyle = scaleColor('#5a3a1a', f); ctx.fillRect(i, top, 1, Math.max(1, Math.round(hh * 0.07)));   // 윗 테두리
                if (eye > OBST_H) {   // 눈이 박스보다 높으면 윗면이 보임: 앞 모서리(top)부터 뒤 모서리까지
                    const yf = Math.floor(half + (eye - OBST_H) * proj / bc.perp2), ft = Math.max(0.1, (200 - bc.perp * 0.25) / 200);
                    ctx.fillStyle = scaleColor('#c9944f', ft); ctx.fillRect(i, yf, 1, top - yf);
                    ctx.fillStyle = scaleColor('#5a3a1a', ft); ctx.fillRect(i, yf, 1, 1);
                }
                wallDist[i] = Math.min(wallDist[i], bc.perp);
            }

            const onBox = eye > OBST_H ? boxUnder(observer) : null;   // 내가 올라선 박스: 발밑부터 박스 가장자리까지가 윗면
            if (onBox) for (let i = 0; i < width; i++) {
                const ra = observer.angle + Math.atan((i + 0.5 - width / 2) / proj), rdx = Math.cos(ra), rdy = Math.sin(ra);
                const te = Math.min(rdx > 0 ? (onBox.x + OBST_HALF - observer.x) / rdx : rdx < 0 ? (onBox.x - OBST_HALF - observer.x) / rdx : Infinity,
                                    rdy > 0 ? (onBox.y + OBST_HALF - observer.y) / rdy : rdy < 0 ? (onBox.y - OBST_HALF - observer.y) / rdy : Infinity);
                const pe = Math.max(1, te * Math.cos(ra - observer.angle)), ye = Math.max(0, Math.floor(half + (eye - OBST_H) * proj / pe));
                if (ye >= height) continue;
                const fe = Math.max(0.1, (200 - pe * 0.25) / 200);
                ctx.fillStyle = scaleColor('#c9944f', fe); ctx.fillRect(i, ye, 1, height - ye);
                ctx.fillStyle = scaleColor('#5a3a1a', fe); ctx.fillRect(i, ye, 1, 1);
            }

            // 순간이동 목적지: 바닥의 빨간 원 (내 화면에서만 보임). 바라보는 방향 정면 blinkD 앞에 놓이므로 화면 가운데에 투영됨
            if (observer.blinkOn && observer.blinkD >= 20) {
                const bf = observer.blinkD, bx = width / 2, by = half + eye * proj / bf;
                const brx = BLINK_R * proj / bf, bry = Math.max(1, brx * eye / bf);   // 바닥 원은 멀수록 납작한 타원
                const pulse = 0.75 + 0.25 * Math.sin(gameTime * 14);
                ctx.save();
                ctx.fillStyle = 'rgba(255,40,40,' + (0.35 * pulse) + ')';
                ctx.beginPath(); ctx.ellipse(bx, by, brx, bry, 0, 0, Math.PI * 2); ctx.fill();
                ctx.strokeStyle = '#ff2a2a'; ctx.lineWidth = 2;
                ctx.beginPath(); ctx.ellipse(bx, by, brx, bry, 0, 0, Math.PI * 2); ctx.stroke();
                ctx.strokeStyle = 'rgba(255,200,200,0.8)'; ctx.lineWidth = 1;
                ctx.beginPath(); ctx.ellipse(bx, by, brx * 0.5, bry * 0.5, 0, 0, Math.PI * 2); ctx.stroke();
                ctx.restore();
            }

            // 2. 상대 스프라이트 (열 단위로 벽 가림 판정)
            const dx = enemy.x - observer.x;
            const dy = enemy.y - observer.y;
            const cosA = Math.cos(observer.angle);
            const sinA = Math.sin(observer.angle);
            const forward = dx * cosA + dy * sinA;
            const lateral = -dx * sinA + dy * cosA;

            // 장풍 기 덩어리: far=true 는 상대보다 먼(지나간) 것 → 상대 뒤에 그려서 점프로 피한 상대 몸에 겹쳐 보이지 않게
            const drawKiBalls = far => {
                for (const b of kiBalls) {
                    const bf = (b.x - observer.x) * cosA + (b.y - observer.y) * sinA;
                    if (bf < 40 || (forward > 5 && bf > forward) !== far) continue;
                    const bx = width / 2 + ((-(b.x - observer.x) * sinA + (b.y - observer.y) * cosA) / bf) * proj;
                    if (bx < 0 || bx >= width || bf >= wallDist[Math.floor(bx)]) continue;   // 화면 밖 · 벽 뒤
                    drawKiOrb(ctx, bx, half + ((eye - MAP_SIZE * 0.375) * proj) / bf, KI_R * (b.full ? 1.6 : 1) * proj / bf, b.full);
                }
            };
            drawKiBalls(true);
            // 납작해진 상대가 차 밑에 깔려 있으면 차가 상대 위에 그려지도록, 차를 상대보다 가까운 것으로 취급
            const enemyUnderCar = !!car && car.warn <= 0 && enemy.flat > 0 && Math.abs(enemy.x - car.x) < (car.dx ? car.len : car.wid) / 2 + PLAYER_RADIUS && Math.abs(enemy.y - car.y) < (car.dx ? car.wid : car.len) / 2 + PLAYER_RADIUS;
            // 도시 자동차: 직사각형 상자를 줄마다 광선으로 맞혀 그림 (옆면 창문 · 앞 전조등 · 뒤 후미등). far=true 는 상대보다 먼 것
            const drawCar = far => {
                if (!car || car.warn > 0) return;
                const cf = (car.x - observer.x) * cosA + (car.y - observer.y) * sinA;
                if ((forward > 5 && cf > forward && !enemyUnderCar) !== far) return;
                const horiz = car.dx !== 0, hx = horiz ? car.len / 2 : car.wid / 2, hy = horiz ? car.wid / 2 : car.len / 2;
                const bx0 = car.x - hx, bx1 = car.x + hx, by0 = car.y - hy, by1 = car.y + hy;
                const body = (car.bus ? BUS_COLOR : CAR_COLORS[0]), travel = horiz ? car.dx : car.dy;
                ctx.imageSmoothingEnabled = false;
                for (let i = 0; i < width; i++) {
                    const off = Math.atan((i + 0.5 - width / 2) / proj), ang = observer.angle + off, rdx = Math.cos(ang), rdy = Math.sin(ang), co = Math.cos(off);
                    let tn = -Infinity, tf = Infinity, fx = false;
                    if (Math.abs(rdx) < 1e-9) { if (observer.x < bx0 || observer.x > bx1) continue; }
                    else { const a = (bx0 - observer.x) / rdx, b = (bx1 - observer.x) / rdx; tn = Math.min(a, b); tf = Math.max(a, b); fx = true; }
                    if (Math.abs(rdy) < 1e-9) { if (observer.y < by0 || observer.y > by1) continue; }
                    else { const a = (by0 - observer.y) / rdy, b = (by1 - observer.y) / rdy, n2 = Math.min(a, b), f2 = Math.max(a, b); if (n2 > tn) { tn = n2; fx = false; } if (f2 < tf) tf = f2; }
                    if (tn <= 0 || tn > tf) continue;   // 못 맞힘 / 카메라가 차 안
                    const perp = Math.max(1, tn * co);
                    if (perp >= wallDist[i]) continue;   // 벽 · 기둥 뒤
                    const hxp = observer.x + rdx * tn, hyp = observer.y + rdy * tn;
                    const isEnd = horiz ? fx : !fx;   // 앞 · 뒤 면
                    const side = fx ? (rdx < 0 ? 1 : -1) : (rdy < 0 ? 1 : -1), front = side === travel;
                    const u = isEnd ? (horiz ? hyp - by0 : hxp - bx0) / car.wid : (horiz ? hxp - bx0 : hyp - by0) / car.len;
                    const gnd = half + eye * proj / perp, top = half + (eye - car.h) * proj / perp, h = gnd - top;
                    const f = Math.max(0.3, 1 - perp / 900) * (isEnd ? 0.8 : 1);
                    const vk = VEH_IMG[car.bus ? 'bus' : 'car'];   // 보이는 면의 그림 고르기: 바깥 방향 (nx, ny) 기준
                    const nx = fx ? side : 0, ny = fx ? 0 : side;
                    const vs = vk[isEnd ? (front ? 'front' : 'back') : ((horiz ? car.dx * ny : -car.dy * nx) > 0 ? 'R' : 'L')];
                    if (vs) {
                        const flip = ((isEnd ? !horiz : horiz) ? ny : -nx) < 0;   // 보는 사람 기준으로 u 가 왼쪽 방향이면 그림을 뒤집어 읽음
                        let si = 0; while (si < VEH_SHADES.length - 1 && f < (VEH_SHADES[si] + VEH_SHADES[si + 1]) / 2) si++;
                        const im = vs[si], sx = Math.min(im.width - 1, Math.max(0, Math.floor((flip ? 1 - u : u) * im.width)));
                        const y0 = Math.floor(top);
                        if (i & 1) continue;   // 2px 폭으로 그려서 그리는 횟수를 절반으로 (느린 기기용)
                        ctx.drawImage(im, sx, 0, 1, im.height, i, y0, 2, Math.ceil(gnd) - y0);
                        continue;
                    }
                    if (eye > car.h) {   // 눈이 차보다 높으면 지붕이 보임
                        const farTop = half + (eye - car.h) * proj / Math.max(1, tf * co);
                        ctx.fillStyle = scaleColor(body, f);
                        ctx.fillRect(i, Math.floor(farTop), 1, Math.ceil(top) - Math.floor(farTop) + 1);
                    }
                    const band = (v0, v1, col) => {
                        const y0 = Math.floor(gnd - h * v1), y1 = Math.ceil(gnd - h * v0);
                        if (y1 > y0) { ctx.fillStyle = scaleColor(col, f); ctx.fillRect(i, y0, 1, y1 - y0); }
                    };
                    band(0, 1, body);
                    band(0, 0.14, '#1d1d22');   // 범퍼 아래 그늘
                    if (isEnd) {
                        if (u > (car.bus ? 0.06 : 0.12) && u < (car.bus ? 0.94 : 0.88)) band(car.bus ? 0.45 : 0.52, 0.9, '#8fc1e6');   // 앞 · 뒤 유리 (버스는 더 큼)
                        if (u < 0.26 || u > 0.74) band(0.2, 0.4, front ? '#ffe9a0' : '#ff3b3b');   // 전조등 / 후미등
                    } else if (car.bus) {
                        if (u > 0.04 && u < 0.96 && (u * 9) % 1 > 0.12) band(0.5, 0.88, '#8fc1e6');   // 옆 창문 줄 (창문 사이 칸막이는 차체색)
                        if ((u > 0.1 && u < 0.18) || (u > 0.82 && u < 0.9)) band(0, 0.3, '#1d1d22');   // 바퀴
                    } else {
                        if (u > 0.3 && u < 0.7) band(0.52, 0.9, '#8fc1e6');   // 옆 유리
                        if ((u > 0.1 && u < 0.26) || (u > 0.74 && u < 0.9)) band(0, 0.32, '#1d1d22');   // 바퀴
                    }
                }
            };
            drawCar(true);

            // 순간이동 잔상: 떠난 자리에 반투명한 모습이 깜빡이다 사라짐 (내 것 · 상대 것 모두, 벽에 가려짐)
            for (const o of [enemy, observer]) {
                if (!(o.ghostT > 0)) continue;
                const gdx = o.ghostX - observer.x, gdy = o.ghostY - observer.y;
                const gfw = gdx * cosA + gdy * sinA;
                if (gfw <= 5) continue;
                const grel = o.ghostA - Math.atan2(gdy, gdx);
                const gside = Math.abs(Math.sin(grel)) > 0.7, gback = !gside && Math.cos(grel) > 0;
                let gfr = o.sprite;
                if (gside && gfr.side) gfr = gfr.side; else if (gback && gfr.back) gfr = gfr.back;
                const gflip = gside && Math.sin(grel) < 0;
                const gx = width / 2 + ((-gdx * sinA + gdy * cosA) / gfw) * proj;
                const gh = (MAP_SIZE * 0.75 * proj) / gfw * (o.bodyScale || 1) * (o === enemy && observer.giant ? GIANT_VIEW_SHRINK : 1);
                const gw = gh * (gfr.width / gfr.height);
                const gtop = half + (eye * proj) / gfw - gh;
                const gl = Math.floor(gx - gw / 2), gr = Math.ceil(gx + gw / 2);
                const gxa = Math.max(0, gl), gxb = Math.min(width, gr);
                ctx.save();
                ctx.beginPath();
                let gany = false, grun = -1;
                for (let x = gxa; x <= gxb; x++) {
                    const vis = x < gxb && gfw < wallDist[x];
                    if (vis && grun < 0) grun = x;
                    else if (!vis && grun >= 0) { ctx.rect(grun, 0, x - grun, height); gany = true; grun = -1; }
                }
                if (gany) {
                    ctx.clip();
                    const flick = Math.floor(o.ghostT * 16) % 2 === 0;   // 켜졌다 꺼졌다 깜빡임
                    ctx.globalAlpha = (flick ? 0.55 : 0.1) * Math.min(1, o.ghostT / 0.35);   // 사라지기 직전엔 서서히 옅어짐
                    if (gflip) { ctx.translate(gl + gr, 0); ctx.scale(-1, 1); ctx.drawImage(gfr, gl, gtop, gr - gl, gh); }
                    else ctx.drawImage(gfr, gl, gtop, gr - gl, gh);
                }
                ctx.restore();
            }

            // 상대 본체(투명이면 안 보임)와 분신들을 먼 것부터 그림
            const foes = enemy.invisT > 0 ? [] : [enemy];
            for (const c of clones) foes.push(c);
            foes.sort((u, v) => ((v.x - observer.x) * cosA + (v.y - observer.y) * sinA) - ((u.x - observer.x) * cosA + (u.y - observer.y) * sinA));
            for (const enemy of foes) {
            const dx = enemy.x - observer.x, dy = enemy.y - observer.y;
            const forward = dx * cosA + dy * sinA, lateral = -dx * sinA + dy * cosA;
            if (forward > 5) {
                // 상대가 때릴 때: 포즈 스프라이트 + 앞으로 돌진 / 와인드업 때는 살짝 뒤로
                let frame = enemy.sprite;
                let lunge = 0;
                if (enemy.moving) frame = enemy.poseSprites.walk[Math.floor(gameTime * 7) % 2];   // 움직이면 다리를 번갈아 든다
                if (enemy.guard > 0) frame = enemy.poseSprites.guard;
                if (enemy.kicking) {
                    const kp = kickPose(Math.min(1, enemy.kickT / KICK_DURATION));
                    if (kp > 0.08) frame = enemy.poseSprites.kick;
                    lunge = 26 * kp;
                }
                if (enemy.attacking) {
                    const ep = punchPose(Math.min(1, enemy.attackT / ATTACK_DURATION));
                    if (ep.k > 0.3) frame = enemy.poseSprites.strike[enemy.punchHand];
                    else if (ep.pull > 0.3) frame = enemy.poseSprites.wind[enemy.punchHand];
                    lunge = 22 * ep.k - 8 * ep.pull;
                }
                if (enemy.shoryuOn) { frame = enemy.poseSprites.strike[1]; lunge = 18; }
                if (enemy.flurryOn) { frame = enemy.poseSprites.strike[Math.floor(enemy.flurryT * FLURRY_RATE * 2) % 2]; lunge = 20; }   // 백열권: 두 주먹을 번갈아 내지름   // 승룡권: 돌면서 어퍼컷
                // 상대가 나를 보는 시선에 대해 옆을 보고 있으면 옆모습 스프라이트 사용 (화면 왼쪽을 보면 좌우 반전)
                const rel = enemy.angle - Math.atan2(dy, dx);
                const sideView = Math.abs(Math.sin(rel)) > 0.7;
                const backView = !sideView && Math.cos(rel) > 0;   // 나를 등지고 있음
                const hitPose = enemy.hitSprite && (enemy.slideT > 0 || enemy.hitFx > 0 || (enemy.z > 0 && !enemy.jumping && !enemy.shoryuAir));   // 맞아서 밀려나는 중 (승룡권을 쓰고 떠오른 시전자는 피격 자세로 안 보임): 어느 방향에서 봐도 같은 피격 자세
                const flip = !hitPose && sideView && Math.sin(rel) < 0;
                if (hitPose) frame = enemy.hitSprite;
                else if (sideView && frame.side) frame = frame.side;
                else if (backView && frame.back) frame = frame.back;
                const fv = Math.max(8, forward - lunge);   // 보이는 거리만 바꾸고 벽 가림 판정은 실제 거리 사용
                const screenX = width / 2 + (lateral / fv) * proj;
                const spriteH0 = (MAP_SIZE * 0.75 * proj) / fv * (enemy.bodyScale || 1) * (observer.giant ? GIANT_VIEW_SHRINK : 1);   // 거대화 카드: 상대 화면엔 더 크게, 내 화면엔 상대가 조금 작게
                const ek = flatK(enemy);   // 납작: 키는 FLAT_SQUASH 배로 줄고 폭은 FLAT_WIDEN 배로 퍼짐
                const spriteH = spriteH0 * (1 - ek * (1 - FLAT_SQUASH));
                const spriteW = spriteH0 * (frame.width / frame.height) * (1 + ek * (FLAT_WIDEN - 1));
                const groundY = half + (eye * proj) / fv;                    // 바닥(그림자) 위치
                // 승룡권에 맞아 뜬 상대(착지할 때까지)가 시전자 시점 밖(위쪽)으로 사라지거나 순간이동하지 않게, 시전자와의 높이 차이를 줄여서 계속 같은 식으로 그림
                let zDraw = enemy.z;
                if (enemy.noGuard && enemy.z > 0) zDraw = observer.z * CAM_RISE + Math.min(16, Math.max(0, (enemy.z - observer.z) * 0.3));
                if (enemy.fallT > 0) zDraw = -Math.min(1, (SEA_TIME - enemy.fallT) / 0.6) * 24;   // 바다에 빠지는 상대는 가라앉음
                const floorY = half + ((eye - zDraw) * proj) / fv;           // 발 위치(공중이면 위로)
                const top = floorY - spriteH;

                const x0 = Math.floor(screenX - spriteW / 2);
                const x1 = Math.ceil(screenX + spriteW / 2);
                const xa = Math.max(0, x0), xb = Math.min(width, x1);

                // 벽에 가려지지 않은 열을 연속 구간으로 묶어 클리핑 → 스프라이트는 한 번만 그림
                ctx.save();
                ctx.beginPath();
                let any = false, runStart = -1;
                const eb = obstacles.length ? boxUnder(enemy) : null;   // 상대가 올라서 있는 박스
                if (obstacles.length && (enemy.z > 0.5 || observer.z > 0.5)) {   // 둘 중 하나라도 공중 · 박스 위: 박스는 깊이로 통째로 가리지 않고 박스 윗선 아래쪽만 가림 (점프로 올라가는 순간에도 서로 보임)
                    for (let x = xa; x < xb; x++) {
                        if (!(forward < wallRaw[x])) continue;   // 벽 · 기둥 뒤는 그대로 가림
                        const bc = boxCol[x];
                        ctx.rect(x, 0, 1, bc && bc.perp < forward ? Math.max(0, Math.floor(half + (eye - OBST_H) * proj / (eye > OBST_H && forward > bc.perp2 ? bc.perp2 : bc.perp))) : height);   // 눈이 박스보다 높고 상대가 박스 뒤면 윗면 뒤쪽 모서리까지 가림
                        any = true;
                    }
                } else
                for (let x = xa; x <= xb; x++) {
                    const vis = x < xb && forward < wallDist[x];
                    if (vis && runStart < 0) runStart = x;
                    else if (!vis && runStart >= 0) {
                        ctx.rect(runStart, 0, x - runStart, height);
                        any = true;
                        runStart = -1;
                    }
                }
                if (any) {
                    ctx.clip();
                    if (enemy.z > 0.5 && !eb) {
                        // 바닥 그림자 (높이 뜰수록 작고 옅게)
                        const rx = spriteW * 0.5 * Math.max(0.5, 1 - enemy.z / 120);
                        ctx.fillStyle = 'rgba(0,0,0,' + Math.max(0.15, 0.4 - enemy.z / 200) + ')';
                        ctx.beginPath();
                        ctx.ellipse(screenX, groundY, rx, Math.max(1.5, spriteH * 0.05), 0, 0, Math.PI * 2);
                        ctx.fill();
                    }
                    if (enemy.dashT > 0) ctx.globalAlpha = 0.5;
                    if (enemy.fallT > 0) ctx.globalAlpha = Math.max(0.5, 1 - (SEA_TIME - enemy.fallT) / 0.6);   // 가라앉으며 반투명해짐 (헤엄치는 모습은 보임)   // 대쉬 중(무적)에는 반투명
                    if (flip) {
                        ctx.save();
                        ctx.translate(x0 + x1, 0);
                        ctx.scale(-1, 1);
                        ctx.drawImage(frame, x0, top, x1 - x0, spriteH);
                        ctx.restore();
                    } else {
                        ctx.drawImage(frame, x0, top, x1 - x0, spriteH);
                    }
                    if (enemy.flurryOn && !hitPose) {   // 백열권: 반대 손 주먹을 반투명으로 겹쳐 그려 주먹이 여러 개로 보이게 (옆모습은 두 그림이 같아서 앞쪽으로 살짝 어긋나게)
                        let gf = enemy.poseSprites.strike[(Math.floor(enemy.flurryT * FLURRY_RATE * 2) + 1) % 2];
                        if (sideView && gf.side) gf = gf.side; else if (backView && gf.back) gf = gf.back;
                        const gx = sideView ? (flip ? -1 : 1) * spriteW * 0.07 * (0.5 + 0.5 * Math.sin(enemy.flurryT * 70)) : 0;   // 화면 기준 어긋남
                        const ga = ctx.globalAlpha; ctx.globalAlpha = ga * 0.55;
                        if (flip) { ctx.save(); ctx.translate(x0 + x1, 0); ctx.scale(-1, 1); ctx.drawImage(gf, x0 - gx, top, x1 - x0, spriteH); ctx.restore(); }
                        else ctx.drawImage(gf, x0 + gx, top, x1 - x0, spriteH);
                        ctx.globalAlpha = ga;
                    }
                    if (hitPose || ek > 0) { /* 피격 자세 · 납작할 때는 총 · 칼을 덧그리지 않음 */ }
                    else if (isHoldingGun(enemy)) drawEnemyGun(ctx, enemy, screenX, top, spriteH, sideView, backView, flip);
                    else if (enemy.knife) drawEnemyKnife(ctx, enemy, screenX, top, spriteH, sideView, backView, flip);
                    if (enemy.dizzy > 0 && !(enemy.flat > 0)) drawStars(ctx, screenX, top, spriteW, spriteH);
                    if (enemy.tauntT > 0) drawBubble(ctx, 'EZ', screenX, top, spriteW, spriteH, enemy.tauntT);
                    if (!hitPose && enemy.gunT > GUN_FX_TIME * 0.5) { const m = enemyGunPose(enemy, screenX, top, spriteH, sideView, flip); drawMuzzle(ctx, backView ? screenX : m.muzzleX, backView ? top + spriteH * 0.4 : m.muzzleY, spriteH); }
                    if (enemy.hitFx > 0) drawHitFx(ctx, enemy, screenX, top + spriteH * 0.35, spriteW);
                    if (enemy.kiOn) { const kr = enemy.kiT / KI_TIME; drawKiOrb(ctx, screenX, top + spriteH * 0.45, spriteH * (0.03 + 0.07 * kr), kr >= 1); }   // 기를 모으는 중
                }
                ctx.restore();
                if (enemy.isClone && !(enemy.fallT > 0)) {   // 분신 체력바: 머리 위에 떠 있음 (박스 체력바와 같은 모양). 벽 · 박스에 가려지면 안 보임
                    const col = Math.floor(screenX), bw = Math.max(10, spriteW * 0.7), bh = Math.max(3, bw * 0.12), by = top - bh - 3;
                    if (col >= 0 && col < width) {
                        const geo = obstacles.length && (enemy.z > 0.5 || observer.z > 0.5), bc = boxCol[col];
                        const clipBar = geo ? (bc && bc.perp < forward ? Math.floor(half + (eye - OBST_H) * proj / (eye > OBST_H && forward > bc.perp2 ? bc.perp2 : bc.perp)) : height) : (bc && bc.perp < forward ? 0 : height);
                        if (forward < (geo ? wallRaw[col] : wallDist[col]) && by + bh <= clipBar) {
                            const bk = Math.max(0, Math.min(1, enemy.hp / enemy.maxHp));
                            ctx.fillStyle = '#000'; ctx.fillRect(screenX - bw / 2 - 1, by - 1, bw + 2, bh + 2);
                            ctx.fillStyle = bk > 0.5 ? '#3ddc5a' : '#e74c3c'; ctx.fillRect(screenX - bw / 2, by, bw * bk, bh);
                        }
                    }
                }
            }
            for (const br of boxBars) {   // 이 상대보다 가까운 박스 체력바는 상대 위에 다시 그림 (다른 박스가 더 가까이서 가리고 있으면 그대로 둠)
                const bc = boxCol[Math.floor(br.bx)];
                if (br.bf < forward && !(bc && bc.perp < br.bf - OBST_HALF * 1.5)) drawBoxBar(br);
            }
            }

            drawKiBalls(false);   // 장풍 기 덩어리 중 상대보다 가까운 것: 상대 위에 그림
            drawCar(false);

            // 3. 주먹 HUD
            if (!(observer.invisT > 0)) drawHUD(ctx, width, height, observer);   // 투명하면 내 손도 안 보임

            ctx.restore();

            // 기절(공격 불가) 중에는 화면을 흑백으로
            if (observer.stun > 0 && !(observer.fallT > 0)) toGrayscale(ctx, width, height);

            // 4. 피격 플래시
            if (observer.hitFlash > 0) {
                const hc = parseInt(observer.color.slice(1), 16);
                ctx.fillStyle = 'rgba(' + ((hc >> 16) & 255) + ',' + ((hc >> 8) & 255) + ',' + (hc & 255) + ',' + (observer.hitFlash / 0.3 * 0.5) + ')';   // 맞은 사람의 색으로 번쩍
                ctx.fillRect(0, 0, width, height);
            }

            if (observer.blockFlash > 0) {
                ctx.fillStyle = 'rgba(120,200,255,' + (observer.blockFlash / 0.2 * 0.35) + ')';
                ctx.fillRect(0, 0, width, height);
            }

            drawInkOverlay(ctx, width, height, observer);   // 먹물에 맞으면 화면을 가림 (미니맵은 보임)
            drawSeaOverlay(ctx, width, height, observer);   // 바다에 빠지는 중: 화면이 파랗게 물듦 + 안내 문구
            drawLackOverlay(ctx, width, height, observer);   // 스테미나 부족: 화면 흐려짐 + 안내 문구

            // 5. 미니맵
            drawMinimap(ctx, width, observer, enemy);

            // 6. 콤보 표시
            drawCombo(ctx, width, height, observer);
            drawCharge(ctx, width, height, observer);
            drawHold(ctx, width, height, observer);
            drawKiCharge(ctx, width, height, observer);
            drawShoryuHud(ctx, width, height, observer);
            if (observer.dashT > 0) drawDashFx(ctx, width, height, observer);
            if (!gameOver && burnT > 0) drawBurning(ctx, width, height);
            if (shoryuFxT > 0) drawShoryuFire(ctx, width, height);
            if (!gameOver && !tutorial && !practice && roundIntroT < 1.5) drawRoundIntro(ctx, width, height);

            // 7. KO 오버레이
            if (gameOver && !introPick) drawGameOver(ctx, width, height, observer);
        }

        // 콤보 표시: 2콤보부터 왼쪽에 뜨고, 맞힐 때마다 숫자가 커졌다 줄어듦. 마지막 적중 1초 뒤 사라짐
        // 말풍선 (도발): 캐릭터 머리 위에 표시
        function drawBubble(ctx, text, cx, top, spriteW, spriteH, t) {
            const fs = Math.max(8, Math.round(spriteH * 0.12));
            const bw = Math.round(fs * 3.2), bh = Math.round(fs * 2);
            const bob = Math.sin(t * 14) * 2;   // 통통 튀는 느낌
            const x = Math.round(cx - bw / 2);
            const y = Math.round(top - bh - fs * 0.8 + bob);
            ctx.save();
            ctx.fillStyle = '#000';
            ctx.fillRect(x - 3, y - 3, bw + 6, bh + 6);
            ctx.fillStyle = '#fff';
            ctx.fillRect(x, y, bw, bh);
            // 꼬리 (픽셀 계단)
            const tx = Math.round(cx - fs * 0.4), ty = y + bh;
            for (let i = 0; i < 3; i++) {
                const w = Math.round(fs * (0.9 - i * 0.3));
                ctx.fillStyle = '#000'; ctx.fillRect(tx - 3, ty + i * 4 - (i ? 0 : 3), w + 6, 4 + (i ? 0 : 3));
            }
            for (let i = 0; i < 3; i++) {
                const w = Math.round(fs * (0.9 - i * 0.3));
                ctx.fillStyle = '#fff'; ctx.fillRect(tx, ty + i * 4 - 3, w, 4 + (i === 0 ? 3 : 0));
            }
            ctx.fillStyle = '#000';
            ctx.font = fs + 'px "Press Start 2P", monospace';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText(text, x + bw / 2, y + bh / 2 + 1);
            ctx.restore();
        }

        // Burning Time: 시작하면 크게 알리고(2.5초), 이후에는 위쪽에 작게 표시
        // 라운드 시작 표시: 'ROUND n'이 처음엔 커졌다가 줄어들고, 끝에 깜빡이며 사라짐
        function drawRoundIntro(ctx, width, height) {
            const pop = 1 + Math.max(0, 0.3 - roundIntroT) * 2;
            const fs = Math.round(Math.min(40, width / 12) * pop);
            ctx.save();
            ctx.globalAlpha = roundIntroT > 1.1 ? Math.max(0, (1.5 - roundIntroT) / 0.4) : 1;
            ctx.textAlign = 'center';
            ctx.font = fs + 'px "Press Start 2P", monospace';
            ctx.fillStyle = '#000';
            ctx.fillText('ROUND ' + round, width / 2 + 4, height * 0.4 + 4);
            ctx.fillStyle = '#f1c40f';
            ctx.fillText('ROUND ' + round, width / 2, height * 0.4);
            ctx.restore();
        }

        function drawDashFx(ctx, width, height, p) {   // 대쉬: 화면 가운데에서 바깥으로 퍼지는 속도선
            const cx = width / 2, cy = height / 2, n = 30, rOut = Math.hypot(width, height) / 2;
            ctx.save();
            ctx.lineWidth = 2;
            for (let i = 0; i < n; i++) {
                const a = (i / n) * Math.PI * 2 + Math.sin(i * 12.9898) * 0.08;
                const r0 = Math.min(width, height) * (0.26 + 0.22 * ((i * 7) % 5) / 5);
                ctx.strokeStyle = 'rgba(255,255,255,' + (0.3 + 0.3 * Math.abs(Math.sin(gameTime * 50 + i))) + ')';
                ctx.beginPath();
                ctx.moveTo(cx + Math.cos(a) * r0, cy + Math.sin(a) * r0);
                ctx.lineTo(cx + Math.cos(a) * rOut, cy + Math.sin(a) * rOut);
                ctx.stroke();
            }
            ctx.restore();
        }

        function drawShoryuFire(ctx, width, height) {   // 승룡권: 화면 위·아래가 잠깐 불타오름
            const k = shoryuFxT / SHORYU_FIRE_TIME;   // 1 → 0
            const grow = Math.min(1, (1 - k) * 8), fade = Math.min(1, k * 3);
            const band = height * 0.22 * grow, cw = 8, n = Math.ceil(width / cw);
            const layers = [['#c0392b', 1], ['#ff6b2b', 0.72], ['#ffd32a', 0.42]];
            ctx.save();
            ctx.globalAlpha = fade * 0.9;
            for (const [col, sc] of layers) {
                ctx.fillStyle = col;
                for (let i = 0; i < n; i++) {
                    const f = 0.45 + 0.55 * Math.abs(Math.sin(i * 1.7 + gameTime * 20 + sc * 3)) * (0.6 + 0.4 * Math.sin(i * 0.5 + gameTime * 9));
                    const fh = Math.round(band * sc * f);
                    ctx.fillRect(i * cw, 0, cw, fh);                    // 위쪽 불꽃
                    ctx.fillRect(i * cw, height - fh, cw, fh);          // 아래쪽 불꽃
                }
            }
            ctx.restore();
        }

        function drawBurning(ctx, width, height) {
            ctx.save();
            ctx.textAlign = 'center';
            const blink = Math.floor(burnT * 2) % 2 === 0;   // 깜빡임 느리게
            if (burnT < 2.5) {
                const pop = 1 + Math.max(0, 0.4 - burnT) * 1.5;   // 처음엔 커졌다가 줄어듦
                const fs = Math.round(Math.min(34, width / 15) * pop);
                ctx.fillStyle = 'rgba(255,40,0,0.12)';   // 붉은 막은 깜빡이지 않고 일정하게
                ctx.fillRect(0, 0, width, height);
                ctx.font = fs + 'px "Press Start 2P", monospace';
                ctx.fillStyle = '#000';
                ctx.fillText('BURNING TIME', width / 2 + 4, height * 0.4 + 4);
                ctx.fillStyle = blink ? '#ff6b1a' : '#f1c40f';
                ctx.fillText('BURNING TIME', width / 2, height * 0.4);
                ctx.font = Math.round(fs * 0.5) + 'px "Press Start 2P", monospace';
                ctx.fillStyle = '#000';
                ctx.fillText('DAMAGE x2', width / 2 + 3, height * 0.4 + fs + 3);
                ctx.fillStyle = '#fff';
                ctx.fillText('DAMAGE x2', width / 2, height * 0.4 + fs);
            } else {
                ctx.font = '10px "Press Start 2P", monospace';
                ctx.fillStyle = '#000';
                ctx.fillText('BURNING x2', width / 2 + 2, 52);
                ctx.fillStyle = blink ? '#ff6b1a' : '#f1c40f';
                ctx.fillText('BURNING x2', width / 2, 50);
            }
            ctx.restore();
        }

        // 힘조절 충전: 화면 가장자리가 달아오르고, 기가 가운데로 빨려 들어오는 선 + 아래 가운데 게이지
        function drawKiOrb(ctx, x, y, r, full) {   // 기 덩어리: 흰 중심 + 파랑(최대 충전은 주황) 빛
            r *= 1 + 0.12 * Math.sin(performance.now() / 50);
            const g = ctx.createRadialGradient(x, y, 0, x, y, r * 2);
            g.addColorStop(0, 'rgba(255,255,255,1)');
            g.addColorStop(0.35, full ? 'rgba(255,170,60,0.95)' : 'rgba(120,220,255,0.95)');
            g.addColorStop(1, full ? 'rgba(255,80,40,0)' : 'rgba(60,140,255,0)');
            ctx.fillStyle = g;
            ctx.beginPath();
            ctx.arc(x, y, r * 2, 0, Math.PI * 2);
            ctx.fill();
        }
        function drawShoryuHud(ctx, width, height, p) {   // 승룡권: 회전 진행 게이지 / 준비 완료 표시
            if (!p.canShoryu || p.shoryuOn) return;
            const ready = p.shoryuReady > 0, r = ready ? p.shoryuReady / SHORYU_READY_TIME : Math.min(1, Math.abs(p.spinAcc) / SHORYU_SPIN);
            if (!ready && r <= 0) return;
            const w = Math.round(width * 0.3), h = 8, x = Math.round((width - w) / 2), y = Math.round(height * 0.1);
            ctx.fillStyle = '#000'; ctx.fillRect(x - 3, y - 3, w + 6, h + 6);
            ctx.fillStyle = '#333'; ctx.fillRect(x, y, w, h);
            ctx.fillStyle = ready ? '#ffd700' : '#74b9ff'; ctx.fillRect(x, y, Math.round(w * r), h);
            if (ready) {
                ctx.textAlign = 'center';
                ctx.font = 'bold 14px sans-serif';
                ctx.fillStyle = '#ffd700';
                ctx.fillText('승룡권 준비! 특수 키!', width / 2, y - 8);
            }
        }
        function drawKiCharge(ctx, width, height, p) {   // 장풍 충전: 기운 + 게이지 (칸막이 = 발사 가능선)
            if (!p.kiOn) return;
            const r = p.kiT / KI_TIME, full = r >= 1, ready = r >= KI_MIN;
            const rgb = full ? '255,120,40' : ready ? '80,200,255' : '150,150,160';
            drawKiOrb(ctx, width / 2, height * 0.66, width * (0.02 + 0.07 * r), full);
            const w = Math.round(width * 0.36), h = 10, x = Math.round((width - w) / 2), y = Math.round(height * 0.84);
            ctx.fillStyle = '#000';
            ctx.fillRect(x - 3, y - 3, w + 6, h + 6);
            ctx.fillStyle = '#333';
            ctx.fillRect(x, y, w, h);
            ctx.fillStyle = 'rgb(' + rgb + ')';
            ctx.fillRect(x, y, Math.round(w * r), h);
            ctx.fillStyle = '#fff';
            ctx.fillRect(x + Math.round(w * KI_MIN) - 1, y - 3, 2, h + 6);
            ctx.textAlign = 'center';
            ctx.font = '10px "Press Start 2P", monospace';
            ctx.fillStyle = full ? '#ff7828' : '#fff';
            ctx.fillText(full ? 'MAX' : ready ? 'READY' : '', width / 2, y - 8);
        }
        function drawHold(ctx, width, height, p) {   // 점프 · 백열권: 키를 누르는 동안 아래쪽에 게이지 (점프는 흰 눈금 이후에 떼면 점프)
            if (!p.hold) return;
            const jump = p.hold === 'kick', r = Math.min(1, p.holdT / (jump ? JUMP_HOLD_MAX : FLURRY_HOLD));
            const w = width * 0.3, h = Math.max(4, height * 0.02), x = (width - w) / 2, y = height * 0.78;
            ctx.fillStyle = '#000'; ctx.fillRect(x - 2, y - 2, w + 4, h + 4);
            ctx.fillStyle = r >= 1 ? '#ff4757' : (jump && p.holdT < JUMP_HOLD_MIN ? '#888' : '#f1c40f'); ctx.fillRect(x, y, w * r, h);
            if (jump) { ctx.fillStyle = '#fff'; ctx.fillRect(x + w * JUMP_HOLD_MIN / JUMP_HOLD_MAX - 1, y - 2, 2, h + 4); }
        }
        function drawCharge(ctx, width, height, p) {
            if (!p.charging) return;
            const r = Math.min(1, p.chargeT / CHARGE_TIME);
            const mul = CHARGE_MIN + (CHARGE_MAXMUL - CHARGE_MIN) * r;
            const full = r >= 1;
            const rgb = full ? '255,71,87' : r > 0.5 ? '255,159,67' : '241,196,15';
            const now = performance.now();
            const pulse = full ? 0.75 + 0.25 * Math.sin(now / 60) : 1;

            // 가장자리 오라
            const cx = width / 2, cy = height / 2, rad = Math.hypot(cx, cy);
            const g = ctx.createRadialGradient(cx, cy, rad * 0.45, cx, cy, rad);
            g.addColorStop(0, 'rgba(' + rgb + ',0)');
            g.addColorStop(1, 'rgba(' + rgb + ',' + (0.12 + 0.4 * r) * pulse + ')');
            ctx.fillStyle = g;
            ctx.fillRect(0, 0, width, height);

            // 기가 모이는 선: 바깥에서 중심으로 빨려 들어옴 (충전할수록 많고 빨라짐)
            const n = 6 + Math.round(r * 14);
            ctx.strokeStyle = 'rgba(' + rgb + ',0.85)';
            ctx.lineWidth = 2;
            ctx.beginPath();
            for (let k = 0; k < n; k++) {
                const ang = k * 2.399 + Math.floor(now / 700 + k) * 1.7;   // 선마다 각도가 달라지고 매 주기마다 바뀜
                const ph = ((now / (700 - r * 350)) + k / n) % 1;
                const d1 = rad * (1 - ph) * 0.9 + 12, d2 = d1 + 10 + r * 14;
                ctx.moveTo(cx + Math.cos(ang) * d2, cy + Math.sin(ang) * d2);
                ctx.lineTo(cx + Math.cos(ang) * d1, cy + Math.sin(ang) * d1);
            }
            ctx.stroke();

            // 게이지
            const w = Math.round(width * 0.36), h = 10, x = Math.round((width - w) / 2), y = Math.round(height * 0.84);
            ctx.fillStyle = '#000';
            ctx.fillRect(x - 3, y - 3, w + 6, h + 6);
            ctx.fillStyle = '#333';
            ctx.fillRect(x, y, w, h);
            ctx.fillStyle = 'rgb(' + rgb + ')';
            ctx.fillRect(x, y, Math.round(w * r), h);
            ctx.textAlign = 'center';
            ctx.font = '10px "Press Start 2P", monospace';
            ctx.fillStyle = '#000';
            ctx.fillText('x' + mul.toFixed(1), width / 2 + 2, y - 8 + 2);
            ctx.fillStyle = full ? '#ff4757' : '#fff';
            ctx.fillText(full ? 'MAX x' + mul.toFixed(1) : 'x' + mul.toFixed(1), width / 2, y - 8);
        }

        function drawCombo(ctx, width, height, p) {
            if (p.combo < 2 || p.comboT >= COMBO_WINDOW) return;
            const c = p.combo, t = p.comboT;
            const pop = t < 0.06 ? 1.5 : t < 0.12 ? 1.25 : 1;   // 픽셀이 뭉개지지 않게 단계로 확대
            const rainbow = c >= 5;
            const color = rainbow ? 'hsl(' + Math.floor(gameTime * 600 % 360 / 30) * 30 + ',100%,60%)' : c >= 3 ? '#ff4757' : '#ff9f43';   // 단계는 3개: 2 주황 / 3~4 빨강 / 5+ 무지개
            const word = c >= 5 ? 'UNSTOPPABLE!' : c >= 3 ? 'GREAT!' : 'COMBO!';
            const sh = c >= 5 ? 3 : 0;   // 최고 단계에서만 글자가 부들부들 떨림
            const pulse = 1 + 0.05 * Math.sin(gameTime * 18);
            ctx.save();
            ctx.globalAlpha = t > COMBO_WINDOW - COMBO_FADE ? (COMBO_WINDOW - t) / COMBO_FADE : 1;   // 사라지기 전 서서히 투명해짐
            ctx.translate(16 + (sh ? Math.round((Math.random() * 2 - 1) * sh) : 0), Math.round(height * 0.36) + (sh ? Math.round((Math.random() * 2 - 1) * sh) : 0));
            ctx.scale(pop * pulse, pop * pulse);
            ctx.textAlign = 'left';
            {   // 불꽃 파편: 처음부터 솟아오름 (콤보가 높을수록 조금 더 많이)
                const n = Math.min(16, 10 + (c >= 3 ? 3 : 0) + (c >= 5 ? 3 : 0)), cols = ['#ffd32a', '#ff9f43', '#ff4757'];
                for (let i = 0; i < n; i++) {
                    const ph = (gameTime * 1.8 + i / n) % 1;
                    const x = 4 + i * (110 / n) + Math.sin(i * 7 + gameTime * 6) * 6, y = -8 - ph * 54;
                    ctx.save(); ctx.globalAlpha *= 1 - ph;
                    ctx.fillStyle = rainbow ? 'hsl(' + (i * 40 + gameTime * 300) % 360 + ',100%,65%)' : cols[i % 3];
                    ctx.fillRect(Math.round(x), Math.round(y), 4, 4);
                    ctx.restore();
                }
            }
            ctx.shadowColor = color; ctx.shadowBlur = 16;   // 빛번짐 (처음부터 항상)
            const draw = (str, y, size) => {
                ctx.font = size + 'px \"Press Start 2P\", monospace';
                ctx.fillStyle = '#000';
                for (const [ox, oy] of [[-3, 0], [3, 0], [0, -3], [0, 3], [3, 3]]) ctx.fillText(str, ox, y + oy);
                ctx.fillStyle = color;
                ctx.fillText(str, 0, y);
            };
            draw(String(c), 0, 44);
            draw(word, 22, 12);
            ctx.restore();
        }

        // 기절 표시: 머리 위를 도는 픽셀 별 3개
        function drawStars(ctx, cx, top, spriteW, spriteH) {
            const unit = Math.max(1, Math.round(spriteH * 0.03));
            for (let i = 0; i < 3; i++) {
                const a = gameTime * 5 + i * Math.PI * 2 / 3;
                const x = Math.round(cx + Math.cos(a) * spriteW * 0.4);
                const y = Math.round(top - spriteH * 0.04 + Math.sin(a) * spriteH * 0.045);
                ctx.fillStyle = '#f1c40f';
                ctx.fillRect(x - unit, y, unit * 3, unit);
                ctx.fillRect(x, y - unit, unit, unit * 3);
                ctx.fillStyle = '#fff';
                ctx.fillRect(x, y, unit, unit);
            }
        }

        // 피격 이펙트: 가슴 위치에서 번쩍이는 십자 + 튀는 픽셀 파편
        // 피격 이펙트: 맞은 캐릭터 자신의 색으로 충격 십자 + 링 + 파편이 사방으로 튐
        function drawHitFx(ctx, p, cx, cy, spriteW) {
            const t = 1 - p.hitFx / HIT_FX_TIME;   // 0 → 1
            const unit = Math.max(2, Math.round(spriteW * 0.08));
            const base = p.color, light = shade(p.color, 0.5), dark = shade(p.color, -0.35);
            if (t < 0.4) {   // 충격 십자 + 중심 번쩍
                const r = Math.round(unit * (2 + t * 10));
                ctx.fillStyle = light;
                ctx.fillRect(Math.round(cx - r), Math.round(cy - unit / 2), r * 2, unit);
                ctx.fillRect(Math.round(cx - unit / 2), Math.round(cy - r), unit, r * 2);
                ctx.fillStyle = '#fff';
                ctx.fillRect(Math.round(cx - unit), Math.round(cy - unit), unit * 2, unit * 2);
            }
            if (t < 0.6) {   // 퍼지는 네모 링 (점선처럼 도트로)
                const rr = unit * (1.5 + t * 14);
                ctx.fillStyle = t < 0.3 ? base : dark;
                for (let i = 0; i < 16; i++) {
                    const a = (i / 16) * Math.PI * 2;
                    ctx.fillRect(Math.round(cx + Math.cos(a) * rr - unit / 2), Math.round(cy + Math.sin(a) * rr - unit / 2), unit, unit);
                }
            }
            const cols = [base, light, '#fff'];
            for (const f of p.fx) {
                const d = f.s * t * spriteW * 1.5;
                const size = Math.max(1, Math.round(unit * f.k * (1 - t * 0.8)));
                ctx.fillStyle = t > 0.75 && f.c !== 2 ? dark : cols[f.c];
                const x = Math.round(cx + Math.cos(f.a) * d);
                const y = Math.round(cy + Math.sin(f.a) * d + t * t * spriteW * 0.6);
                ctx.fillRect(x, y, size, size);
            }
        }

        // '#rrggbb' 색에 밝기 배율 f(0~1)를 곱함
        const scaleCache = new Map();
        function scaleColor(hex, f) {
            const q = Math.round(f * 64);
            const key = hex + q;
            let v = scaleCache.get(key);
            if (!v) {
                const n = parseInt(hex.slice(1), 16);
                const k = q / 64;
                v = 'rgb(' + (((n >> 16) & 255) * k | 0) + ',' + (((n >> 8) & 255) * k | 0) + ',' + ((n & 255) * k | 0) + ')';
                scaleCache.set(key, v);
            }
            return v;
        }

        // 색 밝게(+) / 어둡게(-) : f는 -1 ~ 1
        function shade(hex, f) {
            const n = parseInt(hex.slice(1), 16);
            let r = (n >> 16) & 255, g = (n >> 8) & 255, b = n & 255;
            const t = f < 0 ? 0 : 255;
            const a = Math.abs(f);
            r = Math.round(r + (t - r) * a);
            g = Math.round(g + (t - g) * a);
            b = Math.round(b + (t - b) * a);
            return 'rgb(' + r + ',' + g + ',' + b + ')';
        }

        function roundRectPath(ctx, x, y, w, h, r) {
            ctx.beginPath();
            ctx.moveTo(x + r, y);
            ctx.arcTo(x + w, y, x + w, y + h, r);
            ctx.arcTo(x + w, y + h, x, y + h, r);
            ctx.arcTo(x, y + h, x, y, r);
            ctx.arcTo(x, y, x + w, y, r);
            ctx.closePath();
        }

        // 픽셀 주먹 스프라이트 (24x32, 왼손 기준 / 엄지가 오른쪽)

        function generateFistSprite(color) {
            const c = document.createElement('canvas');
            c.width = FIST_W;
            c.height = FIST_H;
            const g = c.getContext('2d');

            const SKIN = color, LIGHT = shade(color, 0.5), DARK = shade(color, -0.3);
            const SLEEVE = shade(color, -0.5), SLEEVE_DARK = shade(color, -0.7);
            const rect = (x, y, w, h, col) => { g.fillStyle = col; g.fillRect(x, y, w, h); };
            // 모서리를 1px 깎은 사각형
            const bevel = (x, y, w, h, col) => {
                rect(x + 1, y, w - 2, 1, col);
                rect(x, y + 1, w, h - 2, col);
                rect(x + 1, y + h - 1, w - 2, 1, col);
            };
            const outlined = (x, y, w, h, col) => {
                bevel(x - 1, y - 1, w + 2, h + 2, '#000');
                bevel(x, y, w, h, col);
            };

            // 소매
            rect(5, 16, 14, 16, '#000');
            rect(6, 16, 12, 16, SLEEVE);
            rect(14, 16, 4, 16, SLEEVE_DARK);

            // 주먹: 둥근 블록 하나 + 하이라이트/그림자
            outlined(3, 4, 18, 13, SKIN);
            rect(17, 6, 3, 10, DARK);         // 오른쪽 음영
            rect(4, 15, 13, 1, DARK);         // 아래 음영
            rect(5, 5, 4, 1, LIGHT);          // 하이라이트

            return c;
        }

        // x, y = 주먹 중심, side: 1 = 왼손, -1 = 오른손(좌우 반전)
        function toGrayscale(ctx, w, h) {
            const img = ctx.getImageData(0, 0, w, h);
            const d = img.data;
            for (let i = 0; i < d.length; i += 4) {
                const v = (d[i] * 0.3 + d[i + 1] * 0.59 + d[i + 2] * 0.11) | 0;
                d[i] = d[i + 1] = d[i + 2] = v;
            }
            ctx.putImageData(img, 0, 0);
        }

        function drawFist(ctx, x, y, scale, rot, side, sprite, color, alpha, withArm, knife) {
            ctx.save();
            ctx.globalAlpha = alpha;
            ctx.imageSmoothingEnabled = false;
            ctx.translate(Math.round(x), Math.round(y));
            ctx.rotate(rot);
            ctx.scale(HUD_PX * scale * side, HUD_PX * scale);

            if (withArm) {
                // 소매를 화면 아래까지 연장
                const top = FIST_H - FIST_ANCHOR_Y - 13;   // 소매 시작 위치(스프라이트 y=19)
                ctx.fillStyle = '#000';
                ctx.fillRect(-7, top, 14, 400);
                ctx.fillStyle = shade(color, -0.5);
                ctx.fillRect(-6, top, 12, 400);
                ctx.fillStyle = shade(color, -0.7);
                ctx.fillRect(2, top, 4, 400);
            }
            ctx.drawImage(sprite, -FIST_ANCHOR_X, -FIST_ANCHOR_Y);
            if (knife) {   // 한손 단검: 주먹 위로 솟은 짧은 칼날 + 날밑
                ctx.fillStyle = '#000'; ctx.fillRect(-8, -13, 16, 5);
                ctx.fillStyle = '#8395a7'; ctx.fillRect(-7, -12, 14, 3);
                ctx.fillStyle = '#000'; ctx.fillRect(-4, -34, 8, 22);
                ctx.fillStyle = '#dfe6e9'; ctx.fillRect(-3, -33, 6, 20);
                ctx.fillStyle = '#fff'; ctx.fillRect(-3, -33, 2, 20);
                ctx.fillStyle = '#000'; ctx.fillRect(-2, -38, 4, 4);
                ctx.fillStyle = '#dfe6e9'; ctx.fillRect(-1, -36, 2, 3);
            }
            ctx.restore();
        }

        // 공격 진행도(0~1) → 와인드업(pull) / 타격(k) 값
        // 0~0.18: 뒤로 당김 → 0.18~0.36: 빠르게 뻗음(타격 시점에 최대, 살짝 오버슈트) → 0.36~0.46: 임팩트 유지 → 0.46~1: 복귀
        function punchPose(p) {
            if (p < 0.18) {
                const u = p / 0.18;
                return { pull: u * u * (3 - 2 * u), k: 0 };
            }
            if (p < 0.36) {
                const u = (p - 0.18) / 0.18;
                return { pull: 1 - u, k: (1 - Math.pow(1 - u, 3)) * 1.1 };
            }
            if (p < 0.46) {
                const u = (p - 0.36) / 0.10;
                return { pull: 0, k: 1.1 - 0.1 * u * u * (3 - 2 * u) };
            }
            const u = (p - 0.46) / 0.54;
            return { pull: 0, k: 1 - u * u * (3 - 2 * u) };
        }

        function handTransform(restX, center, width, height, pull, k, bob, restBase) {
            const dir = restX < center ? 1 : -1;   // 1: 왼손(안쪽이 +x)
            const restY = (restBase === undefined ? height - 38 : restBase) + bob;
            const strikeY = height * 0.38;
            const arc = Math.sin(Math.min(1, k) * Math.PI) * 14;   // 뻗는 중 살짝 위로 휘는 궤적
            return {
                x: restX - dir * 20 * pull + (center - restX) * 0.85 * k,
                y: restY + 38 * pull + (strikeY - restY) * k - arc,
                s: 1 - 0.15 * pull + 0.95 * k,
                rot: dir * (0.32 * k - 0.12 * pull),
                dir: dir
            };
        }

        // 발차기 진행도(0~1) → 발이 올라온 정도(0~1)
        // 0~0.25: 살짝 들어올림 → 0.25~0.4: 빠르게 뻗음(타격 시점) → 0.4~0.55: 유지 → 복귀
        function kickPose(p) {
            const sm = u => u * u * (3 - 2 * u);
            if (p < 0.25) return 0.15 * sm(p / 0.25);
            if (p < 0.4) { const u = (p - 0.25) / 0.15; return 0.15 + 0.85 * (1 - Math.pow(1 - u, 3)); }
            if (p < 0.55) return 1;
            return 1 - sm((p - 0.55) / 0.45);
        }

        // 1인칭 발차기: 화면 아래에서 신발이 올라와 정면으로 뻗음
        function drawKickHUD(ctx, width, height, player) {
            const k = kickPose(Math.min(1, player.kickT / KICK_DURATION));
            if (player.legSprite) {   // 그림 다리: 화면 아래쪽에서 올라와 앞으로 뻗음 (예전보다 낮은 위치)
                const U = width / 104 * 0.5 * (1 + 0.4 * k);
                const x = Math.round(width / 2 + 10 - k * 10);
                const y = Math.round((height + 90) + (height * 0.8 - height - 90) * k);
                ctx.save();
                ctx.imageSmoothingEnabled = false;
                ctx.translate(x, y);
                ctx.scale(U, U);
                ctx.drawImage(player.legSprite, -LEG_OX, -LEG_OY);
                ctx.restore();
                return;
            }
            const s = 1 + 1.0 * k;
            const x = Math.round(width / 2 + 24 - k * 10);
            const y = Math.round(height + 40 - k * height * 0.4);
            const c = player.color;
            ctx.save();
            ctx.translate(x, y);
            ctx.scale(s, s);
            ctx.fillStyle = '#000';
            ctx.fillRect(-15, -4, 30, 160);                 // 다리
            ctx.fillStyle = shade(c, -0.5);
            ctx.fillRect(-13, -4, 26, 160);
            ctx.fillStyle = shade(c, -0.7);
            ctx.fillRect(4, -4, 9, 160);
            ctx.fillStyle = '#000';
            ctx.fillRect(-20, -38, 40, 38);                 // 신발
            ctx.fillStyle = shade(c, 0.25);
            ctx.fillRect(-18, -36, 36, 34);
            ctx.fillStyle = shade(c, 0.6);
            ctx.fillRect(-18, -36, 36, 8);                  // 앞코
            ctx.fillStyle = shade(c, -0.3);
            ctx.fillRect(-18, -8, 36, 6);                   // 밑창 음영
            ctx.restore();
        }

        // 총을 들고 있는 상태: 총 카드가 있고 주먹/발차기/가드 중이 아닐 때 (두 손으로 권총을 잡음)
        function isHoldingGun(p) {
            return p.gun && !p.attacking && !p.kicking && p.guard <= 0;
        }

        // 총 반동 세기 0~1: 쏘는 순간 확 튀었다가(0.05초), 쿨타임이 끝날 때까지 서서히 0으로 돌아옴
        function gunRecoil(p) {
            if (!p.gun || p.gunCd <= 0) return 0;
            const el = GUN_COOLDOWN - p.gunCd;   // 쏜 뒤 지난 시간
            const KICK = 0.05;
            if (el < KICK) return el / KICK;
            return Math.pow(1 - (el - KICK) / (GUN_COOLDOWN - KICK), 1.5);
        }

        // 총: 조준점은 항상, 들고 있을 때는 오른손이 권총을 쥐고 왼손은 옆에 둔 1인칭. 쏘면 반동 + 총구 불꽃 + 탄도선
        function drawGunHUD(ctx, width, height, player) {
            const cx = Math.round(width / 2), cy = Math.round(height / 2);
            ctx.fillStyle = 'rgba(255,255,255,0.85)';
            ctx.fillRect(cx - 1, cy - 7, 2, 4);
            ctx.fillRect(cx - 1, cy + 3, 2, 4);
            ctx.fillRect(cx - 7, cy - 1, 4, 2);
            ctx.fillRect(cx + 3, cy - 1, 4, 2);
            ctx.save();   // 남은 탄 표시 (오른쪽 아래)
            for (let i = 0; i < GUN_MAG; i++) {
                const bx = width - 12 - (GUN_MAG - i) * 9, by = height - 22;
                ctx.fillStyle = '#000'; ctx.fillRect(bx - 1, by - 1, 8, 14);
                ctx.fillStyle = i < player.gunAmmo ? '#f1c40f' : '#444'; ctx.fillRect(bx, by, 6, 12);
            }
            ctx.restore();
            if (!isHoldingGun(player)) return;
            if (player.gunReload > 0 && player.gunT <= 0) {   // 장전 중: 두 손으로 탄창을 갈아 끼움
                const spr = player.reloadSprite;
                if (spr && spr.width) {
                    const sz = Math.round(height * 1.05), wob = Math.round(Math.sin(gameTime * 10) * 2);
                    ctx.save();
                    ctx.imageSmoothingEnabled = false;
                    ctx.drawImage(spr, Math.round((width - sz) / 2), height - sz + Math.round(height * 0.25) + wob, sz, sz);   // 화면 아래쪽으로 내려서 그림
                    ctx.restore();
                }
                const k = 1 - player.gunReload / GUN_RELOAD_TIME;   // 장전 진행바
                ctx.fillStyle = '#000'; ctx.fillRect(cx - 22, cy + 14, 44, 8);
                ctx.fillStyle = '#f1c40f'; ctx.fillRect(cx - 20, cy + 16, Math.round(40 * k), 4);
                return;
            }

            const bob = Math.round(player.moving ? Math.sin(gameTime * 12) * 3 : Math.sin(gameTime * 2) * 1.5);
            const t = player.gunT > 0 ? player.gunT / GUN_FX_TIME : 0;   // 1 → 0
            const rec = gunRecoil(player);
            const S = width / GUNVIEW_ROWS[0].length;                    // 그림 한 칸 = 화면 몇 px
            const oy = Math.round(height * GUNVIEW_TOP - 1.5 * S) + bob; // 총구가 GUNVIEW_TOP 높이에 오도록
            ctx.save();
            ctx.imageSmoothingEnabled = false;
            // 오른손: 권총을 쥠. 반동: 아래로 밀리며 손목을 축으로 총구가 살짝 돌아감
            const px = GUNVIEW_PIVOT[0] * S, py = oy + GUNVIEW_PIVOT[1] * S, rot = -rec * 0.1, dy = rec * height * 0.05;
            ctx.translate(px, py + dy);
            ctx.rotate(rot);
            ctx.translate(-px, -py);
            ctx.drawImage(player.gunViewR, GUNVIEW_SPLIT * S - S, oy - S, player.gunViewR.width * S, player.gunViewR.height * S);
            ctx.restore();
            // 총구 위치(화면 좌표): 손 그림과 같은 반동 변환을 적용
            const bx = GUNVIEW_MUZZLE[0] * S - px, by = oy + GUNVIEW_MUZZLE[1] * S - py;
            const mx = Math.round(px + bx * Math.cos(rot) - by * Math.sin(rot));
            const my = Math.round(py + dy + bx * Math.sin(rot) + by * Math.cos(rot));
            const U = width / 104 * ARM_SCALE;   // 총구 불꽃 크기 기준

            if (t > 0.4) {   // 탄도선: 총구에서 조준점까지
                ctx.fillStyle = t > 0.7 ? '#fff' : '#f1c40f';
                for (let i = 0; i < 14; i++) {
                    const k = i / 14;
                    ctx.fillRect(Math.round(mx + (cx - mx) * k) - 1, Math.round(my + (cy - my) * k) - 1, 3, 3);
                }
            }
            if (t > 0.5) {   // 총구 불꽃
                const f = Math.max(5, Math.round(U * 3));
                ctx.fillStyle = '#f1c40f'; ctx.fillRect(Math.round(mx - f * 1.3), Math.round(my - f * 0.5), Math.round(f * 2.6), Math.round(f));
                ctx.fillRect(Math.round(mx - f * 0.35), Math.round(my - f * 1.8), Math.round(f * 0.7), Math.round(f * 2.6));
                ctx.fillStyle = '#fff'; ctx.fillRect(Math.round(mx - f * 0.7), Math.round(my - f * 0.9), Math.round(f * 1.4), Math.round(f * 1.4));
            }
        }

        // 상대가 든 권총 위치 (정면에서 화면 왼쪽 = 상대의 오른손 한 손으로 쥠). 총구 불꽃도 이 위치에서 나옴
        function enemyGunPose(enemy, screenX, top, spriteH, sideView, flip) {
            const u = spriteH / 23;
            if (sideView) {
                const d = flip ? -1 : 1;
                return { u, d, x: screenX, y: top + u * 6.7, muzzleX: screenX + d * 10.9 * u, muzzleY: top + u * 6.2 };   // 가드 자세의 주먹 높이에서 앞으로
            }
            return { u, x: screenX - 4.4 * u, y: top + u * 9.6, muzzleX: screenX - 4.4 * u, muzzleY: top + u * 8.6 };   // 대기 자세의 오른 주먹
        }

        // 상대가 들고 있는 권총 (상대 화면의 스프라이트 위에 덧그림). 오른손 한 손이 손잡이를 쥐고 총구가 앞으로. 앞/옆모습만 보임
        function drawEnemyGun(ctx, enemy, screenX, top, spriteH, sideView, backView, flip) {
            if (backView) return;
            const gp = enemyGunPose(enemy, screenX, top, spriteH, sideView, flip);
            const u = gp.u, fy = gp.y;
            const R = (x, y, w, h, c) => { ctx.fillStyle = c; ctx.fillRect(Math.round(x), Math.round(y), Math.max(1, Math.round(w)), Math.max(1, Math.round(h))); };
            const col = enemy.color, hi = shade(col, 0.45), lo = shade(col, 0.25);
            if (sideView) {
                const X = (x, w) => gp.d > 0 ? screenX + x * u : screenX - (x + w) * u;
                R(X(3.4, 7.6), fy - 1.8 * u, 7.6 * u, 2.5 * u, '#000');          // 슬라이드 외곽
                R(X(3.7, 7.0), fy - 1.5 * u, 7.0 * u, 1.9 * u, '#6c7a7b');
                R(X(3.7, 7.0), fy - 1.5 * u, 7.0 * u, 0.5 * u, '#bdc3c7');       // 광택
                R(X(10.5, 0.4), fy - 1.0 * u, 0.4 * u, 1.0 * u, '#2f3640');      // 총구
                R(X(10.0, 0.5), fy - 2.3 * u, 0.5 * u, 0.6 * u, '#000');         // 가늠쇠
                R(X(3.7, 0.7), fy - 2.3 * u, 0.7 * u, 0.6 * u, '#000');
                R(X(3.5, 2.0), fy + 0.5 * u, 2.0 * u, 2.8 * u, '#000');          // 손잡이
                R(X(3.8, 1.4), fy + 0.5 * u, 1.4 * u, 2.4 * u, '#2f3640');
                R(X(2.9, 3.4), fy - 0.9 * u, 3.4 * u, 3.0 * u, '#000');          // 손잡이를 감싼 오른손
                R(X(3.2, 2.8), fy - 0.6 * u, 2.8 * u, 2.4 * u, col);
                R(X(3.2, 2.8), fy - 0.6 * u, 2.8 * u, 0.6 * u, hi);
                R(X(3.2, 2.8), fy + 0.5 * u, 2.8 * u, 0.3 * u, lo); R(X(3.2, 2.8), fy + 1.2 * u, 2.8 * u, 0.3 * u, lo);   // 손가락 선
                R(X(5.6, 1.6), fy - 1.0 * u, 1.6 * u, 1.0 * u, '#000'); R(X(5.8, 1.2), fy - 0.8 * u, 1.2 * u, 0.6 * u, hi);   // 엄지가 슬라이드 옆을 누름
            } else {   // 정면: 오른 주먹이 쥔 권총의 총구가 나를 향함
                const x = gp.x;
                R(x - 0.8 * u, fy + 0.4 * u, 1.6 * u, 2.3 * u, '#000');          // 손잡이 아래쪽
                R(x - 0.5 * u, fy + 0.4 * u, 1.0 * u, 1.9 * u, '#2f3640');
                R(x - 1.7 * u, fy + 0.5 * u, 3.4 * u, 1.5 * u, '#000');          // 손잡이를 감싼 손가락
                R(x - 1.4 * u, fy + 0.8 * u, 2.8 * u, 0.9 * u, col);
                R(x - 1.4 * u, fy + 0.8 * u, 2.8 * u, 0.3 * u, hi);
                R(x - 1.6 * u, fy - 2.1 * u, 3.2 * u, 2.9 * u, '#000');          // 슬라이드 앞면
                R(x - 1.3 * u, fy - 1.8 * u, 2.6 * u, 2.3 * u, '#6c7a7b');
                R(x - 1.3 * u, fy - 1.8 * u, 2.6 * u, 0.5 * u, '#bdc3c7');
                R(x - 0.5 * u, fy - 1.0 * u, 1.0 * u, 1.0 * u, '#000');          // 총구 구멍
                R(x - 0.3 * u, fy - 2.6 * u, 0.6 * u, 0.6 * u, '#000');          // 가늠쇠
            }
        }

        // 상대가 든 단검 (상대 화면의 스프라이트 위에 덧그림). 칼은 상대의 오른손(정면에서 화면 왼쪽 주먹)에 쥐여 있고,
        // 공격할 때 나가는 주먹(strike[0])과 같은 손이라 칼이 주먹과 함께 나감. 앞/옆모습만 보임
        function drawEnemyKnife(ctx, enemy, screenX, top, spriteH, sideView, backView, flip) {
            if (backView) return;
            const u = spriteH / 23;   // 스프라이트 한 칸
            const R = (x, y, w, h, c) => { ctx.fillStyle = c; ctx.fillRect(Math.round(x), Math.round(y), Math.max(1, Math.round(w)), Math.max(1, Math.round(h))); };
            const striking = enemy.attacking && punchPose(Math.min(1, enemy.attackT / ATTACK_DURATION)).k > 0.3;   // 주먹 프레임이 나가는 중 (renderView 와 같은 조건)
            if (sideView) {   // 옆모습: 앞으로 내민 주먹 앞쪽에서 칼날이 앞으로 뻗음
                const d = flip ? -1 : 1;
                const X = (x, w) => d > 0 ? screenX + x * u : screenX - (x + w) * u;
                const y0 = top + u * (striking ? 6.5 : 6.7);   // 주먹 높이 (뻗은 팔 / 가드 자세)
                const o = 1.8;                                  // 주먹 앞면에 가드가 닿도록 앞으로 이동
                R(X(4.6 + o, 1), y0 - u * 1.4, u, 2.8 * u, '#000');            // 가드
                R(X(4.8 + o, 0.6), y0 - u * 1.2, 0.6 * u, 2.4 * u, '#8395a7');
                R(X(5.6 + o, 6), y0 - u * 0.8, 6 * u, 1.6 * u, '#000');         // 칼날 외곽
                R(X(5.8 + o, 5.4), y0 - u * 0.5, 5.4 * u, 1 * u, '#dfe6e9');
                R(X(5.8 + o, 5.4), y0 - u * 0.5, 5.4 * u, 0.4 * u, '#fff');
                R(X(11.6 + o, 0.8), y0 - u * 0.4, 0.8 * u, 0.8 * u, '#000');    // 끝
                return;
            }
            // 정면: 왼쪽 주먹(공격 때는 커진 주먹) 위로 솟은 단검. 가드 자세 스프라이트가 기본 자세와 같아 위치도 같음
            const hx = screenX + u * (striking ? -3.45 : -4.4);                              // 대기 주먹은 바깥쪽·아래, 나가는 주먹은 안쪽·위
            const hy = top + u * (striking ? 8.05 - 2.5 : 9.6 - 1.7) + 0.4 * u;              // 가드가 주먹 윗면에 닿음
            const bl = striking ? 7 : 5.2;                                   // 찌를 때는 칼날이 더 길어 보임
            const bt = hy - 1.2 * u - bl * u;                                // 칼날 윗끝
            R(hx - 0.55 * u, hy - 0.2 * u, 1.1 * u, 1.8 * u, '#000');       // 주먹 속으로 들어가는 자루
            R(hx - 0.35 * u, hy, 0.7 * u, 1.4 * u, '#4a535b');
            R(hx - 1.5 * u, hy - 1.2 * u, 3 * u, 1 * u, '#000');            // 가드
            R(hx - 1.2 * u, hy - 1.0 * u, 2.4 * u, 0.6 * u, '#8395a7');
            R(hx - 0.8 * u, bt, 1.6 * u, bl * u, '#000');                    // 칼날 외곽
            R(hx - 0.5 * u, bt + 0.3 * u, 1.0 * u, (bl - 0.4) * u, '#dfe6e9');
            R(hx - 0.5 * u, bt + 0.3 * u, 0.4 * u, (bl - 0.4) * u, '#fff');
            R(hx - 0.4 * u, bt - 0.8 * u, 0.8 * u, 0.9 * u, '#000');        // 끝
        }

        // 상대가 총을 쏠 때 상대 손 위치의 총구 불꽃
        function drawMuzzle(ctx, cx, cy, spriteH) {
            const u = Math.max(2, Math.round(spriteH * 0.04));
            const r = u * 3;
            ctx.fillStyle = '#fff';
            ctx.fillRect(Math.round(cx - r), Math.round(cy - u / 2), r * 2, u);
            ctx.fillRect(Math.round(cx - u / 2), Math.round(cy - r), u, r * 2);
            ctx.fillStyle = '#f1c40f';
            ctx.fillRect(Math.round(cx - u), Math.round(cy - u), u * 2, u * 2);
        }

        // ===== 오징어 먹물 =====
        // 오징어: 몸통 끝(0행)부터 다리 끝(31행)까지 세로로 선 그림. 손에 잡히는 쪽이 0행이라 그릴 때 위아래를 뒤집어 다리가 앞(위)을 향하게 함
        const SQUID_W = 22, SQUID_H = 32;
        function generateSquidSprite() {
            const c = document.createElement('canvas');
            c.width = SQUID_W + 2; c.height = SQUID_H + 2;
            const g = c.getContext('2d');
            const cx = (SQUID_W - 1) / 2;
            for (let y = 0; y < SQUID_H; y++) for (let x = 0; x < SQUID_W; x++) {
                const dx = x - cx;
                let k = null;
                if (y <= 17) {   // 몸통(뾰족한 끝에서 점점 넓어짐) + 양옆 지느러미
                    const hw = 0.6 + 4.6 * Math.sin(Math.min(1, y / 16) * Math.PI / 2);
                    const fw = Math.max(0, 4.5 - Math.abs(y - 6) * 0.9);
                    if (Math.abs(dx) <= hw) {
                        const u = dx / hw;
                        k = u < -0.5 ? '#ffd2c8' : u < 0.1 ? '#f4a6a0' : u < 0.55 ? '#e08a88' : '#c46a6c';
                        if (y > 5 && y < 16 && (x * 7 + y * 13) % 11 === 0) k = '#b85a5e';   // 점무늬
                    } else if (y >= 1 && y <= 11 && Math.abs(dx) <= hw + fw) k = Math.abs(dx) > hw + fw - 1 ? '#c46a6c' : '#e68f8c';
                } else if (y <= 21) {   // 머리 + 툭 튀어나온 눈
                    const hw = 3.6 - 0.2 * (y - 18);
                    if (Math.abs(dx) <= hw) k = dx < 0 ? '#f4a6a0' : '#e08a88';
                    else if ((y === 19 || y === 20) && Math.abs(dx) <= 5.6) k = Math.abs(dx) > 5 ? '#000' : '#fff';
                } else {   // 다리 8개 (가운데 두 개가 더 길고 굵음)
                    for (let i = 0; i < 8; i++) {
                        const len = 6 + (3.5 - Math.abs(i - 3.5)) * 0.9;
                        if (y > 21 + len) continue;
                        const tx = Math.round(cx + (i - 3.5) * 1.7 * (1 + (y - 22) * 0.04) + Math.sin(y * 0.8 + i) * 0.6);
                        const wide = i === 3 || i === 4 ? 1 : 0;
                        if (x === tx || (wide && x === tx + (i === 3 ? -1 : 1))) { k = (y % 3 === 0) ? '#ffd2c8' : '#f0a09a'; break; }
                    }
                }
                if (k) { g.fillStyle = k; g.fillRect(x + 1, y + 1, 1, 1); }
            }
            const src = g.getImageData(0, 0, SQUID_W + 2, SQUID_H + 2).data;
            const filled = (x, y) => x >= 0 && y >= 0 && x < SQUID_W + 2 && y < SQUID_H + 2 && src[(y * (SQUID_W + 2) + x) * 4 + 3] > 0;
            g.fillStyle = '#000';
            for (let py = 0; py < SQUID_H + 2; py++) for (let px = 0; px < SQUID_W + 2; px++) {
                if (!filled(px, py) && (filled(px - 1, py) || filled(px + 1, py) || filled(px, py - 1) || filled(px, py + 1))) g.fillRect(px, py, 1, 1);
            }
            return c;
        }
        const SQUID_SPRITE = generateSquidSprite();

        // 먹물 얼룩: 맞은 사람 화면 크기에 맞춰 한 번 만들어 두고(시드마다), 퍼지는 동안 크기만 바꿔 그림
        function makeInkMask(width, height, seed) {
            const c = document.createElement('canvas');
            c.width = width; c.height = height;
            const g = c.getContext('2d');
            let sd = Math.floor(seed * 2147483646) + 1;
            const rnd = () => (sd = sd * 48271 % 2147483647) / 2147483647;
            const D = 4;
            const dot = (x, y, w, h, col) => { g.fillStyle = col; g.fillRect(Math.round(x / D) * D, Math.round(y / D) * D, w, h); };
            const blob = (bx, by, r) => {
                for (let y = -r; y <= r; y += D) for (let x = -r; x <= r; x += D) {
                    if (Math.hypot(x, y) + (rnd() - 0.5) * r * 0.35 > r) continue;
                    dot(bx + x, by + y, D, D, '#0d0b16');
                }
                dot(bx - r * 0.45, by - r * 0.45, D, D, '#3a3860');   // 반짝이는 먹물
                dot(bx - r * 0.45 + D, by - r * 0.45, D, D, '#2a2848');
            };
            blob(width / 2, height / 2, width * 0.2);
            const blobs = [];
            for (let i = 0; i < 14; i++) { const b = [width * rnd(), height * rnd(), width * (0.06 + 0.1 * rnd())]; blobs.push(b); blob(b[0], b[1], b[2]); }
            for (let i = 0; i < 8; i++) {   // 흘러내리는 먹물
                const b = blobs[i], len = 20 + rnd() * 60, x = b[0] + (rnd() - 0.5) * b[2];
                dot(x, b[1], D * 2, b[2] + len, '#0d0b16');
            }
            for (let i = 0; i < 30; i++) blob(width * rnd(), height * rnd(), D * (1 + Math.floor(rnd() * 2)));   // 튄 방울
            return c;
        }
        // 먹물에 맞은 쪽 화면: 처음 0.2초 동안 중앙에서 퍼지고, 마지막 1초 동안 옅어짐
        function drawInkOverlay(ctx, width, height, p) {
            if (p.inked <= 0) return;
            if (!p.inkMask || p.inkMaskSeed !== p.inkSeed || p.inkMask.width !== width || p.inkMask.height !== height) {
                p.inkMask = makeInkMask(width, height, p.inkSeed);
                p.inkMaskSeed = p.inkSeed;
            }
            const grow = Math.min(1, (INK_TIME - p.inked) / 0.2), fade = Math.min(1, p.inked / 1);
            const sc = 0.5 + 0.5 * grow;
            ctx.save();
            ctx.imageSmoothingEnabled = false;
            ctx.globalAlpha = fade * (0.5 + 0.5 * grow);
            ctx.drawImage(p.inkMask, width / 2 * (1 - sc), height / 2 * (1 - sc), width * sc, height * sc);
            ctx.restore();
        }

        // 스테미나가 모자란데 기술을 쓰려 하면: 처음 0.15초에 화면이 흐려지고, 마지막 0.3초에 걷힘
        function drawLackOverlay(ctx, width, height, p) {
            if (p.lackT <= 0) return;
            const k = Math.min(1, (LACK_TIME - p.lackT) / 0.15, p.lackT / 0.3);
            const bw = Math.max(1, Math.round(width / 6)), bh = Math.max(1, Math.round(height / 6));
            if (!p.lackBuf) p.lackBuf = document.createElement('canvas');
            if (p.lackBuf.width !== bw || p.lackBuf.height !== bh) { p.lackBuf.width = bw; p.lackBuf.height = bh; }
            const b = p.lackBuf.getContext('2d');
            b.imageSmoothingEnabled = true;
            b.drawImage(ctx.canvas, 0, 0, width, height, 0, 0, bw, bh);   // 작게 줄였다가 키우면 흐려짐
            ctx.save();
            ctx.imageSmoothingEnabled = true;
            ctx.globalAlpha = k;
            ctx.drawImage(p.lackBuf, 0, 0, bw, bh, 0, 0, width, height);
            ctx.globalAlpha = k * 0.25;
            ctx.fillStyle = '#000';
            ctx.fillRect(0, 0, width, height);
            ctx.globalAlpha = k;
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.font = '18px "Galmuri11", monospace';
            ctx.fillStyle = '#000';
            const msg = p.lackMsg || '스테미나 부족';
            ctx.fillText(msg, Math.round(width / 2) + 2, Math.round(height / 2) + 2);
            ctx.fillStyle = '#f1c40f';
            ctx.fillText(msg, Math.round(width / 2), Math.round(height / 2));
            ctx.restore();
        }

        // 쏘는 쪽 1인칭: 오른손이 오징어 몸통을 쥐고 다리 끝에서 조준점 쪽으로 먹물을 뿜음
        function drawInkHUD(ctx, width, height, player) {
            const cx = Math.round(width / 2), cy = Math.round(height / 2);
            const k = 1 - player.inkT / INK_FX_TIME;   // 0 → 1
            const S = width / 127 * 1.25, TILT = -0.3, GRIP = -4;   // GRIP: 몸통 끝이 주먹보다 몇 칸 위에 오는지 (음수 = 주먹 위에 올려 쥠)
            const bob = Math.round(Math.sin(gameTime * 2) * 1.5);
            const th = handTransform(width * 0.65, cx, width, height, 0, Math.sin(Math.min(1, k * 1.5) * Math.PI) * 0.12, bob, height * 0.93);
            drawArmHand(ctx, th.x, th.y, th.s, th.rot, -1, player.armSprite, 1, width, false);   // 주먹 위에 오징어를 올려 쥠
            ctx.save();
            ctx.imageSmoothingEnabled = false;
            ctx.translate(Math.round(th.x), Math.round(th.y));
            ctx.rotate(TILT);
            ctx.scale(S, -S);   // 위아래를 뒤집어 다리가 위(앞)를 향함
            ctx.drawImage(SQUID_SPRITE, -(SQUID_W + 2) / 2, -1 - GRIP);
            ctx.restore();
            // 다리 끝 → 조준점: 먹물 방울이 날아가며 작아짐
            const tipX = th.x + Math.sin(TILT) * ((SQUID_H - GRIP) * S), tipY = th.y - Math.cos(TILT) * ((SQUID_H - GRIP) * S);
            const n = Math.floor(Math.min(1, k * 2.2) * 16);
            for (let i = 0; i < n; i++) {
                const f = i / 16, wob = Math.sin(i * 2.3 + gameTime * 30) * (3 + f * 14);
                const x = Math.round(tipX + (cx - tipX) * f + wob), y = Math.round(tipY + (cy - tipY) * f + Math.cos(i * 1.7) * (2 + f * 8));
                const r = Math.max(3, Math.round(9 - f * 6));
                ctx.fillStyle = '#0d0b16'; ctx.fillRect(x - r, y - r, r * 2, r * 2);
                ctx.fillStyle = '#3a3860'; ctx.fillRect(x - r, y - r, Math.max(2, r - 1), 2);
            }
        }

        // 백열권 1인칭: 두 주먹이 번갈아 빠르게 나가고, 한 손당 FLURRY_GHOSTS 개의 주먹이 시차를 두고 겹쳐 보임 (맨 앞 j=0 이 진짜, 나머지는 반투명 잔상)
        // 힐: 물약을 쥔 두 손이 아래에서 올라와 입 쪽으로 다가감 (파란 손은 플레이어 색, 물약은 그대로)
        const HEAL_B64 = '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';
        const HEAL_IMG = new Image();
        HEAL_IMG.src = 'data:image/png;base64,' + HEAL_B64;
        const healArt = {};
        function healSprite(color) {
            if (healArt[color]) return healArt[color];
            const im = HEAL_IMG;
            if (!im.complete || !im.naturalWidth) return null;
            const c = document.createElement('canvas');
            c.width = im.naturalWidth; c.height = im.naturalHeight;
            const g = c.getContext('2d');
            g.drawImage(im, 0, 0);
            if (color.toLowerCase() !== '#1e90ff') {
                const d = g.getImageData(0, 0, c.width, c.height), px = d.data;
                const n = parseInt(color.slice(1), 16), tc = [(n >> 16) & 255, (n >> 8) & 255, n & 255];
                for (let i = 0; i < px.length; i += 4) {
                    if (px[i + 3] === 0) continue;
                    if (!(px[i + 2] > px[i + 1] + 25 && px[i + 2] > px[i] + 25)) continue;   // 파란 칸(손)만 색을 바꿈 (외곽선 · 물약 · 유리는 그대로)
                    const L = px[i] * 0.3 + px[i + 1] * 0.59 + px[i + 2] * 0.11, r = L / 122;
                    for (let k = 0; k < 3; k++) px[i + k] = Math.round(r <= 1 ? tc[k] * r : tc[k] + (255 - tc[k]) * Math.min(1, (r - 1) / 0.9));
                }
                g.putImageData(d, 0, 0);
            }
            return healArt[color] = c;
        }
        let healSplit = 0;
        function drawHealHUD(ctx, width, height, player) {   // 왼손(주먹)은 가만히, 오른손(물약)은 손목을 축으로 내 쪽(화면 가운데)으로 기울어짐
            const art = healSprite(player.color);
            const t = player.healT, r = Math.min(1, t / HEAL_HOLD);
            if (art) {
                const W = art.width, H = art.height;
                if (!healSplit) {   // 두 손 사이 가장 빈 세로줄 찾기 (한 번만)
                    const d = art.getContext('2d').getImageData(0, 0, W, H).data;
                    let best = 1e9;
                    for (let x = Math.floor(W * 0.4); x < Math.floor(W * 0.6); x++) {
                        let n = 0;
                        for (let y = 0; y < H; y++) if (d[(y * W + x) * 4 + 3] > 0) n++;
                        if (n < best) { best = n; healSplit = x; }
                    }
                }
                const w = width * 0.8, sc = w / W, h = H * sc;
                const rise = 1 - Math.pow(1 - Math.min(1, t / 0.25), 2);   // 처음 0.25초에 두 손이 올라옴
                const x0 = (width - w) / 2, y0 = height - h * (-0.15 + 0.7 * rise);   // 아래쪽은 화면 밖으로 살짝 넘겨서 팔이 잘려 보이지 않게
                ctx.save();
                ctx.imageSmoothingEnabled = false;
                ctx.drawImage(art, 0, 0, healSplit, H, x0, y0, healSplit * sc, h);   // 왼손
                const tilt = Math.min(1, Math.max(0, (t - 0.25) / 0.6));
                const ease = tilt * tilt * (3 - 2 * tilt);
                const ang = -(0.32 * ease + Math.sin(t * 10) * 0.02 * ease), zoom = 1 + 0.08 * ease;   // 시계 반대 방향: 위쪽이 가운데(나) 쪽으로
                const px = x0 + (healSplit + (W - healSplit) * 0.8) * sc, py = y0 + h * 0.85;   // 손목 (오른쪽 아래)
                ctx.translate(px, py); ctx.rotate(ang); ctx.scale(zoom, zoom); ctx.translate(-px, -py);
                ctx.drawImage(art, healSplit, 0, W - healSplit, H, x0 + healSplit * sc, y0, (W - healSplit) * sc, h);   // 오른손 + 물약
                ctx.restore();
            }
            const bw = width * 0.3, bh = Math.max(4, height * 0.02), bx = (width - bw) / 2, by = height * 0.1;   // 마시는 게이지
            ctx.fillStyle = '#000'; ctx.fillRect(bx - 2, by - 2, bw + 4, bh + 4);
            ctx.fillStyle = '#2ecc71'; ctx.fillRect(bx, by, bw * r, bh);
        }

        function drawFlurryHUD(ctx, width, height, player, hands, bob, restBase, center, arm) {
            const ph = player.flurryT * FLURRY_RATE;
            for (const h of hands) {
                for (let j = FLURRY_GHOSTS - 1; j >= 0; j--) {
                    const pose = punchPose((ph + (h.id === 0 ? 0.5 : 0) + j / FLURRY_GHOSTS) % 1);
                    const t = handTransform(h.restX, center, width, height, pose.pull, pose.k, bob, restBase);
                    const fan = (j % 2 ? 1 : -1) * Math.ceil(j / 2) * 0.16;   // 잔상마다 기울기 · 위치를 달리해 따로 뻗는 주먹처럼
                    t.rot += fan; t.x += fan * 70; t.y += Math.abs(fan) * 30;
                    const alpha = j === 0 ? 1 : 0.6 - j * 0.09;
                    if (arm) drawArmHand(ctx, t.x, t.y, t.s, t.rot, h.side, arm, alpha, width, false);
                    else drawFist(ctx, t.x, t.y, t.s, t.rot, h.side, player.fistSprite, player.color, alpha, j === 0, false);
                }
            }
        }

        function drawHUD(ctx, width, height, player) {
            const bob = player.moving ? Math.sin(gameTime * 12) * 3 : Math.sin(gameTime * 2) * 1.5;
            const center = width / 2;
            const arm = player.armSprite;   // 2P: 그림 팔+주먹 (대기 자세는 가운데 가까이, 화면 중간 높이)
            const restBase = arm ? height * 0.7 : undefined;
            const hands = [
                { restX: width * (arm ? 0.35 : 0.27), side: 1,  id: 1 },   // 왼손
                { restX: width * (arm ? 0.65 : 0.73), side: -1, id: 0 }    // 오른손
            ];
            const p = player.attacking ? Math.min(1, player.attackT / ATTACK_DURATION) : 0;
            // 가드: 양 주먹이 얼굴 앞으로 올라왔다 내려감 (올림/내림 각 0.04초)
            const gf = player.guard > 0
                ? Math.min(1, (GUARD_TIME - player.guard) / 0.04, player.guard / 0.04) : 0;

            if (player.inkT > 0) { drawInkHUD(ctx, width, height, player); return; }   // 먹물을 뿌리는 동안은 오징어를 듦

            if (isHoldingGun(player)) { drawGunHUD(ctx, width, height, player); return; }
            if (player.healOn) { drawHealHUD(ctx, width, height, player); return; }
            if (player.flurryOn) { drawFlurryHUD(ctx, width, height, player, hands, bob, restBase, center, arm); return; }   // 총을 들면 주먹 대신 권총을 두 손으로 잡음

            if (player.kicking) drawKickHUD(ctx, width, height, player);   // 주먹보다 먼저 그려서 주먹을 가리지 않음

            const ap = player.attacking ? punchPose(p) : { pull: 0, k: 0 };
            // 승룡권: 시전하는 동안 오른손을 번쩍 들어올림 (시작 0.1초에 올라가고 끝나기 전 0.1초에 내려옴)
            const shoryuLift = player.shoryuOn ? Math.max(0, Math.min(1, player.shoryuT / 0.1, (SHORYU_TIME - player.shoryuT) / 0.1)) : 0;
            for (const h of hands) {
                if (player.knife && h.id === 1) continue;   // 칼을 들면 왼손(주먹)은 보이지 않음
                const active = player.attacking && player.punchHand === h.id;
                const pose = active ? ap : { pull: 0, k: 0 };
                const t = handTransform(h.restX, center, width, height, pose.pull, pose.k, bob, restBase);
                if (player.kicking) t.y += 30 * kickPose(Math.min(1, player.kickT / KICK_DURATION));   // 발차기 중 주먹은 아래로
                if (shoryuLift > 0) {
                    if (h.id === 0) {   // 오른손: 화면 위쪽으로 높이 치켜듦
                        const r = handTransform(h.restX, center, width, height, 0, shoryuLift, bob, restBase);
                        t.x = r.x; t.y = r.y - height * 0.16 * shoryuLift; t.s = r.s; const tu = Math.min(1, player.shoryuT / 0.45);   // 기울기는 시전 시간 대부분에 걸쳐 서서히 커짐
                        t.rot = 0.5 * tu * tu * (3 - 2 * tu) * Math.min(1, (SHORYU_TIME - player.shoryuT) / 0.1);   // 바깥쪽(오른쪽)으로 기울임 (+: 시계 방향)
                    } else {   // 왼손: 안쪽으로 모이며 살짝 내려감
                        t.x += (center - t.x) * 0.1 * shoryuLift; t.y += 10 * shoryuLift;
                    }
                }
                if (player.attacking && !active) {   // 반대 손은 안쪽으로 모이며 살짝 내려감
                    t.x += (center - t.x) * 0.1 * Math.min(1, ap.k);
                    t.y += 8 * Math.min(1, ap.k) + 4 * ap.pull;
                }

                if (gf > 0) {
                    const tx = center + (h.side === 1 ? -width * 0.09 : width * 0.09);
                    t.x += (tx - t.x) * gf;
                    t.y += (height * 0.52 - t.y) * gf;
                    t.s += (1.2 - t.s) * gf;
                    t.rot += (t.dir * 0.2 - t.rot) * gf;
                }

                const knifeHand = player.knife && h.id === 0;   // 칼은 오른손
                // 타격 중 잔상(모션 블러)
                if (active && p > 0.18 && p < 0.55) {
                    for (let i = 5; i >= 1; i--) {
                        const gp = punchPose(Math.max(0, p - i * 0.025));
                        const gt = handTransform(h.restX, center, width, height, gp.pull, gp.k, bob, restBase);
                        if (arm) drawArmHand(ctx, gt.x, gt.y, gt.s, gt.rot, h.side, knifeHand ? player.armKnifeSprite : arm, 0.12, width, knifeHand);
                        else drawFist(ctx, gt.x, gt.y, gt.s, gt.rot, h.side, player.fistSprite, player.color, 0.12, false);
                    }
                }

                if (arm) drawArmHand(ctx, t.x, t.y, t.s, t.rot, h.side, knifeHand ? player.armKnifeSprite : arm, 1, width, knifeHand);
                else drawFist(ctx, t.x, t.y, t.s, t.rot, h.side, player.fistSprite, player.color, 1, true, player.knife && h.id === 0);
            }
            if (player.gun) drawGunHUD(ctx, width, height, player);
        }

        // 미니맵: 오른쪽 위, 북쪽이 위. 삼각형 = 나(바라보는 방향), 동그라미 = 상대
        let MINI_S = 6;   // 큰 맵(도시)은 미니맵이 화면을 너무 가리지 않게 칸 크기를 줄임
        function drawMinimap(ctx, width, observer, enemy) {
            MINI_S = Math.min(6, 120 / MAP_W);
            const w = MAP_W * MINI_S, h = MAP_H * MINI_S;
            const x0 = width - w - 8, y0 = 8;
            ctx.fillStyle = 'rgba(0,0,0,0.55)';
            ctx.fillRect(x0 - 2, y0 - 2, w + 4, h + 4);
            if (arena) {   // 콜로세움: 파란 바다 위에 둥근 바닥과 가장자리 기둥
                ctx.fillStyle = 'rgba(205,200,184,0.8)';   // 네모 방 바깥은 벽 색, 안쪽 둥근 벽 안이 바다
                ctx.fillRect(x0, y0, w, h);
                ctx.fillStyle = 'rgba(30,110,190,0.9)';
                ctx.beginPath();
                ctx.arc(x0 + ARENA_C / MAP_SIZE * MINI_S, y0 + ARENA_C / MAP_SIZE * MINI_S, WALL_R / MAP_SIZE * MINI_S, 0, Math.PI * 2);
                ctx.fill();
                ctx.fillStyle = 'rgba(205,185,140,0.9)';
                ctx.beginPath();
                ctx.arc(x0 + ARENA_C / MAP_SIZE * MINI_S, y0 + ARENA_C / MAP_SIZE * MINI_S, ARENA_R / MAP_SIZE * MINI_S, 0, Math.PI * 2);
                ctx.fill();
                ctx.fillStyle = 'rgba(240,240,245,0.95)';
                for (const [cx, cy] of RING) ctx.fillRect(x0 + cx / MAP_SIZE * MINI_S - 1.5, y0 + cy / MAP_SIZE * MINI_S - 1.5, 3, 3);
            }
            if (city) { ctx.fillStyle = 'rgba(70,70,78,0.85)'; ctx.fillRect(x0, y0, w, h); }   // 도시: 도로 바탕에 건물 칸이 밝게
            ctx.fillStyle = 'rgba(205,200,184,0.8)';
            for (let r = 0; r < MAP_H; r++) {
                for (let c = 0; c < MAP_W; c++) {
                    if (map[r][c] === 1 && !arena) {
                        ctx.fillStyle = 'rgba(205,200,184,0.8)';
                        ctx.fillRect(x0 + c * MINI_S, y0 + r * MINI_S, MINI_S, MINI_S);
                    } else if (map[r][c] === 2) {
                        ctx.fillStyle = 'rgba(240,240,245,0.95)';
                        ctx.fillRect(x0 + c * MINI_S + MINI_S / 2 - 1.5, y0 + r * MINI_S + MINI_S / 2 - 1.5, 3, 3);
                    }
                }
            }
            ctx.fillStyle = '#b07a3c';   // 설치한 박스
            const bs = Math.max(3, OBST_HALF * 2 / MAP_SIZE * MINI_S);
            for (const b of obstacles) ctx.fillRect(x0 + b.x / MAP_SIZE * MINI_S - bs / 2, y0 + b.y / MAP_SIZE * MINI_S - bs / 2, bs, bs);
            if (car && car.warn > 0) {   // 차가 오기 전: 지나갈 길이 빨개짐
                const w = carWarnPath(car);
                ctx.fillStyle = 'rgba(255,50,50,0.6)';
                ctx.fillRect(x0 + w.x0 / MAP_SIZE * MINI_S, y0 + w.y0 / MAP_SIZE * MINI_S, (w.x1 - w.x0) / MAP_SIZE * MINI_S, (w.y1 - w.y0) / MAP_SIZE * MINI_S);
            } else if (car && car.x > 0 && car.x < MAP_W * MAP_SIZE && car.y > 0 && car.y < MAP_H * MAP_SIZE) {   // 도시 자동차 (노랑) · 버스 (주황)
                const cw = Math.max(3, (car.dx ? car.len : car.wid) / MAP_SIZE * MINI_S), ch = Math.max(3, (car.dx ? car.wid : car.len) / MAP_SIZE * MINI_S);
                ctx.fillStyle = car.bus ? '#e67e22' : '#f1c40f';
                ctx.fillRect(x0 + car.x / MAP_SIZE * MINI_S - cw / 2, y0 + car.y / MAP_SIZE * MINI_S - ch / 2, cw, ch);
            }
            if (!(enemy.invisT > 0)) {   // 투명한 상대는 미니맵에서도 안 보임
                const ex = x0 + enemy.x / MAP_SIZE * MINI_S;
                const ey = y0 + enemy.y / MAP_SIZE * MINI_S;
                ctx.fillStyle = enemy.color;
                ctx.beginPath();
                ctx.arc(ex, ey, 2.5, 0, Math.PI * 2);
                ctx.fill();
            }

            const ox = x0 + observer.x / MAP_SIZE * MINI_S;
            const oy = y0 + observer.y / MAP_SIZE * MINI_S;
            const a = observer.angle;
            ctx.beginPath();
            ctx.moveTo(ox + Math.cos(a) * 5, oy + Math.sin(a) * 5);
            ctx.lineTo(ox + Math.cos(a + 2.5) * 4, oy + Math.sin(a + 2.5) * 4);
            ctx.lineTo(ox + Math.cos(a - 2.5) * 4, oy + Math.sin(a - 2.5) * 4);
            ctx.closePath();
            ctx.fillStyle = observer.color;
            ctx.fill();
            ctx.strokeStyle = '#fff';
            ctx.lineWidth = 1;
            ctx.stroke();
        }

        // 천장 전등: 월드 좌표에 고정된 직사각형의 네 모서리를 천장 높이로 투영해서 그림
        // (시점을 돌리면 전등도 천장 위에서 같이 돌아가 보임. 벽은 나중에 위에 그려져 자연스럽게 가려짐)
        const CEIL_LIGHTS = [];
        for (const lx of [192, 384, 576]) for (const ly of [144, 288, 432]) CEIL_LIGHTS.push([lx, ly]);
        function drawCeilingLights(ctx, observer, width, half, proj, eye) {
            const k = (CEIL_H - eye) * proj;
            if (k <= 0) return;
            const cosA = Math.cos(observer.angle), sinA = Math.sin(observer.angle);
            const NEAR = 4;   // 카메라 바로 위/뒤로 넘어가는 부분은 이 깊이에서 잘라냄
            const fillQuad = (lx, ly, hx, hy, color) => {
                const pts = [[-hx, -hy], [hx, -hy], [hx, hy], [-hx, hy]].map(([ox, oy]) => {
                    const dx = lx + ox - observer.x, dy = ly + oy - observer.y;
                    return [dx * cosA + dy * sinA, -dx * sinA + dy * cosA];   // [깊이, 좌우]
                });
                const out = [];
                for (let i = 0; i < 4; i++) {
                    const a = pts[i], b = pts[(i + 1) % 4];
                    const ain = a[0] >= NEAR, bin = b[0] >= NEAR;
                    if (ain) out.push(a);
                    if (ain !== bin) {
                        const t = (NEAR - a[0]) / (b[0] - a[0]);
                        out.push([NEAR, a[1] + (b[1] - a[1]) * t]);
                    }
                }
                if (out.length < 3) return;
                ctx.fillStyle = color;
                ctx.beginPath();
                out.forEach(([f, l], i) => {
                    const sx = width / 2 + l / f * proj, sy = half - k / f;
                    if (i) ctx.lineTo(sx, sy); else ctx.moveTo(sx, sy);
                });
                ctx.closePath();
                ctx.fill();
            };
            for (const [lx, ly] of CEIL_LIGHTS) {
                fillQuad(lx, ly, 28, 13, '#20252a');       // 전등 틀
                fillQuad(lx, ly, 26, 11, '#fff7cf');       // 불빛
                fillQuad(lx, ly, 15, 4.5, '#ffffff');      // 하이라이트
            }
        }

        // 경기가 끝났을 때: 이긴 사람 머리 위에 도발 EZ 말풍선, 옆에는 밀려나는 자세(피격)의 진 사람
        function drawMatchTaunt(ctx, width, height, observer) {
            const t = performance.now() / 1000;
            const loser = winner === p1 ? p2 : p1;
            const wname = winner === p1 ? 'PLAYER 1' : 'PLAYER 2';
            const lname = loser === p1 ? 'PLAYER 1' : 'PLAYER 2';
            ctx.save();
            ctx.imageSmoothingEnabled = false;
            ctx.fillStyle = 'rgba(0,0,0,0.78)';
            ctx.fillRect(0, 0, width, height);
            ctx.textAlign = 'center';
            ctx.textBaseline = 'alphabetic';

            // 누가 이겼는지
            ctx.font = '16px "Press Start 2P", monospace';
            ctx.fillStyle = '#000'; ctx.fillText(wname + ' WINS!', width / 2 + 2, 32);
            ctx.fillStyle = winner.color; ctx.fillText(wname + ' WINS!', width / 2, 30);
            ctx.font = '12px "Galmuri11", monospace';
            ctx.fillStyle = winner === observer ? '#2ed573' : '#ff6b81';
            ctx.fillText(winner === observer ? '내가 이겼어요!' : '상대가 이겼어요', width / 2, 50);

            const sh = 115, feetY = height - 34;
            const person = (spr, cx, name, color) => {
                ctx.fillStyle = 'rgba(0,0,0,0.5)';
                ctx.beginPath(); ctx.ellipse(cx, feetY, 34, 7, 0, 0, Math.PI * 2); ctx.fill();
                if (spr && spr.width) ctx.drawImage(spr, cx - sh * spr.width / spr.height / 2, feetY - sh, sh * spr.width / spr.height, sh);
                ctx.font = '8px "Press Start 2P", monospace';
                ctx.fillStyle = color;
                ctx.fillText(name, cx, feetY + 18);
            };
            person(loser.hitSprite, width * 0.28, lname, loser.color);   // 진 사람: 맞아서 밀려날 때 그림
            person(winner.sprite, width * 0.72, wname, winner.color);    // 이긴 사람 + 도발 말풍선
            drawBubble(ctx, 'EZ', width * 0.72, feetY - sh, 0, 200, t);

            ctx.font = '11px "Galmuri11", monospace';
            ctx.textAlign = 'center'; ctx.textBaseline = 'alphabetic';
            ctx.fillStyle = '#ccc';
            ctx.fillText(document.body.classList.contains('touch') ? '아래 [새 경기] 버튼을 누르세요' : 'Enter / R 로 새 경기', width / 2, height - 10);
            ctx.restore();
        }

        function drawGameOver(ctx, width, height, observer) {
            if (matchOver && winner && !tutorial && !practice) { drawMatchTaunt(ctx, width, height, observer); return; }   // 경기 종료 (1인 · 2인 · 온라인 공통)
            const mine = winner === observer;
            const draw = !winner;
            ctx.fillStyle = 'rgba(0,0,0,0.6)';
            ctx.fillRect(0, 0, width, height);
            ctx.textAlign = 'center';
            ctx.fillStyle = '#f1c40f';
            ctx.font = '48px "Press Start 2P", monospace';
            ctx.fillText(timeUp ? 'TIME UP' : 'KO!', width / 2, height / 2 - 20);
            ctx.fillStyle = draw ? '#ddd' : mine ? '#2ed573' : '#ff6b81';
            if (draw) {
                ctx.font = '16px "Press Start 2P", monospace';
                ctx.fillText('DRAW', width / 2, height / 2 + 20);
            } else if (matchOver) {
                ctx.font = '24px "Press Start 2P", monospace';
                ctx.fillText(mine ? 'YOU WIN' : 'YOU LOSE', width / 2, height / 2 + 20);
            } else {
                ctx.font = '16px "Press Start 2P", monospace';
                ctx.fillText(mine ? 'ROUND WIN' : 'ROUND LOSE', width / 2, height / 2 + 20);
            }
            ctx.font = '11px "Galmuri11", monospace';
            ctx.fillStyle = '#ccc';
            ctx.fillText(matchOver ? (document.body.classList.contains('touch') ? '아래 [새 경기] 버튼을 누르세요' : 'Enter / R 로 새 경기')
                : (draw ? (picking ? '둘 다 카드를 고르는 중...' : '무승부 - 둘 다 카드 선택') : picking ? '진 사람이 카드를 고르는 중...' : '곧 카드 선택'), width / 2, height / 2 + 50);
            ctx.textAlign = 'start';
        }

        // ===== 메인 루프 (deltaTime 기반) =====
        let lastTime = performance.now();
        // ===== 1P 모드 AI: 2P 키 입력을 대신 만들어 줌 =====
        let aiSeenAtk = false, aiReactT = 0, aiLastHp = 0, aiPostHit = false;
        // 라운드가 지날수록 AI가 조금씩 강해짐 (라운드당 약 8%, 최대 6라운드 분)
        function aiScaled() {
            const k = Math.min(round - 1, 6), m = 1 + 0.08 * k;
            return {
                guard: aiLevel.guard * m, attack: aiLevel.attack * m, kick: aiLevel.kick * m, speed: aiLevel.speed * m,
                aim: aiLevel.aim / m,
                react: Math.min(1, aiLevel.react + 0.05 * k), hitGuard: Math.min(0.95, aiLevel.hitGuard + 0.05 * k),
                delay: [aiLevel.delay[0] / m, aiLevel.delay[1] / m]
            };
        }
        const AI_INK_FREEZE = 3;   // AI가 먹물을 맞으면 멈추는 시간(초)
        let aiFreezeT = 0;
        const AI_SHORYU_CD = 8;   // 보통 난이도 기준 초 (난이도 이동 속도 배율로 나눔: 애기모드는 더 길고 하드는 더 짧음)
        let aiSpinOn = false, aiSpinDir = 1;   // AI가 승룡권 준비로 한 바퀴 도는 중인지 / 도는 방향
        let aiDetourT = 0, aiDetourHold = 0, aiDetourSide = 1;   // 기둥에 가려 막혔을 때 돌아가는 남은 시간 / 같은 쪽을 유지할 시간 / 돌아갈 쪽
        let aiRetreat = false, aiSide = 1, aiStuckT = 0, aiLastX = 0, aiLastY = 0, aiKiGoal = 1, aiChargeGoal = 1;   // aiKiGoal / aiChargeGoal: 이번에 모을 목표 충전 비율(0~1)
        function aiControl(dt) {
            if (aiFreezeT > 0) {   // 먹물을 맞아 멈춤: 이동 · 회전 · 충전을 모두 멈추고 아무것도 안 함
                aiFreezeT = Math.max(0, aiFreezeT - dt);
                const k = aiKeys(); keys[k.left] = keys[k.right] = keys[k.up] = keys[k.down] = false;
                aiSelf.kiOn = false; aiSelf.kiT = 0; aiSelf.charging = ''; aiSelf.chargeT = 0;
                aiReactT = 0; aiPostHit = false;
                return;
            }
            const lv = aiScaled();
            const foeBox = !aiSelf.gun && obstacles.length ? boxUnder(aiFoe) : null;   // 상대가 올라서 있는 박스: 주먹 · 발차기는 박스에 막히니 박스를 목표로 삼아 부숨 (총은 박스 위 사람도 맞힘)
            const tgt = foeBox || aiFoe;
            const dx = tgt.x - aiSelf.x, dy = tgt.y - aiSelf.y;
            const dist = Math.hypot(dx, dy);
            let da = Math.atan2(dy, dx) - aiSelf.angle;
            while (da < -Math.PI) da += Math.PI * 2;
            while (da > Math.PI) da -= Math.PI * 2;
            if (aiFoe.invisT > 0 && dist > ATTACK_REACH * aiSelf.reachMul) {   // 상대가 투명하면 모습을 못 봄: 멈춰 서 있음 (코앞까지 오거나 상대가 공격하면 다시 보임)
                const k = aiKeys(); keys[k.left] = keys[k.right] = keys[k.up] = keys[k.down] = false;
                aiSelf.kiOn = false; aiSelf.kiT = 0; aiSelf.charging = ''; aiSelf.chargeT = 0;
                aiReactT = 0; aiPostHit = false;
                return;
            }
            const reach = aiSelf.gun ? GUN_RANGE : ATTACK_REACH * aiSelf.reachMul;
            // 스테미나가 바닥나면 상대를 비스듬히 보면서 뒤로 물러나 회복 (공격할 만큼 회복되면 다시 싸움)
            const need = aiSelf.gun ? GUN_COST : ATTACK_COST + (aiSelf.knife ? KNIFE_COST : 0);
            if (gameOver) aiRetreat = false;
            else if (!aiRetreat && aiSelf.stamina < need) { aiRetreat = true; aiSide = Math.random() < 0.5 ? 1 : -1; aiStuckT = 0; aiLastX = aiSelf.x; aiLastY = aiSelf.y; }
            else if (aiRetreat && aiSelf.stamina >= Math.min(aiSelf.maxStamina * 0.9, Math.max(need * 2, aiSelf.maxStamina * 0.6))) aiRetreat = false;
            const retreat = aiRetreat;
            if (aiDetourHold > 0) aiDetourHold -= dt;
            if (foeBox) aiDetourT = 0;   // 박스를 부수러 갈 때는 박스를 기둥처럼 돌아가지 않음
            if (aiDetourT > 0) aiDetourT -= dt;
            else if (!retreat && !aiSelf.kiOn && dist > 40 && !foeBox) {   // 상대와 사이에 기둥이 있으면(몸 폭만큼 양옆 선까지 확인) 더 트인 쪽으로 잠깐 돌아감
                const ang = Math.atan2(dy, dx), off = Math.atan2(22, dist);
                const clear = a => { castRay(aiSelf.x, aiSelf.y, a); return rayDist >= dist - 12; };
                if (!(clear(ang) && clear(ang + off) && clear(ang - off))) {
                    if (aiDetourHold <= 0) { castRay(aiSelf.x, aiSelf.y, ang - 0.9); const r1 = rayDist; castRay(aiSelf.x, aiSelf.y, ang + 0.9); aiDetourSide = r1 >= rayDist ? 1 : -1; }
                    aiDetourT = 0.6; aiDetourHold = 1.5;
                }
            }
            if (aiSelf.canShoryu && !gameOver) aiShoryuCd = Math.max(0, aiShoryuCd - dt);
            const spinNear = ATTACK_REACH * aiSelf.reachMul;
            if (aiSpinOn) {   // 한 바퀴를 다 돌았거나(준비 완료) 상황이 바뀌면 돌기를 멈춤
                if (aiSelf.shoryuReady > 0 || retreat || gameOver || dist < spinNear * 1.2 || aiSelf.stun > 0 || aiSelf.dizzy > 0 || aiSelf.z > 0) {
                    if (aiSelf.shoryuReady <= 0) aiSelf.spinAcc = 0;
                    aiSpinOn = false;
                }
            } else if (aiSelf.canShoryu && !gameOver && aiShoryuCd <= 0 && aiSelf.shoryuReady <= 0 && !aiSelf.shoryuOn && !retreat && aiSelf.z <= 0
                && !aiSelf.attacking && !aiSelf.kicking && !aiSelf.kiOn && !aiSelf.charging && aiSelf.stun <= 0 && aiSelf.dizzy <= 0
                && aiSelf.stamina >= aiSelf.maxStamina * SHORYU_COST && dist > spinNear * 2.2 && Math.random() < dt * lv.attack * 0.5) {   // 상대와 거리가 있을 때만 제자리에서 한 바퀴 돎
                aiSpinOn = true; aiSpinDir = Math.random() < 0.5 ? 1 : -1; aiSelf.spinAcc = 0;
            }
            if (aiSpinOn) {
                keys[aiKeys().left] = aiSpinDir < 0;
                keys[aiKeys().right] = aiSpinDir > 0;
                keys[aiKeys().up] = false;
                keys[aiKeys().down] = false;
                return;
            }
            if (retreat && arena && Math.hypot(aiSelf.x + Math.cos(aiSelf.angle + Math.PI) * 40 - ARENA_C, aiSelf.y + Math.sin(aiSelf.angle + Math.PI) * 40 - ARENA_C) > ARENA_R - 20) {   // 콜로세움: 뒤가 가장자리(바다)면 뒷걸음 대신 중앙 쪽으로 몸을 돌려 걸어 바다에 안 빠짐
                let ca = Math.atan2(ARENA_C - aiSelf.y, ARENA_C - aiSelf.x) - aiSelf.angle;
                while (ca < -Math.PI) ca += Math.PI * 2;
                while (ca > Math.PI) ca -= Math.PI * 2;
                keys[aiKeys().left] = ca < -0.12;
                keys[aiKeys().right] = ca > 0.12;
                keys[aiKeys().up] = Math.abs(ca) < 0.6;
                keys[aiKeys().down] = false;
            } else if (retreat) {   // 앞으로만 움직일 수 있어서, 상대에게서 약 40도 비껴 보고 뒤로 걸으면 대각선 뒤로 빠짐
                aiStuckT += dt;
                if (aiStuckT > 0.4) {   // 벽에 막혀 못 물러나면 반대쪽 대각선으로
                    if (Math.hypot(aiSelf.x - aiLastX, aiSelf.y - aiLastY) < 12) aiSide = -aiSide;
                    aiStuckT = 0; aiLastX = aiSelf.x; aiLastY = aiSelf.y;
                }
                const ta = da - aiSide * 0.7;
                keys[aiKeys().left] = ta < -0.12;
                keys[aiKeys().right] = ta > 0.12;
                keys[aiKeys().up] = false;
                keys[aiKeys().down] = true;
            } else if (aiDetourT > 0) {   // 기둥 돌아가기: 상대를 비스듬히 보면서 앞으로
                const ta = da - aiDetourSide * 0.9;
                keys[aiKeys().left] = ta < -0.12;
                keys[aiKeys().right] = ta > 0.12;
                keys[aiKeys().up] = true;
                keys[aiKeys().down] = false;
            } else {
                keys[aiKeys().left] = da < -lv.aim;
                keys[aiKeys().right] = da > lv.aim;
                keys[aiKeys().up] = !aiSelf.gun && !aiSelf.kiOn && dist > reach * 0.8;   // 멀면 다가감 (장풍을 모으는 중에는 멈춤)
                keys[aiKeys().down] = false;
            }
            // 공격받으면 확률로 가드 (보통/어려움): 상대 공격 모션이 시작되면 잠깐 뒤 가드, 맞은 뒤에는 연타를 끊으려 가드
            const foeAtk = aiFoe.attacking || aiFoe.kicking;
            if (foeAtk && !aiSeenAtk && dist < ATTACK_REACH * aiFoe.reachMul * 1.3 && Math.random() < lv.react)
                aiReactT = lv.delay[0] + Math.random() * (lv.delay[1] - lv.delay[0]);
            aiSeenAtk = foeAtk;
            if (aiSelf.hp < aiLastHp) aiPostHit = true;
            aiLastHp = aiSelf.hp;
            if (gameOver) { aiReactT = 0; aiPostHit = false; }
            if (aiReactT > 0 && (aiReactT -= dt) <= 0) startGuard(aiSelf);
            if (aiPostHit && aiSelf.stun <= 0 && !gameOver) { aiPostHit = false; if (Math.random() < lv.hitGuard) startGuard(aiSelf); }
            if (!retreat && !aiSelf.charging && dist < reach * 1.5 && Math.random() < dt * lv.guard) startGuard(aiSelf);   // 내 공격에 반응하지 않고, 가까이 있을 때 몇 초에 한 번꼴로 확률적으로 가드 (힘조절 충전 중에는 안 함: 충전이 끊기므로)
            if (!retreat && aiSelf.canInk && Math.abs(da) < 0.4 && dist < INK_RANGE && Math.random() < dt * lv.attack * 0.25) startInk(aiSelf);
            if (aiSelf.canShoryu && !gameOver) {   // 승룡권: 한 바퀴 돌아 준비된 상태에서 상대가 코앞이면 사용 (준비 제한 시간 안에)
                if (aiSelf.shoryuReady > 0 && !retreat && aiSelf.stamina >= aiSelf.maxStamina * SHORYU_COST && Math.abs(da) < 0.25 && dist < ATTACK_REACH * aiSelf.reachMul * 0.9) {
                    if (tryShoryu(aiSelf)) aiShoryuCd = AI_SHORYU_CD / lv.speed;
                }
            }
            // ----- 카드로 얻은 기술들 (주먹 사거리 기준으로 "멀다/가깝다"를 따짐: 총을 들어도 같음) -----
            const mReach = ATTACK_REACH * aiSelf.reachMul;
            if (aiSelf.kiOn) {   // 장풍: 목표만큼 모았고 상대 쪽을 보면 발사, 상대가 코앞까지 오면 접고 주먹으로
                if (dist < mReach * 0.8) { aiSelf.kiOn = false; aiSelf.kiT = 0; }
                else if (aiSelf.kiT / KI_TIME >= aiKiGoal && Math.abs(da) < lv.aim + 0.03) releaseKi(aiSelf);
            } else if (aiSelf.canKi && !retreat && aiSelf.kiCd <= 0 && aiSelf.stamina >= KI_COST + 15 && dist > mReach * 1.3 && dist < KI_RANGE * 0.8 && Math.abs(da) < 0.25 && Math.random() < dt * lv.attack * 0.3) {
                startKi(aiSelf); aiKiGoal = 0.55 + Math.random() * 0.45;
            }
            // 대쉬 / 돌진베기: 상대 쪽을 똑바로 보고 있고, 한 번에 닿는 거리(약 200)이며, 돌진하고도 공격할 스테미나가 남을 때
            if ((aiSelf.canDash || aiSelf.canSlash) && !retreat && Math.abs(da) < 0.15 && dist > mReach * 1.1 && dist < 190
                && aiSelf.stamina >= (aiSelf.canSlash ? SLASH_COST : DASH_COST) + need && Math.random() < dt * lv.attack * 0.5) tryDash(aiSelf);
            if (aiSelf.canJump && !retreat && dist > mReach * 1.5 && aiSelf.stamina >= aiSelf.maxStamina * 0.6 && Math.random() < dt * 0.25) tryJump(aiSelf);   // 점프: 멀 때 가끔 폴짝
            if (aiSelf.canTaunt && !retreat && dist > mReach * 1.5 && Math.random() < dt * 0.2) startTaunt(aiSelf);   // 도발: 멀 때 가끔
            if (aiSelf.canHeal && aiSelf.hp <= aiSelf.maxHp - HEAL_AMOUNT && Math.random() < dt * 0.5) startHeal(aiSelf);   // 힐: 체력이 2칸 넘게 닳았을 때
            if (aiSelf.canInvis && !retreat && dist > mReach * 1.5 && Math.random() < dt * 0.3) startInvis(aiSelf);   // 투명: 멀 때 가끔
            if (aiSelf.canClone && !retreat && dist < 260 && Math.random() < dt * 0.4) startClone(aiSelf);   // 분신: 싸움이 가까울 때
            if (aiSelf.canObst && !retreat && dist > mReach * 1.5 && dist < 220 && Math.abs(da) < 0.3 && Math.random() < dt * 0.2) startObst(aiSelf);   // 장애물: 상대 쪽을 보고 있을 때 앞에 세움
            if (aiSelf.charging) {   // 힘조절: 목표만큼 모았고 맞출 수 있으면 놓음 (사거리 밖이면 모은 채로 다가감)
                if (aiSelf.chargeT / CHARGE_TIME >= aiChargeGoal && Math.abs(da) < 0.3 && dist < reach) releaseAction(aiSelf, 'ai');
            } else if (!retreat && Math.abs(da) < 0.3 && dist < reach) {
                if (Math.random() < dt * lv.attack) {
                    if (aiSelf.canCharge && !aiSelf.gun) {   // 힘조절이 있으면 바로 치지 않고 충전 시작 (살짝 ×1 / 기절 ×2 / 끝까지 ×3 중 무작위)
                        if (aiSelf.stamina >= need) { pressAction(aiSelf, 'punch', 'ai'); aiChargeGoal = [0.2, 0.62, 1][Math.floor(Math.random() * 3)]; }
                    } else startAttack(aiSelf);
                } else if (!aiSelf.gun && Math.random() < dt * lv.kick) { aiSelf.dmgMul = 1; startKick(aiSelf); }   // 발차기는 충전 안 함 (남은 충전 배율 초기화)
            }
        }


        // ===== BGM: WebAudio 칩튠 시퀀서 (외부 음원 파일 없음) =====
        const bgm = (() => {
            // 4마디 × 16스텝(16분음표) 루프. Am - F - C - G
            const CHORDS = [
                { r: 45, a: [57, 60, 64] }, { r: 41, a: [53, 57, 60] },
                { r: 48, a: [60, 64, 67] }, { r: 43, a: [55, 59, 62] }
            ];
            const MELODY = [   // [스텝, 음, 길이]
                [[0,69,2],[2,72,2],[4,76,4],[8,74,2],[10,72,2],[12,69,4]],
                [[0,65,2],[2,69,2],[4,72,4],[8,72,2],[10,69,2],[12,65,4]],
                [[0,76,2],[2,79,2],[4,76,2],[6,74,2],[8,72,4],[12,76,4]],
                [[0,74,2],[2,71,2],[4,67,2],[6,71,2],[8,74,4],[12,76,2],[14,74,2]]
            ];
            const TRACKS = {
                menu:   { bpm: 92,  tr: 0, lead: ['triangle', 0.16], drums: 0, arp: 0.03 },
                battle: { bpm: 140, tr: 0, lead: ['square', 0.07],   drums: 1, arp: 0.03 },
                burn:   { bpm: 168, tr: 3, lead: ['square', 0.08],   drums: 2, arp: 0.04 },
                tutorial: { bpm: 112, tr: 7, lead: ['square', 0.05], drums: 3, arp: 0.025 }   // 가벼운 드럼의 느긋한 곡
            };
            const FIGHT = { battle: 1, burn: 1 };
            const ARP_IDX = [0, 1, 2, 1];
            let ac = null, master = null, sfxOut = null, noiseBuf = null;
            let want = 'menu', cur = '', track = TRACKS.menu, step = 0, nextT = 0;
            let muted = false, duck = 1;
            try { muted = localStorage.getItem('yacha-bgm-muted') === '1'; } catch (e) {}

            const hz = m => 440 * Math.pow(2, (m - 69) / 12);

            function tone(type, m, t, dur, vol) {
                const o = ac.createOscillator(), g = ac.createGain();
                o.type = type; o.frequency.value = hz(m);
                g.gain.setValueAtTime(0.0001, t);
                g.gain.linearRampToValueAtTime(vol, t + 0.005);
                g.gain.setValueAtTime(vol, t + dur * 0.7);
                g.gain.exponentialRampToValueAtTime(0.0001, t + dur);
                o.connect(g); g.connect(master);
                o.start(t); o.stop(t + dur + 0.02);
            }
            function noise(t, dur, vol, freq) {
                const src = ac.createBufferSource(), f = ac.createBiquadFilter(), g = ac.createGain();
                src.buffer = noiseBuf; f.type = 'highpass'; f.frequency.value = freq;
                g.gain.setValueAtTime(vol, t);
                g.gain.exponentialRampToValueAtTime(0.0001, t + dur);
                src.connect(f); f.connect(g); g.connect(master);
                src.start(t); src.stop(t + dur);
            }
            function kick(t, vol) {
                const o = ac.createOscillator(), g = ac.createGain();
                o.frequency.setValueAtTime(150, t);
                o.frequency.exponentialRampToValueAtTime(45, t + 0.12);
                g.gain.setValueAtTime(vol, t);
                g.gain.exponentialRampToValueAtTime(0.0001, t + 0.15);
                o.connect(g); g.connect(master);
                o.start(t); o.stop(t + 0.16);
            }


            // ----- 효과음: 기술 사용 소리 + 맞는 쪽 소리(1종) -----
            function sweep(type, f0, f1, t, dur, vol) {   // 음높이가 f0 → f1 으로 변하는 짧은 소리
                const o = ac.createOscillator(), g = ac.createGain();
                o.type = type;
                o.frequency.setValueAtTime(f0, t);
                o.frequency.exponentialRampToValueAtTime(f1, t + dur);
                g.gain.setValueAtTime(vol, t);
                g.gain.exponentialRampToValueAtTime(0.0001, t + dur);
                o.connect(g); g.connect(sfxOut);
                o.start(t); o.stop(t + dur + 0.02);
            }
            function swish(type, f0, f1, t, dur, vol) {   // 필터 주파수가 f0 → f1 으로 움직이는 바람 소리/폭발음
                const src = ac.createBufferSource(), f = ac.createBiquadFilter(), g = ac.createGain();
                src.buffer = noiseBuf; f.type = type; f.Q.value = 1;
                f.frequency.setValueAtTime(f0, t);
                f.frequency.exponentialRampToValueAtTime(f1, t + dur);
                g.gain.setValueAtTime(0.0001, t);
                g.gain.linearRampToValueAtTime(vol, t + 0.015);
                g.gain.exponentialRampToValueAtTime(0.0001, t + dur);
                src.connect(f); f.connect(g); g.connect(sfxOut);
                src.start(t); src.stop(t + dur + 0.02);
            }
            const SFX = {
                punch: t => swish('bandpass', 800, 2500, t, 0.11, 0.3),
                knife: t => swish('bandpass', 1800, 5000, t, 0.1, 0.28),
                kick:  t => swish('bandpass', 300, 1200, t, 0.18, 0.4),
                gun:   t => { swish('highpass', 4000, 1500, t, 0.12, 0.4); sweep('sine', 320, 60, t, 0.14, 0.5); },
                ink:   t => { swish('lowpass', 2200, 250, t, 0.3, 0.5); sweep('sine', 180, 70, t, 0.22, 0.35); },
                guard: t => sweep('triangle', 300, 700, t, 0.18, 0.3),
                jump:  t => sweep('sine', 200, 520, t, 0.2, 0.3),
                deny:  t => { sweep('square', 200, 150, t, 0.4, 0.13); sweep('sawtooth', 100, 72, t, 0.45, 0.22); },   // 기술이 안 나가는데 누름: 길고 묵직한 경고음
                taunt: t => { sweep('square', 420, 300, t, 0.12, 0.1); sweep('square', 520, 360, t + 0.13, 0.15, 0.1); },
                horn:  t => { sweep('square', 330, 320, t, 0.55, 0.1); sweep('square', 415, 405, t, 0.55, 0.1); },   // 자동차가 나올 때 빵!
                hit:   t => { sweep('sine', 230, 55, t, 0.1, 0.9); swish('bandpass', 1400, 350, t, 0.07, 0.7); swish('lowpass', 2500, 600, t, 0.03, 0.5); }   // 맞는 쪽은 이 소리 하나만 (짧고 묵직하게 때리는 퍽)
            };

            // 기 모으는 소리: 충전할수록 음이 올라가고 커지는 지속음 (id 1·2 = 플레이어, r < 0 이면 정지)
            const chargers = {};
            function charge(id, r) {
                if (!ac || ac.state !== 'running' || muted) r = -1;
                let c = chargers[id];
                if (r < 0) {
                    if (c) { c.g.gain.setTargetAtTime(0.0001, ac.currentTime, 0.03); c.o.stop(ac.currentTime + 0.2); delete chargers[id]; }
                    return;
                }
                if (!c) {
                    const o = ac.createOscillator(), g = ac.createGain();
                    o.type = 'triangle'; g.gain.value = 0.0001;
                    o.connect(g); g.connect(sfxOut); o.start();
                    c = chargers[id] = { o, g };
                }
                r = Math.min(1, r);
                c.o.frequency.setTargetAtTime(90 * Math.pow(8, r), ac.currentTime, 0.05);   // 90Hz → 720Hz
                c.g.gain.setTargetAtTime(0.05 + 0.1 * r, ac.currentTime, 0.05);
            }

            function playStep(s, t) {
                const bar = s >> 4, i = s & 15, tr = track.tr, sd = 60 / track.bpm / 4;
                const ch = CHORDS[bar], fight = track.drums > 0;
                // 베이스
                if (fight) {
                    if (i % 2 === 0) tone('triangle', ch.r + tr + (i % 8 === 6 ? 12 : 0), t, sd * 1.8, 0.22);
                } else if (i === 0) tone('triangle', ch.r + tr, t, sd * 14, 0.2);
                // 아르페지오
                if (fight || i % 2 === 0) tone('square', ch.a[ARP_IDX[fight ? i & 3 : (i >> 1) & 3]] + tr, t, sd * (fight ? 1.2 : 3), track.arp);
                // 멜로디
                for (const [st, m, len] of MELODY[bar]) {
                    if (st === i) tone(track.lead[0], m + tr, t, sd * len * 0.95, track.lead[1]);
                }
                // 드럼
                if (track.drums >= 1) {
                    const kicks = track.drums === 2 ? (i % 4 === 0) : track.drums === 3 ? (i === 0) : (i === 0 || i === 8);
                    if (kicks) kick(t, 0.35);
                    if (track.drums !== 3 && (i === 4 || i === 12)) noise(t, 0.12, 0.09, 1500);
                    if (track.drums === 2 ? true : i % 4 === 2) noise(t, 0.03, track.drums === 2 ? 0.02 : 0.03, 7000);
                }
            }

            function tick() {
                if (!ac || ac.state !== 'running') return;
                if (nextT < ac.currentTime - 0.1) nextT = ac.currentTime + 0.05;   // 탭이 멈췄다 돌아왔을 때 따라잡기 방지
                while (nextT < ac.currentTime + 0.15) {
                    playStep(step, nextT);
                    nextT += 60 / track.bpm / 4;
                    step = (step + 1) % 64;
                }
            }
            function apply() {
                if (!ac || want === cur) return;
                if (!(FIGHT[want] && FIGHT[cur])) step = 0;   // 전투 ↔ 버닝은 박자를 이어가고, 그 외엔 처음부터
                track = TRACKS[want]; cur = want;
                nextT = Math.max(nextT, ac.currentTime + 0.05);
            }
            function level() {
                if (master) master.gain.setTargetAtTime(muted ? 0 : 0.5 * duck, ac.currentTime, 0.05);
                if (sfxOut) sfxOut.gain.setTargetAtTime(muted ? 0 : 1.1, ac.currentTime, 0.05);
            }
            function unlock() {
                if (!ac) {
                    const AC = window.AudioContext || window.webkitAudioContext;
                    if (!AC) return;
                    ac = new AC();
                    master = ac.createGain(); master.connect(ac.destination);
                    sfxOut = ac.createGain(); sfxOut.connect(ac.destination);
                    noiseBuf = ac.createBuffer(1, ac.sampleRate, ac.sampleRate);
                    const d = noiseBuf.getChannelData(0);
                    for (let k = 0; k < d.length; k++) d[k] = Math.random() * 2 - 1;
                    setInterval(tick, 25);
                    level();
                }
                if (ac.state === 'suspended') ac.resume();
                apply();
            }
            const btn = document.getElementById('bgmBtn');
            function paintBtn() {
                btn.textContent = muted ? '♪ SOUND OFF' : '♪ SOUND ON';
                btn.classList.toggle('off', muted);
            }
            function toggleMute() {
                muted = !muted;
                try { localStorage.setItem('yacha-bgm-muted', muted ? '1' : '0'); } catch (e) {}
                paintBtn(); unlock(); level();
            }
            paintBtn();
            btn.addEventListener('click', () => { toggleMute(); btn.blur(); });
            window.addEventListener('pointerdown', unlock);
            window.addEventListener('keydown', e => {
                unlock();
                if (e.code === 'KeyM' && !e.repeat) toggleMute();
            });
            document.addEventListener('visibilitychange', () => {   // 다른 탭으로 가면 BGM 멈춤
                if (!ac) return;
                if (document.hidden) ac.suspend(); else ac.resume();
            });
            return {
                set(n) { want = n; apply(); },
                duck(v) { if (v !== duck) { duck = v; level(); } },
                charge,
                sfx(n) { if (ac && ac.state === 'running' && !muted && SFX[n]) SFX[n](ac.currentTime); }
            };
        })();
        // 게임 상태에 맞는 곡 선택: 튜토리얼 → tutorial, 메뉴/경기 종료 → menu, 경기 중 → battle, 버닝 타임 → burn, 일시정지 → 작게
        function bgmSync() {
            let n = 'menu';
            if (started && tutorial) n = 'tutorial';
            else if (started && !matchOver) n = (!gameOver && burnT > 0) ? 'burn' : 'battle';
            bgm.set(n);
            bgm.duck(paused ? 0.3 : 1);
            if (paused) { bgm.charge(1, -1); bgm.charge(2, -1); }   // 일시정지 중엔 충전음 정지
        }

        function gameLoop(now) {
            bgmSync();
            if (!started || paused) { lastTime = now; requestAnimationFrame(gameLoop); return; }
            const dt = Math.min(0.05, (now - lastTime) / 1000) * (practice && practiceSettings.slow ? 0.4 : 1);   // 연습 모드 슬로우 모션
            lastTime = now;
            gameTime += dt;
            roundIntroT += dt;
            if (window.NET && NET.guest) { NET.guestFrame(dt); requestAnimationFrame(gameLoop); return; }   // 멀티플레이 손님: 계산은 방장이 함

            // 라운드가 끝나면 일정 시간 뒤 자동으로 다음 라운드 (경기 종료 시에는 대기)
            if (gameOver && !matchOver && !picking && !fusing) {
                roundEndT += dt;
                if (roundEndT >= CARD_DELAY) {
                    openCards();   // KO 연출 뒤 진 사람이 카드 선택 (무승부면 둘 다)
                }
            }

            // 라운드 시간: 다 되면 체력이 더 많은 쪽이 승리, 같으면 무승부 (튜토리얼에서는 시간이 흐르지 않음)
            if (!gameOver && !tutorial && !practice) {
                roundTime = Math.max(0, roundTime - dt);
                if (roundTime <= DOUBLE_DMG_TIME) burnT += dt;
                updateUI();
                if (roundTime <= 0) {
                    gameOver = true;
                    timeUp = true;
                    if (p1.hp !== p2.hp) {
                        winner = p1.hp > p2.hp ? p1 : p2;
                        winner.wins++;
                        matchOver = winner.wins >= matchCfg.wins;
                    }
                    updateUI();
                }
            }

            if (shoryuFxT > 0) shoryuFxT = Math.max(0, shoryuFxT - dt);
            if (!gameOver) {
                if (aiMode && !tutorial && !paused && !(practice && practiceSettings.dummy === 'idle')) aiControl(dt);
                movePlayer(p1, P1_KEYS, dt);
                movePlayer(p2, P2_KEYS, dt);
                separatePlayers();
            } else {
                p1.moving = false;
                p2.moving = false;
            }
            updateAttack(p1, p2, dt);
            updateAttack(p2, p1, dt);
            updateKi(dt);
            updateCar(dt);
            updateHeal(dt);
            updateClones(dt);
            updateObstacles(dt);
            updateFlurry(p1, p2, dt);
            updateFlurry(p2, p1, dt);
            updateBlink(p1, dt);
            updateBlink(p2, dt);
            updateShoryu(p1, p2, dt);
            updateShoryu(p2, p1, dt);
            updateDash(p1, p2, dt);
            updateDash(p2, p1, dt);
            updateSlide(p1, dt);
            updateSlide(p2, dt);
            updateAir(p1, dt);
            updateAir(p2, dt);
            updateStomp(p1, p2);
            updateStomp(p2, p1);
            updateSea(p1, dt);
            updateSea(p2, dt);
            updateStamina();
            updateSkills();
            if (practice) practiceTick();
            if (window.NET && NET.host) NET.hostTick();   // 멀티플레이 방장: 상태를 상대에게 보냄

            for (const v of views) renderView(v);
            requestAnimationFrame(gameLoop);
        }

        updateUI();
        updateStamina();
        updateSkills();
        requestAnimationFrame(gameLoop);
    </script>
    <script>
    // ===== 모바일 지원 + 화면 조작키 (키보드 이벤트를 흉내 내서 기존 입력 코드를 그대로 사용) =====
    // 모바일 모드 ON + 2인 대전: 폰을 가운데 두고 마주 보며 동시에 플레이 (1P 화면·조작키는 180도 회전)
    (() => {
        const $ = id => document.getElementById(id);
        const IS_TOUCH = matchMedia('(pointer: coarse)').matches;
        const body = document.body;
        if (IS_TOUCH) body.classList.add('touch');

        const DEF = { on: IS_TOUCH, scale: 100, opacity: 70, swap: false, player: 1 };
        let vc = { ...DEF };
        try { Object.assign(vc, JSON.parse(localStorage.getItem('yacha-vpad') || '{}')); } catch (e) {}
        const clamp = (v, a, b, d) => Math.min(b, Math.max(a, Number.isFinite(+v) ? +v : d));
        const norm = () => { vc.scale = clamp(vc.scale, 50, 150, 100); vc.opacity = clamp(vc.opacity, 20, 100, 70); vc.on = !!vc.on; vc.swap = !!vc.swap; vc.player = vc.player === 2 ? 2 : 1; };
        norm();
        const save = () => { try { localStorage.setItem('yacha-vpad', JSON.stringify(vc)); } catch (e) {} };

        const mmOn = () => vc.on && !tutorial;                // 튜토리얼 중에는 모바일 모드 꺼짐
        window.yachaMmOn = mmOn;   // 연습 모드 시작(앞쪽 스크립트)에서 모바일 모드 여부를 알 수 있게
        const isF2f = () => mmOn() && started && !aiMode && !(window.NET && NET.on);     // 2인 대전 + 모바일 모드 = 마주 보기
        const solo2 = () => aiMode ? aiSelf === p1 : (window.NET && NET.on) ? NET.me === p2 : vc.player === 2;   // 1인용이면 AI가 아닌 쪽, 아니면 선택한 쪽
        const soloKeys = () => solo2() ? P2_KEYS : P1_KEYS;   // 마주 보기가 아닐 때 조작할 플레이어
        const soloMe = () => solo2() ? p2 : p1;

        // --- 조작키 한 세트(조이스틱 + 버튼) ---
        function makeCtl(root, rot, keysFn, meFn) {
            const pad = root.querySelector('.vp-pad'), held = new Set();
            let padId = null, padKeys = null;
            const knob = (x, y) => { pad.style.setProperty('--kx', x + 'px'); pad.style.setProperty('--ky', y + 'px'); };
            const clearPad = () => { pad.classList.remove('u', 'd', 'l', 'r'); knob(0, 0); };
            function setKey(code, down) {
                if (down === held.has(code)) return;
                down ? held.add(code) : held.delete(code);
                window.dispatchEvent(new KeyboardEvent(down ? 'keydown' : 'keyup', { code, key: code, bubbles: true, cancelable: true }));
            }
            function releaseAll() {
                for (const c of [...held]) setKey(c, false);
                padId = null; clearPad();
                root.querySelectorAll('.vb.on').forEach(b => b.classList.remove('on'));
            }
            function padUpdate(e) {   // 조이스틱: 누른 채 옮기면 방향이 바뀜 (회전된 세트는 방향도 뒤집어 계산)
                const r = pad.getBoundingClientRect(), R = r.width / 2, dz = 0.3, sg = rot ? -1 : 1;
                const dx = sg * (e.clientX - r.left - R) / R, dy = sg * (e.clientY - r.top - R) / R;
                const st = { u: dy < -dz, d: dy > dz, l: dx < -dz, r: dx > dz };
                setKey(padKeys.up, st.u); setKey(padKeys.down, st.d); setKey(padKeys.left, st.l); setKey(padKeys.right, st.r);
                for (const k in st) pad.classList.toggle(k, st[k]);
                const len = Math.hypot(dx, dy) || 1, kk = Math.min(1, len) / len * 42;
                knob(dx * kk, dy * kk);
            }
            const padEnd = e => {
                if (e.pointerId !== padId) return;
                padId = null;
                for (const k of ['up', 'down', 'left', 'right']) setKey(padKeys[k], false);
                clearPad();
            };
            pad.addEventListener('pointerdown', e => {
                e.preventDefault();
                if (padId !== null) return;
                padId = e.pointerId; padKeys = keysFn();
                try { pad.setPointerCapture(e.pointerId); } catch (_) {}
                padUpdate(e);
            });
            pad.addEventListener('pointermove', e => { if (e.pointerId === padId) padUpdate(e); });
            ['pointerup', 'pointercancel', 'lostpointercapture'].forEach(t => pad.addEventListener(t, padEnd));
            root.querySelectorAll('.vb').forEach(b => {
                let code = null;
                const up = () => { if (code) { setKey(code, false); code = null; } b.classList.remove('on'); };
                b.addEventListener('pointerdown', e => {
                    e.preventDefault();
                    try { b.setPointerCapture(e.pointerId); } catch (_) {}
                    up(); code = keysFn()[b.dataset.act]; b.classList.add('on'); setKey(code, true);
                });
                ['pointerup', 'pointercancel', 'lostpointercapture'].forEach(t => b.addEventListener(t, up));
            });
            return { root, releaseAll, me: meFn };
        }
        const vpad2 = $('vpad');
        const vpad1 = vpad2.cloneNode(true); vpad1.id = 'vpad1'; vpad1.classList.add('rot'); body.appendChild(vpad1);
        const ctl1 = makeCtl(vpad1, true, () => P1_KEYS, () => p1);                                           // 마주 보기: 위쪽 1P
        const ctl2 = makeCtl(vpad2, false, () => isF2f() ? P2_KEYS : soloKeys(), () => isF2f() ? p2 : soloMe()); // 마주 보기: 아래쪽 2P / 그 외: 선택한 한 명
        const releaseAll = () => { ctl1.releaseAll(); ctl2.releaseAll(); };

        // --- 설정창 ---
        const ctrlScreen = $('ctrl-screen');
        const ctrlOpen = () => !ctrlScreen.classList.contains('vhide');
        function applyVc() {
            for (const v of [vpad1, vpad2]) {
                v.style.setProperty('--vs', vc.scale / 100);
                v.style.setProperty('--vo', vc.opacity / 100);
                v.classList.toggle('swap', vc.swap);
            }
            body.style.setProperty('--vs', vc.scale / 100);
        }
        function refreshCtrl() {
            $('cOn').textContent = vc.on ? '켜짐' : '꺼짐';
            $('cScale').value = vc.scale; $('cScaleV').textContent = vc.scale + '%';
            $('cOpa').value = vc.opacity; $('cOpaV').textContent = vc.opacity + '%';
            $('cSwap').textContent = vc.swap ? '오른쪽' : '왼쪽';
            $('cPlayer').textContent = isF2f() ? '1P+2P 맞대결' : aiMode ? (solo2() ? '2P' : '1P') + ' (1인용)' : vc.player + 'P';
            $('cPlayer').disabled = aiMode || isF2f();
            applyVc();
        }
        const change = fn => { releaseAll(); fn(); norm(); save(); refreshCtrl(); sync(); };
        const blur = () => { if (document.activeElement) document.activeElement.blur(); };
        function openCtrl() { ctrlScreen.classList.remove('vhide'); body.classList.add('ctrl-open'); refreshCtrl(); sync(); blur(); }
        function closeCtrl() { ctrlScreen.classList.add('vhide'); body.classList.remove('ctrl-open'); sync(); blur(); }
        $('ctrlBtn').addEventListener('click', openCtrl);
        $('cClose').addEventListener('click', closeCtrl);
        // --- 일시정지 메뉴: 카드 목록 (등급 높은 순) ---
        const clScreen = $('cardlist-screen');
        const clOpen = () => !clScreen.classList.contains('vhide');
        function openCardList() {
            const tiers = Object.keys(RARITY).sort((a, b) => RANK[b] - RANK[a]);
            $('cl-body').innerHTML = tiers.map(r => '<div class="cl-group cl-' + r + '"><div class="cl-head">' + RARITY[r].nm + (RARITY[r].w ? ' · ' + RARITY[r].w + '%' : ' · 장풍 + 점프 / 대쉬 + 칼을 모으면 자동으로 합쳐짐') + '</div>'
                + CARD_POOL.filter(c => c.r === r).map(c => '<div class="cl-item"><div class="cl-nm">' + cardName(c) + '</div><div class="cl-ds">' + c.ds + '</div></div>').join('') + '</div>').join('');
            clScreen.classList.remove('vhide'); blur();
        }
        function closeCardList() { clScreen.classList.add('vhide'); clHeld.clear(); blur(); }
        // 카드 목록이 열려 있는 동안 위/아래 방향키(화면 조작키 · 키보드)를 누르고 있으면 목록이 스크롤됨
        const clHeld = new Set(), CL_UP = ['KeyW', 'ArrowUp'], CL_DOWN = ['KeyS', 'ArrowDown'];
        const prOpen = () => practice && paused;   // 연습 모드 능력 목록(ESC)이 열려 있음
        window.addEventListener('keydown', e => { if ((clOpen() || prOpen()) && (CL_UP.includes(e.code) || CL_DOWN.includes(e.code))) { clHeld.add(e.code); e.preventDefault(); } }, true);
        window.addEventListener('keyup', e => clHeld.delete(e.code), true);
        let clLast = performance.now();
        (function clTick(t) {
            const dt = Math.min(0.05, Math.max(0, (t - clLast) / 1000)); clLast = t;
            if (clOpen() || prOpen()) {
                const v = (CL_DOWN.some(k => clHeld.has(k)) ? 1 : 0) - (CL_UP.some(k => clHeld.has(k)) ? 1 : 0);
                if (v) (clOpen() ? $('cl-body') : $('pr-body')).scrollTop += v * 420 * dt;
            }
            requestAnimationFrame(clTick);
        })(clLast);
        $('cardsBtn').addEventListener('click', openCardList);
        $('clClose').addEventListener('click', closeCardList);
        // 카드 목록이 열려 있을 땐 ESC = 목록만 닫기, Enter = 처음 화면으로 가지 않게 막기
        window.addEventListener('keydown', e => {
            if (!clOpen()) return;
            if (e.code === 'Escape') { e.preventDefault(); e.stopImmediatePropagation(); closeCardList(); }
            else if (e.code === 'Enter' || e.code === 'NumpadEnter') e.stopImmediatePropagation();
        }, true);
        $('cOn').addEventListener('click', () => change(() => { vc.on = !vc.on; }));
        $('cSwap').addEventListener('click', () => change(() => { vc.swap = !vc.swap; }));
        $('cPlayer').addEventListener('click', () => change(() => { vc.player = vc.player === 1 ? 2 : 1; }));
        $('cReset').addEventListener('click', () => change(() => { vc = { ...DEF }; }));
        $('cScale').addEventListener('input', e => change(() => { vc.scale = e.target.value; }));
        $('cOpa').addEventListener('input', e => change(() => { vc.opacity = e.target.value; }));
        // 설정창이 열려 있을 땐 ESC = 설정창만 닫기, Enter = 처음 화면으로 가지 않게 막기
        window.addEventListener('keydown', e => {
            if (!ctrlOpen()) return;
            if (e.code === 'Escape') { e.preventDefault(); e.stopImmediatePropagation(); closeCtrl(); }
            else if (e.code === 'Enter' || e.code === 'NumpadEnter') e.stopImmediatePropagation();
        }, true);

        // --- 일시정지 메뉴 / 새 경기 버튼 ---
        $('resumeBtn').addEventListener('click', () => { togglePause(); blur(); });
        $('pauseBtn').addEventListener('click', () => { togglePause(); blur(); });
        $('rematchBtn').addEventListener('click', () => {
            for (const t of ['keydown', 'keyup']) window.dispatchEvent(new KeyboardEvent(t, { code: 'Enter', key: 'Enter', bubbles: true, cancelable: true }));
            blur();
        });

        // --- 화면 상태에 따라 보이기/숨기기 ---
        let lockedPt = false;
        function sync() {
            const co = ctrlOpen();
            if (co && started && !paused) closeCtrl();
            const f2f = isF2f(), mob = (IS_TOUCH && vc.on) || f2f;   // 모바일 모드를 끄면 폰이어도 일반(PC) 화면 · 가로 가능
            body.classList.toggle('f2f', f2f);
            body.classList.toggle('touch', mob);
            body.classList.toggle('playing', started);
            body.classList.toggle('pick1', f2f && picking && pickPlayer === p1);
            const cl = clOpen(), pr = prOpen();
            const pickPad = picking && !paused && !(aiMode && pickPlayer === aiSelf) && !(window.NET && NET.on && NET.notMyPick());   // 카드 고르는 사람의 조작키 (좌우 = 고르기 · 공격 = 선택 · 앞뒤앞앞뒤+공격 = 개발자 모드)
            const show = mmOn() && ((started && !paused && !picking) || co || cl || pr || pickPad);
            const p1Pick = f2f && pickPad && pickPlayer === p1;   // 마주 보기: 1P가 고를 땐 위쪽(1P) 조작키만
            vpad2.classList.toggle('vhide', !(show && !(pickPad && p1Pick)));
            vpad1.classList.toggle('vhide', !(show && f2f && !cl && !pr && (!pickPad || p1Pick)));
            body.classList.toggle('picking-pad', pickPad && show);
            body.classList.toggle('ptsolo', mob && started && !f2f);   // 모바일 1인용도 세로 화면 레이아웃
            body.classList.toggle('me1', mob && started && !f2f && !tutorial && !solo2());   // 혼자 할 때 내 화면이 아래로 오게: 내가 1P이면 위·아래를 맞바꿈
            body.classList.toggle('pad-on', show);
            body.classList.toggle('cl-open', cl && show);
            body.classList.toggle('pr-open', pr && show);
            if (!show || p1Pick) ctl2.releaseAll();
            if (!(show && f2f && !cl && !pr && (!pickPad || p1Pick))) ctl1.releaseAll();
            const wantLock = vc.on && started && !body.classList.contains('focus');   // '내 화면만 크게'를 켜면 가로로도 할 수 있게 세로 고정을 풀어 둠
            if (IS_TOUCH && screen.orientation && screen.orientation.lock && lockedPt !== wantLock) {   // 전투 중에는 세로 고정 (전체화면에서만 동작하는 기기가 많음)
                lockedPt = wantLock;
                try { Promise.resolve(wantLock ? screen.orientation.lock('portrait') : screen.orientation.unlock()).catch(() => {}); } catch (e) {}
            }
            for (const c of [ctl1, ctl2]) {
                const m = c.me(), j = c.root.querySelector('.vb-jump');
                j.classList.add('vhide');   // 점프 버튼은 따로 두지 않고 특수 버튼 하나로 통일
                const sp = c.root.querySelector('.vb-ink');
                sp.classList.toggle('vhide', !(m.canTaunt || m.canInk || m.canKi || m.canShoryu || m.canBlink || m.canClone || m.canInvis || m.canHeal || m.canObst));
                sp.style.whiteSpace = 'pre-line';
                sp.textContent = m.canTaunt ? '도발' : m.canKi ? '장풍' : m.canInk ? '먹물' : m.canBlink ? '순간\n이동' : m.canClone ? '분신' : m.canInvis ? '투명' : m.canHeal ? '힐' : m.canObst ? '장애물' : '승룡권';
            }
            $('pauseBtn').classList.toggle('vhide', !(mob && started && !paused && !tutorial));
            $('rematchBtn').classList.toggle('vhide', !(started && !paused && matchOver && gameOver && !picking && (mob || mmOn())));
        }
        setInterval(sync, 100);
        applyVc();

        // --- 전체화면 (모바일): 시작 화면을 처음 터치할 때 진입 ---
        const de = document.documentElement;
        const reqFs = de.requestFullscreen || de.webkitRequestFullscreen;
        const exitFs = document.exitFullscreen || document.webkitExitFullscreen;
        const inFs = () => !!(document.fullscreenElement || document.webkitFullscreenElement);
        function goFs() {
            if (!IS_TOUCH || !reqFs || inFs()) return;
            Promise.resolve(reqFs.call(de, { navigationUI: 'hide' })).catch(() => {});
        }
        if (!reqFs) { $('fsBtn').style.display = 'none'; if (IS_TOUCH) $('fsHint').classList.add('show'); }
        $('fsBtn').addEventListener('click', () => { inFs() ? exitFs.call(document) : goFs(); blur(); });
        const fsLabel = () => { $('fsBtn').textContent = inFs() ? '전체화면 해제' : '전체화면'; };
        document.addEventListener('fullscreenchange', fsLabel); document.addEventListener('webkitfullscreenchange', fsLabel);
        $('start-screen').addEventListener('click', goFs);

        // --- 모바일 전투는 세로 화면만: 가로로 돌리면 안내를 띄우고 일시정지 ---
        const landscape = matchMedia('(orientation: landscape)');
        const onOrient = () => { if (IS_TOUCH && vc.on && landscape.matches && started && !paused && !tutorial && !body.classList.contains('focus')) togglePause(); };
        landscape.addEventListener ? landscape.addEventListener('change', onOrient) : landscape.addListener(onOrient);

        // --- 모바일: 스크롤/확대/길게 눌러 메뉴 막기 ---
        if (IS_TOUCH) {
            document.addEventListener('contextmenu', e => e.preventDefault());
            document.addEventListener('touchmove', e => { if (!e.target.closest('#ctrl-panel, #card-list')) e.preventDefault(); }, { passive: false });
        }
    })();
    </script>
<script>
// ===== 멀티플레이 (온라인 2인 대전) =====
// 방식: 서버 없이 PeerJS(WebRTC)로 1:1 연결. 매칭 대기자(방장 = 1P)가 게임을 계산하고,
//       상대(손님 = 2P)는 키 입력만 보내고 방장이 보내 주는 상태를 받아 그리기만 함.
// 매칭: 'yacha-mm1-0' ~ 'yacha-mm1-11' 슬롯 이름을 먼저 차지한 사람이 대기자가 되고,
//       나중에 찾는 사람이 슬롯을 훑어서 대기자를 발견하면 둘이 연결됨.
const NET = (() => {
    const SLOTS = 12, PFX = 'yacha-mm1-';
    const PEER_OPTS = { debug: 0 };   // 자체 PeerJS 서버를 쓰려면 { host, port, path, secure } 를 추가
    const PEER_SRC = ['https://cdn.jsdelivr.net/npm/peerjs@1.5.4/dist/peerjs.min.js', 'https://unpkg.com/peerjs@1.5.4/dist/peerjs.min.js'];
    const $ = id => document.getElementById(id);
    const mm = $('mm-screen'), mmTitle = $('mm-title'), mmSub = $('mm-sub'), mmDots = $('mm-dots'), mmCancel = $('mm-cancel');
    const net = { on: false, host: false, guest: false, me: null, searching: false };

    let stage = '', tok = 0, scanPeer = null, slotPeer = null, slotN = 0, conn = null;
    let offered = null, offerTmr = 0, rescan = 0, scanning = false, hb = 0, lastRx = 0, mmHide = 0;

    // ---------- 화면 ----------
    function showMm(title, sub, opt = {}) {
        clearTimeout(mmHide);
        mmTitle.textContent = title; mmSub.textContent = sub || '';
        mmDots.classList.toggle('off', !!opt.noDots);
        mmCancel.style.display = opt.btn === false ? 'none' : '';
        mmCancel.textContent = opt.btn || '취소 [ESC]';
        mm.classList.remove('hidden');
        if (document.activeElement) document.activeElement.blur();
    }
    const hideMm = () => { clearTimeout(mmHide); mm.classList.add('hidden'); };

    // ---------- PeerJS ----------
    function loadLib() {
        if (window.Peer) return Promise.resolve();
        return new Promise((ok, no) => {
            let i = 0;
            const next = () => {
                if (i >= PEER_SRC.length) return no(new Error('lib'));
                const s = document.createElement('script');
                s.src = PEER_SRC[i++];
                s.onload = () => window.Peer ? ok() : next();
                s.onerror = () => { s.remove(); next(); };
                document.head.appendChild(s);
            };
            next();
        });
    }
    function mkPeer(id) {
        return new Promise((ok, no) => {
            const p = new Peer(id || 'yacha-' + Math.random().toString(36).slice(2, 12) + Date.now().toString(36), PEER_OPTS);   // ID 를 직접 정하면 서버에서 ID 를 받아오는 HTTP 요청을 건너뜀
            let opened = false;
            p.on('open', () => { opened = true; ok(p); });
            p.on('error', e => { if (!opened) { try { p.destroy(); } catch (_) {} no(e); } else if (p.__onerr) p.__onerr(e); });
            p.on('disconnected', () => { if (!p.destroyed && (net.searching || net.on)) { try { p.reconnect(); } catch (_) {} } });
        });
    }
    const killPeer = p => { if (p) { try { p.destroy(); } catch (_) {} } };
    const send = m => { if (conn && conn.open) { try { conn.send(m); } catch (_) {} } };

    // ---------- 매칭 ----------
    function cleanup() {
        clearTimeout(offerTmr); clearInterval(rescan); clearInterval(hb);
        offered = null; scanning = false;
        const c = conn, a = scanPeer, b = slotPeer;
        conn = scanPeer = slotPeer = null;
        setTimeout(() => { try { c && c.close(); } catch (_) {} killPeer(a); killPeer(b); }, 150);   // 'bye' 가 먼저 전달되도록 잠깐 뒤에 닫음
    }
    function fail(msg) {
        tok++; net.searching = false; cleanup();
        showMm('연결 실패', msg, { noDots: true, btn: '확인 [ESC]' });
    }
    function cancel() {
        tok++; net.searching = false; cleanup(); hideMm();
    }

    // 모든 슬롯(0 ~ limit-1)에 동시에 접속해 보고, 기다리는 사람이 있으면 그 연결을 돌려줌
    function scan(limit) {
        return new Promise(resolve => {
            let left = limit, won = null, over = false;
            const conns = [];
            const end = () => {
                if (over) return; over = true; clearTimeout(tmr);
                if (scanPeer) scanPeer.__onerr = null;
                for (const c of conns) if (c !== won) { try { c.close(); } catch (_) {} }
                resolve(won);
            };
            const tmr = setTimeout(end, 4000);
            const done = c => { if (!c._done) { c._done = true; if (--left <= 0 && !won) end(); } };
            if (limit <= 0) { end(); return; }
            scanPeer.__onerr = e => {   // 그 슬롯에 아무도 없으면 'peer-unavailable'
                if (!e || e.type !== 'peer-unavailable') return;
                const m = /peer\s+(\S+)/.exec(e.message || '');
                const c = m && conns.find(x => x.peer === m[1]);
                if (c) done(c);
            };
            for (let n = 0; n < limit; n++) {
                const c = scanPeer.connect(PFX + n, { reliable: true, serialization: 'json' });
                conns.push(c);
                c.on('open', () => { if (!over) c.send({ t: 'hi' }); });
                c.on('data', m => {
                    if (c === conn) return onData(m);
                    if (over || !m) return;
                    if (m.t === 'offer') { if (!won) { won = c; conn = c; c.send({ t: 'ok' }); end(); } else c.send({ t: 'no' }); }
                    else if (m.t === 'busy') done(c);
                });
                c.on('close', () => { if (c === conn) lost(); else done(c); });
                c.on('error', () => done(c));
            }
        });
    }
    // 내가 대기자 슬롯을 차지함 (비어 있는 가장 낮은 번호)
    async function claim() {
        for (let n = 0; n < SLOTS; n++) {
            try { slotPeer = await mkPeer(PFX + n); slotN = n; listen(slotPeer); return true; }
            catch (e) { if (e && e.type === 'unavailable-id') continue; throw e; }
        }
        return false;
    }
    function listen(p) {
        p.on('connection', c => {
            c.on('data', m => {
                if (!m) return;
                if (c === conn) return onData(m);
                if (m.t === 'hi') {
                    if (!net.searching || offered || conn) { c.send({ t: 'busy' }); return; }
                    offered = c; c.send({ t: 'offer' });   // 한 번에 한 명에게만 제안 (상대가 'ok' 하면 확정)
                    offerTmr = setTimeout(() => { if (offered === c) offered = null; }, 3500);
                } else if (m.t === 'ok' && c === offered) { conn = c; commit(true); }
                else if (m.t === 'no' && c === offered) offered = null;
            });
            c.on('close', () => { if (offered === c) offered = null; if (c === conn) lost(); });
        });
    }
    function commit(asHost) {
        clearTimeout(offerTmr); clearInterval(rescan); offered = null;
        net.searching = false;
        if (asHost) { killPeer(scanPeer); scanPeer = null; } else { killPeer(slotPeer); slotPeer = null; }   // 연결을 쥔 쪽만 남김
        net.on = true; net.host = asHost; net.guest = !asHost; net.me = asHost ? p1 : p2;
        document.body.classList.add('online');
        lastRx = performance.now();
        hb = setInterval(() => { send({ t: 'p' }); if (performance.now() - lastRx > 8000) lost(); }, 1500);
        showMm('매칭 완료!', asHost ? '당신은 1P (빨강)' : '당신은 2P (파랑)', { noDots: true, btn: false });
        mmHide = setTimeout(hideMm, 1100);
        if (asHost) {
            matchCfg = { ...DEF_CFG };
            resetSync();
            send({ t: 'start', cfg: matchCfg });
            beginGame(false);
        }
    }

    function describe(e) {   // 오류 객체가 비어 있어도 알 수 있는 건 모두 모음
        if (!e) return '알 수 없음';
        const parts = [e.type, e.name, e.message, e.reason, e.code].filter(Boolean);
        try { if (!parts.length) parts.push(JSON.stringify(e, Object.getOwnPropertyNames(e))); } catch (_) {}
        return (parts.join(' / ') || String(e)).slice(0, 160);
    }
    async function find(attempt = 0) {
        if (started || net.searching || net.on) return;
        net.searching = true;
        const my = ++tok;
        showMm('플레이어 찾는 중', '다른 플레이어가 MULTIPLAY 를 누르면 바로 연결돼요');
        try { await loadLib(); } catch (e) { if (my === tok) fail('연결 도구를 불러오지 못했어요.\n인터넷 연결을 확인해 주세요.'); return; }
        if (my !== tok) return;
        try {
            stage = '서버 접속';
            scanPeer = await mkPeer('yacha-c-' + Math.random().toString(36).slice(2, 10) + Date.now().toString(36));   // 서버에서 ID 를 받아오는 요청(server-error 원인)을 건너뛰고 직접 정함
            if (my !== tok) { killPeer(scanPeer); scanPeer = null; return; }
            stage = '대기자 찾기';
            let w = await scan(SLOTS);
            if (my !== tok) return;
            if (w) { commit(false); return; }
            stage = '대기실 만들기';
            while (my === tok) {
                if (await claim()) break;
                showMm('플레이어 찾는 중', '대기실이 꽉 찼어요. 잠시 뒤 다시 찾아요');   // 슬롯 12개 모두 사용 중
                await new Promise(r => setTimeout(r, 3000));
            }
            if (my !== tok) return;
            // 기다리는 동안 번호가 더 낮은 슬롯에 대기자가 생겼는지 주기적으로 확인 (낮은 번호 쪽이 방장)
            rescan = setInterval(async () => {
                if (my !== tok || !net.searching || offered || scanning || conn) return;
                scanning = true;
                const c = await scan(slotN);
                scanning = false;
                if (my !== tok || !net.searching) { if (c && c !== conn) { try { c.close(); } catch (_) {} } return; }
                if (c) commit(false);
            }, 2500);
        } catch (e) {
            const info = describe(e);
            console.error('[YACHA 멀티플레이] 단계: ' + stage + ' / ' + info, e);
            if (my !== tok) return;
            if (attempt < 2) {   // 서버가 잠깐 불안정할 수 있어 자동으로 다시 시도
                tok++; net.searching = false; cleanup();
                showMm('다시 연결하는 중', '매칭 서버 응답이 없어요 (' + (attempt + 1) + '/3)');
                const again = tok;
                setTimeout(() => { if (again === tok && mm.classList.contains('hidden') === false) find(attempt + 1); }, 1500);
                return;
            }
            const why = '\n(단계: ' + stage + ' / ' + info + ')';
            fail('매칭 서버(PeerJS)에 연결하지 못했어요.\n회사 · 학교 와이파이나 VPN, 광고 차단 확장 프로그램이 막고 있을 수 있어요.' + why);
        }
    }

    function lost(msg) {
        if (net.on) {
            goHome();
            showMm('연결이 끊겼어요', msg || '상대가 나갔거나 연결이 불안정해요', { noDots: true, btn: '확인 [ESC]' });
        } else if (net.searching) {   // 확정 전에 끊김: 조용히 처음부터 다시 찾음
            tok++; net.searching = false; cleanup();
            find();
        }
    }
    function leave() {   // 처음 화면으로 갈 때 (goHome 이 부름)
        if (!net.on && !net.searching) return;
        if (net.on) send({ t: 'bye' });
        tok++;
        net.on = net.host = net.guest = false; net.me = null; net.searching = false;
        document.body.classList.remove('online');
        held.clear(); rheld.clear(); iconDown.clear();
        chatBox.classList.add('hidden'); chatLog.innerHTML = '';
        cleanup();
    }

    // ---------- 입력 ----------
    // 키보드 이벤트를 흉내 내서 기존 입력 코드를 그대로 쓴다. 로컬 입력은 전부 '내 쪽' 키로 바꿔서 처리 (WASD · 방향키 아무거나 OK)
    const ACTS = ['up', 'down', 'left', 'right', 'attack', 'guard', 'kick', 'ink'];
    const ACT = {};
    for (const a of ACTS) { ACT[P1_KEYS[a]] = a; ACT[P2_KEYS[a]] = a; }
    const P2_CODES = new Set(ACTS.map(a => P2_KEYS[a]));
    const myKeys = () => net.me === p1 ? P1_KEYS : P2_KEYS;
    const held = new Set(), rheld = new Set(), iconDown = new Set();
    let injecting = false;
    function inject(type, code) {
        injecting = true;
        try { window.dispatchEvent(new KeyboardEvent(type, { code, key: code, bubbles: true, cancelable: true })); }
        finally { injecting = false; }
    }
    const startVisible = () => !startScreen.classList.contains('hidden');
    function onKey(e) {
        if (e.target === chatInput) return;   // 채팅 입력 중
        const down = e.type === 'keydown';
        if (!net.on) {
            if (net.searching || !mm.classList.contains('hidden')) {   // 찾는 중 / 안내창: 다른 키는 모두 막고 ESC 로 닫기
                e.stopImmediatePropagation(); e.preventDefault();
                if (down && e.code === 'Escape' && !e.repeat) { net.searching ? cancel() : hideMm(); }
            } else if (down && !e.repeat && e.code === 'Digit3' && !started && startVisible() && !matchOpen() && !levelOpen()) {
                e.stopImmediatePropagation(); find();
            }
            return;
        }
        if (injecting) return;   // 우리가 만든 이벤트: 그대로 통과
        if (!mm.classList.contains('hidden') && down && e.code === 'Escape') { hideMm(); e.stopImmediatePropagation(); return; }
        if (e.code === 'KeyT' && !injecting) { e.stopImmediatePropagation(); e.preventDefault(); if (down && !e.repeat) openChat(); return; }   // T = 채팅
        const act = ACT[e.code];
        if (act) {
            e.stopImmediatePropagation(); e.preventDefault();
            const code = myKeys()[act];
            if (down === held.has(code)) return;   // 반복 입력 · 중복 뗌 무시
            down ? held.add(code) : held.delete(code);
            if (net.host) inject(e.type, code); else send({ t: 'k', c: code, d: down ? 1 : 0 });
            return;
        }
        if (e.code === 'Escape' || e.code === 'KeyM') return;   // 메뉴 · 음소거는 그대로
        const enter = e.code === 'Enter' || e.code === 'NumpadEnter';
        if (net.guest) {   // 손님은 게임 로직을 돌리지 않으므로 나머지 키는 막고 필요한 것만 방장에게 전달
            e.stopImmediatePropagation(); e.preventDefault();
            if (!down || e.repeat) return;
            if (enter && picking && pickPlayer === p2) { send({ t: 'k', c: P2_KEYS.attack, d: 1 }); send({ t: 'k', c: P2_KEYS.attack, d: 0 }); }   // Enter = 카드 선택
            else if ((enter || e.code === 'KeyR') && matchOver && gameOver && !picking) send({ t: 'rm' });
            return;
        }
        if (/^(Digit|Numpad)\d$/.test(e.code) || (enter && picking && pickPlayer !== p1)) { e.stopImmediatePropagation(); e.preventDefault(); }   // 개발자 모드 입력 · 상대 카드 대신 고르기 막기
    }
    const releaseHeld = () => {
        if (!net.on) return;
        if (net.guest) for (const c of held) send({ t: 'k', c, d: 0 });
        held.clear();
    };
    window.addEventListener('blur', releaseHeld);
    document.addEventListener('visibilitychange', () => { if (document.hidden) releaseHeld(); });
    for (const t of ['pointerup', 'pointercancel']) window.addEventListener(t, e => {   // 손님이 기술 아이콘에서 손을 뗌
        if (net.guest && iconDown.has(e.pointerId)) { iconDown.delete(e.pointerId); send({ t: 'iu', id: e.pointerId }); }
    }, true);
    $('multiBtn').addEventListener('click', find);
    mmCancel.addEventListener('click', () => { net.searching ? cancel() : hideMm(); });


    // ---------- 채팅 ----------
    const chatLog = $('chat-log'), chatBox = $('chat-box'), chatInput = $('chat-input');
    let chatLast = 0;
    const chatOpen = () => !chatBox.classList.contains('hidden');
    function addChat(who, text) {   // who: 1 | 2 (보낸 쪽)
        const row = document.createElement('div');
        const nm = document.createElement('b');
        nm.textContent = (who === (net.host ? 1 : 2) ? '나' : '상대') + ': ';
        nm.style.color = (who === 1 ? p1 : p2).color;
        row.append(nm, document.createTextNode(text));
        chatLog.appendChild(row);
        while (chatLog.children.length > 6) chatLog.firstChild.remove();
        setTimeout(() => row.remove(), 10000);
    }
    function openChat() {
        if (!net.on || chatOpen()) return;
        releaseHeld();   // 입력하는 동안 캐릭터가 멈추게 누르고 있던 키를 뗌
        chatBox.classList.remove('hidden');
        chatInput.value = '';
        chatInput.focus();
    }
    function closeChat() { chatBox.classList.add('hidden'); chatInput.blur(); }
    function sendChat() {
        const text = chatInput.value.trim().slice(0, 80);
        closeChat();
        if (!text || !net.on) return;
        const now = performance.now();
        if (now - chatLast < 500) return;   // 도배 방지
        chatLast = now;
        addChat(net.host ? 1 : 2, text);
        send({ t: 'chat', m: text });
    }
    // 입력창에서 누른 키는 게임으로 새지 않게 (WASD 를 쳐도 캐릭터가 움직이지 않음)
    for (const t of ['keydown', 'keyup', 'keypress']) chatInput.addEventListener(t, e => {
        e.stopPropagation();
        if (t === 'keydown' && !e.isComposing) {
            if (e.key === 'Enter') { e.preventDefault(); sendChat(); }
            else if (e.key === 'Escape') { e.preventDefault(); closeChat(); }
        }
    });
    $('chat-send').addEventListener('click', sendChat);
    $('chatBtn').addEventListener('click', () => { chatOpen() ? closeChat() : openChat(); });

    // ---------- 소리: 방장에서 난 소리를 손님에게도 ----------
    const bgmOrig = { sfx: bgm.sfx, charge: bgm.charge };
    const lastCh = [null, null, null];
    bgm.sfx = n => {
        if (net.host) { send({ t: 'sn', n }); if (injecting && n === 'deny') return; }   // 손님이 누른 키의 경고음은 손님에게만
        bgmOrig.sfx(n);
    };
    bgm.charge = (pi, v) => {
        if (net.host) { const q = Math.round(v * 50); if (lastCh[pi] !== q) { lastCh[pi] = q; send({ t: 'ch', pi, v }); } }
        bgmOrig.charge(pi, v);
    };

    // ---------- 상태 동기화 (방장 → 손님) ----------
    let last = [{}, {}], lastG = '', lastK = '', lastPk = '', lastO = '', lastC = '', lastCar = '';
    const tgt = [{}, {}];
    const r3 = v => Math.round(v * 1000) / 1000;
    const idxOf = c => CARD_POOL.indexOf(c);
    function resetSync() { last = [{}, {}]; lastG = ''; lastK = ''; lastPk = ''; lastO = ''; lastC = ''; lastCar = ''; }
    function diff(p, l) {   // 바뀐 필드만 (숫자 · 문자 · 불리언 · null / 카드 목록 / 파편 이펙트)
        let d = null;
        for (const k in p) {
            const v = p[k], t = typeof v;
            let w;
            if (v === null || t === 'string' || t === 'boolean') w = v;
            else if (t === 'number') w = r3(v);
            else if (k === 'cards') { w = v.map(idxOf).join(','); if (l.cards !== w) { l.cards = w; (d = d || {}).cards = v.map(idxOf); } continue; }
            else if (k === 'fx') { if (l.fx !== v) { l.fx = v; (d = d || {}).fx = v; } continue; }
            else continue;
            if (l[k] !== w) { l[k] = w; (d = d || {})[k] = w; }
        }
        return d;
    }
    function hostTick() {
        if (!conn || !conn.open) return;
        const d = {};
        const a = diff(p1, last[0]), b = diff(p2, last[1]);
        if (a) d.a = a; if (b) d.b = b;
        const g = [gameOver ? 1 : 0, matchOver ? 1 : 0, round, r3(roundTime), r3(burnT), timeUp ? 1 : 0, r3(roundIntroT), r3(shoryuFxT), winner === p1 ? 1 : winner === p2 ? 2 : 0, r3(roundEndT)];
        const gs = g.join(',');
        if (gs !== lastG) { lastG = gs; d.g = g; }
        const k = kiBalls.map(o => [r3(o.x), r3(o.y), r3(o.dx), r3(o.dy), r3(o.d), r3(o.max), o.owner === p1 ? 1 : 2, o.full ? 1 : 0]);
        const ks = JSON.stringify(k);
        if (ks !== lastK) { lastK = ks; d.k = k; }
        const ob = obstacles.map(o => [r3(o.x), r3(o.y), o.hp]), os = JSON.stringify(ob);   // 장애물 · 분신도 방장이 계산해서 손님에게 보냄
        if (os !== lastO) { lastO = os; d.o = ob; }
        const cl = clones.map(c => [r3(c.x), r3(c.y), r3(c.angle), c.hp, c.owner === p1 ? 1 : 2, c.attacking ? 1 : 0, r3(c.attackT), c.punchHand, c.moving ? 1 : 0, r3(c.hitFx)]), cs = JSON.stringify(cl);
        if (cs !== lastC) { lastC = cs; d.c = cl; }
        const cr = car ? [r3(car.x), r3(car.y), car.dx, car.dy, car.ci, r3(car.warn), car.bus ? 1 : 0] : 0, crs = JSON.stringify(cr);   // 도시 자동차도 방장이 계산해서 손님에게 보냄
        if (crs !== lastCar) { lastCar = crs; d.cr = cr; }
        const pk = picking ? [pickPlayer === p1 ? 1 : 2, pickCards.map(idxOf), pickIdx, introPick ? 1 : 0] : 0;
        const ps = JSON.stringify(pk);
        if (ps !== lastPk) { lastPk = ps; d.pk = pk; setPickText(); }
        for (const _ in d) { d.t = 's'; send(d); break; }
    }
    function setPickText() {   // 카드 선택창 안내 문구: 내 차례 / 상대 차례
        if (!picking) return;
        const mine = pickPlayer === net.me;
        $('card-sub').textContent = mine ? 'A / D (← / →) 로 고르고 Z 로 선택 (탭 · 클릭도 가능)' : '상대가 고르는 중…';
    }
    // 손님: 받은 상태를 그대로 적용 (위치 · 각도는 부드럽게 따라감)
    function applyP(p, o, i) {
        for (const k in o) {
            const v = o[k];
            if (k === 'x' || k === 'y' || k === 'angle') {
                tgt[i][k] = v;
                if (tgt[i].init !== true || (k !== 'angle' && Math.abs(v - p[k]) > 100)) p[k] = v;
            } else if (k === 'cards') p.cards = v.map(n => CARD_POOL[n]).filter(Boolean);
            else p[k] = v;
        }
        tgt[i].init = true;
    }
    function applyState(m) {
        if (m.a) applyP(p1, m.a, 0);
        if (m.b) applyP(p2, m.b, 1);
        if (m.g) {
            const g = m.g;
            gameOver = !!g[0]; matchOver = !!g[1]; round = g[2]; roundTime = g[3]; burnT = g[4]; timeUp = !!g[5];
            roundIntroT = g[6]; shoryuFxT = g[7]; winner = g[8] === 1 ? p1 : g[8] === 2 ? p2 : null; roundEndT = g[9];
        }
        if (m.k) {
            kiBalls.length = 0;
            for (const a of m.k) kiBalls.push({ x: a[0], y: a[1], dx: a[2], dy: a[3], d: a[4], max: a[5], owner: a[6] === 1 ? p1 : p2, full: !!a[7] });
        }
        if (m.o) setObstacles(m.o);
        if ('cr' in m) car = m.cr ? fitCar({ x: m.cr[0], y: m.cr[1], dx: m.cr[2], dy: m.cr[3], ci: m.cr[4], warn: m.cr[5], bus: !!m.cr[6], hit: [true, true] }) : null;
        if (m.c) {
            clones.length = 0;
            for (const a of m.c) {
                const c = mkClone(a[4] === 1 ? p1 : p2, a[0], a[1], a[2]);
                c.hp = a[3]; c.attacking = !!a[5]; c.attackT = a[6]; c.punchHand = a[7]; c.moving = !!a[8]; c.hitFx = a[9];
                clones.push(c);
            }
        }
        if ('pk' in m) applyPick(m.pk);
    }
    let scTmr = 0, showing = false;
    function guestShowPick(idx) {   // 방장이 고른 카드를 손님 화면에서도 2초 크게
        const els = [...cardListEl.children];
        if (!els[idx]) return;
        els.forEach((el, k) => { if (k !== idx) el.style.display = 'none'; else el.classList.add('picked'); });
        cardScreen.classList.add('showpick'); cardScreen.classList.remove('hidden');
        clearTimeout(scTmr); showing = true;
        scTmr = setTimeout(() => { showing = false; cardScreen.classList.remove('showpick'); if (!picking) cardScreen.classList.add('hidden'); }, 2000);
    }
    function applyPick(pk) {
        if (!pk) { if (picking) { picking = false; if (!showing) cardScreen.classList.add('hidden'); } introPick = false; return; }
        const [who, ids, idx, intro] = pk;
        const cards = ids.map(n => CARD_POOL[n]).filter(Boolean);
        const same = pickCards.length === cards.length && cards.every((c, i) => pickCards[i] === c);
        const wasOpen = picking;
        picking = true; pickPlayer = who === 1 ? p1 : p2; pickIdx = idx; introPick = !!intro;
        const title = $('card-title');
        title.textContent = (who === 1 ? 'PLAYER 1' : 'PLAYER 2') + (intro ? ' 시작 능력 선택' : ' 카드 선택');
        title.style.color = pickPlayer.color;
        $('card-dev').style.display = 'none'; cardScreen.classList.remove('dev');
        setPickText();
        if (!same || !wasOpen) {
            clearTimeout(scTmr); showing = false; cardScreen.classList.remove('showpick');
            pickCards = cards;
            cardListEl.innerHTML = '';
            cards.forEach((c, i) => {
                const el = document.createElement('div');
                el.className = 'card ' + (c.kind === 'skill' ? 'skill' : 'stat') + ' r-' + c.r;
                el.innerHTML = (c.r === 'legend' || c.r === 'fusion' ? '<i class="sp s1"></i><i class="sp s2"></i><i class="sp s3"></i>' : '') + '<div class="rar">' + RARITY[c.r].nm + '</div><div class="ic">' + c.ic + '</div><div class="nm">' + cardName(c) + '</div><div class="ds">' + c.ds + '</div>';
                el.addEventListener('click', () => { if (pickPlayer === p2) send({ t: 'pk', i }); });
                cardListEl.appendChild(el);
            });
        }
        renderCards();
        cardScreen.classList.remove('hidden');
    }
    function guestFrame(dt) {
        const k = 1 - Math.exp(-dt * 28);
        [p1, p2].forEach((p, i) => {
            const t = tgt[i];
            if (t.x !== undefined) { p.x += (t.x - p.x) * k; p.y += (t.y - p.y) * k; }
            if (t.angle !== undefined) {
                let df = t.angle - p.angle;
                df = ((df + Math.PI) % (Math.PI * 2) + Math.PI * 2) % (Math.PI * 2) - Math.PI;
                p.angle = Math.abs(df) > 1 ? t.angle : p.angle + df * k;
            }
        });
        if (car) { if (car.warn > 0) car.warn = Math.max(0, car.warn - dt); else { car.x += car.dx * car.speed * dt; car.y += car.dy * car.speed * dt; } }   // 다음 메시지가 올 때까지 자동차도 부드럽게 따라감
        updateUI(); updateStamina(); updateSkills();
        for (const v of views) renderView(v);
    }

    // ---------- 받은 메시지 처리 ----------
    function onData(m) {
        if (!m || typeof m.t !== 'string') return;
        lastRx = performance.now();
        switch (m.t) {
            case 's': if (net.guest) applyState(m); break;
            case 'start':
                if (net.guest && !started) {
                    matchCfg = { ...DEF_CFG, ...m.cfg };
                    tgt[0] = {}; tgt[1] = {};
                    beginGame(false, true);   // 시작 능력 선택은 방장이 진행 (상태가 손님에게 전달됨)
                }
                break;
            case 'k':   // 손님의 키 입력 (2P 키만 허용)
                if (net.host && started && P2_CODES.has(m.c)) {
                    const down = !!m.d;
                    if (down === rheld.has(m.c)) break;
                    down ? rheld.add(m.c) : rheld.delete(m.c);
                    inject(down ? 'keydown' : 'keyup', m.c);
                }
                break;
            case 'pk':   // 손님이 카드를 탭해서 고름
                if (net.host && picking && pickPlayer === p2 && Number.isInteger(m.i) && m.i >= 0 && m.i < pickCards.length) { pickIdx = m.i; confirmCard(); }
                break;
            case 'rm':   // 손님이 새 경기 시작을 누름
                if (net.host && matchOver && gameOver && !picking) inject('keydown', 'Enter'), inject('keyup', 'Enter');
                break;
            case 'ic':   // 손님이 기술 아이콘을 누름 → 2P 아이콘을 대신 눌러 줌
                if (net.host && started && Number.isInteger(m.i)) {
                    const s = skillSlots.find(x => x.player === p2 && x.i === m.i);
                    if (s) { injecting = true; try { s.el.dispatchEvent(new PointerEvent('pointerdown', { pointerId: 1000 + (m.id | 0), bubbles: true, cancelable: true })); } finally { injecting = false; } }
                }
                break;
            case 'iu':
                if (net.host) window.dispatchEvent(new PointerEvent('pointerup', { pointerId: 1000 + (m.id | 0), bubbles: true }));
                break;
            case 'sc': if (net.guest && Number.isInteger(m.i)) guestShowPick(m.i); break;
            case 'fu': if (net.guest) { const a = CARD_POOL[m.p[0]], b = CARD_POOL[m.p[1]], r = CARD_POOL[m.r]; if (a && b && r) playFusion({ parts: [a, b], result: r }, () => {}); } break;
            case 'sn': if (net.guest) bgmOrig.sfx(m.n); break;
            case 'ch': if (net.guest) bgmOrig.charge(m.pi, m.v); break;
            case 'chat': if (typeof m.m === 'string' && m.m) addChat(net.host ? 2 : 1, m.m.slice(0, 80)); break;
            case 'bye': lost('상대가 나갔어요'); break;
        }
    }

    return {
        get on() { return net.on; }, get host() { return net.host; }, get guest() { return net.guest; }, get me() { return net.me; },
        find, leave, hostTick, guestFrame, onKey,
        notMyPick: () => pickPlayer !== net.me,
        menu() { pauseScreen.classList.toggle('hidden'); },   // 온라인에서는 게임이 멈추지 않고 메뉴만 열림
        picked(i) { if (net.host) send({ t: 'sc', i }); },
        fuse(f) { if (net.host) send({ t: 'fu', p: f.parts.map(idxOf), r: idxOf(f.result) }); },
        icon(pl, i, e) {   // true 를 돌려주면 이 누르기는 여기서 처리 끝
            if (injecting) return false;
            if (pl !== net.me) return true;
            if (net.guest) { iconDown.add(e.pointerId); send({ t: 'ic', i, id: e.pointerId }); return true; }
            return false;
        }
    };
})();
window.NET = NET;

// ===== 내 화면만 크게 (ESC 메뉴 버튼): 1인용 · 멀티에서 상대 화면을 숨기고 내 화면만 크게 =====
(() => {
    const btn = document.getElementById('viewBtn');
    let pref = false;
    try { pref = localStorage.getItem('yacha-focus') === '1'; } catch (e) {}
    const mySide = () => NET.on ? NET.me : (started && !tutorial && aiMode) ? (aiSelf === p1 ? p2 : p1) : null;   // 사람이 한 명일 때 내 쪽
    function apply() {
        const side = mySide(), on = pref && !!side;
        btn.style.display = (side || (pauseScreen.classList.contains('startmenu') && !pauseScreen.classList.contains('hidden'))) ? '' : 'none';   // 처음 화면 설정 메뉴에서도 보임
        btn.textContent = '내 화면만 크게: ' + (pref ? 'ON' : 'OFF');
        document.body.classList.toggle('focus', on);
        document.body.classList.toggle('focus-p1', on && side === p1);
        document.body.classList.toggle('focus-p2', on && side === p2);
    }
    btn.addEventListener('click', () => { pref = !pref; try { localStorage.setItem('yacha-focus', pref ? '1' : '0'); } catch (e) {} apply(); btn.blur(); });
    setInterval(apply, 150);
    apply();
})();

// ===== 톱니(설정) 버튼: 처음 화면에서는 설정 메뉴(카드 목록 · 조작키 · 소리), 연습 화면에서는 ESC 와 똑같이 동작 =====
(() => {
    const gear = document.getElementById('gearBtn'), resume = document.getElementById('resumeBtn'), home = document.getElementById('homeBtn');
    const pt = pauseScreen.querySelector('.pause-title'), ps = pauseScreen.querySelector('.pause-sub');
    const menuOpen = () => pauseScreen.classList.contains('startmenu') && !pauseScreen.classList.contains('hidden');
    function openMenu() {
        pauseScreen.classList.add('startmenu'); pauseScreen.classList.remove('hidden');
        resume.textContent = '닫기'; home.style.display = 'none';
        pt.textContent = 'SETTINGS'; ps.textContent = 'ESC 를 눌러 닫기';
        if (document.activeElement) document.activeElement.blur();
    }
    function closeMenu() {
        pauseScreen.classList.add('hidden'); pauseScreen.classList.remove('startmenu');
        resume.textContent = '계속하기'; home.style.display = '';
        pt.textContent = 'PAUSED'; ps.textContent = 'ESC 를 눌러 계속하기';
    }
    gear.addEventListener('click', () => {
        gear.blur();
        if (started) { for (const t of ['keydown', 'keyup']) window.dispatchEvent(new KeyboardEvent(t, { code: 'Escape', key: 'Escape', bubbles: true, cancelable: true })); }   // 연습: ESC 와 동일
        else openMenu();
    });
    resume.addEventListener('click', () => { if (menuOpen()) closeMenu(); });
    window.addEventListener('keydown', e => {   // 처음 화면 메뉴가 열려 있을 땐 ESC 로 닫고, 다른 키가 게임을 시작하지 못하게 막음
        if (!menuOpen()) return;
        if (e.code === 'Escape') { e.stopImmediatePropagation(); e.preventDefault(); closeMenu(); }
        else if (e.code !== 'KeyM') { e.stopImmediatePropagation(); e.preventDefault(); }
    }, true);
    setInterval(() => {
        if (started && !practice && menuOpen()) closeMenu();
        const show = !tutorial && (!started ? (!menuOpen() && document.getElementById('mm-screen').classList.contains('hidden') && matchScreen.classList.contains('hidden') && levelScreen.classList.contains('hidden')) : (practice && !paused));
        gear.classList.toggle('vhide', !show);
    }, 150);
})();

</script>
</body>
</html>
