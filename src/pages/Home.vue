<template>
  <div>
    <strong>父組件 Home.vue</strong>
    <div>
      inputValue:
      <span style="border: 1px dotted">
        {{ inputValue }}
      </span>
    </div>

    <hr>

    <InputSeven v-model="inputValue" />
  </div>
</template>

<script>
import InputSeven from '@/components/InputSeven.vue';

export default {
  components: {
    InputSeven,
  },
  data() {
    return {
      inputValue: '我是父組件的 data',
    };
  },
};
</script>
