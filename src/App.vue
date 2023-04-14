<script setup lang="ts">
import TextHighlight from "./components/TextHighlight.vue";
import TextShadow from "./components/TextShadow.vue";
import TextSvgAnimation from "./components/TextSvgAnimation.vue";
import ShadowImage from "./components/ShadowImage.vue";
import SplitText from "./components/TextSplit.vue";
</script>

<template>
  <h1>「<a href="https://soupcurry-jack.com/" target="_blank">大阪発！本格札幌スープカレーJACK</a>」で用いられるCSS技術</h1>
  <section>
    <h2>text-shadow</h2>
    <TextShadow text="山道を登りながら、ふと考えた" />
  </section>
  <hr />
  <section>
    <h2>テキストのハイライト表現</h2>
    <TextHighlight text="山道を登りながら、ふと考えた" />
  </section>
  <hr />
  <section>
    <h2>一文字ずつ出てくる表現</h2>
    <SplitText text="EAT OR DIE" />
  </section>
  <hr />
  <section>
    <h2>
      内側のbox-shadow, 負のspread-radius<a
        href="https://developer.mozilla.org/ja/docs/Web/CSS/box-shadow"
        >（MDN - box-shadow）</a
      >
    </h2>
    <ShadowImage />
  </section>
  <hr />
  <section>
    <h2>SVGのラインアニメーション</h2>
    <TextSvgAnimation />
  </section>
</template>

<style scoped lang="scss">
section {
  padding: 32px 16px;
}
</style>
