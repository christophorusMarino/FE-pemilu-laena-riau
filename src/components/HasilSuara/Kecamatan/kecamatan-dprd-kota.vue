<template>
  <div>
    <v-card flat v-if="kec"></v-card>
  </div>
</template>

<script>
export default {
  props: ["kec", "hasilSuara", "kabupaten", "kecamatan"],
};
</script>