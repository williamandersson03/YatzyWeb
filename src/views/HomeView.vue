<template>
  <div class="header">
    <h1>Välkommen till YatzyWeb</h1>
    <h3>Ett projekt av William Andersson</h3>
    <div class="btndiv">
      <button class="btn">LOGGA IN</button>
      <button class="btn">SKAPA KONTO</button>
    </div>
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
  .btndiv {
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    padding-top: 1rem;
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
  .btndiv {
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    padding-top: 1.5rem;
  }
}

.btn {
    padding: 1rem;
    margin: 0.5rem;
    background: hsla(160, 100%, 37%, 1);
    color: white;
    border-radius: 0.5rem;
    border: none;
  }
.btn:hover {
  background: rgb(1, 134, 90);
  color: black;
}
.btn:active {
  background: rgb(1, 70, 47);
}
</style>
