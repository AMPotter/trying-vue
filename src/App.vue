<template>
  <div id="app">
    <div class="nav has-shadow">
      <div class="container">
        <div class="nav-left">
          <p><a class="nav-item">Andrew Learns Vue: The Website</a></p>
        </div>

        <span class="nav-toggle" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="nav-right nav-menu" v-bind:class="{ 'is-active': isActive }">

          <router-link to="/" class="nav-item r-item">Home</router-link>
          <!-- <router-link to="about" class="nav-item r-item">About</router-link> -->
          <!-- <router-link to="faq" class="nav-item r-item">FAQ</router-link> -->

        </div>
      </div>
    </div>

    <router-view></router-view>

    <footer class="is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>i.am.andrew.potter@gmail.com</p>
          </div>
          <div class="column has-text-right is-one-quarter">
            <a class="icon" href="http://linkedin.com/profile/"><i class="fa fa-linkedin"></i></a>
            <a class="icon" href="http://github.com/AMPotter"><i class="fa fa-github"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function () {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

.button.is-primary.is-outlined
  border-color: $primary !important
  color: $primary !important

.nav
  background-color: #383838
  text-align: center
  a:hover
    color: gray

.nav-left a
  color: #fff
  font-weight: bold

a.r-item
  color:#C1C1C1
  padding: 0.5rem 1.75rem
  +mobile
    color: gray
    &:hover
      background-color: #F1F1F1

.nav-toggle span
  background-color: #C1C1C1

footer
  background-color: $primary !important
  color: #fff

  .icon
    color: #fff
    margin-left: 20px

</style>
