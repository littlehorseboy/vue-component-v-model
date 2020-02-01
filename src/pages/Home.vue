<template>
  <div>
    <div>父組件 Home.vue 的 inputValue: {{ inputValue }}</div>

    <hr>

    <Input :inputValue="inputValue" :handleInputValue="handleInputValue" />
  </div>
</template>

<script>
import Input from '@/components/Input.vue'

export default {
  components: {
    Input,
  },
  data() {
    return {
      inputValue: 'test',
    };
  },
  methods: {
    handleInputValue(event) {
      this.inputValue = event.target.value;
    },
  },
};
</script>
