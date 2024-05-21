<template>
  <div class="job-list">
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h1>{{ job.title }} in {{ job.location }}</h1>
        <div class="salary">
            <p>USD {{ job.salary }}</p>
        </div>
        <div class="description">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis eos adipisci asperiores explicabo similique non magni! Debitis iure error ducimus fuga! Consectetur ipsum molestias eveniet deserunt sint! Harum, vel nemo.
        </div>
    </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import Job from "../types/Job";

export default defineComponent({
  props: {
    jobs: {
      required: true,
      type: Array as PropType<Job[]>,
    },
  },
});
</script>

<style></style>
