<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>{{username}}</p>
    <button @click="changeUser">Change Username</button>
  </div>
</template>

<script>
export default {
  props: ["username"],
  methods:{
      changeUser() {
        this.username = "Malik";
        this.$emit('userChanged',this.username)
      }
  }
};
</script>

<style scoped>
div {
  background-color: chocolate;
}
</style>
