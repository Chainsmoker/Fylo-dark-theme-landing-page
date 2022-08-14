<template>
  <div class="features__item">
    <figure class="features__image">
        <img :src="image" alt="">
    </figure>
    <div class="features__texts">
        <h1>{{ title }}</h1>
        <p>
            {{ desc }}
        </p>
    </div>
  </div>
</template>

<script lang="ts">
export default {
    props: {
        title: String,
        desc: String,
        image: String
    },
}
</script>

<style>
    .features__item {
        height: 200px;
        width: 300px;
        display: flex;
        flex-direction: column;
        align-items: center;
        color: #fff;
    }

    .features__image {
        width: 30%;
        height: 50%;
    }

    .features__texts {
        margin-top: 20px;
        text-align: center;
    }

    .features__texts h1 {
        font-size: 1.5rem;
    }

    .features__texts p {
        font-size: 0.9rem;
        margin-top: 10px;
    }
</style>