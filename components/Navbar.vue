<template>
  <nav class="fixed whitespace-nowrap bg-[#F4F3F9] w-full z-50 h-[80px]">
    <div
      class="right-0 left-0 flex justify-between items-center h-[80px] font-medium container md:px-10 px-5 mx-auto"
    >
      <div @click="$router.push('/')" class="cursor-pointer flex items-end gap-2">
        <img v-if="$router.currentRoute.value.name == 'business-id'" src="@/assets/svg/back.svg" alt="">
        <p><img src="/logo.svg" /></p>
      </div>
      <ul class="lg:flex hidden gap-16 -mb-2 text-xl">
        <li>
          <router-link to="/"
            >Home
            <p
              class="hidden bg-[#027DFC] mt-[2px] -mb-[2px] w-[70%] h-[3px]"
            ></p
          ></router-link>
        </li>
        <li>
          <router-link to="/categories">
            Category
            <p
              class="hidden bg-[#027DFC] mt-[2px] -mb-[2px] w-[70%] h-[3px]"
            ></p>
          </router-link>
        </li>
        <li>
          <router-link to="/locations">
            Locations
            <p
              class="hidden bg-[#027DFC] mt-[2px] -mb-[2px] w-[70%] h-[3px]"
            ></p>
          </router-link>
        </li>
      </ul>
      <ul class="flex gap-3">
        <li class="md:block hidden">
          <button
            class="h-10 rounded-[10px] px-10 text-white font-medium bg-black"
          >
            Login
          </button>
        </li>
        <li>
          <button
            class="md:text-[16px] text-xs md:h-10 h-8 rounded-[10px] md:px-10 px-8 text-white font-medium bg-black"
          >
            Sign in
          </button>
        </li>
      </ul>
    </div>

    <ul
      v-if="store.navbar"
      class="xl:hidden !pb-40 flex flex-col container md:py-16 sm:py-10 py-5 md:px-10 px-5 mx-auto overflow-hidden overflow-y-auto bg-white h-[calc(100vh_-_80px)] text-[40px] leading-normal gap-16 text-2xl"
    >
      <li data-aos="fade-left">
        <router-link to="/"
          >Home
          <p class="hidden bg-[#027DFC] mt-[8px] -mb-[8px] w-[70%] h-[3px]"></p
        ></router-link>
      </li>
      <li data-aos="fade-up">
        <router-link to="/services">
          Services
          <p class="hidden bg-[#027DFC] mt-[8px] -mb-[8px] w-[70%] h-[3px]"></p>
        </router-link>
      </li>
      <li data-aos="fade-down">
        <router-link to="/about_us">
          About us
          <p class="hidden bg-[#027DFC] mt-[8px] -mb-[8px] w-[70%] h-[3px]"></p>
        </router-link>
      </li>
      <li data-aos="fade-right" data-duration="500">
        <router-link to="/contact_us">
          Contact us
          <p class="hidden bg-[#027DFC] mt-[8px] -mb-[8px] w-[70%] h-[3px]"></p>
        </router-link>
      </li>
      <li class="sm:hidden block">
        <ul class="flex gap-3 text-[11px]">
          <li class="px-5 py-2 bg-[#E0EBED] rounded-[10px]">
            <img src="@/assets/navbar/lang.svg" />
            <p class="text-center">English</p>
          </li>
          <li class="px-5 py-2 bg-[#E0EBED] rounded-[10px]">
            <img src="@/assets/navbar/heart.svg" />
            <p class="text-center">Likes</p>
          </li>
          <li class="px-5 py-2 bg-[#E0EBED] rounded-[10px]">
            <img src="@/assets/navbar/cart.svg" />
            <p class="text-center">Cart</p>
          </li>
        </ul>
      </li>
    </ul>

    <div
      class="fixed bottom-0 md:hidden flex items-center justify-between w-full px-[10px] bg-white border-t h-[75px]"
    >
      <router-link
        to="/"
        class="flex flex-col text-[#555] items-center justify-center w-16"
      >
        <img class="h-8 w-8 img" src="@/assets/navbar/home.svg" alt="" />
        <img
          class="h-8 w-8 active hidden"
          src="@/assets/navbar/home_active.svg"
          alt=""
        />
        <p>LocalBiz</p>
      </router-link>
      <router-link
        to="/contact"
        class="flex flex-col text-[#555] items-center justify-center w-16"
      >
        <img class="h-8 w-8 img" src="@/assets/navbar/contact.svg" alt="" />
        <img
          class="h-8 w-8 active hidden"
          src="@/assets/navbar/contact_active.svg"
          alt=""
        />
        <p>Contact</p> </router-link
      ><router-link
        to="/favorites"
        class="flex flex-col text-[#555] items-center justify-center w-16"
      >
        <img class="h-8 w-8 img" src="@/assets/navbar/heart.svg" alt="" />
        <img
          class="h-8 w-8 active hidden"
          src="@/assets/navbar/heart_active.svg"
          alt=""
        />
        <p>Favorites</p> </router-link
      ><router-link
        to="/history"
        class="flex flex-col text-[#555] items-center justify-center w-16"
      >
        <img class="h-8 w-8 img" src="@/assets/navbar/watched.svg" alt="" />
        <img
          class="h-8 w-8 active hidden"
          src="@/assets/navbar/watched_active.svg"
          alt=""
        />
        <p>History</p> </router-link
      ><router-link
        to="/profile"
        class="flex flex-col text-[#555] items-center justify-center w-16"
      >
        <img class="h-8 w-8 img" src="@/assets/navbar/profile.svg" alt="" />
        <img
          class="h-8 w-8 active hidden"
          src="@/assets/navbar/profile_active.svg"
          alt=""
        />
        <p>Profile</p>
      </router-link>
    </div>
  </nav>
</template>

<script setup>
const store = reactive({
  navbar: false,
});

const router = useRouter();

watch(
  () => router.currentRoute.value,
  () => {
    store.navbar = false;
  }
);
</script>

<style lang="scss">
ul li {
  cursor: pointer;
}

.router-link-exact-active {
  p {
    display: block;
    color: black;
  }

  .img {
    display: none;
  }

  .active {
    display: block;
  }
}
</style>
