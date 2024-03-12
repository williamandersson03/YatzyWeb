<template>
  <div class="header">
    <h1>Välkommen till YatzyWeb</h1>
    <h3>Ett projekt av <a href="https://github.com/williamandersson03/YatzyWeb" target="_blank" rel="noopener noreferrer">William Andersson</a></h3>
    <div class="btndiv">
      <button class="btn" @click="$router.push('login')">LOGGA IN</button>
      <button class="btn" @click="$router.push('signup')">SKAPA KONTO</button>
    </div>
  </div>
</template>

<style scoped>
@import '../assets/defaultviewstyle.css';
@media (max-width: 1023px)
{
  .btndiv
  {
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    padding-top: 1rem;
  }
}
@media (min-width: 1024px)
{
  .btndiv
  {
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
    font-weight: bold;
    font-size: 1rem;
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
</style>