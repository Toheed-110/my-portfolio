<script setup>
</script>


<template>
  <section class="text-white mt-20" id="contact">
    <h2 class="text-4xl font-bold text-white text-left mb-4 px-4 xl:pl-16">Let's Connect</h2>
    <div class="grid md:grid-cols-2 gap-4 relative px-4 xl:px-16 mt-8" data-aos="zoom-in-up">
      <div>
        <p class="text-[#adb7be]">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo natus distinctio
          voluptate
          ad eum ipsa provident necessitatibus cum assumenda. Saepe, ipsa. Totam, exercitationem tenetur! Nihil quod
          error
          labore nam doloribus.
        </p>
        <div class="col-lg-4 col-md-4 mb-lg-0 mt-5">
          <div class="flex mb-10 items-center">
            <div class="p-2"
              style="background-color: #111a3e; width: 50px;height: 46px;display: flex;justify-content: center;border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
              <img src="https://img.icons8.com/metro/500/ffffff/new-post.png" alt="new post" class="w-6">
            </div>
            <div class="ml-5 text-white">
              <h4>Email</h4>
              <p>toheedulhaq12@gmail.com</p>
            </div>
          </div>
          <div class="flex mb-10 items-center">
            <div class="p-2"
              style="background-color: #111a3e; width: 50px;height: 46px;display: flex;justify-content: center;border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
              <img src="https://img.icons8.com/ios-filled/500/ffffff/phone.png" alt="phone" class="w-6">
            </div>
            <div class="ml-5 text-white">
              <h4>Phone</h4>
              <p>+923157065512</p>
            </div>
          </div>
          <div class="flex mb-10 items-center">
            <div class="p-2"
              style="background-color: #111a3e; width: 50px;height: 46px;display: flex; justify-content: center;border-radius: 50%;
                    overflow: hidden;border: 1px solid#111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
              <img src="https://img.icons8.com/ios-filled/500/ffffff/linkedin.png" alt="linkedin" class="w-6">
            </div>
            <div class="ml-5 text-white">
              <h4>LinkedIn</h4>
              <p>www.linkedin.com</p>
            </div>
          </div>
        </div>
      </div>
      <div
        style="background-color: #111a3e; width: 100%;height: 100%;border-radius: 20px;
                     overflow: hidden;border: 1px solid #111a3e;backdrop-filter: blur(9px);-webkit-backdrop-filter: blur(9px);">
        <form class="flex flex-col p-2" data-aos="zoom-in-up">
          <div class="mb-6">
            <label for="email" class="text-white block text-sm font-medium mb-2">Email</label>
            <input type="email" id="email"
              class="bg-[#111827] placeholder:[#9CA2A9] w-full text-gray-100 text-sm rounded-lg p-2.5"
              placeholder="toheedulhaq12@gmail.com" name="email">
          </div>
          <div class="mb-6">
            <label for="subject" class="text-white block text-sm font-medium mb-2">Subject</label>
            <input type="subject" id="subject"
              class="bg-[#111827] placeholder:[#9CA2A9] w-full text-gray-100 text-sm rounded-lg p-2.5"
              placeholder="subject" name="email">
          </div>
          <div class="mb-6">
            <label for="message" class="text-white block text-sm font-medium mb-2">Message</label>
            <textarea id="Message"
              class="bg-[#111827] placeholder:[#9CA2A9] w-full text-gray-100 text-sm rounded-lg p-2.5"
              placeholder="Let's talk about ..." name="email"></textarea>
          </div>
          <button
            class="z-1 w-[100%!important] px-6 md:px7 py-3 rounded-full sm:w-max flex justify-center text-white bg-[#FB7E09] border-2 border-transparent">
            Send Message
          </button>
        </form>
      </div>
    </div>
    <div class="bg-gradient-to-tr from-[#570cac] to-[#FB7E09] blur-2xl h-20 w-80 z-0 absolute -top-1/2 -left-4 transform -translate-x-2/3 translate-1/2"></div>
  </section>
</template>