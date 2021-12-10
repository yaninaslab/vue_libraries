<template>
  <div>
    <button-one @button_clicked="react_to_btn_clicked"></button-one>
    <page-quote v-for="quote in quotes" :key="quote._id" :quote="quote">
    </page-quote>
  </div>
</template>

<script>
import ButtonOne from "./ButtonOne.vue";
import PageQuote from "./PageQuote.vue";
export default {
  name: "home-content",
  components: {
    ButtonOne,
    PageQuote,
  },
  methods: {
    react_to_btn_clicked(payload) {
      this.quotes = payload;
    },
  },
  data() {
    return {
      quotes: [],
    };
  },
};
</script>

<style scoped>
</style>