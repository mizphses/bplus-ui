<template>
  <div>
    <div class="weeks-view">
      <div v-for="weeks in classes" :key="weeks" class="list-view">
        <div>
          <p>{{weeks.day}}</p>
        </div>
        <div v-for="classinfo in weeks.classes" :key="classinfo.time"  :class="selectiveWidth()[0]">
          <div>
            <div class="badge">{{classinfo.time}}</div>
            <p>{{classinfo.name}}（{{classinfo.teacher}}）</p>
          </div>
          <div class="roomnum">{{classinfo.room}}</div>
        </div>
      </div>
    </div>
    <p>シラバスデータは中央大学シラバス公表サイトのデータをもとに作成されています．講義内容の検索はManabaまたはシラバスサイトをご確認ください．</p>
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
        "monday": {
          "day": "月",
          "classes": [
            {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 2},
            {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "tuesday": {
          "day": "火",
          "classes": [
            {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "wednesday": {
          "day": "水",
          "classes": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 5, "name": "外書講読（政治学）Ａ１（独）／外書講読（政治学）Ｂ１（独）	", "teacher": "井関　正久", "room": "???", "department": "law.undergraduate", "cource-id": 1},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "thursday":  {
          "day": "木",
          "classes": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 5, "name": "外書講読（政治学）Ａ１（独）／外書講読（政治学）Ｂ１（独）	", "teacher": "井関　正久", "room": "???", "department": "law.undergraduate", "cource-id": 1},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "friday": {
          "day": "金",
          "classes": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 5, "name": "外書講読（政治学）Ａ１（独）／外書講読（政治学）Ｂ１（独）	", "teacher": "井関　正久", "room": "???", "department": "law.undergraduate", "cource-id": 1},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "saturday":  {
          "day": "土",
          "classes": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
        "others": {
          "day": "その他",
          "classes": [
            {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
            {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F404", "department": "econ.undergraduate", "cource-id": 1},
          ]
        },
      }
    }
  },
  methods: {
    selectiveWidth() {
      if (this.classes.others.classes.length > 0) {
        return ["weeks-plus-classbox"]
      } else {
        return ["classbox"]
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
    width: calc(100vw - 5em);
  }
  .classbox{
    width: calc(calc(100vw - 3em)/6 - 2em);
    margin: 0.1em 0.3em;
    padding: 0.5em;
    height: calc(100% / 4.5);
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .weeks-plus-classbox{
    width: calc(calc(100vw - 3em)/7 - 2em);
    margin: 0.2em 0.1em;
    padding: 0.5em;
    height: 150px;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  @media print {
    .weeks-view{
      font-size: 0.8em;
    }
    .classbox, .weeks-plus-classbox{
      height: 100px;
    }
  }
  @media (max-width: 768px) {
    .weeks-view{
      overflow-x: scroll;
      width: calc(100vw - 4em);
    }
    .classbox, .weeks-plus-classbox{
      width: 10em;
    }
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