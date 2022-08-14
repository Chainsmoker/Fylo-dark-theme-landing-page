<template>
  <div class="hero">
    <Navbar />
    <Presentation direction="column" image="/images/illustration-intro.png" title="All your files in one secure location, accessible anywhere." desc="Fylo stores all your most important files in one secure location. Access them wherever you need, share and collaborate with friends family, and co-workers."/>>
  </div>
  <div class="container">
    <div class="features__container">
      <FeaturesItem image="/images/icon-access-anywhere.svg" title="Access your files, anywhere" desc="The ability to use a smartphone, tablet, or computer to access your account means your files follow you everywhere." />
      <FeaturesItem image="/images/icon-security.svg" title="Security you can trust" desc="2-factor authentication and user-controlled encryption are just a couple of the security features we allow to help secure your files." />
      <FeaturesItem image="/images/icon-collaboration.svg" title="Real-time collaboration" desc="Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required." />
      <FeaturesItem image="/images/icon-any-file.svg" title="Store any type of file" desc="Whether you're sharing holidays photos or work documents, Fylo has you covered allowing for all file types to be securely stored and shared." />
    </div>
    <Presentation direction="row" image="/images/illustration-stay-productive.png" title="Stay productive, wherever you are" desc="Never let location be an issue when accessing your files. Fylo has you covered for all of your file storage needs." />
    <div class="testimonials__container">
      <TestimonialsCards userPic="/images/profile-1.jpg" userName="Satish Patel" userPosition="Founder & CEO, Huddle" content="Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine."/>
      <TestimonialsCards userPic="/images/profile-2.jpg" userName="Bruce McKenzie" userPosition="Founder & CEO, Huddle" content="Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine."/>
      <TestimonialsCards userPic="/images/profile-3.jpg" userName="Iva Boyd" userPosition="Founder & CEO, Huddle" content="Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine." />
    </div>
    <footer>
      <Footer />
      <p style="text-align:center;color:#fff; margin-top: 30px;">
        Challenge by <a style="color: var(--Cyan)" href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
        Coded by <a style="color: var(--Cyan)" target="_blank" href="https://github.com/Chainsmoker">Chainsmoker By Calvin</a>.
    </p>
    </footer>
  </div>
</template>

<script lang="ts">
import Navbar from './components/Navbar.vue';
import Presentation from './components/Presentation.vue';
import FeaturesItem from './components/FeaturesItem.vue';
import TestimonialsCards from './components/TestimonialsCards.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Presentation,
    FeaturesItem,
    TestimonialsCards,
    Footer,
},
}
</script>

<style>
 :root {
    --Dark-Blue: hsl(217, 28%, 15%);
    --Dark-Blue-1: hsl(218, 28%, 13%);
    --Dark-Blue-2: hsl(216, 53%, 9%);
    --Dark-Blue-3: hsl(219, 30%, 18%);
    --Cyan: hsl(176, 68%, 64%);
    --Blue: hsl(198, 60%, 50%);
    --Light-Red: hsl(0, 100%, 63%);
 }

  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  body {
    background-color: var(--Dark-Blue);
    max-width: 1400px;
    margin: 0 auto;
  }

  .hero {
    background-image: url(../public/images/bg-curvy-desktop.svg);
    background-position-y: bottom;
    background-repeat: no-repeat;
    padding: 0 50px;
  }

  @media(max-width: 630px) {
    .hero {
      background-image: url(../public/images/bg-curvy-mobile.svg);
      padding: 0;
    }
  }

  .container {
    background-color: var(--Dark-Blue-1);
  }

  .features__container {
    width: 90%;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 100px;
  }

  .testimonials__container {
    display: flex;
    gap: 50px;
    flex-wrap: wrap;
    width: 90%;
    justify-content: center;
    margin: 0 auto;
  }

  footer {
    background-color: var(--Dark-Blue-2);
    min-height: 400px;
    width: 100%;
    margin-top: 300px;
    font-family: 'Raleway', sans-serif;
  }
  
  .anim:hover {
        animation: btnAnim 1s ease-in-out;
  }

  @keyframes btnAnim {
    0% {
      background-position-x: 0;
    }

    100% {
      background-position-x: 230px;
    }
  }
</style>
