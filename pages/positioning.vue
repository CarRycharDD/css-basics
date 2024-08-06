<template>
  <div class="container">
    <div class="text-container">
      <div>
        <h1>Positioning</h1>
        <p>
          <b>Definition:</b> The <code>position</code> property in CSS is used
          to define how an element is positioned in the document.
        </p>
        <h3>Types of Positioning:</h3>
        <ul>
          <li>
            <p>
              <b>Static:</b> The default position; the element is positioned
              according to the normal flow of the document.
            </p>
          </li>
          <li>
            <p>
              <b>Relative:</b> The element is positioned relative to its normal
              position.
            </p>
          </li>
          <li>
            <p>
              <b>Absolute:</b> The element is positioned relative to the nearest
              positioned ancestor (other than static).
            </p>
          </li>
          <li>
            <p>
              <b>Fixed:</b> The element is positioned relative to the browser
              window.
            </p>
          </li>
        </ul>
        <h3>Best Practices:</h3>
        <ul>
          <li>
            <p>
              <b>Static:</b> Use for elements that do not require special
              positioning.
            </p>
          </li>
          <li>
            <p>
              <b>Relative:</b> Useful for slight adjustments or to establish a
              reference for absolute positioning.
            </p>
          </li>
          <li>
            <p>
              <b>Absolute:</b> Use for elements that need to be placed precisely
              in a specific location.
            </p>
          </li>
          <li>
            <p>
              <b>Fixed:</b> Ideal for elements that should remain in a fixed
              position relative to the viewport, such as headers or footers.
            </p>
          </li>
        </ul>
      </div>
    </div>
    <h3>Code:</h3>
    <div class="code-container">
      <h4>HTML:</h4>
      <pre><code class="language-html">
&lt;div class=&quot;positioning-container&quot;&gt;
  &lt;div class=&quot;static&quot;&gt;Static Position&lt;/div&gt;
  &lt;div class=&quot;relative&quot;&gt;Relative Position&lt;/div&gt;
  &lt;div class=&quot;absolute&quot;&gt;Absolute Position&lt;/div&gt;
  &lt;div class=&quot;fixed&quot;&gt;Fixed Position&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
      <h4>CSS:</h4>
      <pre><code class="language-css">
.positioning-container {
  position: relative;
  width: 300px;
  height: 300px;
  margin: 20px;
  padding: 10px;
  border: 1px solid black;
  background-color: lightyellow;
}

.static {
  position: static;
  background-color: lightblue;
  padding: 10px;
  margin-bottom: 5px;
}

.relative {
  position: relative;
  top: 10px;
  left: 20px;
  background-color: lightgreen;
  padding: 10px;
  margin-bottom: 5px;
}

.absolute {
  position: absolute;
  top: 40px;
  right: 10px;
  background-color: lightcoral;
  padding: 10px;
  margin-bottom: 5px;
}

.fixed {
  position: fixed;
  bottom: 10px;
  left: 10px;
  background-color: lightpink;
  padding: 10px;
}
        </code></pre>
    </div>
    <h3>Outcome:</h3>
    <div class="positioning-container">
      <div class="static">Static Position</div>
      <div class="relative">Relative Position</div>
      <div class="absolute">Absolute Position</div>
      <div class="fixed">Fixed Position</div>
    </div>
  </div>
</template>

<script setup>
import { ref, watch, onMounted, nextTick } from "vue";
import Prism from "prismjs";

const selectedSection = ref("positioning");

watch(selectedSection, async () => {
  await nextTick();
  Prism.highlightAll();
});

onMounted(async () => {
  await nextTick();
  Prism.highlightAll();
});
</script>

<style>
.button-container {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
  gap: 10px;
}
.btn {
  background-color: var(--color-blue);
  width: 150px;
}
.code-container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}

.container {
  width: 80vw;
}

.positioning-container {
  position: relative;
  width: 300px;
  height: 300px;
  margin: 20px;
  padding: 10px;
  border: 1px solid black;
  background-color: lightyellow;
}

.static {
  position: static;
  background-color: lightblue;
  padding: 10px;
  margin-bottom: 5px;
}

.relative {
  position: relative;
  top: 10px;
  left: 20px;
  background-color: lightgreen;
  padding: 10px;
  margin-bottom: 5px;
}

.absolute {
  position: absolute;
  top: 40px;
  right: 10px;
  background-color: lightcoral;
  padding: 10px;
  margin-bottom: 5px;
}

.fixed {
  position: fixed;
  bottom: 10px;
  left: 10px;
  background-color: lightpink;
  padding: 10px;
}
</style>
