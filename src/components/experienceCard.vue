<template>
  <v-card
    class="mx-auto"
    max-width="344"
    elevation="5"
  >
    <v-img
      :src="experience.image"
      height="200px"
      width="400px"
    ></v-img>

    <v-card-title>
      {{experience.companyName}}
    </v-card-title>

    <v-card-subtitle>
      {{experience.post}} <br>
      {{experience.duration}}
    </v-card-subtitle>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
        @click="openCertificate(experience.certificate)"
      >
        Certificate
      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          {{ experience.summary }}
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
export default {
  name: 'experience',
  props: [ 'experience' ],
  methods: {
    openCertificate: function (certificate) {
      window.open(certificate, '_blank')
    }
  },
  data () {
    return {
      show: false
    }
  }
}
</script>

<style lang='scss'>

</style>
