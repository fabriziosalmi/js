# js
Basic JS snippets

## Retrieve remote JSON and print to div

**`index.html`**

```
<html>
<body>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
$.getJSON( "api.json", function( data ) {
    var items = [];
    $parent = $("#json_export");
    $.each( data, function( key, val ) {
    $parent.append( "<p>" + key + " : " + val + "</p>" );
  });
});
</script>
<div id="json_export"></div>
</body>
</html>
```

**`api.json`**

```
{
  "one": "Singular sensation",
  "two": "Beady little eyes",
  "three": "Little birds pitch by my doorstep"
}
```

