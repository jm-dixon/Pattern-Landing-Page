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
@import "~/assets/css/settings/media-queries.css";

.TheHero {
  height: calc(100vh - var(--spacing-md));
  display: flex;
  flex-direction: column;

  & > * {
    flex: 1;
  }

  @media (--tablet) {
    flex-direction: row;
  }
}
</style>
