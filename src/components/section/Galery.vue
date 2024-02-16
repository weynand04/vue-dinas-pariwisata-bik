<template>
  <!-- start section Galery -->
  <div class="container galery">
    <div class="text-center text-dark">
      <h1>GALERY</h1>
      <p>Pesona Pariwisata di Kabupaten Biak Numfor</p>
      <hr class="featurette-divider" />
    </div>
    <div class="row">
      <div v-for="image in galleryImages" :key="image.id" class="col-4 pb-4">
        <img style="width: 350px; height: 290px" :src="'src' + image.src" class="img-fluid"
          :alt="'Gallery Image ' + image.id" />
      </div>
    </div>
  </div>
  <!-- end section Galery -->
</template>

<script>
export default {
  data() {
    return {
      galleryImages: [
        {
          id: 1,
          src: '/assets/img/canva.png'
        },
        {
          id: 2,
          src: '/assets/img/batupica.jpg'
        },
        {
          id: 3,
          src: '/assets/img/airterjun.webp'
        },
        {
          id: 4,
          src: '/assets/img/wari-beach.jpg'
        },
        {
          id: 5,
          src: '/assets/img/kalibiru.jpg'
        },
        {
          id: 5,
          src: '/assets/img/batupica.jpg'
        }
      ]
    };
  }
};
</script>