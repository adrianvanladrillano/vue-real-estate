<template>
  <div>
    <section
      class="hero is-medium header-image"
      style="margin-left: -8vw; margin-right: -8vw; height: "
    >
      <div
        class="hero-body"
        style="margin-left: 8vw; margin-right: 8vw; margin-top: 25px"
      >
        <div class="columns">
          <div class="column">
            <p class="subtitle has-text-white">It's great to be home</p>
            <p
              class="title has-text-white"
              style="font-size: 64px; color: #feaf11"
            >
              Find a property today
            </p>
          </div>
        </div>

        <div class="columns">
          <div class="column is-5">
            <p class="subtitle mb-4 has-text-white">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Cupiditate, quas libero. Praesentium, quae inventore. Explicabo
              nostrum iste eius.
            </p>
          </div>
        </div>

        <div class="columns">
          <div class="column is-8">
            <div class="card p-2" style="border-radius: 12px">
              <div class="columns">
                <div class="column is-3 px-5">
                  <b-field>
                    <div class="block mt-2">
                      <b-radio v-model="radio" name="Rent" native-value="Flint">
                        Buy
                      </b-radio>
                      <b-radio
                        v-model="radio"
                        name="Rent"
                        native-value="Silver"
                      >
                        Rent
                      </b-radio>
                      <b-radio
                        v-model="radio"
                        name="Rent"
                        native-value="Silver"
                      >
                        Sold
                      </b-radio>
                    </div>
                  </b-field>
                </div>
                <div class="column is-6">
                  <b-input
                    placeholder="Search..."
                    icon-pack="fas"
                    icon="search"
                  >
                  </b-input>
                </div>
                <div class="column is-3">
                  <b-button expanded type=" is-primary">Search</b-button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div
        class="hero-footer"
      >
        <CarouselDeveloper />
      </div>
    </section>
  </div>
</template>

<script>
var philippines = require('philippines')
var regions = require('philippines/regions')
var provinces = require('philippines/provinces')
var cities = require('philippines/cities')

export default {
  data() {
    return {
      citiesSelect: [],
      name: '',
    }
  },
  computed: {},
  mounted() {
    console.log(cities)
    this.citiesSelect = cities
  },
}
</script>

<style>
.header-image {
  background-image: url('~/assets/hero.png');
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}
</style>
