<template>
  <div id="contact-component">
    <address class="contact-section">
      <h1 class="contact-tittle">CONTÁCTANOS</h1>
      <div class="contact-main-section">
        <div class="contact-phone">
          <i class="fas fa-phone-alt"></i>
          <p>312-555-3333</p>
        </div>
        <div class="contact-email">
          <i class="far fa-envelope"></i>
          <p>info@marca.com</p>
        </div>
      </div>
    </address>
    <div class="question-section">
      <h1 class="contact-tittle">TIENES ALGUNA DUDA?</h1>
      <form class="questions-main-section">
        <p class="question-title">Nombre *</p>
        <textField :length="12" :message="'Name'" :heigth="'1rem'" />
        <p class="question-title">Email *</p>
        <textField :length="12" :message="'Email'" :heigth="'1rem'" :rule="emailRules" />
        <p class="question-title">Mensaje *</p>
        <textField
          :length="12"
          :message="'Message'"
          :heigth="'10rem'"
          :rule="messageRules"
        />
      </form>
      <div class="contact-button">
        <button type="submit">Enviar</button>
      </div>
    </div>
  </div>
</template>

<script>
import textField from "./Text-field";
export default {
  components: {
    textField,
  },
  data() {
    return {
      email: "",
      emailRules: [
        (v) => !!v || "E-mail is required",
        (v) =>
          /^(([^<>()[\]\\.,;:\s@']+(\.[^<>()\\[\]\\.,;:\s@']+)*)|('.+'))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/.test(
            v
          ) || "E-mail must be valid",
      ],
      messageRules: [
        (v) => (v || "").length <= 200 || "Description must be 200 characters or less",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
#contact-component {
  background-color: $dark-theme-background2;
  color: $main-font-color;
  font-family: $contact-main-font;
  padding: 4rem 1rem;

  @media screen and (min-width: $breakpoint-desktop) {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
}
.contact-section {
  background-color: $dark-theme-surface;
  border-radius: 10px;
  box-sizing: border-box;
  margin: 2rem 0;
  padding: 1rem;
  width: 100%;

  @media screen and (min-width: $breakpoint-desktop) {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 1.5rem;
    width: 50%;
  }

  .contact-main-section {
    display: flex;
    justify-content: space-around;
    padding: 2rem 0;

    @media screen and (min-width: $breakpoint-desktop) {
      align-items: center;
      flex-direction: column;
      padding: 0;
    }
  }

  .contact-tittle {
    font-family: $contact-title-font;
    font-size: 1.2rem;
    padding: 1rem;
    text-align: center;

    @media screen and (min-width: $breakpoint-tablet) and (max-width: $breakpoint-desktop) {
      font-size: 1.5rem;
    }

    @media screen and (min-width: $breakpoint-desktop) {
      font-size: 2rem;
      margin: 1rem 0;
    }
  }

  .contact-phone,
  .contact-email {
    align-items: center;
    display: flex;
    flex-direction: column;
    font-size: 0.9rem;
    width: 50%;

    @media screen and (min-width: $breakpoint-tablet) and (max-width: $breakpoint-desktop) {
      font-size: 1.3rem;
    }

    @media screen and (min-width: $breakpoint-desktop) {
      display: flex;
      font-size: 1.8rem;
      flex-direction: row;
      justify-content: center;
      padding: 2rem 0;
      width: 25rem;
    }

    p {
      font-family: $contact-text-font;
      padding-top: 1rem;

      @media screen and (min-width: $breakpoint-desktop) {
        padding: 0;
        margin: 0;
      }
    }
    i {
      padding: 0 1rem;

      @media screen and (min-width: $breakpoint-desktop) {
        align-self: center;
      }
    }
  }

  .contact-phone {
    border-right: 3px solid white;

    @media screen and (min-width: $breakpoint-desktop) {
      border-right: none;
      border-top: 2px solid white;
      border-bottom: 2px solid white;
      padding: 3rem 0;
    }
  }
}

.question-section {
  background-color: $dark-theme-surface;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  margin: 2rem 0;
  padding: 1rem;
  width: 100%;

  @media screen and (min-width: $breakpoint-desktop) {
    font-size: 1.2rem;
    margin: 1.5rem;
    width: 50%;
  }

  .contact-tittle {
    font-family: $contact-title-font;
    font-size: 1.2rem;
    padding: 1rem;
    text-align: center;

    @media screen and (min-width: $breakpoint-desktop) {
      font-size: 1.5rem;
    }
  }

  .question-title {
    margin-left: 12px;
    font-family: $contact-text-font;
  }

  .contact-button {
    text-align: center;
    width: 100%;
  }

  button {
    background-color: $main-background-color;
    border: 3px solid $main-font-color;
    color: $main-font-color;
    cursor: pointer;
    font-family: $contact-text-font;
    font-size: 0.8rem;
    margin: auto;
    padding: 0.5rem 2rem;
    transition: 0.5s;

    &:hover {
      background-color: $secondary-background-color;
      color: $secondary-font-color;
    }

    @media screen and (min-width: $breakpoint-tablet) and (max-width: $breakpoint-desktop) {
      font-size: 1rem;
    }

    @media screen and (min-width: $breakpoint-desktop) {
      font-size: 1.2rem;
    }
  }
}
</style>
