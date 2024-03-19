<template>
  <div class="gdpr-container">
    <section class="gdpr-section">
      <h1 class="text">Datahantering</h1>
      <p class="gdpr-intro">Denna sida är ett personligt projekt av William Andersson, och jag åtar mig att skydda integriteten för mina användare. Nedan beskrivs hur data hanteras i detta projekt.</p>
    </section>
    <section class="gdpr-section">
      <h2>Insamling av information</h2>
      <p>Information som samlas in inkluderar användarnamn, e-postadress och lösenord (hashat och saltat). Speldata, såsom poäng, betraktas inte som personlig information men hanteras med hög säkerhet.</p>
    </section>
    <section class="gdpr-section">
      <h2>Användning av information</h2>
      <p>Informationen används för att förbättra tjänsten, skydda användare och för kommunikation.</p>
    </section>
    <section class="gdpr-section">
      <h2>Säkerhet</h2>
      <p>Lämpliga säkerhetsåtgärder tas för att skydda din information.</p>
      <p>All känslig information hashas och saltas för maximal säkerhet.</p>
    </section>
    <section class="gdpr-section">
      <h2>Dina rättigheter</h2>
      <p>Du har rätt till tillgång, rättelse och radering av dina personuppgifter. Kontakta mig för dessa ändamål.</p>
      <p>E-post: <a href="mailto:williamandersson08@gmail.com">williamandersson08@gmail.com</a></p>
      <p>För radering av din data, klicka <RouterLink to="/deleteme">HÄR.</RouterLink></p>
    </section>
    <section class="gdpr-section">
      <h2>Ändringar i denna policy</h2>
      <p>Eventuella ändringar i datahanteringspolicyn kommer att kommuniceras.</p>
    </section>
  </div>
</template>

<style scoped>
@import '../assets/defaultviewstyle.css';

.header, .gdpr-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.text, .gdpr-intro, .gdpr-section h2, .gdpr-section p {
  text-align: center;
}

.gdpr-container {
  max-width: 800px; /* Or your desired max-width */
  margin: 2rem auto;
  padding: 1rem;
  background-color: rgba(255, 255, 255, 0.1); /* Or your desired background */
  border-radius: 10px;
}

.gdpr-section {
  margin-bottom: 2rem;
}

@media (max-width: 1023px) {
  .image {
    width: 200px; /* Adjust the size as per your requirement */
    height: 200px; /* Adjust the size as per your requirement */
  }
}

@media (min-width: 1024px) {
  .image {
    width: 300px; /* Adjust the size as per your requirement */
    height: 300px; /* Adjust the size as per your requirement */
  }
}
</style>
