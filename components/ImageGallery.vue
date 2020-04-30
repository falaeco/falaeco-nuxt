<template>
  <div>
    <swiper class="swiper" :options="imageSwiperOptions">
      <!-- insert swiper image slides here --->
      <slot />
    </swiper>
    <div class="gallery-navigation inline-flex absolute bottom-0 left-0">
      <m-button class="image-swiper-next">
        <i class="icon-left-dir" />
      </m-button>
      <div class="image-swiper-fract" />
      <m-button class="image-swiper-prev">
        <i class="icon-right-dir" />
      </m-button>
    </div>
  </div>
</template>

<script>
import MButton from '@/components/MButton'

export default {
  name: 'ImageGallery',
  components: {
    MButton
  },
  data () {
    return {
      imageSwiperOptions: {
        navigation: {
          nextEl: '.image-swiper-next',
          prevEl: '.image-swiper-prev'
        }
      }
    }
  }
}
</script>

<style>

</style>
