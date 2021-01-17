<template>
    <v-card
        class="mx-auto"
        id="card"
        elevation="24"
    >
        <v-img
        :src="image"
        height="200px"
        ></v-img>

        <v-card-title>
        {{ title }}
        </v-card-title>

        <v-card-subtitle>
        {{ summary }}
        </v-card-subtitle>

        <v-card-actions>
        <v-btn
            id="button-reserve"
            text
            :href="'https://api.whatsapp.com/send?phone=+57 312 555 3333&text=Hola!%20Me%20gustar%C3%ADa%20tener%20m%C3%A1s%20informaci%C3%B3n%20sobre%20sus%20productos%20'"
            target="_blank"
        >
            COMPRAR
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn
            icon
            @click="show = !show"
        >
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
        </v-card-actions>

        <v-expand-transition>
        <div v-show="show">
            <v-divider></v-divider>

            <v-card-text>
            {{ content }}
            </v-card-text>
        </div>
        </v-expand-transition>
    </v-card>
</template>

<style lang="scss" scoped>
    div.mx-auto.v-card {
        width: 90%;
        max-width: 325px;
        margin: 10px;
    }
    #card {
        height: 100%;
    }
    #card,
    #card div,
    .v-btn.v-btn--flat.v-btn--icon
    {
        background-color: $dark-theme-surface;
        color: $main-font-color;
        font-family: $section-body-font;
        font-size: 12px;
        @media (min-width: $breakpoint-desktop) {
            font-size: 18px;
        }
    }
    #button-reserve {
        color: $main-links-color;
        font-family: $section-button-font;
        font-size: 10.15px;
        @media (min-width: $breakpoint-desktop) {
            font-size: 15px;
        }
    }
    #card .v-card__title {
        font-family: $section-title-font;
        font-size: 18px;
        @media (min-width: $breakpoint-desktop) {
            font-size: 24px;
        }
    }
    #card .v-card__subtitle {
        padding-top: 25px;
    }
</style>

<script>
export default {
    props: ['image', 'title', 'summary', 'content'],
    data: () => ({
      show: false,
    }),
}
</script>