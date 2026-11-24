<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Kuis Skala Prioritas - Najiha</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:"Segoe UI",Arial,sans-serif;color:#4a2040;min-height:100vh;
background:radial-gradient(circle at 12px 12px,#ffd6e7 3px,transparent 4px) 0 0/34px 34px,linear-gradient(160deg,#fff7c2,#ffe3ef 55%,#fff3b0);background-attachment:fixed}
.wrap{max-width:640px;margin:0 auto;padding:16px;position:relative;z-index:1}
.fl{position:fixed;font-size:30px;opacity:.55;z-index:0;animation:fl 7s ease-in-out infinite;pointer-events:none}
@keyframes fl{50%{transform:translateY(-22px) rotate(12deg)}}
.card{background:#fffdf5;border:3px solid #ffb6d1;border-radius:26px;padding:22px;box-shadow:0 8px 0 #ffe27a,0 14px 26px rgba(244,114,182,.3);margin-bottom:22px;position:relative}
.banner{margin:-22px -22px 14px;padding:18px 20px 14px;border-radius:22px 22px 60px 60px/22px 22px 26px 26px;background:linear-gradient(120deg,#ffe27a,#ffb6d1 70%,#ff9ec4);text-align:center;border-bottom:3px dashed #fff}
h1{margin:0;color:#be185d;font-size:28px;text-shadow:2px 2px 0 #fff3a8}
h3{color:#db2777}
.sub{display:inline-block;background:#fff;color:#c2410c;font-weight:800;padding:3px 14px;border-radius:20px;margin-top:6px;border:2px solid #ffe27a}
.by{font-size:14px;color:#9d4a78;margin-top:8px}
.hero{font-size:72px;text-align:center;animation:bob 2s infinite;filter:drop-shadow(0 4px 0 #fff)}
@keyframes bob{50%{transform:translateY(-8px) rotate(-4deg)}}
.mat{background:#fff0f6;border-left:6px solid #ff8fb8;border-radius:14px;padding:6px 14px}
ol.tp{padding-left:0;list-style:none;counter-reset:n}
ol.tp li{counter-increment:n;background:#fff6c9;border-radius:14px;padding:10px 12px 10px 48px;margin:8px 0;position:relative}
ol.tp li::before{content:counter(n);position:absolute;left:10px;top:50%;transform:translateY(-50%);width:28px;height:28px;border-radius:50%;background:#ff7eb3;color:#fff;font-weight:800;text-align:center;line-height:28px}
button{font:inherit;cursor:pointer;border:0;border-radius:16px}
.btn{background:linear-gradient(120deg,#ff7eb3,#ff9a8b);color:#fff;padding:14px 22px;font-weight:800;width:100%;font-size:17px;box-shadow:0 5px 0 #e0558f;transition:.15s;margin-top:8px}
.btn:hover{transform:translateY(-2px) scale(1.02)}
.btn:active{transform:translateY(4px);box-shadow:0 1px 0 #e0558f}
.btn:disabled{background:#e5d4dc;box-shadow:0 5px 0 #cbb7c1;cursor:not-allowed;transform:none}
.opt{display:block;width:100%;text-align:left;padding:13px 15px;margin:10px 0;border:3px solid transparent;font-size:16px;color:#4a2040;transition:.15s;box-shadow:0 3px 0 rgba(0,0,0,.08)}
.opt:nth-child(1){background:#fff3a8}.opt:nth-child(2){background:#ffd6e7}.opt:nth-child(3){background:#ffe9b8}.opt:nth-child(4){background:#ffc9dd}
.opt:hover{transform:translateX(6px)}
.opt.sel{border-color:#db2777;font-weight:800;transform:scale(1.03);box-shadow:0 0 0 4px #fff,0 0 0 7px #ffb6d1}
.bar{height:16px;background:#fff;border:2px solid #ffb6d1;border-radius:12px;overflow:hidden}
.bar i{display:block;height:100%;width:0;background:repeating-linear-gradient(45deg,#ff7eb3 0 12px,#ffe27a 12px 24px);transition:.4s}
.top{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px;font-weight:800;color:#be185d}
.mute{background:#fff;padding:6px 12px;font-size:18px;border:2px solid #ffb6d1}
.pic{font-size:64px;text-align:center;margin:0 auto 8px;width:120px;height:120px;line-height:120px;border-radius:50%;background:radial-gradient(circle,#fff,#ffe9a8);border:4px dashed #ff9ec4;animation:pop .4s}
@keyframes pop{from{transform:scale(.4) rotate(-20deg);opacity:0}}
.score{font-size:70px;font-weight:900;text-align:center;color:#db2777;margin:0;text-shadow:3px 3px 0 #ffe27a}
.msg{text-align:center;font-size:18px;margin:4px 0 12px}
.rev{border-left:8px solid;padding:10px 12px;border-radius:14px;margin:12px 0;background:#fff;font-size:15px}
.rev.ok{border-color:#4ade80;background:#f2fff6}.rev.no{border-color:#fb7185;background:#fff1f4}
.tag{font-weight:800}.ok .tag{color:#16a34a}.no .tag{color:#e11d48}
.hide{display:none}
.conf{position:fixed;top:-20px;font-size:26px;animation:fall 3s linear forwards;pointer-events:none;z-index:9}
@keyframes fall{to{transform:translateY(110vh) rotate(360deg)}}
.fld{width:100%;padding:12px 14px;margin:6px 0;border:3px solid #ffb6d1;border-radius:14px;font:inherit;background:#fff;color:#4a2040}
.fld:focus{outline:none;border-color:#db2777;box-shadow:0 0 0 4px #ffe27a}
.err{color:#e11d48;font-weight:700;min-height:22px;margin:4px 0}
</style>
</head>
<body>
<span class="fl" style="left:4vw;top:12vh;animation-delay:0s">🌸</span><span class="fl" style="left:88vw;top:8vh;animation-delay:1s">⭐</span><span class="fl" style="left:92vw;top:45vh;animation-delay:2s">🪙</span><span class="fl" style="left:3vw;top:55vh;animation-delay:3s">💛</span><span class="fl" style="left:85vw;top:80vh;animation-delay:4s">🎀</span><span class="fl" style="left:8vw;top:86vh;animation-delay:5s">✨</span><span class="fl" style="left:50vw;top:3vh;animation-delay:2s">🌼</span>
<div class="wrap">

<div id="start" class="card">
 <div class="banner"><div class="hero">⚖️💰</div>
 <h1>Kuis Skala Prioritas</h1>
 <div class="sub">Ekonomi SMA/MA/SMK</div>
 <div class="by">Oleh <b>Najiha</b> &middot; NIM 06031182429020</div></div>
 <h3>📖 Materi Singkat</h3>
 <p class="mat"><b>Skala prioritas</b> adalah daftar kebutuhan yang disusun dari yang paling penting dan mendesak hingga kurang penting, karena sumber daya terbatas. Kebutuhan dibagi menjadi <b>primer</b> (pangan, sandang, papan), <b>sekunder</b> (kendaraan, buku, perangkat belajar), dan <b>tersier</b> (barang mewah). Dasar penyusunan: urgensi, manfaat, dampak jika tidak dipenuhi, dan kemampuan keuangan.</p>
 <h3>🎯 Tujuan Pembelajaran</h3>
 <ol class="tp">
  <li>Peserta didik dapat menjelaskan pengertian kebutuhan dan skala prioritas.</li>
  <li>Peserta didik dapat membedakan kebutuhan primer, sekunder, dan tersier.</li>
  <li>Peserta didik dapat menyusun skala prioritas berdasarkan kasus nyata.</li>
 </ol>
 <div id="form"><h3>🧑‍🎓 Isi Data Dulu Ya</h3>
 <input class="fld" id="nama" placeholder="Nama lengkap" maxlength="50" autocomplete="off">
 <input class="fld" id="kelas" placeholder="Kelas (contoh: XI IPS 2)" maxlength="20" autocomplete="off">
 <div class="err" id="err"></div>
 <button class="btn" onclick="begin()">🚀 Mulai Kuis (10 Soal)</button></div>
 <div id="done" class="mat hide"></div>
</div>

<div id="quiz" class="hide">
 <div class="top"><span id="no">Soal 1/10</span><button class="mute" id="mute" onclick="toggleMute()">🔊</button></div>
 <div class="bar"><i id="prog"></i></div>
 <div class="card" style="margin-top:12px">
  <div class="pic" id="pic"></div>
  <h3 id="q"></h3>
  <div id="opts"></div>
  <button class="btn" id="next" onclick="next()" disabled>Lanjut ➡️</button>
 </div>
</div>

<div id="result" class="hide">
 <div class="card">
  <div class="pic" id="rpic"></div>
  <p class="score" id="score"></p>
  <p class="msg" id="msg"></p>
  <p class="msg">✅ Benar: <b id="cb"></b> &nbsp; ❌ Salah: <b id="cs"></b></p>
  <p class="msg" id="who"></p><p class="msg" id="sent"></p><button class="btn" onclick="startQuiz()">🔄 Ulangi Kuis</button>
 </div>
 <div class="card"><h3>📝 Jawaban &amp; Pembahasan</h3><div id="review"></div></div>
 <div class="by" style="text-align:center">Dibuat oleh Najiha &middot; NIM 06031182429020</div>
</div>

</div>
<script>
const Q=[
{p:"📋",q:"Daftar kebutuhan yang disusun dari yang paling penting sampai kurang penting disebut...",o:["Daftar belanja","Skala prioritas","Anggaran","Skala harga"],a:1,e:"Skala prioritas adalah urutan kebutuhan berdasarkan tingkat kepentingan dan urgensinya."},
{p:"💸",q:"Mengapa skala prioritas diperlukan?",o:["Karena uang tidak terbatas","Karena semua kebutuhan sama penting","Karena sumber daya terbatas sedangkan kebutuhan manusia tidak terbatas","Agar bisa berbelanja boros"],a:2,e:"Sumber daya terbatas membuat kita harus memilih kebutuhan yang paling penting lebih dulu."},
{p:"🍚👕🏠",q:"Beras, pakaian, dan tempat tinggal termasuk kebutuhan...",o:["Tersier","Sekunder","Primer","Mewah"],a:2,e:"Pangan, sandang, dan papan adalah kebutuhan pokok (primer) yang wajib dipenuhi."},
{p:"💻",q:"Laptop untuk belajar daring bagi pelajar umumnya termasuk kebutuhan...",o:["Primer","Sekunder","Tersier","Tidak diperlukan"],a:1,e:"Laptop menunjang aktivitas belajar tetapi tidak vital bagi kelangsungan hidup, jadi sekunder."},
{p:"🏎️",q:"Membeli mobil sport mewah padahal belum punya rumah termasuk kebutuhan...",o:["Primer","Sekunder","Tersier","Mendesak"],a:2,e:"Barang mewah dan bersifat kemewahan termasuk kebutuhan tersier."},
{p:"🚨",q:"Kebutuhan yang harus segera dipenuhi karena dampaknya besar jika ditunda disebut kebutuhan...",o:["Tidak mendesak","Mendesak","Tersier","Kolektif"],a:1,e:"Kebutuhan mendesak adalah kebutuhan yang tidak boleh ditunda pemenuhannya."},
{p:"🏥🎓",q:"Asuransi kesehatan dan tabungan pendidikan termasuk kebutuhan berdasarkan waktu...",o:["Sekarang","Masa depan","Rohani","Kolektif"],a:1,e:"Kebutuhan masa depan dipenuhi untuk mengantisipasi kebutuhan yang akan datang."},
{p:"🍱🚌",q:"Uang saku Rina Rp50.000. Pilihan dengan skala prioritas paling tepat adalah...",o:["Membeli skin game","Membeli aksesori","Membeli makan siang dan ongkos pulang","Membeli tiket konser"],a:2,e:"Makan siang dan transportasi pulang adalah kebutuhan primer dan mendesak, sehingga didahulukan."},
{p:"🔢",q:"Urutkan dari prioritas tertinggi: (1) tiket konser, (2) makan, (3) buku pelajaran, (4) mobil sport.",o:["1-2-3-4","4-3-2-1","2-3-1-4","3-4-1-2"],a:2,e:"Makan (primer) lalu buku pelajaran (sekunder), kemudian hiburan konser, dan terakhir mobil sport (tersier)."},
{p:"🤔",q:"Faktor yang TIDAK perlu dipertimbangkan saat menyusun skala prioritas adalah...",o:["Tingkat urgensi","Kemampuan keuangan","Manfaat","Ikut-ikutan tren teman"],a:3,e:"Ikut-ikutan tren menghasilkan keputusan konsumtif, bukan berdasarkan kebutuhan nyata."}
];
const SHEET_URL="";/* tempel link Apps Script di sini */
let me={},lastScore0=0;
const KEY="kuisNajiha";
function saved(){try{return JSON.parse(localStorage.getItem(KEY))}catch(e){return null}}
function lock(v){$("form").classList.add("hide");$("done").classList.remove("hide");$("done").innerHTML="🔒 <b>Kamu sudah mengerjakan kuis ini.</b><br>👤 "+esc(v.n)+" — "+esc(v.k)+"<br>🏅 Skor: <b>"+v.skor+"</b> (benar "+v.benar+", salah "+(10-v.benar)+")<br><small>Kuis hanya bisa diisi 1 kali.</small>"}
function esc(t){return String(t).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]))}
async function begin(){const n=$("nama").value.trim(),k=$("kelas").value.trim();
 if(!n||!k){$("err").textContent="Isi nama dan kelas dulu ya 🌸";return}
 me={n,k};
 $("err").textContent="";startQuiz()}
function save(sc,c){const rec={n:me.n,k:me.k,skor:sc,benar:c};
 $("who").textContent="👤 "+me.n+" — "+me.k;
 if(SHEET_URL){$("sent").textContent="⏳ Mengirim skor...";
  fetch(SHEET_URL+"?action=submit&nama="+encodeURIComponent(me.n)+"&kelas="+encodeURIComponent(me.k)+"&skor="+sc+"&benar="+c)
  .then(()=>$("sent").textContent="✅ Skor sudah tersimpan untuk guru").catch(()=>$("sent").textContent="⚠️ Skor gagal terkirim, cek internet")}}
let i=0,ans=[],muted=false,ctx;
const $=id=>document.getElementById(id);
function getCtx(){ctx=ctx||new(window.AudioContext||window.webkitAudioContext)();if(ctx.state==="suspended")ctx.resume();return ctx}
function beep(f,d,t="sine",delay=0,v=.15){if(muted)return;try{getCtx();const o=ctx.createOscillator(),g=ctx.createGain();o.type=t;o.frequency.value=f;g.gain.value=v;o.connect(g);g.connect(ctx.destination);const s=ctx.currentTime+delay;o.start(s);g.gain.exponentialRampToValueAtTime(.001,s+d);o.stop(s+d)}catch(e){}}
let mus=null,st=0;
const MEL=[523,659,784,659,880,784,659,587,523,659,784,1047,880,784,659,587,698,880,1047,880,784,659,587,659,523,0,659,0,784,0,523,0];
const BAS=[262,262,349,349,262,262,196,196];
function tick(){if(muted)return;beepM(MEL[st%32],BAS,st);st++}
function beepM(f,B,n){if(f)beep(f,.24,"triangle",0,.07);if(n%4==0)beep(B[(n/4)%8],.9,"sine",0,.09)}
function startMusic(){stopMusic();if(muted)return;try{getCtx()}catch(e){return}st=0;tick();mus=setInterval(tick,240)}
function stopMusic(){clearInterval(mus);mus=null}
let lastScore=0;
const RM={
 s:{m:[523,659,784,1047,784,1047,1319,1047,880,1047,1175,1319,1568,1319,1047,784],b:[262,349,392,262],d:.2,w:"triangle",t:200},
 a:{m:[523,587,659,784,659,784,880,784,698,784,880,1047,880,784,659,523],b:[262,349,262,196],d:.24,w:"triangle",t:260},
 b:{m:[392,440,523,440,392,349,392,0,330,392,440,392,349,330,294,0],b:[196,175,196,147],d:.3,w:"sine",t:340},
 c:{m:[440,0,392,0,349,0,330,0,349,0,330,0,294,0,262,0],b:[220,175,196,220],d:.4,w:"sine",t:460}};
function resultMusic(sc){stopMusic();if(muted)return;try{getCtx()}catch(e){return}
 const T=sc>=90?RM.s:sc>=70?RM.a:sc>=50?RM.b:RM.c;let n=0;
 const p=()=>{if(muted)return;const f=T.m[n%16];if(f)beep(f,T.d,T.w,0,.08);if(n%4==0)beep(T.b[(n/4|0)%4],T.t*3/1000,"sine",0,.09);n++};
 p();mus=setInterval(p,T.t)}
function toggleMute(){muted=!muted;$("mute").textContent=muted?"🔇":"🔊";if(muted)stopMusic();else if(!$("quiz").classList.contains("hide"))startMusic();else if(!$("result").classList.contains("hide"))resultMusic(lastScore)}
function show(id){["start","quiz","result"].forEach(x=>$(x).classList.toggle("hide",x!==id))}
function startQuiz(){i=0;ans=[];beep(523,.15,"triangle");beep(659,.15,"triangle",.12);beep(784,.25,"triangle",.24);show("quiz");render();startMusic();window.scrollTo(0,0)}
function render(){const d=Q[i];$("no").textContent="Soal "+(i+1)+"/"+Q.length;$("prog").style.width=(i/Q.length*100)+"%";$("pic").textContent=d.p;$("q").textContent=(i+1)+". "+d.q;
$("opts").innerHTML=d.o.map((t,k)=>`<button class="opt" onclick="pick(${k})">${"ABCD"[k]}. ${t}</button>`).join("");
$("next").disabled=true;$("next").textContent=i==Q.length-1?"🏁 Selesai & Lihat Skor":"Lanjut ➡️"}
function pick(k){ans[i]=k;document.querySelectorAll(".opt").forEach((b,x)=>b.classList.toggle("sel",x==k));$("next").disabled=false;beep(440,.08,"square")}
function next(){beep(600,.08);if(i<Q.length-1){i++;render()}else finish()}
function confetti(){["🎉","⭐","🪙","✨","🎊"].forEach((e,n)=>{for(let j=0;j<5;j++){const s=document.createElement("span");s.className="conf";s.textContent=e;s.style.left=Math.random()*95+"vw";s.style.animationDelay=Math.random()*1.2+"s";document.body.appendChild(s);setTimeout(()=>s.remove(),4500)}})}
function finish(){stopMusic();$("prog").style.width="100%";let c=0;
$("review").innerHTML=Q.map((d,n)=>{const ok=ans[n]===d.a;if(ok)c++;return `<div class="rev ${ok?"ok":"no"}"><b>${n+1}. ${d.q}</b><br><span class="tag">${ok?"✅ Benar":"❌ Salah"}</span><br>Jawaban kamu: ${"ABCD"[ans[n]]}. ${d.o[ans[n]]}<br>${ok?"":`Jawaban benar: <b>${"ABCD"[d.a]}. ${d.o[d.a]}</b><br>`}💡 <i>${d.e}</i></div>`}).join("");
const sc=c*10;$("score").textContent=sc;$("cb").textContent=c;$("cs").textContent=Q.length-c;
const g=sc>=90?["🏆","Luar biasa! Kamu ahli skala prioritas!"]:sc>=70?["🌟","Bagus sekali! Sedikit lagi sempurna."]:sc>=50?["👍","Cukup baik, pelajari lagi pembahasannya ya."]:["📚","Ayo semangat, baca materi lalu coba lagi!"];
$("rpic").textContent=g[0];$("msg").textContent=g[1];show("result");window.scrollTo(0,0);
if(sc>=70)confetti();lastScore=sc;save(sc,c);resultMusic(sc)}
</script>
</body>
</html>
