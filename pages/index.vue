<template>
  <div class="container-fluid">
    <h1>Welcome NUXT-1</h1>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "content",
        },
      ],
      htmlAttrs: {
        lang: "en",
      },
    };
  },
};
</script>
