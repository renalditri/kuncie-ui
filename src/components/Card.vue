<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  contentType: {
    type: String,
    required: false,
    default: "Video",
  },
  duration: {
    type: String,
    required: false,
  },
  variant: {
    type: String,
    required: true,
    default: "module",
    validators: (value) => ["module", "video"].includes(value),
  },
  color: {
    type: String,
    require: false,
    default: "red",
    validators: (value) => ["blue", "red", "yellow"].includes(value),
  },
  newContent: {
    type: Boolean,
    required: false,
    default: false,
  },
  presenter: {
    type: String,
    required: false,
  },
  presenter_url: {
    type: String,
    required: false,
  },
  disabled: {
    type: Boolean,
    required: false,
    default: false,
  },
  href: {
    type: String,
    required: true,
    default: false,
  },
});

const isModule = () => props.variant == "module";
const isVideo = () => props.variant == "video";
const addClass = () => {
  return {
    video: isVideo(props.variant),
    module: isModule(props.variant),
    blue: props.color == "blue",
    yellow: props.color == "yellow",
    red: props.color == "red",
    disabled: props.disabled,
  };
};
</script>

<template>
  <a class="card" :class="addClass()" :href="href">
    <h3>{{ title }}</h3>
    <h4 v-if="isVideo()" class="tag">
      {{ contentType }} <span class="dot" /> {{ duration }}
    </h4>
    <div class="presenter-wrapper">
      <img class="presenter-img" :src="presenter_url" />
      <div v-if="isModule()" class="body-1">
        {{ presenter }}
        <img src="../assets/svg/icons/plus-circle.svg" />
      </div>
      <img
        v-if="isVideo() && !disabled"
        class="play-button"
        src="../assets/svg/icons/play-button.svg"
      />
      <img
        v-if="disabled"
        class="play-button"
        src="../assets/svg/icons/lock.svg"
      />
    </div>
    <img
      v-if="newContent"
      class="new-content"
      src="../assets/svg/new-content.svg"
    />
  </a>
</template>

<style scoped>
.card {
  position: relative;
  border-radius: 8px;
  filter: drop-shadow(0px 4px 10px rgba(55, 51, 69, 0.2));
  padding: 1rem 0.75rem;
  box-shadow: 0px 4px 10px rgba(55, 51, 69, 0.2);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: start;
}

.play-button {
  margin-left: auto;
  margin-right: 0px;
  float: right;
}

.card .body-1 {
  color: #09050a;
  align-items: end;
}

.presenter-wrapper {
  line-height: 0px;
  width: 100%;
  box-sizing: border-box;
}
.presenter-img {
  border-radius: 1000px;
}
.presenter-wrapper .body-1 {
  display: flex;
  width: 100%;
  box-sizing: border-box;
  justify-content: space-between;
}
.module .presenter-img {
  margin-bottom: 0.5rem;
  height: 48px;
  width: 48px;
}
.video {
  height: 168px;
  background-size: 100% 100%, auto;
  background-repeat: no-repeat;
  font-size: 4rem;
}
.module {
  height: 242px;
  background-position: 0px 105px, 100% 50%, -100% 0%, 100% 0%;
  background-repeat: no-repeat;
}
.new-content {
  position: absolute;
  top: -2px;
  left: -2px;
}
.tag {
  padding: 4px 8px;
  background: rgba(44, 26, 50, 0.3);
  border-radius: 4px;
  display: inline-block;
}
.module.red {
  background-image: url("../assets/svg/card-circle-left-red.svg"),
    url("../assets/svg/card-circle-right-red.svg"),
    url("../assets/svg/card-circle-big-red.svg"),
    url("../assets/svg/card-circle-corner-red.svg");
  font-size: 4rem;
}
.module.blue {
  background-image: url("../assets/svg/card-circle-left-blue.svg"),
    url("../assets/svg/card-circle-right-blue.svg"),
    url("../assets/svg/card-circle-big-blue.svg"),
    url("../assets/svg/card-circle-corner-blue.svg");
  font-size: 4rem;
}
.module.yellow {
  background-image: url("../assets/svg/card-circle-left-yellow.svg"),
    url("../assets/svg/card-circle-right-yellow.svg"),
    url("../assets/svg/card-circle-big-yellow.svg"),
    url("../assets/svg/card-circle-corner-yellow.svg");
  font-size: 4rem;
  color: black;
}
.video .presenter-img {
  height: 40px;
  width: 40px;
}
.video.red {
  background-image: linear-gradient(
      rgba(240, 122, 90, 0.9),
      rgba(240, 122, 90, 0.9)
    ),
    url("../assets/png/bg-1.png");
}
.video.blue {
  background-image: linear-gradient(
      rgba(42, 136, 170, 0.9),
      rgba(42, 136, 170, 0.9)
    ),
    url("../assets/png/bg-2.png");
}
.video.yellow {
  background-image: linear-gradient(
      rgba(245, 197, 119, 0.9),
      rgba(245, 197, 119, 0.9)
    ),
    url("../assets/png/bg-2.png");
}
.dot {
  margin-bottom: 2px;
  display: inline-block;
  width: 4px;
  height: 4px;
  background: #ffffff;
  border-radius: 1000px;
}
.video {
  min-width: 224px;
  max-width: 224px;
}
.module {
  min-width: 194px;
  max-width: 194px;
}
.disabled {
  color: #6b5f6f !important;
  background-color: #e5e5e5;
  background-image: none !important;
}

.disabled .presenter-img {
  filter: grayscale(100%);
}
</style>
