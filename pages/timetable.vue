<template>
  <div>
    <NavBar />
    <div class="padding-2em">
      <h2>時間割サービス</h2>
      <div class="caution" v-if="windowstatus_1">
        <div class="flex-row align-center justify-between">
          <p class="title">学部間共通科目・他学部履修の登録方法</p>
          <a class="material-symbols-outlined no-decorator" href="#" @click="closewindow_1">close</a>
        </div>
        <p>標記の種別の科目については、詳細検索タブより科目名をご入力下さい。</p>
      </div>
      <TimetableWindow />
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        windowstatus_1: true,
      }
    },
    methods: {
      closewindow_1() {
        this.windowstatus_1 = false;
      }
    }
  }
</script>

<style lang="scss" scoped>
  .padding-2em {
    padding: 2em;
  }
  .flex-timetable{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  @media print {
    .weeks-view{
      font-size: 0.8em;
    }
    .caution{
      display: none;
    }
    .classbox, .weeks-plus-classbox{
      height: 100px;
    }
    .padding-2em{
      padding: 0;
    }
  }
</style>