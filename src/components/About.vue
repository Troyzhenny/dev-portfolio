<script setup>

</script>

<template>
    <div class="about--container" id="about">
        <h2>WHO AM I?</h2>
        <div class="bio--cont">
            <p>
                I am an enthusiastic web developer and graphic designer located in North Carolina.
                With a passion for my craft, I excel in crafting sleek, minimalist, and responsive
                web solutions that not only meet but exceed client expectations.

                <!-- I am eager to embark on a journey where I can not only
                    showcase my skills but also continually enhance them.
                    I am committed to evolving into an even more proficient and versatile version
                    of myself.
                    <br><br>
                    When I'm not coding or designing, I enjoy hanging out with friends, the beach, and
                    creating videos about design and web development on my <a rel="noopener"
                        title="this is a link to Tevin's youTube Channel"
                        href="https://youtube.com/@Troyzhen?si=BLpLFJiKb3nxRy70" target="_blank">YouTube</a>
                    channel 🙂📸. -->
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

    h2 {
        font-size: 5em;
        font-weight: 600;
        color: $darkGray;
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