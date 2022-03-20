<template>
  <nav>
    <!-- data-binding to the name is safer in case you make changes down the track -->
    <router-link :to="{ name: 'Home' }">Home</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link> |
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </nav>

  <router-view/>
  <div class="inline-flex mt-16">
    <button @click="back" class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-l text-sm">Prev</button>
    <button @click="redirect" class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 text-sm">Home</button>
    <button @click="forward" class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-r text-sm">Next</button>
  </div>
</template>
<script>
export default {
  methods: {
    redirect() {
      this.$router.push({ name: 'Home'})

    },
    back() {
      this.$router.go(-1)

    },
    forward() {
      this.$router.go(1)

    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>