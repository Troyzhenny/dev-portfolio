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
                    <span>
                        <i class="fa-brands fa-linkedin-in"></i>
                        <p>linkedin.com/in/tevin-campbell</p>
                    </span>
                    <span>
                        <i class="fa-brands fa-github"></i>
                        <p>github.com/Troyzhenny</p>
                    </span>
                    <span>
                        <i class="fa-solid fa-envelope"></i>
                        <p>tevincampbell@yahoo.com</p>
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
    flex-wrap: wrap;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    min-height: 100vh;

    color: $darkGray;
    background-color: $light;

    .heading--cont {
        // border: 3px solid blue;
        width: 100%;
        height: 10%;
        
        h2 {
            margin: 60px;
            font-size: 5em;
        }
    }

    .content {
        display: flex;
        flex-wrap: wrap;
        place-items: center;
        justify-content: center;
        width: 100%;
        min-height: 100%;
        // border: 4px solid #ff0080;
        .social--container {
            // border: 3px solid #00ff37;
            display: flex;
            place-items: center;
            justify-content: center;
            width: 50%;
            min-height: 100%;
            padding: 50px;
            .socialLinks {
                display: flex;
                flex-direction: column;
                gap: 30px;
                
                span {
                    font-size: 1.3em;
                    color: $secondary;
                    display: flex;
                    place-items: center;
                    gap: 1rem;
                }
            }
        }

        .form--container {
            // border: 3px solid #0099ff;
            display: flex;
            place-items: center;
            justify-content: center;
            width: 50%;
            min-height: 100%;
            padding: 50px;

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
                    width: 500px;
                    border-radius: 3px;
                    outline: transparent;
                    border: 2px solid $secondary;
                    background-color: transparent;
                    border-bottom: 2px solid $secondary;
                }

                textarea {
                    font-size: 1em;
                    padding: 10px;
                    border-radius: 3px;
                    outline: transparent;
                    border: 2px solid $secondary;
                    background-color: transparent;
                    border-bottom: 2px solid $secondary;
                }

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