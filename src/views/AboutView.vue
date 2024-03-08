<template>
  <div class="header">
    <h1>{{ answer.answer }}</h1>
    <img :src="answer.image" alt="answer" />
  </div>
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

<style scoped>
@import '../assets/main.css';
@media (max-width: 1023px) {
  .header {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 0.5rem;
  }
}
@media (min-width: 1024px) {
  .header {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
}
</style>
