<template>
  <div class="blog-main">
    <img
      width="1000"
      height="1000"
      class="lazyload"
      :src="img"
      :data-src="img"
      :alt="content.images[0].alt"
    />
    <!-- eslint-disable-next-line vue/no-v-html -->
    <div v-html="content.html"></div>
  </div>
</template>

<script>
import { Component, Vue, Prop } from 'vue-property-decorator'

@Component
export default class Blog extends Vue {
  @Prop({ type: Object, required: true })
  content

  get img() {
    const src = require(`static/${this.content.images[0].url}`)
    return src
  }
}
</script>

<style>
.blog-main {
  padding-right: 8px;
  padding-left: 8px;
  line-height: 150%;
}
.blog-main img {
  width: 100%;
  height: auto;
}
.blog-main a:link {
  color: #008cff;
}
.blog-main a:visited {
  color: #0b67a5;
}
.blog-main a:hover {
  color: #ff3c00;
}
.blog-main a:active {
  color: #ffa600;
}
</style>
