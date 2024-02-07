<script setup>

</script>

<template>
    <div class="contact--container" id="contact">
        <div class="heading--cont">
            <h2>LETS CONNECT!</h2>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.contact--container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    min-height: 100vh;

    color: $darkGray;
    background-color: $light;

    .heading--cont {
        h2 {
            font-size: 5em;
            margin: 60px;
        }
    }
}
</style>