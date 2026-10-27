# SafeSpeak

A client-side message safety checker built for AUF CCS. You type a message, it runs
through TensorFlow.js's toxicity model in the browser, and you get back an AI-assisted
read on whether the language is likely to be harmful — before you hit send.

## How it works

- Loads [`@tensorflow-models/toxicity`](https://github.com/tensorflow/tfjs-models/tree/master/toxicity) via TensorFlow.js, entirely client-side
- A 500-character message box with a live character counter
- "Try an example" buttons (positive / neutral / toxic) to see the model in action without typing your own message
- No backend, no server calls for the analysis itself — the model runs in the visitor's browser

## Tech stack
- HTML / CSS
- TensorFlow.js + the TF.js toxicity model (loaded from a CDN)

## Run it
No build step. Open `index.html` in a browser, or serve it locally:

```bash
python3 -m http.server 8000
```

---
Built by Melvin Carlo Villanueva, for AUF CCS.
