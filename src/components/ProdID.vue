<script setup>
import { ref } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const id = parseInt(route.params.id);

const CoffeeList = ref([
  { id: 1, name: 'Treespresso cafe', img: "https://www.ryoiireview.com/upload/article/202304/1681731156_d018557a4a10aed6c8f450ad0db6d60d.jpg",Tex:"ร้านนี้บรรยากาศดีมากก อยู่ใต้ต้นร่มใหญ่มีความร่มรื่น เขียวขจี ตัวร้านจะมีเน้นโทนไม้ ให้ความรู้สึกอบอุ่น มีความผ่อนคลาย จะมานั่งพักผ่อนชิลๆ ก็เหมาะ หรือจะมาถ่ายก็ดีงามสุดๆ!" },
  { id: 2, name: 'Simply Happy cafe', img: "https://www.ryoiireview.com/upload/article/202111/1636963137_cf5793938b321b67b3b667655b375703.jpg",Tex:"สไตล์โฮมมี่ที่บรรยากาศนั่งสุดๆ ตัวร้านสีขาวบวกกับความเป็นไม้่สีน้ำตาลเข้มฟีลอบอุ่นสุดๆ บริเวณด้านนอกปกคลุมด้วยต้นไม้ใหญ่ พื้นหญ้าสีเขียว" },
  { id: 3, name: 'Polaris Sunrise Café', img: "https://www.ryoiireview.com/upload/article/202304/1681733919_1dc9da5619cecf386917f0533fd4ce31.jpg",Tex:"บรรยากาศดีสไตล์มินิมอล แถมรายล้อมด้วยต้นไม้เขียวขจี บรรยากาศดีมากก ที่นั่งมีทั้งโซน indoor และ outdoor จะมุมไหนก็น่านั่งค่ะ ทั้งต้นไม้ น้ำตก และลำธาร " },
  { id: 4, name: 'Chapter 2WO', img: "https://www.ryoiireview.com/upload/article/202304/1681732353_3374a1e478e443690a89fcfb04c52150.jpg",Tex:"บรรยากาศดีมากก เงียบสงบสุดๆ แถมยังอยู่ใต้ร่มไม้ใหญ่ มานั่งพักผ่อนจิบกาแฟชิลๆ บอกเลยว่าประทับใจแน่นอนค่ะ ในส่วนของเมนูก็หน้าตาดูดี" },
  { id: 5, name: 'MYTH OVEN', img: "https://www.ryoiireview.com/upload/article/202304/1681733535_ceea4fe6aece45f4d4e266a93599e4d0.jpg" ,Tex:"บรรยากาศดีๆ และเมนูอร่อยๆ ร้านนี้จะตกแต่งออกมาแบบเรียบง่าย แต่ดูแล้วอบอุ่นมากๆ เหมาะแก่การมาพักผ่อนทานขนมอร่อยๆ ในแต่ละวันจริงๆ ค่ะ ในส่วนของเมนูจะเน้นเป็นเบเกอรีโฮมเมดอบสดใหม่ทุกๆ เช้าค่ะ"},
  { id: 6, name: 'Nuan cafe & bistro', img: "https://www.ryoiireview.com/upload/article/202304/1681707959_4a870111f80d82cea86ea6a0a43a04e5.jpg",Tex:"คาเฟ่บรรยากาศอบอุ่นที่เปิดบริการอยู่ในบ้านไม้สีขาวสไตล์วินเทจ เมนูที่ร้านมีทั้งเครื่องดื่มและเบเกอรีโฮมเมดค่ะ บอกเลยว่าน่าทานมากๆ" }
]);

</script>
<template>
 <!-- Coffee Products -->
 <div class="bg-body-tertiary me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden">
    <div class="my-3 p-3">
    <RouterLink to="/" style ="font-family: 'Itim', cursive;" class="btn-back">Back </RouterLink >
    <h2 class="display-5">{{ CoffeeList[id - 1].name }}</h2>
      <p class="lead">cafe {{ id }}</p>
    </div>
    <div class="bg-dark shadow-sm mx-auto" style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;">
      <img :src="CoffeeList[id - 1].img" width="450" height="300" style="margin-top: 10px;" />
    </div> <br> <br>
    {{ CoffeeList[id - 1].Tex }}
 <br> <br> <br> </div> 
  </template>
  


<style>
@import url('https://fonts.googleapis.com/css2?family=Itim&family=Mali&family=Mooli&family=Nunito:wght@500&family=Roboto+Slab&display=swap');

.btn-back {
 margin-right: 90%;
 display: inline-block;
 padding: 0.5rem 1.8rem;
 font-size: 16px;
 font-weight: 700;
 color: rgb(0, 0, 0);
 border: 3px solid rgb(249, 8, 48);
 cursor: pointer;
 position: relative;
 background-color: transparent;
 text-decoration: none;
 overflow: hidden;
 z-index: 1;
 font-family: inherit;
 border-radius: 20px;
}

.btn-back::before {
 content: "";
 position: absolute;
 left: 0;
 top: 0;
 width: 100%;
 height: 100%;
 background-color: rgb(211, 28, 89);
 transform: translateX(-100%);
 transition: all .5s;
 z-index: -1;
}

.btn-back:hover::before {
 transform: translateX(0);
}
.container {
  max-width: 960px;
}

.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(222, 80, 146, 0.85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #643400;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #643400;
  text-decoration: none;
}


.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #db0187;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #db0187;
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