<template>
  <div>
    <input v-model="model" />

    <div>子組件 Input.vue 的 inputValue: {{ model }}</div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
    },
  },
  computed:{
    model: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
      },
    },
  },
};
</script>
