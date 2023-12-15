<template lang="">
  <main>
    <div class="wrapper">
      <div class="section-title">
        current series
      </div>
      <AppCurrent/>
    </div>
  </main>
  <AppBanner/>
</template>

<script>
import AppBanner from './AppBanner.vue';
import AppCurrent from './AppCurrent.vue';

export default {
  name: 'AppMain',
  data() {
    return {

    }
  },
  components:{
    AppBanner,
    AppCurrent
  }
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {
  color: $white;
  background-color: $main-bg;
  
  .wrapper {
    width: $base-width;
    position: relative;
    padding: 5rem 0;
    margin: 0 auto;
    font-size: 1.5rem;
    font-weight: 600;
    .section-title{
      position: absolute;
      text-transform: uppercase;
      background-color: $accent-color;
      top: -20px;
      left: 0;
      padding: .25rem 1rem;
    }
    
  }
}
</style>