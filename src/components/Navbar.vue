<template>
  <nav>
    <div class="nav-wrapper white lighten-2">
      <a href="#" class="brand-logo center brown-text">
        <slot name="logo" />
      </a>
      <a href="#" data-target="mobile-sidenav" class="sidenav-trigger">
        <slot name="sidenav-trigger" />
      </a>
      <ul id="nav-mobile" class="left hide-on-med-and-down">
        <slot name="secondary-menu" />
      </ul>
      <ul id="nav-mobile" class="right hide-on-med-and-down">
        <slot name="primary-menu" />
      </ul>
    </div>
    <ul class="sidenav" id="mobile-sidenav">
      <slot name="sidenav" />
    </ul>
  </nav>
</template>

<script>
import { onMounted } from "vue";

export default {
  setup() {
    onMounted(() => {
      var sidenav = document.querySelectorAll('.sidenav');
      M.Sidenav.init(sidenav, {});
    })
  }
}
</script>

