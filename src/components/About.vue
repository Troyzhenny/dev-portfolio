<script setup>

</script>

<template>
    <div class="about--container" id="about">
        <div class="heading--cont">
            <h2>WHO AM I?</h2>
        </div>
        <div class="bio--cont">
            <p>
                I am an enthusiastic web developer and graphic designer located in North Carolina.
                With a passion for my craft, I excel in crafting sleek, minimalist, and responsive
                web solutions that not only meet but exceed client expectations.

                I am eager to embark on a journey where I can not only
                showcase my skills but also continually enhance them.
                I am committed to evolving into an even more proficient and versatile version
                of myself.
                <br><br>
                When I'm not coding or designing, I enjoy spending time with my daughter, hanging out with friends, and the beach.
            </p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.about--container {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    min-height: 100vh;
    background-color: $light;

    .heading--cont {
        h2 {
            font-size: 5em;
            margin: 60px;
            color: $darkGray;
        }
    }


    .bio--cont {
        padding: 40px;
        width: 100%;

        p {
            color: $lightGray;
            font-size: 3em;
        }
    }
}
</style>