<template>
  <div>New For VUE.JS {{ name }}</div>
  <div v-html="tag"></div>
  <div v-bind:id="bindId">This is ID</div>
  <button v-bind:disabled="isDisabled">Toggle</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">Promoted</h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">Soldout? movie</h2>

  <h2
    v-bind:style="{
      color: highlightColor,
      fontSize: headerSize + 'px',
    }"
  >
    Binding Styles
  </h2>
</template>

<script>
export default {
  name: "Binding",
  data() {
    return {
      name: "Nhatty",
      tag: "<h1>Vue.JS</h1>",
      bindId: "thisId",
      isDisabled: false,
      //Binding Class
      isPromoted: true, //Based on the boolean logic
      isSoldout: false,
      //Binding Styles
      highlightColor: "red",
      headerSize: 30,
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
