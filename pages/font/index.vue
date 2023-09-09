<template>
  <div>
    <header class="head">
      Use the Bits Symbol font in your project
    </header>
    <div class="text">
      👇️Add this <code>script</code> tag to your document👇️<br>
      <code class="tag">
        &lt;script src="https://bits.name/bitsSymbol.js"&gt;&lt;/script&gt;
      </code><br>
      Or <a href="/FontKit.zip" class="download">download the zip</a> and <code><em>src</em></code> the files locally
    </div>
  </div>
    <div class="icons">
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol"></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol_tilt"></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol_tilt"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol_noLine"></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol_noLine"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol_tilt_noLine"></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol_tilt_noLine"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol-Coin">
          <span class="path1"></span><span class="path2"></span>
          <span class="path3"></span><span class="path4"></span>
          <span class="path5"></span><span class="path6"></span>
          <span class="path7"></span></span>
        <div class="code">
          &lt;i class="Bits-Symbol-Coin"&gt;&lt;/i&gt;
        </div>
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol-Coin_tilt">
          <span class="path1"></span><span class="path2"></span>
          <span class="path3"></span><span class="path4"></span>
          <span class="path5"></span><span class="path6"></span>
          <span class="path7"></span></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol-Coin_tilt"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol-Coin_noLine">
            <span class="path1"></span><span class="path2"></span>
            <span class="path3"></span><span class="path4"></span>
            <span class="path5"></span><span class="path6"></span>
            <span class="path7"></span></span>
        </div>
        <div class="code">
          &lt;i class="Bits-Symbol-Coin_noLine"&gt;&lt;/i&gt;
        </div>
      </div>
      <div class="glyph fs1">
        <div class="clearfix bshadow0 pbs">
          <span class="icon-Bits-Symbol-Coin_tilt_noLine">
          <span class="path1"></span><span class="path2"></span>
          <span class="path3"></span><span class="path4"></span>
          <span class="path5"></span><span class="path6"></span>
          <span class="path7"></span></span>
        <div class="code">
          &lt;i class="Bits-Symbol-Coin_tilt_noLine"&gt;&lt;/i&gt;
        </div>
        </div>
      </div>
    </div>
</template>

<script setup lang="ts">
import { onMounted } from "vue";

onMounted(() => {
  const link = document.createElement("link");
  link.rel = "stylesheet";
  link.href = "/font/style.css";
  document.head.appendChild(link);
});
</script>

<style scoped>
.head {
  @apply text-center mt-20 mb-10 text-3xl
}

.text {
  @apply text-center
}

.tag {
  @apply italic font-bold;
}

.icons {
  @apply text-center text-4xl mt-10
}

.code {
  @apply text-sm mb-10
}

.download {
  @apply text-blue-900 mb-0;
}

.download:hover {
  @apply underline cursor-pointer
}
</style>
