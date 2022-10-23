<template>
<div id="appbar">
  <a href="#"><img src="@/assets/mbs-logo.png" alt="logo mbs purworejo"></a>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Timeline</a></li>
      <li><a href="#">Contact</a></li>
      <li class="btn"><a href="#">Login</a></li>
    </ul>
  </nav>
</div>
</template>

<script>
export default {
  name: "AppBar"
}
</script>

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
}

ul li {
  display: inline;
  margin-right: 18px;
}

ul li a {
  color: var(--primary-color);
}
ul li:not(.btn) a:hover::after{
  content: '';
  width: 18px;
  height: 4px;
  border-radius: 5px;
  position: absolute;
  transform: translate(calc(-50% - 18px), -12px);
  background-color: var(--primary-color);
}

ul .btn a {
  background-color: var(--primary-color);
  padding: 8px 16px;
  border-radius: 25px;
  color: var(--vt-c-text-dark-1);
}
</style>