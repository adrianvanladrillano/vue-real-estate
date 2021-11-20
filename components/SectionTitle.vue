<template>
  <div>
    <section class="section" style="background: none">
      <h1 class="title" style="font-weight: 700; color: #2d3161">
        {{ title }}
      </h1>

      <h2 class="subtitle" style="color: #feaf11; font-weight: 500">
        {{ subtitle }}
      </h2>
    </section>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
}
</script>

<style>
</style>