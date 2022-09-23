<template>
  <div class="HeroImage">
    <img :src="imageUrl" class="HeroImage__image">
  </div>
</template>

<script>
import heroImageUrl from '~/assets/images/hero-image.jpg';

export default {
  name: 'HeroImage',

  data() {
    return {
      imageUrl: heroImageUrl,
    };
  },
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";
@import "~/assets/css/mixins/media.css";

.HeroImage {
  @mixin media;
  @mixin media-full;

  /*
  @media (--desktop-lg) {
    height: 80rem;
    grid-column: 2 / 3;
    grid-row: 1 / 2;
  }
  */
}

/* .HeroImage__image {
  @mixin interpolate height, 45, 65;

  width: 100%;
  object-fit: cover;

  @media (--desktop-lg) {
    height: 80rem;
  }
} */
</style>
