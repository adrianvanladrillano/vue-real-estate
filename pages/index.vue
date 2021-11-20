<template>
<div >
  <Hero />
    <SectionTitle title="Featured Properties" subtitle="Lorem Ipsum." icon="asdsd" />
    <CarouselList />

    <!-- <section class="hero my-5 headline" style="padding-left: -8vw;padding-right: -8vw;">
      <div class="hero-body py-5" style="margin-left: 8vw;margin-right: 8vw;">
        <div class="columns">
          <div class="column is-4">
            <img src="~/assets/fam.png" alt="" style="width: 100%;">
          </div>
          <div class="column is-8">
            <p class="title" style="font-weight: 700;color: #feaf11;font-size: 48px;">
          Financing made easy
        </p>
        <p class="subtitle  mt-2" style="color: #2D3161">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eaque deleniti, distinctio omnis provident modi mollitia sequi. Porro laboriosam libero fugit aperiam quia maxime odit tempora ducimus accusantium, cumque officiis temporibus!
        </p>

        <p class="subtitle " style="color: #2D3161">
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eaque deleniti, distinctio omnis provident modi mollitia sequi. 
        </p>
          </div>
        </div>
        
      </div>

      
    </section> -->

    <SectionTitle title="Properties on sale" subtitle="Lorem Ipsum." icon="asdsd" />
    
    <CarouselList />
    <!-- <div class="columns is-multiline px-5 py-5">
      <div class="column is-4 is-rounded" v-for="item in items" :key="item.text">
        <div class="card"  style="border-radius: 12px;">
          <div class="card-image">
            <b-carousel :indicator-inside="false">
              <b-carousel-item v-for="(item, i) in 6" :key="i">
                <span class="image">
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
                <p class="title is-4">Studio type - Ayala lands</p>
                <p class="subtitle is-6">
                  <b-icon pack="fas" icon="map-marker-alt" size="is-small" />
                  Parañaque
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
                      <span class="title is-5">2</span>
                      <small class="subtitle is-6">Bedroom(s)</small>
                    </span>
                  </div>
                  <div class="column">
                    <span class="icon-text">
                      <span class="icon">
                        <b-icon pack="fas" icon="toilet" size="is-small" />
                      </span>
                      <span class="title is-5">2</span>
                      <small class="subtitle is-6">Restroom(s)</small>
                    </span>
                  </div>
                  <div class="column">
                    <span class="icon-text">
                      <span class="icon">
                        <b-icon pack="fas" icon="chart-area" size="is-small" />
                      </span>
                      <span class="title is-5">50 Sqm</span>
                      <small class="subtitle is-6">Area</small>
                    </span>
                  </div>
                </div>

                <div class="columns">
                  <div class="column">
                    <span class="subtitle is-4" style="float: right">
                      999,999.00</span
                    >
                    <span class="title is-4">Price: </span>
                    <br />
                    <b-button type="is-success" expanded
                      >View Property</b-button
                    >
                  </div>
                </div>
              </footer>
            </div>
          </div>
        </div>
      </div>
     </div>

    <div class="columns my-5">
      <div class="column is-offset-5 is-2">
        <b-button type="is-success is-rounded" expanded>View more</b-button>
      </div>
    </div> -->
<!-- 
    <SectionTitle title="Browse Our Most Popular Locations" subtitle="Rent a quality place in three easy steps!" icon="asdsd" />

    <div class="container">
      <Places />
    </div> -->
<!-- 
    <div class="columns">
      <div class="column is-whole">
        <img src="~/assets/perks.png" style="wdith: 50%;" alt="">
      </div>
    </div>

    <section
      class="hero mt-5 px-5"
      style="background-img: url('/assets/bg.png)"
    >
      <div class="hero-body px-5" style="">
        <div class="columns px-5">
          <div class="column">
            <p class="subtitle" style="font-weight: 500">
              OUR LATEST HOUSE TOUR
            </p>
            <p class="title">
              SHOCKINGLY HUGE MANSION | ICONIC HERITAGE MANSION IN AYALA ALABANG
            </p>
            <p class="subtitle">
             Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum non temporibus accusantium commodi neque, et consequuntur eos, consectetur voluptas exercitationem reiciendis voluptatem dicta vel adipisci. Dolorem rem architecto ducimus suscipit?
            </p>
          </div>
        </div>
      </div>
    </section>
     -->

    <!-- <div
      class="columns mt-5"
    >
      <div class="column mt-5">
        <figure class="image is-16by9">
          <img
            class="has-ratio"
            src="../assets/bg.png"
          ></img>
        </figure>
      </div>
    </div> -->
  </section>
  </div>
</template>

<style lang="css">
.has-bg-img {
  background: url('https://rentalbee.ph/images/hero_banner.webp');
}
</style>


<script>
export default {
  data() {
    return {
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
          color: 'success',
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
          color: 'success',
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
<style>
section .headline {
  background: url('~/assets/bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
}
</style>