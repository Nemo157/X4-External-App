<script setup>
import Main from './components/Main.vue'
import X4Header from './components/X4Header.vue'</script>
<script>
export default {
  data() {
    return {
      isPendingUpdate: false,
    }
  },
  methods: {
    /**
     * @param isPending
     */
    updatePending(isPending) {
      this.isPendingUpdate = isPending;
    }
  },
}
</script>

<template>
  <X4-header :is-pending-update="isPendingUpdate"/>
  <Main @updatePending="updatePending"/>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Muli:300,400,700');
</style>
