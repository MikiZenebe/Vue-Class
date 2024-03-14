<template>
  <h2 v-if="num === 0">The No is zero</h2>
  <h2 v-else-if="num < 0">The No is Negative</h2>
  <h2 v-else-if="num > 0">The No is Positive</h2>
  <h2 v-else>The No is not zero</h2>
  <h2 v-else>Not a number</h2>

  <template v-if="display">
    <h2>Miki</h2>
    <h2>Learn</h2>
    <h2>Vue</h2>
  </template>

  <h2 v-show="isShown">Use V-Show</h2>
</template>

<script>
export default {
  name: "ConditionalRender",
  data() {
    return {
      num: 0,
      display: true,
      isShown: true,
    };
  },
};
</script>
