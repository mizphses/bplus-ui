<template>
  <div :class="selectiveWidth()[0]">
    <div v-for="weeks in classes" :key="weeks" class="list-view">
      <div v-for="classinfo in weeks" :key="classinfo.time"  :class="selectiveWidth()[1]">
        <div>
          <div class="badge">{{classinfo.time}}</div>
          <p>{{classinfo.name}}（{{classinfo.teacher}}）</p>
        </div>
        <div class="roomnum">{{classinfo.room}}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TimetableWindow',
  data () {
    return {
      user: {
        name: "Fuminori Ogawa",
        id: "mizphses",
        grade: 2,
        department: "econ.undergraduate",
      },
      classes: {
        "monday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "tuesday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "wednesday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 5, "name": "外書講読（政治学）Ａ１（独）／外書講読（政治学）Ｂ１（独）	", "teacher": "井関　正久", "room": "???", "department": "law.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "thursday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "gflp.undergraduate"},
          {"time": 5, "name": "演習Ⅱ（Social Research）", "teacher": "武石 智香子", "room": "2010", "department": "com.master"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "friday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "saturday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate"},
        ],
        "others": [
          {"time": null, "name": "ＡＩデータサイエンスツールＶＩ", "teacher": "山田 一郎, 佐藤 次郎, 鈴木 三郎", "room": "F404", "department": "ads.undergraduate"},
        ],
      }
    }
  },
  methods: {
    selectiveWidth() {
      if (this.classes.others.length > 0) {
        return ["weeks-plus-view", "weeks-plus-classbox"]
      } else {
        return ["weeks-plus-view", "classbox"]
      }
    }
  },
}
</script>

<style scoped>
  .weeks-view{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: calc(100vw - 4em);
  }
  .weeks-plus-view{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: calc(100vw - 4em);
  }
  .classbox{
    font-size: 50%;
    width: calc(calc(100vw - 3em)/6 - 2em);
    margin: 0.1em 0.3em;
    padding: 0.5em;
    min-height: calc(100% / 4.5);
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .weeks-plus-classbox{
    font-size: 50%;
    width: calc(calc(100vw - 3em)/7 - 3em);
    margin: 0.2em 0.1em;
    padding: 0.5em;
    min-height: calc(100% / 4.5);
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .badge {
    background: rgb(0, 102, 103);
    padding: 0.3em;
    width: 1em;
    height: 1em;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    color: #ffffff;
  }
  .roomnum{
    font-size: 0.8em;
    padding-top: 2px;
    padding-bottom: 2px;
    text-align: center;
    width: 100%;
    background: rgb(200, 252, 255);
    border-radius: 0.3em;
  }
</style>