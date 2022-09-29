<template>
  <div class="TheHero">
    <HeroLogo />
    <HeroImage />
  </div>
</template>

<script>
export default {
  name: 'TheHero'
}
</script>

<style lang="postcss" scoped>
  .TheHero {
    height: calc(100vh - var(--spacing-md));
    display: flex;

    & > * {
      flex: 1;
    }

    @media (--laptop) {
      flex-direction: row;
    }
  }
</style>
