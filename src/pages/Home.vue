<template>
  <div>
    <Input inputValue="inputValue" />
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
      inputValue: '隨便給個值',
    };
  },
};
</script>
