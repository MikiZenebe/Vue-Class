<script>
import Binding from "@/components/Binding.vue";
import ConditionalRender from "@/components/ConditionalRender.vue";
import ListRendering from "@/components/ListRendering.vue";
import Methods from "@/components/Methods.vue";
import EventHandler from '@/components/EventHandler.vue'

export default {
  name: "App",
  components: {
    Binding,
    ConditionalRender,
    ListRendering,
    Methods,
    EventHandler
  },
};
</script>

<template>
  <!-- <Binding />
  <ConditionalRender /> -->
  <!-- <ListRendering /> -->
  <!-- <Methods /> -->
  <EventHandler />
</template>
;


<style>

  #app{
   text-align: center;
  }
</style>