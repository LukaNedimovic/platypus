<template>
  <section class="user-account-section-header">
    <h1 class="user-account-section-header__title">
      <slot name="title" />
    </h1>
    <p class="user-account-section-header__description">
      <slot name="description" />
    </p>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue-demi'

export default defineComponent({
  name: 'UserAccountSectionHeader'
})
</script>

<style lang="scss" scoped>
@import 'carbon-components/scss/globals/scss/typography';
@import '~/../scss/variables/mq.scss';
@import '~/../scss/variables/colors.scss';
@import '~/../scss/mixins/mixins.scss';

$max-description-width: 38rem;

.user-account-section-header {
  padding-bottom: $spacing-05;
  border-bottom: 2px solid $border-color-light-2;

  &__container {
    @include type-style('body-long-01');
    padding-bottom: $spacing-05;
  }

  &__title {
    @include type-style('expressive-heading-05', $fluid: true);
    padding-bottom: $spacing-05;
    color: $text-active-color;
  }

  &__description {
    max-width: $max-description-width;
  }
}
</style>
