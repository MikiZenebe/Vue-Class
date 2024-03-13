<template>
  <div>New For VUE.JS {{ name }}</div>
  <div v-html="tag"></div>
  <div v-bind:id="bindId">This is ID</div>
  <button v-bind:disabled="isDisabled">Toggle</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted</h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>
</template>


<script>
export default {
  name: "App",
  data() {
    return {
      name: "Nhatty",
      tag: "<h1>Vue.JS</h1>",
      bindId: "thisId",
      isDisabled: false,
      isPromoted: true, //Based on the boolean logic
      isSoldout: false
    };
  },
};
</script>


<style scoped>
  .underline {
    text-decoration: underline;
  }

  .promoted {
    font-style: italic;
  }

  .new {
    color: green;
  }

  .sold-out {
    color: red;
  }
</style>
