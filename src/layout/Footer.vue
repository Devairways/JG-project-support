<template>
  <footer>
    <div class="contactinfo">
      <ul class="contacts">
        <li>Contact</li>
        <li>
          <i class="fas fa-phone"></i>
          <p>+599 7900002</p>
        </li>
        <li>
          <i class="far fa-envelope"></i>
          <p>info@jgprojectsupport.com</p>
        </li>
        <li>
          <i class="fas fa-map-marker-alt"></i>
          <p>Bonaire</p>
        </li>
      </ul>
      <div class="additional">
        <ul>
          <li>Ma-Vr: 7:00 am - 4:00 pm</li>
          <li>Za-Zo: Alleen op afspraak</li>
        </ul>
        <ul class="certification">
          <li><img src="img/GPI-logo.png" alt="" class="GPI-logo" /></li>
          <li><img src="img/VCA-logo.png" alt="" class="VCA-logo" /></li>
          <li>
            <img src="img/NEN3140-logo.png" alt="" class="NEN3140-logo" />
          </li>
          <li><img src="img/Boels-logo.png" alt="" class="Boels-logo" /></li>
        </ul>
      </div>
      <ul class="icons">
        <li>
          <a
            href="https://api.whatsapp.com/send?phone=+5997900002"
            target="_blank"
            ><i class="fab fa-whatsapp"></i
          ></a>
        </li>
        <li>
          <a href="mailto: info@jgprojectsupport.com"
            ><i class="far fa-envelope"></i
          ></a>
        </li>
        <li>
          <a href="https://www.linkedin.com/mwlite/in/jimmy-g-87a18810b"
            ><i class="fab fa-linkedin-in"></i
          ></a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
footer {
  padding: 10px;
  background: #1a1a1d;
  margin-top: 20px;
  color: #fff;

  .contactinfo {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 25px;
  }

  .certification {
    display: flex;
    margin: auto;

    li {
      width: 45%;
      max-width: 100px;
      padding: 5px;

      &:nth-child(4) {
        img {
          padding-top: 6px;
        }
      }
    }
    img {
      width: 100%;
    }
  }

  .contacts {
    width: 215px;

    li {
      display: flex;
      flex-direction: row;
      align-items: center;

      p {
        margin: 5px 0;
        padding-left: 10px;
      }
    }
  }

  .icons {
    width: 100%;
    margin: auto;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;

    li {
      padding: 0 10px;

      i {
        color: #fff !important;
      }

      &:nth-child(3) {
        margin-bottom: 2px;
      }
    }
  }
  @media only screen and (min-width: 768px) {
    .contactinfo {
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-evenly;
      align-items: unset;
    }

    .certification {
      flex-wrap: wrap-reverse;
      width: 205px;
    }
  }
}
</style>
