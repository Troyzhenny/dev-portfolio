<script>
// NAVIGATION
import { onMounted, ref } from 'vue';

export default {
    setup() {
        const links = ref([
            { text: "Home", url: "#home" },
            { text: "About", url: "#about" },
            { text: "Projects", url: "#projects" },
            { text: "Resume", url: "#resume" },
            { text: "Contact", url: "#contact" }
        ]);

        let burgerMenu;
        let offScreenMenu;

        onMounted(() => {
            burgerMenu = document.querySelector(".burger-menu");
            offScreenMenu = document.querySelector(".off-screen-menu");

            // Event listener to close menu when a link is clicked
            offScreenMenu.querySelectorAll("a").forEach(link => {
                link.addEventListener("click", () => {
                    handleMenuToggle();
                });
            });
        });


        const handleMenuToggle = () => {
            if (burgerMenu && offScreenMenu) {
                burgerMenu.classList.toggle("active-ham")
                offScreenMenu.classList.toggle("active-menu")
            }
        }


        return {
            links,
            handleMenuToggle
        };
    },
};

</script>


<template>
    <div>
        <header :class="{ 'menu-open': burgerMenu }">
            <div>
                <a :href="links.length > 0 ? links[0].url : '#home'">
                    <img src="/images/logo-light.svg" id="logo" alt="Tevin's logo icon">
                </a>
            </div>
            <nav>
                <div>
                    <ul>
                        <li v-for="(link, index) in links" :key="index" class="nav-items">
                            <a v-bind:title="`Links to ${link.url}`" v-bind:href="link.url" class="nav-link">{{ link.text
                            }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
            <div class="off-screen-menu">
                <ul>
                    <li v-for="(link, index) in links" :key="index" class="nav-items">
                        <a v-bind:title="`Links to ${link.url}`" v-bind:href="link.url" class="nav-link">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
            <div class="burger-menu" @click="handleMenuToggle">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </header>
    </div>
</template>


<style scoped lang="scss">
@import "../assets/scss/variables";

header {
    top: 0;
    left: 0;
    right: 0;
    height: 50px;
    position: fixed;
    padding: 35px 40px;
    background-color: $dark;
    @include flex-box;
    justify-content: space-between;

    transition: padding-right 0.2s ease;

    &.menu-open {
        padding-right: -450px;
    }

    #logo {
        width: 30px;
    }

    ul {
        @include flex-box;
        gap: 60px;
    }


    nav {
        @include flex-box;
        justify-content: space-between;
    }

    .off-screen-menu {
        height: 100vh;
        width: 100%;
        max-width: 450px;
        position: fixed;
        top: 0;
        right: -450px; //Change to -450px to hide
        background-color: $dark;

        display: flex;
        justify-content: center;
        transition: .2s ease;
        position: absolute;


        ul {
            display: flex;
            flex-direction: column;

            li,
            a {
                color: $light;
            }
        }
    }

    .off-screen-menu.active-menu {
        right: 0px;
    }


    .burger-menu {
        display: none;
        flex-direction: column;
        place-items: left;
        justify-content: center;
        position: relative;
        cursor: pointer;
        width: 40px;
        height: 40px;

        span {
            width: 40px;
            min-height: .2rem;
            background-color: $light;
        }


        span:nth-child(1) {
            width: 25px;
            margin-bottom: 10px;
        }

        span:nth-child(3) {
            width: 20px;
            place-self: flex-end;
            margin-top: 10px;
        }
    }

    .burger-menu.active-ham {

        span:nth-child(1) {
            width: 0%;
            transition: .2s ease;
        }

        span:nth-child(2) {
            transform: rotateZ(-45deg);
            transition: .2s ease;
        }

        span:nth-child(3) {
            width: 100%;
            margin-top: -.2rem;
            transform: rotateZ(45deg);
            transition: .2s ease;
        }

    }
}

// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
    header {
        padding-right: 40px;

        nav {
            ul {
                display: none;
            }
        }

        .burger-menu {
            display: flex;
        }

        .off-screen-menu {
            ul {
                display: flex;
                flex-direction: column;

                li,
                a {
                    font-size: 1.25em;
                    font-weight: 600;
                    color: $light;
                }
            }
        }
    }
}
</style>