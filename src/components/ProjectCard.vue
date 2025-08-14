<template>
  <div
    class="flex flex-col sm:flex-row gap-4 mt-12 sm:gap-[80px] items-center sm:mt-20 relative"
    :class="{ 'sm:flex-row-reverse': reverse }"
  >
    <!-- Horizontal Line & Dot -->
    <div
      class="h-[1px] bg-[#1788ae] absolute top-1/2 hidden sm:block"
      :class="linePosition"
    ></div>
    <div
      class="w-4 h-4 rounded-full absolute left-1/2 -translate-x-1/2 bg-[#111] z-10 hover:scale-110 ease-in-out duration-100 hidden sm:block"
      :style="{ borderColor: dotColor, borderWidth: '3px', borderStyle: 'solid' }"
    ></div>

    <!-- Image Block -->
    <a :href="link" class="relative flex justify-center w-full sm:justify-start" target="_blank">
      <div
        class="relative flex flex-col items-center duration-200 ease-in-out group sm:hover:scale-105"
        :class="{ 'sm:ml-auto': reverse, 'sm:mr-auto': !reverse }"
      >
        <img
          class="max-w-[400px] w-full relative z-10 drop-shadow-[0_0px_60px_rgba(59,130,246,0.6)]"
          :src="image"
          alt=""
        />
        <span
          v-if="tag"
          class="flex items-center gap-1 px-2 py-1 mt-2 text-sm duration-200 rounded group-hover:-top-14 ease-jump sm:absolute left-1/2 sm:-translate-x-1/2 top-5 sm:text-base w-max after:hidden sm:after:block after:w-4 after:h-4 after:bg-inherit after:absolute after:left-1/2 after:-translate-x-1/2 after:rotate-45 after:-bottom-2"
          :style="{ backgroundColor: tagBgColor, color: tagTextColor }"
        >
          {{ tag }}
          <svg
                xmlns="http://www.w3.org/2000/svg"
                width="16"
                height="16"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="feather feather-external-link"
              >
                <path
                  d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                ></path>
                <polyline points="15 3 21 3 21 9"></polyline>
                <line x1="10" y1="14" x2="21" y2="3"></line>
              </svg>
        </span>
      </div>
    </a>

    <!-- Text Block -->
    <div class="w-full">
      <h3 :style="{ color: titleColor }" class="text-2xl font-bold md:text-4xl">
        {{ title }}
      </h3>
      <span :style="{ color: titleColor }" class="text-base md:text-lg">({{ subtitle }})</span>
      <p class="mt-2 text-sm text-justify md:text-base">
        {{ description }}
      </p>
      <ul class="flex flex-wrap gap-2 mt-2">
        <li
          v-for="(tech, index) in techStack"
          :key="index"
          class="border rounded-[50px] border-[#999] px-[10px] py-[5px] text-sm md:text-base"
        >
          {{ tech }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    title: String,
    subtitle: String,
    description: String,
    image: String,
    link: String,
    techStack: Array,
    tag: String,
    tagBgColor: String,
    tagTextColor: {
      type: String,
      default: 'white'
    },
    dotColor: String,
    linePosition: {
      type: String,
      default: 'left-1/4 right-1/2'
    },
    reverse: {
      type: Boolean,
      default: false
    },
    titleColor: String
  }
}
</script>
