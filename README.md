# JSXPress

JSXPress is a zero-config JSX renderer for quickly previewing JSX snippets in the browser.

Paste JSX from an AI chat, a component body, or a small React component file into the editor and JSXPress will transpile it in the browser with Babel and render it instantly with React 18.

## Live site

<https://elliottlawson.github.io/jsxpress/>

## Features

- Single-file app with no build step
- Live JSX transpilation and rendering in the browser
- Inline syntax and runtime error reporting
- Support for:
  - raw JSX markup
  - component bodies with hooks
  - common `export default` React snippets
- Example, copy, and share-link controls
- Empty-first editor with a resizable split view on desktop
- Mobile responsive split-pane layout

## How it works

JSXPress loads React, ReactDOM, and `@babel/standalone` from a CDN. User input is normalized into a renderable component, transpiled in the browser, and mounted with `ReactDOM.createRoot`.

Shared links store the current snippet in the URL hash so someone else can open the same JSX without needing a server-side backend.

## Safety note

Pasted code is transpiled and executed directly in the browser so event handlers and interactive components work in the preview. Treat shared snippets as code you trust, just as you would with any local HTML/JS playground.

## Local usage

Because the page loads browser scripts from CDNs, you can open `index.html` directly in a browser or serve the repository with any static file server.

## GitHub Pages

To publish on GitHub Pages, set the repository Pages source to:

- Branch: `master`
- Folder: `/ (root)`
