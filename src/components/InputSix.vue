<template>
  <div>
    <input :value="value" @input="$emit('input', $event.target.value)" />

    <div>子組件 Input.vue 的 inputValue: {{ value }}</div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
    },
  },
};
</script>
