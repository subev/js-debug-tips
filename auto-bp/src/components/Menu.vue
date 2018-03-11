<template>
  <div class="menu">
    <div
      class='btn'
      @mouseenter='open'
      @mouseout='close'
      @click='close'
      @mousedown='close'>

      &#9776; Menu
    </div>
    <div class="content" v-if='opened'>
      <ul>
        <li>Foo</li>
        <li>Bar</li>
        <li>Baz</li>
      </ul>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Menu',
  props: {
  },
  data: function () {
    return {
      opened: false
    };
  },
  computed: {
  },
  methods: {
    open: function() {
      this.opened = true;
    },
    close: function() {
      this.opened = false;
    }
  }
});
</script>

<style scoped>
.menu {
  position: relative;
}

.btn {
  border: 1px solid transparent;

  &:hover {
    border-color: #4fc08d;
  }
}

.content {
  position: absolute;
  border: 1px solid #4fc08d;
  padding: 10px;
  background: white;
  border-radius: 4px;
}
</style>
