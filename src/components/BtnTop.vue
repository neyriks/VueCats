<template lang="html">
  <span id="scroll-top" class="absolute" @click="scrollToTop"
    ><i class="fas fa-arrow-up"></i
  ></span>
</template>

<script>
export default {
  name: "btntop",
  methods: {
    scrollToTop() {
      window.scroll({
        top: top,
        left: 0,
        behavior: "smooth",
      });
    },
  }
}
</script>
