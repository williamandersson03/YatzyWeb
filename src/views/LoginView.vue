<template>
    <h1>{{ answer.answer }}</h1>
    <img :src="answer.image" alt="answer" />
</template>
  
  <script lang="ts">
  import axios from "axios";
  import { defineComponent } from 'vue'

  interface Answer {
  answer: string;
  image: string;
}
  
  export default  defineComponent({
    name: "App",
    data() {
      return {
        answer: {} as Answer,
      };
    },
    methods: {
      async getAnswer() {
        const { data } = await axios.get("https://yesno.wtf/api");
        this.answer = data;
      },
    },
    beforeMount() {
      this.getAnswer();
    },
  });
  </script>