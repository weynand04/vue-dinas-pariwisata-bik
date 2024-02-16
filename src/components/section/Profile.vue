<template>
  <!-- start section profile -->
  <div class="container py-3 my-3">
    <div class="row mb-5">
      <div class="col-12 text-center text-dark">
        <h1>PROFILE</h1>
        <p>Tentang Dinas Pariwisata Kabupaten Biak Numfor</p>
        <hr class="featurette-divider" />
      </div>
    </div>
    <div class="row">
      <div v-for="(item, index) in items" :key="index" class="col-lg-3 py-2 text-center text-dark">
        <div class="card d-flex flex-column h-100">
          <div class="card-header">
            <img :src="'src' + item.img" height="150" width="150" class="bd-placeholder-img rounded-circle py-1"
              alt="...">
            <h5>{{ item.heading }}</h5>
          </div>
          <div class="card-body">
            <p>{{ truncateContent(item.content) }}</p>
          </div>
          <p><a class="btn btn-secondary" :href="item.detailsLink">View details &raquo;</a></p>
        </div>
      </div>
    </div>
  </div>
  <!-- end section profile  -->
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          heading: "Sejarah Singkat",
          content: "Pada tahun 1526 Gubernur Portugis untuk Ternate Jorge de Menezes berangkat dari Malaka menuju Ternate. Disebabkan badai, kapalnya terdampar di Warsa Biak Utara. Selama 6 bulan ia tinggal di Warsa (Desember 1526 sampai Mei 1527) menunggu cuaca yang baik dan di bulan Mei 1527 ia berangkat meninggalkan Biak serta tiba di Ternate pada tanggal 31 Mei 1527",
          detailsLink: "#",
          img: '/assets/img/sejarahbiak.png',
        },
        {
          heading: "Struktur Organisasi",
          content: "Another exciting bit of representative placeholder content. This time, we've moved on to the second column.",
          detailsLink: "#",
          img: '/assets/img/648418b43d3df.jpg',
        },
        {
          heading: "Tugas Pokok dan Fungsi",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/wari-beach.jpg',
        },
        {
          heading: "Program dan Kegiatan",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/648418b43d3df.jpg',
        },
        {
          heading: "Data Pemimpin",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/Destinasi-Wisata-Biak-Numfor-Air-Terjun-Wafsarak.webp',
        },
        {
          heading: "New Data Pemimpin",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/Destinasi-Wisata-Biak-Numfor-Air-Terjun-Wafsarak.webp',
        },
        {
          heading: "Data Pegawai",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/pulau-auki.png',
        },
        {
          heading: " New Data Pegawai",
          content: "And lastly this, the third column of representative placeholder content.",
          detailsLink: "#",
          img: '/assets/img/pulau-auki.png',
        }
      ]
    };
  },
  methods: {
    truncateContent(content) {
      const words = content.split(' ');
      const truncatedContent = words.slice(0, 20).join(' ');
      return truncatedContent + (words.length > 20 ? '...' : '');
    }
  }
}
</script>