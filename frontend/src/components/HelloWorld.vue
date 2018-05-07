<template>
  <div class="hello">
    <div class="columns">
      <!-- Page sidebar -->
      <div class="collumnhas-background-light">
        
      </div>
      <!-- Main content -->
      <div class="collumn has-background-light">
        <div class="media">
          <div class="tile">
            <article class="tile is-child notification is-light">
              <aplayer
              :music="{
                title: 'Zero Opening Stage',
                artist: 'Mega Man X Corrupted',
                src: 'http://66.90.93.122/ost/megaman-x-corrupted/lderepew/05%20-%20Zero%20Opening%20Stage.mp3',
                pic: 'https://i.ytimg.com/vi/GQ47immxaQ8/hqdefault.jpg'
              }"
              />
            </article>
          </div>
          <div class="tile">
            <article class="tile is-child notification is-light">
              <aplayer
                :music="{
                  title: 'Stickerbrush Symphony',
                  artist: 'Donkey Kong Country 2',
                  src: 'https://cs1.mp3.pm/download/85870084/M0NsaUt5cTh2bFk0N3lXTUZ3UHovVThsQTZicVpMVGp6UnI3U1FHL2o4azJFT2dSK2R3Q0R1ZmlNL3ZoQUswOUg3bUI1VlIyV3RsV1M3eGo5OEIwdE93SDM2VzVBNUFuWmFpQ09DT3hFZm5NbG5oTXAwejBxeEVLSkdjL2psM2Y/Donkey_Kong_Country_2_-_17._Stickerbrush_Symphony_(mp3.pm).mp3',
                  pic: 'https://cdn02.nintendo-europe.com/media/images/03_teaser_module_1_square/games_3/game_boy_advance_5/TM_GBA_DonkeyKongCountry2.png'
                }"
              />
            </article>
          </div>
          <div class="tile">
            <article class="tile is-child notification is-light">
              <aplayer
              :music="{
                title: 'Into the Wilderness',
                artist: 'Wild Arms',
                src: 'http://66.90.93.122/ost/wild-arms-original-game-soundtrack/kfbkgbxc/01%20into%20the%20wilderness.mp3',
                pic: 'http://images2.wikia.nocookie.net/__cb20080424154713/wildarms/images/3/3d/Wildarms.jpg'
              }"
              />
            </article>
          </div>
        </div>
      </div>
      <!-- Playlist example -->
      <div class="collumn has-background-light">
        <div class="tile">
          <article class="tile is-child notification is-light">
            <aplayer
              autoplay
              theme="pic"
              shuffle
              repeat="list"
              :controls="controls"
              :muted.sync="muted"
              :music.sync='music'
              :list='list'
            />    
          </article>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Aplayer from "vue-aplayer";

export default {
  name: "HelloWorld",
  components: {
    Aplayer
  },
  props: {
    msg: String
  },
  created() {
    this.music = this.list[0];
  },
  data() {
    return {
      muted: false,
      music3: null,
      list: [
        {
          title: "Zero Opening Stage",
          artist: "Mega Man X Corrupted",
          src:
            "http://66.90.93.122/ost/megaman-x-corrupted/lderepew/05%20-%20Zero%20Opening%20Stage.mp3",
          pic: "https://i.ytimg.com/vi/GQ47immxaQ8/hqdefault.jpg"
        },
        {
          title: "Stickerbrush Symphony",
          artist: "Donkey Kong Country 2",
          src:
            "https://cs1.mp3.pm/download/85870084/M0NsaUt5cTh2bFk0N3lXTUZ3UHovVThsQTZicVpMVGp6UnI3U1FHL2o4azJFT2dSK2R3Q0R1ZmlNL3ZoQUswOUg3bUI1VlIyV3RsV1M3eGo5OEIwdE93SDM2VzVBNUFuWmFpQ09DT3hFZm5NbG5oTXAwejBxeEVLSkdjL2psM2Y/Donkey_Kong_Country_2_-_17._Stickerbrush_Symphony_(mp3.pm).mp3",
          pic:
            "https://cdn02.nintendo-europe.com/media/images/03_teaser_module_1_square/games_3/game_boy_advance_5/TM_GBA_DonkeyKongCountry2.png"
        },
        {
          title: "Into the Wilderness",
          artist: "Wild Arms",
          src:
            "http://66.90.93.122/ost/wild-arms-original-game-soundtrack/kfbkgbxc/01%20into%20the%20wilderness.mp3",
          pic:
            "http://images2.wikia.nocookie.net/__cb20080424154713/wildarms/images/3/3d/Wildarms.jpg"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
</style>
