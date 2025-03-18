<template>
    <div class="text-white bg-black">
        <section class="max-w-screen-xl px-4 pb-12 mx-auto">
      <h2
        class="text-3xl sm:text-[40px] bg-[#111] relative z-10 font-bold px-4 py-2 w-max mx-auto text-center text-[#1788ae] sm:border-2 border-[#1788ae] rounded-md"
      >
        Let's Connect
      </h2>
      <div class="flex flex-col items-center mt-10 md:flex-row">
        <div class="w-full">
          <img src="../assets/images/contact.png" alt="phone" />
        </div>
        <form action="https://formsubmit.co/4a9f5993e6393322b5e1b3410aab49bf" method="POST" class="w-full" name="contactUS">
          <input type="hidden" name="_captcha" value="false"> <!-- Disables CAPTCHA -->
          <input type="hidden" name="_next" value="http://localhost:5173"> <!-- Redirects to the same page -->
          <label
            for="name"
            class="block mb-2 text-sm font-medium text-white"
            >Name</label
          >
          <div class="relative mb-4">
            <div
              class="absolute inset-y-0 start-0 flex items-center ps-3.5 pointer-events-none"
            >
              <svg  
                class="w-4 h-4 text-gray-400"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  d="M10 0a10 10 0 1 0 10 10A10.011 10.011 0 0 0 10 0Zm0 5a3 3 0 1 1 0 6 3 3 0 0 1 0-6Zm0 13a8.949 8.949 0 0 1-4.951-1.488A3.987 3.987 0 0 1 9 13h2a3.987 3.987 0 0 1 3.951 3.512A8.949 8.949 0 0 1 10 18Z"
                />
              </svg>
            </div>
            <input
              type="text"
              id="name"
              name="name"
              required
              class="border-2 outline-none text-sm rounded-lg focus:ring-[#1788ae] focus:border-[#1788ae] block w-full ps-10 p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
              placeholder="Enter your name"
            />
          </div>
          <label
            for="email"
            class="block mb-2 text-sm font-medium text-white"
            >Your Email</label
          >
          <div class="relative mb-4">
            <div
              class="absolute inset-y-0 start-0 flex items-center ps-3.5 pointer-events-none"
            >
              <svg
                class="w-4 h-4 text-gray-400"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 16"
              >
                <path
                  d="m10.036 8.278 9.258-7.79A1.979 1.979 0 0 0 18 0H2A1.987 1.987 0 0 0 .641.541l9.395 7.737Z"
                />
                <path
                  d="M11.241 9.817c-.36.275-.801.425-1.255.427-.428 0-.845-.138-1.187-.395L0 2.6V14a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V2.5l-8.759 7.317Z"
                />
              </svg>
            </div>
            <input
              type="text"
              id="email"
              name="email"
              required
              class="border-2 outline-none   text-sm rounded-lg focus:ring-[#1788ae] focus:border-[#1788ae] block w-full ps-10 p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
              placeholder="name@gmail.com"
            />
          </div>
          <label
            for="message"
            class="block mb-2 text-sm font-medium text-white"
            >Message</label
          >
          <div class="relative mb-4">
            <div
              class="absolute inset-y-0 start-0 flex items-center ps-3.5 pointer-events-none"
            ></div>
            <textarea
              id="message"
              name="message"
              required
              rows="8"
              class="border-2 outline-none text-sm rounded-lg focus:ring-[#1788ae] focus:border-[#1788ae] block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white"
            ></textarea>
          </div>
          <button
            type="submit"
            class="w-full text-white bg-[#1788ae] hover:bg-[#1280a4] focus:ring-4 focus:ring-[#4489a0] font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 focus:outline-none"
          >
            Send
          </button>
        </form>
      </div>
    </section>
    </div>
</template>

<script>
export default {
    name: 'ContactComponent',
    data() {
        return {
            // Add your component data here
        };
    },
    methods: {
        // Add your component methods here
    }
};
</script>