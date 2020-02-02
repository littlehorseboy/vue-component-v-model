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

    <InputTwo :inputValue="inputValue" @handleInputValue="handleInputValue" />
  </div>
</template>

<script>
import InputTwo from '@/components/InputTwo.vue';

export default {
  components: {
    InputTwo,
  },
  data() {
    return {
      inputValue: '我是父組件的 data',
    };
  },
  methods: {
    handleInputValue(value) {
      this.inputValue = value;
    },
  },
};
</script>
