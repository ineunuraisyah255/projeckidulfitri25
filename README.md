<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kartu Ucapan Idul Fitri</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="bintik" style="top: 100px; left: 50px;"></div>
  <div class="bintik" style="top: 200px; left: 150px;"></div>
  <div class="bintik" style="top: 300px; left: 250px;"></div>
  <div class="bintik" style="top: 400px; left: 350px;"></div>
  <div class="bintik" style="top: 500px; left: 450px;"></div>
  <div class="moonstar"></div>
  <div class="moonstar"></div>
    <div class="pesan">
      <h2>Hallo tetehQU</h2>
    </div>

    <div clas="container">
    <div class="card">
    <div class="slide" id="slide1">
      <img src="sticker 1.jpg" alt="sticker">
      <h1>Selamat Hari Raya Idul fitri teteh &#128591;</h1>
      <p>Di hari yang Fitri ini Mari kita saling bermaaf-maafan</p>
      <p>Maaf jika selama ini adik tingkat mu suka membuat kesalahan yang namanya manusia tidak pernah luput dari yang namanya kesalahan</p>
      <P>Taqabalallahu Mina Wamingkum Siyamana siyamakum</P>
      <p>Minal Aidzin Walfaidzin Mohon maaf lahir dan batin</p>
      <button onclick="prevSlide()"Sebelumnya></button>
    </div>
    <div class="slide" id="slide2">
      <img src="gambar 3.jpg" alt="sticker THR" class="gambar-thr">
      <h1>THR dari hati yang tulus untuk teteh yang paling terbaik</h1>
      <p>Semoga lebaran kali ini membawa keberkahan dan bahagiaan bagi kita semua.</p>
      <p>Eeitttsss THR nya nanti ya dikosan wkwkwk</p>
      <p>Jangan diliat dari nilai nya ya tapi liatlah dari ketusannya</p>
      <button onclick="prevSlide()"Sebelumnya></button>
    </div>
    <div class="slide" id="slide3">
      <img src="Aisyah teh raya1 .jpg" alt="Aisyah-teh raya">
      <h1>Teteh, Terimakasih ya</h1>
      <p>teteh selama ini udah jadi temen nonton aisyah, temen nabung aisyah, temen berjuangnya aisyah, sampe menjadi temen umroh aisyah nanti</p>
      <p>Walaupun terkadang suka membuat teteh kesel kecewa dan marah</p>
      <P>Maafin segala kesalahan aisyah yang dulu sekarang dan masa yang akan datang ya teh</P>
      <p>Dari sekian banyak nya kating yang deket sama aisyah, tapi teteh adalah kating yang terbaik aisyah.</p>
      <p>Sehat selalu teteh doa dan harapanku selalu menyertaimu</p>
      <p>#Aisyah Si anak Teknik</p>
      <button onclick="prevSlide()"selanjutnya></button>
    </div>
    </div>
  </div>
  <script src="script.js"></script>
  <script>
    // Ambil elemen pesan
    const pesanElement = document.querySelector('.pesan');

    //Tahbahkan kelas 'show' setelah 1 detik
    setTimeout(() => {
       pesanElement.classList.add('show');
        }, 1000);
  </script>
</body>
</html>
body, html {
    margin: 0;
    padding: 0;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: lightblue;
}

.bintik {
  position: absolute;
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background-color: rgba(234, 208, 17, 0.9);
  animation: berkedip 1s infinite alternate;
}

@keyframes berkedip {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  100% {
    transform: scale(1.5);
    opacity: 0;
  }
}

.moonstar {
  position: absolute;
  width: 50px;
  height: 50px;
  background-color: rgba(237, 245, 14, 0.902);
  clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
  animation: gerakan 10s linear infinite alternate;
}

@keyframes gerakan {
  0% {
    transform: translateX(0) translateY(0) rotate(0);
  }
  100% {
    transform: translateX(200vw) translateY(200vh) rotate(360deg);
  }
}

.pesan {
  background-color: rgb(118, 126, 128);
  padding: 20px;
  text-align: center;
  opacity: 0;
  transition: opacity 0.5s ease;
}

.pesan.show {
  opacity: 1;
}

.container {
  display: grid;
  justify-content: center;
  align-items: center;
  height: 100vh;
  overflow: hidden;
}

.slide {
  display: none;
  text-align: center;
  position: relative;
}

.slide img {
  max-width: 300px;
  height: 200px;
  margin-top: 20px;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
}

.gambar-slide {
  width: 100px;
  height: 50px;
}

.slide img.header-image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: -1;
}

.card {
  background-color: silver;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 20px;
  margin-top: 20px;
  text-align: center;
}

.card img {
  max-width: 100%;
  border-radius: 10px;
  margin: 10px;
}

.card h1 {
  color: rgb(6, 110, 246);
}

.card p {
  color: black;
}
  
const slides = document.querySelectorAll('.slide');
let currentSlide = 0;

function showSlide(index) {
  slides.forEach((slide) => {
    slide.style.display = 'none';
  });
  slides[index].style.display = 'block';
}

function nextSlide() {
  currentSlide++;
  if (currentSlide >= slides.length) {
    currentSlide = 0;
  }
  showSlide(currentSlide);
}

function prevSlide() {
  currentSlide--;
  if (currentSlide < 0) {
    currentSlide = slides.length - 1;
  }
  showSlide(currentSlide);
}

showSlide(currentSlide);  
