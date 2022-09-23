<template>
  <div class="HeroLogo">
    <div class="HeroLogo__logo-wrapper">
      <img :src="logoUrl" class="HeroLogo__logo-img">
      <h3 class="HeroLogo__coming-soon">Coming Soon</h3>
    </div>
    <div class="HeroLogo__texture-img">
      <img
        src="images/texture.jpg"
        srcset="images/texture-horiz.jpg 1080w, images/texture.jpg 197w"
        sizes="(max-width: 767px) 1080px, 197px"
      >
    </div>
  </div>
</template>

<script>
import PatternShopLogoUrl from '@/assets/images/pattern-shop-logo-01.svg';

export default {
  name: 'HeroLogo',

  data() {
    return {
      logoUrl: PatternShopLogoUrl,
    };
  },

  computed: {
    isDesktopLg() {
      return this.$store.state.isDesktopLg;
    },
  },

  watch: {
    isDesktopLg: {
      handler(newVal) {
        this.textureImgUrl = newVal ? this.textureUrl : this.textureHorizUrl;
      },
      immediate: true,
    },
  },
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";
@import "~/assets/css/mixins/media.css";

.HeroLogo {
  display: flex;
  flex-direction: column;
  background-color: var(--color-black);
  color: white;

  @media (--laptop) {
    flex-direction: row;
  }
}

.HeroLogo__logo-wrapper {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  align-items: center;
  justify-content: center;
  row-gap: var(--spacing-md);

  @media (--laptop) {
    row-gap: var(--spacing-2xl);
  }

  @media (--desktop-xl) {
    row-gap: var(--spacing-4xl);
  }
}

.HeroLogo__logo-img {
  width: 11rem;

  /* @media (--phone-lg) {
    width: 20%;
  }

  @media (--tablet) {
    width: 20%;
  } */

  @media (--laptop) {
    width: 17.5rem;
  }

  @media (--desktop-xl) {
    width: 22.2rem;
  }
}

.HeroLogo__texture-img {
  @mixin media;
  @mixin media-full;

  width: 100%;
  height: 3.3rem !important;

  @media (--laptop) {
    height: 100% !important;
    width: 6rem;
  }

  @media (--desktop-xl) {
    width: 9rem;
  }

  /* @media (--desktop-lg) {
    width: 7%;
    height: 100%;
  } */
}

.HeroLogo__coming-soon {
  @mixin interpolate font-size, 2, 2.5;

  color: var(--color-lighter-orange);

  @media (--desktop-lg) {
    font-size: 3rem;
    margin-bottom: 0;
  }
}
</style>
