<template>
  <h2>Jobs</h2>
  <div v-if="jobs.length">
    <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: { id: job.id } }"
        ><h5>{{ job.title }}</h5></router-link
      >
    </div>
  </div>

  <div v-else>
    <p>Loading Jobs..</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs")
      .then((res) => res.json())
      .then((data) => (this.jobs = data))
      .catch((err) => console.log(err.message));
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
