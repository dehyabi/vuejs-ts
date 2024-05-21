<template>
  <div class="app">
    <p>{{ name }}</p>
    <button @click="changeName('updated')">change name</button>
  </div>
</template>

<script lang="ts">
let age: string | number = 29
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: 'Link',
      age: 29
    };
  },
  methods: {
    changeName(name: string) {
      this.name = name;
    },
  },
});
</script>

<style></style>
