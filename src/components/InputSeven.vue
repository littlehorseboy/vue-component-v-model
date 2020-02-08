<template>
  <div>
    <div>
      <strong>子組件 InputSeven.vue</strong>
      <br>
      <input v-model="model" />
    </div>

    <div>
      props value: 
      <span style="border: 1px dotted">
        {{ value }}
      </span>
    </div>
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
