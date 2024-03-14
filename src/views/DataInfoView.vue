<template>
  <div class="gdpr-container">
    <section class="gdpr-section">
      <h1 class="text">Datahantering</h1>
      <p class="gdpr-intro">Denna sida är ett personligt projekt av William Andersson, och jag är åtagen till att skydda integriteten för mina användare. Nedan beskrivs hur data hanteras i detta projekt.</p>
    </section>
    <section class="gdpr-section">
      <h2>Insamling av information</h2>
      <p>Information som samlas in inkluderar användarnamn, e-postadress och lösenord (krypterat). Speldata som poäng betraktas inte som personlig information men hanteras med hög säkerhet.</p>
    </section>
    <section class="gdpr-section">
      <h2>Användning av information</h2>
      <p>Informationen används för att förbättra tjänsten, skydda användare och för kommunikation.</p>
    </section>
    <section class="gdpr-section">
      <h2>Säkerhet</h2>
      <p>Lämpliga säkerhetsåtgärder tas för att skydda din information.</p>
    </section>
    <section class="gdpr-section">
      <h2>Dina rättigheter</h2>
      <p>Du har rätt till tillgång, rättelse, och radering av dina personuppgifter. Kontakta mig för dessa ändamål.</p>
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
  margin: 0.5rem;
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