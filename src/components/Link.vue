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
    padding: 5px 0;
    color: #215732;
    font-weight: 600;
    text-decoration: none;
    font-size: 1.4rem;
    border-bottom: 2px solid #215732;
  }
  a:hover{
    border-color: #215732;
  }

  @media (max-width: 768px){
    a{
      font-size: 1rem;
    }
  }
</style>