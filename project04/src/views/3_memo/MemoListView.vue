<template>
  <div>
    <!-- MemoListView.vue -->
    <!-- ● Bankend : SpringBoot기반 (spring10_memo프로젝트 참조) -->
    <!-- MemoListView.vue -->
    <h3>방명록</h3>
    <p>
      <button class="btn btn-primary" @click="getlist">목록</button>
    </p>
    <ul class="list-group">
      <li v-if="memoList.length == 0" class="list-group-item">게시물이 없습니다</li>
      <li v-for="memo in memoList" :key="memo.memono" class="list-group-item">{{ memo.subject }} <span class="badge">{{memo.readcnt}}</span></li>
    </ul>
  </div>
</template>

<script>

export default {

  data () {
    return {
      memoList: []
    }
  },
  methods: {
    getlist () {
      // alert('getlist 함수 호출')
      // fetch() 자바스크립 기반의 서버와 데이터 통신
      fetch('http://localhost:9095/memolist').then((response) => {
        if (response.ok) {
          return response.json()
        }// if end
      }).then((json) => {
        this.memoList = json
      })
    }
  }
}
</script>

<style>
 @import 'https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css';
</style>
