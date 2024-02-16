<template>
  <!-- start section Layanan -->
  <div class="container layanan pt-5">
    <div class="text-center text-dark">
      <h1>LAYANAN</h1>
      <p>Layanan Khusus Dinas Pariwisata Kabupaten Biak Numfor</p>
      <hr class="featurette-divider" />
    </div>
    <div class="row row-cols-1 row-cols-md-3 mb-3 text-center text-dark">
      <div v-for="service in services" :key="service.id" class="col">
        <div class="card mb-4 rounded-3 shadow-sm">
          <div class="card-header py-3">
            <h4 class="my-0 fw-normal">{{ service.name }}</h4>
          </div>
          <div class="card-body">
            <h1 class="card-title pricing-card-title">
              {{ service.price }}<small class="text-muted fw-light">/mo</small>
            </h1>
            <ul class="list-unstyled mt-3 mb-4">
              <li v-for="feature in service.features" :key="feature">
                {{ feature }}
              </li>
            </ul>
            <button type="button" class="w-100 btn btn-lg" :class="service.buttonClass">
              {{ service.buttonText }}
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- end section Layanan -->
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          id: 1,
          name: 'Free',
          price: '$0',
          features: ['10 users included', '2 GB of storage', 'Email support', 'Help center access'],
          buttonClass: 'btn-outline-primary',
          buttonText: 'Sign up for free'
        },
        {
          id: 2,
          name: 'Pro',
          price: '$15',
          features: ['20 users included', '10 GB of storage', 'Priority email support', 'Help center access'],
          buttonClass: 'btn-primary',
          buttonText: 'Get started'
        },
        {
          id: 3,
          name: 'Enterprise',
          price: '$29',
          features: ['30 users included', '15 GB of storage', 'Phone and email support', 'Help center access'],
          buttonClass: 'btn-primary',
          buttonText: 'Contact us'
        }
      ]
    };
  }
};
</script>

