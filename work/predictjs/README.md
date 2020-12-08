# Object prediction JavaScript library

## Usage

Include library with
```html
<script src="predict.min.js"></script>
<script>
(async () => {

  var predictor = createPredictor(document.getElementById("@div where canvas will be@"), @canvas width@, @canvas height@, @pen_size(10 is recommended)@);

  var res = await predictor.predict('@object_class@', '@models url@');
})();
</script>
```

## Example

```javascript
(async () => {

  var predictor = createPredictor(document.getElementById("test_div"), 224, 224, 12);

  var res = await predictor.predict('spider', 'http://localhost:8000/models/');
  // in res we can find 1 if drawn object belong to selected class or 0 if it isn't
})();
```

## Working with canvas

```javascript
predictor.clear_canvas(); // Clearing the canvas
predictor.clear_canvases() // Removing all of canvases created for image processing
```
