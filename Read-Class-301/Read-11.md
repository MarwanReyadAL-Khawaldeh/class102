# EJS

# What is EJS?
What is the "E" for? "Embedded?" Could be. How about "Effective," "Elegant," or just "Easy"? EJS is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript.

## Install
It's easy to install EJS with NPM.
```
$ npm install ejs
```

# Use
Pass EJS a template string and some data. BOOM, you've got some HTML.
```
let ejs = require('ejs');
let people = ['geddy', 'neil', 'alex'];
let html = ejs.render('<%= people.join(", "); %>', {people: people});
```

# CLI
Feed it a template file and a data file, and specify an output file.
```
ejs ./template_file.ejs -f data_file.json -o ./output.html
```

# Browser support
Download a browser build from the latest release, and use it in a script tag.
```
<script src="ejs.js"></script>
<script>
  let people = ['geddy', 'neil', 'alex'];
  let html = ejs.render('<%= people.join(", "); %>', {people: people});
</script>
```

# Example
```
<% if (user) { %>
  <h2><%= user.name %></h2>
<% } %>
```

# Usage
```
let template = ejs.compile(str, options);
template(data);
// => Rendered HTML string

ejs.render(str, data, options);
// => Rendered HTML string

ejs.renderFile(filename, data, options, function(err, str){
    // str => Rendered HTML string
});
```

# Options
* cache Compiled functions are cached, requires filename
* filename Used by cache to key caches, and for includes
* root Set project root for includes with an absolute path (e.g, /file.ejs). Can be array to try to resolve include from multiple directories.
* views An array of paths to use when resolving includes with relative paths.
* context Function execution context
* compileDebug When false no debug instrumentation is compiled
* client Returns standalone compiled function
* delimiter Character to use for inner delimiter, by default '%'
* openDelimiter Character to use for opening delimiter, by default '<'
* closeDelimiter Character to use for closing delimiter, by default '>'
* debug Outputs generated function body
* strict When set to `true`, generated function is in strict mode
* _with Whether or not to use with() {} constructs. If false then the locals will be stored in the locals object. (Implies `--strict`)
* localsName Name to use for the object storing local variables when not using with Defaults to locals
* rmWhitespace Remove all safe-to-remove whitespace, including leading and trailing whitespace. It also enables a safer version of -%> line slurping for all scriptlet tags (it does not strip new lines of tags in the middle of a line).
* escape The escaping function used with <%= construct. It is used in rendering and is .toString()ed in the generation of client functions. (By default escapes XML).
* outputFunctionName Set to a string (e.g., 'echo' or 'print') for a function to print output inside scriptlet tags.
* async When true, EJS will use an async function for rendering. (Depends on async/await support in the JS runtime.

# Includes
Includes are relative to the template with the include call. (This requires the 'filename' option.) For example if you have "./views/users.ejs" and "./views/user/show.ejs" you would use <%- include('user/show'); %>.

You'll likely want to use the raw output tag (<%-) with your include to avoid double-escaping the HTML output.
```
<ul>
  <% users.forEach(function(user){ %>
    <%- include('user/show', {user: user}); %>
  <% }); %>
</ul>
```

# Custom delimiters
Custom delimiters can be applied on a per-template basis, or globally:
```
let ejs = require('ejs'),
    users = ['geddy', 'neil', 'alex'];

// Just one template
ejs.render('<?= users.join(" | "); ?>', {users: users},
    {delimiter: '?'});
// => 'geddy | neil | alex'
// Or globally
ejs.delimiter = '$';
ejs.render('<$= users.join(" | "); $>', {users: users});
// => 'geddy | neil | alex'
```

# Caching
EJS ships with a basic in-process cache for caching the intermediate JavaScript functions used to render templates. It's easy to plug in LRU caching using Node's `lru-cache` library:
```
let ejs = require('ejs'),
    LRU = require('lru-cache');
ejs.cache = LRU(100); // LRU cache with 100-item limit
```
If you want to clear the EJS cache, call ejs.clearCache. If you're using the LRU cache and need a different limit, simple reset `ejs.cache` to a new instance of the LRU.

# Custom file loader
The default file loader is fs.readFileSync, if you want to customize it, you can set ejs.fileLoader.
```
let ejs = require('ejs');
let myFileLoader = function (filePath) {
  return 'myFileLoader: ' + fs.readFileSync(filePath);
};

ejs.fileLoader = myFileLoader;
```
With this feature, you can preprocess the template before reading it.

# Layouts
EJS does not specifically support blocks, but layouts can be implemented by including headers and footers, like so:
```
<%- include('header'); -%>
<h1>
  Title
</h1>
<p>
  My page
</p>
<%- include('footer'); -%>
```
