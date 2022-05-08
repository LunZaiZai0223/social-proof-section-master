<template>
  <header>
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
  </header>
</template>

<script>
export default {
  name: 'TheHeader',
  data () {
    return {
      title: '10,000+ of our users love our products.',
      description: 'We only provide great products combined with excellent customer service. See what our satisfied customers are saying about our services.'
    }
  }
}
</script>

<style lang="scss" scoped>
header {
  text-align: start;
  grid-column: 1 / 2;
}

h1 {
  font-size: 3rem;
  color: $primary-dark;
  width: 75%;
  margin-bottom: 0.75rem;
  @media screen and (max-width: 768px) {
    width: 85%;
    margin: 0 auto;
    text-align: center;
  }
}

p {
  line-height: 1.25rem;
  color: $secondary-dark;
  @media screen and (max-width: 768px) {
    margin: 1.5rem 0;
    text-align: center;
    font-size: 1.25rem;
    line-height: 1.5rem;
  }
}
</style>
