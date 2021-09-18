<template>
  <section id="contact">
    <div class="container">
      <h1 class="header">Contact opnemen</h1>
      <p class="subtext">
        Voor meer informatie kunt u uw contactgegevens invullen.  Dan nemen wij
        contact met u op.
      </p>
      <form>
        <label for="name">Naam</label>
        <input type="text" id="name" />
        <label for="email">Email</label>
        <input type="email" id="email" />
        <label for="phone">Telefoon</label>
        <input type="tel" id="phone" />
        <label for="msg">Bericht</label>
        <textarea type="text" id="msg" />
        <button>Indienen</button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contact",
};
</script>

<style lang="scss" scoped>
#contact {
  form {
    display: flex;
    flex-direction: column;
    margin: auto;
    width: 80%;

    input,
    textarea {
      height: 38px;
      border: none;
      border-bottom: 1px solid #8c8c8c;
      font-size: 16px;
      &:focus {
        outline: none;
      }
    }

    textarea {
      resize: none;
      height: 175px;
    }

    label {
      text-align: left;
      font-weight: 600;
      font-size: 12px;
      padding-top: 15px;
    }

    button {
      background: #ff4d58;
      width: 45%;
      max-width: 330px;
      height: 40px;
      border: none;
      border-radius: 5px;
      color: #fff;
      margin: 20px 0;
      margin-left: auto;
      font-size: 18px;
    }
  }
}
</style>
