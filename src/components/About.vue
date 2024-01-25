<script setup>

</script>

<template>
    <div class="about--container">
        <div class="about--shelf">
            <h1>Who Am i?</h1>
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
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.about--container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 100%;
    min-height: 100%;
    background-color: $light;
    

    .about--shelf {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        width: 100%;
        min-height: 100vh;
        gap: 20px;

        img {
            border: 1px solid blueviolet;
        }
        .bio--cont {
            padding: 50px;
            border: 1px solid yellowgreen;
            
            p {
                text-align:start;
                color: $lightGray;
                font-size: 2em;
            }
        }
    }
}
</style>