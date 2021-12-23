<template>
  <h2>Jobs</h2>
  <div v-for="job in jobs" :key="job.id">
    <h5>{{ job.title }}</h5>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { id: 1, title: "UX/UI designer", desc: "Hire UX/UI designer" },
        { id: 2, title: "Frontend developer ", desc: "Frontend developer" },
        { id: 3, title: "UX/UI developer", desc: "Hire UX/UI designer" },
      ],
    };
  },
};
</script>

<style>
h5 {
  font-family: sans-serif;
}
</style>
