<template>
  <swiper ref="mySwiper" v-observe-visibility="visibilityChanged" class="swiper" :options="swiperOptions">
    <swiper-slide class="bg-gray-200">
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure expedita aspernatur nulla sunt provident. Corrupti fugiat atque sit inventore dignissimos nesciunt aperiam? Facilis, quidem. Minima, voluptatibus quis? Odit, impedit reprehenderit.</p>
    </swiper-slide>
    <swiper-slide class="bg-gray-400">
      Slide 2
    </swiper-slide>
    <swiper-slide class="bg-gray-200">
      Slide 3
    </swiper-slide>
    <div slot="scrollbar" class="swiper-scrollbar" />
  </swiper>
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
