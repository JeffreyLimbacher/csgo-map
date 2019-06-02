<template>
  <div>
    <div class="area">
      <h2><p>{{ getName }}</p></h2>
    </div>
    <div class="area">
      <div class="health-box">
        <div class="health-bar-red"></div>
        <div class="health-bar-blue"></div>
        <div class="health-bar" v-bind:style="getHealthStyle"></div>
        <div class="health-bar-text">{{ player.health }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    player: {
      type: Object,
      required: true
    }
  },
  computed: {
    getName () {
      console.log(this.player.name)
      return this.player.name
    },
    getHealthStyle() {
      return this.player.health + '%';
    }
  }
}
</script>

<style>
.area {
  padding: 10px;
  text-align: center;
}

h2 {
  padding: 5px;
  text-align: center;
}

p {
  width: 500px;
  padding: 1%;
  margin: auto;
}

.health-box {
  background-color: #ccc;
  height: 30px;
  width: 500px;
  margin: 0 auto;
  border: solid 1px #aaa;
}

.health-bar {
  background-color: #007f00;
  width: inherit;
  height: 28px;
  position: relative;
  bottom: 56px;
}

.health-bar-red {
  width: 100%;
  height: 100%;
  background-color: #cc0000;
}

.health-bar-blue {
  width: 100%;
  height: 100%;
  background-color: #3bd3df;
  bottom: 28px;
  position: relative;
}

.health-bar-text {
  position: relative;
  bottom: 80px;
}

.message-box {
  text-align: center;
  padding: 5px;
}

.total,
.message-box {
  font-size: 16px;
  margin: 5px;
}
</style>
