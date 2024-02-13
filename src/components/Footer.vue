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
            {name: "Discord: @troyzhen"}
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
                <h3>Links</h3>
                <span>
                    <a v-for="(footerLink, index) in footerLinks" :key="index" :href="footerLink.url" target="_blank">
                        <p>{{ footerLink.name }}</p>
                    </a>
                </span>
            </div>
            <div id="sq2">
                <h3>Contact</h3>
                <span>
                    <a v-for="(mailLink, index) in mailLinks" :key="index" :href="mailLink.url">
                        <p>{{ mailLink.name }}</p>
                    </a>
                </span>
            </div>
            <div class="to--top">
                <a href="#home">
                    <i class="fa-solid fa-shuttle-space"></i>
                    <p>BLAST OFF</p>
                </a>
            </div>
        </div>
        <div class="copyright--container">
            <p>©2024 Tevin Campbell  — built with Vue and lots of 💖</p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.footer--container {
    display: flex;
    flex-wrap: wrap;
    place-items: center;
    width: 100%;
    min-height: 100%;
    color: $mainColor;
    background-color: $darkGray;

    border: 1px solid $mainColor;


    .links--container {
        display: flex;
        place-items: center;
        justify-content: space-between;
        padding: 40px;
        width: 100%;
        min-height: 100%;
        color: $lightGray;

    border: 1px solid $mainColor;


        :is(#sq1, #sq2) {
            display: flex;
            justify-content: center;
            flex-direction: column;
            width: 100%;
            min-height: 100%;
            
            border: 1px solid $mainColor;
            
            
            h3 {
                color: $light;
                font-size: 1em;
                margin-bottom: 10px;
            }

            span > a  {
                display: flex;
                place-items: center;
                margin-bottom: 15px;
                font-size: 1em;
                gap: 8px;
                color: $lightGray;
                &:hover {
                    color: $mainColor;
                }
            }
        }
    }
    .to--top a {
        display: flex;
        place-items: center;
        justify-content: center;
        width: 100%;
        min-height: 100%;
        gap: 5px;
    
        border: 1px solid $mainColor;
    
    
        .fa-shuttle-space {
            font-size: 2em;
            transform: rotateZ(-90deg);
            color: $lightGray;
    
            &:hover {
                color: $mainColor;
                transform: rotate(-90deg) translateX(20px);
                transition: .3s ease-in-out;
            }
        }
    
        p {
            font-weight: 500;
            color: $lightGray;
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
    }
}
</style>