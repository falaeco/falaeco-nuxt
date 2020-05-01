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
      <image-gallery id="concepts" :img-src="gallery.urlzero" />
    </swiper-slide>
    <swiper-slide>
      <image-gallery id="explo" :img-src="gallery.urltwo" />
    </swiper-slide>
    <swiper-slide>
      <image-gallery id="final" :img-src="gallery.urlthree" />
    </swiper-slide>
  </project-content-slider>
</template>

<script>
import ProjectContentSlider from '@/components/ProjectContent'
import ImageGallery from '@/components/ImageGallery'
export default {
  components: {
    ProjectContentSlider, ImageGallery
  },
  data () {
    return {
      gallery: {
        urlzero: [
          'ruinism/ruin-concept1.jpg',
          'ruinism/ruin-concept2.jpg',
          'ruinism/ruin-concept3.jpg'
        ],
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

.text-container{
  padding: 1rem;
  background-color: #181616;
  color:#302e2e;
}
.text-container p{
  margin-bottom: 0.25rem;
}
</style>
