# Style Guide Manager

A browser-based tool for designers to manage color palettes and typography across multiple projects. Single self-contained HTML file — no install, no backend, no account.

**[Try it live →](https://lylamnrose.github.io/style-guide-manager/)**

## What's in it

- **Projects.** Create, rename, duplicate, and delete style guide projects from the sidebar.
- **Colors.** Add colors with hex + a purpose label. Drag to reorder. Click any swatch to copy. Each color has an explorer for shades (auto-generated 50–950 scale) and harmony (complementary, analogous, triadic, split-complementary, tetradic, monochromatic).
- **Color blindness preview.** View the whole palette as protanopia, deuteranopia, tritanopia, or achromatopsia.
- **Contrast checker.** Every color paired against every other color, plus pure white and black, scored against the WCAG AA 4.5:1 contrast ratio. Click any cell to copy the text color.
- **Typography.** Add Google Fonts with named weight options (Light, Regular, Semibold, Bold, etc.), style options (Italic, Oblique), and switchable size units (px / pt / rem / em). The Compare expander shows side-by-side ladders for weight, style, and size. Keyboard shortcuts: `[` `]` step weight, `−` `=` step size.
- **Export.** JSON, CSS custom properties, or print-to-PDF (uses the browser's native print engine — no extra dependencies).
- **Persists locally.** Saves to your browser's `localStorage`. No account, no tracking, works offline after first load.

## How this was built — and what's mine vs. what's the AI's

I'm a student with limited coding experience. The actual code in this project — almost all of the JavaScript, almost all of the CSS — was written by Claude (Anthropic's AI assistant), through what's sometimes called *vibe coding*: I described the product I wanted in plain English, looked at what Claude built, told it what to change, and repeated until it was good.

What I contributed:

- The product idea and the feature scope.
- The UX direction — what should be on screen, how interactions should feel, what defaults make sense.
- A lot of small judgment calls during iteration ("the contrast checker needs a Valid/All toggle," "weights should be named not numeric," "let's add a shades generator," "the harmony grid is broken in this browser").
- Evaluation: did each thing actually work, did it feel right, was it useful?
- A few lines of HTML/CSS for navigation that I wrote myself.
- Deployment to GitHub Pages.

I'm being explicit about this because I want to be honest about the workflow and because I think this is a useful example of what's possible when you have a clear product vision but limited engineering skill.

## Tech

- React 18 + ReactDOM (loaded via CDN)
- Tailwind CSS (Play CDN, in-browser JIT compilation)
- Babel-standalone for in-browser JSX
- Everything bundled in one self-contained `index.html` — no build step

## Run it locally

Open `index.html` in any modern browser. That's it.

## Deploy your own

1. Fork this repo.
2. In the repo settings, enable GitHub Pages from the `main` branch root.
3. Visit `https://your-username.github.io/style-guide-manager/`.

## License

MIT — fork it, remix it, or use it as inspiration.
