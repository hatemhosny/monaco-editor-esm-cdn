# monaco-editor-esm-cdn

This is an ESM build of Monaco Editor which can be loaded from CDN.

## Usage

The editor is bundled as ESM. It can be used like this:

[try in LiveCodes](https://livecodes.io/?x=id/dgzkpnfzzbq)

```html
<div id="container" style="height: 200px;"></div>

<script type="module">
  import { monaco } from "https://cdn.jsdelivr.net/npm/monaco-editor-esm-cdn/monaco.js";

  monaco.editor.create(document.getElementById("container"), {
    value: `function x() {\n\tconsole.log("Hello world!");\n}`,
    language: "javascript",
  });
</script>
```

Alternatively, options can be specified, by using the `loadMonaco` function:

```js
import { loadMonaco } from "https://cdn.jsdelivr.net/npm/monaco-editor-esm-cdn/load-monaco.js";

const baseUrl = "https://cdn.jsdelivr.net/npm/monaco-editor-esm-cdn/dist/";
const monaco = await loadMonaco({ baseUrl, injectStyles: false });
```

## Build

```bash
npm run build
```

## License

MIT License
