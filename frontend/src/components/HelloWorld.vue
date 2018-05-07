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
            <li><a>Dashboard</a></li>
            <li><a>Customers</a></li>
          </ul>
          <p class="menu-label">
            Administration
          </p>
          <ul class="menu-list">
            <li><a>Team Settings</a></li>
            <li>
              <a class="is-active">Manage Your Team</a>
              <ul>
                <li><a>Members</a></li>
                <li><a>Plugins</a></li>
                <li><a>Add a member</a></li>
              </ul>
            </li>
            <li><a>Invitations</a></li>
            <li><a>Cloud Storage Environment Settings</a></li>
            <li><a>Authentication</a></li>
          </ul>
          <p class="menu-label">
            Transactions
          </p>
          <ul class="menu-list">
            <li><a>Payments</a></li>
            <li><a>Transfers</a></li>
            <li><a>Balance</a></li>
          </ul>
        </aside>
      </div>
      <!-- Main content -->
      <div class="collumn has-background-light is-three-quarters">
        <div class="media">
          <div class="tile is-pulled-right">
            <article class="tile is-child notification is-light">
              <aplayer
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
      controls: false,
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
