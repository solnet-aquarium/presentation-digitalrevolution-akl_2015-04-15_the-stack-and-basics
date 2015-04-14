# Forbidden Features - block-less-statements

``JS
if (ok)
    t = true;
```

can become:

```JS
if (ok)
    t = true;
    advance();
```

which looks like:

```JS
if (ok) {
    t = true;
    advance();
}
```

but which actually means:

```JS
if (ok) {
    t = true;
}
advance();
```

**Programs that appear to do one thing but actually do another are much harder to get right. A disciplined and consistent use of blocks makes it easier to get it right.**

#### References:

Bad Parts: Appendix B - JavaScript: The Good Parts
http://archive.oreilly.com/pub/a/javascript/excerpts/javascript-good-parts/bad-parts.html
Douglas Crockford
