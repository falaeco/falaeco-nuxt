<template>
  <client-only>
    <swiper ref="projectSwiper" v-observe-visibility="visibilityChanged" class="swiper c-swiper" :options="swiperOptions">
      <!-- insert project swiper slides here -->
      <slot />
      <div slot="scrollbar" class="swiper-scrollbar" />
    </swiper>
  </client-only>
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
        allowTouchMove: false,
        breakpoints: {
          768: {
            allowTouchMove: true
          }
        },
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
        window.innerWidth <= 768 ? 'vertical' : 'horizontal'
      )
    }
  }
}
</script>

<style scoped>

</style>

<style>
.c-swiper{
  height: inherit;
}

.c-swiper .c-slide {
  width: auto;
  height: auto;
}

.c-swiper .swiper-scrollbar {
  visibility: hidden;
}

@media (min-width: 768px){
  /** TODO: add space for the scroll bar maybe */
  .c-swiper .c-slide {
    height: 100%;
  }

  .c-swiper .swiper-scrollbar{
    visibility: visible;
  }
}
</style>
