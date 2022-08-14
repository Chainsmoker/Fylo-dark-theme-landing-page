<template>
  <div class="testimonials__card">
    <div class="testimonials__content">
        {{ content }}
    </div>
    <div class="testimonials__user">
        <figure class="testimonials__user--pic">
            <img :src="userPic" alt="">
        </figure>
        <div class="testimonials__user--info">
            <h2>{{ userName }}</h2>
            <p>{{ userPosition }}</p>
        </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
    props: {
        content: String,
        userName: String,
        userPosition: String,
        userPic: String
    },
}
</script>

<style>
    .testimonials__card {
        width: 400px;
        min-height: 200px;
        background-color: var(--Dark-Blue-3);
        padding: 20px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        color: #fff;
        border-radius: 10px;
        font-family: 'Raleway', sans-serif;
        transition: width 0.5s ease-in-out;
    }

    @media(max-width: 900px) {
        .testimonials__card {
           width: 100%;
        }
    }

    .testimonials__user {
        display: flex;
        gap: 20px;
        margin-top: 30px;
    }

    .testimonials__user--pic img{
        width: 50px;
        height: 50px;
        object-fit: cover;
        border-radius: 50%;
    }

    .testimonials__user--info h2 {
        font-size: 1rem;
        margin-top: 10px;
    }

    .testimonials__user--info p {
        font-size: 0.8rem;
    }
</style>