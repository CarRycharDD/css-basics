<template>
  <div class="container">
    <div class="button-container">
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'gridBasics'"
      >
        Grid Basics
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'gridTemplate'"
      >
        Grid Template
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'gridGap'"
      >
        Grid Gap
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'gridArea'"
      >
        Grid Area
      </button>
    </div>

    <!-- Grid Basics Section -->
    <div v-if="selectedSection === 'gridBasics'">
      <div class="text-container">
        <div>
          <h1>Grid Basics</h1>
          <p>
            The <b>CSS Grid Layout</b> provides a two-dimensional grid-based
            layout system, optimized for responsive design.
          </p>
          <p>
            The <b>CSS Grid Layout</b> allows you to define rows and columns and
            place items into these grid cells.
          </p>
          <h3>Key Properties:</h3>
          <ul>
            <li>
              <b>display: grid;</b> - This property turns an element into a grid
              container.
            </li>
            <li>
              <b>grid-template-columns:</b> - Defines the columns of the grid
              with a space-separated list of values. For example,
              <code>grid-template-columns: 100px 1fr;</code> creates two
              columns, one with a fixed width of 100px and one that takes up the
              remaining space.
            </li>
            <li>
              <b>grid-template-rows:</b> - Similar to
              <code>grid-template-columns</code>, but for rows.
            </li>
            <li>
              <b>grid-gap:</b> - Sets the gaps (gutters) between rows and
              columns.
            </li>
            <li>
              <b>grid-template-areas:</b> - Defines a grid template by
              referencing the names of the grid areas which are specified with
              the <code>grid-area</code> property.
            </li>
            <li>
              <b>grid-area:</b> - Gives an item a name so that it can be
              referenced by <code>grid-template-areas</code>.
            </li>
          </ul>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;grid-container basic-grid&quot;&gt;
  &lt;div class=&quot;grid-item&quot;&gt;1&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;2&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;3&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;4&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;5&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;6&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.basic-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}

.grid-container {
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.grid-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  text-align: center;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Basic Grid:</b></p>
          <div class="grid-container basic-grid">
            <div class="grid-item">1</div>
            <div class="grid-item">2</div>
            <div class="grid-item">3</div>
            <div class="grid-item">4</div>
            <div class="grid-item">5</div>
            <div class="grid-item">6</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Grid Template Section -->
    <div v-if="selectedSection === 'gridTemplate'">
      <div class="text-container">
        <div>
          <h1>Grid Template</h1>
          <p>
            The <b>grid-template-columns</b> and
            <b>grid-template-rows</b> properties define the columns and rows of
            the grid.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;grid-container custom-grid-template&quot;&gt;
  &lt;div class=&quot;grid-item&quot;&gt;1&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;2&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;3&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;4&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;5&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;6&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.custom-grid-template {
  display: grid;
  grid-template-columns: 100px 1fr 2fr;
  grid-template-rows: 100px 200px;
  grid-gap: 10px;
}

.grid-container {
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.grid-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  text-align: center;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Custom Grid Template:</b></p>
          <div class="grid-container custom-grid-template">
            <div class="grid-item">1</div>
            <div class="grid-item">2</div>
            <div class="grid-item">3</div>
            <div class="grid-item">4</div>
            <div class="grid-item">5</div>
            <div class="grid-item">6</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Grid Gap Section -->
    <div v-if="selectedSection === 'gridGap'">
      <div class="text-container">
        <div>
          <h1>Grid Gap</h1>
          <p>
            The <b>grid-gap</b> property sets the gaps (gutters) between rows
            and columns.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;grid-container grid-gap&quot;&gt;
  &lt;div class=&quot;grid-item&quot;&gt;1&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;2&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;3&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;4&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;5&lt;/div&gt;
  &lt;div class=&quot;grid-item&quot;&gt;6&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.grid-gap {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}

.grid-container {
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.grid-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  text-align: center;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Grid with Gap:</b></p>
          <div class="grid-container grid-gap">
            <div class="grid-item">1</div>
            <div class="grid-item">2</div>
            <div class="grid-item">3</div>
            <div class="grid-item">4</div>
            <div class="grid-item">5</div>
            <div class="grid-item">6</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Grid Area Section -->
    <div v-if="selectedSection === 'gridArea'">
      <div class="text-container">
        <div>
          <h1>Grid Area</h1>
          <p>
            The <b>grid-area</b> property allows you to place an item in a
            specific area of the grid defined by grid-template-areas.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;grid-container grid-area&quot;&gt;
  &lt;div class=&quot;grid-item header&quot;&gt;Header&lt;/div&gt;
  &lt;div class=&quot;grid-item sidebar&quot;&gt;Sidebar&lt;/div&gt;
  &lt;div class=&quot;grid-item content&quot;&gt;Content&lt;/div&gt;
  &lt;div class=&quot;grid-item footer&quot;&gt;Footer&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.grid-area {
  display: grid;
  grid-template-areas: 
    'header header header'
    'sidebar content content'
    'footer footer footer';
  grid-gap: 10px;
}

.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.content {
  grid-area: content;
}

.footer {
  grid-area: footer;
}

.grid-container {
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.grid-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  text-align: center;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Grid with Areas:</b></p>
          <div class="grid-container grid-area">
            <div class="grid-item header">Header</div>
            <div class="grid-item sidebar">Sidebar</div>
            <div class="grid-item content">Content</div>
            <div class="grid-item footer">Footer</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import Prism from "prismjs";

const selectedSection = ref("gridBasics");
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
  margin-bottom: 20px;
  background-color: #f4f4f4;
  padding: 10px;
  border-radius: 5px;
}

.container {
  width: 80vw;
}

.text-container {
  margin-bottom: 20px;
}

.grid-container {
  display: grid;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.grid-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  text-align: center;
}

.basic-grid {
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}

.custom-grid-template {
  grid-template-columns: 100px 1fr 2fr;
  grid-template-rows: 100px 200px;
  grid-gap: 10px;
}

.grid-gap {
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}

.grid-area {
  grid-template-areas:
    "header header header"
    "sidebar content content"
    "footer footer footer";
  grid-gap: 10px;
}

.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.content {
  grid-area: content;
}

.footer {
  grid-area: footer;
}
</style>
