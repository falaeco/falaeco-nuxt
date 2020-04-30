<template>
  <project-content-slider>
    <swiper-slide class="c-slide">
      <div class="max-w-xs text-container">
        <h1 class="title">
          Ruinism
        </h1>
        <h2 class="subtitle mb-2">
          January 2019
        </h2>
        <p class="text-light">
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
      <div>
        <img src="~/assets/img/projects/ruinism/ruin-front.png">
      </div>
    </swiper-slide>
    <swiper-slide class="c-slide bg-gray-200">
      Slide 3
    </swiper-slide>
    <!-- dont close my tag-->
  </project-content-slider>
</template>

<script>
import ProjectContentSlider from '@/components/ProjectContent'

export default {
  components: {
    ProjectContentSlider
  }
}
</script>

<style scoped>
.title{
  font-family: acumin-pro-condensed, sans-serif;
  font-weight: 700;
  font-style: normal;
  text-transform: uppercase;
  font-size: 1.5rem;
}
.subtitle{
  font-family: acumin-pro-condensed, sans-serif;
  font-weight: 600;
  font-style: normal;
}
.text{
  font-family: acumin-pro, sans-serif;
  font-weight: 400;
  font-style: normal;
}
.text-light {
  font-family: acumin-pro, sans-serif;
  font-weight: 300;
  font-style: normal;
}
.title, .subtitle, .text, .text-light{
  color: #ffffff
}
.text-container{
  padding: 1rem;
  background-color: #181616;
}
.text-container p{
  margin-bottom: 0.25rem;
}
</style>
