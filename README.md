# essential-html-snippets
Some Stuff is Essential Some is not this one is.

```html
<script>
(function() {
  var loadScript = document.createElement('script')
  var esmVersion = './module.mjs'
  var cjsVersion = './module.js'

  if (!'noModule' in HTMLScriptElement.prototype) {
     loadScript.src = cjsVersion
  } else {
     loadScript.type = 'module'
     loadScript.src = esmVersion
  }

  document.body.append(loadScript)
})()
</script>
``` 
