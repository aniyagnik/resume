<template>
  <v-app>
    <div id='nav'>
      <router-link v-for='item in items' :key='item.text' :to="`${item.route}`">
        <v-btn text tile  height=55 class='white--text'>
          <v-icon left>{{ item.icon }}</v-icon>
          <span>{{ item.text }}</span>
        </v-btn>
      </router-link>
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
          text: 'education',
          icon: 'mdi-book-open-page-variant',
          route: '/education'
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
  background-color: black;
}
</style>
