<template>
  <footer>
    <div class="footer-mainSection">
      <div class="footer-leftSection">
        <p class="footer-title">@MARCA</p>
        <p>
          @MARCA Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent a
          viverra magna. Maecenas vitae est nunc. Phasellus vitae odio posuere, cursus
          purus id, faucibus metus. Cras posuere porttitor elit. Etiam dignissim, purus
          nec suscipit pretium.
        </p>
      </div>
      <div class="footer-middleSection">
        <p class="footer-title">CONTÁCTANOS</p>
        <p>
          TELÉFONO: +57 312-555-3333 <br />
          EMAIL: info@marca.com <br />WHATSAPP:
          <a
            class="footer-whatsAppLink"
            href="https://api.whatsapp.com/send?phone=+57 312 555 3333&text=Hola%20me%20gustaría%20saber%20más"
          >
            Click aquí
          </a>
        </p>
      </div>
      <div class="footer-rightSection">
        <p class="footer-title">Siguenos</p>
        <div class="footer-icons">
          <a href="#"
            ><i class="fab fa-facebook fa-lg"></i
          ></a>
          <a href="#">
            <i class="fab fa-instagram fa-lg"></i>
          </a>
          <a href="#">
            <i class="fab fa-youtube fa-lg"></i>
          </a>
          <a href="https://github.com/Manuel-2011/EcommerceWebPage">
            <i class="fab fa-github fa-lg"></i>
          </a>
        </div>
      </div>
    </div>
    <p class="footer-copyRight">
      2020 &copy; Nombre Marca
    </p>
  </footer>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>
* {
  margin-bottom: 0.5rem;
  text-align: center;
  @media screen and (min-width: $breakpoint-desktop) {
    text-align: start;
  }
}

footer {
  color: $main-font-color;
  background: $main-background-color;
  display: inline-block;
  font-family: $footer-main-font;
  margin: 0;
  padding: 3rem 0;
  width: 100%;

  .footer-mainSection {
    @media screen and (min-width: $breakpoint-desktop) {
      display: flex;
      width: 100%;
      justify-content: space-evenly;
      align-items: flex-start;
    }
  }

  .footer-title {
    font-family: $footer-title-font;
  }

  .footer-copyRight {
    font-family: $footer-copyRigth-font;
    padding: 0.8rem;

    @media screen and (min-width: $breakpoint-desktop) {
      text-align: center;
    }
  }

  .footer-leftSection,
  .footer-middleSection,
  .footer-rightSection,
  .copy,
  .footer-icons {
    align-items: center;
    margin: 0.5rem;
    padding: 0.8rem;

    @media screen and (min-width: $breakpoint-desktop) {
      align-items: flex-start;
    }
  }

  .footer-leftSection {
    @media screen and (min-width: $breakpoint-desktop) {
      width: 20%;
    }
  }

  .footer-rightSection {
    display: flex;
    flex-direction: column;

    @media screen and (min-width: $breakpoint-desktop) {
      width: 20%;
      align-items: center;
    }
  }

  .footer-icons {
    display: flex;
    height: 0;
    justify-content: space-evenly;
    width: 100%;

    @media screen and (min-width: $breakpoint-tablet) and (max-width: $breakpoint-desktop) {
      width: 40%;
    }
  }

  .footer-copyRightLink,
  .footer-whatsAppLink {
    &:hover {
      color: $main-links-color;
      border-bottom: 1px solid;
    }
  }

  i {
    @media screen and (min-width: $breakpoint-desktop) {
      font-size: 2vw;
      padding: 0 2rem;
    }

    @media screen and (min-width: $breakpoint-desktopLarge) {
      font-size: 1vw;
    }

    &:hover {
      color: $main-links-color;
    }
  }
}
</style>
