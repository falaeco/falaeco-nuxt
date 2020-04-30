<template>
  <swiper ref="projectSwiper" v-observe-visibility="visibilityChanged" class="swiper" :options="swiperOptions">
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
      console.log('isVisible ' + isVisible)
      this.updateSwiperDirection()
    },
    updateSwiperDirection () {
      console.log('Call from change direction')
      this.$refs.projectSwiper.$swiper.changeDirection(
        window.innerWidth <= 640 ? 'vertical' : 'horizontal'
      )
    }
  }
}
</script>
