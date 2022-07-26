<template>
  <p><slot /></p>
</template>

<style scoped>
  p{
    color: #3e3e3e;
    font-size: 1.3rem;
    line-height: 1.5;
    margin-top: 0;
    margin-bottom: 2rem;
  }
  @media (max-width: 768px){
    p{
      font-size: 1rem;
    }
  }
</style>

<script>
export default {
  name: 'Text'
};
</script>

