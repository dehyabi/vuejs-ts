<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import Job from "./types/Job";
import JobList from "./components/JobsList.vue";

export default defineComponent({
  name: "App",
  components: { JobList },
  setup() {
    const jobs = ref<Job[]>([
      { title: "Laravel Developer", location: "USA", salary: 4000, id: "1" },
      {
        title: "Javascript Developer",
        location: "Japan",
        salary: 4200,
        id: "2",
      },
      { title: "Backend developer", location: "UK", salary: 5000, id: "3" },
    ]);
    return { jobs };
  },
});
</script>

<style></style>
