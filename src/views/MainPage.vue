<script setup>
import ProductDetail from './ProductDetail.vue';
</script>
<template>
   <!--Coffee Prod Header-->
   <div class="position-relative overflow-hidden p-3 p-md-5 m-md-3 text-center bg-body-tertiary">
      <div class="col-md-6 p-lg-5 mx-auto my-5">
        <h1 class="display-3 fw-bold">🍦Select your like cafe☕ </h1>
        <div class="d-flex gap-3 justify-content-center lead fw-normal"></div>
      </div>
      <div class="product-device shadow-sm d-none d-md-block"></div>
      <div class="product-device product-device-2 shadow-sm d-none d-md-block"></div>
    </div> 
    <div class="me-md-3 pt-3 px-3 pt-md-2 px-md-5 text-center overflow-hidden" style="background-color: #ff3ca7; color: rgb(255, 255, 255);">
      <div class="my-3 p-3">
        <h2 class="display-6">เลือกร้านที่ใช่สำหรับคุณ</h2>
      </div>
    </div> <br>
    <ProductDetail/>
  </template>
  


<style>
@import url('https://fonts.googleapis.com/css2?family=Itim&family=Mali&family=Mooli&family=Nunito:wght@500&family=Roboto+Slab&display=swap');
.container {
  max-width: 960px;
}
h1{
  font-family: 'Itim', cursive;
}
h2{
  font-family: 'Itim', cursive;}
.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(0, 0, 0, .85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #ee5d31;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #ee5d31;
  text-decoration: none;
}


.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #ff0faf;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #ed009e;
}
.flex-equal > * {
  flex: 1;
}
@media (min-width: 768px) {
  .flex-md-equal > * {
    flex: 1;
  }
}

</style>