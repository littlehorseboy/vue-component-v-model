<template>
  <div>
    <input :value="inputValue" />
  </div>
</template>

<script>
export default {
  props: {
    inputValue: {
      type: String,
    },
  },
};
</script>
