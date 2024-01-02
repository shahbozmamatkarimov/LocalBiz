<template>
  <main>
    <section
      class="slider_main relative lg:h-[450px] md:h-[400px] sm:h-[380px] h-[240px] rounded-[20px] bg-[#F4F3F9]"
    >
      <img
        class="absolute top-0 left-0"
        src="@/assets/svg/slide_top.svg"
        alt=""
      />
      <div
        class="slider flex items-center justify-between lg:px-[100px] md:px-10 px-5 lg:gap-[320px] h-full"
      >
        <div class="title_slider lg:space-y-3 sm:space-y-2 z-10">
          <h1 class="lg:text-[20px] text-[16px] font-medium">Product name</h1>
          <p class="lg:text-[30px] md:text-[24px] text-[20px] font-semibold">
            50$
          </p>
          <p class="lg:text-[40px] md:text-[32px] text-[28px] font-bold">
            Bombay Spice
          </p>
          <div>
            <button
              class="bg-black sm:mt-5 mt-2 text-white lg:text-[22px] md:text-lg text-sm font-medium px-10 rounded-xl lg:h-[66px] md:h-[56px] h-10"
            >
              Explore more
            </button>
          </div>
        </div>
        <div class="flex slider_images lg:gap-6 gap-4">
          <div class="md:block hidden space-y-[21px]">
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] lg:w-[90px] w-[70px]"
              src="@/assets/images/slide1.png"
              alt=""
            />
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] lg:w-[90px] w-[70px]"
              src="@/assets/images/slide2.png"
              alt=""
            />
            <img
              class="object-cover rounded-[6px] lg:h-[106px] h-[99.5px] lg:w-[90px] w-[70px]"
              src="@/assets/images/slide3.png"
              alt=""
            />
          </div>
          <img
            class="image_slider object-cover rounded-[12px] lg:h-[360px] md:h-[340px] h-[220px] lg:w-[270px] md:w-[250px] w-[170px]"
            src="@/assets/images/slide.png"
            alt=""
          />
        </div>
      </div>
    </section>

    <section>
      <h1
        class="md:text-[40px] text-[24px] md:mt-[60px] mt-5 md:mb-6 mb-3 whitespace-nowrap font-bold"
      >
        Explore Local Businesses
      </h1>
      <div class="flex items-center justify-between">
        <div class="flex text-sm w-full">
          <input
            class="lg:w-[70%] w-[80%]"
            type="text"
            placeholder="Search for local products and services"
          />
          <div
            class="flex items-center -ml-5 h-[46px] bg-[#F4F3F9] pr-5 pl-4 rounded-r-[10px]"
          >
            <img src="@/assets/svg/search.svg" alt="" />
          </div>
        </div>
        <div class="lg:flex hidden gap-5">
          <el-dropdown>
            <div class="flex text-sm min-w-[170px]">
              <input type="text" placeholder="Sort by Category" />
              <div
                class="flex items-center -ml-5 sm:h-[46px] !h-10 bg-[#F4F3F9] pr-5 pl-4 rounded-r-[10px]"
              >
                <img
                  class="min-w-[16px]"
                  src="@/assets/svg/select_arrow.svg"
                  alt=""
                />
              </div>
            </div>
            <template #dropdown>
              <el-dropdown-menu class="w-[229px]">
                <el-dropdown-item>Action 1</el-dropdown-item>
                <el-dropdown-item>Action 2</el-dropdown-item>
                <el-dropdown-item>Action 3</el-dropdown-item>
                <el-dropdown-item>Action 4</el-dropdown-item>
                <el-dropdown-item>Action 5</el-dropdown-item>
              </el-dropdown-menu>
            </template>
          </el-dropdown>
          <el-dropdown>
            <div class="flex text-sm min-w-[170px]">
              <input type="text" placeholder="Sort by Category" />
              <div
                class="flex items-center -ml-5 h-[46px] bg-[#F4F3F9] pr-5 pl-4 rounded-r-[10px]"
              >
                <img
                  class="min-w-[16px]"
                  src="@/assets/svg/select_arrow.svg"
                  alt=""
                />
              </div>
            </div>
            <template #dropdown>
              <el-dropdown-menu class="w-[229px]">
                <el-dropdown-item>Action 1</el-dropdown-item>
                <el-dropdown-item>Action 2</el-dropdown-item>
                <el-dropdown-item>Action 3</el-dropdown-item>
                <el-dropdown-item>Action 4</el-dropdown-item>
                <el-dropdown-item>Action 5</el-dropdown-item>
              </el-dropdown-menu>
            </template>
          </el-dropdown>
        </div>
        <button
          class="lg:hidden flex items-center justify-center sm:h-[46px] sm:min-w-[46px] h-10 min-w-[40px] rounded-[5px] bg-[#F4F3F9]"
        >
          <img src="@/assets/svg/filter.svg" alt="" />
        </button>
      </div>
      <!-- filters result -->
      <div class="flex gap-2 mt-5 mb-6 items-center flex-wrap">
        <p
          v-for="i in 5"
          class="flex sm:text-[16px] text-sm gap-2 items-center px-[14px] sm:h-8 h-6 whitespace-nowrap border border-[#027DFC] rounded-full"
        >
          Flowers
          <img
            class="hover:bg-[#F4F3F9] sm:w-6 sm:h-6 h-4 w-4 cursor-pointer rounded-full sm:p-1 p-0.5 -mr-1"
            src="@/assets/svg/blue_x.svg"
            alt=""
          />
        </p>
      </div>
    </section>

    <section class="grid_cards">
      <div
        v-for="i in 8"
        @click="$router.push('/business/' + i)"
        class="flex cursor-pointer sm:block gap-3 sm:mb-0 mb-[10px] bg-[#F8F8F8] sm:mx-auto sm:space-y-[11px] p-[10px] sm:pb-5 rounded-[10px] sm:w-[280px]"
      >
        <img
          class="sm:w-[260px] sm:h-[260px] w-[120px] h-[120px] rounded-[10px]"
          src="@/assets/images/card.png"
          alt=""
        />
        <div class="relative sm:space-y-[11px] space-y-[6px]">
          <h1
            class="sm:text-lg text-[16px] leading-4 line-clamp-1 font-medium -mt-0.5"
          >
            Comfortable armchair
          </h1>
          <p class="sm:text-lg text-[16px] font-bold line-clamp-1 leading-4">
            Grocery Store
          </p>
          <p
            class="sm:text-[16px] text-sm h-[32px] line-clamp-2 leading-4 w-[90%]"
          >
            999 Upper james, Hamilton, ON 999 Upper james, Hamilton, ON 999
            Upper james, Hamilton, ON 999 Upper james, Hamilton, ON
          </p>
          <div class="flex items-center justify-between">
            <p></p>
            <div class="flex gap-4">
              <button
                class="sm:relative absolute right-0 bottom-0 flex items-center gap-1 bg-white py-0.5 px-2 rounded-full"
              >
                <img
                  class="w-5 h-5 hover:scale-125 duration-500"
                  src="@/assets/svg/heart.svg"
                  alt=""
                />
                <p
                  class="sm:text-[24px] text-[20px] font-medium -mt-0.5 leading-[16px]"
                >
                  16
                </p>
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>
    <button
      class="md:mt-[10px] mt-[5px] w-full mx-auto sm:h-14 h-10 rounded-[10px] font-medium sm:text-lg text-sm bg-[#F4F3F9]"
    >
      Show more
    </button>
  </main>
</template>

<script></script>

<style lang="scss" scoped>
@media (min-width: 640px) {
  .grid_cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    grid-gap: 24px;
  }
}

@media (max-width: 500px) {
  .title_slider {
    position: absolute;
    padding: 20px;
  }

  .slider_images {
    width: 100%;
  }

  .image_slider {
    width: 100%;
    height: 240px;
  }

  .slider {
    padding: 0;
  }
}

@media (max-width: 440px) {
  .slider,
  .slider_main,
  .image_slider {
    max-height: 200px;
  }
}

@media (max-width: 380px) {
  .slider,
  .slider_main,
  .image_slider {
    max-height: 180px;
  }
}
</style>
