<script setup>
const props = defineProps({
  point: {
    type: String,
    required: true,
  },
  streak: {
    type: String,
    required: true,
  },
  key_point: {
    type: String,
    required: true,
  },
  setting: {
    type: Boolean,
    required: false,
    default: true,
  },
  back: {
    type: Boolean,
    required: false,
    default: false,
  },
  light: {
    type: Boolean,
    required: false,
    default: false,
  },
});
console.log(props.point, props.streak, props.key_point)
</script>

<template>
  <div class="reward-bar" :class="{ light: light }">
    <a v-if="back" class="arrow" href="/">
      <img class="reward-icon" src="../assets/svg/icons/arrow-left.svg" />
    </a>
    <div class="point">
      <img class="reward-icon" src="../assets/svg/icons/reward.svg" />
      <span>{{ point }}P</span>
    </div>
    <div class="streak">
      <img class="reward-icon" src="../assets/svg/icons/streak.svg" />
      <span>{{ streak }}</span>
    </div>
    <div class="key">
      <img class="reward-icon" src="../assets/svg/icons/key.svg" />
      <span>{{ key_point }}</span>
    </div>
    <div v-if="setting" class="setting">
      <img class="reward-icon" src="../assets/svg/icons/setting.svg" />
    </div>
  </div>
</template>

<style scoped>
.reward-bar {
  display: flex;
  align-items: stretch;
  margin-top: -4px;
  margin-bottom: 1rem;
  width: 100%;
}
.reward-icon {
  height: 1rem;
}
.reward-bar div {
  line-height: 0px;
  padding: 0.5rem;
  background: #413147;
  border-radius: 1rem;
  text-align: center;
}
.light div {
  background-color: #f2f2f2;
}
.reward-bar span {
  margin-left: 6px;
}
.light span {
  color: #000000;
}
.point {
  font-family: "Roboto Mono";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 18px;
  display: flex;
  align-items: center;
}
.streak {
  font-family: "Roboto Mono";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 18px;
  display: flex;
  align-items: center;
  margin-left: 0.5rem;
}
.key {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 18px;
  display: flex;
  align-items: center;
  margin-left: 0.5rem;
}
.setting {
  position: absolute;
  right: 0;
  background: transparent !important;
  padding: 0px !important;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
.setting .reward-icon {
  width: 20px !important;
  height: 20px !important;
  margin: auto;
}
.arrow {
  background: transparent !important;
  padding: 0px !important;
  display: flex;
  align-items: center;
  justify-content: center;
}
.arrow .reward-icon {
  background: transparent !important;
  width: 24px !important;
  height: 24px !important;
  margin-right: 1rem;
}
</style>
