<template>
<div class="contact has-background-light">
    <div class="section">
        <div class="columns is-gapless">
            <!-- Page sidebar -->
            <div class="column is-3">
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
            <div class="column is-6">
                <div class="content">
                    <div class="control is-centered">
                        <div class="level">
                            <div class="level-left is-centered has-text-centered">
                                <div class="level-item">
                                    <div>
                                        <label class="heading">Enter your beautiful name</label>
                                        <input class="input is-focused is-large is-primary" type="text" placeholder="Identify yourself">
                                    </div>
                                </div>
                            </div>
                            <div class="level-right is-centered has-text-centered">
                                <div class="level-item">
                                    <div>
                                        <label class="heading">Give me your email so I can reply back</label>
                                        <input class="input is-focused is-large is-primary" type="email" placeholder="Email goes here">
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="level">
                            <div class="level-item">
                                <div class="field is-centered">
                                    <div class="control is-centered has-text-centered">
                                        <label class="heading">Enlighten me about your thoughts</label>
                                        <textarea class="textarea is-primary is-large is-focused" type="text" placeholder="Discuss your dreams and hopes"></textarea>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="level">
                            <div class="level-item">
                                <p class="buttons">
                                    <a class="button is-primary is-rounded is-focused is-large">
                                        <span>Feed me mails!</span>
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
textarea {
    width: 900px;
    height: 200px;
}
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
