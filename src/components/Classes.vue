<template>
    <div id="class-component">
        <h2 class="main-header">VENTAJAS</h2>
        <main>
        <div v-if="windowWidth<768" class="classes-carousel">
            <v-carousel 
            show-arrows-on-hover
            height="auto"
            id="v-carousel">
                <v-carousel-item
                v-for="(card, i) in content"
                :key="i"
                >
                <v-sheet
                    light
                    tile
                >
                    <v-row
                    class="fill-height"
                    align="center"
                    justify="center"
                    >
                    <div class="display-3" id="carousel-card">
                        <Card 
                        :image="card.image"
                        :title="card.title"
                        :summary="card.summary"
                        :content="card.content"
                        />
                    </div>
                    </v-row>
                </v-sheet>
                </v-carousel-item>
            </v-carousel>
        </div>
        <div v-else class="classes">
            <Card 
            v-for="(card, i) in content"
            :key="i"
            :image="card.image"
            :title="card.title"
            :summary="card.summary"
            :content="card.content"
            />
        </div>
        </main>
    </div>
</template>

<style lang="scss" scoped>
    #class-component {
        padding: 50px 0;
        padding-top: 110px;
        background-color: $dark-theme-background2;
        min-height: 100vh;
        color: $main-font-color;
        @media (min-width: $breakpoint-tablet) {
            padding: 50px 40px;
            padding-top: 140px;
        }
        @media (min-width: $breakpoint-desktop) {
            padding-top: 110px;
        }
    }
    .main-header {
        font-family: $section-main-title-font;
        font-size: 30px;
        margin: auto;
        text-align: center;
        @media (min-width: $breakpoint-desktop) {
            font-size: 72px;
        }
    }
    main {
        min-height: 85vh;
        display: flex;
        align-items: center;
    }
    // mobile view
    #v-carousel {
        padding: 100px 0;
    }
    .classes-carousel {
        width: 90%;
        margin: 0 auto;
        .div.row.fill-height {
            margin: 0;
        }
        .display-3 {
            width: 100%;
        }
        .v-sheet
        {
            background-color: $dark-theme-background;
        }
    }
    // tablet and desktop view
    .classes {
        margin: 0 auto;
        width: 90%;  
        display: flex;
        flex-wrap: wrap;
        @media (min-width: $breakpoint-tablet) {
            width: 100%;
            max-width: 970px;
        }
        @media (min-width: $breakpoint-desktop) {
            max-width: 100%;
        }
    }
</style>

<script>
import Card from "./ClassCard"
export default {
    components: {
        Card,
    },
    data: () => ({
      windowWidth: 0,
      content: [
            {
                title: 'Ventaja 1',
                image: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
                summary: "1,000 miles of wonder",
                content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
            },
            {
                title: 'Ventaja 2',
                image: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
                summary: "1,000 miles of wonder",
                content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
            },
            {
                title: 'Ventaja 3',
                image: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
                summary: "1,000 miles of wonder",
                content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
            },
            {
                title: 'Ventaja 4',
                image: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
                summary: "1,000 miles of wonder",
                content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
            },
      ]
    }),
    created() {
        this.setWindowWidth()
        window.addEventListener('resize', () => {
        this.setWindowWidth()
      })
    },
    methods: {
        setWindowWidth() {
        this.windowWidth = window.innerWidth
        },
    }
}
</script>