<script lang="ts">
import axios from 'axios';

export default {
  methods: {
    async handleSubmit(event: Event) {
      try {
        event.preventDefault();
        const target = event.target as HTMLFormElement;
        const username = target.username.value;
        const password = target.password.value;

        const response = await axios.post('http://localhost:3000/api/deleteme', {
          username,
          password
        });

        this.deletemeResult = response.data;
        this.deletemeMessage = this.deletemeResult.includes('successful') ? 'deletemeMessageSuccess' : 'deletemeMessageError';

      } catch (error: any) {
        this.deletemeResult = error.message;
        this.deletemeMessage = 'deletemeMessageError';
      }
    }
  },
  data() {
    return {
      deletemeResult: '',
      deletemeMessage: ''
    }
  }
}
</script>
<template>
  <div class="header">
    <div class="deleteme-form">
      <form @submit="handleSubmit">
        <h1>RADERA MIN DATA</h1>
        <div class="deletemeMessageDiv" :class="deletemeMessage" v-if="deletemeResult">
          <h3>{{ deletemeResult }}</h3>
        </div>
        <div class="form-group">
          <label for="username">Användarnamn:</label>
          <input type="text" id="username" name="username" required />
        </div>
        <div class="form-group">
          <label for="password">Lösenord:</label>
          <input type="password" id="password" name="password" required />
        </div>
        <button type="submit" class="btn">RADERA</button>
      </form>
      <br>
      <RouterLink to="/datainfo">Hur hanteras min data?</RouterLink>
    </div>
  </div>
</template>

<style scoped>
@import '../assets/defaultviewstyle.css';
@media (max-width: 1023px) {
  /* Add your styles for smaller screens here */
}
@media (min-width: 1024px) {
  /* Add your styles for larger screens here */
}

.btn
{
  background: rgb(218, 0, 0);
}
.btn:hover {
background: rgb(160, 1, 1);
.btntext{
    color: black;
  }
}
.btn:active {
background: rgb(100, 0, 0);
}

.deletemeMessageDiv
{
  padding: 0.5rem 1rem;
  border-radius: 3px;
  color: white;
  font-weight: bold;
  text-align: center;
}

.deletemeMessageSuccess
{
  background-color: green;
}

.deletemeMessageError
{
  background-color: red;
}

.deleteme-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(255, 255, 255, 0.1);
    background-color: var(--color-background);
  }
  
  .form-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 1rem;
    margin-top: 1rem;
  }
  
  label {
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  
  input[type="text"],
  input[type="password"] {
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  
  button {
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 3px;
    background-color: var(--color-primary);
    color: white;
    font-weight: bold;
    cursor: pointer;
  }
</style>
