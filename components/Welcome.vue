<template>
  <div class="Welcome">
    <h1 class="Welcome__heading">Welcome to<br />The Pattern Shop</h1>
    <p class="Welcome__text text-default">
      Reinvented for today’s innovators and located in the heart of the vibrant
      city of Newcastle adjacent to Central Station, this extraordinary building
      with its remarkable 200-year history, is the ideal base for businesses
      looking to make their mark.
    </p>
    <p class="Welcome__text text-default">
      The Pattern Shop brings industry leading digital connectivity and best in
      class sustainability technology, whilst retaining its soulful character,
      to offer you flexible office spaces between 1,108 sqft and 32,367 sqft,
      across 4 floors.
    </p>
    <p class="Welcome__text_subheading text-default">
      <a href="/pdf/the-pattern-shop-newcastle-brochure.pdf" download class="text-bold">
        <u> Download brochure here </u>
      </a>
    </p>
    <p class="Welcome__text_subheading text-default">
      If you’re intrigued to find out more, our team are on hand to discuss your
      requirements and are always happy to help.
    </p>
    <p class="Welcome__text_subheading text-bold">Patrick Matheson</p>
    <div class="Welcome__grid">
      <img :src="icons.phoneIconUrl" class="Welcome__icons" />
      <a href="tel:+441915925015">
        <p class="Welcome__text text-default">
          <u>0191 592 5015</u>
        </p>
      </a>
    </div>
    <div class="Welcome__grid">
      <img :src="icons.emailIconUrl" class="Welcome__icons email" />
      <a href="mailto:patrick.matheson@knightfrank.com">
        <p class="Welcome__text text-default">
          <u>patrick.matheson@knightfrank.com</u>
        </p>
      </a>
    </div>
    <p class="Welcome__text_subheading text-bold">Nathan Douglas</p>
    <div class="Welcome__grid">
      <img :src="icons.phoneIconUrl" class="Welcome__icons" />
      <a href="tel:+441915925002">
        <p class="Welcome__text text-default">
          <u>0191 592 5002</u>
        </p>
      </a>
    </div>
    <div class="Welcome__grid">
      <img :src="icons.emailIconUrl" class="Welcome__icons email" />
      <a href="mailto:nathan.douglas@knightfrank.com">
        <p class="Welcome__text text-default">
          <u>nathan.douglas@knightfrank.com</u>
        </p>
      </a>
    </div>
  </div>
</template>

<script>
import phoneIcon from '~/assets/images/THE PATTERNSHOP-Icon-Telephone-RGB.svg';
import emailIcon from '~/assets/images/THE PATTERNSHOP-Icon-Mail-RGB.svg';

export default {
  name: 'Welcome',
  data() {
    return {
      icons: {
        phoneIconUrl: phoneIcon,
        emailIconUrl: emailIcon
      }
    }
  }
}
</script>

<style lang="postcss">
@import "~/assets/css/settings/media-queries.css";
@import "~/assets/css/mixins/utils.css";

.Welcome {
  @mixin interpolate padding-top, 5, 10;
  @mixin interpolate padding-bottom, 5, 10;

  width: 100%;
  padding-left: 15%;
  padding-right: 15%;
  background-color: var(--color-primary);

  @media (--phone-md) {
    padding-left: 8%;
    padding-right: 8%;
  }
}

.Welcome__heading {
  @mixin interpolate margin-bottom, 3, 5;

  padding-left: 8px;
  color: var(--color-black);
}

.Welcome__text {
  line-height: 1.3;
  color: var(--color-black);
}

.Welcome__text_subheading {
  margin-top: 4rem;
  line-height: 1.3;
  color: var(--color-black);
}

.Welcome__text:not(:first-of-type) {
  margin-top: 2rem;
}

.Welcome__icons {
  width: 100%;
  margin-top: 1.8em;

  @media (--desktop-lg) {
    width: 100%;
    margin-top: 2.7em;
  }
}

.Welcome__grid {
  display: flex;
  column-gap: 10px;
  margin: 1em 0 1em 0;
  justify-content: flex-start;
  align-items: center;

  img {
    width: 3%;
    margin: auto 0;
  }

  p {
    margin: auto 0;
  }
}

.email {
  padding-top: 0.5em;
}
</style>
