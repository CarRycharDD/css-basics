<template>
  <div class="container">
    <div class="button-container">
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'blockElements'"
      >
        Block Elements
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'inlineElements'"
      >
        Inline Elements
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'inlineBlockElements'"
      >
        Inline-Block Elements
      </button>
    </div>
    <p>
      The <b>display</b> property specifies the display behavior (the type of
      rendering box) of an element.
    </p>
    <div v-if="selectedSection == 'blockElements'">
      <div class="text-container">
        <div>
          <h1>Block Elements</h1>

          <p>
            <b>Definition:</b> Block-level elements start on a new line, take up
            the full width available, and can have width and height set.
          </p>
          <p>
            <b>Common Block Elements:</b> &lt;div&gt;, &lt;p&gt;, &lt;h1&gt;,
            &lt;section&gt;, &lt;header&gt;, &lt;footer&gt;.
          </p>
          <h3>Use Cases:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>Structural Layouts:</b> Use block elements for structural
                elements like headers, footers, sections, articles, and
                dividers.
              </p>
            </li>
            <li>
              <p>
                <b>Containers:</b> Use for containers that group other elements
                and need to control their width and height.
              </p>
            </li>
          </ul>
          <h3>Best Practices:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>New Lines:</b> Remember that block elements will start on a
                new line. This can be beneficial for clear separation of content
                sections.
              </p>
            </li>
            <li>
              <p>
                <b>Full Width:</b> Utilize the full-width behavior for elements
                that should span the entire width of their parent container.
              </p>
            </li>
            <li>
              <p>
                <b>Margin and Padding:</b> Apply margins and paddings to control
                spacing between block elements.
              </p>
            </li>
          </ul>
          <p></p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;element-container&quot;&gt;
  &lt;div class=&quot;block&quot;&gt;Block Element 1&lt;/div&gt;
  &lt;div class=&quot;block&quot;&gt;Block Element 2&lt;/div&gt;
&lt;/div&gt;
      </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.block {
  display: block;
  background-color: lightblue;
  margin-bottom: 3px;
}
      </code></pre>
      </div>
      <h3>Outcome:</h3>
      <div class="element-container">
        <div class="block">Block Element 1</div>
        <div class="block">Block Element 2</div>
      </div>
    </div>
    <div v-if="selectedSection == 'inlineElements'">
      <div class="text-container">
        <div>
          <h1>Inline Elements</h1>
          <p>
            <b>Definition:</b> Inline elements do not start on a new line and
            only take up as much width as necessary. Width and height properties
            do not apply.
          </p>
          <p>
            <b>Common Inline Elements:</b> &lt;span&gt;, &lt;a&gt;,
            &lt;strong&gt;, &lt;em&gt;.
          </p>
          <h3>Use Cases:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>Text Formatting:</b> Use inline elements within paragraphs or
                other text containers for styling specific parts of text.
              </p>
            </li>
            <li>
              <p>
                <b>Links:</b> Use inline elements for links within text or lists
              </p>
            </li>
          </ul>
          <h3>Best Practices:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>No Width/Height:</b> Avoid trying to set width and height on
                inline elements as they will not apply.
              </p>
            </li>
            <li>
              <p>
                <b>Flow with Text:</b> Utilize inline elements to flow naturally
                with text without breaking the line.
              </p>
            </li>
            <li>
              <p>
                <b>Spacing:</b> Use margin and padding sparingly as they can
                disrupt the inline flow.
              </p>
            </li>
          </ul>
          <p></p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;element-container&quot;&gt;
  &lt;span class=&quot;inline&quot;&gt;Inline Element 1&lt;/span&gt;
  &lt;span class=&quot;inline&quot;&gt;Inline Element 2&lt;/span&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.inline {
  display: inline;
  background-color: lightgreen;
  margin-right: 3px;
}
        </code></pre>
      </div>
      <h3>Outcome:</h3>
      <div class="element-container">
        <span class="inline">Inline Element 1</span>
        <span class="inline">Inline Element 2</span>
      </div>
    </div>
    <div v-if="selectedSection == 'inlineBlockElements'">
      <div class="text-container">
        <div>
          <h1>Inline-block Elements</h1>
          <p>
            <b>Definition:</b> Inline-block elements are like inline elements,
            but they respect width and height properties.
          </p>
          <p>
            <b>Common Uses:</b> Often used for layout purposes where you want
            elements to flow inline but also have the ability to set width and
            height.
          </p>
          <h3>Use Cases:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>Layouts:</b> Use inline-block for elements that need to be
                inline but also need to respect width and height settings, such
                as buttons, navigation links, or grid items.
              </p>
            </li>
            <li>
              <p>
                <b>Alignment:</b> Useful for aligning multiple items
                horizontally while allowing for dimensions.
              </p>
            </li>
          </ul>
          <h3>Best Practices:</h3>
          <p></p>
          <ul>
            <li>
              <p>
                <b>Horizontal Flow:</b> Use inline-block elements for items that
                should appear next to each other, but where you need control
                over their dimensions.
              </p>
            </li>
            <li>
              <p>
                <b>Whitespace:</b> Be aware of the whitespace issue in HTML
                where spaces between inline-block elements can cause unexpected
                gaps. This can be managed with CSS tricks like setting font-size
                to 0 on the parent container or removing the spaces in HTML.
              </p>
            </li>
            <li>
              <p>
                <b>Consistency:</b> Maintain consistent padding, margin, and
                border settings for inline-block elements to ensure a uniform
                appearance.
              </p>
            </li>
          </ul>
          <p></p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;element-container&quot;&gt;
  &lt;div class=&quot;inline-block&quot;&gt;Inline-Block 1&lt;/div&gt;
  &lt;div class=&quot;inline-block&quot;&gt;Inline-Block 2&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.inline-block {
  display: inline-block;
  background-color: lightcoral;
  width: 100px;
  height: 100px;
  margin-right: 3px;
}
        </code></pre>
      </div>
      <h3>Outcome:</h3>
      <div class="element-container">
        <div class="inline-block">Inline-Block 1</div>
        <div class="inline-block">Inline-Block 2</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Prism from "prismjs";

const selectedSection = ref("blockElements");
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

.element-container {
  margin-bottom: 20px;
}

.block {
  display: block;
  background-color: lightblue;
  margin-bottom: 3px;
}

.inline {
  display: inline;
  background-color: lightgreen;
  margin-right: 3px;
}

.inline-block {
  display: inline-block;
  background-color: lightcoral;
  width: 100px;
  height: 100px;
  margin-right: 3px;
}
</style>
