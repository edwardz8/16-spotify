<template lang="html">
  <div class="SongItem">
  <div class="panel-block">
  <div class="media is-fullwidth">
  <div class="media-left">
    <img src="http://vignette2.wikia.nocookie.net/coheed/images/8/8e/The_Afterman_Descension_album_cover.jpg/revision/20130117201415" alt=""
    class="track__frame">{{track.frame}}</div>
    <div class="media-content">

    <div class="track__artist">{{track.artist}}</div>
    <div class="track__name">{{track.name}}</div>

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
  props: ['track'],
  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
