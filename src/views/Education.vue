<template>
  <div id='education'>
    <div class='flex-item' v-for='(item,i) in institutes' :key=i>
      <edu-container :institute='item'></edu-container>
    </div>
  </div>
</template>

<script>
import eduBox from '../components/eduBox.vue'

export default {
  name: 'education',
  components: {
    'edu-container': eduBox
  },
  data () {
    return {
      institutes: [
        {
          title: 'schooling',
          name: 'Universal Public School',
          session: '2017',
          marks1: '9.5',
          ex1: '10th CCE percentile : ',
          marks2: '93.5',
          ex2: '12th Board percentage : '
        },
        {
          title: 'Graduation',
          name: 'Maharaja Surajmal Institute Of Technology',
          session: '2017-2021',
          marks1: '8',
          ex1: 'current SPGA : ',
          marks2: '',
          ex2: ''
        }
      ]
    }
  }
}
</script>
<style lang="scss">
#education{
  background-image: url('../assets/28156.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 92.5vh;
}
</style>
