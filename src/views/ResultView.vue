import {} from 
<template>
    <div class="container">
        <div class="small_title">후보별 득표율</div>

      <VoteOneOne v-bind:candidates="items"/>

    </div>
</template>
<script>
import VoteOneOne from "@/components/VoteOne";
export default {
  name: "ResultView",
  components: {
    VoteOneOne,
  },
  data() {
    return {
      items: [
        {id: 1, name: "김오돌", voteEarned: 10, voteRate: 45.5},
        {id: 2, name: "김이돌", voteEarned: 2, voteRate: 9.1},
        {id: 3, name: "김삼돌", voteEarned: 1, voteRate: 4.5},
        {id: 4, name: "김사돌", voteEarned: 3, voteRate: 13.6},
        {id: 5, name: "김오돌", voteEarned: 3, voteRate: 13.6},
        {id: 6, name: "김육돌", voteEarned: 2, voteRate: 9.1},
        {id: 7, name: "김칠돌", voteEarned: 1, voteRate: 4.5}
      ]
    }
  }
};
</script>
<style lang="scss" scoped>
tr {
    border: 1px solid black;
}
.container {
    border-spacing: 5%;
    width: 90%;
    margin-left: auto;
    margin-right: auto;
    .small_title {
        width: 100%;
        text-align: center;
        font-size: 30px;
        margin: 1%;
    }
}
    
</style>