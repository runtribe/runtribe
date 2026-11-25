<!DOCTYPE html><html lang="en"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1"><title>RUNTRIBE – Member Panel</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
<style>
:root{--g:#39ff14;--c:#0e0e0e;--m:#888;--r:#ff4d4d}
*{box-sizing:border-box}body{margin:0;background:#000;color:#eee;font:15px system-ui,sans-serif}
header{display:flex;justify-content:space-between;align-items:center;padding:14px 20px;border-bottom:1px solid #1d1d1d}
.logo{font-weight:900;font-size:24px;letter-spacing:3px}.logo b{color:var(--g);text-shadow:0 0 12px var(--g)}
main{max-width:720px;margin:auto;padding:20px}
.card{background:var(--c);border:1px solid #1f1f1f;border-radius:16px;padding:20px;margin-bottom:16px;animation:f .4s}
@keyframes f{from{opacity:0;transform:translateY(8px)}}
input,select,textarea{width:100%;padding:11px;margin:4px 0 12px;background:#111;border:1px solid #2a2a2a;border-radius:10px;color:#fff;font:inherit}
input:focus,select:focus,textarea:focus{outline:0;border-color:var(--g)}
label{font-size:12px;color:var(--m)}
button,a.btn{display:inline-block;background:var(--g);color:#000;border:0;padding:11px 18px;border-radius:10px;font-weight:700;cursor:pointer;text-decoration:none;font-size:15px}
button.o{background:none;color:var(--g);border:1px solid var(--g)}button:disabled{opacity:.4;cursor:not-allowed}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:0 12px}@media(max-width:560px){.grid{grid-template-columns:1fr}}
.badge{padding:3px 10px;border-radius:20px;font-size:12px;font-weight:700;border:1px solid}
.PENDING{color:#ffc400}.APPROVED,.ACTIVE{color:var(--g)}.REJECTED,.SUSPENDED{color:var(--r)}
#toast{position:fixed;bottom:20px;left:50%;transform:translateX(-50%);background:#111;border:1px solid var(--g);padding:12px 20px;border-radius:10px;display:none;z-index:9;max-width:90%}
.hide{display:none!important}.av{width:84px;height:84px;border-radius:50%;object-fit:cover;border:2px solid var(--g)}
.row{display:flex;justify-content:space-between;padding:8px 0;border-bottom:1px solid #1a1a1a;gap:10px}.row span:first-child{color:var(--m)}
#qr{background:#fff;padding:12px;border-radius:12px;display:inline-block}progress{width:100%}
</style></head><body>
<header><div class="logo">RUN<b>TRIBE</b></div><button class="o hide" id="lo">Logout</button></header>
<main>
<div id="ann" class="card hide"></div>
<div id="vAuth" class="hide"><div class="card"><h2>Welcome to the Tribe 🏃</h2>
<div style="display:flex;gap:8px;margin-bottom:14px"><button id="tL">Login</button><button class="o" id="tR">Register</button></div>
<form id="fL"><label>Email</label><input id="le" type="email" required><label>Password</label><input id="lp" type="password" required>
<button id="lb">Login</button> <button type="button" class="o" id="fp">Forgot password?</button></form>
<form id="fR" class="hide"><div id="closed" class="hide" style="color:var(--r);margin-bottom:10px">Registration is currently closed.</div>
<div class="grid"><div><label>Full Name</label><input id="n" required></div><div><label>Date of Birth</label><input id="dob" type="date" required></div>
<div><label>Email</label><input id="em" type="email" required></div><div><label>Phone Number</label><input id="ph" inputmode="numeric" maxlength="10" required></div>
<div><label>Emergency Phone</label><input id="eph" inputmode="numeric" maxlength="10" required></div>
<div><label>Gender</label><select id="gn" required><option value="">Select</option><option>Male</option><option>Female</option><option>Other</option></select></div>
<div><label>Place / City</label><input id="ct" required></div><div><label>PIN Code</label><input id="pin" inputmode="numeric" maxlength="6" required></div></div>
<label>Full Address</label><textarea id="ad" rows="2" required></textarea>
<label>Profile Photo (optional – JPG/PNG/WEBP, max 5 MB)</label><input id="pf" type="file" accept="image/jpeg,image/png,image/webp">
<div class="grid"><div><label>Password</label><input id="pw" type="password" minlength="6" required></div><div><label>Confirm Password</label><input id="pw2" type="password" required></div></div>
<button id="rb">Register &amp; Continue to Payment</button></form></div></div>

<div id="vNone" class="hide card"><h3>No registration found</h3><p>This account has no registration record. Please contact the club admin.</p></div>

<div id="vPay" class="hide"><div class="card" style="text-align:center"><h2>Membership Payment</h2><h1 id="fee" style="color:var(--g);margin:6px"></h1>
<div id="qr"></div><p>UPI ID: <b id="upi"></b></p>
<button class="o" id="cp">Copy UPI ID</button> <a class="btn" id="pn" href="#">Pay Now</a>
<ol style="text-align:left;color:var(--m)"><li>Scan the QR (or tap Pay Now) and pay the exact amount.</li><li>Take a screenshot of the successful payment.</li><li>Upload it below. Admin will verify manually.</li></ol><p id="ins" style="color:var(--m)"></p></div>
<div class="card"><h3>Upload Payment Screenshot</h3><label>Screenshot (JPG/PNG/WEBP, max 5 MB)</label><input id="sf" type="file" accept="image/jpeg,image/png,image/webp">
<img id="pv" class="hide" style="max-width:100%;max-height:300px;border-radius:10px;margin-bottom:10px"><label>UTR / Transaction ID (optional)</label><input id="utr">
<progress id="pg" value="0" max="100" class="hide"></progress><br><button id="up">Upload Screenshot</button></div></div>

<div id="vDash" class="hide"></div>
</main><div id="toast"></div>
<script type="module">
import {initializeApp} from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";
import {getAuth,createUserWithEmailAndPassword as cu,signInWithEmailAndPassword as si,onAuthStateChanged as oa,signOut,sendPasswordResetEmail as rp} from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";
import {getDatabase,ref,set,onValue} from "https://www.gstatic.com/firebasejs/10.12.2/firebase-database.js";
import {getStorage,ref as sr,uploadBytes,uploadBytesResumable,getDownloadURL} from "https://www.gstatic.com/firebasejs/10.12.2/firebase-storage.js";
const firebaseConfig={apiKey:"AIzaSyBqy7-zU55iUPGuW_j2D_ExxckZFvHte64",authDomain:"hanuman-mandir-a4520.firebaseapp.com",databaseURL:"https://hanuman-mandir-a4520-default-rtdb.firebaseio.com",projectId:"hanuman-mandir-a4520",storageBucket:"hanuman-mandir-a4520.firebasestorage.app",messagingSenderId:"420324145072",appId:"1:420324145072:web:6464fc0d554472024ac875",measurementId:"G-56TL9FRKMQ"};
const app=initializeApp(firebaseConfig),auth=getAuth(app),db=getDatabase(app),st=getStorage(app);
const $=i=>document.getElementById(i),esc=s=>String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const toast=(m,e)=>{const t=$('toast');t.textContent=m;t.style.borderColor=e?'#ff4d4d':'#39ff14';t.style.display='block';clearTimeout(t.h);t.h=setTimeout(()=>t.style.display='none',4500)};
const ERR={'auth/email-already-in-use':'This email is already registered. Please login.','auth/invalid-credential':'Wrong email or password.','auth/weak-password':'Password is too weak.','auth/invalid-email':'Invalid email address.','auth/too-many-requests':'Too many attempts. Try later.','PERMISSION_DENIED':'Permission denied.'};
const em=e=>ERR[e.code]||ERR[e.message]||e.message;
const show=v=>['vAuth','vNone','vPay','vDash'].forEach(x=>$(x).classList.toggle('hide',x!==v));
const dt=t=>t?new Date(t).toLocaleString():'-';
const OK=/^image\/(jpeg|png|webp)$/;
const DEF={fee:21,upi:'8011035684@ybl',wa:'https://chat.whatsapp.com/Hq6XN8gDlxC9cOpY0gAvfs',regOpen:true,announcement:'',instructions:''};
let S=DEF,U,R,P,V,busy=false,repay=false,un=[],ld={};
onValue(ref(db,'clubSettings'),s=>{S={...DEF,...(s.val()||{})};render()});
oa(auth,u=>{un.forEach(f=>f());un=[];U=u;R=P=V=null;ld={};repay=false;$('lo').classList.toggle('hide',!u);
 if(u)['registrations','paymentProofs','reviewStatus'].forEach(p=>un.push(onValue(ref(db,p+'/'+u.uid),s=>{const v=s.val();if(p[0]=='r'&&p[1]=='e'&&p[2]=='g')R=v;else if(p[0]=='p')P=v;else V=v;ld[p]=1;render()},e=>toast(em(e),1))));
 render()});
function render(){
 $('ann').classList.toggle('hide',!S.announcement);$('ann').textContent='📢 '+S.announcement;
 $('closed').classList.toggle('hide',!!S.regOpen);
 if(busy)return;if(!U)return show('vAuth');
 if(!(ld.registrations&&ld.paymentProofs&&ld.reviewStatus))return;
 if(!R)return show('vNone');
 if(!P||repay)return pay();dash()}
function pay(){show('vPay');const f=Number(S.fee).toFixed(2),l=`upi://pay?pa=${S.upi}&pn=RUNTRIBE&am=${f}&cu=INR&tn=RUNTRIBE%20Registration`;
 $('fee').textContent='₹'+f;$('upi').textContent=S.upi;$('pn').href=l;$('ins').textContent=S.instructions||'';
 if($('qr').dataset.l!==l){$('qr').dataset.l=l;$('qr').innerHTML='';new QRCode($('qr'),{text:l,width:220,height:220})}}
function dash(){show('vDash');const ps=V?.paymentStatus||'PENDING',ms=V?.membershipStatus||'INACTIVE',ok=ps=='APPROVED'&&ms=='ACTIVE';
 const r=(k,v)=>`<div class="row"><span>${k}</span><span>${v}</span></div>`;
 $('vDash').innerHTML=`<div class="card" style="display:flex;gap:16px;align-items:center">${R.photoURL?`<img class="av" src="${esc(R.photoURL)}">`:`<div class="av" style="display:flex;align-items:center;justify-content:center;font-size:34px;font-weight:900;color:var(--g)">${esc((R.name||'?')[0].toUpperCase())}</div>`}<div><h2 style="margin:0">${esc(R.name)}</h2><div style="color:var(--m)">${esc(R.regId)}</div></div></div>
<div class="card"><h3>Membership</h3>${r('Payment status',`<span class="badge ${ps}">${ps}</span>`)}${r('Membership status',`<span class="badge ${ms}">${ms}</span>`)}${r('Amount',P.amount?'₹'+Number(P.amount).toFixed(2):'-')}${r('Registered',dt(R.createdAt))}${V?.memberId?r('Member ID',esc(V.memberId)):''}${V?.approvedAt?r('Approved on',dt(V.approvedAt)):''}
${ps=='REJECTED'?`<p style="color:var(--r)">❌ Payment rejected. Reason: ${esc(V.rejectionReason||'Not specified')}</p><button id="re">Upload new screenshot</button>`:''}
${ps=='PENDING'?'<p style="color:#ffc400">⏳ Your payment is awaiting admin verification.</p>':''}
${ok?'<p style="color:var(--g)">✅ Membership confirmed. Welcome to RUNTRIBE!</p>':''}${ms=='SUSPENDED'?'<p style="color:var(--r)">Your membership is suspended. Contact admin.</p>':''}
${ok?`<a class="btn" target="_blank" rel="noopener" href="${esc(S.wa)}">JOIN RUNTRIBE WHATSAPP GROUP</a>`:'<button disabled>JOIN RUNTRIBE WHATSAPP GROUP</button><p style="color:var(--m);font-size:13px">Activates after admin approval.</p>'}</div>
<div class="card"><h3>Profile</h3>${r('Email',esc(R.email))}${r('Date of birth',esc(R.dob))}${r('Phone',esc(R.phone))}${r('Emergency',esc(R.emergency))}${r('Gender',esc(R.gender))}${r('City',esc(R.city))}${r('PIN',esc(R.pin))}${r('Address',esc(R.address))}</div>
<div class="card"><h3>Payment Screenshot</h3><a href="${esc(P.url)}" target="_blank" rel="noopener"><img src="${esc(P.url)}" style="max-width:100%;max-height:320px;border-radius:10px"></a>${P.utr?`<p>UTR: ${esc(P.utr)}</p>`:''}</div>`;
 if($('re'))$('re').onclick=()=>{repay=true;render()}}
$('tL').onclick=()=>{$('fL').classList.remove('hide');$('fR').classList.add('hide')};
$('tR').onclick=()=>{$('fR').classList.remove('hide');$('fL').classList.add('hide')};
$('fL').onsubmit=async e=>{e.preventDefault();$('lb').disabled=true;try{await si(auth,$('le').value.trim(),$('lp').value)}catch(x){toast(em(x),1)}$('lb').disabled=false};
$('fp').onclick=async()=>{const m=$('le').value.trim();if(!m)return toast('Enter your email first',1);try{await rp(auth,m);toast('Password reset email sent')}catch(x){toast(em(x),1)}};
$('lo').onclick=()=>signOut(auth);
$('fR').onsubmit=async e=>{e.preventDefault();
 if(!S.regOpen)return toast('Registration is currently closed',1);
 const v=i=>$(i).value.trim(),f=$('pf').files[0];
 if(!/^\d{10}$/.test(v('ph'))||!/^\d{10}$/.test(v('eph')))return toast('Enter valid 10-digit phone numbers',1);
 if(!/^\d{6}$/.test(v('pin')))return toast('PIN code must be 6 digits',1);
 if(f&&(!OK.test(f.type)||f.size>5242880))return toast('Profile photo must be JPG/PNG/WEBP up to 5 MB (or leave it empty)',1);
 if($('pw').value.length<6||$('pw').value!==$('pw2').value)return toast('Passwords must match (min 6 characters)',1);
 busy=true;const b=$('rb');b.disabled=true;b.textContent='Registering...';let c;
 try{c=await cu(auth,v('em'),$('pw').value);const uid=c.user.uid;let photoURL='',photoPath='';
  if(f){const r=sr(st,`profiles/${uid}/photo`);await uploadBytes(r,f,{contentType:f.type});photoURL=await getDownloadURL(r);photoPath=`profiles/${uid}/photo`}
  await set(ref(db,'registrations/'+uid),{name:v('n'),dob:$('dob').value,email:v('em').toLowerCase(),phone:v('ph'),emergency:v('eph'),gender:$('gn').value,city:v('ct'),pin:v('pin'),address:v('ad'),photoURL,photoPath,regId:'RT-'+Date.now().toString(36).toUpperCase()+Math.random().toString(36).slice(2,5).toUpperCase(),createdAt:Date.now()});
  toast('Registered! Please complete the payment.');
 }catch(x){toast(em(x),1);if(c)await c.user.delete().catch(()=>{})}
 busy=false;b.disabled=false;b.textContent='Register & Continue to Payment';render()};
$('cp').onclick=()=>navigator.clipboard.writeText(S.upi).then(()=>toast('UPI ID copied'),()=>toast('Copy failed',1));
$('sf').onchange=()=>{const f=$('sf').files[0];if(f){$('pv').src=URL.createObjectURL(f);$('pv').classList.remove('hide')}};
$('up').onclick=async()=>{const f=$('sf').files[0];
 if(!f||!OK.test(f.type))return toast('Select a JPG, PNG or WEBP screenshot',1);
 if(f.size>5242880)return toast('Max size is 5 MB',1);
 const b=$('up');b.disabled=true;$('pg').classList.remove('hide');
 try{const path=`payments/${U.uid}/proof`,r=sr(st,path),t=uploadBytesResumable(r,f,{contentType:f.type});
  await new Promise((ok,no)=>t.on('state_changed',s=>$('pg').value=100*s.bytesTransferred/s.totalBytes,no,ok));
  const url=await getDownloadURL(r);
  await set(ref(db,'paymentProofs/'+U.uid),{url,path,utr:$('utr').value.trim(),amount:Number(S.fee),uploadedAt:Date.now()});
  await set(ref(db,'reviewStatus/'+U.uid),{paymentStatus:'PENDING',membershipStatus:'INACTIVE'});
  repay=false;toast('Uploaded! Awaiting admin verification.');
 }catch(x){toast(em(x),1)}
 b.disabled=false;$('pg').classList.add('hide');render()};
</script></body></html>
