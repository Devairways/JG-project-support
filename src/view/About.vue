<template>
  <section id="about">
    <div class="container">
      <h1 class="header">Over Ons</h1>
      <div class="subtext">
        <h2>Opgericht in 2021</h2>
        <p>
          <span class="company_name">JG project-support</span> is opgericht door
          <span class="founder"> Ing. Jimmy Gloudemans</span> in 2021 op Bonaire
          en ontstaan vanuit het gedachtegoed hoe een project op een effectieve
          manier aangestuurd kan worden. De opgedane kennis en ervaringen binnen
          energieprojecten hebben invloed gehad op het vormen van zijn denk- en
          werkwijze. Rationeel denken, eigenaarschap en adaptatievermogen staan
          hierin centraal.
        </p>
      </div>
      <Card>
        <h2>Waarom JG project-support</h2>
        <p>
          De afgelopen 10 jaar zijn projecten meer multidisciplinair geworden en
          daarmee ook complexer. Een ander soort aansturing wordt gevraagd dat
          verbindingen legt tussen verschillende projectaspecten. Een project
          support office (PSO) geeft hier antwoord op. JG project-support denkt
          graag met u mee waarin uw project aangevuld kan worden.
        </p>
      </Card>
      <h2>Onze kernwaarden</h2>
      <div class="values">
        <Card>
          <img src="img/balance.png" alt="balance" />
          <h3>Balans</h3>
          <p>
            Ruim 10 jaar ervaring binnen de energiemarkt wordt ingezet om het
            project tot een succes te maken. JG project-support is praktisch en
            theoretisch opgeleid om balans te vinden tussen de behoefte van de
            operatie en het management.
          </p>
        </Card>
        <Card>
          <img src="img/empathy.png" alt="empathy" />
          <h3>Inlevingsvermogen</h3>
          <p>
            JG project-support past zich aan naar de omstandigheden van elk
            klein of groot project. De sleutel tot succes ligt bij het
            meebewegen met de project dynamiek.
          </p>
        </Card>
        <Card>
          <img src="img/human.png" alt="human" />
          <h3>Rationaliteit</h3>
          <p>
            JG project-support stelt zich op als sparringspartner om tijdens het
            verloop van het project rationele en concrete beslissingen te nemen.
            Samen gaan we de uitdaging aan.
          </p>
        </Card>
        <Card>
          <img src="img/heart.png" alt="loyalty" />
          <h3>Loyaliteit</h3>
          <p>
            Partnerschap betekent voor JG project-support een duurzame en
            innovatieve relatie, gebaseerd op eigenaarschap en loyaliteit dat
            voor een langdurige samenwerking zorgt
          </p>
        </Card>
      </div>
      <div>
        JG project-support denkt graag met u mee in de gewenste aansturing voor
        uw project. Meer weten? Neem contact op!
      </div>
    </div>
  </section>
</template>

<script>
import Card from "@/components/card/Card.vue";

export default {
  name: "About",
  components: { Card },
};
</script>

<style lang="scss" scoped>
#about {
  h3 {
    color: #ff4d58;
  }

  .company_name {
    color: #ff4d58;
    font-weight: 900;
  }

  .founder {
    color: #000;
  }

  img {
    width: 80px;
  }

  @media only screen and (min-width: 768px) {
    .values {
      display: flex;
      flex-wrap: wrap;

      .card {
        width: 40%;
        min-width: 295px;
      }
    }
  }
}
</style>
