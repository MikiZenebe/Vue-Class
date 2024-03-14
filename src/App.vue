<script>
import Binding from "@/components/Binding.vue";
import ConditionalRender from "@/components/ConditionalRender.vue";
import ListRendering from "@/components/ListRendering.vue";

export default {
  name: "App",
  components: {
    Binding,
    ConditionalRender,
    ListRendering,
  },
};
</script>

<template>
  <!-- <Binding />
  <ConditionalRender /> -->
  <ListRendering />
</template>
;
