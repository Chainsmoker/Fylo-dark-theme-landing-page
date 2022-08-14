<template>
  <div class="presentation__container" :style="directionFlex">
    <figure class="presentation__image">
        <img :src="image" alt="">
    </figure>
    <div class="presentation__texts" :style="containerStyle">
        <h1 :style="textStyle">{{ title }}</h1>
        <p>
            {{ desc }}
        </p>
        <div v-if="direction=='row'">
            <p>Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.</p>
            <a class="btn-1 anim" href="">See how Fylo works</a>
        </div>
        <div v-else>
            <a class="btn-2 anim" href="">Get Started</a>
        </div>
    </div>
  </div>
</template>

<script lang="ts">
import { computed } from 'vue'
export default {
    props: {
        direction: String,
        title: String,
        desc: String,
        image: String,
    },

    setup(props: any) {
        const directionFlex = computed(
            ()=>{
                return props.direction == 'column' ? 'flex-direction: column; width: 50%' : (
                    'flex-direction: row; width: 90%;'
                )
            }
        )
        
        const containerStyle = computed(
            ()=>{
                return props.direction == 'column' ? 'text-align: center;' : (
                    'text-align: start; '
                )
            }
        )

        const textStyle = computed(
            ()=>{
                return props.title.includes('Stay') ? 'text-align: center' : (
                    ''
                )
            }
        )

        return {
            directionFlex, containerStyle, textStyle
        }
    }
}
</script>

<style>
    @import url(https://fonts.google.com/specimen/Open+Sans);

    .presentation__container {
        display: flex;
        margin: 100px auto;
        transition: width .3s ease-in-out;
        font-family: 'Open Sans', sans-serif;
        color: #fff;
    }

    @media(max-width: 768px) {
        .presentation__container {
            width: 90% !important;
            flex-wrap: wrap;
        }
    }

    .presentation__image img {
        width: 100%;
    }
    
    .presentation__texts {
        margin: 40px 0;
    }

    .presentation__texts h1 {
        line-height: 40px;
    }

    @media(max-width: 400px) {
        .presentation__texts h1 {
            line-height: 30px;
            font-size: 1.5rem;
        }
    }

    .presentation__texts p {
        margin: 20px auto;
        width: 80%;
    }

    .btn-2 {
        display: inline-block;
        margin-top: 20px;
        text-decoration: none;
        color: #fff;
        font-weight: 700;
        background-image: linear-gradient(to right, var(--Cyan), var(--Blue));
        min-width: 200px;
        min-height: 40px;
        border-radius: 50px;
        line-height: 40px;
    }

    .btn-1 {
        display: inline-block;
        width: 100%;
        text-align: center;
        color: var(--Cyan);
        text-decoration: none;
        font-weight: 700;
    }
</style>