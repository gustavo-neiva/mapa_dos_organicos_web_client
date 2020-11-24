<style lang="scss" scoped>
</style>

<template>
    <l-marker :lat-lng="latlng">
      <l-popup>
        <div>
          Title
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque
            sed pretium nisl, ut sagittis sapien. Sed vel sollicitudin nisi.
            Donec finibus semper metus id malesuada.
          </p>
        </div>
      </l-popup>
    </l-marker>
</template>

<script>
export default {
  name: 'MapMarker',
  props: {
    latlng: {
      type: String,
      required: true
    },
  }
}
</script>
