<template lang="html">
  <div class="app">
    <div class="page">
      <div class="panel">
        <input type="text" class="panel-heading" placeholder="search">
        </div>
          <div class="results">

          <div class="panel-block">
            <div class="media is-fullwidth">
            <div class="media-left">
              <img src="http://vignette2.wikia.nocookie.net/coheed/images/8/8e/The_Afterman_Descension_album_cover.jpg/revision/20130117201415" alt=""
              class="track__frame">{{track.frame}}</div>
              <div class="media-content">

              <div class="track__artist">{{track.artist}}</div>
              <div class="track__name">{{track.name}}</div>
              <SongItem v-for="item in list" v-bind:repo="item"></SongItem>

            </div>
            <div class="media-right">
            <span class="fa fa-spotify" aria-hidden="true"></span>
            </div>
          </div>
            </div>


        </div>
        </div>





    </div>
</template>

<script>
import SongItem from './song-item.vue';

export default {
  component: {
    SongItem,
  },

  created() {
    fetch('https://api.spotify.com/v1/search?query=katy&type=track&offset=0&limit=20')
    .then(t => t.json())
    .then((track) => {
      this.list = track;
    });
  },

  data() {
    return {
      track: {

      },

    list: [
      {frame: '' },
      {artist: '' },
      {name: '' }
    ],
    };
  },

  methods: {

  },
};
</script>
