# KelbyOne Components Library

### In order for all components to load, this must be present on the page

```
<!-- UNPKG hosted js -->
<script src="https://unpkg.com/@kelbyone/components@latest/dist/koc.umd.min.js"></script>

<script>
  // Assign koc to window glob if not already defined
  (function (w, f) {
    var l = f + 'Queue'; w[l] = w[l] || [];
    w[f] = w[f] || function () { w[l].push(arguments); };
  })(window, 'koc');

  // Global components configuration
  koc("configure", {
    debug: false,
    api: {
      uri: "...",
      version: ".."
    }
  });
</script>
```
