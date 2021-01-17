<template>
  <div id="home-component">
    <div class="layer">
        <h1>NOMBRE MARCA</h1>
        <div class="subtitle">
        <div class="point"></div>
        <h4>KEEP MOVING</h4>
        <div class="point"></div>
        </div>
        <button id="principal-button">IR A PRODUCTOS</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
    #home-component {
        font-size: 10px;
        width: 100%;
        height: 100vh;
        padding-top: 1px;
        background-image: url('../assets/images/background-wallpaper.jpg');
        background-size: cover;
        @media (max-width: $breakpoint-columns) {
            font-size: 5px;
        }
    }
    .layer {
        width: 100%;
        height: 100vh;
        background-color: rgba(0,0,0,0.2);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    /* Titutlo principal */
    h1 {
        display: inline-block;
        margin-top: -70px;
        margin-bottom: -5px;
        font-family: $section-main-title-font;
        text-align: center;
        width: 6em;
        font-size: 11em;
        letter-spacing: -0.04em;
        color: $main-font-color;
    }
    /* Subtitulo */
    .subtitle {
        width: 50em;
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 20em;
        margin-bottom: 30px;
        color: $main-font-color;
        @media (max-width: $breakpoint-columns) {
            font-size: 2em;
        }
    }
    .subtitle h4 {
        font-family: $section-title-font;
        font-size: 1.5em;
        text-align: center;
    }
    .point {
        background-color: $main-font-color;
        width: 1em;
        height: 1em;
        border-radius: 50%;
    }
    /* Boton principal */
    button {
        padding: 10px 20px;
        border: 3px solid $main-font-color;
        color: $main-font-color;
        background-color: $main-background-color;
        cursor: pointer;
        font-family: $section-button-font;
        transition: 0.5s;
        font-size: 10px;
        &:hover {
            background-color: $secondary-background-color;
            color: $secondary-font-color;
        }
    }

#principal-button {
  font-size: 2em;
  width: 16em;
  margin-bottom: 75px;
}
</style>

<script>
export default {};
</script>
