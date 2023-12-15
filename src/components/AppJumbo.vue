<template>
  <section>
    <img src="../assets/img/jumbotron.jpg" alt="jumbo">
  </section>
</template>
<script>
export default {
  name:'AppJumbo'
}
</script>
<style lang="scss" scoped>
  section{
    height: 300px;
    overflow: hidden;
    img{
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position:top;
    }
  }
</style>