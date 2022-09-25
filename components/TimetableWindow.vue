<template>
  <div class="weeks-view">
    <div v-for="weeks in classes" :key="weeks" class="list-view">
      <div v-for="classinfo in weeks" :key="classinfo.time" class="classbox">
        <div class="flex-row">
          <div class="badge">{{classinfo.time}}</div> &nbsp; {{classinfo.name}}
          <p></p>
        </div>
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
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "tuesday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "wednesday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "thursday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "gflp.undergraduate"},
          {"time": 5, "name": "演習Ⅱ（Social Research）", "teacher": "武石 智香子", "room": "2010", "department": "comm.master"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "friday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "saturday": [
          {"time": 1, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 2, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 3, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 4, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 5, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
          {"time": 6, "name": "情報基礎", "teacher": "山田太郎", "room": "F", "department": "econ.undergraduate"},
        ],
        "others": [
        ],
      }
    }
  },
}
</script>

<style>
  .weeks-view{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
  }
  .classbox{
    width: calc(calc(100vw - 3em)/6 - 2em);
    margin: 0.3em;
    padding: 0.5em;
    height: calc(100% / 6);
    border: 1px solid black;
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
    color: #fff;
  }
  .flex-row{
    display: flex;
    flex-direction: row;
    width: 100%;
  }
</style>