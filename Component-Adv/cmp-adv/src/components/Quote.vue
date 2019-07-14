<template>
  <div>
    <div>
      <slot name="title"></slot>
    </div>
    <hr>
    <div>
        <slot name="quote"></slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
div {
  background-color: cadetblue;
  box-shadow: 1px 1px 5px black;
  margin: 20px auto;
  padding: 30px;
  text-align: center;
  color: red;
  font-size: 14pt;
}
h1 {
  color: black;
  text-emphasis: 4px;
}
</style>
