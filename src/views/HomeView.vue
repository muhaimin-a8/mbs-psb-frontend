<script setup lang="ts">
// import TheWelcome from '../components/TheWelcome.vue'
import AppBar from "../components/AppBar.vue";
import Footer from "../components/Footer.vue";

function getDateFromStamp(timestamp: number): string {
  const date = new Date(timestamp * 1000);
  const months = [
    "Januari",
    "Februari",
    "Maret",
    "April",
    "Mei",
    "Juni",
    "Juli",
    "Agustus",
    "September",
    "Oktober",
    "November",
    "Desember",
  ];
  return `${date.getUTCDate()} ${
    months[date.getUTCMonth()]
  } ${date.getUTCFullYear()}`;
}
</script>

<template>
  <header>
    <AppBar id="appbar" />
  </header>
  <main>
    <section id="home">
      <div class="left">
        <h1>Menjadi Santri adalah Pemberian Terbaik</h1>
        <p>
          Tidak ada pemberian dari ibu dan bapak yang paling berharga kepada anaknya, melainkan pendidikan akhlak mulia.
          Lulusan pesantren itu tidak cuma bisa jadi guru mengaji ataupun kyai! Tapi, juga bisa menjadi kalangan berdasi dan pengusaha yang mandiri.
        </p>
        <div class="btn-container">
          <div class="btn"><a href="https://docs.google.com/forms/d/1aTCToPUchaEipAYpffO-Q-lBP7qqj4QsKm9AyukLaAw/edit" target="_blank">Daftar Sekarang</a></div>
          <div id="lihat-brosur"><a href="https://drive.google.com/file/d/1T7u3u31er0fhiaH4FCgPhPJM6KtrEjvy/view?usp=sharing" target="_blank">Lihat Brosur</a></div>
        </div>
      </div>
      <div class="right">
        <img src="@/assets/home-ilustration.jpg" alt="admission cartoon" />
      </div>
    </section>

    <section id="timeline">
      <h2 class="title">Timeline Pendaftaran</h2>
      <ul>
        <li class="card">
          <h3>Gelombang I</h3>
          <p>{{ getDateFromStamp(1662005228) }} - {{ getDateFromStamp(1667275628) }}</p>
        </li>
        <li class="card">
          <h3>Gelombang II</h3>
          <p>{{ getDateFromStamp(1668053228) }} - {{ getDateFromStamp(1675224428) }}</p>
        </li>
        <li class="card">
          <h3>Gelombang III</h3>
          <p>{{ getDateFromStamp(1676434028) }} - {{ getDateFromStamp(1685592428) }}</p>
        </li>
      </ul>
    </section>

    <section id="syarat-pendaftaran">
      <h2 class="title">Syarat Pendaftaran</h2>
      <div class="container">
        <div class="right">
          <img src="@/assets/home-ilustration.jpg" alt="admission cartoon" />
        </div>
        <div class="left">
          <ul>
            <h3 class="subtitle">Persyaratan Umum</h3>
            <li>Laki-laki atau perempuan beragama Islam</li>
            <li>Sehat jasmani dan rohani</li>
            <li>Bersedia tinggal si asrama dan sanggup menaati peraturan pondok pesantren</li>
            <li>Mampu membaca Al-Qur'an</li>
            <li>Memiliki Ijazah dan SKHUN</li>
            <li>Lulus seleksi PSB MBS Purworejo</li>
          </ul>
          <ul>
            <h3 class="subtitle">Persyaratan Utama</h3>
            <li>FotoCopy KK & KTP kedua orangtua/wali (2 lembar)</li>
            <li>FotoCopy Akta kelahiran (2 lembar) </li>
            <li>FotoCopy raport SD/Mi kelas VI semester I (1 lembar) </li>
            <li>FotoCopy raport SMP/MTs kelas IX semester I (1 lembar) </li>
            <li>Pas Foto berwarna ukuran 3x4 (4 lembar)</li>
            <li>Foto Copy sertifikat atau piagam prestai (jika ada)</li>
          </ul>
          <ul>
            <h3 class="subtitle">Persyaratan Tanbahan (jika ada)</h3>
            <li>FotoCopy Ijazah (2 lembar)</li>
            <li>FotoCopy SKHUN (2 lembar) </li>
          </ul>
        </div>
      </div>
    </section>
  </main>
  <footer>
    <Footer />
  </footer>
</template>

<style>
header {
  display: inline;
}

#appbar {
  position: sticky;
  top: 0;
}

#home {
  min-height: 540px;
  background-color: #fff;
  display: flex;
  align-items: center;
}

section:not(:first-child) {
  margin-top: 96px;
}

#home .left {
  width: 50%;
}

#home .left h1 {
  color: var(--primary-color);
  font-size: 3em;
  font-weight: bolder;
}

#home .left p {
  color: var(--vt-c-text-light-1);
  margin-top: 16px;
}

.btn-container {
  display: flex;
  align-items: center;
  margin-top: 18px;
}

#lihat-brosur {
  margin-left: 18px;
}

#lihat-brosur a {
  color: var(--primary-color);
}

#home .left .btn a {
  font-size: 16px;
}

#home .right {
  width: 50%;
}

#home .right img {
  width: 100%;
}

.title {
  color: var(--primary-color);
  text-align: center;
  font-weight: bold;
}

/*.title::after {*/
/*  content: "";*/
/*  height: 4px;*/
/*  width: 126px;*/
/*  border-radius: 12px;*/
/*  background-color: var(--primary-color);*/
/*  position: absolute;*/
/*  transform: translate(-100%, 36px);*/
/*}*/

#timeline ul {
  text-align: center;
  margin-top: 24px;
  list-style: none;
  width: 100%;
  display: flex;
  overflow: auto;
  padding: 18px;
}

#timeline li {
  margin-right: 36px;
  background-color: #fff;
  min-width: 360px;
}
#timeline li:last-child {
  margin-right: 0;
}

.card {
  padding: 16px;
  box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.5);
  border-radius: 8px;
  border: 1px solid rgba(0, 0, 0, 0.2);
}

#timeline h3 {
  color: var(--primary-color);
  font-weight: 500;
}

#syarat-pendaftaran .container {
  display: flex;
  margin-top: 18px;
}

#syarat-pendaftaran .left ul {
  margin-top: 18px;
}
#syarat-pendaftaran li {
  margin-top: 16px;
  font-size: 1em;
}

#syarat-pendaftaran .subtitle {
  color: var(--primary-color);
  font-weight: 500;
}

#syarat-pendaftaran .right,
#syarat-pendaftaran .left {
  width: 50%;
}

#syarat-pendaftaran img {
  width: 100%;
}

@media (max-width: 450px) {
  #home {
    display: block;
  }

  #home .left,
  #home .right {
    width: 100%;
  }

  #syarat-pendaftaran .container {
    display: block;
  }

  #syarat-pendaftaran .right,
  #syarat-pendaftaran .left {
    width: 100%;
  }
}
</style>

<script lang="ts"></script>
