<template>
  <div>
    <nav>
      <div class="logo">
        <h4>Name</h4>
      </div>
      <ul class="nav-links">
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/about">About</nuxt-link>
        <nuxt-link to="/gallery">Gallery</nuxt-link>
        <nuxt-link to="/contact">Contact</nuxt-link>
      </ul>

      <div class="burger">
        <div class="line1"></div>
        <div class="line2"></div>
        <div class="line3"></div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    mounted() {
      const navSlide = () => {
        const burger = document.querySelector('.burger');
        const nav = document.querySelector('.nav-links');
        const navLinks = document.querySelectorAll('.nav-links li');

        // toggle nav
        burger.addEventListener('click', () => {
          nav.classList.toggle('nav-active');

          // animate links
          navLinks.forEach((link, index) => {
            if (link.style.animation) {
              link.style.animation = ''
            } else {
              link.style.animation = `navLinkFade 0.5s ease forwards ${index /7 + 0/3}s`;
            }
          });
          // Burger Animation
          burger.classList.toggle('toggle');
        });
      }
      navSlide();
    }
  }

</script>


<style lang="scss">
  * {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }

  nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    min-height: 8vh;
    font-family: 'Montserrat', sans-serif;
    background-color: rgb(61, 0, 160);
    color: white;
  }

  .logo {
    text-transform: uppercase;
    letter-spacing: 5px;
    font-size: 20px;
  }

  .nav-links {
    display: flex;
    width: 20px;
    justify-content: space-around;
  }

  .nav-links li {
    list-style: none;
  }

  .nav-links a {
    color: white;
    text-decoration: none;
    letter-spacing: 3px;
    font-weight: bold;
    font-size: 14px;
    padding: 5px;
  }

  .burger {
    display: none;
  }

  .burger div {
    width: 25px;
    height: 3px;
    background-color: white;
    margin: 5px;
    transition: all 0.3s ease;
  }

  @media screen and (max-width:768px) {
    body {
      overflow-x: hidden;
    }

    .nav-links {
      position: absolute;
      right: 0px;
      height: 92vh;
      top: 8vh;
      background-color: rgb(61, 0, 160);
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 20%;
      transform: translateX(100%);
      transition: transform 0.5s ease-in;
      z-index: 9;
    }

    .nav-links li {
      opacity: 0;
    }

    .burger {
      display: block;
      cursor: pointer;
    }
  }

  .nav-active {
    transform: translateX(0%);
  }

  @keyframes navLinkFade {
    from {
      opacity: 0;
      transform: translateX(50px);
    }

    to {
      opacity: 1;
      transform: translateX(0px);
    }
  }

  .toggle .line1 {
    transform: rotate(-45deg) translate(-5px, 6px);
  }

  .toggle .line2 {
    opacity: 0;
  }

  .toggle .line3 {
    transform: rotate(45deg) translate(-5px, -6px);
  }

</style>
