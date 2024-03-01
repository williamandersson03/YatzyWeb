<template>
  <div class="header">
    <h1>Om projektet</h1>
    <br>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer lorem nunc, eleifend id consectetur id, porttitor a libero. Proin pulvinar mi ligula, vel fringilla sapien porta non. Nulla nisl libero, pellentesque non luctus sit amet, bibendum quis mauris. Aliquam convallis pellentesque egestas. Nam ut eleifend lorem. Aliquam vehicula eros in elementum tempor. Duis tempor id nisl ut lobortis. Integer sodales, ante eu aliquam consectetur, orci ex mollis arcu, a porta ante mi ullamcorper risus. Fusce ac semper arcu. Phasellus fringilla euismod rhoncus.</p>
    <br>
    <p>Morbi at lacus luctus, tempus nibh dictum, pharetra orci. Etiam vitae mi tincidunt sapien consectetur mattis. Praesent vehicula, lorem ut condimentum viverra, turpis nunc euismod enim, vitae convallis mauris nisi et libero. Nam nisl nulla, auctor at elit eget, ullamcorper gravida diam. Cras eu mi tortor. Aliquam elementum sem et nisi sagittis, at malesuada arcu feugiat. Nunc sit amet eros quis ipsum efficitur lobortis. Maecenas sit amet diam ipsum. Vivamus id massa blandit eros tempus laoreet ut in magna. Curabitur convallis orci dolor, nec aliquet lectus mollis a.</p>
    <br>
    <p>Donec vitae feugiat erat, sed pulvinar erat. Curabitur ut bibendum orci. Maecenas quis leo mi. Aenean eu porttitor est. Nunc aliquam nunc ut mi luctus consectetur. Pellentesque euismod est at.</p>
    <h3>Ett projekt av <a href="https://github.com/williamandersson03/YatzyWeb" target="_blank" rel="noopener noreferrer">William Andersson</a></h3>
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
