<template>
  <div>
    <h5>
      {{ displayText.join("") }}
      <span :class="{ cursor: true, 'cursor--blink': blinkCursor }">|</span>
    </h5>
  </div>
</template>

<script>
export default {
  name: "TypeWriter",
  props: {
    speed: {
      type: Number,
      default: 100,
    },
    deleteSpeed: {
      type: Number,
      default: 30,
    },
    nextWordInterval: {
      type: Number,
      default: 1200,
    },
    words: {
      type: Array,
    },
  },
  data() {
    return {
      displayText: [],
      currentWord: "",
      wordIdx: 0,
      timeoutSpeed: null,
      isWaitingNextWord: false,
      blinkCursor: false,
    };
  },
  mounted() {
    this.start();
  },
  methods: {
    start() {
      if (this.words && this.words.length > 0) {
        this.currentWord = this.words[this.wordIdx].split("");
        this.timeoutSpeed = this.speed;
        this.animate = setTimeout(this.type, this.timeoutSpeed);
      }
    },
    type() {
      if (this.currentWord.length > 0) {
        this.displayText.push(this.currentWord.shift());
        this.timeoutSpeed = this.speed;
        this.animate = setTimeout(this.type, this.timeoutSpeed);
      } else {
        this.blinkCursor = true;
        this.isWaitingNextWord = true;
        this.timeoutSpeed = this.nextWordInterval;
        this.animate = setTimeout(this.delete, this.timeoutSpeed);
      }
    },
    nextWord() {
      this.isWaitingNextWord = false;
      this.displayText = [];
      if (++this.wordIdx >= this.words.length) {
        this.wordIdx = 0;
      }
      this.blinkCursor = false;
      this.currentWord = this.words[this.wordIdx].split("");
      this.timeoutSpeed = this.speed;
      this.animate = setTimeout(this.type, this.timeoutSpeed);
    },
    delete() {
      if (this.displayText.length > 0) {
        this.blinkCursor = false;
        this.displayText.pop();
        this.timeoutSpeed = this.deleteSpeed;
        this.animate = setTimeout(this.delete, this.timeoutSpeed);
      } else {
        this.blinkCursor = true;
        this.isWaitingNextWord = false;
        this.timeoutSpeed = this.nextWordInterval;
        this.animate = setTimeout(this.nextWord, this.timeoutSpeed);
      }
    },
    shuffleArray(array) {
      for (var i = array.length - 1; i > 0; i--) {
        // Generate random number
        var j = Math.floor(Math.random() * (i + 1));

        var temp = array[i];
        array[i] = array[j];
        array[j] = temp;
      }

      return array;
    },
  },
};
</script>

<style lang="scss" scoped>
@keyframes blink-animation {
  to {
    visibility: hidden;
  }
}

.cursor {
  display: inline-block;
  margin-left: -5px;

  &--blink {
    animation: blink-animation 1s steps(2, start) infinite;
  }
}
</style>
