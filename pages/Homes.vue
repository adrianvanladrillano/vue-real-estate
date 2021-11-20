<template>
  <div>
    <!-- <Hero /> -->

    <!-- <Headline style="margin-left: -8vw; margin-right: -8vw" /> -->
    <div class="container-fluid mt-5">
      <div class="columns">
        <div class="column is-2">
          <div class="box">
            <h3 class="subtitle" style="font-weight: 700">Property Type</h3>
            <div class="columns">
              <div class="column">
                <button class="button is-primary is-light is-fullwidth">
                  House
                </button>
              </div>

              <div class="column">
                <button class="button is-primary is-light is-fullwidth">
                  Commercial
                </button>
              </div>
            </div>

            <div class="columns">
              <div class="column">
                <button class="button is-primary is-light is-fullwidth">
                  Apartment
                </button>
              </div>

              <div class="column">
                <button class="button is-primary is-light is-fullwidth">
                  Landplot
                </button>
              </div>
            </div>

            <h3 class="subtitle mt-5" style="font-weight: 700">Price Range</h3>
            <b-field
              :label="`${slider[0].toLocaleString()}-${slider[1].toLocaleString()}`"
            >
              <b-field>
                <b-slider
                  lazy
                  v-model="slider"
                  type="is-primary"
                  :min="100000"
                  :max="9999999"
                  :step="2"
                >
                </b-slider>
              </b-field>
            </b-field>

            <h3 class="subtitle mt-5" style="font-weight: 700">
              Room Property
            </h3>
            <div class="columns is-mutiline">
              <div class="column">
                <a class="button is-light">
                  <span style="font-weight: 700">1</span>
                </a>
              </div>

              <div class="column">
                <a class="button is-light">
                  <span style="font-weight: 700">1</span>
                </a>
              </div>

              <div class="column">
                <a class="button is-light">
                  <span style="font-weight: 700">1</span>
                </a>
              </div>

              <div class="column">
                <a class="button is-light">
                  <span style="font-weight: 700">1</span>
                </a>
              </div>
            </div>

            <h3 class="subtitle mt-5" style="font-weight: 700">Bathroom</h3>
            <div class="columns">
              <div class="column">
                <a class="button is-light">
                  <span style="font-weight: 700">1</span>
                </a>
              </div>
            </div>

            <h3 class="subtitle mt-5" style="font-weight: 700">Amenities</h3>
            <div class="columns">
              <div class="column">
                <b-checkbox v-model="checkbox" label="">
                  Installment
                </b-checkbox>
                <br />
                <b-checkbox v-model="checkbox" label="" class="mt-2">
                  Pet Friendly
                </b-checkbox>
                <br />
                <b-checkbox v-model="checkbox" label="" class="mt-2">
                  Pet Friendly
                </b-checkbox>
              </div>
            </div>
          </div>
        </div>

        <div class="column is-10">
          <!-- <SectionTitle
            title="List of all Properties"
            subtitle="Lorem Ipsum."
            icon="asdsd"
          /> -->
 

          <div class="columns">
            <div class="column mx-5">
              <span><strong>1,235</strong> properties listed </span>
            </div>

            <div class="column mx-5">
              <div class="field is-grouped is-grouped-right">
                <b-select
                  placeholder="Filter by"
                  rounded
                  class="is-pulled-right"
                >
                  <option value="flint">Price (High to low)</option>
                  <option value="silver">Price (Low to high)</option>
                  <option value="vane">Old to New</option>
                  <option value="billy">New to Old</option>
                  <option value="jack">Ratings</option>
                  <option value="jack">Sold</option>
                </b-select>

                <a class="button is-primary mr-2 is-grouped-right">
                  <b-icon pack="fas" icon="boxes" size="is-small" />
                </a>

                <a class="button is-light mr-2 is-grouped-right">
                  <b-icon pack="fas" icon="list" size="is-small" />
                </a>
              </div>
            </div>
          </div>

          <div class="columns is-multiline px-5 py-5">
            <div
              class="column is-3"
              v-for="listing in listings"
              :key="listing.listing_id"
            >
              <NuxtLink :to="{ path: '/ViewHome/' + listing.listing_id }">
                <div class="card" style="border-radius: 12px" >
                  <div class="card-image">
                    <b-carousel :indicator-inside="false">
                      <b-carousel-item v-for="(item, i) in 6" :key="i">
                        <span class="image is-5by4">
                          <img :src="getImgUrl(i)" />
                        </span>
                      </b-carousel-item>
                      <template #indicators="props">
                        <span class="al image">
                          <img :src="getImgUrl(props.i)" :title="props.i" />
                        </span>
                      </template>
                    </b-carousel>
                  </div>
                  <div class="card-content">
                    <div class="media">
                      <div class="media-content">
                        <p class="title is-6">
                          {{ listing.listing_name }}
                          <br />
                          <small
                            class=""
                            style="opacity: 0.8; font-weight: 400"
                          >
                            {{ listing.listing_location }}
                          </small>
                        </p>
                      </div>
                    </div>

                    <div class="content">
                      <footer>
                        <!-- <div class="columns">
                          <div class="column">
                            <span class="icon-text">
                              <span class="icon">
                                <b-icon pack="fas" icon="bed" size="is-small" />
                              </span>
                              <span class="title is-5">2</span>
                              <small class="subtitle is-6">Bedroom(s)</small>
                            </span>
                          </div>
                          <div class="column">
                            <span class="icon-text">
                              <span class="icon">
                                <b-icon
                                  pack="fas"
                                  icon="toilet"
                                  size="is-small"
                                />
                              </span>
                              <span class="title is-5">2</span>
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
                              <span class="title is-5">50 Sqm</span>
                              <small class="subtitle is-6">Area</small>
                            </span>
                          </div>
                        </div> -->

                        <div class="columns">
                          <div class="column">
                            <span class="is-size-5 has-text-weight-bold">
                              PHP 999,999.00</span
                            >
                            <br />
                            <!-- <b-button
                              tag="router-link"
                              :to="{ path: '/ViewHome/' + 'asdas' }"
                              type="is-primary is-fullwidth"
                              >View Property</b-button
                            > -->
                          </div>
                        </div>
                      </footer>
                    </div>
                  </div>
                </div>
              </NuxtLink>
            </div>
          </div>

          <div class="columns">
            <div class="column mx-5">
              <b-pagination
                :total="total"
                v-model="current"
                :range-before="rangeBefore"
                :range-after="rangeAfter"
                :order="order"
                :size="size"
                :simple="isSimple"
                :rounded="isRounded"
                :per-page="perPage"
                :icon-prev="prevIcon"
                :icon-next="nextIcon"
                aria-next-label="Next page"
                aria-previous-label="Previous page"
                aria-page-label="Page"
                aria-current-label="Current page"
              >
              </b-pagination>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Breadcrumb from '~/components/Breadcrumb.vue'
import axios from 'axios'

export default {
  components: { Breadcrumb },
  data() {
    return {
      // Pagination
      slider: [0, 0],

      //   Arrays
      carousels: [
        {
          text: 'Slide 1',
          color: 'primary',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
        {
          text: 'Slide 2',
          color: 'info',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
        {
          text: 'Slide 3',
          color: 'primary',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
        {
          text: 'Slide 4',
          color: 'warning',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
        {
          text: 'Slide 5',
          color: 'primary',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
      ],
      items: [
        {
          title: '1',
        },
        {
          title: '2',
        },
        {
          title: '3',
        },
        {
          title: '4',
        },
        {
          title: '5',
        },
        {
          title: '6',
        },
        {
          title: '4',
        },
        {
          title: '5',
        },
        {
          title: '6',
        },
      ],
      listings: [],
    }
  },
  methods: {
    getImgUrl(value) {
      return `https://picsum.photos/id/43${value}/1230/800`
    },
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
}
</script>

<style></style>
