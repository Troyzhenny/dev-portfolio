<script>
import { ref } from 'vue';

export default {
    setup() {
        const footerLinks = ref([
            { name: "Github", url: "https://github.com/Troyzhenny" },
            { name: "LinkedIn", url: "https://www.linkedin.com/in/tevin-campbell/" }
        ]);

        const mailLinks = ref([
            { name: "tevincampbell73@yahoo.com", url: "mailto:tevincampbell@yahoo.com" }
        ]);

        return {
            footerLinks,
            mailLinks
        }
    }
}
</script>

<template>
    <section class="contact--container" id="contact">
        <div class="heading--cont">
            <h2>GET IN TOUCH</h2>
        </div>
        <div class="social--container">
            <div class="socialLinks">
                <h3>CONTACT INFO</h3>
                <span>
                    <a v-for="(mailLink, index) in mailLinks" :key="index" :href="mailLink.url">
                        <i class="fa-solid fa-envelope"></i>
                        <p>{{ mailLink.name }}</p>
                    </a>
                </span>
                <br>
                <h3>MY DIGITAL SPACES</h3>
                <span>
                    <a v-for="(footerLink, index) in footerLinks" :key="index" :href="footerLink.url" target="_blank">
                        <i class="fa-brands fa-linkedin-in"></i>
                        <p>{{ footerLink.name }}</p>
                    </a>
                </span>
            </div>
        </div>
        <div class="form--container">
            <form action="#" method="post">
                <label for="name">Your Name *</label>
                <input type="text" id="name" name="name" placeholder="Dan Houser" required>

                <label for="email">Email *</label>
                <input type="email" name="email" id="email" placeholder="dh@rockstargames.com" required>

                <label for="message">Message *</label>
                <textarea name="message" id="message" cols="50" rows="4" placeholder="Hey Tevin, we're reaching out to. . ."
                    required></textarea>

                <input type="button" id="submit-btn" value="Submit">
            </form>
        </div>
    </section>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.contact--container {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    min-height: 100vh;

    color: $darkGray;
    background-color: $light;


    .heading--cont {
        width: 100%;

        h2 {
            margin: 60px;
            font-size: 5em;
        }
    }


    .social--container {
        display: flex;
        width: 100%;
        min-height: 100%;

        .socialLinks {
            display: flex;
            flex-direction: column;
            gap: 30px;

            h3 {
                color: $dark;
                font-size: 1.8em;
            }

            span>a {
                font-size: 1.5em;
                color: $lightGray;
                display: flex;
                place-items: center;
                margin-bottom: 1rem;
                gap: 1rem;
            }
        }
    }

    .form--container {
        display: flex;
        place-items: center;
        min-height: 100%;

        form {
            width: 100%;
            height: 100%;

            label {
                font-size: 1.5em;
                font-weight: 600;
                margin: 10px 0;
                position: relative;
                color: $dark;
            }

            input,
            textarea {
                font-size: 1.2em;
                font-weight: 600;
                color: $darkGray;
                padding: 15px;
                margin-bottom: 20px;
                width: 100%;
                outline: transparent;
                border-radius: 5px;
                background-color: transparent;
                border: .13rem solid $mainColor;

                &:focus {
                    background-color: $focus;
                }
            }

            #submit-btn {
                width: 150px;
                margin-top: 40px;
                cursor: pointer;
                font-weight: 600;
                color: $dark;
                border: 2px solid $mainColor;
                background-color: $mainColor;

                &:hover {
                    color: $mainColor;
                    background-color: transparent;
                    border: 2px solid $mainColor;
                    transition: .5s ease-in-out;
                }
            }
        }
    }
}



// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
    .contact--container {
        .heading--cont>h2 {
            font-size: 3em;
            margin: 50px;
        }
    }
}
</style>