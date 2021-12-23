<template>
  <h2>Jobs</h2>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }"
      ><h5>{{ job.title }}</h5></router-link
    >
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
.job h5 {
  font-family: sans-serif;
  padding: 20px;
  border-radius: 10px;
  cursor: pointer;
  color: #444;
  margin: 10px auto;
  background: #f4f4f4;
  max-width: 600px;
}
a {
  text-decoration: none;
}
</style>
