<template>
<div class="contact">
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
                    <li><a>Contact</a></li>
                    <li><a>About</a></li>
                    <li><a>Reccomend a song</a></li>
                </ul>
                </aside>
            </div>
            <!-- Main content -->
            <div class="collumn has-background-light">
                <div class="content is-centered">
                </div>
            </div>
        </div>
  </div>
</div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/bulma/css/bulma.min.css";
</style>

<script>
export default {
    name: "Contact",
    data () {
        return {

        }
    }
}
</script>
