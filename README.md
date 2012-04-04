# formatter

This is a simple library designed to do one thing and one thing only - replace variables in strings with variable values.  It is built in such a way that the formatter strings are parsed and you are provided with a function than can efficiently be called to provide the custom output.

For example:

```js
// create the "I like food formatter"
var likefood = formatter('I like {{ 0 }}, {{ 0 }} is excellent and kicks the pants off {{ 1 }}.');

// I can then log out how much I like bacon
console.log(likefood('bacon', 'bread'));
```

If you have a look at your console output, you should see the following:

```
I like bacon, bacon is excellent and kicks the pants off bread.
```

## Using named variables

In the examples above we saw how the formatter can be used to replace function arguments in a formatter string.  We can also set up a formatter to use particular key values from an input string instead if that is more suitable:

```js
// create the "I like food formatter" (named style)
var likefood = formatter('I like {{ great }}, {{ great }} is excellent and kicks the pants off {{ poor }}.');

// I can then log out how much I like bacon
console.log(likefood({ great: 'bacon', poor: 'bread' }));
```

This will yield the same output as our first example.

