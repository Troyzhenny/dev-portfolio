<script>
// NAVIGATION
import { ref } from 'vue';

export default {
    setup() {
        const links = ref([
            { text: "Home", url: "#home" },
            { text: "About", url: "#about" },
            { text: "Projects", url: "#projects" },
            { text: "Resume", url: "#resume" },
            { text: "Contact", url: "#contact" }
        ]);

        return {
            links
        };
    },
};

</script>


<template>
    <div>
        <header>
            <div>
                <a :href="links.length > 0 ? links[0].url : '#home'">
                    <img src="/images/logo-light.svg" id="logo" alt="Tevin's logo icon">
                </a>
            </div>
            <nav>
                <div>
                    <ul>
                        <li v-for="(link, index) in links" :key="index" class="nav-items">
                            <a v-bind:title="`Links to ${link.url}`" v-bind:href="link.url" class="nav-link">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
            </nav>
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

    #logo {
        width: 30px;
    }

    ul {
        @include flex-box;
        gap: 60px;
    }


    nav {
        @include flex-box;
        flex-wrap: wrap;
        justify-content: space-between;
    }
}
</style>