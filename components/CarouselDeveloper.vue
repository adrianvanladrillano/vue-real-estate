<template>
  <div>
    <div class="columns">
      <div
        class="column"
        style="
          padding-left: 8vw;
          padding-right: 8vw;
          height: ;
          background: white;
        "
      >
        <b-carousel-list
          v-model="test"
          :data="developers"
          :items-to-show="7"
          class="px-5 is-shadowless"
        >
          <template #item="developers">
            <div class="px-5 py-5">
              <img
                :src="developers.developer_logo"
                alt=""
                style="width: 100%; filter: grayscale(100%); height: 70px"
              />
            </div>
          </template>
        </b-carousel-list>
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
      developers: [],
      items: [
        {
          title: 'Slide 1',
          image:
            'https://5.imimg.com/data5/WJ/PR/HS/SELLER-81339524/freeshipping-ice-bingo-i12-earphone-hands-free-png-500x500-500x500.png',
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
      .get('http://localhost:6969/developers')
      .then(function (response) {
        // handle success
        // console.log(response.data)
        self.developers = response.data
        console.log(self.developers)
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
