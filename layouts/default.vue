<template>
  <div id="header">
    <header class="shadow-sm bg white">
      <img
        src="`assets/Logo.png`"
        class="rounded float-start logo m-2"
        alt="Ubuntu Travel Logo"
      />
      <nav class="container mx-auto p-4 flex justify-between">
        <nuxt-link to="/" class="font-bold"></nuxt-link>
        <ul class="flex gap-4">
          <li><nuxt-link to="/">Home</nuxt-link></li>
          <li><nuxt-link to="/travel">Book</nuxt-link></li>
          <li><nuxt-link to="/about">About</nuxt-link></li>
        </ul>
      </nav>
    </header>
  </div>

  <div id="body">
    <div class="container mx-auto p-4">
      <slot />
    </div>
  </div>
  <div id="footer" class="container">
    <!-- <img src="`/assets/background.jpg`" alt="" /> -->
  </div>
</template>

<style>
.router-link-exact-active {
  color: #12b488;
}
.logo {
  width: 200px;
}
header > img {
  max-width: 90px;
}
#header {
  height: 20vh;
}
#body {
  height: 40vh;
}

#footer > img {
  clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
  max-height: 400px;
}
ul {
  list-style-type: none;
}

ul > li {
  display: inline-block;
  margin: 0 20px;
}
</style>
