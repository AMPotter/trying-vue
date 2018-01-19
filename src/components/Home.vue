<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
          <div class="is-paddingless">
            <h2 class="subtitle is-4">{{ subheading }}</h2>
          </div>
          <a class="button is-large is-primary" id="learn" href="http://github.com/AMPotter">Here's my GitHub!</a>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1 has-text-centered">
            <i class="fa fa-cog is-primary"></i>
          </div>
          <div class="column is-one-third-desktop">
            <p class="title"><strong>I checked out Vue.JS today. It's neat.<br><br>Click on my projects below. Thanks!</strong></p>
          </div>
          <div class="column">
            <p><strong>I think the work you do is fantastic. The websites you build are striking and elegant, and I can think of no better place for me to grow as a developer by working hard with a great team to deliver consistent, clean, and jaw-dropping results.<br><br>I want to work with <a class="fine-link" href="https://www.wearefine.com/assets/images/hero_quote.jpg">giants</a>.<br><br>And I want to pet that <a class="fine-link" href="http://wearefine.com/assets/images/home/FINE_hero1-724648c68c7ad6960e949e582345852eadd823204851c39bde30dad3f3c71f55.jpg">dog</a>.</strong></p>
          </div>
        </div>
      </div>

      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title"><a class="button is-primary card-button" href="http://bushroot.herokuapp.com">Bushroot</a></p>
              <p class="subtitle">Plan your next garden.<br><br>Full MERN stack</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title"><a class="button is-primary card-button" href="http://bookbagpdx.herokuapp.com">Bookbag</a></p>
              <p class="subtitle">Discover your next page-turner.<br><br>MVC/Handlebars/jQuery/PostgreSQL/Tastedive API</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="title"><a class="button is-primary card-button" href="https://github.com/jubilant-disco/jubilant-disco">Jubilant Disco</a></p>
              <p class="subtitle">Find your next record-swapping buddy.<br><br>MongoDB/Mongoose/Discogs API (Back-end only)</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      heading: 'Andrew Potter Writes Code',
      subheading:
        'And I\'d love to write lots of code for FINE, if you\'ll have me.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='sass' scoped>
@import '../mq'

.hero
  text-align: center

  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem

h2
  margin: 1.5rem 0 2rem 0 !important

.button
  background-color: $primary !important

.fa-cog
  font-size: 40px

#learn
  +desktop
    margin-bottom: 2rem

.pd
  +tablet
    padding: 2em 0

.card-button
  display: block
  margin: 0 auto
  text-align: center

.fine-link
  color: $primary !important

</style>
