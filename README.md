# js
Basic JS snippets

## Retrieve remote JSON and print to div

**`index.html`**

```
<html>
<body>
<head>
<style></style>
</head>
<body>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
$.getJSON( "api.json", function( data ) {
    var items = [];
    $parent = $("#json_export");
    $.each( data, function( key, val ) {
    $parent.append( "" + key + " : " + val + "<br>" );
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
  "key1": "value1",
  "key2": "value2",
  "key3": "value3"
}
```

