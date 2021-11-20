<template>
  <div>
    <Navbar />
    <section class="main-content">
      <div
        class="container-fluid"
        style="padding-left: 8vw; padding-right: 8vw;background: #FFF"
      >
        <nuxt />
      </div>
    </section>

    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          title: 'Home',
          icon: 'home',
          to: { name: 'index' },
        },
        {
          title: 'Inspire',
          icon: 'lightbulb',
          to: { name: 'inspire' },
        },
      ],
    }
  },
}
</script>

<style>
.is-primary {
  color: #2d3161;
  background-color: #2d3161;
}
</style>