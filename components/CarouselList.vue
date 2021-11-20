<template>
  <div>
    <div class="columns">
      <b-carousel-list
        v-model="test"
        :data="listings"
        :items-to-show="4"
        class="px-5 is-shadowless"
      >
        <template #item="listings">
          <div class="card mr-4" style="border-radius: 12px">
            <div class="card-image">
              <figure class="image is-5by4">
                <a @click="info(items.index)"><img :src="listings.listing_icon" /></a>
              </figure>
              <b-tag
                type="is-medium"
                class="mt-2 ml-2 is-warning"
                size="is-large"
                style="position: absolute; top: 0"
                ><b>50%</b></b-tag
              >
            </div>
            <div class="card-content">
              <div class="media">
                <div class="media-content">
                  <p class="title is-4">{{ listings.listing_name }}</p>
                  <p class="subtitle is-6">
                    <b-icon pack="fas" icon="map-marker-alt" size="is-small" />
                    {{ listings.listing_location }}
                  </p>
                </div>
              </div>

              <div class="content">
                <footer>
                  <div class="columns">
                    <div class="column">
                      <span class="icon-text">
                        <span class="icon">
                          <b-icon pack="fas" icon="bed" size="is-small" />
                        </span>
                        <span class="title is-5">{{ listings.listing_bedroom }}</span>
                        <small class="subtitle is-6">Bedroom(s)</small>
                      </span>
                    </div>
                    <div class="column">
                      <span class="icon-text">
                        <span class="icon">
                          <b-icon pack="fas" icon="toilet" size="is-small" />
                        </span>
                        <span class="title is-5">{{ listings.listing_bathroom }}</span>
                        <small class="subtitle is-6">Restroom(s)</small>
                      </span>
                    </div>
                    <div class="column">
                      <span class="icon-text">
                        <span class="icon">
                          <b-icon
                            pack="fas"
                            icon="chart-area"
                            size="is-small"
                          />
                        </span>
                        <span class="title is-5">{{ listings.listing_land }} Sqm</span>
                        <small class="subtitle is-6">Area</small>
                      </span>
                    </div>
                  </div>

                  <div class="columns">
                    <div class="column">
                      <span class="subtitle is-4" style="float: right">
                        {{ listings.listing_price }}</span
                      >
                      <span class="title is-4">Price: </span>
                      <br />
                      <b-button type="is-primary" expanded
                        >View Property</b-button
                      >
                    </div>
                  </div>
                </footer>
              </div>
            </div>
          </div>
        </template>
      </b-carousel-list>
    </div>

    <div class="columns">
      <div class="column my-5" justify="center" align="center">
        <b-button class="px-5 is-medium is-rounded is-warning"
          >View more</b-button
        >
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      test: 0,
      listings: [],
      items: [
        {
          title: 'Slide 1',
          image: 'https://5.imimg.com/data5/WJ/PR/HS/SELLER-81339524/freeshipping-ice-bingo-i12-earphone-hands-free-png-500x500-500x500.png',
          rating: 4.4,
        },
        {
          title: 'Slide 2',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 3.5,
        },
        {
          title: 'Slide 3',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 5,
        },
        {
          title: 'Slide 4',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
        },
        {
          title: 'Slide 5',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 5,
        },
        {
          title: 'Slide 6',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 4,
        },
        {
          title: 'Slide 7',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 2.7,
        },
        {
          title: 'Slide 8',
          image: 'https://buefy.org/static/img/placeholder-1280x960.png',
          rating: 1.5,
        },
      ],
    }
  },
  mounted() {
    const self = this
    axios
      .get('http://localhost:6969/listings')
      .then(function (response) {
        // handle success
        // console.log(response.data)
        self.listings = response.data
        console.log(self.listings)
      })
      .catch(function (error) {
        // handle error
        console.log(error)
      })
      .then(function () {
        // always executed
      })
  },
  methods: {
    info(value) {
      this.test = value
    },
    getImgUrl(value) {
      return `https://picsum.photos/id/43${value}/1230/800`
    },
  },
}
</script>
