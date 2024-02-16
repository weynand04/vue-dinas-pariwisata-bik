<template>
  <!-- start navbar -->
  <div class="container">
    <a class="navbar-brand" href="#">
      <img src="@/assets/img/logo.png" alt="" width="49" height="61" />
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown"
      aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse justify-content-md-end" id="navbarNavDropdown">
      <ul class="navbar-nav">
        <li v-for="item in navItems" :key="item.id" class="nav-item">
          <a :class="['nav-link', { active: item.isActive }]" :href="item.link">{{ item.label }}</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-toggle="dropdown"
            aria-expanded="false">
            Layanan
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
            <li v-for="layanan in layananItems" :key="layanan.id">
              <a class="dropdown-item" :href="layanan.link">{{ layanan.label }}</a>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
  <!-- end navbar  -->
</template>

<script>
export default {
  data() {
    return {
      navItems: [
        { id: 1, label: 'Home', link: '#', isActive: true },
        { id: 2, label: 'Profile', link: '#profile' },
        { id: 3, label: 'News', link: '#news' },
        { id: 4, label: 'Gallery', link: '#galery' }
      ],
      layananItems: [
        { id: 1, label: 'Layanan 1', link: '#' },
        { id: 2, label: 'Layanan 2', link: '#' }
      ]
    };
  }
};
</script>