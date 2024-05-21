<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('updated')">change name</button>
  </div>
</template>

<script lang="ts">

import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  data() {
    return {
      name: 'Link',
      age: 29 as number | string
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
