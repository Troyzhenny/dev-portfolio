<script setup>

</script>

<template>
    <div class="footer--container">
        <dir class="links--container">
            <div>
                <!-- Social Links -->
            </div>
            <div>
                <!-- Contact info: Email ONLY -->
            </div>
            <div>
                <!-- Back to top -->
            </div>
        </dir>
        <div class="copyright--container">
            <p>©2024 Tevin Campbell</p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.footer--container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    color: $light;
    background-color: $dark;

    .copyright--container {
        display: flex;
        place-items: center;
        justify-content: center;
        width: 100%;
    }
}
</style>