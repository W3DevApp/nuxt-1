<template>
  <div>
    <Navigation />
    <div>
      <nuxt />
    </div>
  </div>
</template>

<script>
import Navigation from "../components/Navigation";

export default {
  components: {
    Navigation,
  },
};
</script>