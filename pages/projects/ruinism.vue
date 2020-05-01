<template>
  <project-content-slider>
    <swiper-slide class="c-slide">
      <div class="h-auto md:h-full">
        <img src="~/assets/img/ruinism/ruin-front.png" class="h-auto">
      </div>
    </swiper-slide>
    <swiper-slide class="c-slide">
      <div class="text-container md:max-w-sm">
        <div class="mb-4">
          <h1 class="title uppercase text-5xl">
            Ruinism
          </h1>
          <h2 class="subtitle">
            January 2019
          </h2>
        </div>
        <p class="text">
          Stuart Howard's third album <em>Ruinism</em> certainly didn't go unnoticed. Considered by most as an affirmation
          of his musical career, Lapalux's compositions veer off into the abstract, somewhere between a classical and
          post-electro mindset. Prominently featuring women collaborator, the record can feels as much cold and dystopic
          as sensitive and humane.
        </p>
        <p class="text">
          For this project I was tasked to redesign the vinyl sleeve of this album. Applying the iterative design
          methodology, I meticulously explored various concepts and refined my ideas to create a strong design for the
          sleeve. The final piece is a portrait of my listening experience of the album. The colour palette is evocative
          of the strong feminine contribution to the album, while the shape and texture is a depiction of the abstract
          quality of Howard's composition.
        </p>
      </div>
    </swiper-slide>
    <swiper-slide class="c-slide bg-gray-400">
      <div class="concept">
        <swiper class="swiper image-swiper" :options="gallerySwiperOptions">
          <swiper-slide class="image-slide">
            <img src="~/assets/img/ruinism/ruin-concept1.jpg">
          </swiper-slide>
          <swiper-slide class="image-slide">
            <img src="~/assets/img/ruinism/ruin-concept2.jpg">
          </swiper-slide>
          <swiper-slide class="image-slide">
            <img src="~/assets/img/ruinism/ruin-concept3.jpg">
          </swiper-slide>
        </swiper>
        <div class="inline-flex absolute bottom-0 left-0 z-10">
          <m-button class="image-swiper-prev">
            <i class="icon-left-dir" />
          </m-button>
          <div class="image-swiper-fract btn-colour-theme px-4 flex-none font-acuminXcondensed tracking-wide" style="line-height: 45px">
            Fract
          </div>
          <m-button class="image-swiper-next">
            <i class="icon-right-dir" />
          </m-button>
          <div class="font-acuminXcondensed">
            <p>First Iteration: Early Sketches of concepts</p>
          </div>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <!--dc-->
      <image-gallery id="explo" :img-src="gallery.urltwo" />
    </swiper-slide>
    <swiper-slide>
      <image-gallery id="final" :img-src="gallery.urlthree" />
    </swiper-slide>
  </project-content-slider>
</template>

<script>
import ProjectContentSlider from '@/components/ProjectContent'
import MButton from '@/components/MButton'
import ImageGallery from '@/components/ImageGallery'
export default {
  components: {
    ProjectContentSlider, MButton, ImageGallery
  },
  data () {
    return {
      gallery: {
        urltwo: [
          'ruinism/ruin-explo1.png',
          'ruinism/ruin-explo2.png',
          'ruinism/ruin-explo3.png',
          'ruinism/ruin-explo4.png'
        ],
        urlthree: [
          'ruinism/ruin-anacover-back.jpg',
          'ruinism/ruin-anacover-front.jpg'
        ]
      },
      gallerySwiperOptions: {
        pagination: {
          el: '.image-swiper-fract',
          type: 'fraction'
        },
        navigation: {
          nextEl: '.image-swiper-next',
          prevEl: '.image-swiper-prev'
        }
      }
    }
  }
}
</script>

<style scoped>
.image-swiper-fract.swiper-pagination-fraction{
  width: auto;
}

.image-slide img{
  width: auto;
}

.title{
  font-family: acumin-pro-condensed, sans-serif;
  font-weight: 700;
  font-style: normal;
  letter-spacing: 0.06rem;
  color: #f7f3f3;
  line-height: 1;
}
.subtitle{
  font-family: acumin-pro-condensed, sans-serif;
  font-weight: 400;
  font-style: normal;
  color: #c4c2c2;
  letter-spacing: 0.05rem;
}
.text{
  font-family: acumin-pro, sans-serif;
  font-weight: 400;
  font-style: normal;
  color: #dcdada
}

.text-container{
  padding: 1rem;
  background-color: #181616;
  color:#302e2e;
}
.text-container p{
  margin-bottom: 0.25rem;
}
</style>
