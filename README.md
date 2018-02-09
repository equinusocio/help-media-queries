<img width="277" alt="Help Media Queries" src="https://cloud.githubusercontent.com/assets/10454741/20606336/8025011c-b270-11e6-988b-e083942e7f78.png"><br/><img width="24px" alt="Google Chrome" src="https://cdn.rawgit.com/alrra/browser-logos/2109c114/src/chrome/chrome_48x48.png"><img width="24px" alt="Firefox" src="https://cdn.rawgit.com/alrra/browser-logos/2109c114/src/firefox/firefox_48x48.png"><img width="24px" alt="Safari" src="https://cdn.rawgit.com/alrra/browser-logos/2109c114/src/safari/safari_48x48.png" title="💩"><img width="24px" alt="Microsoft Edge" src="https://cdn.rawgit.com/alrra/browser-logos/2109c114/src/edge/edge_48x48.png" title="💩">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="https://beerpay.io/equinusocio/help-media-queries"><img alt="Beerpay" src="https://beerpay.io/equinusocio/help-media-queries/badge.svg?style=flat-square"></a>
<a href="https://github.com/equinusocio/help-media-queries/issues"><img alt="Issues" src="https://img.shields.io/github/issues/equinusocio/help-media-queries.svg?colorB=80d4cd&style=flat-square"></a>
<a href="https://github.com/equinusocio/hhelp-media-queries/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/equinusocio/help-media-queries.svg?colorB=44cc11&style=flat-square"></a>
<a href="https://github.com/equinusocio/hhelp-media-queries/stargazers"><img alt="Usage" src="https://img.shields.io/npm/dt/help-media-queries.svg?style=flat-square&label=downloads"></a>
<a href="https://www.codacy.com/app/astorino-design/help-media-queries?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=equinusocio/help-media-queries&amp;utm_campaign=Badge_Grade"><img src="https://api.codacy.com/project/badge/Grade/703947b1dda3484aac7b845a911a6f76"/></a>

## What's "Help Media Queries"?

With this tool you can handle your responsive project without stress. You will be able to create a set of breakpoints (`min-width` obviously) that allow you to easily manage your layout .. and your components.

**HMQ** (Help Media Queries) offer also an useful tooltip sticked at the bottom of the page that will display your active media query, your screen density and the screen/viewport orientation.

<p align="center"><img width="586" alt="Help media Queries Tooltip" src="https://cloud.githubusercontent.com/assets/10454741/20607562/d382febe-b279-11e6-804e-0faa21584511.png"></p>

**HMQ** provide also two useful SASS functions that make your media queries easy to write, `break()` and `density()`

Here some examples:

**With break(..)**
```scss
.Header {
  background-color: #FF00FF;

  // Green background from 960px width
  @media screen and (break(medium)) {
    background-color: #00FF00;
  }
}

.Menu {
  color: #FF00FF;

  // Green color from 960px width and retina display
  @media screen and (break(medium)) and (density(2x)) {
    color: #00FF00;
  }
}

```

## How?
Install this tool with `npm install -D help-media-queries`. If you use [Yarn](https://yarnpkg.com/), run `yarn add --dev help-media-queries`

##### Gulp/Grunt

```scss
// Import the functions break() and density()
@import 'node_modules/help-media-queries/src/helpers.scss';
// Import the tooltip flag
@import 'node_modules/help-media-queries/src/tooltip.scss';
```

##### Webpack

Inside your `scss` entry point, import once the tooltip file:
```scss
// Import the tooltip flag
@import '~help-media-queries/src/tooltip.scss';
```
Import media queries functions inside each component `scss` file:
```scss
// Import the functions break() and density()
@import '~help-media-queries/src/helpers.scss';
```

**By default HMQ is active, so make sure to disable it by set `$hmq-enable-tooltip` to `false` (before of imports), or by removing the tooltip ```@import``` when your are on production!**

## Settings

You can override this settings in your project.

```scss
// Enable or disable the HMQ tooltip (set false when you are on production!)
$hmq-enable-tooltip: true;

// If true the tooltip text color will be random each breakpoint
$hmq-enable-random-color: false;

// Set a dark theme for the tooltip (useful on white background)
$hmq-dark-theme: false;

// This is the default breakpoints map, useful for a wide usage.
$breakpoints: (
  extraSmall : 30em,
  small      : 48em,
  medium     : 60em,
  large      : 80em,
  extraLarge : 100em
);

// Screen densities. You don't need to change this values.
$densities: (
  1x  : '96dpi',
  15x : '144dpi',
  2x  : '192dpi',
  3x  : '288dpi',
  4x  : '384dpi'
);

```

## Support on Beerpay
Hey dude! Help me out for a couple of :beers:!

[![Beerpay](https://beerpay.io/equinusocio/help-media-queries/badge.svg?style=beer-square)](https://beerpay.io/equinusocio/help-media-queries)  [![Beerpay](https://beerpay.io/equinusocio/help-media-queries/make-wish.svg?style=flat-square)](https://beerpay.io/equinusocio/help-media-queries?focus=wish)
