<template>
  <v-alert
    v-bind="$attrs"
    :class="[`elevation-${elevation}`]"
    :value="value"
    class="v-alert--notification"
  >
    <slot />
  </v-alert>
</template>

<script>
export default {
  inheritAttrs: false,
  
  props: {
    elevation: {
      type: [Number, String],
      default: 6
    },
    value: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style>
.v-alert--notification {
  border-radius: 4px !important;
  border-top: none !important;
}
</style>
