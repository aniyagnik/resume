<template>
    <b-container>
        <div class="flex-inside-item">
          <a :href="`${websiteLink.link}`">
            <v-icon left dark x-large>{{ websiteLink.icon }}</v-icon>
            <span style='font-size: 1.1em' class='font-weight-bold white--text text-capitalize'>{{ websiteLink.name }}</span>
          </a>
        </div>
    </b-container>
</template>

<script>
export default {
  name: 'websiteLinkbox',
  props: [ 'websiteLink' ],
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
.flex-inside-item{
        opacity: 0.6;
        // border:1px solid rgb(235, 11, 11);
        padding-left: 4vw;
        padding-right: 4vw;
    }
    .flex-inside-item:hover{
      cursor: pointer;
      opacity:1.1;
    }
</style>
