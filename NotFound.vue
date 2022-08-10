<template>
  <div class="relative flex items-center justify-center w-full h-screen bg-[#f3f5f8] overflow-hidden">
    <div class="absolute h-screen right-0 z-10">
      <img src="@/assets/svg/bg-shape.svg" class="h-full" alt="background shape">
    </div>
    <div class="container relative flex flex-col md:flex-row items-center justify-center z-20">
      <div>
        <div class="mb-10 w-4/5 mx-auto md:ml-0">
          <img src="@/assets/svg/404.svg" class="w-full h-full" alt="404">
        </div>
        <!-- <p class="font-medium text-2xl text-[#334055]">{{ $t("forbiddenTitle") }}</p> -->
        <!-- <p class="font-normal text-base text-[#8390A6] -tracking-[0.3]">{{ $t("forbiddenDescription") }}</p> -->
        <p class="font-['Rubik'] font-medium text-2xl text-[#334055] mb-1"> Oh oh oh! I don't think we have such a page
          : (</p>
        <p class="font-['Rubik'] font-normal text-base text-[#8390A6] max-w-[383px] mb-8 -tracking-[0.3]"> This page
          can't be found or deleted. Try later again </p>
      </div>
      <div class="flex items-center justify-center">
        <Vue3Lottie :animationData="forbidden" class="svg-container flex items-center justify-center w-full h-full z-20" />
      </div>
    </div>
  </div>
</template>

<script>
import { Vue3Lottie } from "vue3-lottie";
import "vue3-lottie/dist/style.css";
import * as forbidden from "./Forbidden.json";

export default {
  name: "NotFound",
  components: { Vue3Lottie },
  data() {
    return {
      forbidden
    }
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');

@media (max-width: 768px) {
  .svg-container svg {
    margin-right: 35%;
  }
}
</style>