<template>
  <section class="-mt-2 bg-black">
    <div class="relative max-w-screen-xl px-4 pb-8 mx-auto sm:pb-16">
      <h2
        class="text-3xl sm:text-[40px] bg-[#111] relative z-10 font-bold px-4 py-2 w-max mx-auto text-center text-[#1788ae] sm:border-b-2 border-[#1788ae]"
      >
        Latest Works
      </h2>

      <!-- Reusable Cards -->
      <ProjectCard
        title="Nirdhara Fresh Juicery"
        subtitle="Ecommerce Website"
        description="Nirdhara is an eCommerce platform designed for our client to sell fresh juices, featuring a seamless subscription model for recurring orders."
        :image="NirdharaImg"
        link="https://nirdhara.com"
        :techStack="['#angular', '#python', '#fast api', '#mysql', '#tailwind css', '#typescript']"
        tag="Nirdhara"
        tagBgColor="#459bd5"
        dotColor="#459bd5"
        titleColor="#459bd5"
      />

      <ProjectCard
        title="Easy My Tasks"
        subtitle="EMT"
        description="EasyMyTasks is a workflow management platform designed for CAs to streamline their operations. It allows task assignment, employee tracking, and efficient service management."
        :image="EMTImg"
        link="https://easymytasks.com"
        :techStack="['#angular', '#python', '#fast api', '#postgresql', '#tailwind css', '#typescript']"
        tag="EMT"
        tagBgColor="#ffe578"
        tagTextColor="black"
        dotColor="#ffe578"
        linePosition="left-1/2 right-1/4"
        :reverse="true"
        titleColor="#ffe578"
      />

      <ProjectCard
        title="Video Surveillance System"
        subtitle="Live Streaming"
        description="VMS is a role-based access system for adding, viewing, and recording live camera feeds. Built the entire platform from scratch for private client, ensuring secure and efficient access control."
        :image="VMSImg"
        link="#"
        :techStack="['#angular', '#python', '#flask', '#postgresql', '#bootstrap', '#typescript']"
        tag=""
        dotColor="#fc815c"
        titleColor="#fc815c"
      />

      <!-- Center vertical line -->
      <div
        class="w-[2px] hidden sm:block bg-[#1788ae] absolute top-0 bottom-0 left-1/2 -translate-x-1/2"
      ></div>
    </div>
  </section>
</template>

<script>
import ProjectCard from './ProjectCard.vue';

import NirdharaImg from '@/assets/images/nirdhara.png';
import EMTImg from '@/assets/images/EMT.png';
import VMSImg from '@/assets/images/VMS.png';

export default {
  name: 'LatestWorksComponent',
  components: { ProjectCard },
  data() {
    return {
      NirdharaImg,
      EMTImg,
      VMSImg
    };
  }
};
</script>

