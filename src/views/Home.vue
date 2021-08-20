<template>
  <div id="home">
    <b-row class="m-0"
      ><b-col cols="12" class="m-2">
        <b-button block pill variant="success">success</b-button></b-col
      ><b-col cols="12" class="m-2">
        <b-button block pill variant="info">info</b-button></b-col
      ><b-col cols="12" class="m-2">
        <b-button block pill variant="danger">danger</b-button></b-col
      ></b-row
    >
  </div>
</template>

<script>

export default {
  name: "Home",
  components: {},
  beforeCreate() {
    this.$liff.init({ liffId: "home" });
    if (!this.$liff.isLoggedIn()) {
      this.$liff.login({ redirectUri: "https://example.com/path1/path2/" });
    }
  },
  mounted() {
    this.startline();
  },
  methods: {
    async startline() {
      // if (!liff.isLoggedIn()) {
      //   liff.login({ redirectUri: "https://example.com/path1/path2/" });
      // }
    },
  },
};
</script>
