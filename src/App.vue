<template>
  <v-app>
    <div id='nav'>
        <v-btn v-for='item in items' :key='item.text' :to="`${item.route}`" text tile  height=55 class='white--text'>
          <v-icon left>{{ item.icon }}</v-icon> <br>
          <span class='hidden-xs-only'>{{ item.text }}</span>
        </v-btn>
    </div>
    <v-content>
      <router-view></router-view>
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
          text: 'about',
          icon: 'mdi-account',
          route: '/about'
        },
        {
          text: 'portfolio',
          icon: 'mdi-account-card-details',
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
  background-image: linear-gradient(to top, #051937, #001e2e, #001e1f, #0f1c16, #191a16);
  box-shadow: 0px 10px 30px #001e1f;
}
</style>
