# gatsby-universal

[![CircleCI](https://circleci.com/gh/fabe/gatsby-universal.svg?style=svg)](https://circleci.com/gh/fabe/gatsby-universal) [![styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier) [![deploys by netlify](https://img.shields.io/badge/deploys%20by-netlify-00c7b7.svg)](https://www.netlify.com)

An *opinionated* starter for using Gatsby v2 with React Context, tag-agnostic styled-components, page transitions, scroll events with `IntersectionObserver`. Made for state-of-the-art marketing sites.

## Features

- [X] 💅 `styled-components`, tag agnostic if needed
- [ ] 🤩 Page Transitions, component-based (with no-js support)
  > Following Gatsby's switch to @reach/router, page transitions are currently not supported. Follow the progress at [#8](https://github.com/fabe/gatsby-universal/issues/8).
- [X] 👮‍♂️ `IntersectionObserver`, component-based (with polyfill)
- [X] 🌿 React Context for global UI state, with SSR
- [X] 💯 Optimized with Google Lighthouse
- [X] 🔥 Code Splitting of CSS and JS (component based)
- [X] ⚙️ One config file for site-wide settings
- [X] 💙 Most social + meta tags in one component
- [X] 🖼 All favicons generated, only one icon file needed
- [X] 🌐 Offline support
- [X] 📄 Manifest support
- [X] 🗺 Sitemap support
- [X] 📱 Generated media queries for easy use
- [X] 😎 Prettier for code style
- [X] 👷‍♂️ CircleCI support
- [ ] 🐙 Schema JSONLD

## Lighthouse scores (on Netlify)

[![Lighthouse scores (on Netlify)](https://lighthouse.now.sh/?perf=100&pwa=100&a11y=100&bp=100&seo=100)](https://circleci.com/gh/fabe/gatsby-universal)

## Usage

> To make sure you have the correct beta versions of Gatsby, please use `yarn` to install the dependencies.

```bash
# Installation
gatsby new my-site https://github.com/fabe/gatsby-universal

# To develop
yarn develop

# To build
yarn build

# To test SSR (for Lighthouse etc.)
yarn ssr

# To format JS (precommit)
yarn format

# To generate favicons (included in `build`)
yarn build:favicons
```

## Configuration

Find the site-wide configuration in `site-config.js`.

```js
module.exports = {
  siteTitle: `Gatsby Universal`,
  siteTitleShort: `GatsbyU`,
  siteDescription: `An opinionated starter for Gatsby.`,
  siteUrl: `https://gu.fabianschultz.com`,
  themeColor: `#000`,
  backgroundColor: `#fff`,
  pathPrefix: null,
  logo: path.resolve(__dirname, 'src/images/icon.png'),
  social: {
    twitter: `gatsbyjs`,
    fbAppId: `966242223397117`,
  },
};
```

## Folder structure
```bash
├── README.md
├── gatsby-browser.js
├── gatsby-config.js
├── gatsby-node.js
├── gatsby-ssr.js
├── package.json
├── src
│   ├── components
│   │   ├── head # All meta tags etc.
│   │   │   └── head.js
│   │   ├── io # Intersection Observer component, uses render props
│   │   │   └── io.js
│   │   ├── layout # Layout component
│   │   │   ├── layout.css.js # .css.js for component's styled-components
│   │   │   └── layout.js
│   │   └── transition # Page Transition component, can be used with any other
│   │       └── transition.js
│   ├── constants
│   ├── containers
│   ├── helpers
│   │   ├── agnosticStyled.js # Tag-agnostic styled-component
│   │   ├── mediaTemplates.js # Creates media queries for styled-components
│   │   └── toFallbackStyleString.js # Creates fallback styles for no-js page transitions
│   ├── images
│   ├── pages
│   ├── reset.css.js # Global CSS
│   └── store
└── yarn.lock
```

## Author

* Fabian Schultz ([@fschultz\_](https://twitter.com/fschultz_)) - [Stink Studios](https://stinkstudios.com)
