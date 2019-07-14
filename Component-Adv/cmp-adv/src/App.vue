<template>
  <div>
      <app-quote>
          <h1>{{quoteHead}}</h1>
          <p>A beautiful quote!</p>
      </app-quote>
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";
export default {
    data(){
        return{
            quoteHead:"The Quote"
        }
    },
  components: {
    appQuote: Quote
  }
};
</script>

<style>
</style>
