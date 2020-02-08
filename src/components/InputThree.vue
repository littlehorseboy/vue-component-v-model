<template>
  <div>
    <div>
      <strong>子組件 InputThree.vue</strong>
      <br>
      <input :value="inputValue" @input="$emit('update:inputValue', $event.target.value)" />
    </div>

    <div>
      props inputValue: 
      <span style="border: 1px dotted">
        {{ inputValue }}
      </span>
    </div>
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
