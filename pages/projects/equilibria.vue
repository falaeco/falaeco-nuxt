<template>
  <div>
    <div class="bg-gray-200 four-three-container">
      <div class="p-4">
        <h1 class="text-lg">
          Image
        </h1>
      </div>
    </div>
    <div class="bg-gray-400 four-three-container">
      <div>
        <h1 class="text-lg">
          Equilibria
        </h1>
        <p class="text-sm">
          {{ first_text_slide }}
        </p>
      </div>
    </div>
    <div class="bg-gray-200 four-three-container">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide>
          <p class="text-sm">{{ first_text_slide }}</p>
        </swiper-slide>
        <swiper-slide>
          <p class="text-sm">{{ second_text_slide }}</p>
        </swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <div slot="button-prev" class="swiper-button-prev" />
        <!-- <div slot="button-next" class="swiper-button-next" /> -->
      </swiper>
    </div>
    <!-- Buttons -->
    <div>
      <button class="my-button-next p-2 border border-solid border-red-600 bg-black hover:bg-white text-white hover:text-black">
        <i class="icon-right-dir" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      first_text_slide: 'Equilibria is a dialogue between an ecosystem in peril and the viewer. As visitors interact with an interactive sculpture, they are forced to confront the reality that their consumption ultimately leads to the system’s destruction. This realization prompts viewers to consider how best to conserve the experience for future visitors, who serve as a proxy for future generations. Equilibria invites viewers to think about their place within the global ecosystem and hopes to develop an awareness of their own finite reality',
      second_text_slide: 'For this project, I was tasked to design and build the central structure, and program our interactive branches via Arduino and UDP protocol. In addition, I worked actively with my team on the design of the forest and how we would kill section of the forest when visitors would stay too long in one part of the installation. With the help of my teammates Emily and Audrey, we went on the top of the Mount Royal to get some footage for the installation',
      swiperOption: {
        navigation: {
          nextEl: '.my-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  }
}
</script>

<style>

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

</style>
