<template>
  <div class="faq">
      <div class="container">
          <section class="section">
              <h1 class="title">FAQ</h1>
              <h2 class="subtitle is-4">Facts About Quolls</h2>
              <img id="quoll-img" alt="Facts About Quolls" src="https://www.activewild.com/wp-content/uploads/2015/12/Quoll-Facts-For-Kids-624x416.jpg">

              <div class="columns" v-if="faqs && faqs.length">
                  <div class="column is-one-third" v-for="faq of faqs" :key="faq">
                      <div class="card">
                          <div class="card-content">
                              <p class="title">{{ faq.title }}</p>
                              <p class="answer">{{ faq.body }}</p>
                          </div>
                      </div>
                  </div>
              </div>
          </section>
      </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'faq',
  data: () => ({
    faqs: [],
    errors: []
  }),

  created () {
    axios.get('http://localhost:8080/static/quoll.json')
      .then(response => {
        this.faqs = response.data.slice(0, 10)
      })
      .catch(e => {
        this.errors.push(e)
      })
  }
}
</script>

<style lang="sass" scoped>
@import '../mq'

.pd
    padding: 2.5em 0 1.5em 0

.answer
    margin-top: 10px !important
    color: gray

.columns
    flex-wrap: wrap

#quoll-img
    display: block
    margin: 0 auto
    padding: 1.5rem 0 3rem 0

</style>
