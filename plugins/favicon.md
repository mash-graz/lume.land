---
title: Favicon
description: Create all favicons needed automatically using a svg file as the source
mod: plugins/favicon.ts
tags:
  - images
---

## Description

This plugin reads a file (by default `/favicon.svg`) and generates the following
files:

- `/favicon.ico`
- `/favicon-16.png`
- `/favicon-32.png`
- `/apple-touch-icon.png`

It also add the `<link>` elements to all HTML pages to configure the favicons
properly.

## Installation

Import this plugin in your `_config.ts` file to use it:

```js
import lume from "lume/mod.ts";
import favicon from "lume/plugins/favicon.ts";

const site = lume();

site.use(favicon(/* Options */));

export default site;
```

Note that you need the `/favicon.svg` file in your source folder with a 1/1
aspect ratio. You can set another filename or image format in the configuration:

```js
site.use(favicon({
  input: "/my-custom-favicon.png",
}));
```
