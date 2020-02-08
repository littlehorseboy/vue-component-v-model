<template>
  <div>
    <div>
      <strong>子組件 InputFive.vue</strong>
      <br>
      <input :value="value" @input="$emit('input', $event.target.value)" />
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
};
</script>
