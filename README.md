<img width="277" alt="Help Media Queries" src="https://cloud.githubusercontent.com/assets/10454741/20606336/8025011c-b270-11e6-988b-e083942e7f78.png">

<img width="24px" alt="Google Chrome" src="https://cdn.rawgit.com/alrra/browser-logos/master/chrome/chrome_48x48.png">
<img width="24px" alt="Firefox" src="https://cdn.rawgit.com/alrra/browser-logos/master/firefox/firefox_48x48.png">
<img width="24px" alt="Safari" src="https://cdn.rawgit.com/alrra/browser-logos/master/safari/safari_48x48.png">
<img width="24px" alt="Safari" src="https://cdn.rawgit.com/alrra/browser-logos/master/edge/edge_48x48.png" title="💩">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![Beerpay](https://beerpay.io/equinusocio/help-media-queries/badge.svg?style=flat-square)](https://beerpay.io/equinusocio/help-media-queries)
[![GitHub issues](https://img.shields.io/github/issues/equinusocio/help-media-queries.svg?colorB=80d4cd&style=flat-square)](https://github.com/equinusocio/help-media-queries/issues)
[![GitHub stars](https://img.shields.io/github/stars/equinusocio/help-media-queries.svg?colorB=80d4cd&style=flat-square)](https://github.com/equinusocio/hhelp-media-queries/stargazers)



## What's "Help Media Queries"?

With this tool you can handle your responsive project without stress. You will be able to create a set of breakpoints (`min-width` obviously) that allow you to easily manage your layout .. and your components.

**HMQ** (Help Media Queries) offer also an useful tooltip sticked at the bottom of the page that will display your active media query, your screen density and the screen/viewport orientation.

<p align="center"><img width="586" alt="Help media Queries Tooltip" src="https://cloud.githubusercontent.com/assets/10454741/20607562/d382febe-b279-11e6-804e-0faa21584511.png"></p>

## How?
Just import the `help-media-queries.scss` file from `node_modules` inside your scss project, then compile.
```scss
@import 'node_modules/help-media-queries/src/help-media-queries.scss';
```
By default **HMQ** is active, so make sure to disable it by setting `$hmq-enabled` to `false`, or by removing the ```@import``` when your are on production!

**HMQ** provide two useful SASS function that make your media queries easy to write, `break()` and `density()`

Here some examples:

**With break(..)**
```scss
.Header {
  background-color: #FF00FF;

  // Green background from 960px
  @media screen and (break(medium)) {
    background-color: #00FF00;
  }
}

```

**With break(..) and density(..)**
```scss
.Header {
  background-color: #FF00FF;

  // Green background from 960px width and retina display
  @media screen and (break(medium)) and (density(2x)) {
    background-color: #00FF00;
  }
}

```




## Settings

You can override this settings in your project.

```scss
// Enable or disable HMQ (set false when you are on production!)
$hmq-enabled: true;

// If true the tooltip text color will be random each breakpoint
$hmq-enable-random-color: false;

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
