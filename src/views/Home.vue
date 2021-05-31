<template>
  <main>
    <div class="container">
      <div class="filters">
        <breedlist/>
        <span>Сортировка по алфавиту</span>
      </div>
      <div class="main-content relative">
        <HelloWorld />
        <btntop/>
      </div>
    </div>
  </main>
</template>

<script>
// @ is an alias to /src
import btntop from "@/components/BtnTop.vue";
import HelloWorld from "@/components/HelloWorld.vue";
import breedlist from "@/components/BreedList.vue";
export default {
  name: "Home",
  components: {
    HelloWorld,
    btntop,
    breedlist
  },
};
</script>
