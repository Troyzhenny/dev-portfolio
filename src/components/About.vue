<script>

</script>

<template>
    <div class="about--container" id="about">
        <div class="heading--cont">
            <h2>ABOUT.</h2>
        </div>
        <div class="image--block">
            <img src="/images/Tevin3.png" alt="">
        </div>
        <div class="bio--cont">
            <p>
                I am an enthusiastic web developer and graphic designer located in North Carolina.
                With a passion for my craft, I excel in crafting sleek, minimalist, and responsive
                web solutions that not only meet but exceed client expectations.
                <br><br>
                When I'm not coding or designing, I enjoy spending time with my daughter, hanging out with friends, and the
                beach.
            </p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.about--container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    place-items: center;
    width: 100%;
    min-height: 100vh;
    background-color: $light;


    .heading--cont {
        width: 100%;

        h2 {
            margin: 60px;
            color: $darkGray;
        }
    }

    .image--block {
        @include flex-box;
        box-shadow: 10px 10px 20px -10px $projectCardShadow;

        img {
            width: 380px;
            border-radius: 5px;
        }
    }


    .bio--cont {
        margin: 60px 0;
        padding: 5rem;
        width: 50%;

        p {
            font-size: 2em;
            color: $lightGray;
        }
    }
}

// Queries //
/* Styles for smaller screens */
@media screen and (max-width: 768px) {
    .about--container {
        h2 {
            font-size: 2.8em;
        }

        p {
            font-size: 1.25em;
        }

        .image--block {
            @include flex-box;

            img {
                width: 290px;
                border-radius: 5px;
            }
        }


        .bio--cont {
            margin: 0 0 60px;
            padding: 2rem;
            width: 100%;

            p {
                font-size: 1.25em;
                color: $lightGray;
            }
        }
    }
}
</style>