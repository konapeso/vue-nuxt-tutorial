<template>
  <div>
    <TheHeader/>
    <div class="wrapper">
      <nuxt class="container"/>
    </div>
  </div>
</template>

<script>
import TheHeader from "~/components/The.Header.vue";

export default {
  components: {
    TheHeader
  }
};
</script>