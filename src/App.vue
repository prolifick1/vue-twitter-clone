<template>
  <div id="app">
    @{{ user.username }} - {{ fullName }} <strong>Followers: </strong>
    {{ followers }}
    <button @click="followUser">follow</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: "_VinceWinkelstein",
        firstname: "vincent",
        lastname: "winkelstein",
        email: "vince@home.com",
        isAdmin: true,
      },
    };
  },
  computed: {
    fullName() {
      return `${this.user.firstname} ${this.user.lastname}`;
    },
  },
  methods: {
    followUser() {
      this.followers++;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
  text-align: center;
}
</style>
