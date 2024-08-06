<template>
  <div class="container">
    <div class="button-container">
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'variablesBasics'"
      >
        Variables Basics
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'variablesUsage'"
      >
        Variable Usage
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'variablesTheming'"
      >
        Theming with Variables
      </button>
    </div>

    <!-- Variables Basics Section -->
    <div v-if="selectedSection === 'variablesBasics'">
      <div class="text-container">
        <div>
          <h1>Variables Basics</h1>
          <p>
            <b>CSS Variables</b> (Custom Properties) are entities defined by CSS
            authors that contain specific values to be reused throughout a
            document.
          </p>
          <p>
            They are defined within a <code>:root</code> or any other CSS
            selector and can be accessed using the <code>var()</code> function.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;box&quot;&gt;&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
:root {
  --box-size: 100px;
  --box-color: lightblue;
}

.box {
  width: var(--box-size);
  height: var(--box-size);
  background-color: var(--box-color);
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Basic Variables:</b></p>
          <div class="box"></div>
        </li>
      </ul>
    </div>

    <!-- Variables Usage Section -->
    <div v-if="selectedSection === 'variablesUsage'">
      <div class="text-container">
        <div>
          <h1>Variable Usage</h1>
          <p>
            CSS variables can be used to define common styles and allow for
            easier updates across a stylesheet.
          </p>
          <p>
            You can use variables within any CSS property and they can also
            inherit their values from parent elements.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div&gt;
  &lt;div class=&quot;box&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
&lt;div class=&quot;box-container&quot;&gt;
  &lt;div class=&quot;box&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
:root {
  --box-size: 100px;
  --box-color: lightblue;
}

.container {
  --box-size: 150px; /* Overriding variable for container */
}

.box {
  width: var(--box-size);
  height: var(--box-size);
  background-color: var(--box-color);
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Variable Usage:</b></p>
          <div>
            <div class="box"></div>
          </div>
          <div class="box-container">
            <div class="box"></div>
          </div>
        </li>
      </ul>
    </div>

    <!-- Variables Theming Section -->
    <div v-if="selectedSection === 'variablesTheming'">
      <div class="text-container">
        <div>
          <h1>Theming with Variables</h1>
          <p>
            CSS variables are ideal for theming. You can define color schemes,
            spacing, fonts, and more using variables, making it easier to switch
            themes across a site.
          </p>
        </div>
      </div>
      <h3>Code:</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;theme-light&quot;&gt;
  &lt;div class=&quot;box&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
&lt;div class=&quot;theme-dark&quot;&gt;
  &lt;div class=&quot;box&quot;&gt;&lt;/div&gt;
&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
:root {
  --box-color: lightblue;
}

.theme-dark {
  --box-color: darkgray;
}

.theme-light {
  --box-color: pink;
}

.box {
  width: 100px;
  height: 100px;
  background-color: var(--box-color);
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Original:</b></p>
          <div style="margin-bottom: 15px">
            <div class="box"></div>
          </div>
        </li>
        <li>
          <p><b>Theme Light:</b></p>
          <div class="theme-light" style="margin-bottom: 15px">
            <div class="box"></div>
          </div>
        </li>
        <li>
          <p><b>Theme Dark:</b></p>
          <div class="theme-dark">
            <div class="box"></div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { ref, watch, nextTick, onMounted } from "vue";
import Prism from "prismjs";

const selectedSection = ref("variablesBasics");

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
.box,
.color-box,
.multi-box,
.responsive-box,
.dynamic-box {
  margin-top: 20px;
}
.text-container {
  margin-bottom: 20px;
}
.box {
  width: var(--box-size);
  height: var(--box-size);
  background-color: var(--box-color, lightblue);
}
.box-container {
  --box-size: 150px;
}
.theme-dark {
  --box-color: darkgray;
}
.theme-light {
  --box-color: pink;
}
body {
  background-color: var(--background-color, white);
}
.responsive-box {
  width: var(--box-width);
  height: var(--box-height);
  background-color: lightcoral;
}
.dynamic-box {
  width: 100px;
  height: 100px;
  background-color: var(--box-background);
}
</style>
