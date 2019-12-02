## Example 2 Truths 1 Lie Code
### HTML
``` HTML
<div class="main-content">
  <h1>Two Truths and a Lie</h1>
  <div class="flex-display">
    <div class="factoid">
      <h3>Visiting Haiti</h3>
      <p>The only time I have been out of the country was when I went to Haiti, one of the poorest countries in the
        world.</p>
    </div>

    <div class="factoid">
      <h3>Custom Build</h3>
      <p>I custom built my first computer when I was just 10 years old.</p>
    </div>

    <div class="factoid">
      <h3>Art School Dropout</h3>
      <p>After one semester in art school it was announced that they would be shutting down the program.</p>
    </div>
  </div>
</div>
```

### CSS
``` CSS
h1 {
  color: lightgreen;
  text-align: center;
}
h3 {
  color: blue;
}
p {
  color: red;
}
.main-content {
  border: solid 3px black;
  border-radius: 15px;
  background-color: grey;
}
.flex-display {
	display: flex;
}
.factoid {
  border: solid 1px black;
  border-radius: 15px;
	background-color: lightgrey;
	width: 33.33333%;
}
```