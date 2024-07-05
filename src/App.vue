<script>
import ProfileMobile from "./components/ProfileMobile.vue";
import ProfileDesktop from "./components/ProfileDesktop.vue";
import Footer from "./components/Footer.vue";
export default {
  data() {
    return {
      showShareMobile: false,
      showShareDesktop: false,
    };
  },
  components: {
    ProfileMobile,
    ProfileDesktop,
    Footer,
  },
};
</script>

<template>
  <main class="py-[74px] bg-lightGrayishBlue md:py-[260px]">
    <div class="w-[87%] mx-auto max-w-[729px] flex flex-col md:flex-row">
      <div
        class="w-full md:basis-[285px] md:shrink-0 rounded-[12px_12px_0_0] overflow-hidden md:rounded-[12px_0_0_12px]"
      >
        <img
          class="h-[200px] object-[50%_26%] object-cover md:h-full w-full md:object-[2%_26%]"
          src="./assets/drawers.jpg"
          alt="drawers"
        />
      </div>
      <div>
        <div
          class="p-[35px_32px_19px_33px] bg-white md:p-[33px_32px_9px_40px] md:rounded-[0_12px_0_0]"
        >
          <p
            class="font-manrope font-extrabold text-[16px] text-veryDarkGrayishBlue md:text-[20px] md:leading-7"
          >
            Shift the overall look and feel by adding these wonderful touches to
            furniture in your home
          </p>
          <p
            class="text-[14.6px] [word-spacing:-2px] leading-5 mt-[13px] ps-[0px] pe-[2px] text-desaturatedDarkBlue md:text-[14px] md:mt-[11px] md:[word-spacing:-0.6px]"
          >
            Ever been in a room and felt like something was missing? Perhaps it
            felt slightly bare and uninviting. I&rsquo;ve got some simple tips
            to help you make any room feel complete.
          </p>
        </div>
        <ProfileMobile
          class="md:hidden rounded-[0_0_12px_12px]"
          :showShareMobile="showShareMobile"
          @changeShowShare="showShareMobile = !showShareMobile"
        />
        <ProfileDesktop
          class="hidden md:flex md:rounded-[0_0_12px_0]"
          :showShareDesktop="showShareDesktop"
          @changeShowShare="showShareDesktop = !showShareDesktop"
        />
      </div>
    </div>
  </main>
  <Footer />
</template>
