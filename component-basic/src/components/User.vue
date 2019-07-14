<template>
  <div class="component">
    <h1>The User Component</h1>
    <p>I'm an awesome User!</p>
    <p>{{name}}</p>
    <hr />
    <div class="row">
      <div class="col-xs-12 col-sm-6">
        <app-user-detail :userage="age" :username="name" @userChanged="name=$event"></app-user-detail>
      </div>
      <div class="col-xs-12 col-sm-6">
        <app-user-edit  :userage="age"></app-user-edit>
      </div>
    </div>
  </div>
</template>

<script>
import UserDetail from "./UserDetail.vue";
import UserEdit from "./UserEdit.vue";
export default {
  data() {
    return {
      age: 30,
      name: "AASHISH"
    };
  },
  components: {
    appUserDetail: UserDetail,
    appUserEdit: UserEdit
  }
};
</script>
    
<style>
div {
  background-color: lightblue;
}
</style>
