<a href="https://farhadg.github.io/script-tag-data" target="_blank">Script Tag Data</a>
=======================================================================================

Set and read data from a `<script>` tag. You can check this out being used in my <a href="https://www.github.com/farhadg/repo-card" target="_blank">Repo Card</a> project.

### Installation

Bower
```bash
$ bower install script-tag-data --save
```

CDN
```html
<script src="https://rawgit.com/FarhadG/script-tag-data/master/script-tag-data.min.js"></script>
```

### Usage

```html
<script src="https://cdn.com/lib-name.js" id="lib-name" data-weather="sunny" data... /></script>
```

Provide the user / app a simple `<script>` tag, a CSS `#id` and whatever data points as HTML5 `data` attributes.

- Get all of the data values from a `<script>` tag: `ScriptTagData.getData(scriptId)`
- Only get the `<script>` tag: `ScriptTagData.getScript(scriptId)`

### Examples

Some website with your `<script>` tag, an ID and the desired data points.
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Title</title>
</head>
<body>
    ...

    <script id="your-library" src="./your-library.js" data-car="pagani" data-star-repo="yes, please :)">
</body>
</html>
```

Your JS file where you have ScriptTagData library loaded by either referencing from here on <a href="https://cdn.rawgit.com/FarhadG/script-tag-data/master/script-tag-data.min.js" target="_blank">GitHub</a> or serving it yourself.
```javascript
/**
 * This returns the following:
 *
 * {
 *   car: 'pagani',
 *   starRepo: 'yes, please :)'
 * }
 */

ScriptTagData.getData('your-library');

/**
 * This returns the just <script> tag
 */

ScriptTagData.getData('your-library');
```

### Questions

Please use issues page for any questions or concerns.
