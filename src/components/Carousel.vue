<template>
  <div class="q-pa-none" id="body">
    <q-carousel
      swipeable
      animated
      v-model="slide"
      thumbnails
      infinite
    >
      <q-carousel-slide class="carousel-slide" :name="1" :img-src="images.mountains" />
      <q-carousel-slide class="carousel-slide" :name="2" :img-src="images.parallax1" />
      <q-carousel-slide class="carousel-slide" :name="3" :img-src="images.parallax2" />
      <q-carousel-slide class="carousel-slide" :name="4" :img-src="images.quasar" />
      
    </q-carousel>

  </div>
</template>

<script>
import { ref } from 'vue'
import mountains from '../assets/10.jpg'
import parallax1 from '../assets/20.jpg'
import parallax2 from '../assets/30.jpg'
import quasar from '../assets/40.jpg'

export default {
  setup () {
    const images = {
      mountains,
      parallax1,
      parallax2,
      quasar
    }

    return {
      slide: ref(1),
      images
    }
  }
}
</script>

<style scoped>
#body {
  margin-top: 2%;
}

.carousel-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%; /* Atur tinggi slide agar gambar bisa diperbesar */
}

.carousel-slide img {
  width: 100%;
  height: auto;
  object-fit: cover; /* Menyesuaikan gambar agar tetap proporsional */
  
}

@media (max-width: 600px) {
  .carousel-slide img {
    height: auto; /* Biarkan gambar menyesuaikan tingginya secara otomatis */
  }
}
</style>
