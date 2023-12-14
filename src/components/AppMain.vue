<template lang="">
  <main>
    <section>
      &RightArrow; Content goes here &LeftArrow;  
    </section>
  </main>
</template>

<script>
export default {
  name: 'AppMain',
  data() {
    return {

    }
  },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

main {
  color: $white;
  background-color: $main-bg;
  padding: 5rem 0;

  section {
    width: $base-width;
    margin: 0 auto;
    font-size: 2rem;
    font-weight: 600;
  }
}
</style>