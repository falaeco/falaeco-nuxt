<template>
  <div>
    <client-only>
      <swiper class="swiper image-swiper" :options="gallerySwiperOptions">
        <swiper-slide v-for="(img, index) in imgSrc" :key="index" class="image-slide">
          <img :src="require(`~/assets/img/${img}`)">
        </swiper-slide>
      </swiper>
    </client-only>
    <div class="gal-navigation inline-flex absolute bottom-0 left-0 z-10">
      <m-button :class="id + 'image-swiper-prev gal-button gal-next'">
        <i class="icon-left-dir" />
      </m-button>
      <div :class="id + 'image-swiper-fract btn-colour-theme px-4 flex-none gal-fract font-acuminXcondensed'" />
      <m-button :class="id + 'image-swiper-next gal-button'">
        <i class="icon-right-dir" />
      </m-button>
      <div v-if="title" class="gallery-title">
        <p>{{ title }}</p>
      </div>
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
  props: {
    id: {
      type: String,
      required: true
    },
    imgSrc: {
      type: Array,
      default () {
        return ['https://picsum.photos/500', 'https://picsum.photos/200', 'https://picsum.photos/200']
      }
    },
    title: {
      type: String,
      default: ''
    }
  },
  data () {
    return {
      gallerySwiperOptions: {
        pagination: {
          el: '.' + this.id + 'image-swiper-fract',
          type: 'fraction'
        },
        navigation: {
          nextEl: '.' + this.id + 'image-swiper-next',
          prevEl: '.' + this.id + 'image-swiper-prev'
        }
      }
    }
  }
}
</script>

<style scoped>
.gal-next, .gal-fract {
  border-right: 1px solid #181616
}

.gal-navigation .swiper-pagination-fraction {
  width: auto;
}

.gal-fract {
  line-height: 45px;
  letter-spacing: 0.2rem;
}
</style>
