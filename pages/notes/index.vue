<template>
  <div class="container-fluid">
    <h1>Notes</h1>
    <Note
      v-for="note of notes"
      :key="note.id"
      :id="note.id"
      :title="note.title"
      :content="note.content"
    />
  </div>
</template>

<script>
import axios from "axios";
import Note from "../../components/Note";

export default {
  components: {
    Note,
  },
  data() {
    return {
      notes: [],
    };
  },
  async created() {
    const res = await axios.get("http://your_backend_host:your_backend_port");
    this.notes = res.data;
  },
};
</script>