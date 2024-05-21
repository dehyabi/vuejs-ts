<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('bill')">change name</button>
    <button @click="changeAge('34')">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    // const state = reactive({
    //   name: "Link",
    //   age: 28 as string | number,
    // });

    // state.name = "James"
    // state.age = 37
    // return { ...toRefs(state) };
    const name = ref('Link');
    name.value = 'Youtube'
  },
  methods: {
    changeName(name: string) {
      this.name = name;
      return name;
    },
    changeAge(age: string | number) {
      this.age = age;
      return age;
    },
  },
});
</script>

<style></style>
