# Skribbl Excercise

On [skribbl.io](https://skribbl.io) people can choose between three words they will draw on a
white canvas. Other people in 'the room' need to guess what is being drawn. The first to guess the
correct word wins! This is a fun game to play with a class.

The canvas is a quite low level pixel canvas. This could as well be a table with lots of cells.
Nice. We could turn this into a programming excercise ... and close the lesson with an actual
skribbl game (not on our selfmade canvas, but on [skribbl.io](https://skribbl.io) ... but still
people will get the feeling of understanding what is actually happening more 😃)

## Online

To do this exercise online we can use [codepen.io](https://codepen.io). This has an online
development environment with three editors and an execution window.

### HTML

```html
<div class="whole">
  <div class="header">
    Pictionary
  </div>
  <div class="main">
    <div id="painting" class="painting">
      the painting
    </div>
    <div class="toolbox">
      <p>the toolbox</p>
      <div class="tools">
        <div id="resetButton">reset</div>
      </div>
    </div>
  </div>
</div>
<script>
  function paint(el, event) {
    let name = el.id;
    console.log(`painting div [${name}]: ${event.type}`)
    el.style.backgroundColor = "red";
  }
</script>
```

```css
.whole {
  display:grid;
  grid-template-rows: 2em auto;
  padding: 3px;
  background-color: dodgerblue;
  height: 20em;
}
.header {
  display: block;
  background-color: #f1f1f1;
  text-align: center;
  font-size: 1.5em;
}
.main {
  margin: 10px auto;
  padding: 3px;
  display: grid;
  grid-template-columns: auto 5em;
  width: 100%;
}
.painting {
  background-color: #f1f1f1;
  border: 1px solid black;
  margin: auto 3px;
/*   display: inline-grid;
  grid-auto-flow: column; */
  display: flex;
  flex-wrap: wrap;
}
.cell {
  background-color: light-grey;
  height: 4px;
  width: 4px;
}
.toolbox {
  background-color: #f1f1f1;
  border: 1px solid black;
  margin: auto 3px;
}
.tools {
  display: grid;
  grid-template-columns: auto auto;
}
```

```javascript
import $ from "https://esm.sh/jquery";

function resetPainting() {
  let divs = "";
  for (let i = 0; i < 100000; i++) {
    divs += `<div id="cell${i}" class="cell" onmouseover="paint(this, event)"></div>`;
  }
   $("#painting").html(divs);
}

$("#resetButton").on("click", function() {
  resetPainting()
});
```
