<template>
  <div class="hello">{{msg}}</div>
</template>

<script>
const aSymbol = Symbol("test symbol");

export default {
  name: "HelloWorld",
  props: {
    msg: { type: [String, Symbol], default: aSymbol }
  },
  data() {
    return {
      dataMsg: this.msg !== aSymbol ? this.msg : "Hello World"
    };
  }
};
</script>
