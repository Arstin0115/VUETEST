<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import NavbarDefault from "../..//examples/navbars/NavbarDefault.vue";
// import DefaultFooter from "../../examples/footers/FooterDefault.vue";
import Header from "../../examples/Header.vue";
import FilledInfoCard from "../../examples/cards/infoCards/FilledInfoCard.vue";
import yelufooter from "../../examples/footers/yelufooter.vue";


//Vue Material Kit 2 components
import MaterialSocialButton from "@/components/MaterialSocialButton.vue";

// sections
import PresentationCounter from "./Sections/PresentationCounter.vue";
import PresentationPages from "./Sections/PresentationPages.vue";
// import PresentationExample from "./Sections/PresentationExample.vue";
// import data from "./Sections/Data/designBlocksData";
import BuiltByDevelopers from "./Components/BuiltByDevelopers.vue";
import PresentationTestimonials from "./Sections/PresentationTestimonials.vue";
import PresentationInformation from "./Sections/PresentationInformation.vue";

//images
// import vueMkHeader from "@/assets/img/vue-mk-header.jpg";
import bg02 from "@/assets/img/bg/bg02.jpg";
import wavesWhite from "@/assets/img/waves-white.svg";
import logoBootstrap from "@/assets/img/logos/bootstrap5.jpg";
import logoTailwind from "@/assets/img/logos/icon-tailwind.jpg";
import logoVue from "@/assets/img/logos/vue.jpg";
import logoAngular from "@/assets/img/logos/angular.jpg";
import logoReact from "@/assets/img/logos/react.jpg";
import logoSketch from "@/assets/img/logos/sketch.jpg";

//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <Header>
    <!-- 首頁圖片/文字在這設定 -->
    <div
      class="page-header min-vh-75"
      :style="`background-image: url(${bg02})`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative">
            <h1
              class="text-white pt-3 mt-n5 me-2"
              :style="{ display: 'inline-block ' }"
            >
            YELU CAMP露營GO!
            </h1>
            <p class="lead text-white px-5 mt-3" :style="{ fontWeight: '500' }">
            #Camping #Glamping #Recreational vehicles #享受生活</p>
            <p class="lead text-white px-5 mt-3" :style="{ fontWeight: '500' }">
              山間秘境旅遊的極致享受，體驗自然，仰望星空、山嵐，聆聽蟲鳴鳥叫</p>
            
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <!-- import進來呈現的視覺 先後順序在這裡設定 -->
    <PresentationCounter />
    <PresentationPages />
    

    <div class="container">
      <div class="col-lg-6 mx-auto text-center mt-6">
          <h2 class="mb-0">行程選擇</h2>
          <!-- <h2 class="text-gradient text-warning  mb-3">
           Enjoy Your Camp
          </h2> -->
          <p class="lead">
            Many Fortune 500 companies, startups.
          </p>
        </div>
      <div class="row mt-6"> 
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-warning ' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="Getting Started"
            description="Check the possible ways of working with our product and the necessary files for building your own project."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/overview/material-kit/',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-warning ' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="Getting Started"
            description="Check the possible ways of working with our product and the necessary files for building your own project."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/overview/material-kit/',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
        <div class="col-lg-4">
          <FilledInfoCard
            class="p-4"
            :color="{ text: 'white', background: 'bg-gradient-warning ' }"
            :icon="{ component: 'flag', color: 'white' }"
            title="Getting Started"
            description="Check the possible ways of working with our product and the necessary files for building your own project."
            :action="{
              route:
                'https://www.creative-tim.com/learning-lab/vue/overview/material-kit/',
              label: { text: 'Let\'s start', color: 'white' }
            }"
          />
        </div>
      </div>
    </div>

  <!-- 活動 -->
    <PresentationInformation />
  <!-- 商店 -->
     <PresentationTestimonials />
  
    <!-- <div
      class="container-fluid mt-sm-5 border-radius-xl">
      <div
        class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
        :style="{
          backgroundImage: `url(${wavesWhite})`
        }"
        loading="lazy"
      >
        <span class="mask bg-warning "></span>
        <div class="container">
          <div class="row">
            <div class="d-flex justify-content-center p-5">
              
            </div>
          </div>
        </div>
      </div>
    </div> -->

   
  </div>
  <!-- <DefaultFooter /> -->
  <yelufooter/>
</template>
