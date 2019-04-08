<template>
  <div>
    <p>First component Counter is: {{ counter }}</p>
    <p>First component Clicks is: {{ clicks }}</p>
  </div>
</template>

<script>
import * as types from "../store/types";
export default {
  computed: {
    counter() {
      return this.$store.getters[types.DOUBLE_COUNTER];
    },
    clicks() {
      return this.$store.getters[types.CLICK_COUNTER];
    }
  }
};
</script>