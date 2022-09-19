<template>
    <a :href="link">
      <slot />
    </a>
</template>

<script>
export default {
  name: "Link",
  props: {
    link: String
  },
}
</script>

<style scoped>
  a{
    text-transform: uppercase;
    display: inline-block;
    padding: 2px 0;
    color: #1A5632;
    font-weight: 500;
    text-decoration: none;
    font-size: 28px;
    line-height: 34px;
    border-bottom: 1px solid #215732;
    -webkit-hyphens: none;
  }
  a:hover{
    border-color: #215732;
  }

  @media (max-width: 768px){
    a{
      font-size: 24px;
      line-height: 29px;
    }
  }
</style>