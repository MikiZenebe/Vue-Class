<script>
import Binding from "@/components/Binding.vue";
import ConditionalRender from "@/components/ConditionalRender.vue";

export default {
  name: "App",
  components: {
    Binding,
    ConditionalRender,
  },
};
</script>

<template>
  <Binding />
  <ConditionalRender />
</template>
;
