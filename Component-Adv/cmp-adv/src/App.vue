<template>
  <section>
    <div>
      <button @click="selected='appBlue'">Blue</button>
      <button @click="selected='appGreen'">Green</button>
      <button @click="selected='appRed'">Red</button>
      <hr />
      <p>{{selected}}</p>
      <hr />
        <component :is='selected'>
          <p>Dynamic Component</p>
        </component >
    </div>
    <hr />
    <hr />
    <div>
      <app-quote>
        <h1 slot="title">{{quoteHead}}</h1>
        <p slot="quote">A beautiful quote!</p>
      </app-quote>
    </div>
  </section>
</template>

<script>
import Quote from "./components/Quote.vue";
import Red from "./components/Red.vue";
import Green from "./components/Green";
import Blue from "./components/Blue.vue";
export default {
  data() {
    return {
      quoteHead: "The Quote",
      selected: "appRed"
    };
  },
  components: {
    appQuote: Quote,
    appRed: Red,
    appBlue: Blue,
    appGreen: Green
  }
};
</script>

<style>
</style>
