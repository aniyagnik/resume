<template>
  <div class='edu-box'>
    <p class="display-1 text-uppercase font-weight-bold" style="font-family:castellar;">{{ institute.title }}</p>
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
   background-image: radial-gradient(circle, #201d1f, #3b1a37, #4f1257, #5c047d, #5b00aa, #4d17b7, #3825c3, #0030d0, #003bb4, #1f4195, #334374, #404452);
  opacity: 0.9;
  padding: 1vw;
  box-shadow: 0px 6px 20px white;
  color: whitesmoke;
  cursor: pointer;
}
.edu-box:active {
    color:red;
    box-shadow: 0px 6px 15px rgb(148, 4, 4);
}
</style>
