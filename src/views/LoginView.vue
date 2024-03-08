<template>
    <div class="header">
      <h1>LOGGA IN</h1>
      <img src="https://yesno.wtf/assets/no/30-d37eee83c3c2180de4edb7da6fa9f5b7.gif" alt="answer" />
    </div>
  </template>
  
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
  