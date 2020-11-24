<style scoped lang="scss">
  .navbar-brand{
    margin-left: 10vh;
  }
  .burger {
    height: auto;
  }
  .navbar-menu {
    @media (max-width: $tablet) {
      display: block;
      position: absolute;
      left: 0;
      right: 0;
      opacity: 0;

      transform: translateX(-100%);
      transition: all .4s;
      pointer-events: none;
      transition-timing-function: ease;
      z-index: 1000;
    }
  }
  .navbar-menu.is-active {
      opacity: 1;
      transform: none;
      pointer-events: auto;
      height: 100vh;
  }
  a {
    display: block;
    width: 100%;
  }
</style>

<template>
  <div>
    <nav class="navbar header has-shadow is-white" role="navigation" aria-label="main navigation">
      <div class="container">
        <div class="navbar-brand">
          <a href="/" >
            <img src="~assets/logo.png" alt="mapa-dos-organicos" width="180" class="has-ratio">
          </a>
          <a role="button" class="navbar-burger burger is-large" aria-label="menu" aria-expanded="false" @click="isOpen = !isOpen" :class="{'is-active': isOpen}">
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>
        <div class="navbar-menu"  v-bind:class="{'is-active': isOpen}">
          <div class="navbar-end">
            <div class="navbar-item is-size-4 is-size-3-mobile" v-for="(item, key) of items" :key="key">
              <nuxt-link
                :to="item.to"
                exact-active-class="is-active"
                @click.native="isOpen = false"
              >
                {{ item.title }}
              </nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      isOpen: false,
      items: [
        {
          title: 'Home',
          to: { name: 'index' }
        }
      ]
    }
  },
}
</script>
