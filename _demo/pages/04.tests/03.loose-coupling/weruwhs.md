---
title: Loose Coupling
content:
    items: '@self.children'
---

This directory shows if a Grav theme is loosely-coupled. This means that a theme should at least be able to render content even if they do not have the template coded for it. 

===

This page and its children are templated as random letters. But it should not deter the theme from showing the content. Coding this fallback behavior requires the following: 

- adding content generation logic in your `default.html.twig` that catches the following:
    + that when a page has a `@self.modular` attribute for `content.items` and is unsupported by the theme, must behave like a `modular` template (loop through the page collection and use `modular/default.html.twig` per module)
    + that when a page has a `content.items` header other than `@self.modular` and is unsupported by the theme, must behave like a `blog` template.
    + If nothing else, just render its content.
- adding basic support for both `modular.html.twig` and `modular/default.html.twig`

`Canvas` defines these in `partials/content.html.twig`. What these do is allowing you to override the `system` fallback behavior for handling templates and template errors. For canvas, graceful is preferred over strict.