<template>
  <footer>
    <div class="above">
      <div class="container identity">
        <img src="@/assets/mbs-logo-web.svg" alt="mbs logo" />
        <p class="address">
          Jl. Srudutan No.06 Dukuh Wetan, Pituruh, Purworejo, Jawa Tengah 54263
        </p>
      </div>
      <div class="container links">
        <h3>Visit Our Website</h3>
        <ul>
          <li>
            <a href="#" target="_blank">Lazismu</a>
          </li>
          <li>
            <a href="https://mbspurworejo.sch.id/" target="_blank">Website Utama</a>
          </li>
          <li>
            <a href="https://pesram.mbspurworejo.sch.id/" target="_blank">Pesantren Ramadhan</a>
          </li>
          <li>
            <a href="#" target="_blank">OSAI</a>
          </li>
        </ul>
      </div>
      <div class="container connect-us">
        <h3>Connect with Us</h3>
        <ul>
          <li>
            <a href="https://wa.me/6282286909231" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
          </li>
          <li>
            <a href="https://www.youtube.com/channel/UCmO4lFIgzpJmSkbjTdFUvLQ?view_as=subscriber" target="_blank"><i class="fa-brands fa-youtube"></i></a>
          </li>
          <li>
            <a href="https://id-id.facebook.com/ppmbspurworejo/" target="_blank"><i class="fa-brands fa-facebook"></i></a>
          </li>
          <li>
            <a href="https://www.instagram.com/mbspurworejo/?hl=id" target="_blank"><i class="fa-brands fa-instagram"></i></a>
          </li>
        </ul>
      </div>
    </div>
    <div class="copyright">
      <p class="author">
        Created By : <a href="#" target="_blank">Muhaimin Abdillah</a>
      </p>
      <p>Copyright &copy; 2022 PPM MBS Purworejo. All rights reserved.</p>
    </div>
  </footer>
</template>

<script lang="ts">
export default {
  name: "Footer",
};
</script>

<style scoped>
footer {
  color: var(--vt-c-text-light-1);
  background-color: rgba(0, 0, 0, 0.2);
  padding-top: 36px;
}

footer .above {
  display: flex;
}

.container {
  width: 100%;
  padding: 18px;
  border-left: 1px solid rgba(0, 0, 0, 0.2);
}

.container:not(:last-child) {
  margin-right: 18px;
}
.identity {
  text-align: left;
}

.identity img {
  max-height: 57px;
}

.identity .address {
  margin-top: 16px;
  font-size: 1em;
}

.container h3 {
  color: var(--primary-color);
  font-weight: bold;
  text-align: left;
}

.container a {
  color: var(--vt-c-text-light-1);
}

ul {
  margin-top: 16px;
  list-style-type: none;
  list-style-position: outside;
  padding: 0;
}

li {
  margin-top: 8px;
}

.copyright {
  margin-top: 76px;
  background-color: var(--primary-color);
  padding: 14px;
  color: var(--vt-c-text-dark-1);
  text-align: center;
}

.connect-us li {
  display: inline;
}

.connect-us li:not(:last-child) {
  margin-right: 18px;
}

.connect-us li i {
  font-size: 2em;
}

.fa-whatsapp:hover{
  color: #09d573;
}

.fa-youtube:hover {
  color: #ff0000;
}

.fa-facebook:hover {
  color: #4267b2;
}

@media (max-width: 670px) {
  p, a, .address{
    font-size: 0.9em;
  }

  .identity img {
    height: 36px;
  }

  h3 {
    font-size: 1em;
  }

  .connect-us li i {
    font-size: 1.5em;
  }
}

@media (max-width: 450px) {
  .connect-us li {
    display: block;
  }
}
</style>
