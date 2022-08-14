<template>
    <div class="footer__suscribe">
        <h1>Get early access today</h1>
        <p> It only takes a minute to sign up and our free starter tier is extremely generous. If you have any 
        questions, our support team would be happy to help you.</p>
        <form>
            <input type="email" placeholder="Enter your email" v-model="email" :style="checkEmail">
            <button class="anim" type="submit">Get Started For Free</button>
        </form>
    </div>
    <div class="footer__container">
        <div class="footer__item">
            <div class="about__info">
                <figure class="about__logo">
                    <img src="../../public/images/logo.svg" alt="">
                </figure>
            </div>
        </div>
        <div class="footer__item">
            <div class="about">
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et olore magna aliqua</p>
            </div>
            <div class="footer__links--container">
                <a href="">+1-543-123-4567</a>
                <a href="">example@fylo.com</a>
            </div>
            <div class="footer__links--container">
                <a href="">About Us</a>
                <a href="">Jobs</a>
                <a href="">Press</a>
                <a href="">Blog</a>
            </div>
            <div class="footer__links--container">
                <a href="">Contact Us</a>
                <a href="">Terms</a>
                <a href="">Privacy</a>
            </div>
            <div class="footer__links--container">

            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { ref, computed } from 'vue';
export default {
    setup(){
        const email = ref('');
        const checkEmail = computed(() => {
            return email.value.length > 0 && email.value.includes('@') ? 'border: 2px solid green' : 'border: 2px solid red';
        });
        return {
            email,
            checkEmail
        }
    }
}
</script>

<style scoped>
    a {
        color: #fff;
        text-decoration: none;
    }

    .footer__suscribe {
        background-color: var(--Dark-Blue);
        max-width: 600px;
        min-height: 250px;
        margin: 0 auto;
        transform: translateY(-150px);
        border-radius: 10px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        text-align: center;
        color: #fff;
        font-family: 'RaleWay', sans-serif;
        padding: 20px;
    }

    @media(max-width: 630px) {
        .footer__suscribe {
            max-width: 90%;
        }
    }
    .footer__suscribe p {
        margin: 20px 30px;
    }

    form {
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
    }

    .footer__suscribe input {
        flex-grow: 1;
        height: 40px;
        border-radius: 50px;
        outline: none;
        border: none;
        padding-left: 20px;
    }

    .footer__suscribe button  {
        background-image: linear-gradient(to right, var(--Cyan), var(--Blue));
        border: none;
        min-width: 150px;
        height: 40px;
        border-radius: 50px;
        font-weight: 700;
        flex-grow: 1;
        color: #fff;
    }

    .footer__container {
        margin-top: -100px;
        display: flex;
        padding: 0 50px;
        color: #fff;
        flex-direction: column;
    }

    .footer__item:first-child {
        width: 50%;
    }

    .footer__item:last-child {
        display: flex;
        justify-content: space-between;
        margin-top: 20px;
        flex-wrap: wrap;
    }

    .about__logo {
        width: 200px;
    }

    .about {
        width: 30%;
    }

    .footer__links--container {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    a:hover {
        color: var(--Cyan);
    }

    @media (max-width: 680px){
        .footer__item:nth-child(1) {
            width: 100%;
            display: flex;
            justify-content: center;
        }

        .footer__item:nth-child(2) {
            display: flex;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        .about {
            width: 100%;
            text-align: center;
        }

        .footer__links--container {
            width: 200px;
            text-align: center;
            margin: 20px auto;
            flex-grow: 1;
        }
    }
</style>