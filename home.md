---
title: Home
description: 
published: true
date: 2022-04-27T17:35:49.535Z
tags: 
editor: markdown
dateCreated: 2022-04-27T17:31:38.633Z
---

---
sidebar: auto
---

# wikijs-vuepress
This page was created with Wiki.js and loaded into VuePress at build time.

## Wiki.js
The Wiki.js server provides a GraphQL endpoint with which we can get a list of pages and its content.

I started [Wiki.js server](http://wikijs.voidavoid.ru/) to create a test set of pages. I couldn't load pages from wikijs.ynvrs.eu because for this we have to enable API endpoint and generate API key in Wiki.js's administration area.

## VuePress
In the `.vuepress/config.js` configuration file we can assign an async function to the the `additionalPages` parameter that returns an array of pages to be included in the build. Thus, we are able to create pages dynamically.

## Code notes
In the root directory of the project I created a `.env` file to pass GraphQL endpoint URL and API access key.

The code that interacts with Wiki.js and processes the received data is located in the `src/wikijs` directory. In addition to actually loading the pages, I implemented the simple functions to create the header navigation and sidebar.

::: tip
On this page, the sidebar was created using standard VuePress tools by setting the `sidebar: auto` parameter in the frontmatter block of the page. Dynamically created sidebar presented on [the subpages](/sub).
:::

---
