<template>
  <div class="hello">
    <div class="columns">
      <!-- Page sidebar -->
      <div class="collumn is-one-quarter has-background-light">
        <aside class="menu is-light">
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
              <a class="is-active is-primary">Manage Your Team</a>
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

      <div class="collumn is-three-quarters has-background-light">
        <div class="media">
          <div class="tile">
            <article class="tile is-child notification is-light">
              <aplayer autoplay
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
              <aplayer autoplay
                :music="{
                  title: 'Stickerbrush Symphony',
                  artist: 'Donkey Kong Country 2',
                  src: 'https://cs1.mp3.pm/download/85870084/M0NsaUt5cTh2bFk0N3lXTUZ3UHovVThsQTZicVpMVGp6UnI3U1FHL2o4azJFT2dSK2R3Q0R1ZmlNL3ZoQUswOUg3bUI1VlIyV3RsV1M3eGo5OEIwdE93SDM2VzVBNUFuWmFpQ09DT3hFZm5NbG5oTXAwejBxeEVLSkdjL2psM2Y/Donkey_Kong_Country_2_-_17._Stickerbrush_Symphony_(mp3.pm).mp3',
                  pic: 'https://cdn02.nintendo-europe.com/media/images/03_teaser_module_1_square/games_3/game_boy_advance_5/TM_GBA_DonkeyKongCountry2.png'
                }"
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
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
</style>
