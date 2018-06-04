<template>
    <div class="team">
    
    <p class="title">#TeamMEW</p>
    <p class="sub-title">MyEtherWallet</p>

    <div class="team-images">
      <li v-for="person in mainList">
        <img :src="'dist/'+person.image">
        <div class="info">
          <p class="name">{{person.name}}</p>
          <p class="position">{{person.position}}</p>
        </div>
      </li>
    </div>

  </div>
</template>
<script>
  import mainList from "@/lists/main-team.json"
  console.log(mainList)
  export default {
  name: 'app',
  data () {
    return {
      mainList: mainList
    }
  },
  computed: {
    imagePath: function (imgName) {
      return require('@/img/' + imgName)
    }
  }
}
</script>

<style lang="less">
  @import "./styles/styles.less";
</style>