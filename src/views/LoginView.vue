<script lang="ts">
import axios from 'axios';
import CryptoJS from 'crypto-js';

export default {
  methods: {
    handleSubmit(event: Event) {
      event.preventDefault();
      const target = event.target as HTMLFormElement;
      const username = target.username.value;
      const password = target.password.value;

      axios.post('/api/login', {
        username,
        password
      })
      .then(response => {
        // Hantera lyckad inloggning
      })
      .catch(error => {
        // Hantera inloggningsfel
      });
    }
  }
}
</script>
<template>
  <div class="header">
    <div class="login-form">
      <form @submit="handleSubmit">
        <h1>LOGGA IN</h1>
        <div class="form-group">
          <label for="username">Användarnamn:</label>
          <input type="text" id="username" name="username" />
        </div>
        <div class="form-group">
          <label for="password">Lösenord:</label>
          <input type="password" id="password" name="password" />
        </div>
        <button type="submit" class="btn">Logga In</button>
      </form>
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

.login-form {
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
