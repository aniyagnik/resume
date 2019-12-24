<template>
  <div class='edu-box'>
    <p class="display-1 text-capitalize">{{ institute.title }}</p>
    <p class="title">{{ institute.name }}</p>
    <p class="body-2">{{ institute.address }}</p>
    <p class="subtitle-1">SESSION : {{ institute.session }}</p>
    <p class="subtitle-1">{{ institute.ex1 }} {{ institute.marks1 }}</p>
    <p class="subtitle-1">{{ institute.ex2 }} {{ institute.marks2 }}</p>
  </div>
</template>

<script>
export default {
  props: [ 'institute' ]
}
</script>

<style lang="scss">
.edu-box{
    background-image: linear-gradient(to right top, #c5e5ad, #b4ebcb, #b2ede4, #c0edf4, #d5ecf8, #cfdfe9, #c9d3da, #c2c7cb, #a4abaf, #879092, #6b7577, #515c5c);
  opacity: 0.6;
  padding: 1vw;
  box-shadow: 0px 6px 20px white;
}
</style>
