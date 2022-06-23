import {} from 
<template>
    <div class="container">
        <div class="small_title"> {{$route.params.id}}번 {{$route.params.name}} 후보 득표 경향 분석</div>

        <VoteTwoTwo v-bind:votedetails="items"/>

    </div>
</template>
<script>
import VoteTwoTwo from "@/components/VoteTwo";
export default {
  name: "ResultView",
  components: {
    VoteTwoTwo,
  },
  data() {
    return {
      items: [
        {id: 1, age: 10, voteEarned: 4, voteRate:40.0},
        {id: 1, age: 20, voteEarned: 1, voteRate:10.0},
        {id: 1, age: 30, voteEarned: 1, voteRate:10.0},
        {id: 1, age: 40, voteEarned: 1, voteRate:10.0},
        {id: 1, age: 50, voteEarned: 0, voteRate:0.0},
        {id: 1, age: 60, voteEarned: 0, voteRate:0.0},
        {id: 1, age: 70, voteEarned: 2, voteRate:20.0},
        {id: 1, age: 80, voteEarned: 0, voteRate:0.0},
        {id: 1, age: 90, voteEarned: 1, voteRate:10.0},
      ],
    }
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
.container {
    border-spacing: 5%;
    width: 90%;
    margin-left: auto;
    margin-right: auto;
    background-color: white;

    .small_title {
        width: 100%;
        text-align: center;
        font-size: 30px;
        margin: 1%;
    }
}
</style>