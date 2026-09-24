<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SMKarya</title>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

body{
  font-family:Arial,sans-serif;
  background:#fff7fc;
  color:#333;
}

button,input,textarea,select{
  font-family:inherit;
}

button{
  cursor:pointer;
}

.hidden{
  display:none!important;
}

/* =========================
   LOGIN
========================= */

.auth{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:20px;
  background:linear-gradient(135deg,#ffe4f3,#f0e6ff);
}

.auth-box{
  width:100%;
  max-width:400px;
  background:white;
  padding:30px;
  border-radius:25px;
  box-shadow:0 15px 40px rgba(0,0,0,.1);
}

.logo{
  text-align:center;
  font-size:34px;
  font-weight:900;
  color:#d63384;
}

.tagline{
  text-align:center;
  color:#777;
  margin:8px 0 25px;
  font-size:14px;
}

.auth-box h2{
  text-align:center;
  margin-bottom:18px;
}

.field{
  margin-bottom:13px;
}

.field label{
  display:block;
  font-size:13px;
  font-weight:bold;
  margin-bottom:6px;
}

.field input,
.field textarea,
.field select{
  width:100%;
  border:1px solid #ddd;
  padding:12px;
  border-radius:12px;
  outline:none;
  background:#fff;
}

.field textarea{
  min-height:100px;
  resize:vertical;
}

.field input:focus,
.field textarea:focus,
.field select:focus{
  border-color:#d63384;
}

.btn{
  border:0;
  border-radius:12px;
  padding:12px 16px;
  font-weight:bold;
}

.btn-primary{
  width:100%;
  background:#d63384;
  color:white;
}

.btn-secondary{
  width:100%;
  background:#f7e4f0;
  color:#b52b70;
  margin-top:9px;
}

.switch{
  text-align:center;
  margin-top:18px;
  font-size:14px;
}

.switch span{
  color:#d63384;
  font-weight:bold;
  cursor:pointer;
}

/* =========================
   APP
========================= */

header{
  position:sticky;
  top:0;
  z-index:20;
  background:white;
  border-bottom:1px solid #eee;
}

.header-inner{
  max-width:1100px;
  margin:auto;
  padding:13px 18px;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

.brand{
  color:#d63384;
  font-size:24px;
  font-weight:900;
}

.header-user{
  display:flex;
  align-items:center;
  gap:8px;
}

.avatar{
  width:36px;
  height:36px;
  border-radius:50%;
  background:#d63384;
  color:white;
  display:flex;
  align-items:center;
  justify-content:center;
  font-weight:bold;
}

.logout{
  border:0;
  background:#f8e6f1;
  color:#b52b70;
  padding:8px 11px;
  border-radius:10px;
  font-size:12px;
  font-weight:bold;
}

main{
  max-width:1100px;
  margin:auto;
  padding:18px;
  padding-bottom:90px;
}

/* =========================
   NAV
========================= */

.nav{
  display:flex;
  gap:8px;
  overflow-x:auto;
  margin-bottom:20px;
}

.nav button{
  white-space:nowrap;
  border:1px solid #eee;
  background:white;
  padding:10px 16px;
  border-radius:20px;
}

.nav button.active{
  background:#d63384;
  color:white;
  border-color:#d63384;
}

/* =========================
   SEARCH
========================= */

.search{
  width:100%;
  border:1px solid #ddd;
  padding:13px 16px;
  border-radius:14px;
  margin-bottom:20px;
  outline:none;
}

/* =========================
   FEED
========================= */

.section-title{
  font-size:24px;
  margin-bottom:5px;
}

.section-desc{
  color:#777;
  margin-bottom:18px;
  font-size:14px;
}

.feed{
  display:grid;
  grid-template-columns:repeat(auto-fill,minmax(280px,1fr));
  gap:18px;
}

.card{
  background:white;
  border-radius:18px;
  overflow:hidden;
  box-shadow:0 5px 20px rgba(0,0,0,.07);
}

.card-img{
  width:100%;
  aspect-ratio:4/3;
  object-fit:cover;
  background:#f3eaf0;
}

.card-body{
  padding:15px;
}

.card-user{
  font-size:12px;
  color:#d63384;
  font-weight:bold;
  margin-bottom:7px;
}

.card h3{
  font-size:18px;
  margin-bottom:7px;
}

.card p{
  font-size:13px;
  color:#666;
  line-height:1.5;
}

.badge{
  display:inline-block;
  background:#f9e3f0;
  color:#b52b70;
  padding:5px 9px;
  border-radius:20px;
  font-size:11px;
  margin-top:10px;
}

.actions{
  display:flex;
  align-items:center;
  gap:8px;
  margin-top:14px;
  border-top:1px solid #eee;
  padding-top:12px;
}

.action{
  border:0;
  background:#f7f7f7;
  padding:8px 11px;
  border-radius:10px;
  font-size:13px;
}

.action.liked{
  background:#ffe0ee;
  color:#d63384;
}

.delete{
  margin-left:auto;
  color:#d33;
}

/* =========================
   UPLOAD
========================= */

.upload-box{
  max-width:650px;
  margin:auto;
  background:white;
  padding:22px;
  border-radius:20px;
  box-shadow:0 5px 20px rgba(0,0,0,.06);
}

.preview{
  width:100%;
  max-height:350px;
  object-fit:contain;
  background:#f5f5f5;
  border-radius:15px;
  margin-top:10px;
}

/* =========================
   PROFILE
========================= */

.profile{
  background:white;
  border-radius:22px;
  padding:25px;
  text-align:center;
  margin-bottom:20px;
  box-shadow:0 5px 20px rgba(0,0,0,.06);
}

.profile-avatar{
  width:85px;
  height:85px;
  margin:auto;
  border-radius:50%;
  background:#d63384;
  color:white;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:32px;
  font-weight:bold;
  margin-bottom:12px;
}

.profile h2{
  margin-bottom:5px;
}

.profile p{
  color:#777;
  font-size:14px;
}

.stats{
  display:flex;
  justify-content:center;
  gap:40px;
  margin-top:18px;
}

.stat strong{
  display:block;
  font-size:20px;
  color:#d63384;
}

.stat span{
  font-size:12px;
  color:#777;
}

/* =========================
   COMMENTS
========================= */

.comment-box{
  padding:15px;
  background:#fff;
  margin-top:10px;
  border-top:1px solid #eee;
}

.comment{
  padding:9px;
  background:#fafafa;
  border-radius:10px;
  margin-bottom:7px;
  font-size:13px;
}

.comment strong{
  color:#d63384;
}

.comment-input{
  display:flex;
  gap:7px;
  margin-top:10px;
}

.comment-input input{
  flex:1;
  border:1px solid #ddd;
  padding:9px;
  border-radius:9px;
}

.comment-input button{
  background:#d63384;
  color:white;
  border-radius:9px;
  padding:9px 12px;
  border:0;
}

/* =========================
   EMPTY
========================= */

.empty{
  text-align:center;
  padding:50px 20px;
  color:#888;
  background:white;
  border-radius:18px;
}

.empty-icon{
  font-size:45px;
  margin-bottom:10px;
}

/* =========================
   TOAST
========================= */

.toast{
  position:fixed;
  bottom:25px;
  left:50%;
  transform:translateX(-50%);
  background:#333;
  color:white;
  padding:12px 18px;
  border-radius:12px;
  font-size:13px;
  z-index:100;
  opacity:0;
  pointer-events:none;
  transition:.3s;
}

.toast.show{
  opacity:1;
}

/* =========================
   MOBILE
========================= */

@media(max-width:600px){

  .header-inner{
    padding:12px;
  }

  .brand{
    font-size:21px;
  }

  main{
    padding:13px;
  }

  .feed{
    grid-template-columns:1fr;
  }

  .stats{
    gap:25px;
  }
}
</style>
</head>

<body>

<!-- =========================
     AUTH PAGE
========================= -->

<section id="authPage" class="auth">

  <div class="auth-box">

    <div class="logo">SMKarya</div>

    <div class="tagline">
      Berkarya, berbagi, dan bangun portofoliomu.
    </div>

    <!-- LOGIN -->

    <div id="loginForm">

      <h2>Masuk</h2>

      <div class="field">
        <label>Email</label>
        <input id="loginEmail" type="email" placeholder="Masukkan email">
      </div>

      <div class="field">
        <label>Password</label>
        <input id="loginPassword" type="password" placeholder="Masukkan password">
      </div>

      <button class="btn btn-primary" onclick="login()">
        Masuk
      </button>

      <div class="switch">
        Belum punya akun?
        <span onclick="showRegister()">Daftar</span>
      </div>

    </div>

    <!-- REGISTER -->

    <div id="registerForm" class="hidden">

      <h2>Buat Akun</h2>

      <div class="field">
        <label>Nama</label>
        <input id="regName" type="text" placeholder="Nama lengkap">
      </div>

      <div class="field">
        <label>Email</label>
        <input id="regEmail" type="email" placeholder="Email">
      </div>

      <div class="field">
        <label>Password</label>
        <input id="regPassword" type="password" placeholder="Minimal 6 karakter">
      </div>

      <div class="field">
        <label>Jurusan</label>
        <input id="regMajor" type="text" placeholder="Contoh: Tata Busana">
      </div>

      <button class="btn btn-primary" onclick="register()">
        Daftar
      </button>

      <div class="switch">
        Sudah punya akun?
        <span onclick="showLogin()">Masuk</span>
      </div>

    </div>

  </div>

</section>


<!-- =========================
     APP
========================= -->

<section id="app" class="hidden">

<header>

  <div class="header-inner">

    <div class="brand">
      SMKarya
    </div>

    <div class="header-user">

      <div id="headerAvatar" class="avatar">
        ?
      </div>

      <button class="logout" onclick="logout()">
        Keluar
      </button>

    </div>

  </div>

</header>


<main>

  <div class="nav">

    <button id="navHome"
            class="active"
            onclick="showPage('home')">
      🏠 Beranda
    </button>

    <button id="navExplore"
            onclick="showPage('explore')">
      🔎 Explore
    </button>

    <button id="navUpload"
            onclick="showPage('upload')">
      ➕ Upload
    </button>

    <button id="navProfile"
            onclick="showPage('profile')">
      👤 Profil
    </button>

  </div>


  <!-- HOME -->

  <section id="homePage">

    <h1 class="section-title">
      Karya Siswa SMK
    </h1>

    <p class="section-desc">
      Temukan dan apresiasi karya siswa dari berbagai jurusan.
    </p>

    <div id="homeFeed" class="feed"></div>

  </section>


  <!-- EXPLORE -->

  <section id="explorePage" class="hidden">

    <h1 class="section-title">
      Explore
    </h1>

    <p class="section-desc">
      Cari karya berdasarkan judul, nama, jurusan, atau kategori.
    </p>

    <input
      id="searchInput"
      class="search"
      type="text"
      placeholder="Cari karya..."
      oninput="searchWorks()"
    >

    <div id="exploreFeed" class="feed"></div>

  </section>


  <!-- UPLOAD -->

  <section id="uploadPage" class="hidden">

    <h1 class="section-title">
      Upload Karya
    </h1>

    <p class="section-desc">
      Bagikan hasil karya terbaikmu kepada siswa SMK lainnya.
    </p>

    <div class="upload-box">

      <div class="field">
        <label>Foto Karya</label>
        <input
          id="workImage"
          type="file"
          accept="image/*"
          onchange="previewImage(event)"
        >
      </div>

      <img
        id="imagePreview"
        class="preview hidden"
      >

      <div class="field">
        <label>Judul Karya</label>
        <input
          id="workTitle"
          type="text"
          placeholder="Contoh: Busana Batik Modern"
        >
      </div>

      <div class="field">
        <label>Deskripsi</label>
        <textarea
          id="workDescription"
          placeholder="Ceritakan tentang karyamu..."
        ></textarea>
      </div>

      <div class="field">
        <label>Jurusan</label>

        <select id="workMajor">

          <option value="">
            Pilih jurusan
          </option>

          <option>Tata Busana</option>
          <option>Desain Komunikasi Visual</option>
          <option>Teknik Mesin</option>
          <option>Teknik Kendaraan Ringan</option>
          <option>Teknik Sepeda Motor</option>
          <option>Teknik Komputer dan Jaringan</option>
          <option>Rekayasa Perangkat Lunak</option>
          <option>Akuntansi</option>
          <option>Manajemen Perkantoran</option>
          <option>Pemasaran</option>
          <option>Perhotelan</option>
          <option>Usaha Layanan Pariwisata</option>
          <option>Kuliner</option>
          <option>Teknik Ketenagalistrikan</option>
          <option>Teknik Elektronika</option>
          <option>Teknik Konstruksi</option>
          <option>Farmasi</option>
          <option>Kimia Industri</option>
          <option>Animasi</option>
          <option>Broadcasting</option>

        </select>

      </div>

      <div class="field">
        <label>Kategori</label>

        <select id="workCategory">

          <option value="">
            Pilih kategori
          </option>

          <option>Fashion</option>
          <option>Desain</option>
          <option>Produk</option>
          <option>Kuliner</option>
          <option>Teknologi</option>
          <option>Kerajinan</option>
          <option>Fotografi</option>
          <option>Video</option>
          <option>Lainnya</option>

        </select>

      </div>

      <button
        class="btn btn-primary"
        onclick="uploadWork()"
      >
        Publikasikan Karya
      </button>

    </div>

  </section>


  <!-- PROFILE -->

  <section id="profilePage" class="hidden">

    <div class="profile">

      <div
        id="profileAvatar"
        class="profile-avatar"
      >
        ?
      </div>

      <h2 id="profileName">
        -
      </h2>

      <p id="profileEmail">
        -
      </p>

      <p id="profileMajor">
        -
      </p>

      <div class="stats">

        <div class="stat">
          <strong id="profileWorks">0</strong>
          <span>Karya</span>
        </div>

        <div class="stat">
          <strong id="profileLikes">0</strong>
          <span>Like</span>
        </div>

      </div>

    </div>

    <h2 class="section-title">
      Portofolio Saya
    </h2>

    <p class="section-desc">
      Semua karya yang kamu publikasikan akan otomatis menjadi portofolio.
    </p>

    <div id="profileFeed" class="feed"></div>

  </section>

</main>

</section>


<div id="toast" class="toast"></div>


<script>

/* ==================================================
   SMKARYA
   VERSI STANDALONE
   DATA DISIMPAN DI LOCALSTORAGE
================================================== */


/* =========================
   DATABASE LOCAL
========================= */

let users =
  JSON.parse(localStorage.getItem("smkarya_users") || "[]");

let works =
  JSON.parse(localStorage.getItem("smkarya_works") || "[]");

let comments =
  JSON.parse(localStorage.getItem("smkarya_comments") || "[]");

let currentUser =
  JSON.parse(localStorage.getItem("smkarya_current") || "null");


/* =========================
   SAVE DATABASE
========================= */

function saveData(){

  localStorage.setItem(
    "smkarya_users",
    JSON.stringify(users)
  );

  localStorage.setItem(
    "smkarya_works",
    JSON.stringify(works)
  );

  localStorage.setItem(
    "smkarya_comments",
    JSON.stringify(comments)
  );

}


/* =========================
   ID
========================= */

function uid(){

  return Date.now().toString(36) +
         Math.random().toString(36).substring(2);

}


/* =========================
   TOAST
========================= */

function toast(message){

  const el =
    document.getElementById("toast");

  el.textContent = message;

  el.classList.add("show");

  setTimeout(() => {
    el.classList.remove("show");
  },2500);

}


/* =========================
   AUTH PAGE
========================= */

function showRegister(){

  document
    .getElementById("loginForm")
    .classList.add("hidden");

  document
    .getElementById("registerForm")
    .classList.remove("hidden");

}


function showLogin(){

  document
    .getElementById("registerForm")
    .classList.add("hidden");

  document
    .getElementById("loginForm")
    .classList.remove("hidden");

}


/* =========================
   REGISTER
========================= */

function register(){

  const name =
    document.getElementById("regName")
    .value.trim();

  const email =
    document.getElementById("regEmail")
    .value.trim()
    .toLowerCase();

  const password =
    document.getElementById("regPassword")
    .value;

  const major =
    document.getElementById("regMajor")
    .value.trim();


  if(!name || !email || !password || !major){

    toast("Lengkapi semua data.");

    return;
  }


  if(password.length < 6){

    toast("Password minimal 6 karakter.");

    return;
  }


  if(users.some(u => u.email === email)){

    toast("Email sudah terdaftar.");

    return;
  }


  const user = {

    id:uid(),

    name:name,

    email:email,

    password:password,

    major:major,

    createdAt:Date.now()

  };


  users.push(user);

  saveData();


  currentUser = user;

  localStorage.setItem(
    "smkarya_current",
    JSON.stringify(currentUser)
  );


  openApp();

  toast("Akun berhasil dibuat!");

}


/* =========================
   LOGIN
========================= */

function login(){

  const email =
    document.getElementById("loginEmail")
    .value.trim()
    .toLowerCase();

  const password =
    document.getElementById("loginPassword")
    .value;


  const user =
    users.find(
      u =>
        u.email === email &&
        u.password === password
    );


  if(!user){

    toast("Email atau password salah.");

    return;
  }


  currentUser = user;

  localStorage.setItem(
    "smkarya_current",
    JSON.stringify(currentUser)
  );


  openApp();

}


/* =========================
   LOGOUT
========================= */

function logout(){

  currentUser = null;

  localStorage.removeItem(
    "smkarya_current"
  );

  document
    .getElementById("app")
    .classList.add("hidden");

  document
    .getElementById("authPage")
    .classList.remove("hidden");

  showLogin();

}


/* =========================
   OPEN APP
========================= */

function openApp(){

  document
    .getElementById("authPage")
    .classList.add("hidden");

  document
    .getElementById("app")
    .classList.remove("hidden");


  updateProfile();

  renderHome();

}


/* =========================
   PAGE
========================= */

function showPage(page){

  const pages = [

    "homePage",
    "explorePage",
    "uploadPage",
    "profilePage"

  ];


  pages.forEach(id => {

    document
      .getElementById(id)
      .classList.add("hidden");

  });


  document
    .getElementById(page + "Page")
    .classList.remove("hidden");


  document
    .querySelectorAll(".nav button")
    .forEach(btn => {

      btn.classList.remove("active");

    });


  if(page === "home"){

    document
      .getElementById("navHome")
      .classList.add("active");

    renderHome();

  }


  if(page === "explore"){

    document
      .getElementById("navExplore")
      .classList.add("active");

    searchWorks();

  }


  if(page === "upload"){

    document
      .getElementById("navUpload")
      .classList.add("active");

  }


  if(page === "profile"){

    document
      .getElementById("navProfile")
      .classList.add("active");

    renderProfile();

  }

}


/* =========================
   IMAGE PREVIEW
========================= */

function previewImage(event){

  const file =
    event.target.files[0];

  if(!file) return;


  const reader =
    new FileReader();


  reader.onload = function(e){

    const preview =
      document.getElementById("imagePreview");

    preview.src = e.target.result;

    preview.classList.remove("hidden");

  };


  reader.readAsDataURL(file);

}


/* =========================
   UPLOAD WORK
========================= */

function uploadWork(){

  if(!currentUser){

    toast("Silakan login.");

    return;
  }


  const file =
    document
      .getElementById("workImage")
      .files[0];


  const title =
    document
      .getElementById("workTitle")
      .value.trim();


  const description =
    document
      .getElementById("workDescription")
      .value.trim();


  const major =
    document
      .getElementById("workMajor")
      .value;


  const category =
    document
      .getElementById("workCategory")
      .value;


  if(!file || !title || !description || !major || !category){

    toast("Lengkapi semua data karya.");

    return;
  }


  if(!file.type.startsWith("image/")){

    toast("File harus berupa gambar.");

    return;
  }


  const reader =
    new FileReader();


  reader.onload = function(e){

    const work = {

      id:uid(),

      userId:currentUser.id,

      userName:currentUser.name,

      title:title,

      description:description,

      major:major,

      category:category,

      image:e.target.result,

      likes:[],

      createdAt:Date.now()

    };


    works.unshift(work);

    saveData();


    document
      .getElementById("workImage")
      .value = "";

    document
      .getElementById("workTitle")
      .value = "";

    document
      .getElementById("workDescription")
      .value = "";

    document
      .getElementById("workMajor")
      .value = "";

    document
      .getElementById("workCategory")
      .value = "";


    document
      .getElementById("imagePreview")
      .classList.add("hidden");


    toast("Karya berhasil dipublikasikan!");

    showPage("home");

  };


  reader.readAsDataURL(file);

}


/* =========================
   RENDER HOME
========================= */

function renderHome(){

  const container =
    document.getElementById("homeFeed");


  if(!works.length){

    container.innerHTML = emptyHTML(
      "🎨",
      "Belum ada karya",
      "Jadilah siswa pertama yang membagikan karya!"
    );

    return;
  }


  container.innerHTML =
    works.map(workCard).join("");

}


/* =========================
   EXPLORE
========================= */

function searchWorks(){

  const query =
    document
      .getElementById("searchInput")
      .value
      .toLowerCase()
      .trim();


  const filtered =
    works.filter(work =>

      work.title.toLowerCase().includes(query) ||

      work.description.toLowerCase().includes(query) ||

      work.major.toLowerCase().includes(query) ||

      work.category.toLowerCase().includes(query) ||

      work.userName.toLowerCase().includes(query)

    );


  const container =
    document.getElementById("exploreFeed");


  if(!filtered.length){

    container.innerHTML = emptyHTML(
      "🔎",
      "Karya tidak ditemukan",
      "Coba gunakan kata pencarian lain."
    );

    return;
  }


  container.innerHTML =
    filtered.map(workCard).join("");

}


/* =========================
   WORK CARD
========================= */

function workCard(work){

  const liked =
    currentUser &&
    work.likes &&
    work.likes.includes(currentUser.id);


  const commentList =
    comments.filter(
      c => c.workId === work.id
    );


  return `

  <article class="card">

    <img
      class="card-img"
      src="${work.image}"
      alt="${escapeHTML(work.title)}"
    >

    <div class="card-body">

      <div class="card-user">
        👤 ${escapeHTML(work.userName)}
      </div>

      <h3>
        ${escapeHTML(work.title)}
      </h3>

      <p>
        ${escapeHTML(work.description)}
      </p>

      <span class="badge">
        ${escapeHTML(work.major)}
      </span>

      <span class="badge">
        ${escapeHTML(work.category)}
      </span>

      <div class="actions">

        <button
          class="action ${liked ? "liked" : ""}"
          onclick="toggleLike('${work.id}')"
        >
          ❤️ ${work.likes ? work.likes.length : 0}
        </button>

        <button
          class="action"
          onclick="focusComment('${work.id}')"
        >
          💬 ${commentList.length}
        </button>

        ${
          currentUser &&
          currentUser.id === work.userId
          ?
          `
          <button
            class="action delete"
            onclick="deleteWork('${work.id}')"
          >
            🗑️
          </button>
          `
          :
          ""
        }

      </div>

      <div class="comment-box">

        ${
          commentList
            .map(c => `
              <div class="comment">
                <strong>
                  ${escapeHTML(c.userName)}
                </strong>
                <br>
                ${escapeHTML(c.text)}
              </div>
            `)
            .join("")
        }

        <div
          class="comment-input"
          id="comment-${work.id}"
        >

          <input
            id="input-${work.id}"
            type="text"
            placeholder="Tulis komentar..."
            onkeydown="commentKey(event,'${work.id}')"
          >

          <button
            onclick="addComment('${work.id}')"
          >
            Kirim
          </button>

        </div>

      </div>

    </div>

  </article>

  `;

}


/* =========================
   LIKE
========================= */

function toggleLike(workId){

  if(!currentUser){

    toast("Silakan login.");

    return;
  }


  const work =
    works.find(w => w.id === workId);


  if(!work) return;


  if(!work.likes){

    work.likes = [];

  }


  const index =
    work.likes.indexOf(currentUser.id);


  if(index >= 0){

    work.likes.splice(index,1);

  }else{

    work.likes.push(currentUser.id);

  }


  saveData();

  refreshCurrentPage();

}


/* =========================
   COMMENT
========================= */

function addComment(workId){

  if(!currentUser){

    toast("Silakan login.");

    return;
  }


  const input =
    document.getElementById(
      "input-" + workId
    );


  const text =
    input.value.trim();


  if(!text){

    return;
  }


  comments.push({

    id:uid(),

    workId:workId,

    userId:currentUser.id,

    userName:currentUser.name,

    text:text,

    createdAt:Date.now()

  });


  saveData();

  input.value = "";

  refreshCurrentPage();

}


function commentKey(event,workId){

  if(event.key === "Enter"){

    addComment(workId);

  }

}


function focusComment(workId){

  const input =
    document.getElementById(
      "input-" + workId
    );


  if(input){

    input.focus();

    input.scrollIntoView({
      behavior:"smooth",
      block:"center"
    });

  }

}


/* =========================
   DELETE
========================= */

function deleteWork(workId){

  if(!confirm("Hapus karya ini?")){

    return;

  }


  works =
    works.filter(
      w => w.id !== workId
    );


  comments =
    comments.filter(
      c => c.workId !== workId
    );


  saveData();

  toast("Karya berhasil dihapus.");

  refreshCurrentPage();

}


/* =========================
   PROFILE
========================= */

function updateProfile(){

  if(!currentUser) return;


  const initial =
    currentUser.name
      .charAt(0)
      .toUpperCase();


  document
    .getElementById("headerAvatar")
    .textContent = initial;


  document
    .getElementById("profileAvatar")
    .textContent = initial;


  document
    .getElementById("profileName")
    .textContent =
      currentUser.name;


  document
    .getElementById("profileEmail")
    .textContent =
      currentUser.email;


  document
    .getElementById("profileMajor")
    .textContent =
      currentUser.major;


  const myWorks =
    works.filter(
      w => w.userId === currentUser.id
    );


  const likes =
    myWorks.reduce(
      (total,w) =>
        total +
        (w.likes ? w.likes.length : 0),
      0
    );


  document
    .getElementById("profileWorks")
    .textContent =
      myWorks.length;


  document
    .getElementById("profileLikes")
    .textContent =
      likes;

}


function renderProfile(){

  updateProfile();


  const myWorks =
    works.filter(
      w => w.userId === currentUser.id
    );


  const container =
    document.getElementById("profileFeed");


  if(!myWorks.length){

    container.innerHTML =
      emptyHTML(
        "📁",
        "Portofolio masih kosong",
        "Upload karya pertamamu sekarang."
      );

    return;
  }


  container.innerHTML =
    myWorks.map(workCard).join("");

}


/* =========================
   REFRESH PAGE
========================= */

function refreshCurrentPage(){

  const visible =
    document.querySelector(
      "#homePage:not(.hidden)"
    );

  if(visible){

    renderHome();

    return;
  }


  const explore =
    document.querySelector(
      "#explorePage:not(.hidden)"
    );

  if(explore){

    searchWorks();

    return;
  }


  const profile =
    document.querySelector(
      "#profilePage:not(.hidden)"
    );

  if(profile){

    renderProfile();

  }

}


/* =========================
   EMPTY
========================= */

function emptyHTML(icon,title,text){

  return `

    <div class="empty">

      <div class="empty-icon">
        ${icon}
      </div>

      <h3>
        ${title}
      </h3>

      <p style="margin-top:7px">
        ${text}
      </p>

    </div>

  `;

}


/* =========================
   SECURITY DISPLAY
========================= */

function escapeHTML(value){

  return String(value)
    .replace(/&/g,"&amp;")
    .replace(/</g,"&lt;")
    .replace(/>/g,"&gt;")
    .replace(/"/g,"&quot;")
    .replace(/'/g,"&#039;");

}


/* =========================
   START APP
========================= */

if(currentUser){

  openApp();

}else{

  document
    .getElementById("authPage")
    .classList.remove("hidden");

}


/* =========================
   DEMO DATA
========================= */

if(works.length === 0){

  /*
    Tidak dibuat karya contoh otomatis
    supaya halaman benar-benar kosong
    sampai pengguna upload karya.
  */

}

</script>

</body>
</html>
