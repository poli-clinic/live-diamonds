<template>
  <h2 v-if="heading === 1"><slot /></h2>
  <h3 v-if="heading === 2"><slot /></h3>
  <h4 v-if="heading === 3"><slot /></h4>
  <h5 v-if="heading === 4"><slot /></h5>
  <h6 v-if="heading === 5"><slot /></h6>
</template>

<style scoped lang="scss">
  h2{
    font-size: 49px;
    font-weight: 800;
    font-style: normal;
    text-transform: uppercase;
  }
  h3{
    font-size: 43px;
    text-transform: uppercase;
    font-weight: 300;
    font-style: italic;
  }
  h4{ font-size: 1.5rem; }
  h5{ font-size: 1.15rem; text-transform: uppercase; }
  h6{ font-size: 1rem; }

  *{
    color: #1A5632;
    font-family: 'Montserrat', sans-serif;
    margin: 0;
    display: inline-block;
  }

  @media (max-width: 768px){
    h2{
      font-size: 36px;
    }
    h3{
      font-size: 32px;
    }
    *{
      max-width: 90%;
      margin-left: auto;
      margin-right: auto;
    }
  }
  @media (max-width: 390px){
    h2{
      font-size: 32px;
    }
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