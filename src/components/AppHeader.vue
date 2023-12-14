<template lang="">
  <header>
    <div>
      <img src="../assets/img/dc-logo.png" alt="DC logo">
    </div>
    <nav>
      <ul>
        <li>prova</li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      navLinks: [{}]
    }
  },
}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

</style>