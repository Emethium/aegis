<template>
  <div class="section has-background-light">
    <div class="columns">
      <!-- Page sidebar -->
      <div class="collumn has-background-light is-one-quarter">
        <aside class="menu">
          <p class="menu-label">
            General
          </p>
          <ul class="menu-list">
            <li><a>Home</a></li>
            <li><a>Favorites</a></li>
            <li><a>About</a></li>
          </ul>
          <p class="menu-label">
            Categories
          </p>
          <ul class="menu-list">
            <li><a>Action</a></li>
            <li><a>Adventure</a></li>
            <li><a>Platform</a></li>
            <li><a>Role-playing</a></li>
            <li><a>Racing</a></li>
            <li><a>Simulation</a></li>
            <li><a>Survivor Horror</a></li>
            <li><a>Strategy</a></li>
            <li><a>Sports</a></li>
          </ul>
        </aside>
      </div>
      <!-- Main content -->
      <div class="collumn has-background-light">
        <div class="content is-centered">
          <table class="table is-striped is-bordered is-hoverable is-narrow">
            <thead>
              <th class="has-text-primary has-text-centered">Number</th>
              <th class="has-text-primary has-text-centered">Title</th>
              <th class="has-text-primary has-text-centered">Game</th>
              <th class="has-text-primary has-text-centered">Composer</th>
              <th class="has-text-primary has-text-centered">Genre</th>
              <th class="has-text-primary has-text-centered">Platform</th>
              <th class="has-text-primary has-text-centered">Play</th>
            </thead>
            <tbody>
              <tr v-for="s in songList.songs" :key="s.id">
                <td class="has-text-weight-normal">{{s.id}}</td>
                <td class="has-text-weight-normal">{{s.title}}</td>
                <td class="has-text-weight-normal">{{s.game}}</td>
                <td class="has-text-weight-normal">{{s.composer}}</td>
                <td class="has-text-weight-normal">{{s.genre}}</td>
                <td class="has-text-weight-normal">{{s.platform}}</td>
                <td>
                  <div style="padding-top: 1em;">
                    <audio v-bind:src="''+s.url+''" ref="foo" controls="true"></audio>
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.audio  {
  position: absolute;
  padding: 1.6em;
}
</style>

<script>
import AudioVisual from 'vue-audio-visual'
import songs from '../assets/data.json'

export default {
  name: "HelloWorld",
  components: {
    AudioVisual
  },
  created() {
    console.log(this.songList)
  },
  data() {
    return {
      songList: songs
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
</style>
