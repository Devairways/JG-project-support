<template>
  <Header />
  <section id="services">
    <div class="container">
      <h1 class="header">Diensten</h1>
      <p class="subtext">
        Opgedaan door de vele projecten en aangevuld met diverse opleidingen en
        trainingen.  Expertise blijft groeien door continue bij te leren en
        kennis en kunde te delen.
      </p>
      <card class="service_card">
        <img src="img/coaching.png" alt="coaching" />
        <div>
          <h2>Coaching en begeleiding</h2>
          <p>
            We helpen graag uw organisatie mee in de gekozen strategie. Advies
            en aansturing vindt plaats aan de warme en koude kant van de
            verandering. Persoonlijk contact en intensieve begeleiding zorgen
            voor nieuw eigenaarschap en een succesvolle transitie.
          </p>
        </div>
      </card>
      <card class="service_card">
        <img src="img/business-intelligence.png" alt="Business-intelligence" />
        <div>
          <h2>Business Intelligence</h2>
          <p>
            Het verzorgen van de juiste dashboards met concrete KPI's aan de
            hand van zuivere data en/of bronnen vraagt om maatwerk.
            Verschillende software pakketten zijn hiervoor te gebruiken. JG
            project-support biedt dienstverlening in het opstellen, uitwerken en
            implementeren hiervan.
          </p>
        </div>
      </card>
      <card class="service_card">
        <img src="img/task-planning.png" alt="task-planning" />
        <div>
          <h2>Projectplanning</h2>
          <p>
            Bij elk project is een projectplanning crusiaal en geeft de
            mogelijkheid om te sturen. Het goed opzetten en bijhouden van deze
            planning bepaalt mede of het project succesvol afgerond kan worden.
            JG project-support biedt dienstverlening voor verschillende
            planningsoftware pakketten.
          </p>
        </div>
      </card>
    </div>
  </section>
</template>

<script>
import Card from "../components/card/Card.vue";
export default {
  components: { Card },
  name: "Services",
};
</script>

<style lang="scss" scoped>
#services {
  background: #f6f6fb;
  clip-path: polygon(0 4%, 100% 0, 100% 96%, 0 100%);
  padding: 75px 0;

  h2 {
    color: #ff4d58;
  }

  @media only screen and (min-width: 768px) {
    .service_card {
      display: flex;
      align-items: center;

      &:nth-of-type(2) {
        flex-direction: row-reverse;
        div {
          padding-right: 25px;
          text-align: right;
        }
      }

      div {
        padding-left: 25px;
        text-align: left;
      }
    }

    img {
      height: 135px;
    }
  }
}
</style>
