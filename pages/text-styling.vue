<template>
  <div class="container">
    <div class="text-container">
      <h1>Text Styling</h1>
      <p>
        Text styling in CSS allows you to customize the appearance of text
        within your web pages, including properties like font, color, alignment,
        and spacing.
      </p>
      <div>
        <p>
          <b>Definition:</b> Text styling encompasses various CSS properties
          that alter the visual presentation of text, enhancing readability and
          aesthetic appeal.
        </p>
        <h3>Common Properties:</h3>
        <ul>
          <li>
            <p><b>font-family:</b> Specifies the font of the text.</p>
          </li>
          <li>
            <p><b>font-size:</b> Defines the size of the text.</p>
          </li>
          <li>
            <p><b>font-weight:</b> Sets the weight (boldness) of the text.</p>
          </li>
          <li>
            <p><b>color:</b> Sets the color of the text.</p>
          </li>
          <li>
            <p>
              <b>text-align:</b> Specifies the horizontal alignment of text.
            </p>
          </li>
          <li>
            <p>
              <b>text-decoration:</b> Adds decoration to text (like underlines).
            </p>
          </li>
          <li>
            <p><b>line-height:</b> Sets the space between lines of text.</p>
          </li>
          <li>
            <p><b>letter-spacing:</b> Adjusts the space between characters.</p>
          </li>
        </ul>
        <h3>Best Practices:</h3>
        <ul>
          <li>
            <p>
              <b>Readability:</b> Ensure text is easily readable by choosing
              appropriate font sizes, colors, and line heights.
            </p>
          </li>
          <li>
            <p>
              <b>Consistency:</b> Maintain consistent text styles across your
              site to provide a cohesive user experience.
            </p>
          </li>
          <li>
            <p>
              <b>Accessibility:</b> Use sufficient contrast between text and
              background colors to make your text accessible to all users.
            </p>
          </li>
        </ul>
      </div>
    </div>
    <h3>Code:</h3>
    <div class="code-container">
      <h4>HTML:</h4>
      <pre><code class="language-html">
&lt;div class=&quot;text-styling-container&quot;&gt;
  &lt;p class=&quot;text-styling&quot;&gt;This is a sample text.&lt;/p&gt;
  &lt;p class=&quot;text-styling text-example&quot;&gt;Another example of styled text.&lt;/p&gt;
&lt;/div&gt;
        </code></pre>
      <h4>CSS:</h4>
      <pre><code class="language-css">
.text-styling-container {
  width: 300px;
  margin: 20px;
  padding: 10px;
  background-color: lightyellow;
}
.text-styling {
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  color: #333;
  text-align: left;
  text-decoration: none;
  line-height: 1.5;
  letter-spacing: 0.5px;
}
.text-example {
  font-size: 18px;
  font-weight: 700;
  color: darkblue;
  text-align: center;
  text-decoration: underline;
}
        </code></pre>
    </div>
    <h3>Outcome:</h3>
    <div class="text-styling-container">
      <p class="text-styling">This is a sample text.</p>
      <p class="text-styling text-example">Another example of styled text.</p>
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

.text-styling-container {
  width: 300px;
  margin: 20px;
  padding: 10px;
  background-color: lightyellow;
}

.text-styling {
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-weight: 400;
  color: #333;
  text-align: left;
  text-decoration: none;
  line-height: 1.5;
  letter-spacing: 0.5px;
}

.text-example {
  font-size: 18px;
  font-weight: 700;
  color: darkblue;
  text-align: center;
  text-decoration: underline;
}
</style>
