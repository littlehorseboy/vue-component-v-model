<template>
  <div>
    <div>父組件 Home.vue 的 inputValue: {{ inputValue }}</div>

    <hr>

    <Input :inputValue="inputValue" :handleInputValue="handleInputValue" />

    <InputTwo :inputValue="inputValue" @handleInputValue="handleInputValue" />

    <InputThree :inputValue.sync="inputValue" />

    <InputFour :inputValue="inputValue" @update:inputValue="inputValue = $event" />

    <InputFive v-model="inputValue" />

    <InputSix :value="inputValue" @input="inputValue = $event" />

    <InputSeven v-model="inputValue" />
  </div>
</template>

<script>
import Input from '@/components/Input.vue';
import InputTwo from '@/components/InputTwo.vue';
import InputThree from '@/components/InputThree.vue';
import InputFour from '@/components/InputFour.vue';
import InputFive from '@/components/InputFive.vue';
import InputSix from '@/components/InputSix.vue';
import InputSeven from '@/components/InputSeven.vue';

export default {
  components: {
    Input,
    InputTwo,
    InputThree,
    InputFour,
    InputFive,
    InputSix,
    InputSeven,
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
