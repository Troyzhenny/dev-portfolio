<script>
// NAVIGATION
import { ref } from 'vue';

export default {
    setup() {
        const links = ref([
            { text: "Home", url: "index.html" },
            { text: "About", url: "#" },
            { text: "Resume", url: "#" },
            { text: "Contact", url: "#" }
        ]);

        return {
            links
        };
    }
};

</script>


<template>
    <div>
        <header>
            <div>
                <a v-bind:href="links.length > 0 ? links[0].url : '#'">
                    <img src="../assets/images/logo.png" id="logo" alt="Tevin's logo icon">
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
    padding: 20px 40px;
    background-color: $dark;
    @include flex-box;
    justify-content: space-between;

    #logo {
        width: 40px;
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