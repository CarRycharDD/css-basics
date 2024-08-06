<template>
  <div class="container">
    <div class="button-container">
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'transitionBasics'"
      >
        Transition Basics
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'transitionProperties'"
      >
        Transition Properties
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'transitionTiming'"
      >
        Transition Timing
      </button>
      <button
        type="button"
        class="btn btn-dark"
        @click="selectedSection = 'transitionExamples'"
      >
        Transition Examples
      </button>
    </div>

    <!-- Transition Basics Section -->
    <div v-if="selectedSection === 'transitionBasics'">
      <div class="text-container">
        <div>
          <h1>Transition Basics</h1>
          <p>
            CSS transitions provide a way to control the speed of animation
            changes to CSS properties. This lets you create smooth transitions
            from one state to another.
          </p>
          <p>
            To create a transition effect, you must specify at least two things:
            the CSS property you want to add an effect to and the duration of
            the effect.
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
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 2s;
}

.box:hover {
  width: 200px;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Basic Transition:</b></p>
          <div class="box"></div>
        </li>
      </ul>
    </div>

    <!-- Transition Properties Section -->
    <div v-if="selectedSection === 'transitionProperties'">
      <div class="text-container">
        <div>
          <h1>Transition Properties</h1>
          <p>
            The <b>transition</b> property is a shorthand for four other
            properties:
          </p>
          <ul>
            <li>
              <b>transition-property:</b> Specifies the name of the CSS property
              to which the transition is applied.
            </li>
            <li>
              <b>transition-duration:</b> Specifies the duration over which
              transitions should occur.
            </li>
            <li>
              <b>transition-timing-function:</b> Describes how the intermediate
              values of the transition are calculated.
            </li>
            <li>
              <b>transition-delay:</b> Specifies the amount of time to wait
              before starting the transition effect.
            </li>
          </ul>
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
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: ease-in-out;
  transition-delay: 1s;
}

.box:hover {
  width: 200px;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Transition with Properties:</b></p>
          <div class="box2"></div>
        </li>
      </ul>
    </div>

    <!-- Transition Timing Section -->
    <div v-if="selectedSection === 'transitionTiming'">
      <div class="text-container">
        <div>
          <h1>Transition Timing</h1>
          <p>
            The <b>transition-timing-function</b> property specifies the speed
            curve of the transition effect. The speed curve defines how the
            speed during the transition varies over time.
          </p>
          <h3>Common Values:</h3>
          <ul>
            <li>
              <b>ease:</b> Specifies a transition effect with a slow start, then
              fast, then slow end (this is default).
            </li>
            <li>
              <b>linear:</b> Specifies a transition effect with the same speed
              from start to end.
            </li>
            <li>
              <b>ease-in:</b> Specifies a transition effect with a slow start.
            </li>
            <li>
              <b>ease-out:</b> Specifies a transition effect with a slow end.
            </li>
            <li>
              <b>ease-in-out:</b> Specifies a transition effect with a slow
              start and end.
            </li>
          </ul>
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
.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 2s ease-in-out;
}

.box:hover {
  width: 200px;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Transition with Timing Function:</b></p>
          <div class="box3"></div>
        </li>
      </ul>
    </div>

    <!-- Transition Examples Section -->
    <div v-if="selectedSection === 'transitionExamples'">
      <div class="text-container">
        <div>
          <h1>Transition Examples</h1>
          <p>
            Here are some additional examples of using CSS transitions to create
            smooth effects.
          </p>
        </div>
      </div>
      <h3>Example 1: Color Transition</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;color-box&quot;&gt;&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.color-box {
  width: 100px;
  height: 100px;
  background-color: red;
  transition: background-color 1s;
}

.color-box:hover {
  background-color: green;
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Color Transition:</b></p>
          <div class="color-box"></div>
        </li>
      </ul>

      <h3>Example 2: Multiple Property Transition</h3>
      <div class="code-container">
        <h4>HTML:</h4>
        <pre><code class="language-html">
&lt;div class=&quot;multi-box&quot;&gt;&lt;/div&gt;
        </code></pre>
        <h4>CSS:</h4>
        <pre><code class="language-css">
.multi-box {
  width: 100px;
  height: 100px;
  background-color: purple;
  transition: width 2s, height 2s, background-color 2s, transform 2s;
}

.multi-box:hover {
  width: 200px;
  height: 200px;
  background-color: orange;
  transform: rotate(45deg);
}
        </code></pre>
      </div>
      <h3>Outcomes:</h3>
      <ul>
        <li>
          <p><b>Multiple Property Transition:</b></p>
          <div class="multi-box"></div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import Prism from "prismjs";

const selectedSection = ref("transitionBasics");
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

.box {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 2s;
}

.box:hover {
  width: 200px;
}

.box2 {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: ease-in-out;
  transition-delay: 1s;
}

.box2:hover {
  width: 200px;
}

.box3 {
  width: 100px;
  height: 100px;
  background-color: blue;
  transition: width 2s ease-in-out;
}

.box3:hover {
  width: 200px;
}

.color-box {
  width: 100px;
  height: 100px;
  background-color: red;
  transition: background-color 1s;
}

.color-box:hover {
  background-color: green;
}

.multi-box {
  width: 100px;
  height: 100px;
  background-color: purple;
  transition: width 2s, height 2s, background-color 2s, transform 2s;
}

.multi-box:hover {
  width: 200px;
  height: 200px;
  background-color: orange;
  transform: rotate(45deg);
}

.text-container {
  margin-bottom: 20px;
}
</style>
