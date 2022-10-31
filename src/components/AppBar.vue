<template>
  <div id="appbar">
    <a href="/"
      ><img src="@/assets/mbs-logo-web.svg" alt="logo mbs purworejo"
    /></a>
    <nav>
      <img id="menu-bar" src="@/assets/bars-solid.svg" />
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#timeline">Timeline</a></li>
        <li><a href="#syarat-pendaftaran">Syarat Pendaftaran</a></li>
        <li class="btn"><a href="https://docs.google.com/forms/d/1aTCToPUchaEipAYpffO-Q-lBP7qqj4QsKm9AyukLaAw/edit" target="_blank">Daftar Sekarang</a></li>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
#appbar {
  display: flex;
  background-color: var(--vt-c-white);
  padding: 18px;
  justify-content: space-between;
  align-items: center;
}

img {
  height: 50px;
  padding: 3px;
}

ul li {
  display: inline;
  margin-right: 18px;
}

ul li:not(.btn) a {
  color: var(--primary-color);
}
ul li:not(.btn) a:hover::after {
  content: "";
  width: 18px;
  height: 4px;
  border-radius: 5px;
  position: absolute;
  transform: translate(calc(-50% - 18px), -12px);
  background-color: var(--primary-color);
}

#menu-bar {
  height: 26px;
  display: none;
  margin-right: 18px;
}

@media (max-width: 730px) {
  #menu-bar {
    display: block;
    position: relative;
    z-index: 9;
  }

  ul {
    background-color: #c9c8c8;
    padding: 18px;
    display: none;
  }
  .show ul {
    display: block;
    position: absolute;
    right: 0;
    height: 100vh;
    top: 0;
    min-width: 300px;
  }

  ul li {
    display: block;
    margin-top: 18px;
  }
}

@media (max-width: 450px) {
  #menu-bar {
    margin-right: 12px;
  }
}
</style>

<script lang="ts">
export default {
  name: "AppBar",
  mounted() {
    const menuBar = document.querySelector("#menu-bar");
    const nav = document.querySelector("nav");

    menuBar?.addEventListener("click", (e) => {
      if (nav?.classList.contains("show")) {
        nav?.classList.remove("show");
        menuBar?.setAttribute("src", "src/assets/bars-solid.svg");
      } else {
        nav?.classList.add("show");
        menuBar?.setAttribute("src", "src/assets/xmark-solid.svg");
      }
    });
  },
};
</script>
