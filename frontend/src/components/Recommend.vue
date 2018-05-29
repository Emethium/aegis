<template>
<div class="recommend has-background-light">
    <div class="section">
        <div class="columns is-gapless">
            <!-- Page sidebar -->
            <div class="column is-2">
                <aside class="menu">
                <p class="menu-label">
                    General
                </p>
                <ul class="menu-list">
                    <router-link to="/">Home</router-link>
                    <router-link to="/contact">Contact</router-link>
                    <router-link to="/recommend">Recommend a song</router-link>
                </ul>
                </aside>
            </div>
            <!-- Main content -->
            <div class="column is-8">
                <div class="content">
                    <div class="control is-centered">
                        <div class="level">
                            <div class="level-item">
                                <div>
                                    <label class="heading">Which game are we talking about?</label>
                                    <input class="input is-focused is-large is-primary" type="text" placeholder="Game goes here">
                                </div>
                            </div>
                            <div class="level-item">
                                <div>
                                    <label class="heading">Now tell me the name of the song</label>
                                    <input class="input is-focused is-large is-primary" type="email" placeholder="Song goes here">
                                </div>
                            </div>
                            <div class="level-item is-centered has-text-centered">
                                <p class="buttons">
                                    <a class="button is-primary is-rounded is-focused is-large">
                                        <span>Please add this song!</span>
                                    </a>
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
  </div>
</div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
@import "../../node_modules/font-awesome/css/font-awesome.min.css";
</style>

<script>
export default {
    name: "Recommend",
    data () {
        return {

        }
    }
}
</script>
