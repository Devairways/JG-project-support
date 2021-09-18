<template>
  <header>
    <div class="bg_header"></div>
    <div class="header_container">
      <div id="logo" @click="menuOpen = false">
        <img src="img/logo.jpg" alt="" class="img-raised" />
      </div>
      <div id="hamburger_menu" @click="toggleMenuBar">
        <span class="bar" :class="{ cross_bar: menuOpen }"></span>
        <span class="bar" :class="{ cross_bar: menuOpen }"></span>
        <span class="bar" :class="{ cross_bar: menuOpen }"></span>
      </div>
      <nav :style="menuOpen ? { right: '300px' } : ''">
        <ul>
          <li>
            <nav-link el="#about"
              ><i class="fas fa-industry"></i>
              <p>Over ons</p>
            </nav-link>
          </li>
          <li>
            <nav-link el="#services"
              ><i class="fas fa-briefcase"></i>
              <p>Diensten</p>
            </nav-link>
          </li>
          <li>
            <nav-link el="#contact"
              ><i class="fas fa-envelope"></i>
              <p>Contact</p>
            </nav-link>
          </li>
        </ul>
      </nav>
      <div class="welkom">
        <h1>Welkom bij JG project-support</h1>
      </div>
    </div>
  </header>
</template>

<script>
import NavLink from "../components/nav-link/Nav-Link.vue";
export default {
  name: "Header",
  components: { NavLink },
  data() {
    return { menuOpen: false };
  },

  provide() {
    return {
      closeNavbar: this.toggleMenuBar,
    };
  },

  methods: {
    toggleMenuBar() {
      this.menuOpen = !this.menuOpen;
    },
  },

  watch: {
    loggin() {
      console.log("is menu open: ", this.menuOpen);
    },
  },
};
</script>

<style lang="scss" scoped>
header {
  position: relative;
  width: 100%;

  div {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px 20px;
    height: 90px;
  }
  .bg_header {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background: #f6f6fb;
    clip-path: polygon(0 0, 100% 0, 100% 87%, 0 100%);
    z-index: -1;
  }

  .header_container {
    position: relative;
    margin: auto;
    max-width: 1600px;
  }

  #logo {
    img {
      height: 70px;
    }
  }

  #hamburger_menu {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    height: 25px;
    cursor: pointer;

    .bar {
      background: #ff4d58;
      width: 2.5rem;
      height: 0.3rem;
      transition: all 0.3s linear;

      &:nth-child(2) {
        width: 1.2rem;
      }

      &:nth-child(3) {
        width: 2rem;
      }
    }

    .cross_bar {
      position: fixed;
      background: #fff;

      &:nth-child(1) {
        width: 2rem;
        z-index: 32;
        transform: rotateZ(-45deg) translateY(1.1rem);
        margin-top: -6px;
      }

      &:nth-child(2) {
        opacity: 0;
      }

      &:nth-child(3) {
        z-index: 32;
        transform: rotateZ(45deg) translateY(-1rem);
        margin-top: 18px;
      }
    }
  }

  .welkom {
    display: none;
  }

  nav {
    position: fixed;
    display: block;
    top: 0;
    height: 100% !important;
    width: 300px;
    right: 0;
    z-index: 30;
    background-color: #999;
    overflow-y: visible;
    text-align: left;
    transform: translate3d(300px, 0, 0);
    transition: all 0.3s cubic-bezier(0.685, 0.0473, 0.346, 1);

    &:before {
      background: linear-gradient(#ff4d58, #000 80%);
      opacity: 0.76;
      display: block;
      content: "";
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: -1;
    }
  }

  ul {
    margin-top: 10rem;
    position: relative;
    max-height: calc(100vh - 75px);
    min-height: 100%;
    overflow: auto;
    text-align: start;
  }

  li {
    padding: 0 10px;
    color: #fff !important;
    margin: 0.315rem 1rem;
    opacity: 1;

    p {
      color: #fff !important;
      margin: 0 10px;
      cursor: pointer;
    }
  }
  @media only screen and (min-width: 768px) {
    .bg_header {
      background-image: url("../../public/img/header.png");
      background-position: center;
      opacity: 0.6;
    }

    .welkom {
      display: flex;
      position: absolute;
      top: -20px;
      right: 70px;
      align-items: center;

      h1 {
        font-size: 42px;
        background: linear-gradient(35deg, #fff 40%, #ff4d58 0);
        color: transparent;
        background-clip: text;
      }
    }

    #logo {
      img {
        height: 120px;
      }
    }

    div {
      padding: 20px;
      align-items: flex-start;
      height: 600px;
    }
  }

  @media only screen and (min-width: 1025px) {
    #hamburger_menu {
      display: none;
    }

    nav {
      position: unset;
      background: unset;
      transform: translate3d(0, 0, 0);
      height: fit-content;
      width: unset;

      &::before {
        background: unset;
      }
      ul {
        display: flex;
        margin-top: 30px;
        width: max-content;

        li {
          margin: 0;
          padding: 0;
          height: fit-content;

          &:hover {
            background-color: transparentize($color: #fff, $amount: 0.5);
          }
        }

        i {
          color: #ff4d58 !important;
        }

        p {
          font-size: 18px;
          font-weight: 600;
          color: #ff4d58 !important;
          &:hover {
            cursor: pointer;
          }
        }
      }
    }
  }
}
</style>
