<template>
  <div>
    <template v-if="variant == 'h1'">
      <h1 class="oldclass h1" v-bind="$attrs">
        <slot />
      </h1>
    </template>
    <template v-if="variant == 'h2'">
      <h2 class="oldclass h2" v-bind="$attrs">
        <slot />
      </h2>
    </template>
  </div>
</template>
<script>
export default {
  inheritAttrs: false,
  props: {
    variant: {
      type: String,
      required: false,
    },
  },
};
</script>
