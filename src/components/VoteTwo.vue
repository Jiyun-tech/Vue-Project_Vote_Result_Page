<template>
    <table class="do_vote" cellspacing="0">
        <template v-for="detail in votedetails" :key="detail.age">
        <tr v-if="detail.id === 1"> 
            <td class="printname" align="left">
                {{detail.age}}대
            </td>
            <td class="each_result_bar" align="left">
                <img src="@/assets/redbar.png" height=20 :width=getPercent(detail.voteRate)>
                {{detail.voteEarned}} ({{detail.voteRate}}%)
            </td>
        </tr>
        </template>
    </table>
</template>

<script>
export default {
  name: "VoteTwoTwo",
  props: {
    votedetails: Array,
  },
  methods: {
    getPercent: function(n) {
    //   console.log("n : ", n);
      let percent = n * 7;
    //   console.log("percent : ", percent);
      return percent;
    }
  }
};
</script>

<style lang="scss" scoped>
tr {
    border: 1px solid black;
}
.do_vote {
    width: 95%;
    margin-left: auto;
    margin-right: auto;
    border-spacing: 0;
    border-collapse: collapse;
    font-size: 20px;
    border: 1px solid black;
    background-color:white;
    .printname{
        padding-left:1%;
        width: 250px;
    }
    .each_result_bar{
        border-left: 1px solid black;
        font-size: 25px;
    }
}
a:linked {
        color: blue;
    }
   a:visited {
        color: blue;
    }
    
</style>