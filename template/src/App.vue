<template>
    <div id="app">
        <transition 
            name="fade"
            mode="out-in">
            <router-view></router-view>
        </transition>
    </div>
</template>
<style>
html {
  scroll-behavior: smooth;
}
#app{
    font-family: 'Supermolot', sans-serif;
    background: #000;
}
*{
    margin: 0;
    padding: 0;
}
a{
    text-decoration: none;
}
iframe{
    height: 100%;
    width: 100%;
    /* border: 1px solid #ECAA00; */
}
.grad{
    height: 1.5px;
    background: radial-gradient(730.38px at 44.92% 49.97%, rgba(236, 170, 0, 0.5) 0%, rgba(236, 170, 0, 0) 100%);
    transform: matrix(1, 0, 0, -1, 0, 0);
}
/* Router transition */
  .fade-enter-active,
  .fade-leave-active {
    transition-duration: 0.3s;
    transition-property: opacity;
    transition-timing-function: ease;
  }
  .fade-enter,
  .fade-leave-active {
    opacity: 0
  }
</style>
