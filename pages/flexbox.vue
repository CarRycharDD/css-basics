<template>
  <div class="container">
    <div class="button-container">
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'flexboxBasics'"
      >
        Flexbox Basics
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'flexDirection'"
      >
        Flex Direction
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'justifyContent'"
      >
        Justify Content
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'alignItems'"
      >
        Align Items
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'flexWrap'"
      >
        Flex Wrap
      </button>
    </div>

    <!-- Flexbox Basics Section -->
    <div v-if="selectedSection === 'flexboxBasics'">
      <div class="text-container">
        <div>
          <h1>Flexbox Basics</h1>
          <p>
            The <b>flexbox</b> layout model provides a more efficient way to
            layout, align, and distribute space among items in a container, even
            when their size is unknown or dynamic.
          </p>

          <p>
            <b>Definition:</b> The Flexbox layout model allows you to design a
            flexible responsive layout structure without using float or
            positioning.
          </p>
          <h3>Key Properties:</h3>
          <ul>
            <li>
              <p>
                <b>display: flex;</b> Defines a flex container and enables a
                flex context for all its direct children.
              </p>
            </li>
            <li>
              <p>
                <b>flex-direction:</b> Defines the direction of the main axis
                (row, row-reverse, column, column-reverse).
              </p>
            </li>
            <li>
              <p>
                <b>justify-content:</b> Aligns items along the main axis
                (flex-start, flex-end, center, space-between, space-around,
                space-evenly).
              </p>
            </li>
            <li>
              <p>
                <b>align-items:</b> Aligns items along the cross axis
                (flex-start, flex-end, center, baseline, stretch).
              </p>
            </li>
            <li>
              <p>
                <b>flex-wrap:</b> Specifies whether the flex items should wrap
                or not (nowrap, wrap, wrap-reverse).
              </p>
            </li>
            <li>
              <p>
                <b>flex-grow:</b> Defines the ability for a flex item to grow if
                necessary.
              </p>
            </li>
            <li>
              <p>
                <b>flex-shrink:</b> Defines the ability for a flex item to
                shrink if necessary.
              </p>
            </li>
            <li>
              <p>
                <b>flex-basis:</b> Defines the default size of an element before
                the remaining space is distributed.
              </p>
            </li>
          </ul>
          <h3>Best Practices:</h3>
          <ul>
            <li>
              <p>
                <b>Responsive Design:</b> Use Flexbox for responsive design to
                easily manage layout changes across different screen sizes.
              </p>
            </li>
            <li>
              <p>
                <b>Alignment:</b> Utilize the alignment properties to achieve
                precise control over spacing and alignment of flex items.
              </p>
            </li>
            <li>
              <p>
                <b>Flexibility:</b> Take advantage of the flexibility offered by
                Flexbox to create complex layouts with minimal code.
              </p>
            </li>
          </ul>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;flex-container&quot;&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.flex-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.flex-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  flex-grow: 1;
}
        </code></pre>
      </div>
      <h3>Outcome:</h3>
      <div class="flex-container">
        <div class="flex-item">Item 1</div>
        <div class="flex-item">Item 2</div>
        <div class="flex-item">Item 3</div>
      </div>
    </div>

    <!-- Flex Direction Section -->
    <div v-if="selectedSection === 'flexDirection'">
      <div class="text-container">
        <h1>Flex Direction</h1>
        <p>
          <b>flex-direction</b> specifies the direction of the flexible items.
          It is a key property for controlling the layout of items in a flex
          container.
        </p>
        <h3>Code:</h3>
        <div class="code-container">
          <h4>HTML:</h4>
          <pre><code class="language-html">
&lt;!-- Row --&gt;
&lt;div class=&quot;flex-container row&quot;&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Row-Reverse --&gt;
&lt;div class=&quot;flex-container row-reverse&quot;&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Column --&gt;
&lt;div class=&quot;flex-container column&quot;&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Column-Reverse --&gt;
&lt;div class=&quot;flex-container column-reverse&quot;&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
          <h4>CSS:</h4>
          <pre><code class="language-css">
.flex-container {
  display: flex;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.flex-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  flex-grow: 1;
}

.flex-container.row {
  flex-direction: row;
}

.flex-container.row-reverse {
  flex-direction: row-reverse;
}

.flex-container.column {
  flex-direction: column;
}

.flex-container.column-reverse {
  flex-direction: column-reverse;
}
        </code></pre>
        </div>
        <div>
          <h3>Outcome:</h3>
          <ul>
            <li>
              <p><b>Row:</b></p>
              <div class="flex-container row-original">
                <div class="flex-item">Item 1</div>
                <div class="flex-item">Item 2</div>
                <div class="flex-item">Item 3</div>
              </div>
            </li>
            <li>
              <p><b>Row-Reverse:</b></p>
              <div class="flex-container row-reverse">
                <div class="flex-item">Item 1</div>
                <div class="flex-item">Item 2</div>
                <div class="flex-item">Item 3</div>
              </div>
            </li>
            <li>
              <p><b>Column:</b></p>
              <div class="flex-container column">
                <div class="flex-item">Item 1</div>
                <div class="flex-item">Item 2</div>
                <div class="flex-item">Item 3</div>
              </div>
            </li>
            <li>
              <p><b>Column-Reverse:</b></p>
              <div class="flex-container column-reverse">
                <div class="flex-item">Item 1</div>
                <div class="flex-item">Item 2</div>
                <div class="flex-item">Item 3</div>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Justify Content Section -->
    <div v-if="selectedSection === 'justifyContent'">
      <div class="text-container">
        <div>
          <h1>Justify Content</h1>
          <p>
            <b>justify-content</b> aligns the flex items along the main axis of
            the current line of the flex container.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;!-- Flex Start --&gt;
&lt;div class=&quot;flex-container justify-start&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Flex End --&gt;
&lt;div class=&quot;flex-container justify-end&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Center --&gt;
&lt;div class=&quot;flex-container justify-center&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Space Between --&gt;
&lt;div class=&quot;flex-container justify-between&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Space Around --&gt;
&lt;div class=&quot;flex-container justify-around&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Space Evenly --&gt;
&lt;div class=&quot;flex-container justify-evenly&quot;&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.flex-container {
  display: flex;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.flex-item-fixed {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  width: 10%;
  height: 80%;
}

.flex-container.justify-start {
  justify-content: flex-start;
}

.flex-container.justify-end {
  justify-content: flex-end;
}

.flex-container.justify-center {
  justify-content: center;
}

.flex-container.justify-between {
  justify-content: space-between;
}

.flex-container.justify-around {
  justify-content: space-around;
}

.flex-container.justify-evenly {
  justify-content: space-evenly;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Flex Start:</b></p>
          <div class="flex-container justify-start">
            <div class="flex-item-fixed">Item 1</div>
            <div class="flex-item-fixed">Item 2</div>
            <div class="flex-item-fixed">Item 3</div>
          </div>
        </li>
        <li>
          <p><b>Flex End:</b></p>
          <div class="flex-container justify-end">
            <div class="flex-item-fixed">Item 1</div>
            <div class="flex-item-fixed">Item 2</div>
            <div class="flex-item-fixed">Item 3</div>
          </div>
        </li>
        <li>
          <p><b>Center:</b></p>
          <div class="flex-container justify-center">
            <div class="flex-item-fixed">Item 1</div>
            <div class="flex-item-fixed">Item 2</div>
            <div class="flex-item-fixed">Item 3</div>
          </div>
        </li>
        <li>
          <p><b>Space Between:</b></p>
          <div class="flex-container justify-between">
            <div class="flex-item-fixed">Item 1</div>
            <div class="flex-item-fixed">Item 2</div>
            <div class="flex-item-fixed">Item 3</div>
          </div>
        </li>
        <li>
          <p><b>Space Around:</b></p>
          <div class="flex-container justify-around">
            <div class="flex-item-fixed">Item 1</div>
            <div class="flex-item-fixed">Item 2</div>
            <div class="flex-item-fixed">Item 3</div>
          </div>
        </li>
        <li>
          <p><b>Space Evenly:</b></p>
          <div class="flex-container justify-evenly">
            <div class="flex-item">Item 1</div>
            <div class="flex-item">Item 2</div>
            <div class="flex-item">Item 3</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Align Items Section -->
    <div v-if="selectedSection === 'alignItems'">
      <div class="text-container">
        <div>
          <h1>Align Items</h1>
          <p>
            <b>align-items</b> aligns the flex items along the cross axis of the
            flex container.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;!-- Flex Start --&gt;
&lt;div class=&quot;flex-container align-start&quot;&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item short&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Flex End --&gt;
&lt;div class=&quot;flex-container align-end&quot;&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item short&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Center --&gt;
&lt;div class=&quot;flex-container align-center&quot;&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item short&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Baseline --&gt;
&lt;div class=&quot;flex-container align-baseline&quot;&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item short&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Stretch --&gt;
&lt;div class=&quot;flex-container align-stretch&quot;&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item short&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item tall&quot;&gt;Item 3&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.flex-container {
  display: flex;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.flex-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  flex-grow: 1;
}

.flex-item.tall {
  height: 100px;
}

.medium {
  height: 75px;
}

.flex-item.short {
  height: 50px;
}

.flex-container.align-start {
  align-items: flex-start;
}

.flex-container.align-end {
  align-items: flex-end;
}

.flex-container.align-center {
  align-items: center;
}

.flex-container.align-baseline {
  align-items: baseline;
}

.flex-container.align-stretch {
  align-items: stretch;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p>
            <b>Flex Start:</b> The flex-start value aligns the flex items at the
            top of the container.
          </p>
          <div class="flex-container align-start">
            <div class="flex-item tall">Item 1</div>
            <div class="flex-item short">Item 2</div>
            <div class="flex-item medium">Item 3</div>
          </div>
        </li>
        <li>
          <p>
            <b>Flex End:</b> The flex-end value aligns the flex items at the
            bottom of the container.
          </p>
          <div class="flex-container align-end">
            <div class="flex-item tall">Item 1</div>
            <div class="flex-item short">Item 2</div>
            <div class="flex-item medium">Item 3</div>
          </div>
        </li>
        <li>
          <p>
            <b>Center:</b> The center value aligns the flex items in the middle
            of the container.
          </p>
          <div class="flex-container align-center">
            <div class="flex-item tall">Item 1</div>
            <div class="flex-item short">Item 2</div>
            <div class="flex-item medium">Item 3</div>
          </div>
        </li>
        <li>
          <p>
            <b>Baseline:</b> The baseline value aligns the flex items such as
            their baselines aligns.
          </p>
          <div class="flex-container align-baseline">
            <div class="flex-item tall">Item 1</div>
            <div class="flex-item short">Item 2</div>
            <div class="flex-item medium">Item 3</div>
          </div>
        </li>
        <li>
          <p>
            <b>Stretch:</b> The stretch value stretches the flex items to fill
            the container (this is default)
          </p>
          <div class="flex-container align-stretch">
            <div class="flex-item">Item 1</div>
            <div class="flex-item">Item 2</div>
            <div class="flex-item">Item 3</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Flex Wrap Section -->
    <div v-if="selectedSection === 'flexWrap'">
      <div class="text-container">
        <div>
          <h1>Flex Wrap</h1>
          <p>
            <b>flex-wrap</b> specifies whether the flex items should wrap or
            not, if necessary.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;!-- Nowrap --&gt;
&lt;div class=&quot;flex-container nowrap&quot;&gt;
  &lt;div class=&quot;flex-item fixed-width&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item fixed-width&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item fixed-width&quot;&gt;Item 3&lt;/div&gt;
  &lt;div class=&quot;flex-item fixed-width&quot;&gt;Item 4&lt;/div&gt;
  &lt;div class=&quot;flex-item fixed-width&quot;&gt;Item 5&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Wrap --&gt;
&lt;div class=&quot;flex-container wrap&quot;&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 3&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 4&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 5&lt;/div&gt;
&lt;/div&gt;
&lt;!-- Wrap-Reverse --&gt;
&lt;div class=&quot;flex-container wrap-reverse&quot;&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 1&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 2&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 3&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 4&lt;/div&gt;
  &lt;div class=&quot;flex-item-fixed fixed-width&quot;&gt;Item 5&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.flex-container {
  display: flex;
  background-color: lightgrey;
  padding: 10px;
  border: 1px solid black;
}

.flex-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  flex-grow: 1;
  flex-basis: 200px;
}

.flex-item-fixed {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  width: 10%;
  height: 80%;
}

.fixed-width {
  width: 100px;
}

.flex-container.nowrap {
  flex-wrap: nowrap;
}

.flex-container.wrap {
  flex-wrap: wrap;
}

.flex-container.wrap-reverse {
  flex-wrap: wrap-reverse;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p>
            <b>Nowrap:</b> The nowrap value specifies that the flex items will
            not wrap (this is default).
          </p>
          <div class="flex-container narrow nowrap">
            <div class="flex-item fixed-width" width>Item 1</div>
            <div class="flex-item fixed-width" width>Item 2</div>
            <div class="flex-item fixed-width" width>Item 3</div>
            <div class="flex-item fixed-width" width>Item 4</div>
            <div class="flex-item fixed-width" width>Item 5</div>
          </div>
        </li>
        <li>
          <p>
            <b>Wrap:</b> The wrap value specifies that the flex items will wrap
            if necessary.
          </p>
          <div class="flex-container narrow wrap">
            <div class="flex-item-fixed fixed-width" width>Item 1</div>
            <div class="flex-item-fixed fixed-width" width>Item 2</div>
            <div class="flex-item-fixed fixed-width" width>Item 3</div>
            <div class="flex-item-fixed fixed-width" width>Item 4</div>
            <div class="flex-item-fixed fixed-width" width>Item 5</div>
          </div>
        </li>
        <li>
          <p>
            <b>Wrap-Reverse:</b> The wrap-reverse value specifies that the
            flexible items will wrap if necessary, in reverse order.
          </p>
          <div class="flex-container narrow wrap-reverse">
            <div class="flex-item-fixed fixed-width" width>Item 1</div>
            <div class="flex-item-fixed fixed-width" width>Item 2</div>
            <div class="flex-item-fixed fixed-width" width>Item 3</div>
            <div class="flex-item-fixed fixed-width" width>Item 4</div>
            <div class="flex-item-fixed fixed-width" width>Item 5</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import Prism from "prismjs";

const selectedSection = ref("flexboxBasics");
watch(selectedSection, async () => {
  await nextTick();

  Prism.highlightAll();
});
onMounted(async () => {
  await nextTick();
  Prism.highlightAll();
});
</script>

<style scoped>
.container {
  width: 80vw;
}

.button-container {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

.btn {
  background-color: var(--color-blue);
  width: 150px;
}

.text-container {
  margin-bottom: 20px;
}

.code-container {
  margin-bottom: 20px;
  background-color: #f4f4f4;
  padding: 10px;
  border-radius: 5px;
}

.flex-container {
  display: flex;
  background-color: lightgrey;
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid black;
}

.flex-item {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  flex-grow: 1;
}

.flex-item-fixed {
  background-color: lightblue;
  padding: 20px;
  margin: 5px;
  border: 1px solid darkblue;
  width: 10%;
  height: 80%;
}
.tall {
  height: 100px;
}

.short {
  height: 50px;
}

.medium {
  height: 75px;
}

.narrow {
  width: 50%;
}

.fixed-width {
  width: 100px;
}
.flex-container.row-original {
  flex-direction: row;
}

.flex-container.row-reverse {
  flex-direction: row-reverse;
}

.flex-container.column {
  flex-direction: column;
}

.flex-container.column-reverse {
  flex-direction: column-reverse;
}

.flex-container.justify-start {
  justify-content: flex-start;
}

.flex-container.justify-end {
  justify-content: flex-end;
}

.flex-container.justify-center {
  justify-content: center;
}

.flex-container.justify-between {
  justify-content: space-between;
}

.flex-container.justify-around {
  justify-content: space-around;
}

.flex-container.justify-evenly {
  justify-content: space-evenly;
}

.flex-container.align-start {
  align-items: flex-start;
}

.flex-container.align-end {
  align-items: flex-end;
}

.flex-container.align-center {
  align-items: center;
}

.flex-container.align-baseline {
  align-items: baseline;
}

.flex-container.align-stretch {
  align-items: stretch;
}

.flex-container.nowrap {
  flex-wrap: nowrap;
}

.flex-container.wrap {
  flex-wrap: wrap;
}

.flex-container.wrap-reverse {
  flex-wrap: wrap-reverse;
}
</style>
