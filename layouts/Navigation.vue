<template>
  <div class="navigation">

    <div class="mobile-menu-bar">
      <div>
        <button
          class="mobile-menu-btn"
          title="Open Menu"
          @click="showMobileNav"
        >
          <MenuIcon class="mobile-menu-icon" title="Open Menu" />
        </button>
      </div>
    </div>

    <div id="navbar-wrapper">
      <nav class="navbar container">
        <div class="site-name-wrapper">
          <nuxt-link class="site-name" to="/">Samuel Earl</nuxt-link>
        </div>
        <div class="navlink-wrapper">
          <nuxt-link class="navlink" to="/recent-projects">Recent Projects</nuxt-link>
          <nuxt-link class="navlink" to="/code-samples">Code Samples</nuxt-link>
          <nuxt-link class="navlink" to="/contact-me">Contact Me</nuxt-link>
          <!-- <nuxt-link class="navlink" to="/tutorials">Tutorials</nuxt-link> -->
        </div>
      </nav>
    </div>

  </div>
</template>

<script>
import MenuIcon from "vue-material-design-icons/Menu.vue";

export default {
  name: "Navigation",

  components: {
    MenuIcon,
  },

  methods: {
    showMobileNav() {
      const nav = document.getElementById("navbar-wrapper");
      if (nav.style.display === "block") {
        nav.style.display = "none";
      }
      else {
        nav.style.display = "block";
      }
    }
  }
};
</script>

<style lang="stylus" scoped>
@media $xs-up {
  .navigation {

    .mobile-menu-bar {
      position: sticky;
      top: 0;
      display: flex;
      align-items: center;
      width: 100%;
      height: 50px;
      padding: 10px;
      background-color: $primary;

      .mobile-menu-btn {
        font-size: 2rem;

        .mobile-menu-icon {
          color: white;
        }
      }
    }

    #navbar-wrapper {
      display: none;
      position: fixed;
      top: 50px;
      width: 100%;
      padding-bottom: 15px;
      background-color: $primary;

      .navbar {
        display: flex;
        flex-direction: column;
        align-items: center;

        .site-name-wrapper {
          padding-bottom: 5px;

          .site-name {
            border-bottom: none;
            font-size: 1.6rem;
            color: lighten($primary, 65%);
            &:hover {
              color: white;
            }
            &.nuxt-link-exact-active {
              color: white;
            }
          }
        }

        .navlink-wrapper {
          display: flex;
          flex-direction: column;
          align-items: center;

          .navlink {
            border-bottom: none;
            padding: 7px 0;
            font-size: 1.25rem;
            color: lighten($primary, 65%);
            &:hover {
              color: white;
            }
            &.nuxt-link-exact-active {
              color: white;
            }
          }
        }
      }
    }
  }
}

@media $xl-up {
  .navigation {

    .mobile-menu-bar {
      display: none;
    }

    #navbar-wrapper {
      display: block;
      position: fixed;
      top: 0;
      // width: 100%;
      padding-bottom: 0;
      // background-color: $primary;

      .navbar {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        height: 60px;

        .site-name-wrapper {
          padding: 0;

          .site-name {
            font-size: 1.6rem;
            // color: lighten($primary, 75%);
          }
        }

        .navlink-wrapper {
          // display: flex;
          flex-direction: row;
          align-items: center;

          .navlink {
            margin-left: 25px;
            // padding: 7px 0;
            // font-size: 1.25rem;
            // color: white;
          }
        }
      }
    }
  }
}
</style>
