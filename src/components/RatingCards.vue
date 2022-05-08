<template>
  <ul class="rating-card-list">
    <li v-for="(ratingText, index) in ratings" :key="index">
      <div class="rating-card-item" :style="{ transform: `translateX(${2.5 * index}rem)`}">
        <ul class="rating-inner-start">
          <li v-for="num in 5" :key="num">
            <img src="../assets/images/icon-star.svg" />
          </li>
        </ul>
        <p>{{ ratingText }}</p>
      </div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'RatingCards',
  data () {
    return {
      ratings: [
        'Rated 5 Stars in Reviews',
        'Rated 5 Stars in Report Guru',
        'Rated 5 Stars in BestTech'
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

.rating-card {
  &-list {
    grid-column: 2 / 3;
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    @media screen and (max-width: 768px) {
      margin-bottom: 1.5rem;
    }
  }

  &-item {
    display: flex;
    align-items: center;
    padding: 1rem 1.5rem;
    border-radius: 0.5rem;
    gap: 1.5rem;
    background-color: $secondary-light;
    color: $primary-dark;
    font-weight: 500;
    @media screen and (max-width: 768px) {
      transform: translateX(0) !important;
      justify-content: space-between;
      padding: 1rem 15%;
    }
    @media screen and (max-width: 640px) {
      flex-direction: column;
      gap: 0.75rem;
    }
  }
}

.rating-inner {
  &-start {
    display: flex;
    gap: 0.75rem;
  }
}
</style>
