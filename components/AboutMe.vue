<template>
  <div class="block sm:flex sm:gap-4 md:gap-8 mt-10 md:mt-20">
    <!-- About me portfolio image -->
    <div class="w-full sm:w-1/4 mb-7 sm:mb-0">
      <img
        src="https://i.ibb.co/pnQhHMV/IMG-2298-removebg-preview.png"
        class="rounded-lg w-96"
        alt="IMG-2298-removebg-preview"
        border="0"
      />
    </div>

    <!-- About me details -->
    <div class="w-full sm:w-3/4 text-left">
      <p
        v-for="bio in aboutMe"
        :key="bio.id"
        class="mb-4 text-primary-dark dark:text-ternary-light text-lg"
      >
        {{ bio.bio }}
      </p>
    </div>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  data: () => {
    return {
      // Todo
    };
  },
  computed: {
    ...mapState(["aboutMe"]),
  },
};
</script>
