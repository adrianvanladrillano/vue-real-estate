<template>
  <div>
    <b-carousel>
      <b-carousel-item v-for="(carousel, i) in carousels" :key="i">
        <img :src="carousel.img" alt="" style="width: 100%; height: 92vh" />
      </b-carousel-item>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carousels: [
        {
          text: 'Slide 1',
          color: 'primary',
          img: 'https://wallpaperaccess.com/full/259894.jpg',
        },
        {
          text: 'Slide 1',
          color: 'primary',
          img:
            'https://icms-image.slatic.net/images/ims-web/8355ffd1-4400-4532-b170-d2921f59b6c3.jpg',
        },
        {
          text: 'Slide 1',
          color: 'primary',
          img: 'https://wallpaperaccess.com/full/259894.jpg',
        },
        {
          text: 'Slide 1',
          color: 'primary',
          img:
            'https://icms-image.slatic.net/images/ims-web/8355ffd1-4400-4532-b170-d2921f59b6c3.jpg',
        },
        {
          text: 'Slide 1',
          color: 'primary',
          img:
            'https://icms-image.slatic.net/images/ims-web/8355ffd1-4400-4532-b170-d2921f59b6c3.jpg',
        },
      ],
    }
  },
}
</script>
