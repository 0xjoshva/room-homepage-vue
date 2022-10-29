<template>
  <section>
    <nav>
      <img
        src="../assets/icon-close.svg"
        alt=""
        class="close"
        :class="{ show: !links }"
        @click="links = !links"
      />
      <img
        src="../assets/icon-hamburger.svg"
        alt=""
        class="menu"
        @click="links = !links"
        :class="{ show: links }"
      />
      <img src="../assets/logo.svg" alt="" id="logo" :class="{ show: links }" />
      <div class="router-links" :class="{ show: links }">
        <router-link to="/" class="router-link">home</router-link>
        <router-link to="/" class="router-link">shop</router-link>
        <router-link to="/" class="router-link">about</router-link>
        <router-link to="/" class="router-link">contact</router-link>
      </div>
    </nav>
    <div class="container">
      <img src="../assets/desktop-image-hero-1.jpg" alt="" id="carousel-img" />
      <div class="wrapper">
        <div class="text">
          <h2>Discover innovative ways to decorate</h2>
          <p>
            We provide unmateched quality, comfort, and style for property
            owners across the country. Our expert combine form and function in
            bringing your vision to life. Create a room in your own style with
            our collection and make your property a reflection of you and what
            you love.
          </p>
          <button>
            SHOP NOW
            <img src="../assets/icon-arrow.svg" alt="" class="shop-arrow" />
          </button>
        </div>
        <div class="carousel-buttons">
          <div class="arrows">
            <img src="../assets/icon-angle-left.svg" alt="" />
          </div>
          <div class="arrows">
            <img src="../assets/icon-angle-right.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="bottom">
      <img src="../assets/image-about-dark.jpg" alt="" />
      <div class="about">
        <h6>ABOUT OUR FURNITURE</h6>
        <p>
          Our multifunctional collection blends design and function to suit your
          individual taste. Make each room unique, or pick a cohesive theme at
          best express your interests and what inspires you. Find the furniture
          pieces you need, from traditional to contemporary styles or anything
          in between. Product specialists are available to help you create your
          dream space.
        </p>
      </div>
      <img src="../assets/image-about-light.jpg" alt="" />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      links: false,
    };
  },
};
</script>
<style scoped>
section {
  width: 100%;
  min-height: 100vh;
  height: fit-content;
  background: var(--white);
  font-family: "League Spartan", sans-serif;
}
nav {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 3;
  display: flex;
  column-gap: 5rem;
  justify-content: center;
  align-items: center;
  height: 50px;
  padding-top: 6rem;
  padding-left: 6rem;
}
nav img {
  min-height: 20px;
  width: auto;
}
.router-links {
  display: flex;
  flex-direction: row;
  column-gap: 2rem;
}
.router-link {
  font-size: 18px;
  text-decoration: none;
  color: var(--white);
  border-bottom: 2px solid transparent;
  transition: all ease-in-out 0.2s;
}
.container {
  display: flex;
  width: 100%;
  height: 53rem;
  min-height: 53rem;
}
#carousel-img {
  min-width: 1200px;
  width: 1200px;
  min-height: 10rem;
  object-fit: fill;
}
.text {
  padding-top: 10rem;
  width: fit-content;
  height: 100%;
  padding-bottom: 0;
}
.text h2 {
  font-size: 5rem;
  line-height: 5rem;
  font-weight: 600;
  padding-bottom: 2rem;
  margin: 0 auto;
  width: 70%;
}
.text p {
  font-size: 18px;
  color: var(--darkgrey);
  margin: 0 auto;
  width: 70%;
  text-align: justify;
}
.wrapper {
  display: flex;
  flex-direction: column;
}
.carousel-buttons {
  background: var(--white);
  width: 100%;
  max-height: 10rem;
  height: 10rem;
  display: flex;
}
.arrows {
  background: var(--black);
  width: fit-content;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 3.5rem;
  padding-right: 3.5rem;
  transition: 0.2s all cubic-bezier(0.46, 0.03, 0.52, 0.96);
}
.arrows:hover {
  background: var(--verydarkgrey);
}
.wrapper button {
  width: 70%;
  height: fit-content;
  background: var(--white);
  border: none;
  font-size: 1.6rem;
  letter-spacing: 9px;
  display: flex;
  align-items: center;
  margin: 0 auto;
  font-weight: 600;
  padding: 0;
  margin-top: 2rem;
  column-gap: 0px;
  transition: 0.2s all cubic-bezier(0.68, -0.55, 0.27, 1.55);
}
.wrapper button:hover {
  column-gap: 10px;
  letter-spacing: 10px;
  opacity: 0.3;
}
.shop-arrow {
  width: 2rem;
  height: auto;
  width: fit-content;
  height: fit-content;
  margin-left: 2rem;
}
.bottom {
  display: flex;
  align-items: center;
  justify-content: center;
}
.bottom img {
  height: 27.75rem;
  width: 43.6rem;
  object-fit: cover;
}
.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 5rem;
}
.about h6 {
  font-size: 2rem;
  letter-spacing: 8px;
  width: 75%;
  padding-bottom: 1rem;
}
.about p {
  font-size: 18px;
  color: var(--darkgrey);
  width: 75%;
}
.router-link:hover {
  border-bottom: 2px solid var(--white);
  translate: 0px -2px;
}
.menu {
  display: none;
}

.show {
  display: none;
}
@media only screen and (max-width: 600px) {
  /*Big smartphones [426px -> 600px]*/
  .container {
    display: flex;
    flex-direction: column;
  }
  #carousel-img {
    min-width: 100%;
    min-height: 30rem;
    object-fit: fill;
  }
  .router-links {
    display: none;
  }
  .bottom {
    display: flex;
    flex-direction: column;
  }
  .menu {
    display: block;
  }
  .show {
    display: none;
  }
  nav{
    padding-top: 4rem;
  }
}
@media only screen and (max-width: 425px) {
  /*Small smartphones [325px -> 425px]*/
}
</style>
