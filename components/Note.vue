<template>
  <div class="container">
    <div class="row align-items-center mt-3">
      <div class="col">
        <div class="card text-center bg-light mb-3" style="width: 18rem">
          <div class="card-body">
            <h5 class="card-title">Title ID: {{ id }}</h5>
            <p class="card-text font-weight-bold">{{ title }}</p>
            <nuxt-link class="btn btn-primary" :to="'/notes/' + id">
              Read more...
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: `Notes`,
    };
  },
  name: "Note",
  props: ["id", "title"],
};
</script>

