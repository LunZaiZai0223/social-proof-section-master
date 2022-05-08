<template>
  <main>
    <the-header></the-header>
    <rating-cards></rating-cards>
    <comment-cards></comment-cards>
  </main>
</template>

<script>
import TheHeader from './TheHeader.vue';
import RatingCards from './RatingCards.vue';
import CommentCards from './CommentCards.vue';

export default {
  name: 'TheContainer',
  components: {
    TheHeader,
    RatingCards,
    CommentCards,
  }
}
</script>

<style lang="scss" scoped>
main {
  max-width: 1024px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2.5rem;
  padding: 1.5rem;
  @media screen and (max-width: 768px) {
    display: block;
  }

  &:before {
    content: '';
    background-image: url('../assets/images/bg-pattern-top-desktop.svg');
    background-repeat: no-repeat;
    position: absolute;
    height: 362px;
    width: 584px;
    top: 0;
    left: 0;
    @media screen and (max-width: 768px) {
      background-image: url('../assets/images/bg-pattern-top-mobile.svg');
    }
  }

  &:after {
    content: '';
    background-image: url('../assets/images/bg-pattern-bottom-desktop.svg');
    background-repeat: no-repeat;
    position: absolute;
    height: 673px;
    width: 1085px;
    @media screen and (max-width: 768px) {
      background-image: url('../assets/images/bg-pattern-bottom-mobile.svg');
      bottom: 0;
    }
  }
}

</style>
