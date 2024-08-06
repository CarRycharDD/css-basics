<template>
  <div class="container">
    <p>
      The <b>box model</b> describes the rectangular boxes generated for
      elements in the document tree and is crucial for layout and design.
    </p>
    <div class="text-container">
      <div>
        <h1>Box Model</h1>
        <p>
          <b>Definition:</b> The CSS box model is essentially a box that wraps
          around every HTML element. It consists of: margins, borders, padding,
          and the actual content.
        </p>
        <h3>Components:</h3>
        <ul>
          <li>
            <p>
              <b>Content:</b> The content of the box, where text and images
              appear.
            </p>
          </li>
          <li>
            <p>
              <b>Padding:</b> Clears an area around the content. The padding is
              transparent.
            </p>
          </li>
          <li>
            <p>
              <b>Border:</b> A border that goes around the padding (if any) and
              content.
            </p>
          </li>
          <li>
            <p>
              <b>Margin:</b> Clears an area outside the border. The margin is
              transparent.
            </p>
          </li>
        </ul>
        <h3>Best Practices:</h3>
        <ul>
          <li>
            <p>
              <b>Box-Sizing:</b> Use the <code>box-sizing</code> property to
              include padding and border in the element's total width and
              height.
            </p>
          </li>
          <li>
            <p>
              <b>Consistent Layouts:</b> Apply consistent padding and margins to
              maintain a uniform layout.
            </p>
          </li>
        </ul>
      </div>
    </div>
    <h3>Code:</h3>
    <div class="code-container">
      <div>
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div style=&quot;display: flex; justify-content: space-evenly&quot;&gt;
  &lt;div class=&quot;content-container content-box&quot;&gt;Content box&lt;/div&gt;
  &lt;div class=&quot;content-container border-box&quot;&gt;Border box&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
      </div>
      <div>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.content-container {
  width: 160px;
  height: 80px;
  padding: 20px;
  border: 8px solid red;
  background: yellow;
}

.content-box {
  box-sizing: content-box;
  /* Total width: 160px + (2 * 20px) + (2 * 8px) = 216px
      Total height: 80px + (2 * 20px) + (2 * 8px) = 136px
      Content box width: 160px
      Content box height: 80px */
}

.border-box {
  box-sizing: border-box;
  /* Total width: 160px
      Total height: 80px
      Content box width: 160px - (2 * 20px) - (2 * 8px) = 104px
      Content box height: 80px - (2 * 20px) - (2 * 8px) = 24px */
}
        </code></pre>
      </div>
    </div>
    <h3>Outcome:</h3>
    <div style="display: flex; justify-content: space-evenly">
      <div class="content-container content-box">Content box</div>
      <br />
      <div class="content-container border-box">Border box</div>
    </div>
  </div>
</template>

<script setup>
import Prism from "prismjs";

onMounted(async () => {
  await nextTick();
  Prism.highlightAll();
});
</script>

<style>
.code-container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.container {
  width: 80vw;
}

.content-container {
  width: 160px;
  height: 80px;
  padding: 20px;
  border: 8px solid red;
  background: yellow;
}

.content-box {
  box-sizing: content-box;
}

.border-box {
  box-sizing: border-box;
}
</style>
