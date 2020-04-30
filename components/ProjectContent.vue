<template>
  <swiper ref="projectSwiper" v-observe-visibility="visibilityChanged" class="swiper c-swiper" :options="swiperOptions">
    <!-- insert project swiper slides here -->
    <slot />
    <div slot="scrollbar" class="swiper-scrollbar" />
  </swiper>
</template>

<script>
export default {
  name: 'ProjectContentSlider',
  data () {
    return {
      swiperOptions: {
        direction: 'horizontal',
        slidesPerView: 'auto',
        freeMode: true,
        scrollbar: {
          el: '.swiper-scrollbar'
        },
        mousewheel: true,
        on: {
          resize: () => {
            this.updateSwiperDirection()
          }
        }
      }
    }
  },
  methods: {
    visibilityChanged (isVisible, entry) {
      this.isVisible = isVisible
      this.updateSwiperDirection()
    },
    updateSwiperDirection () {
      this.$refs.projectSwiper.$swiper.changeDirection(
        window.innerWidth <= 640 ? 'vertical' : 'horizontal'
      )
    }
  }
}
</script>

<style scoped>

</style>

<style>
.c-swiper .c-slide {
  width: auto;
}
</style>
