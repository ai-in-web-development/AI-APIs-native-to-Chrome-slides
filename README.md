<style>
* {
  box-sizing: border-box;
}

/* Create three equal columns that floats next to each other */
.column {
  float: left;
  width: 33.33%;
  padding: 10px;
  height: 300px; /* Should be removed. Only for demonstration */
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
</style>

## The Dawn of AI in Web Development

Imagine the power of **AI as JS APIs natively available in Chrome**.

**AI is already here**, not just the future of Chrome.

Let's build **smarter, faster, and with more fun - right in the browser**.

[Handwritten notes of 12th April 2025 React Meetup88](https://github.com/kurtzace/diary-2025/tree/main/seminars/reactmeetup88)

---

## Traditional vs. Modern Approach

Traditional client-server model is evolving.
*   Traditional: Client -> Server -> AI model

**Modern Way**: Utilizing browser's compute power.
*   The **browser is the compute engine** for AI.
*   Client + AI model in browser.

---

## Key Libraries for Browser AI
(where browser downloads model)
*   **[TensorFlow.js](https://www.tensorflow.org/js/models)**, [demo](https://holobooth.flutter.dev/#/)
*   **face-api.js**
*   **ml5js**
*   **kalidokit**
*   **[Handtrack.js](https://victordibia.com/handtrack.js/#/)**

Used for real-world applications like image/video processing, face recognition, hand tracking, avatars, and hand gestures directly in the browser.

---

## Utilizing Browser's Built-in Capabilities

Leverage **powerful AI APIs natively available in Chrome**.

Examples of using browser's built-in capabilities:
*   **Translate**
*   **Language Detector**
*   **Summarizer**
*   **Prompt**

--

### Translate Example

Demonstrated creating a translator with `self.ai.translator.create()`.

```javascript
const translator2 = await self.ai.translator.create({
  sourceLanguage: 'es',
  targetLanguage: 'hi',
  monitor(m) {
    m.addEventListener('downloadprogress', (e) => {
      console.log(`Downloaded ${e.loaded} of ${e.total} bytes.`);
    });
  },
});
await translator2.translate("Hello, how are you");
```


--

### Summarizer Example

Creating and using a summarizer.

```javascript
const summarizer = await ai.summarizer.create({
  monitor(m) {
    m.addEventListener('downloadprogress', (e) => {
      console.log(`Downloaded ${e.loaded} of ${e.total} bytes.`);
    });
  }
});
const summary = await summarizer.summarize(text, {
  context: 'These are a prescription data intended to be consumed by doctor.',
});
```

--

### Possible steps to enable AI features

[All Steps](https://www.youtube.com/watch?v=v7mQ_eaT4Gw)

[Fill form](https://docs.google.com/forms/d/e/1FAIpQLSfZXeiwj9KO9jMctffHPym88ln12xNWCrVkMY_u06WfSTulQg/viewform) > [Get Chrome Dev](https://www.google.com/chrome/dev/) > [Follow docs](https://docs.google.com/document/d/18otm-D9xhn_XyObbQrc1v7SI-7lBX3ynZkjEpiS1V04/edit?pli=1&tab=t.0) > Enable flags

chrome://flags/#optimization-guide-on-device-model
chrome://flags/#prompt-api-for-gemini-nano

After 24 hours try <small>`await window.ai.canCreateTextSession()`</small>


---

## Benefits of Browser-Based AI

*   **Cost**
*   **Computation**
*   **Deployment**
*   **Load**
*   **Scale**
*   **Privacy**
*   **User Experience**
*   **Offline AI usage**

---

## What's Coming Next?

**AI-native extensions** are coming.

Future possibilities:
*   **AI in DevTools**
*   **Help in write**

Imagine a site that adjusts layout based on what it predicts your visitor prefers - all done client-side, in Browser.

--

### Enable Devtools AI features
![image](./assets/chromeCanaryENableAI.gif)

--

### Change theme example
![image](./assets/askAIMakeThemeAsLight.gif)


---

## Wrap Up

**AI is becoming an integral part of modern web development**.

- Developers should explore **browser-based AI libraries** and cloud-based AI SDKs.
- Let's build smarter, faster, and with more fun - **right in the browser**.

**Credits**: AI for Web Development by [Vishwesh Jainkuniya](https://www.linkedin.com/in/jainkuniya/), Lead Engineer, [eka.care](http://eka.care/) , [Original Slides](https://t.co/rUFkFpVrp6)

```