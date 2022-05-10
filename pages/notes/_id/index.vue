<template>
  <div class="container">
    <div class="row align-items-center mt-3">
      <div class="col">
        <div class="card text-center bg-light mb-3" style="width: 18rem">
          <div class="card-body">
            <h5 class="card-title">
              <span class="font-weight-bold">Title: </span> {{ note.title }}
            </h5>
            <p class="card-text">
              <span class="font-weight-bold">Content: </span> {{ note.content }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  head() {
    return {
      title: `Show Note with ID: ${this.$route.params.id}`,
    };
  },
  data() {
    return {
      note: {},
    };
  },
  async created() {
    const res = await axios.get(
      "http://your_backend_host:your_backend_port/" + this.$route.params.id
    );
    this.note = res.data;
  },
};
</script>

