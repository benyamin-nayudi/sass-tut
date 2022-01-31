### we can use the math package like this

#### to divide the border radius by 4

```css
@use "sass:math";
math.div($base-border-radius, 4)

/* other methods: */
math.floor(10.25)
math.max(10px , 20px , 15px)
```

### we can use the `@debug` to console values and check them

```css
@debug "hello ninjas";
```

### we can use map to make palettes and something like these

```css
/* color pallette */
$colors: (
  "primary": $primary,
  "secondary": $secondary,
  "error": $error,
  "info": $info,
  "blue": #1919e6,
  "red": #d32752,
  "green": #1ac888,
  "yellow": #f6c31c,
  "orange": #f7931e,
  "purple": #9b51e0,
  "gray": #808080,
  "black": #000,
  "white": #fff
);
```

> to interact with the map we can use its different methods:

- get a property

```css
@debug map-get($colors, "purple");
```

- check a property

```css
@debug map-has-key($colors, "secondary");
```

- remove a property.

```css
@debug map-remove($colors, "primary");
```

- add a property

```css
@debug map-merge($colors, ("pink", #ffc0cb));
```

> to use the map functionality:

```css
.button {
  color: map-get($colors, "primary");
}
```
