<template>
<!-- job details page - from path /jobs/:id -->
<!-- access the id of the route by using $route.params.id -->
  <h1>Job Details Page</h1>
  <p>The job ID is {{ id }}</p>
</template>
<script>
export default {
  data() {
    return {
      id: this.$route.params.id
    }
  }
}
</script>