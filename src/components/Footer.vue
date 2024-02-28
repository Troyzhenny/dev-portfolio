<script>
import { ref } from 'vue';

export default {
    setup() {
        const footerLinks = ref([
            { name: "Github", url: "https://github.com/Troyzhenny" },
            { name: "LinkedIn", url: "https://www.linkedin.com/in/tevin-campbell/" }
        ]);

        const mailLinks = ref([
            { name: "tevincampbell73@yahoo.com", url: "mailto:tevincampbell@yahoo.com" },
            { name: "Discord: @troyzhen" }
        ]);

        return {
            footerLinks,
            mailLinks
        }
    }
}
</script>

<template>
    <div class="footer--container">
        <div class="links--container">
            <div id="sq1">
                <div class="block1">
                    <h3>Links</h3>
                    <span>
                        <a v-for="(footerLink, index) in footerLinks" :key="index" :href="footerLink.url" target="_blank">
                            <p>{{ footerLink.name }}</p>
                        </a>
                    </span>
                </div>
            </div>
            <div id="sq2">
                <div class="block2">
                    <h3>Contact</h3>
                    <span>
                        <a v-for="(mailLink, index) in mailLinks" :key="index" :href="mailLink.url">
                            <p>{{ mailLink.name }}</p>
                        </a>
                    </span>
                </div>
            </div>
            <div class="to--top">
                <a href="#home">
                    <p>BLAST OFF</p>
                </a>
            </div>
        </div>
        <div class="copyright--container">
            <p>©2024 Tevin Campbell — built with Vue and lots of 💖</p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.footer--container {
    display: flex;
    flex-wrap: wrap;
    place-items: center;
    justify-content: center;
    width: 100%;
    min-height: 100%;
    color: $mainColor;
    background-color: $darkGray;


    .links--container {
        display: flex;
        flex-wrap: wrap;
        place-items: center;
        justify-content: space-between;
        width: 100%;
        min-height: 100%;
        color: $lightGray;

        :is(#sq1, #sq2) {
            display: flex;
            justify-content: center;
            width: 50%;
            min-height: 100%;
            padding: 50px;


            :is(.block1, .block2) {
                display: flex;
                justify-content: center;
                flex-direction: column;
                width: 100%;
            }


            h3 {
                color: $light;
                font-size: 1.3em;
                margin-bottom: 10px;
            }

            span>a {
                display: flex;
                place-items: center;
                margin-bottom: 15px;
                font-size: .7em;
                gap: 8px;
                color: $lightGray;

                &:hover {
                    color: $mainColor;
                }
            }
        }
    }

    .to--top {
        display: flex;
        justify-content: center;
        width: 100%;
        min-height: 100%;
        padding-top: 50px;
        padding-bottom: 50px;
        gap: 5px;

        a {
            display: flex;
            place-items: center;
            justify-content: center;
        }

        
        p {
            font-weight: 500;
            color: $lightGray;

            &:hover {
                color: $mainColor;
                transition: .3s ease-in-out;
            }
        }
    }
}


.copyright--container {
    display: flex;
    place-items: center;
    justify-content: center;
    padding: 10px;
    width: 100%;
    background-color: $dark;

    p {
        font-size: 1em;
        text-align: center;
        width: 100%;
        min-width: 50%;
        color: $lightGray;
    }
}

// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
    .footer--container {
        .heading--cont>h2 {
            font-size: 3em;
            margin: 50px;
        }

        .links--container {

            #sq1,
            #sq2 {
                display: flex;
                justify-content: center;
                width: 100%;

            }
        }
    }
}
</style>