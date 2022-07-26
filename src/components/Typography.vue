<template>
  <h2 v-if="heading === 1"><slot /></h2>
  <h3 v-if="heading === 2"><slot /></h3>
  <h4 v-if="heading === 3"><slot /></h4>
  <h5 v-if="heading === 4"><slot /></h5>
  <h6 v-if="heading === 5"><slot /></h6>
</template>

<style scoped lang="scss">
  h2{ font-size: 2rem; text-transform: uppercase }
  h3{ font-size: 2.5rem; font-weight: 600; text-transform: uppercase }
  h4{ font-size: 1.5rem; }
  h5{ font-size: 1.15rem; text-transform: uppercase; }
  h6{ font-size: 1rem; }

  *{
    color: #215732;
    font-family: 'Montserrat', sans-serif;
  }
</style>

<script>
export default {
  name: 'Typography',
  props: {
    heading: Number,
  },
};

</script>