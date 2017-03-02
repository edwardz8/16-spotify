<template lang="html">
  <div class="SongItem">
    <div class="panel-block">
      <div class="media is-fullwidth">
        <div class="media-left">
          <img v-bind:src="tracks.album.images[0].url" alt=""
          class="track__frame"></div>
          <div class="media-content">

          <div class="track__artist">{{tracks.artists[0].name}}</div>
          <div class="track__name">{{tracks.name}}</div>

        </div>
        <div class="media-right">
          <span class="fa fa-spotify" aria-hidden="true"></span>
        </div>
      </div>
    </div>
  </div>


</template>

<script>
export default {
  props: ['tracks'],
  data() {
    return {};
  },

  methods: {

  },
};
</script>
