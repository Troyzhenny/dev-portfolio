<script setup>

</script>

<template>
    <section class="contact--container" id="contact">
        <div class="heading--cont">
            <h2>GET IN TOUCH</h2>
        </div>
        <div class="content">
            <div class="social--container">
                <div class="socialLinks">
                    <h3>CONTACT INFO</h3>
                    <span>
                        <i class="fa-solid fa-envelope"></i>
                        <p>tevincampbell@yahoo.com</p>
                    </span>
                    <br>
                    <h3>MY DIGITAL SPACES</h3>
                    <span>
                        <i class="fa-brands fa-linkedin-in"></i>
                        <p>linkedin</p>
                    </span>
                    <span>
                        <i class="fa-brands fa-github"></i>
                        <p>Github</p>
                    </span>
                </div>
            </div>
            <div class="form--container">
                <form action="#" method="post">
                    <label for="name">name</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">email</label>
                    <input type="email" name="email" id="email" required>

                    <label for="message">message</label>
                    <textarea name="message" id="message" cols="50" rows="4"></textarea>

                    <input type="button" id="submit-btn" value="Submit">
                </form>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@import "../assets/scss/variables";


.contact--container {
    display: flex;
    flex-direction: column;
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

    .content {
        display: flex;
        flex-wrap: wrap;
        place-items: center;
        justify-content: space-around;
        width: 100%;
        min-height: 100%; //100vh - 60px = 740px

        .social--container {
            display: flex;
            place-items: center;
            justify-content: space-around;
            width: 50%;
            min-height: 100%;

            .socialLinks {
                display: flex;
                flex-direction: column;
                gap: 30px;

                span {
                    font-size: 1.3em;
                    color: $lightGray;
                    display: flex;
                    place-items: center;
                    gap: 1rem;
                }

                h3 {
                    color: $accentColor;
                    font-size: 1.8em;
                }
            }
        }

        .form--container {
            display: flex;
            place-items: center;
            justify-content: space-around;
            width: 50%;
            min-height: 100%;

            form {
                display: flex;
                flex-direction: column;

                label {
                    font-size: 1.3em;
                    margin: 10px 0;
                    position: relative;
                    color: $secondary;
                }

                input {
                    font-size: 1em;
                    padding: 10px;
                    width: 600px;
                    border-radius: 3px;
                    outline: transparent;
                    background-color: transparent;
                    border-top: none;
                    border-left: none;
                    border-right: none;
                    border-bottom: 2px solid $secondary;
                }

                textarea {
                    font-size: 1em;
                    padding: 10px;
                    border-radius: 3px;
                    outline: transparent;
                    background-color: transparent;
                    border-top: none;
                    border-left: none;
                    border-right: none;
                    border-bottom: 2px solid $secondary;                }

                #submit-btn {
                    width: 200px;
                    margin-top: 40px;
                    cursor: pointer;
                    font-weight: 600;
                    color: $light;
                    border: 2px solid $secondary;
                    background-color: $secondary;

                    &:hover {
                        color: $secondary;
                        background-color: transparent;
                        border: 2px solid $mainColor;
                        transition: .5s ease-in-out;
                    }
                }
            }
        }
    }
}
</style>