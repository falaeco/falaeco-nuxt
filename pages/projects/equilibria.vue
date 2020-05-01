<template>
  <div>
    <div class="bg-gray-200">
      <swiper class="swiper">
        <swiper-slide><img src="~/assets/img/equilibria/eq-ball.jpg"></swiper-slide>
        <swiper-slide><img src="~/assets/img/equilibria/eq-fullview.jpg"></swiper-slide>
        <swiper-slide><img src="~/assets/img/equilibria/eq-light.jpg"></swiper-slide>
        <swiper-slide><img src="~/assets/img/equilibria/eq-structure.jpg"></swiper-slide>
      </swiper>
    </div>
    <div class="bg-gray-200">
      <div class="p-2">
        <div class="mb-2">
          <h1>Equilibria</h1>
          <h2>December 2019</h2>
        </div>
        <swiper class="swiper" :options="swiperOption">
          <swiper-slide>
            <p class="text-sm">
              {{ first_text_slide }}
            </p>
          </swiper-slide>
          <swiper-slide>
            <p class="text-sm">
              {{ second_text_slide }}
            </p>
          </swiper-slide>
        <!-- <div slot="pagination" class="swiper-pagination" /> -->
        <!-- <div slot="button-prev" class="swiper-button-prev" /> -->
        <!-- <div slot="button-next" class="swiper-button-next" /> -->
        </swiper>
        <div class="inline-flex absolute bottom-0 left-0">
          <m-button class="text-swiper-prev">
            <i class="icon-left-dir" />
          </m-button>
          <div class="text-swiper-fract btn-colour-theme px-2 leading-loose">
            Fract
          </div>
          <m-button class="text-swiper-next">
            <i class="icon-right-dir" />
          </m-button>
        </div>
      </div>
    </div>
    <youtube video-id="UwcoFXKnpOw" class="youtube-wrapper" />
  </div>
</template>

<script>
import MButton from '@/components/MButton'

export default {
  components: {
    MButton
  },
  data () {
    return {
      first_text_slide: 'Equilibria is a dialogue between an ecosystem in peril and the viewer. As visitors interact with an interactive sculpture, they are forced to confront the reality that their consumption ultimately leads to the system’s destruction. This realization prompts viewers to consider how best to conserve the experience for future visitors, who serve as a proxy for future generations. Equilibria invites viewers to think about their place within the global ecosystem and hopes to develop an awareness of their own finite reality',
      second_text_slide: 'For this project, I was tasked to design and build the central structure, and program our interactive branches via Arduino and UDP protocol. In addition, I worked actively with my team on the design of the forest and how we would kill section of the forest when visitors would stay too long in one part of the installation. With the help of my teammates Emily and Audrey, we went on the top of the Mount Royal to get some footage for the installation',
      swiperOption: {
        navigation: {
          nextEl: '.text-swiper-next',
          prevEl: '.text-swiper-prev'
        },
        pagination: {
          el: '.text-swiper-fract',
          type: 'fraction'
        }
      }
    }
  }
}
</script>

<style>
.img-gallery {
  transform: translateY(-50%);
  top: 50%;
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
}

.four-three-container{
  position: relative;
  /* width: 100%;
  padding-top: 75%; */
}

.four-three-container::before {
  display: block;
  content: "";
  width: 100%;
  padding-top: 75%;
}

.four-three-container > :first-child{
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}

.youtube-wrapper {
  position: relative;
  padding-bottom: 56.25%;
  height: 0;
}

.youtube-wrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
