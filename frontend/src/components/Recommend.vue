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
                                    <input class="input is-focused is-large is-primary" type="email" placeholder="Song goes heres">
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
                <div class="section has-background-light">
                    <div class="content fill">
                        <div class="icon audio">
                            <i></i>
                            <i></i>
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
.fill {
    height: 430px;
}

.icon {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 16em;
  height: 16em;
  transform: translate(-50%,-50%);
}

/* Audio */

.audio { color: #1fd13f; }

.audio::after,
.audio i,
.audio i::before,
.audio i::after {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  display: block;
  width: 0.25em;
  height: 0.5em;
  transform: translate(-50%,-50%);
  background: currentColor;
  border-radius: 0.125em;
}

.audio::after { animation: audio4 1.35s infinite; }

.audio i::before {
  left: -0.8125em;
  animation: audio1 1.35s infinite;
}
.audio i::after {
  left: 1.0625em;
  animation: audio3 1.35s infinite;
}

.audio i:first-child {
  margin-left: -1.875em;
  animation: audio2 1.35s infinite;
}

.audio i:last-child {
  margin-left: 1.875em;
  animation: audio6 1.35s infinite;
}

.audio i:last-child::before { animation: audio5 1.35s infinite; }

.audio i:last-child::after { animation: audio7 1.35s infinite; }

@keyframes audio1 {
  9% { height: 1.75em; }
  36% { height: 0.5em; }
  42% { height: 2.375em; }
  69% { height: 0.5em; }
  76% { height: 3.625em; }
  100% { height: 1em; }
}

@keyframes audio2 {
  9% { height: 5.5em; }
  36% { height: 0.5em; }
  42% { height: 5.5em; }
  69% { height: 0.5em; }
  76% { height: 6.75em; }
  100% { height: 1em; }
}

@keyframes audio3 {
  9% { height: 6.5em; }
  36% { height: 0.5em; }
  42% { height: 3.5em; }
  69% { height: 0.5em; }
  76% { height: 3.5em; }
  100% { height: 1em; }
}

@keyframes audio4 {
  9% { height: 1.875em; }
  36% { height: 0.5em; }
  42% { height: 3.75em; }
  69% { height: 0.5em; }
  76% { height: 5.625em; }
  100% { height: 1em; }
}

@keyframes audio5 {
  9% { height: 5em; }
  36% { height: 0.5em; }
  42% { height: 1.25em; }
  69% { height: 0.5em; }
  76% { height: 3.75em; }
  100% { height: 1em; }
}

@keyframes audio6 {
  9% { height: 6.125em; }
  36% { height: 0.5em; }
  42% { height: 6.875em; }
  69% { height: 0.5em; }
  76% { height: 2.5em; }
  100% { height: 1em; }
}

@keyframes audio7 {
  9% { height: 3.125em; }
  36% { height: 0.5em; }
  42% { height: 1.875em; }
  69% { height: 0.5em; }
  76% { height: 3.75em; }
  100% { height: 1em; }
}

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
