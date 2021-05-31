<template>
  <div id="nav">
    <header>
      <div class="container">
        <div class="header-wrapper">
          <router-link to="/">
            <img
              src="https://i.ibb.co/fxPqDdL/image-2.png"
              alt="image-2"
              border="0"
          /></router-link>
          <router-link to="/favorites"
            ><a href="">Избранные котики<i class="far fa-heart"></i></a
          ></router-link>
        </div>
      </div>
    </header>
  </div>
  <router-view />
</template>

<style src="./main.min.css"></style>
