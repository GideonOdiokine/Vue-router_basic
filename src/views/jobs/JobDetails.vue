<template>
  <h3>Job Details Page</h3>
  <p>The job id is {{ id }}</p>
</template>

<script>
export default {
  props: ["id"],
};
</script>

<style>
h3 {
  font-family: "Courier New", Courier, monospace;
}
</style>
