<template>
  <p><slot /></p>
</template>

<style scoped>
  p{
    color: #404040;
    font-size: 20px;
    line-height: 26px;
    margin-top: 0;
    margin-bottom: 2rem;
    hyphens: none;
    word-wrap: unset;
  }
  @media (max-width: 768px){
    p{
      font-size: 18px;
      line-height: 23px;
      max-width: 90%;
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>

<script>
export default {
  name: 'Text'
};
</script>

