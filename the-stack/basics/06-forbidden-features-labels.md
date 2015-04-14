# Forbidden Features `labels`

```JS
var i, j;

loop1:
for (i = 0; i < 3; i++) {      //The first for statement is labeled "loop1"
   loop2:
   for (j = 0; j < 3; j++) {   //The second for statement is labeled "loop2"
      if (i == 1 && j == 1) {
         continue loop1;
      }
      console.log("i = " + i + ", j = " + j);
   }
}

// Output is:
//   "i = 0, j = 0"
//   "i = 0, j = 1"
//   "i = 0, j = 2"
//   "i = 1, j = 0"
//   "i = 2, j = 0"
//   "i = 2, j = 1"
//   "i = 2, j = 2"
// Notice how it skips both "i = 1, j = 1" and "i = 1, j = 2"
```

I look at this and think WTF was going on here.

To me, resorting to a `label` is like trying to get out of a hole you dug yourself into by digging sideways.

Anything that does not directly increase the readability of your code (to others, be objective) is wrong.

#### References 

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/label
