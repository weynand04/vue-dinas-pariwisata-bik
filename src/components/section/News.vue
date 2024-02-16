<template>
  <!-- start section news -->
  <div class="container marketing py-3 my-3">
    <div class="row mb-5">
      <div class="col-12 text-start text-dark">
        <h1>NEWS</h1>
        <p>Kabar seputar Pariwisata di Kabupaten Biak Numfor</p>
        <hr class="featurette-divider" />
      </div>
    </div>
    <div class="row">
      <div class="album py-2">
        <div class="container">
          <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4 g-3">
            <div v-for="(card, index) in cards" :key="index" class="col">
              <div class="card d-flex flex-column h-100 shadow-sm text-dark">
                <img style="width: 350px; height: 290px" :src="'src' + card.img" class="img-thumbnail"
                  alt="Gallery Image 4" />
                <div class="card-body">
                  <h6 class="card-title">{{ card.title }}</h6>
                  <p class="card-text text-dark">{{ card.description }}</p>
                  <div class="d-flex justify-content-between align-items-center">
                    <small class="text-muted">{{ card.date }}</small>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- end section news  -->
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          title: "Sail Teluk Cendrawasi 2023 Biak Papua",
          description: " Sail Teluk Cenderawasih 2023 Jadi Momentum Promosi Potensi Wisata Bahari Papua.",
          date: "12 Desember 2023",
          img: '/assets/img/sail teluk cendrawasi.jpeg'
        },
        {
          title: "Kapal Mewah The World Singgah di Pelabuhan Biak",
          description: "The World, kapal pesiar mewah singgah di pelabuhan Biak membawa wisatawan mancanegara untuk melakukan kunjungan wisata ke destinasi wisata yang ada di Biak.",
          date: "17 Januari 2022",
          img: '/assets/img/kapal pasiar.jpg'
        },
        {
          title: "Wisata Biak",
          description: "Ada banyak tempat wisata yang bisa didatangi selama berlibur ke Kabupaten Biak Numfor, Papua..",
          date: "12 November 2023",
          img: '/assets/img/pulau-auki.png'

        },
        {
          title: "Festival Biak Munara Wamapasi ",
          description: "BIAK Kalau kalian penasaran dengan budaya asli orang Papua, maka berkunjunglah ke Biak, Papua, 21-24 Agustus mendatang. Karena, saat itu bakal digelar Festival Budaya Biak Munara Wampasi (BMW)..",
          date: "12 Desember 2020",
          img: '/assets/img/coba.jpg'
        },
      ],
    };
  },
};
</script>