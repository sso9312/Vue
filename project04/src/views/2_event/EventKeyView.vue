<template>
  <div>
    <!-- 4) EventKeyView.vue -->
    <h3> key 이벤트</h3>
    <input type="search" v-model="searchText" @keyup.enter="doSearch">
    <button @click="doSearch">조회</button>
    <!-- keyup이벤트의 세부 속성들 -->
    <!-- .enter -->
    <!-- .tab -->
    <!-- .delete -->
    <!-- .space -->
    <!-- .ctrl.enter-->
    <hr>

    <!-- $event 현재 시점에서 발생한 이벤트값 -->
    <input type="search" v-model="searchText" @keyup="checkEnter($event)">
  </div>
</template>

<script>

export default {

  data () {
    return {
      searchText: ''
    }
  },
  methods: {
    doSearch () {
      alert(this.searchText)
    },
    checkEnter (event) {
      // alert(event)
      if (event.keycode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>
