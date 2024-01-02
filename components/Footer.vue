<template>
  <div class="md:pb-0 pb-16">
    <section class="flex justify-center gap-5 mx-auto md:mt-[60px] mt-10">
      <div class="lg:block hidden space-y-5">
        <!-- contact info -->
        <div class="bg-[#F4F3F9] p-10 rounded-[10px] max-w-[545px]">
          <h1 class="text-[32px] font-bold">Contact information</h1>
          <div class="text-lg">
            <div class="grid grid-cols-2 mt-9">
              <div>
                <h1 class="flex items-center gap-2 mb-[22px]">
                  <img src="@/assets/contact/phone.svg" alt="" />
                  <p class="text-lg font-medium">Phone</p>
                </h1>
                <div class="space-y-3">
                  <p>+123 456 789 101</p>
                  <p>+321 101 987 654</p>
                </div>
              </div>
              <div>
                <h1 class="flex items-center gap-2 mb-[22px]">
                  <img src="@/assets/contact/email.svg" alt="" />
                  <p class="text-lg font-medium">E-mail</p>
                </h1>
                <div>
                  <p>contact@localbiz.com</p>
                </div>
              </div>
            </div>
            <div class="grid grid-cols-2 mt-9">
              <div>
                <h1 class="flex items-center gap-2 mb-[22px]">
                  <img src="@/assets/contact/location.svg" alt="" />
                  <p class="text-lg font-medium">Address</p>
                </h1>
                <div>
                  <p class="w-[154px]">
                    123 Main Street San Francisco, CA 94103
                  </p>
                </div>
              </div>
              <div>
                <h1 class="flex items-center gap-2 mb-[22px]">
                  <img src="@/assets/contact/connect.svg" alt="" />
                  <p class="text-lg font-medium">Connect with</p>
                </h1>
                <div class="flex items-center gap-2">
                  <img src="@/assets/contact/instagram.svg" alt="" />
                  <img src="@/assets/contact/twitter.svg" alt="" />
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- location -->
        <img src="@/assets/svg/locations.svg" alt="" />
      </div>
      <!-- Send message -->
      <div class="sm:w-[445px] w-full mx-5 bg-black rounded-[10px] text-white md:p-8 p-5">
        <h1 class="md:text-[36px] text-[24px] font-bold whitespace-nowrap">
          Send Us a Message
        </h1>
        <form class="md:space-y-9 space-y-6 md:mt-9 mt-6">
          <div class="grid md:grid-cols-2 md:gap-5">
            <div class="md:space-y-3 space-y-[10px]">
              <label class="block md:text-xl text-[16px] font-medium" for="name"
                >First name</label
              >
              <input
                class="border-b w-full md:text-[16px] text-sm border-white bg-transparent !rounded-none !p-0 !pb-3 !h-auto"
                type="text"
                placeholder="First name"
              />
            </div>
            <div class="md:space-y-3 space-y-[10px] md:mt-0 mt-6">
              <label class="block md:text-xl text-[16px] font-medium" for="name"
                >Last name</label
              >
              <input
                class="border-b w-full md:text-[16px] text-sm border-white bg-transparent !rounded-none !p-0 !pb-3 !h-auto"
                type="text"
                placeholder="Last name"
              />
            </div>
          </div>
          <div class="md:space-y-3 space-y-[10px]">
            <label class="block md:text-xl text-[16px] font-medium" for="name"
              >E-mail</label
            >
            <input
              class="border-b w-full md:text-[16px] text-sm border-white bg-transparent !rounded-none !p-0 !pb-3 !h-auto"
              type="text"
              placeholder="example@gmail.com"
            />
          </div>
          <div class="md:space-y-3 space-y-[10px]">
            <label class="block md:text-xl text-[16px] font-medium" for="name"
              >Message</label
            >
            <textarea
              class="border resize-none md:text-[16px] text-sm w-full md:h-[150px] h-[120px] rounded-[10px] border-white bg-transparent p-[10px]"
              type="text"
              placeholder="Type your message here"
            />
          </div>
          <button
            class="md:h-14 h-10 md:!mt-20 !mt-[60px] w-full text-black md:text-lg text-[16px] font-medium bg-[#F4F3F9] rounded-[10px]"
          >
            Send
          </button>
        </form>
      </div>
    </section>
    <div class="bg-[#F4F3F9] mt-10">
      <footer
        class="sm:flex hidden justify-between text-lg font-medium container md:p-10 p-5 !pb-20 mx-auto"
      >
        <div>
          <router-link to="/"><img src="/logo.svg" /></router-link>
          <p class="text-black/40 mt-3 text-sm font-medium w-[135px]">
            2021 A@ LocalBiz. All rights reserved.
          </p>
        </div>
        <ul class="space-y-6">
          <li>Home</li>
          <li>Pricing</li>
          <li>About us</li>
          <li>Contact</li>
        </ul>
        <ul class="space-y-6">
          <li>Facebook</li>
          <li>Instagram</li>
          <li>Twitter</li>
          <li>Linkedin</li>
        </ul>
        <ul class="space-y-6">
          <li>Privacy Policy</li>
          <li>Terms Of Service</li>
        </ul>
      </footer>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
