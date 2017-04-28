This is a simple HTML/CSS repo with some build tools sprinkled in to make
development easier and production files more performant/reliable.

The build process uses [PostCSS](https://github.com/postcss/postcss) plugins
(configured in [postcss.config.js](/files/postcss.config.js)) to allow things like
minification, SCSS syntax, autoprefixing, SVG loading and more.

#### Setup & Usage
1. Install packages: `npm install`
2. Build CSS & watch for changes: `npm run postcss`

#### Important Folders & Files  
- `src/`:
  - `css/`: pre-build css file/s
    - *note*: While the extensions is `.css`, PostCSS allows you to use select SCSS features in these files. To enable an SCSS feature, add its corresponding PostCSS plugin to the project as an NPM `DevDependency` to and list it in `postcss.config.js`.
  - `svgs/`: SVGs files to be inlined in the production .css file as Data URIs (enabled via `postcss-inline-svg`). This is great for hassle-free icons.
- `dist/`
  - `index.html`: Static HTML for the plugin, wrapped in a container element to make things look nicer while developing. This lives in `/dist` so dist can be easily spun up on a server for visual testing.
  -  `rm-bill-tracker.css`: the production, minified CSS file.
