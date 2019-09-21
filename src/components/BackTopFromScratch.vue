<template>
    <div class="btn-container" v-if="isVisible" @click="scrollTop">
      <i class="fa fa-angle-up fa-2x"></i>
      </div>
</template>

<script>
export default {
  data() {
    return {
      isVisible: ''
    };
  },
  methods: {
    scrollTop() {
      return window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
    scrollHandler () {
       this.isVisible = false;
      if (window.pageYOffset >= 600) {
        this.isVisible = true;
      }
    }
  },
  created() {
    window.addEventListener("scroll", this.scrollHandler);
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.scrollHandler);
  }
};
</script>

<style lang="scss" scoped>
.fa-2x {
    font-size: 3em;
    margin-top: -3px;
}
.btn-container {
  width: 50px;
  position: fixed;
    height: 50px;
    right: 50px;
  bottom: calc(50px);
    z-index: 1000;
    color: rgb(255, 255, 255);
    background-color: rgb(144, 180, 46);
        box-shadow: rgba(0, 0, 0, 0.3) 1px 1px 2px;
    border-radius: 50px;
}
</style>