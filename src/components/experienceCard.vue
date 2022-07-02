<template>
  <v-card
    class="mx-auto"
    max-width="344"
    elevation="5"
    light
    style=' background-image: linear-gradient(to right bottom, #000000, #532623, #975420, #bb9900, #a8eb12);'
  >

<v-list-item three-line>
      <v-list-item-content>
        <div
          class="subtitle-2 mb-4 white--text"
          @click="openNewLink(experience.companyLink)"
          style="cursor: pointer;"
        >
          {{experience.companyName}}
        </div>
        <v-list-item-title class="text-h5 mb-1 yellow--text font-weight-bold">
          {{experience.post}}
        </v-list-item-title>
        <v-list-item-subtitle class="text--body-1 mb-3 white--text">
          {{experience.duration}}
        </v-list-item-subtitle>
        <v-list-item-content>
          <v-list-item-subtitle class="white--text" v-for='(point,i) in experience.summary' :key='i'>{{i+1}}. {{ point }}</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item-content>
    </v-list-item>

    <v-card-actions>
      <v-btn
        color="orange lighten-2"
        text
        @click="openNewLink(experience.certificate)"
      >
        Certificate
      </v-btn>
    </v-card-actions>

  </v-card>
</template>

<script>
export default {
  name: 'experience',
  props: [ 'experience' ],
  methods: {
    openNewLink: function (link) {
      window.open(link, '_blank')
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
