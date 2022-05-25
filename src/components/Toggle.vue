<template>
  <div :class="theme === 'light' ? 'light-theme' : 'dark-theme'" class="main-body">
    <div style="padding: 5px;">
      <div id="heading">Theme Selection</div>
      <button @click="changeTheme">Switch</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Toggle',
  data() {
    return{
      theme: "light"
    }
  },
  methods: {
    changeTheme() {
      console.log("Theme Changed");
      this.theme = this.theme === "dark" ? "light" : "dark";
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main-body{
  height: 100vh;
  padding: 0;
}
.light-theme{
  background: white;
  color: black;
}
.dark-theme{
  background: black;
  color: white;
}
button{
  padding: 10px;
}
#heading{
  font-size: 3rem;
  font-weight: bolder;
}
</style>
