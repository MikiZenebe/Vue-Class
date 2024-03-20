<script>
import Binding from "@/components/Binding.vue";
import ConditionalRender from "@/components/ConditionalRender.vue";
import ListRendering from "@/components/ListRendering.vue";
import Methods from "@/components/Methods.vue";
import EventHandler from '@/components/EventHandler.vue'
import FormHandling from "./components/FormHandling.vue";

export default {
  name: "App",
  components: {
    Binding,
    ConditionalRender,
    ListRendering,
    Methods,
    EventHandler,
    FormHandling
  },
};
</script>

<template>
  <!-- <Binding />
  <ConditionalRender /> -->
  <!-- <ListRendering /> -->
  <!-- <Methods /> -->
  <!-- <EventHandler /> -->
  <FormHandling />
</template>
;


<style>

  #app{
   text-align: center;
  }
</style>