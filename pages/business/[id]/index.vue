<template>
  <main>
    <section
      class="slider_main relative lg:h-[450px] md:h-[400px] sm:h-[380px] h-[340px] rounded-[20px] bg-[#F4F3F9]"
    >
      <img
        class="absolute top-0 left-0"
        src="@/assets/svg/slide_top.svg"
        alt=""
      />
      <div
        class="slider flex items-center justify-between w-full lg:px-10 md:px-10 sm:px-5 h-full"
      >
        <div class="md:block hidden lg:space-y-3 sm:space-y-2 z-10">
          <h1 class="lg:text-[40px] md:text-[32px] text-[28px] font-bold">
            Bombay Spice
          </h1>
          <p class="lg:text-[16px] text-[16px] line-clamp-1 font-semibold">
            999 Upper james, Hamilton, ON
          </p>
          <p class="lg:text-[18px] text-[12px] line-clamp-1 font-medium">
            Monday - Friday: 9:00 a.m to 9.00 p.m
          </p>
          <p class="lg:text-[18px] text-[12px] line-clamp-1 font-medium">
            Saturday & Sunday: 9:00 a.m to 6.00 p.m
          </p>

          <div>
            <button
              class="flex items-center gap-2 bg-black sm:mt-5 mt-2 text-white lg:text-[22px] md:text-lg text-sm font-medium px-6 rounded-xl lg:h-[56px] md:h-[48px] h-10"
            >
              <img src="@/assets/svg/white_phone.svg" alt="" />
              +1 365 888 4444
            </button>
            <button
              class="bg-black sm:mt-5 mt-2 text-white lg:text-[22px] md:text-lg text-sm font-medium px-[58px] rounded-xl lg:h-[56px] md:h-[48px] h-10"
            >
              Get direction
            </button>
          </div>
        </div>
        <div
          class="flex sm:justify-end w_full md:mx-0 mx-auto slider_images lg:gap-6 gap-4 z-10"
        >
          <div class="main_images block space-y-[21px]">
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] w-[90px]"
              src="@/assets/images/slide1.png"
              alt=""
            />
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] w-[90px]"
              src="@/assets/images/slide2.png"
              alt=""
            />
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] w-[90px]"
              src="@/assets/images/slide3.png"
              alt=""
            />
          </div>
          <img
            class="image_slider object-cover rounded-[12px] lg:h-[360px] md:h-[340px] h-[340px] lg:w-[270px] w-[250px] w_full"
            src="@/assets/images/slide.png"
            alt=""
          />
        </div>
      </div>
    </section>
    <div class="justify-between mt-[6px] main_images2 hidden space-x-[21px]">
      <img
        class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] md:w-[90px] sm:w-[110px]"
        src="@/assets/images/slide1.png"
        alt=""
      />
      <img
        class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] md:w-[90px] sm:w-[110px]"
        src="@/assets/images/slide2.png"
        alt=""
      />
      <img
        class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] md:w-[90px] sm:w-[110px]"
        src="@/assets/images/slide3.png"
        alt=""
      />
    </div>
    <div class="md:hidden block lg:space-y-3 sm:mt-5 mt-3 sm:space-y-2 z-10">
      <h1 class="lg:text-[40px] md:text-[32px] text-[28px] font-bold">
        Bombay Spice
      </h1>
      <p class="lg:text-[24px] text-[20px] font-semibold">
        999 Upper james, Hamilton, ON
      </p>
      <p class="lg:text-[24px] text-[16px] font-medium">
        Monday - Friday: 9:00 a.m to 9.00 p.m
      </p>
      <p class="lg:text-[24px] text-[16px] font-medium">
        Saturday & Sunday: 9:00 a.m to 6.00 p.m
      </p>

      <div class="sm:flex gap-5">
        <button
          class="flex items-center gap-2 bg-black sm:mt-5 mt-2 text-white lg:text-[22px] md:text-lg text-sm font-medium px-6 rounded-xl lg:h-[66px] md:h-[56px] h-10"
        >
          <img src="@/assets/svg/white_phone.svg" alt="" />
          +1 365 888 4444
        </button>
        <button
          class="bg-black sm:mt-5 mt-2 text-white lg:text-[22px] md:text-lg text-sm font-medium px-[50px] rounded-xl lg:h-[66px] md:h-[56px] h-10"
        >
          Get direction
        </button>
      </div>
    </div>

    <section class="mt-10">
      <Swiper
        @slide-change-transition-end="setThumbsSwiper"
        class="rounded-[20px] swiper-container"
        :modules="[SwiperAutoplay, SwiperEffectCreative]"
        :slides-per-view="1"
        :loop="true"
        :effect="'creative'"
        spaceBetween="30"
        :centeredSlides="true"
        :autoplay="{
          delay: 4000,
          disableOnInteraction: false,
        }"
        :creative-effect="{
          prev: {
            shadow: false,
            translate: ['-50%', 0, -1],
          },
          next: {
            translate: ['100%', 0, 0],
          },
        }"
      >
        <SwiperSlide v-for="i in 5">
          <img
            class="w-full lg:h-[540px] md:h-[450px] sm:h-[350px] h-[240px] object-contain bg-[#F4F3F9] rounded-[20px]"
            src="@/assets/images/flyer.png"
            alt=""
          />
        </SwiperSlide>
      </Swiper>
      <ul
        class="flex justify-center md:mt-3 mt-1 mb-10 items-center md:gap-8 gap-4"
      >
        <li class="md:h-4 md:w-4 h-2 w-2 rounded-full bg-[#000]"></li>
        <li class="md:h-4 md:w-4 h-2 w-2 rounded-full bg-[#939393]"></li>
        <li class="md:h-4 md:w-4 h-2 w-2 rounded-full bg-[#939393]"></li>
      </ul>
    </section>
  </main>
</template>

<script setup></script>

<style lang="scss" scoped>
@media (max-width: 400px) {
  .main_images {
    display: none;
  }

  .main_images2 {
    display: flex;
  }

  .w_full {
    width: 100%;
  }
}
</style>
