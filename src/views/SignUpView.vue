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
        const email = target.email.value;

        const response = await axios.post('http://localhost:3000/api/signup', {
          username,
          password,
          email
        });

        this.signupResult = response.data;
        this.signupMessage = this.signupResult.includes('successful') ? 'signupMessageSuccess' : 'signupMessageError';

        this.username = '';
        this.password = '';
        this.email = '';

      } catch (error: any) {
        this.signupResult = error.message;
        this.signupMessage = 'signupMessageError';
      }
    }
  },
  data() {
    return {
      signupResult: '',
      signupMessage: ''
    }
  }
}
</script>

<template>
  <div class="header">
    <div class="signup-form">
      <form @submit="handleSubmit">
        <h1>SKAPA KONTO</h1>
        <div class="signupMessageDiv" :class="signupMessage" v-if="signupResult">
          <h3>{{ signupResult }}</h3>
        </div>
        <div class="form-group">
          <label for="username">Användarnamn:</label>
          <input type="text" id="username" name="username" required />
        </div>
        <div class="form-group">
          <label for="password">Lösenord:</label>
          <input type="password" id="password" name="password" required />
        </div>
        <div class="form-group">
          <label for="email">E-post:</label>
          <input type="email" id="email" name="email" required />
        </div>
        <button type="submit" class="btn">SKAPA KONTO</button>
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

.signupMessageDiv
{
  padding: 0.5rem 1rem;
  border-radius: 3px;
  color: white;
  font-weight: bold;
  text-align: center;
}

.signupMessageSuccess
{
  background-color: green;
}

.signupMessageError
{
  background-color: red;
}

.signup-form {
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
  input[type="email"],
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