<template>
  <v-app v-cloak>
    <div id='nav'>
        <v-btn v-for='item in items' :key='item.text' :to="`${item.route}`" text tile  height=55 class='white--text'>
          <v-icon left>{{ item.icon }}</v-icon> <br>
          <span class='hidden-xs-only'>{{ item.text }}</span>
        </v-btn>
    </div>
    <v-content>
      <router-view v-cloak></router-view>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      items: [
        {
          text: 'home',
          icon: 'mdi-home',
          route: '/'
        },
        {
          text: 'profile',
          icon: 'mdi-account',
          route: '/profile'
        },
        {
          text: 'portfolio',
          icon: 'mdi-credit-card',
          route: '/portfolio'
        },
        {
          text: 'contact',
          icon: 'mdi-email',
          route: '/contact'
        }
      ]
    }
  },
  components: {
  }
}
</script>

<style lang="scss">
#nav {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid black;
  background-image: linear-gradient(to right top, #2329b1, #4d1081, #4e0057, #400235, #2b071c, #330921, #3b0b25, #430d2a, #6f014f, #9a007e, #bf00b7, #da00fb);
  box-shadow: 0px 10px 30px #001e1f;
}

[v-cloak] {
    display: none;
}
</style>
