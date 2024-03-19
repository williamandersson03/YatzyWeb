<template>
  <div class="header">
    <img :src="answer.image" alt="answer" class="image" />
    <h1 class="text">{{ answer.answer }}</h1>
  </div>
</template>

<script lang="ts">
import axios from "axios";
import { defineComponent } from 'vue'

interface Answer {
  answer: string;
  image: string;
}

export default defineComponent({
  name: "App",
  data() {
    return {
      answer: {} as Answer,
    };
  },
  methods: {
    async getAnswer() {
      const forceAnswer = 'no'; 
      const { data } = await axios.get(`https://yesno.wtf/api`, {
        params: {
          force: forceAnswer
        }
      });
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
  .image {
    width: 200px; /* Adjust the size as per your requirement */
    height: 200px; /* Adjust the size as per your requirement */
  }
  .text {
    text-align: center;
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
  .image {
    width: 300px; /* Adjust the size as per your requirement */
    height: 300px; /* Adjust the size as per your requirement */
  }
  .text {
    text-align: center;
  }
}
</style>
