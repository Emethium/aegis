<template>
  <div class="home">
    <div class="section has-background-light">
      <div class="columns">
        <!-- Page sidebar -->
        <div class="collumn has-background-light is-one-quarter">
          <aside class="menu">
            <p class="menu-label">
              General
            </p>
            <ul class="menu-list">
              <li @click="revertFiltering()"><a>Home</a></li>
              <router-link to="/contact">Contact</router-link>
              <li><a>About</a></li>
              <li><a>Reccomend a song</a></li>
            </ul>
            <p class="menu-label">
              Categories
            </p>
            <ul class="menu-list" v-for="c in categories" :key="c.id" @click="filterList(c.name)">
              <li><a>{{c.name}}</a></li>
            </ul>
          </aside>
        </div>
        <!-- Main content -->
        <div class="collumn has-background-light">
          <div class="content is-centered">
            <table class="table is-striped is-bordered is-hoverable is-narrow">
              <thead>
                <th class="has-text-success has-text-centered" v-for="c in collumns" :key="c">
                    {{c | capitalize}}
                </th>
              </thead>
              <tbody>
                <tr v-for="s in filteredList" :key="s.id">
                  <td class="has-text-weight-normal has-text-centered">{{s.title}}</td>
                  <td class="has-text-weight-normal has-text-centered">{{s.game}}</td>
                  <td class="has-text-weight-normal has-text-centered">{{s.composer}}</td>
                  <td class="has-text-weight-normal has-text-centered" >{{s.genre}}</td>
                  <td class="has-text-weight-normal has-text-centered">{{s.platform}}</td>
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
  </div>
</template>

<script>
import data from '../assets/data.json'

export default {
  name: "Home",
  components: {
  },
  created() {
    this.categories = this.sortByKey(this.categories, "name")
    this.songList = this.sortByKey(this.songList, "title")
    this.filteredList = this.songList
  },
  data() {
    return {
      songList: data.songs,
      filteredList: [],
      categories: data.categories,
      collumns: ['title', 'game', 'composer', 'genre', 'platform', 'play'],
    };
  },
  filters: {
    capitalize: function (str) {
      return str.charAt(0).toUpperCase() + str.slice(1)
    }
  },
  methods: {
    sortByKey (array, key) {
      return array.sort(function (a, b) {
        var x = a[key]
        var y = b[key]
        return ((x < y) ? -1 : ((x > y) ? 1 : 0))
      })
    },
    filterList (key) {
      this.filteredList = this.songList
      this.filteredList = this.filteredList.filter(function (el) {
        return el.genre.toLowerCase() == key.toLowerCase()
      })
    },
    revertFiltering () {
      this.filteredList = this.songList
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
</style>
