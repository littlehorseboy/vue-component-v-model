<template>
  <div>
    <input :value="inputValue" @input="handleInputValue" />

    <div>子組件 Input.vue 的 inputValue: {{ inputValue }}</div>
  </div>
</template>

<script>
export default {
  props: {
    inputValue: {
      type: String,
    },
    handleInputValue: {
      type: Function,
    },
  },
};
</script>
