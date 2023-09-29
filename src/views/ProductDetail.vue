<script setup>
import{ ref } from "vue";

const CoffeeList = ref([
    { id: 1, name: 'Treespresso cafe', img: "https://www.ryoiireview.com/upload/article/202304/1681731156_d018557a4a10aed6c8f450ad0db6d60d.jpg" },
    { id: 2, name: 'Simply Happy cafe', img: "https://www.ryoiireview.com/upload/article/202111/1636963137_cf5793938b321b67b3b667655b375703.jpg" },
    { id: 3, name: 'Polaris Sunrise Café', img: "https://www.ryoiireview.com/upload/article/202304/1681733919_1dc9da5619cecf386917f0533fd4ce31.jpg" },
    { id: 4, name: 'Chapter 2WO', img: "https://www.ryoiireview.com/upload/article/202304/1681732353_3374a1e478e443690a89fcfb04c52150.jpg" },
    { id: 5, name: 'MYTH OVEN', img: "https://www.ryoiireview.com/upload/article/202304/1681733535_ceea4fe6aece45f4d4e266a93599e4d0.jpg" },
    { id: 6, name: 'Nuan cafe & bistro', img: "https://www.ryoiireview.com/upload/article/202304/1681707959_4a870111f80d82cea86ea6a0a43a04e5.jpg" }
  ]);

</script>
<template>
    <!-- Coffee Products -->
    <div class="bg-body-tertiary me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden"
      v-for="(coffee, index) in CoffeeList"
      :key="index" >
      <div class="12">
        <h2 class="display-5">{{ coffee.name }}</h2>
        <p class="lead">cafe {{ index+1 }}</p>
        <br>
      </div>
      <div
        class="bg-dark shadow-sm mx-auto"
        style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;"
      >
        <img :src="coffee.img" width="450" height="300" style="margin-top: 10px;" />
      </div>
      <div class="d-flex gap-2 justify-content-center py-5">
        <RouterLink :to="{name:'coffee', params: {id: coffee.id }}" class="button" type="button" style="font-family: 'Itim', cursive;">
          จองโต๊ะ 
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            fill="currentColor"
            class="bi bi-arrow-right"
            viewBox="0 1 16 16"
          >
            <path
              fill-rule="evenodd"
              d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8z"
            />
          </svg>
        </RouterLink>
      </div>
    </div>
  </template>
  


<style>

@import url('https://fonts.googleapis.com/css2?family=Itim&family=Mali&family=Mooli&family=Nunito:wght@500&family=Roboto+Slab&display=swap');
.button {
 --color: #e11b74;
 padding: 0.8em 1.7em;
 background-color: transparent;
 border-radius: .3em;
 position: relative;
 overflow: hidden;
 cursor: pointer;
 transition: .5s;
 font-weight: 400;
 font-size: 17px;
 border: 1px solid;
 font-family: inherit;
 text-transform: uppercase;
 color: var(--color);
 z-index: 1;
}

.button::before, .button::after {
 content: '';
 display: block;
 width: 50px;
 height: 50px;
 transform: translate(-50%, -50%);
 position: absolute;
 border-radius: 50%;
 z-index: -1;
 background-color: var(--color);
 transition: 1s ease;
}

.button::before {
 top: -1em;
 left: -1em;
}

.button::after {
 left: calc(100% + 1em);
 top: calc(100% + 1em);
}

.button:hover::before, .button:hover::after {
 height: 410px;
 width: 410px;
}

.button:hover {
 color: rgb(255, 251, 251);
 font-weight: bold;
 font-family: 'Itim', cursive;
}

.button:active {
 filter: brightness(.8);
}

.container {
  max-width: 960px;
}

.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(8, 8, 8, 0.85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #f06800;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #dd0088;
  text-decoration: none;
}

.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #b6004f;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #b6004f;
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