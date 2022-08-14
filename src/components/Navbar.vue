<template>
  <nav class="navbar">
    <figure class="navbar__logo">
        <img src="../../public/images/logo.svg" alt="">
    </figure>
    <div class="navbar__links">
        <a href="">Features</a>
        <a href="">Team</a>
        <a href="">Sign in</a>
    </div>
  </nav>
</template>

<script lang="ts">
export default {

}
</script>

<style scoped>
    @import url(https://fonts.google.com/specimen/Raleway);
    
    .navbar {
        height: 150px;
        display: flex;
        padding: 0 20px;
        align-items: center;
        justify-content: space-between;
        font-family: 'Raleway', sans-serif;
    }

    @media (max-width: 520px){
        .navbar {
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .navbar__links {
            width: 100%;
            display: flex;
            gap: 10%;
            justify-content: center !important;
            margin-top: 50px;
        }
    }
    .navbar__logo {
        width: 150px;
    }

    img {
        width: 100%;
        height: 100%;
    }

    .navbar__links {
        width: 70%;
        display: flex;
        gap: 10%;
        justify-content: flex-end;
    }

    .navbar__links a {
        color: #fff;
        text-decoration: none;
        font-size: 1rem;
    }

    a:hover {
        color: var(--Cyan);
    }
</style>