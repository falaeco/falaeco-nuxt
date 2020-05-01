<template>
  <div>
    <p>Machine to hang with birds</p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isVisible: true,
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
            this.$refs.mySwiper.$swiper.changeDirection(
              window.innerWidth <= 640
                ? 'vertical'
                : 'horizontal'
            )
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
      this.$refs.mySwiper.$swiper.changeDirection(
        window.innerWidth <= 640
          ? 'vertical'
          : 'horizontal'
      )
    }
  }
}
</script>

<style scoped>

</style>
