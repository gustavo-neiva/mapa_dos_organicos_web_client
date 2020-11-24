<style lang="scss" scoped>
</style>

<template>
  <div id="map-wrap" style="height: 80vh">
    <client-only>
      <l-map :zoom=4 :center="[-13,-46]">
        <l-tile-layer url="http://{s}.tile.openstreetmap.org//{z}/{x}/{y}.png"></l-tile-layer>
      </l-map>
    </client-only>
  </div>
</template>

<script>
import MapMarker from '~/components/MapMarker';

export default {
  name: 'BaseMap',
  components: {
    MapMarker
  },
  props: {
    points: {
      type: Array,
      required: true
    },
  }
}
</script>
