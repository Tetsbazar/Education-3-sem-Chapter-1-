# Education-3-sem-Chapter-1-
<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Test Bazar — Class 12 | 3rd Sem | All Sets 1-12</title>
<link href="https://fonts.googleapis.com/css2?family=Tiro+Bangla&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Syne',sans-serif;background:#f0faf4;min-height:100vh;color:#1c2e24}
.top-bar{background:#1a7a4a;padding:0.8rem 1.5rem;display:flex;justify-content:space-between;align-items:center;position:sticky;top:0;z-index:100}
.top-logo{font-size:1.1rem;font-weight:800;color:white}.top-logo span{color:#f9a825}
.timer-box{background:rgba(255,255,255,0.15);border-radius:8px;padding:0.4rem 1rem;display:flex;align-items:center;gap:6px;font-size:1rem;font-weight:700;color:white}
.timer-box.danger{background:#dc3545}
.main{max-width:820px;margin:0 auto;padding:1.5rem 1rem}
.hub-header{text-align:center;margin-bottom:2rem}
.hub-header h1{font-family:'Tiro Bangla',serif;font-size:2rem;color:#1c2e24}
.hub-header p{font-family:'Tiro Bangla',serif;font-size:0.95rem;color:#5a7a66;margin-top:0.3rem}
.set-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:1.2rem}
.set-card{background:white;border-radius:14px;padding:1.5rem;border:1.5px solid #c5dccb;transition:all 0.2s;cursor:pointer;color:#1c2e24;box-shadow:0 2px 8px rgba(26,122,74,0.06)}
.set-card:hover{transform:translateY(-3px);border-color:#1a7a4a;box-shadow:0 6px 20px rgba(26,122,74,0.12)}
.set-card .icon{font-size:2.2rem;margin-bottom:0.3rem}
.set-card .set-num{font-weight:700;font-size:1.1rem;color:#1a7a4a}
.set-card .set-title{font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66;margin:0.2rem 0 0.5rem}
.set-card .set-meta{display:flex;gap:1rem;font-size:0.7rem;color:#5a7a66}
.set-card .set-meta span{background:#f0faf4;padding:0.15rem 0.6rem;border-radius:4px}
.quiz-info{background:white;border-radius:12px;padding:1rem 1.2rem;margin-bottom:1.2rem;border:1px solid #c5dccb;display:flex;gap:1rem;flex-wrap:wrap}
.info-item{font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66}
.info-item strong{color:#1a7a4a}
.progress-wrap{background:#c5dccb;border-radius:4px;height:6px;margin-bottom:1.2rem;overflow:hidden}
.progress-fill{height:100%;background:#1a7a4a;border-radius:4px;transition:width 0.3s}
.q-card{background:white;border-radius:14px;padding:1.4rem;margin-bottom:1rem;border:1px solid #c5dccb;box-shadow:0 2px 10px rgba(26,122,74,0.06)}
.q-num{font-size:0.75rem;font-weight:700;color:#e8730a;letter-spacing:1px;text-transform:uppercase;margin-bottom:0.6rem}
.q-text{font-family:'Tiro Bangla',serif;font-size:1rem;color:#1c2e24;line-height:1.7;margin-bottom:1.1rem}
.opts{display:flex;flex-direction:column;gap:0.6rem}
.opt{display:flex;align-items:flex-start;gap:10px;padding:0.7rem 1rem;border:1.5px solid #c5dccb;border-radius:10px;cursor:pointer;transition:all 0.15s;background:white;text-align:left;width:100%;font-family:inherit}
.opt:hover:not(.disabled){border-color:#1a7a4a;background:#f0faf4}
.opt-circle{min-width:28px;height:28px;border-radius:50%;border:1.5px solid #c5dccb;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;color:#5a7a66;flex-shrink:0;transition:all 0.15s}
.opt-text{font-family:'Tiro Bangla',serif;font-size:0.92rem;color:#1c2e24;line-height:1.6;padding-top:2px}
.opt.correct{border-color:#1a7a4a;background:#e8f7ef}
.opt.correct .opt-circle{background:#1a7a4a;border-color:#1a7a4a;color:white}
.opt.wrong{border-color:#dc3545;background:#fdf0f0}
.opt.wrong .opt-circle{background:#dc3545;border-color:#dc3545;color:white}
.opt.disabled{cursor:default}
.explanation{background:#f0faf4;border-left:3px solid #1a7a4a;border-radius:0 8px 8px 0;padding:0.8rem 1rem;margin-top:0.8rem;display:none}
.explanation.show{display:block}
.explanation p{font-family:'Tiro Bangla',serif;font-size:0.88rem;color:#2c4035;line-height:1.7}
.explanation strong{color:#1a7a4a}
.nav-row{display:flex;justify-content:space-between;align-items:center;margin-top:0.8rem}
.score-show{font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66}
.next-btn{background:#1a7a4a;color:white;border:none;padding:0.6rem 1.4rem;border-radius:8px;font-family:'Tiro Bangla',serif;font-size:0.9rem;cursor:pointer;transition:all 0.15s}
.next-btn:hover{background:#2aad68}
.next-btn:disabled{background:#c5dccb;cursor:default}
.result-wrap{background:white;border-radius:14px;padding:2rem;text-align:center;border:1px solid #c5dccb;display:none}
.result-wrap.show{display:block}
.result-icon{font-size:3rem;margin-bottom:0.5rem}
.result-score{font-size:3.5rem;font-weight:800;color:#1a7a4a}
.result-total{font-size:1rem;color:#5a7a66;margin-bottom:0.5rem;font-family:'Tiro Bangla',serif}
.result-grade{font-size:1.2rem;font-weight:600;color:#1c2e24;margin-bottom:1.5rem;font-family:'Tiro Bangla',serif}
.result-bars{display:grid;grid-template-columns:1fr 1fr 1fr;gap:0.8rem;margin-bottom:1.5rem}
.result-bar{background:#f0faf4;border-radius:10px;padding:0.8rem;text-align:center}
.rb-num{font-size:1.4rem;font-weight:800}
.rb-label{font-family:'Tiro Bangla',serif;font-size:0.8rem;color:#5a7a66;margin-top:0.2rem}
.retry-btn{background:#1a7a4a;color:white;border:none;padding:0.75rem 2rem;border-radius:8px;font-family:'Tiro Bangla',serif;font-size:1rem;cursor:pointer;margin-right:0.5rem}
.review-btn{background:white;color:#1a7a4a;border:1.5px solid #1a7a4a;padding:0.75rem 2rem;border-radius:8px;font-family:'Tiro Bangla',serif;font-size:1rem;cursor:pointer}
.back-btn{background:white;color:#5a7a66;border:1.5px solid #c5dccb;padding:0.75rem 2rem;border-radius:8px;font-family:'Tiro Bangla',serif;font-size:1rem;cursor:pointer;margin-top:0.6rem}
.start-wrap{background:white;border-radius:14px;padding:2rem;text-align:center;border:1px solid #c5dccb}
.start-wrap h2{font-family:'Tiro Bangla',serif;font-size:1.4rem;color:#1c2e24;margin-bottom:0.5rem}
.start-wrap p{font-family:'Tiro Bangla',serif;font-size:0.9rem;color:#5a7a66;line-height:1.7;margin-bottom:1.2rem}
.start-info{display:grid;grid-template-columns:1fr 1fr;gap:0.8rem;margin-bottom:1.5rem}
.si{background:#f0faf4;border-radius:10px;padding:0.8rem;text-align:center}
.si-num{font-size:1.4rem;font-weight:800;color:#1a7a4a}
.si-label{font-family:'Tiro Bangla',serif;font-size:0.8rem;color:#5a7a66}
.start-btn{background:#1a7a4a;color:white;border:none;padding:0.85rem 2.5rem;border-radius:10px;font-family:'Tiro Bangla',serif;font-size:1.05rem;cursor:pointer;box-shadow:0 4px 15px rgba(26,122,74,0.3)}
.start-btn:hover{background:#2aad68}
.start-btn:disabled{background:#c5dccb;cursor:not-allowed;box-shadow:none}
.login-overlay{position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.5);display:flex;align-items:center;justify-content:center;z-index:999;display:none}
.login-overlay.active{display:flex}
.login-modal{background:white;border-radius:16px;padding:2.5rem;max-width:420px;width:90%;box-shadow:0 20px 60px rgba(0,0,0,0.3)}
.login-modal h2{font-family:'Tiro Bangla',serif;font-size:1.3rem;color:#1c2e24;text-align:center;margin-bottom:0.3rem}
.login-modal p{font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66;text-align:center;margin-bottom:1.5rem}
.login-modal label{font-size:0.8rem;font-weight:600;color:#1c2e24;display:block;margin-bottom:0.3rem}
.login-modal input{width:100%;padding:0.7rem 1rem;border:1.5px solid #c5dccb;border-radius:8px;font-size:0.95rem;margin-bottom:1rem;font-family:'Tiro Bangla',serif}
.login-modal input:focus{outline:none;border-color:#1a7a4a}
.login-modal .login-btn{width:100%;background:#1a7a4a;color:white;border:none;padding:0.75rem;border-radius:8px;font-size:1rem;font-weight:700;cursor:pointer;font-family:'Tiro Bangla',serif}
.login-modal .login-btn:hover{background:#2aad68}
.login-modal .login-btn:disabled{background:#c5dccb;cursor:not-allowed}
.login-modal .error-msg{color:#dc3545;font-size:0.8rem;text-align:center;margin-top:0.5rem;font-family:'Tiro Bangla',serif;display:none}
.login-modal .limit-info{background:#fff3cd;border:1px solid #ffc107;border-radius:8px;padding:0.6rem 1rem;margin-bottom:1rem;font-family:'Tiro Bangla',serif;font-size:0.8rem;color:#856404;display:none}
.login-modal .set-name-display{background:#f0faf4;border-radius:8px;padding:0.5rem;text-align:center;margin-bottom:1rem;font-family:'Tiro Bangla',serif;font-size:0.9rem;color:#1a7a4a;font-weight:600}
.hidden{display:none !important}
</style>
</head>
<body>

<div class="top-bar">
  <div class="top-logo">Test <span>Bazar</span></div>
  <div class="timer-box" id="timerBox">⏱ <span id="timerDisplay">10:00</span></div>
</div>

<div class="main">

  <!-- ===== LOGIN OVERLAY (শুধু সেট সিলেক্ট করলে আসবে) ===== -->
  <div class="login-overlay" id="loginOverlay">
    <div class="login-modal">
      <h2>🔐 লগইন করুন</h2>
      <p>Test শুরু করতে আপনার ইউজারনেম ও পাসওয়ার্ড দিন</p>
      <div class="set-name-display" id="loginSetName">📚 Set 1</div>
      <div class="limit-info" id="limitInfo">⚠️ <span id="limitMsg"></span></div>
      <label>ইউজারনেম</label>
      <input type="text" id="loginUsername" placeholder="আপনার ইউজারনেম লিখুন">
      <label>পাসওয়ার্ড</label>
      <input type="password" id="loginPassword" placeholder="আপনার পাসওয়ার্ড লিখুন" onkeydown="if(event.key==='Enter') doLoginFromSet()">
      <button class="login-btn" id="loginBtn" onclick="doLoginFromSet()">✅ লগইন করে Test শুরু করো</button>
      <div class="error-msg" id="loginError">❌ ভুল ইউজারনেম বা পাসওয়ার্ড। আবার চেষ্টা করুন।</div>
    </div>
  </div>

  <!-- ===== HUB PAGE ===== -->
  <div id="hubPage">
    <div class="hub-header">
      <h1>📚 Class 12 — ৩য় সেমিস্টার</h1>
      <p>নিচের সেটগুলো থেকে বেছে নিন। Test শুরু করতে সেটে ক্লিক করুন এবং লগইন করুন।</p>
      <div id="hubUserInfo" style="font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66;margin-top:0.5rem;"></div>
    </div>
    <div class="set-grid" id="setGrid"></div>
  </div>

  <!-- ===== TEST AREA ===== -->
  <div id="testArea" class="hidden">
    <div class="quiz-info">
      <div class="info-item">🎓 <strong id="testSetName">শিক্ষাবিজ্ঞান</strong> — Class 12 | 3rd Sem | <span id="testSetLabel">Set 1</span></div>
      <div class="info-item">📝 <span id="testTopic">শিক্ষা মনোবিজ্ঞান ও শিখন প্রক্রিয়া</span></div>
    </div>
    <div class="progress-wrap"><div class="progress-fill" id="progressFill" style="width:0%"></div></div>
    <div class="q-card" id="qCard">
      <div class="q-num" id="qNum">প্রশ্ন ১ / ১৫</div>
      <div class="q-text" id="qText"></div>
      <div class="opts" id="qOpts"></div>
      <div class="explanation" id="explanation"><p id="explanationText"></p></div>
      <div class="nav-row">
        <div class="score-show" id="scoreShow">সঠিক: ০ | ভুল: ০</div>
        <button class="next-btn" id="nextBtn" onclick="nextQ()" disabled>পরবর্তী →</button>
      </div>
    </div>
  </div>

  <!-- ===== RESULT AREA ===== -->
  <div class="result-wrap" id="resultWrap">
    <div class="result-icon" id="resultIcon"></div>
    <div class="result-score" id="finalScore"></div>
    <div class="result-total">/ ১৫</div>
    <div class="result-grade" id="resultGrade"></div>
    <div class="result-bars">
      <div class="result-bar"><div class="rb-num" id="rbCorrect" style="color:#1a7a4a"></div><div class="rb-label">সঠিক</div></div>
      <div class="result-bar"><div class="rb-num" id="rbWrong" style="color:#dc3545"></div><div class="rb-label">ভুল</div></div>
      <div class="result-bar"><div class="rb-num" id="rbPct" style="color:#e8730a"></div><div class="rb-label">স্কোর</div></div>
    </div>
    <div id="attemptInfo" style="font-family:'Tiro Bangla',serif;font-size:0.85rem;color:#5a7a66;margin-bottom:1rem;"></div>
    <button class="retry-btn" onclick="startQuiz(currentSetId)">আবার চেষ্টা করো</button>
    <button class="review-btn" onclick="showReview()">উত্তর দেখো</button>
    <br>
    <button class="back-btn" onclick="goToHub()">← Class 12 Hub এ ফিরে যাও</button>
  </div>

</div>

<script>
// ============================================================
//  ইউজার ডেটাবেস (৯০টি ইউজার) + attempt কাউন্ট (প্রতি সেটের জন্য আলাদা)
// ============================================================
const MAX_ATTEMPTS = 10;
const TOTAL_SETS = 12;

const userData = [
  {username:"alfa_romeo", password:"ARx7P29m", attempts:{}},
  {username:"santos", password:"St8Qv41L", attempts:{}},
  {username:"falcon", password:"Fc3MZ92k", attempts:{}},
  {username:"titan", password:"Ti6Rp84W", attempts:{}},
  {username:"matrix", password:"Mx5Kd73N", attempts:{}},
  {username:"phoenix", password:"Ph9Js28V", attempts:{}},
  {username:"cobra", password:"Cb4Ln65X", attempts:{}},
  {username:"shadow", password:"Sh7Wp19Q", attempts:{}},
  {username:"rocket", password:"Rc2Ty86M", attempts:{}},
  {username:"warrior", password:"Wr8Az34K", attempts:{}},
  {username:"eagle", password:"Eg5Xq72P", attempts:{}},
  {username:"thunder", password:"Th1Vk93R", attempts:{}},
  {username:"dragon", password:"Dr6Hm48N", attempts:{}},
  {username:"panther", password:"Pa9Nc25J", attempts:{}},
  {username:"viking", password:"Vi4Qs87L", attempts:{}},
  {username:"hunter", password:"Hu7Bp31X", attempts:{}},
  {username:"legend", password:"Le2Mz64T", attempts:{}},
  {username:"ranger", password:"Ra8Kd95W", attempts:{}},
  {username:"knight", password:"Kn3Xp57Q", attempts:{}},
  {username:"turbo", password:"Tu6Lv21N", attempts:{}},
  {username:"alpha", password:"Ap9Rm83K", attempts:{}},
  {username:"bravo", password:"Br5Yt42M", attempts:{}},
  {username:"charlie", password:"Ch7Wq16P", attempts:{}},
  {username:"delta", password:"De4Nk78X", attempts:{}},
  {username:"echo", password:"Ec8Jp35V", attempts:{}},
  {username:"foxtrot", password:"Fx2Lm94Q", attempts:{}},
  {username:"gamma", password:"Ga6Xs27T", attempts:{}},
  {username:"helix", password:"He1Vp85N", attempts:{}},
  {username:"inferno", password:"In9Qk43L", attempts:{}},
  {username:"jaguar", password:"Ja5Mz72W", attempts:{}},
  {username:"karma", password:"Ka8Rp14X", attempts:{}},
  {username:"laser", password:"La3Tn67Q", attempts:{}},
  {username:"meteor", password:"Me7Wx29P", attempts:{}},
  {username:"nova", password:"No4Kz86M", attempts:{}},
  {username:"omega", password:"Om2Lp53V", attempts:{}},
  {username:"pegasus", password:"Pe9Xq71N", attempts:{}},
  {username:"quantum", password:"Qu5Vr38K", attempts:{}},
  {username:"rebel", password:"Re8Mz24T", attempts:{}},
  {username:"storm", password:"St1Kp97W", attempts:{}},
  {username:"tornado", password:"To6Nx45Q", attempts:{}},
  {username:"ultra", password:"Ul3Wp82M", attempts:{}},
  {username:"vector", password:"Ve7Lq19X", attempts:{}},
  {username:"wolf", password:"Wo4Rm63P", attempts:{}},
  {username:"xenon", password:"Xe9Tk25N", attempts:{}},
  {username:"yodha", password:"Yo2Vz78K", attempts:{}},
  {username:"zeus", password:"Ze8Mp41Q", attempts:{}},
  {username:"atlas", password:"At5Lx93W", attempts:{}},
  {username:"blaze", password:"Bl1Qn67M", attempts:{}},
  {username:"cyclone", password:"Cy7Rp34T", attempts:{}},
  {username:"dynamo", password:"Dy4Wk82X", attempts:{}},
  {username:"apollo", password:"Ap7Kx94Lm", attempts:{}},
  {username:"archer", password:"Ar3Vp62Qn", attempts:{}},
  {username:"asteroid", password:"As8Tm15Rw", attempts:{}},
  {username:"bandit", password:"Ba5Qz71Kp", attempts:{}},
  {username:"bison", password:"Bi9Ln34Xt", attempts:{}},
  {username:"bullet", password:"Bu2Wr86Mv", attempts:{}},
  {username:"canyon", password:"Ca6Xp29Qk", attempts:{}},
  {username:"captain", password:"Cp1Mz75Ln", attempts:{}},
  {username:"comet", password:"Co8Tk43Wp", attempts:{}},
  {username:"cyclonex", password:"Cy4Vr92Km", attempts:{}},
  {username:"diesel", password:"Di7Lp18Qx", attempts:{}},
  {username:"domino", password:"Do3Wn67Rt", attempts:{}},
  {username:"duke", password:"Du9Kx25Mv", attempts:{}},
  {username:"empire", password:"Em5Qp84Ln", attempts:{}},
  {username:"explorer", password:"Ex2Vz39Kt", attempts:{}},
  {username:"fighter", password:"Fi8Lm71Qw", attempts:{}},
  {username:"galaxy", password:"Ga4Tk26Xp", attempts:{}},
  {username:"gladiator", password:"Gl7Wp95Mn", attempts:{}},
  {username:"gravity", password:"Gr1Nx53Lq", attempts:{}},
  {username:"hawk", password:"Ha9Kz42Rt", attempts:{}},
  {username:"horizon", password:"Ho5Vm87Xp", attempts:{}},
  {username:"icefire", password:"Ic3Lp16Qn", attempts:{}},
  {username:"impact", password:"Im8Wr74Kt", attempts:{}},
  {username:"ironman", password:"Ir2Xq95Mv", attempts:{}},
  {username:"jetstar", password:"Je6Nk38Lp", attempts:{}},
  {username:"kingston", password:"Ki1Vp72Qw", attempts:{}},
  {username:"lightning", password:"Li9Tm45Rx", attempts:{}},
  {username:"majestic", password:"Ma4Kp83Ln", attempts:{}},
  {username:"monster", password:"Mo7Wz21Qt", attempts:{}},
  {username:"neptune", password:"Ne3Lx96Mv", attempts:{}},
  {username:"ninja", password:"Ni8Qr54Kp", attempts:{}},
  {username:"orbit", password:"Or2Vp73Ln", attempts:{}},
  {username:"patriot", password:"Pa6Tk18Qw", attempts:{}},
  {username:"pioneer", password:"Pi1Xm85Rt", attempts:{}},
  {username:"predator", password:"Pr9Lq47Kv", attempts:{}},
  {username:"proton", password:"Pt4Wn62Mx", attempts:{}},
  {username:"rapid", password:"Ra7Kx93Lp", attempts:{}},
  {username:"samurai", password:"Sa3Vp25Qn", attempts:{}},
  {username:"sniper", password:"Sn8Tm71Rw", attempts:{}},
  {username:"solaris", password:"So2Qk84Mv", attempts:{}},
  {username:"spartan", password:"Sp6Ln39Xt", attempts:{}},
  {username:"striker", password:"St1Wr57Kp", attempts:{}},
  {username:"summit", password:"Su9Xp26Lm", attempts:{}},
  {username:"taurus", password:"Ta5Vz91Qw", attempts:{}},
  {username:"tempest", password:"Te3Kp48Rt", attempts:{}},
  {username:"trident", password:"Tr8Wm72Ln", attempts:{}},
  {username:"valiant", password:"Va2Nx35Qk", attempts:{}},
  {username:"voyager", password:"Vo6Lp97Mx", attempts:{}},
  {username:"wildfire", password:"Wi1Tk64Rv", attempts:{}},
  {username:"zenith", password:"Ze9Qx28Lp", attempts:{}}
];

// ============================================================
//  সব সেটের ডেটা (Set 1-12)
// ============================================================
const allSets = {
  1: {
    name: 'Set 1',
    icon: '🧠',
    topic: 'শিক্ষা মনোবিজ্ঞান ও শিখন প্রক্রিয়া',
    questions: [
      {q: 'শিক্ষা মনোবিজ্ঞানের জনক কাকে বলা হয়?', opts: ['জে. বি. ওয়াটসন', 'এডওয়ার্ড এল. থর্নডাইক', 'জোয়ান ডিউই', 'ফ্রয়েড'], ans: 1, exp: 'এডওয়ার্ড এল. থর্নডাইক (Edward L. Thorndike) কে শিক্ষা মনোবিজ্ঞানের জনক বলা হয়।'},
      {q: 'জন্মগত প্রবৃত্তি (Instinct) তত্ত্ব কে প্রদান করেছেন?', opts: ['পাভলভ', 'থর্নডাইক', 'ম্যাকডগাল', 'স্কিনার'], ans: 2, exp: 'ব্রিটিশ মনোবিজ্ঞানী উইলিয়াম ম্যাকডগাল ১৯০৮ সালে জন্মগত প্রবৃত্তি তত্ত্ব প্রদান করেন।'},
      {q: "'Conditioned Reflex' বা 'শর্তযুক্ত প্রতিবর্ত' তত্ত্ব কে আবিষ্কার করেন?", opts: ['বি. এফ. স্কিনার', 'ইভান পাভলভ', 'জে. বি. ওয়াটসন', 'থর্নডাইক'], ans: 1, exp: 'রাশিয়ার নোবেল বিজয়ী মনোবিজ্ঞানী ইভান পাভলভ শর্তযুক্ত প্রতিবর্ত তত্ত্ব আবিষ্কার করেন।'},
      {q: "'ক্ল্যাসিক্যাল কন্ডিশনার' (Classical Conditioning) কী ধরনের শিখন?", opts: ['সক্রিয় শিখন', 'স্বতঃস্ফূর্ত শিখন', 'অনুকরণমূলক শিখন', 'উদ্দীপক-প্রতিক্রিয়া শিখন'], ans: 3, exp: 'ক্ল্যাসিক্যাল কন্ডিশনার হলো উদ্দীপক-প্রতিক্রিয়া ভিত্তিক এক ধরনের শিখন।'},
      {q: "'অপারেন্ট কন্ডিশনার' (Operant Conditioning) তত্ত্ব কে দিয়েছেন?", opts: ['পাভলভ', 'থর্নডাইক', 'স্কিনার', 'ওয়াটসন'], ans: 2, exp: 'আমেরিকান মনোবিজ্ঞানী বি. এফ. স্কিনার অপারেন্ট কন্ডিশনার তত্ত্ব প্রদান করেন।'},
      {q: "'শিখন' (Learning) -এর থর্নডাইকের সবচেয়ে বিখ্যাত সূত্র কোনটি?", opts: ['প্রস্তুতি সূত্র', 'অভ্যাস সূত্র', 'প্রভাব সূত্র', 'উপরের সবকটি'], ans: 3, exp: 'থর্নডাইকের শিখনের তিনটি প্রধান সূত্র — প্রস্তুতি, অভ্যাস ও প্রভাব সূত্র।'},
      {q: 'মানুষের স্মৃতিশক্তি কয় প্রকার?', opts: ['২ প্রকার', '৩ প্রকার', '৪ প্রকার', '৫ প্রকার'], ans: 1, exp: 'মানুষের স্মৃতিশক্তি প্রধানত ৩ প্রকার — সংবেদন, স্বল্পমেয়াদী ও দীর্ঘমেয়াদী স্মৃতি।'},
      {q: "'পর্যবেক্ষণমূলক শিখন' (Observational Learning) তত্ত্ব কে দিয়েছেন?", opts: ['পাভলভ', 'স্কিনার', 'বান্দুরা', 'থর্নডাইক'], ans: 2, exp: 'কানাডীয় মনোবিজ্ঞানী আলবার্ট বান্দুরা পর্যবেক্ষণমূলক শিখন তত্ত্ব প্রদান করেন।'},
      {q: 'বুদ্ধিমত্তার দ্বি-উপাদান (Two-factor) তত্ত্ব কে দিয়েছেন?', opts: ['থার্স্টোন', 'গিলফোর্ড', 'স্পিয়ারম্যান', 'গার্ডনার'], ans: 2, exp: 'ব্রিটিশ মনোবিজ্ঞানী চার্লস স্পিয়ারম্যান ১৯০৪ সালে দ্বি-উপাদান তত্ত্ব প্রদান করেন।'},
      {q: 'বুদ্ধিমত্তার বহু-উপাদান (Multiple Intelligence) তত্ত্ব কে দিয়েছেন?', opts: ['গার্ডনার', 'থার্স্টোন', 'গিলফোর্ড', 'স্পিয়ারম্যান'], ans: 0, exp: 'আমেরিকান মনোবিজ্ঞানী হাওয়ার্ড গার্ডনার বহু-উপাদান বুদ্ধিমত্তা তত্ত্ব প্রদান করেন।'},
      {q: 'মাসলো (Maslow) -এর প্রয়োজন স্তরক্রম তত্ত্বে সর্বোচ্চ স্তর কোনটি?', opts: ['আত্মসম্মান', 'নিরাপত্তা', 'আত্মবাস্তবায়ন', 'প্রেম ও স্বত্ব'], ans: 2, exp: 'আব্রাহাম মাসলোর প্রয়োজন স্তরক্রম তত্ত্বে সর্বোচ্চ স্তর হলো আত্মবাস্তবায়ন।'},
      {q: "'মনঃসমীক্ষণ' (Psychoanalysis) তত্ত্বের প্রবক্তা কে?", opts: ['ইয়ুং', 'অ্যাডলার', 'ফ্রয়েড', 'পাভলভ'], ans: 2, exp: 'অস্ট্রিয়ান মনোবিজ্ঞানী সিগমুন্ড ফ্রয়েড মনঃসমীক্ষণ তত্ত্বের প্রবক্তা।'},
      {q: 'শিখনে পুরস্কার ও শাস্তির ধারণা কোন তত্ত্বের সাথে সম্পর্কিত?', opts: ['জ্ঞানতত্ত্ব', 'আচরণবাদ', 'অনুভূতিবাদ', 'গঠনবাদ'], ans: 1, exp: 'পুরস্কার ও শাস্তির ধারণা আচরণবাদ তত্ত্বের সাথে সম্পর্কিত।'},
      {q: 'কিশোর বয়সের প্রধান বৈশিষ্ট্য কোনটি?', opts: ['শারীরিক পরিবর্তন', 'মানসিক পরিবর্তন', 'সামাজিক পরিবর্তন', 'উপরের সবকটি'], ans: 3, exp: 'কিশোর বয়স শারীরিক, মানসিক, সামাজিক ও আবেগিক পরিবর্তনের কাল।'},
      {q: 'পাইগেট (Piaget) -এর জ্ঞানমূলক বিকাশ তত্ত্বে কয়টি স্তর রয়েছে?', opts: ['২টি', '৩টি', '৪টি', '৫টি'], ans: 2, exp: 'জিন পাইগেটের জ্ঞানমূলক বিকাশ তত্ত্বে ৪টি স্তর রয়েছে।'}
    ]
  },
  2: {
    name: 'Set 2',
    icon: '🏛️',
    topic: 'বিশ্ববিদ্যালয় শিক্ষা কমিশন — ধারণা ও সুপারিশ',
    questions: [
      {q: 'প্রত্যেকটি মাধ্যমিক বিদ্যালয়ের অবস্থান হবে—', opts: ['গ্রামের শেষ প্রান্তে', 'গ্রামের শুরুতে', 'গ্রামের কেন্দ্রস্থলে', 'গ্রামের বাইরে'], ans: 2, exp: 'গ্রামীণ মাধ্যমিক বিদ্যালয়গুলি গ্রামের কেন্দ্রস্থলে অবস্থান করবে।'},
      {q: 'গ্রামীণ কলেজ ও বিশ্ববিদ্যালয়গুলি পরিচালনার জন্য থাকবে—', opts: ['পরিচালন সমিতি', 'ম্যানেজিং কমিটি', 'গ্রাম কমিটি', 'পরিচালনা সমিতি'], ans: 0, exp: 'প্রতিটি প্রতিষ্ঠানে পরিচালন সমিতি রাখার কথা বলা হয়।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনের তিনজন বিদেশি সদস্যের নাম—', opts: ['ড. জেমস এফ. ডাফ, ড. আর্থার ই. মরগ্যান, ড. জন টিগার্ট', 'ড. আর্থার ই. মরগ্যান, ড. জেমস এফ. ডাফ, ড. টিগার্ট', 'ড. জন আর্থার ই. মরগ্যান, ড. জন টিগার্ট, ড. জাকির হোসেন', 'ড. জন টিগার্ট, ড. জাকির হোসেন, ড. এ. লক্ষ্মণস্বামী মুদালিয়র'], ans: 0, exp: 'ইংল্যান্ডের ড. জেমস এফ. ডাফ এবং আমেরিকার ড. আর্থার ই. মরগ্যান ও ড. জন টিগার্ট।'},
      {q: 'গ্রামীণ বিশ্ববিদ্যালয়ের উদ্দেশ্য ছিল—', opts: ['গ্রামীণ কৃষি, শিল্প, পশুপালন ইত্যাদির বিজ্ঞানসম্মত উন্নয়ন', 'গ্রামীণ কৃষি ও রাস্তাঘাট প্রভৃতির বিজ্ঞানসম্মত উন্নয়ন', 'গ্রামীণ শিল্প, পশুপালন ও মৎস্যচাষের বিজ্ঞানসম্মত উন্নয়ন', 'গ্রামীণ পানীয় জল ও স্বাস্থ্যের উন্নয়ন'], ans: 0, exp: 'গ্রামীণ অর্থনীতি, শিল্প ও পশুপালনের সার্বিক উন্নয়নই ছিল গ্রামীণ বিশ্ববিদ্যালয়ের প্রধান লক্ষ্য।'},
      {q: 'শিক্ষার মাধ্যম সম্পর্কে ত্রিভাষা সূত্রটি হল—', opts: ['আঞ্চলিক ভাষা বা মাতৃভাষা, রাষ্ট্রীয় ভাষা (হিন্দি), ইংরেজি ভাষা', 'মাতৃভাষা, বিদেশি যে-কোনো ভাষা, রাষ্ট্রীয় ভাষা', 'রাষ্ট্রীয় ভাষা, ইংরেজি ভাষা, উর্দু ভাষা', 'আঞ্চলিক ভাষা, উর্দু ভাষা, হিন্দি ভাষা'], ans: 0, exp: 'বিশ্ববিদ্যালয় শিক্ষা কমিশন মাধ্যমিক থেকে বিশ্ববিদ্যালয় স্তর পর্যন্ত ত্রিভাষা সূত্রের সুপারিশ প্রথম করেছিল।'},
      {q: 'স্নাতক স্তরে কোন্ ধরনের ধর্মীয় শিক্ষা দেওয়া হয়?', opts: ['মহাপুরুষদের জীবনী পাঠ', 'ধর্মীয় গ্রন্থের সংকলন পাঠ', 'ধর্মীয় দর্শনের মূল সমস্যা নিয়ে আলোচনা', 'সব ক-টি'], ans: 3, exp: 'স্নাতক স্তরে ধর্মীয় শিক্ষার জন্য তিনটি স্তরে ভিন্ন ভিন্ন বিষয়ের কথা বলা হয়েছিল।'},
      {q: 'UGC-এর সম্পূর্ণ নাম—', opts: ['University Grants Commission', 'University Grants Committee', 'Universal Grants Commission', 'University Grade Commission'], ans: 0, exp: 'উচ্চশিক্ষার ব্যয়ভার নির্বাহের জন্য UGC বা বিশ্ববিদ্যালয় মঞ্জুরি কমিশন গঠনের সুপারিশ করা হয়।'},
      {q: 'স্বাধীনতা লাভের পর প্রথম শিক্ষা কমিশন হল—', opts: ['মুদালিয়র কমিশন', 'কোঠারি কমিশন', 'রাধাকৃষ্ণণ কমিশন', 'অশোক মিত্র কমিশন'], ans: 2, exp: '১৯৪৮ সালে রাধাকৃষ্ণণ কমিশন গঠিত হয়, যা স্বাধীন ভারতের প্রথম শিক্ষা কমিশন।'},
      {q: 'রাধাকৃষ্ণণ কমিশন (1948-49)-এ ভারতীয় সদস্য সংখ্যা হল—', opts: ['আটজন', 'দশজন', 'তিনজন', 'সাতজন'], ans: 3, exp: 'মোট ১০ জন সদস্যের মধ্যে ৭ জন ছিলেন ভারতীয় শিক্ষাবিদ।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষা কমিশন (1948-49)-এ বিদেশি সদস্য সংখ্যা হল—', opts: ['তিনজন', 'পাঁচজন', 'সাতজন', 'আটজন'], ans: 0, exp: 'তিনজন বিদেশি শিক্ষাবিদ এই কমিশনের সদস্য ছিলেন।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষা কমিশন (1948-49)-এর সুপারিশটি ছিল—', opts: ['২০৭ পৃষ্ঠার', '৭৪৭ পৃষ্ঠার', '৫০৯ পৃষ্ঠার', '৪৭৭ পৃষ্ঠার'], ans: 1, exp: '১৯৪৯ সালের আগস্টে জমা দেওয়া রিপোর্টটি ছিল ৭৪৭ পৃষ্ঠার।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষা কমিশনে উত্তর বুনিয়াদি শিক্ষার জন্য সময়কালের সুপারিশ করা হয়—', opts: ['পাঁচ বছর', 'ছয় বছর', 'তিন বছর', 'তিন-চার বছর'], ans: 3, exp: 'প্রাথমিক শিক্ষার পর মাধ্যমিক স্তরের শিক্ষাকাল ছিল ৩-৪ বছর।'},
      {q: 'NCRHE-এর সম্পূর্ণ নাম কী?', opts: ['National Central for Rural Higher Education', 'National Council for Rural Heard Education', 'National Council for Rural Higher Education', 'National Council for Realized Higher Education'], ans: 2, exp: '১৯৫৬ সালে গ্রামীণ উচ্চশিক্ষার প্রসারের জন্য NCRHE গঠন করা হয়েছিল।'},
      {q: 'রাধাকৃষ্ণণ কমিশন, শিক্ষাপ্রতিষ্ঠানগুলিতে দিনের কাজ শুরু করার আগে কয়েক মিনিট কীসের সুপারিশ করা হয়?', opts: ['নীরব প্রার্থনার', 'জাতীয় সংগীত গাওয়ার', 'খবর পড়ার', 'গান গাওয়ার'], ans: 0, exp: 'ধর্ম ও আধ্যাত্মিকতার প্রতি শ্রদ্ধাশীল হতে নীরব প্রার্থনার সুপারিশ করা হয়েছিল।'},
      {q: 'জাতীয় উন্নয়নের মূল ভিত্তি হল—', opts: ['শিক্ষা', 'আস্থা', 'শিল্প', 'বাণিজ্য'], ans: 0, exp: 'স্বাধীন ভারতের সমাজ ও জাতীয় জীবনের অগ্রগতি শিক্ষার মাধ্যমেই সম্ভব।'}
    ]
  },
  3: {
    name: 'Set 3',
    icon: '📜',
    topic: 'রাধাকৃষ্ণণ কমিশনের বিভিন্ন ধারা ও সুপারিশ',
    questions: [
      {q: 'DPI-এর সম্পূর্ণ নাম হল—', opts: ['District of Public Instruction', 'Director of Public Institution', 'Director of Public Instruction', 'Director of Public Instruction'], ans: 2, exp: 'শিক্ষা প্রশাসনের সর্বোচ্চ স্তরে Director of Public Instruction-এর গুরুত্বপূর্ণ ভূমিকা রয়েছে।'},
      {q: 'বহুমুখী বিদ্যালয়ের উদ্দেশ্য হল—', opts: ['শিক্ষার্থীর চাহিদা ও সামর্থ্য অনুযায়ী শিক্ষা', 'শিক্ষার্থীকে গুরুত্ব না দিয়ে শিক্ষা', 'শিক্ষক নির্ভর শিক্ষার ব্যবস্থা', 'কারিগরি শিক্ষা প্রদান'], ans: 0, exp: 'একই ছাদের তলায় শিক্ষার্থীদের নানা রুচি ও সামর্থ্য অনুসারে শিক্ষার সুযোগ দেওয়াই এর লক্ষ্য।'},
      {q: 'রাধাকৃষ্ণণ কমিশনের একজন বিদেশি সদস্য হলেন—', opts: ['ড. জাকির হোসেন', 'জন ডিউই', 'ড. জন টিগার্ট', 'ড. এ. লক্ষ্মণস্বামী মুদালিয়র'], ans: 2, exp: 'আমেরিকার শিক্ষাবিদ ড. জন টিগার্ট ছিলেন এই কমিশনের বিদেশি সদস্য।'},
      {q: 'রাধাকৃষ্ণণ কমিশনের একজন ভারতীয় সদস্য হলেন—', opts: ['ড. জেমস এফ. ডাফ', 'রবীন্দ্রনাথ ঠাকুর', 'ড. এস. কোঠারি', 'ড. কমল নারায়ণ বহল'], ans: 3, exp: 'ড. কমল নারায়ণ বহল ছিলেন রাধাকৃষ্ণণ কমিশনের উল্লেখযোগ্য ভারতীয় সদস্য।'},
      {q: 'বিশ্ববিদ্যালয় কমিশন সুপারিশটি সরকারের কাছে পেশ করেন—', opts: ['১৯৪৯ খ্রিস্টাব্দের নভেম্বর মাসে', '১৯৪৮ খ্রিস্টাব্দের আগস্ট মাসে', '১৯৪৯ খ্রিস্টাব্দের জুন মাসে', '১৯৪৯ খ্রিস্টাব্দের আগস্ট মাসে'], ans: 3, exp: '১৯৪৮ সালের নভেম্বরে কাজ শুরু করে ১৯৪৯ সালের আগস্টে তারা সুপারিশটি জমা দেন।'},
      {q: 'UGC গঠনের একটি উদ্দেশ্য হল—', opts: ['কলেজগুলিকে আর্থিক সাহায্য দান', 'কলেজ ও বিশ্ববিদ্যালয়গুলিকে আর্থিক সাহায্য দান', 'কলেজ পরিচালন কমিটি গঠন', 'সরকারি বিশ্ববিদ্যালয়গুলিকে আর্থিক সাহায্য দান'], ans: 1, exp: 'উচ্চশিক্ষার ব্যয়ভার বহন করে সমস্ত কলেজ ও বিশ্ববিদ্যালয়গুলিকে আর্থিক অনুদান প্রদান করা।'},
      {q: 'গ্রামীণ কলেজ ও বিশ্ববিদ্যালয়গুলি পরিচালনার জন্য থাকবে—', opts: ['পরিচালন ব্যবস্থা', 'পরিচালন সমিতি', 'পরিচালনার কেন্দ্রীয় সংস্থা', 'রাজ্য সংস্থা'], ans: 1, exp: 'প্রতিষ্ঠানগুলিকে স্বাধীনভাবে কাজ করার সুযোগ দিতে পরিচালন সমিতির কথা বলা হয়।'},
      {q: 'গ্রামীণ বিজ্ঞানের সার্টিফিকেট কোর্সের সময়কাল হল—', opts: ['তিন বছর', 'চার বছর', 'দুই বছর', 'এক বছর'], ans: 2, exp: 'গ্রামীণ বিজ্ঞানের সার্টিফিকেট কোর্সের মেয়াদ দু-বছর রাখা হয়েছিল।'},
      {q: 'NCRHE-এর সুপারিশ অনুযায়ী গ্রামসেবা বিজ্ঞানের ডিপ্লোমা কোর্সের সময়কাল হল—', opts: ['চার বছর', 'তিন বছর', 'দুই বছর', 'এক বছর'], ans: 1, exp: 'গ্রামসেবা পেশা হিসেবে গ্রহণের জন্য ডিপ্লোমা কোর্সটি তিন বছরের জন্য নির্দিষ্ট করা হয়।'},
      {q: 'NCRHE-এর সুপারিশে কৃষিবিজ্ঞানে সার্টিফিকেট কোর্সের সময়কাল হল—', opts: ['দুই বছর', 'তিন বছর', 'চার বছর', 'এক বছর'], ans: 0, exp: 'কৃষির উন্নতির জন্য সার্টিফিকেট কোর্সের সময়কাল দু-বছর ধার্য করা হয়েছিল।'},
      {q: 'গ্রামীণ বিশ্ববিদ্যালয়ের স্নাতকোত্তর স্তরে শিক্ষার সময়কাল হল—', opts: ['দুই বছর', 'তিন বছর', 'পাঁচ বছর', 'এক বছর'], ans: 0, exp: 'গ্রামীণ শিক্ষাকাঠামোতে স্নাতকোত্তর শিক্ষার মেয়াদ ২ বছরের জন্য সুপারিশ করা হয়েছিল।'},
      {q: 'বিশ্ববিদ্যালয় মঞ্জুরি কমিটি প্রতিষ্ঠিত হয়—', opts: ['১৯৫৩ খ্রিস্টাব্দে', '১৯৪৫ খ্রিস্টাব্দে', '১৯৪৭ খ্রিস্টাব্দে', '১৯৪৮ খ্রিস্টাব্দে'], ans: 1, exp: 'স্বাধীনতা লাভের ঠিক আগে ১৯৪৫ সালে প্রথম একটি কমিটি গঠিত হয়।'},
      {q: 'বিশ্ববিদ্যালয় মঞ্জুরি কমিশন (UGC) প্রতিষ্ঠিত হয়—', opts: ['১৯৪৫ খ্রিস্টাব্দে', '১৯৪৮ খ্রিস্টাব্দে', '১৯৫৩ খ্রিস্টাব্দে', '১৯৫৬ খ্রিস্টাব্দে'], ans: 2, exp: 'রাধাকৃষ্ণণ কমিশনের সুপারিশের পর ১৯৫৩ সালে এটি প্রতিষ্ঠিত হয়।'},
      {q: 'কোন কমিশনের সুপারিশে বিশ্ববিদ্যালয় মঞ্জুরি কমিশন প্রতিষ্ঠিত হয়?', opts: ['মুদালিয়র কমিশন', 'কোঠারি কমিশন', 'রাধাকৃষ্ণণ কমিশন', 'হান্টার কমিশন'], ans: 2, exp: 'রাধাকৃষ্ণণ কমিশনই প্রথম অনুদান সংস্থা বা UGC গঠনের প্রস্তাব দিয়েছিল।'},
      {q: 'গ্রামীণ উচ্চশিক্ষার বিষয়ে ভারত সরকারকে পরামর্শদানের উদ্দেশ্যে ১৯৫৬ খ্রিস্টাব্দে প্রতিষ্ঠিত হয়—', opts: ['জাতীয় গ্রামীণ উচ্চশিক্ষা পর্ষদ', 'জাতীয় নগর উচ্চশিক্ষা পর্ষদ', 'রাজ্য গ্রামীণ উচ্চশিক্ষা পর্ষদ', 'গ্রামীণ উচ্চশিক্ষা পর্ষদ'], ans: 0, exp: '১৯৫৬ সালে National Council for Rural Higher Education বা NCRHE গঠিত হয়।'}
    ]
  },
  4: {
    name: 'Set 4',
    icon: '📚',
    topic: 'বিশ্ববিদ্যালয় কমিশনের পাঠ্যক্রম, শিক্ষক ও পরীক্ষাব্যবস্থা',
    questions: [
      {q: 'প্রথম কোন কমিশনে ত্রিভাষা সূত্রের কথা বলা হয়েছিল?', opts: ['কোঠারি কমিশনে', 'মুদালিয়র কমিশনে', 'রাধাকৃষ্ণণ কমিশনে', 'হান্টার কমিশনে'], ans: 2, exp: 'প্রথম রাধাকৃষ্ণণ কমিশনই ত্রিভাষা সূত্রের প্রস্তাব দেয়।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষা কমিশনের সম্পাদক ছিলেন—', opts: ['ড. এস. রাধাকৃষ্ণণ', 'ড. জাকির হোসেন', 'ড. তারাচাঁদ', 'ড. এন. কে. সিদ্ধান্ত'], ans: 3, exp: 'ড. নির্মল কুমার সিদ্ধান্ত (এন. কে. সিদ্ধান্ত) ছিলেন কমিশনের সম্পাদক।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষা কমিশনে কলেজের অনার্স কোর্সের জন্য শিক্ষার সময়কালের সুপারিশ করা হয়—', opts: ['দুই বছর', 'তিন বছর', 'পাঁচ বছর', 'আট বছর'], ans: 1, exp: 'অনার্স কোর্সের মেয়াদ তিন বছর করার প্রস্তাব দেওয়া হয়েছিল।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষার পাঠ্যক্রমে কোনটি পেশাগত শিক্ষার বিষয় নয়?', opts: ['বাণিজ্য', 'আইন', 'মানবিক বিষয়', 'চিকিৎসাবিজ্ঞান'], ans: 2, exp: 'মানবিক বিষয় (সাহিত্য, দর্শন, সমাজবিজ্ঞান) সাধারণ শিক্ষার অন্তর্গত।'},
      {q: 'বিশ্ববিদ্যালয় শিক্ষার পাঠ্যক্রমের পেশাগত শিক্ষার বিষয় কোনটি?', opts: ['কৃষি', 'বাণিজ্য', 'আইন', 'সব ক-টি'], ans: 3, exp: 'কমিশনের পেশাগত শিক্ষার তালিকায় এই তিনটি বিষয়সহ ছয়টি বিষয় ছিল।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনে কৃষি শিক্ষাকে অগ্রাধিকার দেওয়ার কথা বলা হয়েছে কেন?', opts: ['সামাজিক অবস্থার উন্নয়নের জন্য', 'জাতীয় অর্থনৈতিক অবস্থার উন্নয়নের জন্য', 'খাদ্যে স্বনির্ভর হওয়ার জন্য', 'দারিদ্র্য দূরীকরণের জন্য'], ans: 1, exp: 'ভারত কৃষিপ্রধান দেশ, তাই কৃষির মাধ্যমে জাতীয় অর্থনীতির উন্নয়নই লক্ষ্য ছিল।'},
      {q: 'বিশ্ববিদ্যালয় কমিশন কয় ধরনের পেশাগত শিক্ষার সুপারিশ করেছেন?', opts: ['চার ধরনের', 'পাঁচ ধরনের', 'তিন ধরনের', 'ছয় ধরনের'], ans: 3, exp: 'ছয় ধরনের পেশাগত শিক্ষা — কৃষি, বাণিজ্য, শিক্ষাবিজ্ঞান, ইঞ্জিনিয়ারিং, আইন ও চিকিৎসাবিজ্ঞান।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনে শিক্ষকদের কয়টি শ্রেণি থাকার কথা বলেছেন?', opts: ['তিনটি', 'চারটি', 'পাঁচটি', 'দুইটি'], ans: 1, exp: 'অধ্যাপক, রিডার, লেকচারার ও ইনস্ট্রাক্টর — এই চারটি শ্রেণিতে ভাগ করার কথা বলা হয়।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনে শিক্ষকদের অবসর গ্রহণের সাধারণ বয়স কত করার সুপারিশ করা হয়েছে?', opts: ['৫৫ বছর', '৬০ বছর', '৬৫ বছর', '৬০ বছর'], ans: 1, exp: 'শিক্ষকদের অবসরের সাধারণ বয়স ৬০ বছর ধার্য করা হয়েছিল।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনের সুপারিশ অনুযায়ী সমগ্র পরীক্ষার মূল্যায়নের কত অংশে অভ্যন্তরীণ পরীক্ষার কথা বলা হয়েছে?', opts: ['দুই-তৃতীয়াংশ', 'এক-তৃতীয়াংশ', 'তিন-চতুর্থাংশ', 'অর্ধাংশ'], ans: 1, exp: 'মোট নম্বরের এক-তৃতীয়াংশ অভ্যন্তরীণ মূল্যায়নের জন্য বরাদ্দ করার কথা বলা হয়।'},
      {q: 'শিক্ষার্থীরা পরীক্ষায় কত শতাংশ নম্বর পেলে প্রথম বিভাগ বলা হবে?', opts: ['৬০ শতাংশে', '৬৫ শতাংশে', '৫৫ শতাংশে', '৭০ শতাংশে'], ans: 3, exp: 'প্রথম বিভাগ পাওয়ার জন্য ন্যূনতম ৭০ শতাংশ নম্বর নির্ধারণ করা হয়েছিল।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনে পরীক্ষাব্যবস্থার সংস্কারের ক্ষেত্রে গ্রেড নম্বর দানের সুপারিশটি কী ছিল?', opts: ['গ্রেড প্রথা বর্জন', 'গ্রেড প্রথা গ্রহণ', 'প্রথম বিভাগের ক্ষেত্রে গ্রেড প্রদান', 'কোনোটিই নয়'], ans: 0, exp: 'রাধাকৃষ্ণণ কমিশন গ্রেড প্রথার পরিবর্তে নম্বরের ভিত্তিতে বিভাগ প্রদানের কথা বলেছিল।'},
      {q: 'শিক্ষার্থীরা কত নম্বর পেলে দ্বিতীয় বিভাগে উত্তীর্ণ বলে ঘোষণা করা হবে?', opts: ['৪০-৫৪ নম্বর', '৪৫-৫৯ নম্বর', '৫৫-৬৯ নম্বর', '৩৫-৪৫ নম্বর'], ans: 2, exp: 'দ্বিতীয় বিভাগের পরিধি ৫৫% থেকে ৬৯% এর মধ্যে নির্দিষ্ট করা হয়েছিল।'},
      {q: 'পরীক্ষক হওয়ার জন্য কত বছরের অভিজ্ঞতা প্রয়োজন?', opts: ['অন্তত চার বছর', 'অন্তত পাঁচ বছর', 'অন্তত তিন বছর', 'অন্তত ছয় বছর'], ans: 1, exp: 'উত্তরপত্র মূল্যায়নে অন্তত পাঁচ বছরের অভিজ্ঞতা সম্পন্ন শিক্ষকদের পরীক্ষক করার কথা বলা হয়েছিল।'},
      {q: 'বিশ্ববিদ্যালয় কমিশন বলেছেন, ধর্মই ভারতের কীসের প্রতীক?', opts: ['আধ্যাত্মিকতার', 'অন্তরাত্মার', 'সামাজিকতার', 'নৈতিকতার'], ans: 1, exp: 'ধর্মকে ভারতীয় সমাজের অন্তরাত্মার প্রতীক বলা হয়েছে।'}
    ]
  },
  5: {
    name: 'Set 5',
    icon: '🎓',
    topic: 'বিশ্ববিদ্যালয় শিক্ষার মান ও মুদালিয়র কমিশনের শুরু',
    questions: [
      {q: 'সাধারণধর্মী শিক্ষার ওপর চাপ কমাতে অধিক সংখ্যায় কোন ধরনের প্রতিষ্ঠান গড়ে তোলার কথা বলা হয়েছে?', opts: ['বৃত্তিমূলক শিক্ষার', 'কারিগরি শিক্ষার', 'সামাজিক শিক্ষার', 'নারীশিক্ষার'], ans: 0, exp: 'বিশ্ববিদ্যালয়ে পঠনপাঠনের মান বজায় রাখতে প্রচুর বৃত্তিশিক্ষা প্রতিষ্ঠান গড়ার ওপর জোর দেওয়া হয়।'},
      {q: 'পরীক্ষাব্যবস্থার কোন বিষয়টি দূর করার জন্য বিশ্ববিদ্যালয় ডিগ্রিকে সরকারি নিয়োগে গুরুত্ব না দিয়ে নিয়োগের জন্য পৃথক পরীক্ষা গ্রহণের সুপারিশ করা হয়েছে?', opts: ['সামগ্রিক উন্নয়ন', 'কুফল দূরীকরণ', 'পরীক্ষার মান উন্নয়ন', 'কোনোটিই নয়'], ans: 1, exp: 'শুধু ডিগ্রির পেছনে ছোটো এবং মুখস্থ বিদ্যার কুফল দূর করতেই ডিগ্রির সঙ্গে চাকরির সম্পর্ক বিচ্ছিন্ন করার কথা বলা হয়।'},
      {q: 'বিশ্ববিদ্যালয় কমিশনে পিএইচডি ডিগ্রির শিক্ষার সময়কাল কত বলা হয়েছে?', opts: ['তিন বছর', 'এক বছর', 'দুই বছর', 'চার বছর'], ans: 2, exp: 'স্নাতকোত্তর ডিগ্রি অর্জনের পর পিএইচডি ডিগ্রির শিক্ষাকাল ন্যূনতম দুই বছর রাখা হয়েছিল।'},
      {q: 'কলেজগুলিতে কার্যদিবস কত দিনের কম হবে না?', opts: ['১৫০ দিন', '১৪০ দিন', '১৮০ দিন', '২০০ দিন'], ans: 2, exp: 'শিক্ষাদানের মান ঠিক রাখতে বছরে অন্তত ১৮০ দিন কলেজ খোলা রাখার নির্দেশ দেওয়া হয়।'},
      {q: 'কলেজ ও বিশ্ববিদ্যালয়গুলিতে সকল বিভাগ মিলিয়ে শিক্ষার্থীর সংখ্যা কত বেশি হবে না?', opts: ['২০০০ ও ৩০০০', '২৫০০ ও ৩৫০০', '১৫০০ ও ৩০০০', '২০০০ ও ৪০০০'], ans: 2, exp: 'কলেজে ১৫০০ এবং বিশ্ববিদ্যালয়ে ৩০০০ শিক্ষার্থীর ঊর্ধ্বসীমা বাঁধা হয়।'},
      {q: 'বিশ্ববিদ্যালয়ে শিক্ষার জন্য বিদ্যালয় স্তরে কত বছরের শিক্ষাগ্রহণ করতে হবে?', opts: ['১০ বছর', '১৪ বছর', '৪০ বছর', '১২ বছর'], ans: 3, exp: 'ইন্টারমিডিয়েট কলেজে বা বিদ্যালয় স্তরে অন্তত ১২ বছর পড়ার পরই বিশ্ববিদ্যালয়ে প্রবেশের যোগ্যতা অর্জন হবে।'},
      {q: 'প্রতিটি কলেজে কোন্ ধরনের ক্লাসের ব্যবস্থা করতে হবে?', opts: ['বৃত্তিমুখী শিক্ষার ক্লাস', 'টিউটোরিয়াল ক্লাস', 'পেশাগত শিক্ষার ক্লাস', 'কারিগরি শিক্ষার ক্লাস'], ans: 1, exp: 'শিক্ষার্থীদের ব্যক্তিগত অসুবিধা দূর করতে প্রতিটি কলেজে টিউটোরিয়াল ক্লাসের ব্যবস্থা রাখার কথা বলা হয়।'},
      {q: 'পশ্চিমবঙ্গের গ্রামীণ সংস্থাটির নাম কী?', opts: ['অমরাবতী', 'ওয়ার্ধা', 'গান্ধিগ্রাম', 'শ্রীনিকেতন'], ans: 3, exp: 'বীরভূমের শ্রীনিকেতন গ্রামীণ শিক্ষার জন্য পরীক্ষামূলকভাবে প্রতিষ্ঠিত ১৪টি গ্রামীণ সংস্থার অন্যতম।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনের সভাপতি ছিলেন—', opts: ['ড. অনাথনাথ বসু', 'ড. এ. লক্ষ্মণস্বামী মুদালিয়র', 'শ্রীমতী হংসরাজ মেহতা', 'শ্রী এম. টি. ব্যাস'], ans: 1, exp: 'তৎকালীন মাদ্রাজ বিশ্ববিদ্যালয়ের উপাচার্য ড. লক্ষ্মণস্বামী মুদালিয়র ছিলেন সভাপতি।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশন গঠিত হয়—', opts: ['২৩ সেপ্টেম্বর ১৯৫২', '২৩ সেপ্টেম্বর ১৯৬২', '২৩ সেপ্টেম্বর ১৯৫২', '২৯ আগস্ট ১৯৫৩'], ans: 0, exp: '১৯৫২ সালের ২৩ সেপ্টেম্বর ভারত সরকার মাধ্যমিক শিক্ষা কমিশন গঠন করে।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনের সম্পাদক ছিলেন—', opts: ['ড. অনাথনাথ বসু', 'ড. এ. লক্ষ্মণস্বামী মুদালিয়র', 'বিদ্যাসাগর', 'বিবেকানন্দ'], ans: 0, exp: 'বিশিষ্ট বাঙালি শিক্ষাবিদ ড. অনাথনাথ বসু মুদালিয়র কমিশনের সম্পাদক ছিলেন।'},
      {q: 'মুদালিয়র কমিশনের সদস্য সংখ্যা ছিল—', opts: ['১০ জন', '৭ জন', '৮ জন', '৯ জন'], ans: 3, exp: 'সভাপতি এবং সম্পাদক সহ মোট ৯ জন সদস্য ছিলেন।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনের বিদেশি সদস্য সংখ্যা ছিল—', opts: ['২ জন', '৩ জন', '৪ জন', '৫ জন'], ans: 0, exp: 'ইংল্যান্ডের জন ক্রিস্টি এবং আমেরিকার কে. আর. উইলিয়াম — এই দুজন বিদেশি সদস্য ছিলেন।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনের সুপারিশের পৃষ্ঠাসংখ্যা হল—', opts: ['২১২টি', '৩৩১টি', '৪১৩টি', '৫০৬টি'], ans: 1, exp: '১৯৫৩ সালের আগস্ট মাসে কমিশন ৩৩১ পৃষ্ঠার এই প্রতিবেদন পেশ করে।'},
      {q: 'দশম শ্রেণিযুক্ত বিদ্যালয় থেকে উত্তীর্ণ শিক্ষার্থীদের জন্য কত বছর প্রাক্-বিশ্ববিদ্যালয় শিক্ষার ব্যবস্থা থাকবে?', opts: ['২ বছরের', '১ বছরের', '৩ বছরের', '২.৫ বছরের'], ans: 1, exp: 'সরাসরি দশম শ্রেণির পর বিশ্ববিদ্যালয়ে যেতে চাইলে ১ বছরের Pre-University Course চালু করা হয়।'}
    ]
  },
  6: {
    name: 'Set 6',
    icon: '📋',
    topic: 'মুদালিয়র কমিশন - সুপারিশসমূহ ও পাঠ্যক্রম',
    questions: [
      {q: 'উচ্চমাধ্যমিক শিক্ষার সময়কাল হল—', opts: ['৪ বছর', '১ বছর', '৩ বছর', '২ বছর'], ans: 2, exp: 'মুদালিয়র কমিশন ইন্টারমিডিয়েট কোর্স তুলে দিয়ে ৩ বছরের উচ্চমাধ্যমিক স্তরের প্রস্তাব দেয়।'},
      {q: 'বিদ্যালয় শিক্ষার কাঠামোটি হল—', opts: ['৫ + ৩ + ৩ = ১১ বছর', '৪ + ৪ + ৩ = ১১ বছর', '৬ + ২ + ৩ = ১১ বছর', '৪ + ৫ + ২ = ১১ বছর'], ans: 0, exp: 'প্রাথমিক (৪/৫ বছর), নিম্ন মাধ্যমিক (৪/৩ বছর) এবং উচ্চমাধ্যমিক (৩ বছর) মিলিয়ে ১১ বছর।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনের (১৯৫২-৫৩) অপর নামটি হল—', opts: ['কোঠারি কমিশন', 'মুদালিয়র কমিশন', 'রাধাকৃষ্ণণ কমিশন', 'হান্টার কমিশন'], ans: 1, exp: 'ড. লক্ষ্মণস্বামী মুদালিয়রের নামানুসারে এটি মুদালিয়র কমিশন নামে পরিচিত।'},
      {q: 'মুদালিয়র কমিশনের সুপারিশ প্রকাশিত হয়—', opts: ['১৯৫৩ খ্রিস্টাব্দের ২৮ আগস্ট', '১৯৫৩ খ্রিস্টাব্দের ২৯ আগস্ট', '১৯৫৩ খ্রিস্টাব্দের ২৩ সেপ্টেম্বর', '১৯৫২ খ্রিস্টাব্দের ২৩ সেপ্টেম্বর'], ans: 1, exp: '১৯৫৩ সালের ২৯ আগস্ট কমিশন তার বিস্তারিত রিপোর্ট প্রকাশ করে।'},
      {q: 'মুদালিয়র কমিশনের মাধ্যমিক বিদ্যালয়ের সুপারিশ হল—', opts: ['একক প্রতিষ্ঠান বিদ্যালয়', 'কমন বিদ্যালয়', 'বহু উদ্দেশ্যসাধক বিদ্যালয়', 'বৃত্তি শিক্ষার বিদ্যালয়'], ans: 2, exp: 'শিক্ষার্থীদের রুচি অনুযায়ী নানা বিষয়ের শিক্ষার সুযোগ দিতে মাল্টিপারপাস স্কুল গড়ার প্রস্তাব দেওয়া হয়।'},
      {q: 'ড. এ. লক্ষ্মণস্বামী মুদালিয়র কে ছিলেন?', opts: ['মাদ্রাজ বিশ্ববিদ্যালয়ের তদানীন্তন উপাচার্য', 'কলকাতা বিশ্ববিদ্যালয়ের তদানীন্তন উপাচার্য', 'দিল্লি বিশ্ববিদ্যালয়ের তদানীন্তন উপাচার্য', 'বিশ্বভারতী বিশ্ববিদ্যালয়ের তদানীন্তন উপাচার্য'], ans: 0, exp: 'তিনি ছিলেন পেশায় চিকিৎসক এবং মাদ্রাজ বিশ্ববিদ্যালয়ের উপাচার্য।'},
      {q: 'CABE-এর সম্পূর্ণ নাম হল—', opts: ['Central Advisory Board of Education', 'Central Advisory Board of Educand', 'Central Advisory Board of Educate', 'Centre Advisory Board of Education'], ans: 0, exp: 'কেন্দ্রীয় শিক্ষা উপদেষ্টা পর্ষদের প্রস্তাবে মুদালিয়র কমিশন গঠিত হয়।'},
      {q: 'মুদালিয়র কমিশনের সুপারিশের মোট অধ্যায়ের সংখ্যা ছিল—', opts: ['৯টি', '৫টি', '১০টি', '১৬টি'], ans: 3, exp: '৩৩১ পৃষ্ঠার প্রতিবেদনটি ১৬টি অধ্যায়ে বিন্যস্ত ছিল।'},
      {q: '"আমাদের মাধ্যমিক শিক্ষা লক্ষ্যহীনতার শিক্ষা" / "weakest link"—এই মন্তব্যটি করেছেন—', opts: ['রাধাকৃষ্ণণ কমিশন', 'মুদালিয়র কমিশন', 'কোঠারি কমিশন', 'হান্টার কমিশন'], ans: 1, exp: 'মুদালিয়র কমিশন মাধ্যমিক শিক্ষাব্যবস্থাকে দুর্বলতম অংশ হিসেবে চিহ্নিত করেছিল।'},
      {q: 'মুদালিয়র কমিশনের একজন ভারতীয় সদস্য হলেন—', opts: ['জন ক্রিস্টি', 'কে. আর. উইলিয়াম', 'ফ্রয়েবেল', 'শ্রীমতী হংসরাজ মেহতা'], ans: 3, exp: 'শ্রীমতী হংসরাজ মেহতা ছিলেন কমিশনের ৭ জন ভারতীয় সদস্যের একজন।'},
      {q: 'মুদালিয়র কমিশনে একজন বিদেশি সদস্য হলেন—', opts: ['ড. অনাথনাথ বসু', 'শ্রী এন. টি ব্যাস', 'জন ক্রিস্টি', 'শ্রী কে. জি. সাইয়াদ্দিন'], ans: 2, exp: 'ইংল্যান্ডের জন ক্রিস্টি ছিলেন বিদেশি সদস্য।'},
      {q: 'মুদালিয়র কমিশনের মতে, মাধ্যমিক বিদ্যালয়ে সাপ্তাহিক কাজের সময় হবে—', opts: ['২৫ পিরিয়ড', '৪০ পিরিয়ড', '৪২ পিরিয়ড', '৪৫ পিরিয়ড'], ans: 3, exp: 'সপ্তাহে অন্তত ৪৫ পিরিয়ড ক্লাসের কথা বলা হয়েছিল।'},
      {q: 'SABE-এর সম্পূর্ণ নাম হল—', opts: ['State Advisory Board of Educand', 'State Advisory Board of Education', 'State Advanced Board of Education', 'State Educated of Education'], ans: 1, exp: 'প্রতিটি রাজ্যে SABE বা রাজ্য শিক্ষা উপদেষ্টা পর্ষদ গঠনের সুপারিশ করা হয়।'},
      {q: 'ঐচ্ছিক পাঠ্যক্রমের বাণিজ্য বিভাগের একটি বিষয় হল—', opts: ['ইতিহাস', 'বুককিপিং', 'উদ্যান রচনা', 'রসায়নবিদ্যা'], ans: 1, exp: 'বাণিজ্য প্রবাহে বুককিপিং বা হিসাবরক্ষণ অন্তর্ভুক্ত ছিল।'},
      {q: 'ঐচ্ছিক পাঠ্যক্রমের চারুকলা বিভাগের একটি বিষয় হল—', opts: ['সংগীত', 'গার্হস্থ্য অর্থনীতি', 'ভূগোল', 'জীবনবিজ্ঞান'], ans: 0, exp: 'চারুকলার প্রবাহে সংগীত একটি আবশ্যিক বিষয় ছিল।'}
    ]
  },
  7: {
    name: 'Set 7',
    icon: '⭐',
    topic: 'মুদালিয়র কমিশনের সুপারিশ ও মূল্যায়ন',
    questions: [
      {q: 'ঐচ্ছিক পাঠ্যক্রমের মানবিক বিজ্ঞান বিভাগের একটি বিষয় হল—', opts: ['পদার্থবিদ্যা', 'রসায়নবিদ্যা', 'গণিত', 'বুককিপিং'], ans: 2, exp: 'মানবিক বিজ্ঞান প্রবাহে ইতিহাস, ভূগোল, অর্থনীতি, পৌরবিজ্ঞান ও গণিত অন্তর্ভুক্ত ছিল।'},
      {q: '1948 খ্রিস্টাব্দে মাধ্যমিক শিক্ষার পুনর্গঠনের জন্য একটি কমিটি গঠনের সুপারিশ করে—', opts: ['CABE', 'UGC', 'SABE', 'NCERT'], ans: 0, exp: 'CABE বা কেন্দ্রীয় শিক্ষা উপদেষ্টা পর্ষদ সর্বভারতীয় কমিশন গঠনের প্রস্তাব করেন।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশন শিক্ষার্থীদের কাজের মূল্যায়নের জন্য কত Point Scale-এর সুপারিশ করেছিলেন?', opts: ['Four Point Scale', 'Three Point Scale', 'Five Point Scale', 'Seven Point Scale'], ans: 2, exp: 'A, B, C, D, E — এই ৫টি সাংকেতিক চিহ্ন বা Five Point Scale ব্যবহারের কথা বলা হয়।'},
      {q: 'AICTE-এর সম্পূর্ণ নাম হল—', opts: ['All India Council of Teacher Education', 'All India Council for Technical Education', 'All Indian Council for Technical Education', 'All India Central for Technical Education'], ans: 1, exp: 'AICTE হলো ভারতের কারিগরি শিক্ষার সর্বোচ্চ সংস্থা।'},
      {q: 'CRC-এর সম্পূর্ণ নাম হল—', opts: ['Cumulative Record Card', 'Central Record Card', 'Cumulative Reading Card', 'Cumulative Record Curve'], ans: 0, exp: 'শিক্ষার্থীর সর্বাত্মক পরিচয় পত্র বা Cumulative Record Card প্রবর্তনের কথা বলা হয়।'},
      {q: 'মুদালিয়র কমিশন অপর যে নামে পরিচিত তা হল—', opts: ['ভারতীয় শিক্ষা কমিশন', 'মাধ্যমিক শিক্ষা কমিশন', 'বিশ্ববিদ্যালয় শিক্ষা কমিশন', 'প্রথম ভারতীয় শিক্ষা কমিশন'], ans: 1, exp: 'স্বাধীন ভারতের মাধ্যমিক শিক্ষাব্যবস্থা পুনর্গঠনের জন্য এটি মাধ্যমিক শিক্ষা কমিশন নামে পরিচিত।'},
      {q: 'মুদালিয়র কমিশনে ভারতীয় সদস্যসংখ্যা ছিল—', opts: ['৫ জন', '২ জন', '৭ জন', '৯ জন'], ans: 2, exp: 'সভাপতি ও সম্পাদক-সহ ৭ জন ভারতীয় এবং ২ জন বিদেশি শিক্ষাবিদ ছিলেন।'},
      {q: 'মাধ্যমিক শিক্ষা কমিশনে শিক্ষার্থীদের মূল্যায়নের ক্ষেত্রে নম্বর দানের পরিবর্তে কীসের সুপারিশ করা হয়?', opts: ['গ্রেড দান', 'বিভাগ দান', 'পুরস্কার প্রদান', 'কোনোটিই নয়'], ans: 0, exp: 'A, B, C, D, E গ্রেড ব্যবহারের সুপারিশ করা হয়েছিল।'},
      {q: 'কমিশনের মতে মাধ্যমিক বিদ্যালয়ে সাপ্তাহিক কাজের সময়সীমা হবে—', opts: ['৩৫ পিরিয়ড', '৪০ পিরিয়ড', '৪৫ পিরিয়ড', '৫০ পিরিয়ড'], ans: 2, exp: 'সপ্তাহে অন্তত ৪৫ পিরিয়ড ক্লাসের কথা বলা হয়েছিল।'},
      {q: 'কমিশনের মতে, মাধ্যমিক বিদ্যালয়ে কাজের সময়সীমা হবে অন্তত পক্ষে—', opts: ['১২০ দিন', '১১০ দিন', '২৩৫ দিন', '২০০ দিন'], ans: 3, exp: 'বছরে অন্ততপক্ষে ২০০ দিন কাজের সময়সীমা নির্ধারণ করতে হবে।'},
      {q: 'কমিশনের মতে, শিক্ষার্থীদের বিদ্যালয় জীবনের সমগ্র ঘটনাবলি লিপিবদ্ধ থাকবে—', opts: ['ARC-তে', 'CRC-তে', 'চূড়ান্ত ফলাফলে', 'শংসাপত্রে'], ans: 1, exp: 'CRC বা Cumulative Record Card-এ সকল তথ্য সংরক্ষণ করা হবে।'},
      {q: 'কমিশন কতজন সদস্য নিয়ে মাধ্যমিক শিক্ষা পর্ষদ গঠনের কথা বলেছিলেন?', opts: ['২০ জন', '২৫ জন', '৩০ জন', '১৮ জন'], ans: 1, exp: 'প্রতিটি রাজ্যে ২৫ জন সদস্যের একটি মাধ্যমিক শিক্ষা পর্ষদ থাকবে।'},
      {q: 'নীচের কোনটি মাধ্যমিক শিক্ষার লক্ষ্য?', opts: ['ধর্মনিরপেক্ষ মনোভাব গঠন', 'নিরক্ষরতা দূরীকরণ', 'কুসংস্কারমুক্ত সমাজ গঠন', 'সব ক-টি'], ans: 3, exp: 'ধর্মনিরপেক্ষতা, নিরক্ষরতা দূরীকরণ ও কুসংস্কারমুক্ত সমাজ গঠন — সবগুলোই মাধ্যমিক শিক্ষার লক্ষ্য।'},
      {q: 'মাধ্যমিক স্তরের ক্ষেত্রে একটি সাধারণ কী ধরনের পরীক্ষার ব্যবস্থা থাকবে?', opts: ['অভ্যন্তরীণ পরীক্ষা', 'মৌখিক পরীক্ষা', 'কম্পার্টমেন্টাল পরীক্ষা', 'বহিঃপরীক্ষা'], ans: 3, exp: 'মাধ্যমিক স্তরের শিক্ষা সমাপ্তির পর একটি সাধারণ বহিঃপরীক্ষা থাকবে।'},
      {q: 'সরকারি পরীক্ষায় কোন নতুন পরীক্ষার প্রবর্তনের কথা বলা হয়েছে?', opts: ['বহিঃপরীক্ষা', 'অভ্যন্তরীণ পরীক্ষা', 'কম্পার্টমেন্টাল পরীক্ষা', 'ব্যবহারিক পরীক্ষা'], ans: 2, exp: 'অনুত্তীর্ণ শিক্ষার্থীদের পুনরায় সুযোগ দেওয়ার জন্য কম্পার্টমেন্টাল পরীক্ষার প্রবর্তন করা হয়।'}
    ]
  },
  8: {
    name: 'Set 8',
    icon: '🏫',
    topic: 'মুদালিয়র কমিশনের অন্যান্য দিক ও কোঠারি কমিশনের সূচনা',
    questions: [
      {q: 'শিক্ষকদের ছেলেমেয়েরা বিদ্যালয়ে কোন্ সুযোগসুবিধা গ্রহণ করতে পারবে?', opts: ['ভরতির সুযোগ', 'হোস্টেলে থাকার সুযোগ', 'বিনা বেতনে শিক্ষাগ্রহণ', 'কোনোটিই নয়'], ans: 2, exp: 'শিক্ষকদের ছেলেমেয়েরা বিদ্যালয়ে বিনা বেতনে শিক্ষাগ্রহণের সুযোগ পাবে।'},
      {q: 'মাধ্যমিক উত্তীর্ণ শিক্ষকদের প্রশিক্ষণকাল কত হবে?', opts: ['এক বছর', 'দুই বছর', 'তিন বছর', 'চার বছর'], ans: 1, exp: 'মাধ্যমিক উত্তীর্ণ শিক্ষকদের প্রশিক্ষণের সময়কাল ২ বছর।'},
      {q: 'স্নাতক উত্তীর্ণ শিক্ষকদের প্রশিক্ষণকাল কত হবে?', opts: ['এক বছর', 'দুই বছর', 'তিন বছর', 'চার বছর'], ans: 0, exp: 'স্নাতক উত্তীর্ণ শিক্ষকদের প্রশিক্ষণের সময়কাল ১ বছর।'},
      {q: 'কোন্ কমিশনে শিল্পশিক্ষা কর প্রবর্তনের কথা বলা হয়েছে?', opts: ['রাধাকৃষ্ণণ কমিশনে', 'মুদালিয়র কমিশনে', 'কোঠারি কমিশনে', 'অশোক মিত্র কমিশনে'], ans: 1, exp: 'মুদালিয়র কমিশন শিল্পশিক্ষা কর প্রবর্তনের সুপারিশ করেছিলেন।'},
      {q: 'NCC-এর সম্পূর্ণ নাম কী?', opts: ['National Cadet Corps', 'Need Cadet Corps', 'Nation Cadet Corps', 'National Cadet Committee'], ans: 0, exp: 'শিক্ষার্থীদের চরিত্র গঠনে প্রতিটি বিদ্যালয়ে NCC চালু করার ওপর জোর দেওয়া হয়।'},
      {q: 'মুদালিয়র কমিশনের মতে, মাধ্যমিক শিক্ষার লক্ষ্য ও উদ্দেশ্য কোন্ দৃষ্টিভঙ্গিকে কেন্দ্র করে নির্ধারণ করতে হবে?', opts: ['আঞ্চলিক', 'রাজ্য', 'জাতীয়', 'বিদেশি'], ans: 2, exp: 'জাতীয় দৃষ্টিভঙ্গিকে কেন্দ্র করে লক্ষ্য নির্ধারণ করতে হবে।'},
      {q: 'মুদালিয়র কমিশনের মতে, নীচের কোনটি মাধ্যমিক শিক্ষার লক্ষ্য ও উদ্দেশ্য নির্ধারণের জাতীয় দৃষ্টিভঙ্গি?', opts: ['গণতান্ত্রিক', 'দারিদ্র্য দূরীকরণ', 'সাংস্কৃতিক পুনরুজ্জীবন', 'সব ক-টি'], ans: 3, exp: 'গণতান্ত্রিক সমাজব্যবস্থা, দারিদ্র্য দূরীকরণ এবং সাংস্কৃতিক পুনরুজ্জীবন — সবই জাতীয় দৃষ্টিভঙ্গি।'},
      {q: 'জাতীয় দৃষ্টিভঙ্গিকে ভিত্তি করে মাধ্যমিক শিক্ষার লক্ষ্য কোনটি?', opts: ['গণতান্ত্রিক নাগরিক গঠন', 'কর্মদক্ষতা বৃদ্ধি', 'সংস্কৃতির সংরক্ষণ ও বিকাশ সাধন', 'সব ক-টি'], ans: 3, exp: 'যোগ্য নাগরিক গঠন, কর্মদক্ষতা বৃদ্ধি ও সংস্কৃতির বিকাশ সবই লক্ষ্য।'},
      {q: 'মাধ্যমিক শিক্ষাব্যবস্থাকে সুপরিচালনার জন্য প্রতিটি রাজ্যে কী গঠন করার সুপারিশ করেছেন?', opts: ['মাধ্যমিক শিক্ষা পরিষদ গঠন', 'শিক্ষাসংস্থা গঠন', 'মাধ্যমিক বিদ্যালয় স্থাপন', 'কোনোটিই নয়'], ans: 0, exp: 'প্রতিটি রাজ্যে মাধ্যমিক শিক্ষা পর্ষদ বা পরিষদ গঠনের সুপারিশ করা হয়।'},
      {q: 'কোঠারি কমিশনের প্রকাশিত রিপোর্টের শিরোনাম হল—', opts: ['শিক্ষা এবং জাতীয় উন্নয়ন', 'শিক্ষা এবং জাতীয় বিকাশ', 'শিক্ষা এবং আন্তর্জাতিক বিকাশ', 'শিক্ষা এবং রাষ্ট্রের বিকাশ'], ans: 1, exp: 'Education and National Development — শিক্ষা ও জাতীয় অগ্রগতি শিরোনামে প্রকাশিত হয়।'},
      {q: 'কোঠারি কমিশনের মতে শিক্ষা কাঠামোটি হল—', opts: ['১০ + ১ + ২ + ৩', '১০ + ২ + ৩ + ২', '১০ + ২ + ৩ + ২', '৪ + ৪ + ২ + ২ + ৩ + ২'], ans: 1, exp: 'কোঠারি কমিশনের প্রস্তাবিত কাঠামো 10 + 2 + 3 + 2।'},
      {q: 'ভারতীয় শিক্ষা কমিশনের অপর নাম হল—', opts: ['মুদালিয়র কমিশন', 'রাধাকৃষ্ণণ কমিশন', 'কোঠারি কমিশন', 'হান্টার কমিশন'], ans: 2, exp: 'ড. ডি. এস. কোঠারির সভাপতিত্বে গঠিত হওয়ায় এটি কোঠারি কমিশন নামে পরিচিত।'},
      {q: 'কোঠারি কমিশন মোট কতজন সদস্য নিয়ে গঠিত?', opts: ['১৬ জন', '১৫ জন', '১৯ জন', '১৭ জন'], ans: 3, exp: 'ভারত সরকার ১৭ জন বিশিষ্ট শিক্ষাবিদ নিয়ে কমিশন গঠন করেন।'},
      {q: 'কোঠারি কমিশনের রিপোর্টটি প্রকাশিত হয়—', opts: ['১৯০৬ খ্রিস্টাব্দের মে মাসে', '১৯৬৬ খ্রিস্টাব্দের জুন মাসে', '১৯৬৪ খ্রিস্টাব্দের জুলাই মাসে', '১৯৬৭ খ্রিস্টাব্দের মে মাসে'], ans: 1, exp: '১৯৬৬ সালের ২৯ জুন কমিশন তাদের রিপোর্ট জমা দেন।'},
      {q: 'কোঠারি কমিশনে কতজন ভারতীয় সদস্য ছিল?', opts: ['১১ জন', '১২ জন', '১৩ জন', '১০ জন'], ans: 3, exp: '১৭ জন সদস্যের মধ্যে ১০ জন বিশিষ্ট ভারতীয় শিক্ষাবিদ ছিলেন।'}
    ]
  },
  9: {
    name: 'Set 9',
    icon: '📖',
    topic: 'কোঠারি কমিশনের প্রাথমিক স্তর ও উচ্চশিক্ষা',
    questions: [
      {q: 'কোঠারি কমিশনের সভাপতি হলেন—', opts: ['ড. জে. পি. নায়েক', 'ডি. এস. কোঠারি', 'ড. এ. লক্ষ্মণস্বামী মুদালিয়র', 'লর্ড কার্জন'], ans: 1, exp: 'বিশিষ্ট জ্যোতির্বিদ ড. দৌলত সিং কোঠারি ছিলেন কমিশনের সভাপতি।'},
      {q: 'কোঠারি কমিশনে বিদেশি সদস্য সংখ্যা হল—', opts: ['১০ জন', '১১ জন', '৫ জন', '৭ জন'], ans: 3, exp: 'ইউনেস্কো, ইংল্যান্ড, আমেরিকা, জাপান, রাশিয়া ও ফ্রান্সের ৭ জন বিদেশি সদস্য ছিলেন।'},
      {q: 'কোঠারি কমিশনে Working Group-এর সংখ্যা হল—', opts: ['৭টি', '৮টি', '৪টি', '১০টি'], ans: 0, exp: '১২টি Task Force এবং ৭টি Working Group নিয়ে কাজ করেছিল।'},
      {q: 'কোঠারি কমিশনের মতে প্রাথমিক শিক্ষার সময়কাল হল—', opts: ['৭/৮ বছর', '৫/৬ বছর', '৮ বছর', '৪/৫ বছর'], ans: 0, exp: 'প্রাথমিক শিক্ষার স্তরটি সাত বা আট বছরের হবে।'},
      {q: 'নিম্ন প্রাথমিক শিক্ষা হবে—', opts: ['প্রথম থেকে চতুর্থ বা পঞ্চম শ্রেণি', 'প্রথম থেকে চতুর্থ শ্রেণি', 'প্রথম থেকে ষষ্ঠ শ্রেণি', 'প্রথম থেকে অষ্টম শ্রেণি'], ans: 0, exp: 'চার বা পাঁচ বছরের শিক্ষাকাল নিম্ন প্রাথমিক স্তর।'},
      {q: 'নিম্ন প্রাথমিক শিক্ষার সর্বোচ্চ সময়কাল হল—', opts: ['৪/৫ বছর', '২ বছর', '৩/৪ বছর', '২/৩ বছর'], ans: 0, exp: 'শিক্ষার্থীদের বয়স ৬ থেকে ১০ বা ১১ বছর এবং শিক্ষাকাল ৪ বা ৫ বছর।'},
      {q: 'উচ্চ প্রাথমিক শিক্ষার সর্বোচ্চ শ্রেণি হল—', opts: ['সপ্তম', 'অষ্টম', 'সপ্তম/অষ্টম', 'কোনোটিই নয়'], ans: 2, exp: 'পঞ্চম বা ষষ্ঠ থেকে সর্বোচ্চ সপ্তম বা অষ্টম শ্রেণি পর্যন্ত।'},
      {q: 'উচ্চশিক্ষার কয়টি স্তর?', opts: ['২টি', '৩টি', '৪টি', '৫টি'], ans: 0, exp: 'উচ্চশিক্ষা প্রধানত দুটি স্তরে (স্নাতক ও স্নাতকোত্তর) ভাগ করা হয়েছে।'},
      {q: 'স্নাতকোত্তর স্তর হল—', opts: ['উচ্চশিক্ষার প্রথম স্তর', 'উচ্চশিক্ষার সর্বশেষ স্তর', 'উচ্চমাধ্যমিক স্তর', 'মাধ্যমিক স্তর'], ans: 1, exp: 'স্নাতকোত্তর স্তর হলো উচ্চশিক্ষার সর্বশেষ পর্যায়।'},
      {q: 'উচ্চশিক্ষার প্রথম স্তরের শিক্ষাকাল হল—', opts: ['৫ বছর', '৪ বছর', '২ বছর', '৩ বছর'], ans: 3, exp: 'স্নাতক স্তরের শিক্ষাকাল তিন বছর।'},
      {q: 'কোঠারি কমিশন কয়টি Task Force গঠন করেছিল?', opts: ['১২টি', '১৭টি', '৯টি', '১০টি'], ans: 0, exp: 'মোট ১২টি টাস্ক ফোর্স গঠন করেছিল।'},
      {q: 'কর্মের মাধ্যমে শিক্ষা হল—', opts: ['সাধারণ শিক্ষা', 'বৃত্তি ও কারিগরি শিক্ষা', 'কর্ম অভিজ্ঞতা', 'কোনোটিই নয়'], ans: 2, exp: 'কমিশন প্রত্যক্ষ কাজের মাধ্যমে অভিজ্ঞতা অর্জনকে কর্ম অভিজ্ঞতা বলেছেন।'},
      {q: 'বৃত্তিমুখী শিক্ষার একটি বৈশিষ্ট্য হল—', opts: ['স্থিতিশীল প্রক্রিয়া', 'সংগতিবিধানের প্রক্রিয়া', 'নির্বাচনধর্মিতা', 'সৌন্দর্যবোধ বিকাশের প্রক্রিয়া'], ans: 2, exp: 'শিক্ষার্থীরা নিজস্ব দক্ষতা অনুযায়ী বিষয় নির্বাচন করতে পারে।'},
      {q: 'কোঠারি কমিশনের মতে উচ্চশিক্ষার প্রথম স্তরে শিক্ষার মাধ্যম হবে—', opts: ['ইংরেজি ভাষা', 'আঞ্চলিক ভাষা', 'হিন্দি ভাষা', 'সংস্কৃত ভাষা'], ans: 1, exp: 'উচ্চশিক্ষার মাধ্যম হিসেবে আঞ্চলিক ভাষা ব্যবহারের সুপারিশ করা হয়েছে।'},
      {q: 'উচ্চশিক্ষার উচ্চমানের শিক্ষা ও গবেষণার জন্য প্রতিষ্ঠিত করতে হবে—', opts: ['প্রধান বিশ্ববিদ্যালয়', 'বিশ্ববিদ্যালয়', 'ডিপ্লোমা কোর্সের বিশ্ববিদ্যালয়', 'সাধারণ মানের বিশ্ববিদ্যালয়'], ans: 0, exp: 'Major Universities বা প্রধান বিশ্ববিদ্যালয় প্রতিষ্ঠা করতে হবে।'}
    ]
  },
  10: {
    name: 'Set 10',
    icon: '🗣️',
    topic: 'কোঠারি কমিশনের সংগঠন ও ভাষানীতি',
    questions: [
      {q: 'কোঠারি কমিশনের একজন ভারতীয় সদস্য হলেন—', opts: ['অধ্যাপক সুনভোষি', 'ড. বি. পি. পল', 'অধ্যাপক রোজার রেভেলি', 'ড. ডি. এস.'], ans: 1, exp: 'ড. বি. পি. পল ছিলেন ১০ জন ভারতীয় সদস্যের একজন।'},
      {q: 'কোঠারি কমিশনের একটি Task Force হল—', opts: ['বিজ্ঞান শিক্ষা এবং গবেষণা', 'প্রাক্-প্রাথমিক শিক্ষা', 'নারীশিক্ষা', 'মধ্যশিক্ষা পর্ষদ'], ans: 0, exp: 'বিজ্ঞান শিক্ষা এবং গবেষণা ছিল ১২টি টাস্ক ফোর্সের একটি।'},
      {q: 'কোঠারি কমিশনের একজন বিদেশি সদস্য হলেন—', opts: ['ড. টি. সেন', 'ড. পি. এন. কিরাপাল', 'ড. জে. পি. নায়েক', 'মিস্টার এম. জেন থমাস'], ans: 3, exp: 'ফ্রান্সের প্রতিনিধি মিস্টার এম. জেন থমাস ছিলেন বিদেশি সদস্য।'},
      {q: 'কোন কমিশন প্রতিটি রাজ্যে রাজ্য শিক্ষা পরিষদ গঠনের সুপারিশ করেছেন?', opts: ['রাধাকৃষ্ণণ কমিশন', 'মুদালিয়র কমিশন', 'হান্টার কমিশন', 'কোঠারি কমিশন'], ans: 3, exp: 'কোঠারি কমিশন রাজ্য শিক্ষা পরিষদ গঠনের সুপারিশ করেছিল।'},
      {q: 'স্কুল কমপ্লেক্স (বিদ্যালয়গুচ্ছ) গঠনের সুপারিশ করা হয়—', opts: ['মুদালিয়র কমিশনে', 'কোঠারি কমিশনে', 'জনার্দন রেডি কমিশনে', 'রাধাকৃষ্ণণ কমিশনে'], ans: 1, exp: 'কোঠারি কমিশন প্রথম বিদ্যালয়গুচ্ছ গঠনের সুপারিশ করেন।'},
      {q: 'কোঠারি কমিশনের মতে, বিদ্যালয়গুলির কাজের দিনসংখ্যা হবে—', opts: ['২১০ দিন', '২১৫ দিন', '২৩৪ দিন', '৩০৭ দিন'], ans: 2, exp: 'কমিশন কাজের দিনসংখ্যা ২৩৪ দিন করার সুপারিশ করেছিলেন।'},
      {q: 'কোঠারি কমিশনের সুপারিশে কমন স্কুলব্যবস্থার দ্বারা কোন বিষয়কে গুরুত্ব দেওয়া হয়েছে?', opts: ['শিক্ষায় সমসুযোগ', 'অপচয় ও অনুন্নয়ন', 'সমাজসেবা', 'জাতীয় উৎপাদন'], ans: 0, exp: 'সকলকে শিক্ষাক্ষেত্রে সমান সুযোগ প্রদান করাই কমন স্কুল ব্যবস্থার লক্ষ্য।'},
      {q: 'কোন শিক্ষার স্তরের ওপর অপচয় ও অনুন্নয়ন সর্বাধিক প্রভাব বিস্তার করে?', opts: ['উচ্চশিক্ষা', 'প্রাক্-প্রাথমিক শিক্ষা', 'প্রাথমিক শিক্ষা', 'মাধ্যমিক শিক্ষা'], ans: 2, exp: 'প্রাথমিক শিক্ষাস্তরে শিক্ষার্থীরা বিদ্যালয় ছেড়ে দেয়ায় অপচয় সর্বাধিক।'},
      {q: 'কোঠারি কমিশনে বহিঃপরীক্ষার উন্নয়নের জন্য সুপারিশ হল—', opts: ['প্রশ্নের সংখ্যা বৃদ্ধি', 'রচনাধর্মী প্রশ্নের ওপর গুরুত্ব', 'প্রশ্নের মানের পরিবর্তন ও বিজ্ঞানভিত্তিক নম্বর দেওয়া', 'পরীক্ষকের সংখ্যা বৃদ্ধি'], ans: 2, exp: 'নম্বর দেওয়ার পদ্ধতিকে বিজ্ঞানভিত্তিক করার সুপারিশ করা হয়।'},
      {q: 'কোঠারি কমিশনের মতে, প্রাক্-প্রাথমিক শিক্ষার প্রধান উদ্দেশ্য হল—', opts: ['নেতৃত্ব দান', 'সু-অভ্যাস গঠন করা', 'বিজ্ঞান শিক্ষা', 'সৃজনশীলতার বিকাশ'], ans: 1, exp: 'শৈশবকালে সু-অভ্যাস গঠন করাই প্রাক্-প্রাথমিক শিক্ষার প্রধান উদ্দেশ্য।'},
      {q: 'কোঠারি কমিশনের মতে, প্রাথমিক শিক্ষাস্তরে ভরতির ন্যূনতম বয়স হবে—', opts: ['৪ বছর', '৬+ বছর', '৭+ বছর', '১০+ বছর'], ans: 1, exp: '৬ বছর বয়স থেকে শিশুদের প্রাথমিক শিক্ষাস্তরে ভরতি হওয়ার কথা বলা হয়েছে।'},
      {q: 'কোঠারি কমিশনের ভিত্তিতে কোন্ জাতীয় শিক্ষানীতি রচিত হয়?', opts: ['১৯৬৮ খ্রিস্টাব্দের জাতীয় শিক্ষানীতি', '১৯৭৮ খ্রিস্টাব্দের জাতীয় শিক্ষানীতি', '১৯৮৬ খ্রিস্টাব্দের জাতীয় শিক্ষানীতি', 'কোনোটিই নয়'], ans: 0, exp: 'কোঠারি কমিশনের সুপারিশের ভিত্তিতে ১৯৬৮ সালে প্রথম জাতীয় শিক্ষানীতি রচিত হয়।'},
      {q: 'কোঠারি কমিশনের মূল রিপোর্ট ছিল—', opts: ['৬৯২ পৃষ্ঠার', '৭৪৭ পৃষ্ঠার', '৪৮৯ পৃষ্ঠার', '৫৪২ পৃষ্ঠার'], ans: 2, exp: '৬৯২ পৃষ্ঠার রিপোর্টের মধ্যে মূল রিপোর্টটি ছিল ৪৮৯ পৃষ্ঠার।'},
      {q: 'কোঠারি কমিশন, তাঁদের রিপোর্টটি জমা দেন—', opts: ['Union Education Minister-এর নিকট', 'United Education Minister-এর নিকট', 'Union Educational Minister-এর নিকট', 'Universal Education Minister-এর নিকট'], ans: 0, exp: '১৯৬৬ সালের ২৯ জুন তৎকালীন শিক্ষামন্ত্রীর কাছে রিপোর্ট জমা দেওয়া হয়।'},
      {q: 'কোঠারি কমিশন কত খ্রিস্টাব্দে কাজ শুরু করে?', opts: ['১৯৬৬ খ্রিস্টাব্দের ২৯ জুন', '১৯৬৪ খ্রিস্টাব্দের ২ অক্টোবর', '১৯৬৫ খ্রিস্টাব্দের ২ অক্টোবর', '১৯৬৪ খ্রিস্টাব্দের ২৯ জুন'], ans: 1, exp: '১৯৬৪ সালের ২ অক্টোবর থেকে আনুষ্ঠানিকভাবে কাজ শুরু করে।'}
    ]
  },
  11: {
    name: 'Set 11',
    icon: '🌐',
    topic: 'কোঠারি কমিশনের ভাষা, কারিগরি ও বিদ্যালয়গুচ্ছ',
    questions: [
      {q: 'অধ্যাপক সদতোশি কোন দেশের লোক ছিলেন?', opts: ['ইংল্যান্ড', 'রাশিয়া', 'ফ্রান্স', 'জাপান'], ans: 3, exp: 'অধ্যাপক সদতোশি ইহারা ছিলেন জাপানের শিক্ষাবিদ।'},
      {q: 'কোঠারি কমিশন কোন শ্রেণি থেকে ইংরেজি ভাষাশিক্ষা শুরু করার কথা বলেছেন?', opts: ['প্রথম শ্রেণি', 'দ্বিতীয় শ্রেণি', 'পঞ্চম শ্রেণি', 'চতুর্থ শ্রেণি'], ans: 2, exp: 'পঞ্চম শ্রেণি থেকে ইংরেজি শেখার কথা বলা হয়েছে।'},
      {q: 'কোঠারি কমিশনে বৃত্তিমুখী শিক্ষা কোন্ স্তর থেকে শুরু করার কথা বলা হয়েছে?', opts: ['প্রাক প্রাথমিক', 'প্রাথমিক', 'নিম্ন মাধ্যমিক', 'উচ্চমাধ্যমিক'], ans: 2, exp: 'নিম্ন মাধ্যমিক স্তর (অষ্টম/নবম শ্রেণি) থেকে বৃত্তিমুখী শিক্ষা দেওয়ার সুপারিশ করা হয়েছে।'},
      {q: 'কারিগরি শিক্ষার সঙ্গে কোন্ ধরনের শিক্ষার গভীর সম্পর্ক বিশেষভাবে লক্ষ করা যায়?', opts: ['সাহিত্য', 'গার্হস্থ্য বিজ্ঞান', 'বাণিজ্য', 'বিজ্ঞান শিক্ষা'], ans: 3, exp: 'বিজ্ঞান এবং কারিগরি শিক্ষা একে অপরের পরিপূরক।'},
      {q: 'কারিগরি শিক্ষার সঙ্গে সম্পর্কিত একটি সংস্থা হল—', opts: ['NCERT', 'NCTE', 'UGC', 'AICTE'], ans: 3, exp: 'AICTE হলো ভারতের কারিগরি শিক্ষার সর্বোচ্চ সংস্থা।'},
      {q: 'ভারতীয় শিক্ষা কমিশন গঠিত হয়—', opts: ['১৯৬৪ খ্রিস্টাব্দে', '১৯৬৬ খ্রিস্টাব্দে', '১৯৪৮ খ্রিস্টাব্দে', '১৯৫২ খ্রিস্টাব্দে'], ans: 0, exp: '১৯৬৪ সালের ১৪ জুলাই ভারতীয় শিক্ষা কমিশন গঠিত হয়।'},
      {q: 'বিদ্যালয় স্তরে পাঠ্যক্রম রচনা করে—', opts: ['NCERT', 'NCTE', 'CABE', 'UGC'], ans: 0, exp: 'NCERT বিদ্যালয় স্তরের পাঠ্যক্রম রচনা করে।'},
      {q: 'কোঠারি কমিশনের মতে, নিম্ন প্রাথমিক স্তরে কয়টি ভাষা শিক্ষার কথা বলা হয়েছে?', opts: ['একটি ভাষা', 'দুটি ভাষা', 'তিনটি ভাষা', 'সব ক-টি'], ans: 0, exp: 'নিম্ন প্রাথমিক স্তরে শুধু একটি ভাষা (মাতৃভাষা) শেখার কথা বলা হয়েছে।'},
      {q: 'উচ্চ প্রাথমিক স্তরে কয়টি ভাষা শিক্ষার কথা বলা হয়েছে?', opts: ['একটি ভাষা', 'দুটি ভাষা', 'তিনটি ভাষা', 'সব ক-টি'], ans: 1, exp: 'উচ্চ প্রাথমিক স্তরে দুটি ভাষা আবশ্যিক করা হয়েছে।'},
      {q: 'নিম্ন মাধ্যমিক স্তরে কয়টি ভাষা শিক্ষার কথা বলা হয়েছে?', opts: ['একটি ভাষা', 'দুটি ভাষা', 'তিনটি ভাষা', 'সব ক-টি'], ans: 2, exp: 'নিম্ন মাধ্যমিক স্তরে ত্রিভাষা সূত্র প্রয়োগ হয়।'},
      {q: 'উচ্চমাধ্যমিক স্তরে কয়টি ভাষা শিক্ষার কথা বলা হয়েছে?', opts: ['একটি ভাষা', 'দুটি ভাষা', 'তিনটি ভাষা', 'সব ক-টি'], ans: 1, exp: 'উচ্চমাধ্যমিক স্তরে দুটি ভাষা বাধ্যতামূলক।'},
      {q: 'বিদ্যালয় শিক্ষার গুণগত মান উন্নয়নের জন্য কী গড়ে তোলার কথা বলা হয়েছে?', opts: ['বিদ্যালয় সংগঠন', 'বিদ্যালয় সংস্থা', 'বিদ্যালয়গুচ্ছ', 'বিদ্যালয় পাঠ্যক্রম'], ans: 2, exp: 'শিক্ষার মান উন্নয়নে বিদ্যালয়গুচ্ছ বা School Complex গঠনের কথা বলা হয়েছে।'},
      {q: 'প্রথম পর্যায়ে কতগুলি বিদ্যালয় নিয়ে বিদ্যালয়গুচ্ছ গঠনের কথা বলা হয়েছে?', opts: ['৮-১৫টি', '৮-১০টি', '১০-১৪টি', '১৫-২০টি'], ans: 1, exp: 'প্রথম পর্যায়ে ৮ থেকে ১০টি বিদ্যালয় নিয়ে গুচ্ছ গঠনের কথা বলা হয়েছে।'},
      {q: 'প্রথম পর্যায়ে বিদ্যালয়গুচ্ছের কেন্দ্রে কোন্ বিদ্যালয় থাকবে?', opts: ['নিম্ন প্রাথমিক বিদ্যালয়', 'উচ্চ প্রাথমিক বিদ্যালয়', 'মাধ্যমিক বিদ্যালয়', 'উচ্চমাধ্যমিক বিদ্যালয়'], ans: 1, exp: 'প্রথম পর্যায়ের কেন্দ্রে একটি উচ্চ প্রাথমিক বিদ্যালয় থাকবে।'},
      {q: 'দ্বিতীয় পর্যায়ে বিদ্যালয়গুচ্ছ কতগুলি বিদ্যালয় নিয়ে গঠিত হবে?', opts: ['১৫-২০টি', '১০-১৫টি', '১৮-২৫', '১০-৩০টি'], ans: 0, exp: 'দ্বিতীয় পর্যায়ে ১৫ থেকে ২০টি বিদ্যালয় নিয়ে গুচ্ছ গঠিত হবে।'}
    ]
  },
  12: {
    name: 'Set 12',
    icon: '👩‍🏫',
    topic: 'কোঠারি কমিশনের শিক্ষক শিক্ষণ, বয়স্ক শিক্ষা ও নারীশিক্ষা',
    questions: [
      {q: 'দ্বিতীয় পর্যায়ে বিদ্যালয়গুচ্ছের কেন্দ্রে কোন বিদ্যালয় থাকবে?', opts: ['উচ্চমাধ্যমিক বিদ্যালয়', 'নিম্ন প্রাথমিক বিদ্যালয়', 'একটি মাধ্যমিক বিদ্যালয়', 'উচ্চমাধ্যমিক বিদ্যালয়'], ans: 2, exp: 'দ্বিতীয় পর্যায়ের কেন্দ্রে একটি মাধ্যমিক বিদ্যালয় থাকবে।'},
      {q: 'প্রতিবেশী বিদ্যালয় প্রথা গঠনের কথা কোন্ কমিশনে বলা হয়েছে?', opts: ['মুদালিয়র কমিশন', 'রাধাকৃষ্ণণ কমিশন', 'কোঠারি কমিশন', 'অশোক মিত্র কমিশন'], ans: 2, exp: 'কোঠারি কমিশন প্রতিবেশী বিদ্যালয় প্রথা গঠনের কথা বলেছেন।'},
      {q: 'প্রতিবেশী বিদ্যালয় প্রথার উদ্দেশ্য কী?', opts: ['অনুদান প্রদান', 'সকল শিশুকে বিদ্যালয়ে ভরতি', 'সকলের শিক্ষায় অধিকার প্রদান', 'আঞ্চলিক শিক্ষায় গুরুত্ব দান'], ans: 2, exp: 'সকলের শিক্ষায় সমান অধিকার নিশ্চিত করাই এর উদ্দেশ্য।'},
      {q: 'SBTE-এর সম্পূর্ণ নাম কী?', opts: ['State Board of Teacher Education', 'State Board of Teacher Educo', 'State Board of Talent Education', 'কোনোটিই নয়'], ans: 0, exp: 'রাজ্য স্তরে State Board of Teacher Education প্রতিষ্ঠার কথা বলা হয়েছে।'},
      {q: 'শিক্ষক শিক্ষণ ব্যবস্থা তদারকি করার জন্য প্রতিটি রাজ্যে কী গঠন করার কথা বলা হয়েছে?', opts: ['শিক্ষক শিক্ষণ সংস্থা', 'রাজ্য শিক্ষক শিক্ষণ পর্ষদ', 'রাজ্য শিক্ষক শিক্ষণ কমিটি', 'রাজ্য শিক্ষক সংগঠন'], ans: 1, exp: 'রাজ্য শিক্ষক শিক্ষণ পর্ষদ গঠনের প্রস্তাব দেওয়া হয়।'},
      {q: 'কর্মরত শিক্ষকদের জ্ঞানের নবীকরণের জন্য কত বছর অন্তর প্রশিক্ষণের ব্যবস্থা করতে হবে?', opts: ['তিন বছর', 'চার বছর', 'পাঁচ বছর', 'দশ বছর'], ans: 2, exp: 'প্রতি ৫ বছর অন্তর প্রশিক্ষণের ব্যবস্থা করতে হবে।'},
      {q: 'বয়স্ক নারীদের সাক্ষর করে তোলার জন্য কাদের নিয়োগ করতে হবে?', opts: ['গ্রামের শিক্ষক', 'গ্রামের ভগিনী', 'গ্রামের মানুষ', 'কোনোটিই নয়'], ans: 1, exp: 'গ্রামের ভগিনী (Village Sister) নিয়োগের কথা বলা হয়েছে।'},
      {q: 'কোঠারি কমিশন নিরক্ষরতা দূরীকরণের জন্য কোন্ কোন্ পদ্ধতির উল্লেখ করেছেন?', opts: ['নির্বাচনমূলক ও ব্যাপক পদ্ধতি', 'নির্বাচনমূলক ও অনুকরণমূলক পদ্ধতি', 'ব্যাপক ও সংকীর্ণ পদ্ধতি', 'ব্যাপক ও পর্যবেক্ষণ পদ্ধতি'], ans: 0, exp: 'নির্বাচনমূলক ও ব্যাপক পদ্ধতি — এই দুটি পদ্ধতির উল্লেখ করা হয়েছে।'},
      {q: 'বয়স্ক ব্যক্তিদের পাঠে আগ্রহ সৃষ্টি করতে গ্রন্থাগার বিষয়ক উপদেষ্টা কমিটি সারা দেশে কী তৈরির সুপারিশ করেন?', opts: ['Library', 'Home Library', 'Library Net Work', 'কোনোটিই নয়'], ans: 2, exp: 'সারা দেশে Library Network তৈরির সুপারিশ করা হয়।'},
      {q: 'NBAE-এর সম্পূর্ণ নাম কী?', opts: ['National Body of Adult Education', 'National Board of Adult Education', 'National Board of Area Education', 'National Board of Adult of Educo'], ans: 1, exp: 'বয়স্ক শিক্ষার জন্য National Board of Adult Education (NBAE) গঠনের কথা বলা হয়েছে।'},
      {q: 'SAT-এর সম্পূর্ণ নাম কী?', opts: ['State Achievement Test', 'Standardized Achievement Test', 'Standard Achievement Test', 'Standardized Achievement Text'], ans: 1, exp: 'Standardized Achievement Test — আদর্শায়িত পারদর্শিতার অভীক্ষা।'},
      {q: 'প্রাথমিক বিদ্যালয়গুলিতে শিক্ষা শেষে বিভিন্ন জেলায় কীসের মাধ্যমে শিক্ষার্থীদের মূল্যায়নের কথা বলা হয়েছে?', opts: ['আদর্শায়িত পারদর্শিতার অভীক্ষা', 'পারদর্শিতার অভীক্ষা', 'বার্ষিক পরীক্ষা', 'ক্রমিক মূল্যায়ন'], ans: 0, exp: 'SAT বা আদর্শায়িত পারদর্শিতার অভীক্ষার মাধ্যমে মূল্যায়ন করা হবে।'},
      {q: 'মাধ্যমিক ও উচ্চমাধ্যমিক স্তরে কোন্ ধরনের পরীক্ষার ব্যবস্থার কথা কোঠারি কমিশনে বলা হয়?', opts: ['অভ্যন্তরীণ পরীক্ষা', 'বহিঃপরীক্ষা', 'বার্ষিক পরীক্ষা', 'অর্ধবার্ষিক পরীক্ষা'], ans: 1, exp: 'মাধ্যমিক ও উচ্চমাধ্যমিক স্তরে বহিঃপরীক্ষা বা বোর্ড পরীক্ষার ব্যবস্থা করার কথা বলা হয়েছে।'},
      {q: 'কোঠারি কমিশনের সুপারিশ অনুযায়ী কতগুলি বিদ্যালয়ের জন্য একজন পরিদর্শক-পরামর্শদাতা নিয়োগ করতে হবে?', opts: ['৫টি', '৭টি', '৯টি', '১০টি'], ans: 3, exp: 'প্রতি ১০টি বিদ্যালয়ের জন্য একজন পরিদর্শক-পরামর্শদাতা নিয়োগের কথা বলা হয়েছে।'},
      {q: 'নারীশিক্ষার প্রসারের জন্য কোঠারি কমিশন কী গঠনের সুপারিশ করেছেন?', opts: ['The National Committee on the Education of Women', 'The National Common on the Education of Women', 'The National Commenly on the Education of Women', 'The National committee on the Educational of Woman'], ans: 0, exp: 'নারীশিক্ষার উন্নয়নে বিশেষ কমিটি গঠনের ওপর গুরুত্ব দেওয়া হয়েছে।'}
    ]
  }
};

// ============================================================
//  গ্লোবাল ভেরিয়েবল
// ============================================================
const LABELS = ['ক', 'খ', 'গ', 'ঘ'];
let currentSetId = 1;
let cur = 0, score = 0, wrong = 0, answered = false, timerInterval, timeLeft = 10 * 60;
let userAnswers = [];
let isLoggedIn = false;
let currentUser = null;
let pendingSetId = null; // সেট সিলেক্ট করলে লগইন আসবে, লগইন হলে এই সেট শুরু হবে

// ============================================================
//  হাব পেজ বিল্ড
// ============================================================
function buildHub() {
  const grid = document.getElementById('setGrid');
  grid.innerHTML = '';
  for (let i = 1; i <= TOTAL_SETS; i++) {
    const set = allSets[i];
    const card = document.createElement('div');
    card.className = 'set-card';
    card.innerHTML = `
      <div class="icon">${set.icon}</div>
      <div class="set-num">${set.name}</div>
      <div class="set-title">${set.topic}</div>
      <div class="set-meta"><span>১৫ প্রশ্ন</span><span>১০ মিনিট</span></div>
    `;
    card.onclick = () => selectSet(i);
    grid.appendChild(card);
  }
}

function showHub() {
  document.getElementById('hubPage').classList.remove('hidden');
  document.getElementById('testArea').classList.add('hidden');
  document.getElementById('resultWrap').classList.remove('show');
  document.getElementById('timerBox').classList.remove('danger');
  clearInterval(timerInterval);
  if (currentUser) {
    document.getElementById('hubUserInfo').innerHTML = `👤 ${currentUser.username} — Test দিতে সেট সিলেক্ট করো।`;
  } else {
    document.getElementById('hubUserInfo').innerHTML = '';
  }
}

function goToHub() {
  document.getElementById('testArea').classList.add('hidden');
  document.getElementById('resultWrap').classList.remove('show');
  document.getElementById('hubPage').classList.remove('hidden');
  document.getElementById('timerBox').classList.remove('danger');
  clearInterval(timerInterval);
}

// ============================================================
//  সেট সিলেক্ট - লগইন চেক
// ============================================================
function selectSet(id) {
  currentSetId = id;
  const set = allSets[id];
  
  // যদি ইতিমধ্যে লগইন করা থাকে
  if (isLoggedIn && currentUser) {
    const setAttempts = currentUser.attempts[id] || 0;
    if (setAttempts >= MAX_ATTEMPTS) {
      alert(`⚠️ আপনি এই অ্যাকাউন্ট দিয়ে ${set.name} এর সর্বোচ্চ ${MAX_ATTEMPTS} বার Test দিয়েছেন। আর Test দেওয়া সম্ভব নয়।`);
      return;
    }
    startQuiz(id);
    return;
  }
  
  // লগইন না থাকলে লগইন মোডাল দেখাও
  pendingSetId = id;
  document.getElementById('loginSetName').textContent = `📚 ${set.name} — ${set.topic}`;
  document.getElementById('loginOverlay').classList.add('active');
  document.getElementById('loginUsername').value = '';
  document.getElementById('loginPassword').value = '';
  document.getElementById('loginError').style.display = 'none';
  document.getElementById('limitInfo').style.display = 'none';
  document.getElementById('loginBtn').disabled = false;
  document.getElementById('loginUsername').focus();
}

// ============================================================
//  লগইন ফাংশন (সেট সিলেক্টের পর)
// ============================================================
function doLoginFromSet() {
  const username = document.getElementById('loginUsername').value.trim();
  const password = document.getElementById('loginPassword').value.trim();
  const errorEl = document.getElementById('loginError');
  const limitInfo = document.getElementById('limitInfo');
  const loginBtn = document.getElementById('loginBtn');

  if (!username || !password) {
    errorEl.textContent = '❌ দয়া করে ইউজারনেম ও পাসওয়ার্ড দিন।';
    errorEl.style.display = 'block';
    return;
  }

  const user = userData.find(u => u.username === username && u.password === password);
  if (user) {
    const setAttempts = user.attempts[currentSetId] || 0;
    if (setAttempts >= MAX_ATTEMPTS) {
      limitInfo.style.display = 'block';
      document.getElementById('limitMsg').textContent = `আপনি এই অ্যাকাউন্ট দিয়ে ${allSets[currentSetId].name} এর সর্বোচ্চ ${MAX_ATTEMPTS} বার Test দিয়েছেন। আর Test দেওয়া সম্ভব নয়।`;
      errorEl.style.display = 'none';
      loginBtn.disabled = true;
      return;
    }
    
    isLoggedIn = true;
    currentUser = user;
    errorEl.style.display = 'none';
    limitInfo.style.display = 'none';
    loginBtn.disabled = false;
    document.getElementById('loginOverlay').classList.remove('active');
    
    // হাব আপডেট
    document.getElementById('hubUserInfo').innerHTML = `👤 ${currentUser.username} — Test দিতে সেট সিলেক্ট করো।`;
    
    // সেট শুরু করো
    startQuiz(currentSetId);
  } else {
    errorEl.textContent = '❌ ভুল ইউজারনেম বা পাসওয়ার্ড। আবার চেষ্টা করুন।';
    errorEl.style.display = 'block';
    limitInfo.style.display = 'none';
  }
}

// Enter key support for login
document.addEventListener('DOMContentLoaded', function() {
  document.getElementById('loginPassword').addEventListener('keydown', function(e) {
    if (e.key === 'Enter') doLoginFromSet();
  });
  document.getElementById('loginUsername').addEventListener('keydown', function(e) {
    if (e.key === 'Enter') doLoginFromSet();
  });
  buildHub();
  document.getElementById('hubPage').classList.remove('hidden');
  document.getElementById('testArea').classList.add('hidden');
  document.getElementById('resultWrap').classList.remove('show');
});

// ============================================================
//  কুইজ ফাংশন
// ============================================================
function startQuiz(setId) {
  if (!isLoggedIn || !currentUser) return;
  
  const setAttempts = currentUser.attempts[setId] || 0;
  if (setAttempts >= MAX_ATTEMPTS) {
    alert(`⚠️ আপনি এই সেটের সর্বোচ্চ ${MAX_ATTEMPTS} বার Test দিয়েছেন।`);
    return;
  }
  
  currentUser.attempts[setId] = (currentUser.attempts[setId] || 0) + 1;
  
  cur = 0; score = 0; wrong = 0; answered = false;
  timeLeft = 10 * 60; userAnswers = [];
  document.getElementById('hubPage').classList.add('hidden');
  document.getElementById('resultWrap').classList.remove('show');
  document.getElementById('testArea').classList.remove('hidden');
  document.getElementById('timerBox').classList.remove('danger');
  
  const set = allSets[setId];
  document.getElementById('testSetLabel').textContent = set.name;
  document.getElementById('testSetName').textContent = 'শিক্ষাবিজ্ঞান';
  document.getElementById('testTopic').textContent = set.topic;
  
  clearInterval(timerInterval);
  timerInterval = setInterval(tick, 1000);
  loadQ();
}

function tick() {
  timeLeft--;
  const m = Math.floor(timeLeft / 60);
  const s = timeLeft % 60;
  document.getElementById('timerDisplay').textContent = m + ':' + (s < 10 ? '0' : '') + s;
  if (timeLeft <= 60) document.getElementById('timerBox').classList.add('danger');
  if (timeLeft <= 0) { clearInterval(timerInterval); showResult(); }
}

function loadQ() {
  answered = false;
  const set = allSets[currentSetId];
  const q = set.questions[cur];
  document.getElementById('qNum').textContent = 'প্রশ্ন ' + (cur + 1) + ' / ' + set.questions.length;
  document.getElementById('qText').textContent = q.q;
  document.getElementById('progressFill').style.width = ((cur + 1) / set.questions.length * 100) + '%';
  document.getElementById('nextBtn').disabled = true;
  document.getElementById('nextBtn').textContent = cur === set.questions.length - 1 ? 'ফলাফল দেখো' : 'পরবর্তী →';
  document.getElementById('explanation').classList.remove('show');

  const opts = document.getElementById('qOpts');
  opts.innerHTML = '';
  q.opts.forEach((o, i) => {
    const btn = document.createElement('button');
    btn.className = 'opt';
    btn.innerHTML = '<div class="opt-circle">' + LABELS[i] + '</div><div class="opt-text">' + o + '</div>';
    btn.onclick = () => answer(i);
    opts.appendChild(btn);
  });
}

function answer(i) {
  if (answered) return;
  answered = true;
  const set = allSets[currentSetId];
  const q = set.questions[cur];
  userAnswers[cur] = i;
  const btns = document.querySelectorAll('.opt');
  btns.forEach(b => b.classList.add('disabled'));
  btns[q.ans].classList.add('correct');
  if (i !== q.ans) { btns[i].classList.add('wrong'); wrong++; }
  else score++;
  document.getElementById('scoreShow').textContent = 'সঠিক: ' + score + ' | ভুল: ' + wrong;
  document.getElementById('explanationText').innerHTML = '<strong>ব্যাখ্যা:</strong> ' + q.exp;
  document.getElementById('explanation').classList.add('show');
  document.getElementById('nextBtn').disabled = false;
}

function nextQ() {
  const set = allSets[currentSetId];
  cur++;
  if (cur >= set.questions.length) { clearInterval(timerInterval); showResult(); return; }
  loadQ();
}

function showResult() {
  document.getElementById('testArea').classList.add('hidden');
  const rw = document.getElementById('resultWrap');
  rw.classList.add('show');
  const set = allSets[currentSetId];
  const pct = Math.round(score / set.questions.length * 100);
  document.getElementById('finalScore').textContent = score;
  document.getElementById('rbCorrect').textContent = score;
  document.getElementById('rbWrong').textContent = wrong;
  document.getElementById('rbPct').textContent = pct + '%';
  
  const remaining = MAX_ATTEMPTS - (currentUser.attempts[currentSetId] || 0);
  document.getElementById('attemptInfo').innerHTML = `👤 ${currentUser.username} — ${set.name}: বাকি আছে <strong>${remaining}</strong> বার Test দেওয়ার সুযোগ (সর্বোচ্চ ${MAX_ATTEMPTS} বার)`;
  
  const grades = [
    [90, '🌟', 'অসাধারণ!'],
    [70, '👍', 'খুব ভালো!'],
    [50, '📚', 'ভালো চেষ্টা!'],
    [0, '💪', 'চেষ্টা চালিয়ে যাও!']
  ];
  const g = grades.find(x => pct >= x[0]);
  document.getElementById('resultIcon').textContent = g[1];
  document.getElementById('resultGrade').textContent = g[2] + ' (' + set.topic + ')';
}

function showReview() {
  document.getElementById('resultWrap').classList.remove('show');
  document.getElementById('testArea').classList.remove('hidden');
  cur = 0;
  loadReview();
}

function loadReview() {
  const set = allSets[currentSetId];
  if (cur >= set.questions.length) { 
    document.getElementById('testArea').classList.add('hidden'); 
    document.getElementById('resultWrap').classList.add('show'); 
    return; 
  }
  const q = set.questions[cur];
  document.getElementById('qNum').textContent = 'Review — প্রশ্ন ' + (cur + 1) + ' / ' + set.questions.length;
  document.getElementById('qText').textContent = q.q;
  document.getElementById('progressFill').style.width = ((cur + 1) / set.questions.length * 100) + '%';
  document.getElementById('nextBtn').disabled = false;
  document.getElementById('nextBtn').textContent = cur === set.questions.length - 1 ? 'শেষ করো' : 'পরবর্তী →';
  document.getElementById('nextBtn').onclick = () => { cur++; loadReview(); };

  const opts = document.getElementById('qOpts');
  opts.innerHTML = '';
  q.opts.forEach((o, i) => {
    const btn = document.createElement('button');
    btn.className = 'opt disabled';
    if (i === q.ans) btn.classList.add('correct');
    else if (userAnswers[cur] === i) btn.classList.add('wrong');
    btn.innerHTML = '<div class="opt-circle">' + LABELS[i] + '</div><div class="opt-text">' + o + '</div>';
    opts.appendChild(btn);
  });

  document.getElementById('explanationText').innerHTML = '<strong>ব্যাখ্যা:</strong> ' + q.exp;
  document.getElementById('explanation').classList.add('show');
  document.getElementById('scoreShow').textContent = 'সবুজ = সঠিক উত্তর';
}
</script>

</body>
</html>
