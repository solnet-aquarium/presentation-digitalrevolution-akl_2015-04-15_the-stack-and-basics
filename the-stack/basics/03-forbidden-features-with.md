# Forbidden Features `with`

```JS
with (obj) {
    a = b;
}
```

does the same thing as:

```JS
if (obj.a === undefined) {
    a = obj.b === undefined ? b : obj.b;
} else {
    obj.a = obj.b === undefined ? b : obj.b;
}
```

So, it is the same as one of these statements:

```
a = b;
a = obj.b;
obj.a = b;
obj.a = obj.b;
```

It is not possible to tell from reading the program which of those statements you will get. 

It can vary from one running of the program to the next. It can even vary while the program is running. 

**If you can't read a program and understand what it is going to do, it is impossible to have confidence that it will correctly do what you want.**

#### References:

Bad Parts: Appendix B - JavaScript: The Good Parts
http://archive.oreilly.com/pub/a/javascript/excerpts/javascript-good-parts/bad-parts.html
Douglas Crockford
