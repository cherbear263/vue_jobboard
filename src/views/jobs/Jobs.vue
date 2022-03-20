<template>
  <div class="max-w-lg sm:mx-auto mx-3">
  <h1 class="font-sans text-2xl text-gray-700 font-bold mb-5">Jobs</h1>
  <div v-for="job in jobs" :key="job.id"
  class="bg-gray-200 rounded-md hover:bg-gray-300 max-w-full my-4 py-5">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }"
    class="text-xl text-emerald-500 font-semibold cursor-pointer">
      <h2>{{job.title }}</h2>
    </router-link>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: 'Ninja UX Designer', id: 1, details: 'lorem'},
        { title: 'Ninja UX Designer', id: 2, details: 'lorem'},
        { title: 'Ninja UX Designer', id: 3, details: 'lorem'},
      ]
    }
  }
}
</script>