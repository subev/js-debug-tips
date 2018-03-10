<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
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
      participants: [
        {
          name: 'Dragan',
          age: 13
        },{
          name: 'Ivan',
          age: 23
        }
      ],
      random: null
    };
  },
  computed: {
    winner: function() {
      return this.participants[this.random];
    },
    winnerName: function() {
      return this.winner.name;
    }
  },
  methods: {
    pickWinner: function() {
      this.random = Math.floor(Math.random() * this.participants.length);
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

.participants {
  display: flex;
}

.participant {
  flex: 1 1 auto;
  margin: 20px 50px;
  border-radius: 4px;
  border: 1px solid #4fc08d;
}
</style>
