<template>
  <div class="header">
    <h1>Välkommen till YatzyWeb</h1>
    <h3>Ett projekt av <a href="https://github.com/williamandersson03/YatzyWeb" target="_blank" rel="noopener noreferrer">William Andersson</a></h3>
    <div class="btndiv">
      <button class="btn"><RouterLink to="/login" class="btntext">LOGGA IN</RouterLink></button>
      <button class="btn"><RouterLink to="/signup" class="btntext">SKAPA KONTO</RouterLink></button>
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
    .btntext{
      color: white;
    }
  }
.btn:hover {
  background: rgb(1, 134, 90);
  .btntext{
      color: black;
    }
}
.btn:active {
  background: rgb(1, 70, 47);
}
.btntext {
  color: white;
  text-decoration: none;
  padding: 0%;
  font-weight: bold;
  font-size: 0.9rem;
}
  
</style>
