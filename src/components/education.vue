<template>
  <div class='institute'>
    <table  style='width:50vw'>
      <tr>
        <td class="first">
          <span>{{institute.year}}</span><br>
          <span>{{institute.place}}</span>
        </td>
        <td class="second">
          <b style='font-size:1.3em;color:gold'>
            <span>{{ institute.name }}</span>
            <span> / {{ institute.degree }}</span>
          </b>
          <ul>
            <li>{{ institute.marks }}</li>
            <li>{{ institute.board }}</li>
          </ul>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  props: [ 'institute' ]
}
</script>
<style lang="scss">
.institute{
    min-width:40vw;
}
.first{
    border-left:10px solid crimson;
    min-width: 30%;
    width: 30%;
    padding-top: 60px;
    font-size:1.1em;
    font-weight: 900;
    text-align: center;
}
span{
    color: aliceblue;
}
.second{
    padding-left: 2%;
    min-width: 70%;
    width: 70%;
    li{
      color: gold;
    }
}
</style>
