<template>
  <div class="hello">
    <h3>{{ msg }}</h3>
    <h2>Jackpot is ${{ jackpot | formatNumber }}</h2>
    <p>
      We randomly choose a winner to take it all!
    </p>
    <div>
      <div class="participants">
        <div v-for='participant in participants' class="participant">
          {{ participant.name }}
        </div>
      </div>
    </div>
    <div>
      <button @click='pickWinner'>Get a Winner!</button>
    </div>
    <h3 v-if='winner'>Winner is {{ winnerName }} </h3>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Lottery',
  props: {
    msg: String,
  },
  data: function () {
    return {
      jackpot: 1000000,
      participants: [
        {
          name: 'Dragan',
          age: 13,
          balance: 0
        },{
          name: 'Ivan',
          age: 23,
          balance: 0
        }
      ],
      random: -1
    };
  },
  created() {
    setInterval(() => {
      this.updateJackpot();
    }, 300);
  },
  computed: {
    winner: function() {
      if (this.random !== null) {
        return this.participants[this.random];
      }
    },
    winnerName: function() {
      return this.winner && this.winner.name;
    }
  },
  methods: {
    pickWinner() {
      this.random = Math.floor(Math.random() * this.participants.length);
      if(this.winner) {
        this.winner.balance += this.jackpot;
      }
      this.jackpot = 1000000;
    },
    updateJackpot() {
      this.jackpot += Math.floor(Math.random() * 100000);
    }
  },
  filters: {
    formatNumber(value: number) {
      return new Intl.NumberFormat().format(value);
    }
  }
});
</script>

<style lang='scss' scoped>
h3 {
  margin: 40px 0 0;
}

.participants {
  display: flex;

  .participant {
    flex: 1 1 auto;
    margin: 20px 50px;
    border-radius: 4px;
    border: 1px solid #4fc08d;
  }
}

</style>
