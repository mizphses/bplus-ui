<template>
  <div>
    <NavBar />
    <div class="padding-2em">
      <h2>時間割サービス</h2>
      <div class="caution">
        <div class="flex-row align-center justify-between">
          <p class="title">学部間共通科目・他学部履修の登録方法</p>
          <a class="material-symbols-outlined no-decorator" href="#">close</a>
        </div>
        <p>標記の種別の科目については、詳細検索タブより科目名をご入力下さい。</p>
      </div>
      <TimetableWindow />
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .padding-2em {
    padding: 2em;
  }
  .flex-timetable{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
</style>