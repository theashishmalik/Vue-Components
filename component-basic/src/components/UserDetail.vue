<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>{{username}}</p>
    <p>{{userage}}</p>
    <button @click="changeUser">Change Username</button>
  </div>
</template>

<script>
import { eventBus } from "../main.js";
export default {
  props: ["username", "userage"],
  methods: {
    changeUser() {
      this.username = "Malik";
      this.$emit("userChanged", this.username);
    }
  },
  created() {
    eventBus.$on("ageChanged", d => {
      this.userage = d;
    });
  }
};
</script>

<style scoped>
div {
  background-color: chocolate;
}
</style>
