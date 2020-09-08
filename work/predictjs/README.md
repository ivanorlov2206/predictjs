# Object prediction JavaScript library

## Usage

Include library with
```html
<script src="predict.min.js"></script>
<script>
(async () => {

  var predictor = createPredictor(document.getElementById("@div where will be canvas@"), @canvas width@, @canvas height@);

  var res = await predictor.predict('@object_class@', '@models url@');
})();
</script>
```

## Example

```javascript
(async () => {

  var predictor = createPredictor(document.getElementById("test_div"), 224, 224);

  var res = await predictor.predict('spider', 'http://localhost:8000/models/');
  // in res we can find 1 if drawn object belong to selected class or 0 if it isn't
})();
```
