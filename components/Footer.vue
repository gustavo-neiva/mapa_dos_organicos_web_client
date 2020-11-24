<template>
  <div>
    <footer class="footer">
      <div class="columns">
        <div class="column is-4 is-offset-2">
          <a href="/" >
            <img src="~assets/logo.png" alt="mapa-dos-organicos" width="112">
          </a>
        </div>
        <div class="column is-6 is-offset-2 mt-6">
          <div class="container">
            <div class="social-links">
              <a href="https://instagram.com/torus">
                <fa :icon="['fab', 'instagram']"  style="font-size: 40px"/>
              </a>
            </div>
          </div>
          <div class="container">
            <p style="color:black;">
              Copyright © 2020 Luiz Gustavo Neiva
            </p>
          </div>
        </div>
      </div>

    </footer>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>
