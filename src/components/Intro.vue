<template>
  <div id="intro">
    <section id="intro-parkour">
      <h2 class="section-header">¿Quiénes somos?</h2>
      <p class="section-body">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras sit amet
        finibus sem, a laoreet quam. Vivamus non orci vel eros bibendum gravida
        nec eget leo. Donec nec euismod nibh. Curabitur lacinia erat non arcu
        sodales, ut fringilla mauris fringilla. Vivamus neque felis, ornare eget
        volutpat eu, rhoncus in risus. Morbi vitae augue vitae metus ornare
        tempus sit amet in nibh. Donec ac lacus leo.
      </p>
      <iframe
        width="556"
        src="https://www.youtube.com/embed/ADj7Nyyh8IM"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </section>
    <div class="aside">
      <section id="benefits">
        <h2 class="section-header">Beneficios</h2>
        <p class="section-body">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras sit amet
          finibus sem, a laoreet quam. Vivamus non orci vel eros bibendum
          gravida nec eget leo. Donec nec euismod nibh. Curabitur lacinia erat
          non arcu sodales, ut fringilla mauris fringilla.
        </p>
      </section>
      <section id="classes">
        <h2 class="section-header">Productos</h2>
        <p class="section-body">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras sit amet
          finibus sem, a laoreet quam. Vivamus non orci vel eros bibendum
          gravida nec eget leo. Donec nec euismod nibh. Curabitur lacinia erat
          non arcu sodales, ut fringilla mauris fring.
        </p>
        <button
          id="button-classes"
          @click="function () {window.location = '/#class-component'}"
          
        >
          CONOCE MÁS
        </button>
      </section>
    </div>
  </div>
</template>

<style lang="scss" scoped>
#intro {
  padding: 50px 0;
  padding-top: 110px;
  background-color: $dark-theme-background;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: $main-font-color;
  @media (min-width: $breakpoint-tablet) {
    padding-top: 140px;
  }
  @media (min-width: $breakpoint-desktop) {
    padding-top: 110px;
    padding-left: 40px;
    padding-right: 40px;
    height: 100vh;
    overflow-y: hidden;
    display: grid;
    grid-template-columns: 7fr 5fr;
    grid-template-areas: "main aside";
    column-gap: 20px;
  }
}
section {
  width: 90%;
  margin: 10px 0;
  padding: 20px;
  border-radius: 4px;
  background-color: $dark-theme-surface;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 11px 15px -7px rgba(0, 0, 0, 0.2);
  @media (min-width: $breakpoint-tablet) {
    width: 100%;
  }
  @media (min-width: $breakpoint-desktop) {
    width: 100%;
    margin: 0;
    height: 100%;
  }
  .section-header {
    margin-bottom: 10px;
    font-family: $section-title-font;
    font-size: 18px;
    @media (min-width: $breakpoint-desktop) {
      font-size: 36px;
      margin-bottom: 65px;
    }
  }
  .section-body {
    margin: 20px 0;
    font-family: $section-body-font;
    font-size: 12px;
    line-height: 20px;
    letter-spacing: 0.5px;
    max-width: 600px;
    @media (min-width: $breakpoint-desktop) {
      font-size: 18px;
      width: 80%;
      line-height: 25px;
    }
  }
  iframe {
    width: 100%;
    max-width: 600px;
    height: 153px;
    margin: 25px 0;
    @media (min-width: $breakpoint-tablet) {
      height: 250px;
    }
    @media (min-width: $breakpoint-desktop) {
      width: 80%;
      height: 335px;
    }
  }
}
#intro-parkour {
  @media (min-width: $breakpoint-tablet) {
    width: 90%;
  }
  @media (min-width: $breakpoint-desktop) {
    width: 100%;
    grid-area: main;
    .section-body,
    iframe {
      max-width: 850px;
    }
  }
}
.aside {
  display: grid;
  justify-items: center;
  width: 100%;
  @media (min-width: $breakpoint-tablet) {
    width: 90%;
    grid-template-columns: 1fr 1fr;
    column-gap: 20px;
  }
  @media (min-width: $breakpoint-desktop) {
    width: 100%;
    height: 100%;
    grid-area: aside;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: auto;
    row-gap: 20px;
  }
  .section-header {
    @media (min-width: $breakpoint-desktop) {
      margin-bottom: 30px;
    }
  }
}
button {
  padding: 10px 20px;
  border: 3px solid $main-font-color;
  color: $main-font-color;
  background-color: $main-background-color;
  cursor: pointer;
  font-family: $section-title-font;
  transition: 0.5s;
  font-size: 10px;
  &:hover {
    background-color: $secondary-background-color;
    color: $secondary-font-color;
  }
  @media (min-width: $breakpoint-desktop) {
    font-size: 14px;
  }
}
</style>

<script>
export default {
  data() {
    return {
      window: "",
    };
  },
  created() {
    this.window = window;
  },
};
</script>
