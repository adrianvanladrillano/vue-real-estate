<template>
  <div>
    <!-- <Hero /> -->
    <div class="container-fluid" style="margin-left: -8vw; margin-right: -8vw">
      <div class="columns">
        <div class="column">
          <b-carousel :indicator-inside="false">
            <b-carousel-item v-for="(item, i) in 6" :key="i">
              <span class="image">
                <img
                  src="https://static-ph.lamudi.com/static/media/bm9uZS9ub25l/2x2x5x880x450/3215ac92d86e0e.jpg"
                  style="height: 70vh"
                />
              </span>
            </b-carousel-item>
          </b-carousel>
        </div>
      </div>
    </div>
    <div class="" style="margin-top: -15vh">
      <div class="card">
        <div class="columns">
          <div class="column px-5 py-5 mx-4 my-4">
            <div class="columns">
              <div class="column">
                <h1 class="title" style="font-weight: 700; color: ">
                  1-Bedroom Unit for Sale in SMDC South Residences, Las Piñas
                  City
                </h1>

                <h2 class="subtitle" style="color: #; opacity: 0.7">
                  Tandang Sora, Quezon City, Metro Manila
                </h2>
              </div>
            </div>

            <div class="columns">
              <div class="column">
                <span class="is-size-2" style="font-weight: 700; color: #2d3161"
                  >₱ 3,400,000</span
                >
                <p style="opacity: 0.8">20% Downpayment required</p>
              </div>
            </div>

            <div class="columns is-multiline">
              <div class="column">
                <div
                  class="card px-5 py-4"
                  style="border-left: 8px solid #2d3161"
                >
                  <span class="is-size-6" style="opacity: 0.8">
                    Bedroom(s)
                  </span>
                  <p class="is-size-5 has-text-weight-semibold">2 Bedrooms</p>
                </div>
              </div>

              <div class="column">
                <div
                  class="card px-5 py-4"
                  style="border-left: 8px solid #2d3161"
                >
                  <span class="is-size-6" style="opacity: 0.8">
                    Bathroom(s)
                  </span>
                  <p class="is-size-5 has-text-weight-semibold">2 Bedrooms</p>
                </div>
              </div>

              <div class="column">
                <div
                  class="card px-5 py-4"
                  style="border-left: 8px solid #2d3161"
                >
                  <span class="is-size-6" style="opacity: 0.8">
                    Floor area
                  </span>
                  <p class="is-size-5 has-text-weight-semibold">365 m2</p>
                </div>
              </div>
            </div>

            <div
              class="columns is-multiline mt-5 mx-1"
              style="background: #f6f7fa; border-radius: 12px"
            >
              <div class="column is-6">
                <span class="is-size-6" style="opacity: 0.8">Project</span>
                <p class="is-size-5 has-text-weight-semibold">
                  SMDC South Residences
                </p>
              </div>

              <div class="column is-6">
                <span class="is-size-6" style="opacity: 0.8">Developer</span>
                <p class="is-size-5 has-text-weight-semibold">Ayala Lands</p>
              </div>

              <div class="column is-6">
                <span class="is-size-6" style="opacity: 0.8"
                  >Property Type</span
                >
                <p class="is-size-5 has-text-weight-semibold">Condominium</p>
              </div>

              <div class="column is-6">
                Downpayment:
                <h2 class="subtitle" style="color: #2d3161; font-weight: 500">
                  20% ({{ (this.price * 0.2).toLocaleString() }})
                </h2>
              </div>
            </div>

            <div class="columns my-5">
              <div class="column">
                <article class="media">
                  <figure class="media-left">
                    <p class="image is-64x64">
                      <img
                        src="https://bulma.io/images/placeholders/128x128.png"
                        class="is-rounded"
                      />
                    </p>
                  </figure>
                  <div class="media-content">
                    <div class="content">
                      <p>
                        <strong>Anjo Liwanag</strong> <small>@johnsmith</small>
                        <small>31m</small>
                        <br />
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Proin ornare magna eros, eu pellentesque tortor
                        vestibulum ut. Maecenas non massa sem. Etiam finibus
                        odio quis feugiat facilisis.
                      </p>
                    </div>
                  </div>
                </article>
              </div>
            </div>

            <div class="columns">
              <div class="column is-4">
                <b-button
                  class="is-expandable is-primary"
                  style="background: #feaf11"
                  expanded
                  @click="modalContact = true"
                >
                  Contact Agent
                </b-button>
              </div>

              <div class="column">
                <b-button
                  class="is-expandable is-primary"
                  style="background: #2d3161"
                  expanded
                  >Book a Viewing</b-button
                >
              </div>
            </div>
          </div>

          <div class="column is-6" style="padding: ">
            <div class="mapouter">
              <div class="gmap_canvas">
                <iframe
                  width="1920"
                  height="800"
                  id="gmap_canvas"
                  src="https://maps.google.com/maps?q=2880%20Broadway,%20New%20York&t=&z=13&ie=UTF8&iwloc=&output=embed"
                  frameborder="0"
                  scrolling="no"
                  marginheight="0"
                  marginwidth="0"
                ></iframe
                ><style>
                  .mapouter {
                    text-align: right;
                    height: 100%;
                    width: 100%;
                  }</style
                ><style>
                  .gmap_canvas {
                    overflow: hidden;
                    background: none !important;
                    height: 100%;
                    width: 100%;
                  }
                </style>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid mt-5">
      <div class="card px-5 py-5 mt-5">
        <div class="columns">
          <div class="column">
            <span class="is-size-2">
              Description
            </span>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam minus molestias odit, cumque ducimus, pariatur laudantium officiis facere a ipsa nemo ea at corporis saepe natus reiciendis accusamus. Iure, placeat!
            </p>

            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ullam minus molestias odit, cumque ducimus, pariatur laudantium officiis facere a ipsa nemo ea at corporis saepe natus reiciendis accusamus. Iure, placeat!
            </p>
          </div>
        </div>
        <b-tabs type="is-toggle" expanded>
          <b-tab-item label="Information" icon="home">
            <div class="columns">
              <div class="column">
                <h1 class="title" style="font-weight: 700; color: #">
                  Additional Information
                </h1>

                <h2
                  class="subtitle"
                  style="color: #; font-weight: ; opacity: 0.8"
                >
                  Something here
                </h2>
              </div>
            </div>

            <div class="columns">
              <div class="column is-6">
                <p style="font-weight: 500; font-size: 24px">Floor plan</p>
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Doloremque rem minima blanditiis natus, accusamus possimus
                  illum eius, voluptate maxime aut autem facere molestias porro
                  obcaecati inventore et, ducimus ipsum necessitatibus.
                </p>

                <p class="mt-5">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Doloremque rem minima blanditiis natus, accusamus possimus
                  illum eius, voluptate maxime aut autem facere molestias porro
                  obcaecati inventore et, ducimus ipsum necessitatibus.
                </p>
              </div>

              <div class="column is-6">
                <img
                  src="https://www.roomsketcher.com/wp-content/uploads/2017/11/RoomSketcher-Site-Plan-Software-3D-Site-Plan.jpg"
                  style="width: 100%"
                  alt=""
                />
              </div>
            </div>
          </b-tab-item>
          <b-tab-item label="Amenities" icon="home">
            <div class="columns">
              <div class="column">
                <h1 class="title" style="font-weight: 700; color: #2d3161">
                  Amenities
                </h1>

                <h2 class="subtitle" style="color: #feaf11; font-weight: 500">
                  LOREM UPSUM
                </h2>
              </div>
            </div>
            <div class="columns">
              <div class="column is-6">
                <p style="font-weight: 500; font-size: 24px">Clubhouse</p>
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Doloremque rem minima blanditiis natus, accusamus possimus
                  illum eius, voluptate maxime aut autem facere molestias porro
                  obcaecati inventore et, ducimus ipsum necessitatibus.
                </p>

                <p class="mt-5">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Doloremque rem minima blanditiis natus, accusamus possimus
                  illum eius, voluptate maxime aut autem facere molestias porro
                  obcaecati inventore et, ducimus ipsum necessitatibus.
                </p>
              </div>

              <div class="column card is-6">
                <img
                  src="http://images.summitmedia-digital.com/spotph/images/2019/03/20/2019-public-pools-640-1553043220.jpg"
                  style="width: 100%"
                  alt=""
                />
              </div>
            </div>
          </b-tab-item>
          <b-tab-item label="Location" icon="home">
            <div class="columns">
              <div class="column">
                <h1 class="title" style="font-weight: 700; color: #2d3161">
                  Location
                </h1>

                <h2 class="subtitle" style="color: #feaf11; font-weight: 500">
                  LOREM UPSUM
                </h2>
              </div>
            </div>
            <div class="columns">
              <div class="column is-8">
                <div class="mapouter">
                  <div class="gmap_canvas">
                    <iframe
                      width="1920"
                      height="1080"
                      id="gmap_canvas"
                      src="https://maps.google.com/maps?q=2880%20Broadway,%20New%20York&t=&z=13&ie=UTF8&iwloc=&output=embed"
                      frameborder="0"
                      scrolling="no"
                      marginheight="0"
                      marginwidth="0"
                    ></iframe
                    ><style>
                      .mapouter {
                        text-align: right;
                        height: 100%;
                        width: 100%;
                      }</style
                    ><style>
                      .gmap_canvas {
                        overflow: hidden;
                        background: none !important;
                        height: 100%;
                        width: 100%;
                      }
                    </style>
                  </div>
                </div>
              </div>
              <div class="column is-4">
                <p style="font-weight: 500; font-size: 24px">Transportations</p>
                <ul>
                  <li>Ayala malls</li>
                  <li>Ayala malls</li>
                </ul>

                <p class="mt-5" style="font-weight: 500; font-size: 24px">
                  Hospitals
                </p>
                <ul>
                  <li>Ayala malls</li>
                  <li>Ayala malls</li>
                </ul>

                <p class="mt-5" style="font-weight: 500; font-size: 24px">
                  Schools
                </p>
                <ul>
                  <li>Ayala malls</li>
                  <li>Ayala malls</li>
                </ul>

                <p class="mt-5" style="font-weight: 500; font-size: 24px">
                  Malls/Supermarkets
                </p>
                <ul>
                  <li>Ayala malls</li>
                  <li>Ayala malls</li>
                </ul>

                <p class="mt-5" style="font-weight: 500; font-size: 24px">
                  Others
                </p>
                <ul>
                  <li>Ayala malls</li>
                  <li>Ayala malls</li>
                </ul>
              </div>
            </div>
          </b-tab-item>
        </b-tabs>
      </div>
    </div>
    <b-modal v-model="modalContact" :width="640" scroll="keep">
      <div class="card p-5">
        <div class="card-title" justify="center" align="center">
          <h1 class="title" style="font-weight: 700; color: #2d3161">
            Ask about the property
          </h1>

          <h2 class="subtitle" style="color: #feaf11; font-weight: 500">
            We are ready to assist in finding your new Home!
          </h2>
        </div>

        <div class="card-content">
          <div class="columns">
            <div class="column">
              <b-field label="First name">
                <b-input placeholder="Enter First name Here.."></b-input>
              </b-field>

              <b-field label="Last name">
                <b-input placeholder="Enter Last name Here.."></b-input>
              </b-field>

              <b-field label="Phone number">
                <p class="control">
                  <span class="button is-static">+63</span>
                </p>
                <b-input
                  type="number"
                  placeholder="999-999-9999"
                  expanded
                ></b-input>
              </b-field>

              <b-field label="Email Address">
                <b-input placeholder="Enter Email Here.." expanded></b-input>
              </b-field>

              <b-button
                style="background: #feaf11"
                class="is-primary mt-5"
                expanded
                >Contact Agent</b-button
              >
            </div>
          </div>
          <div class="content">
            By clicking Contact Seller, you are accepting Lamudi's
            <a>Terms and Condition </a> and <a> Privacy Policy page</a>.
          </div>

          <div class="columns" justify="center" align="center">
            <div class="column">- OR -</div>
          </div>

          <h2
            class="subtitle"
            justify="center"
            align="center"
            style="color: #2d3161; font-weight: 500"
          >
            Call or Message us at
          </h2>

          <div class="columns" justify="center" align="center">
            <div class="column">
              <p>
                <strong>Globe:</strong>
                <br />
                +63 995-900-5870
              </p>
            </div>

            <div class="column">
              <p>
                <strong style="color: #2d3161">Smart:</strong>
                <br />
                +63 995-900-5870
              </p>
            </div>
          </div>
        </div>
      </div>
    </b-modal>
  </div>
</template>

<script>
import Breadcrumb from '~/components/Breadcrumb.vue'
export default {
  components: { Breadcrumb },
  data() {
    return {
      price: 5000000,
      years: 30,
      // Pagination
      modalContact: false,
      details: [
        { title: 'Bedroom', icon: 'bed', subtitle: '', value: '1' },
        { title: 'Bathroom', icon: 'shower', subtitle: '', value: '2' },
        {
          title: 'Floor area (m²)',
          icon: 'chart-area',
          subtitle: '',
          value: '3',
        },
        {
          title: 'Land Size (m²)',
          icon: 'chart-bar',
          subtitle: '',
          value: '4',
        },
        { title: 'Available from', icon: 'calendar', subtitle: '', value: '5' },
      ],

      //   Arrays
      carousels: [
        {
          text: 'Slide 1',
          color: 'primary',
          img:
            'https://static-ph.lamudi.com/static/media/bm9uZS9ub25l/2x2x6x1200x900/ba423af47d7706.jpg',
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
        {
          text: 'Slide 6',
          color: 'primary',
          img:
            'https://image.freepik.com/free-photo/luxury-interior-living-room-dining-table-studio-room-type-condominium-apartment_41418-2779.jpg',
        },
      ],
      items: [
        {
          title: '1',
        },
      ],
    }
  },
  methods: {
    getImgUrl(value) {
      return `https://picsum.photos/id/43${value}/1230/800`
    },
  },
}
</script>

<style></style>
