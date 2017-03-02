<template lang="html">
  <div class="app">
    <div class="page">
      <div class="panel">
        <input type="text" class="panel-heading" placeholder="search">
        </div>
          <div class="results">
            <song-item v-for="item in tracks" v-bind:tracks="item"></song-item>

          <!--<div class="panel-block">
            <div class="media is-fullwidth">
            <div class="media-left">
              <img src="http://vignette2.wikia.nocookie.net/coheed/images/8/8e/The_Afterman_Descension_album_cover.jpg/revision/20130117201415" alt=""
              class="track__frame">{{tracks.frame}}</div>
              <div class="media-content">

              <div class="track__artist">{{tracks.artist}}</div>
              <div class="track__name">{{tracks.name}}</div>
              <song-item v-for="item in tracks" v-bind:repo="item"></song-item>

            </div>
            <div class="media-right">
            <span class="fa fa-spotify" aria-hidden="true"></span>
            </div>
          </div>
        </div>-->


        </div>
        </div>





    </div>
</template>

<script>
import SongItem from './song-item.vue';

export default {
  components: {
    SongItem,
  },

  created() {
    fetch('https://api.spotify.com/v1/search?query=coheed&type=track&offset=0&limit=20')
    .then(r => r.json())
    .then((data) => {
      this.tracks = data.tracks.items;
    });
  },

  data() {
    return {
      tracks: []
    };
  },

  methods: {

  },
};
</script>
