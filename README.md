# learn-jekyll

Learning Jekyll which is a static site generator. I chose to learn this over Gatsby first because after some research it appears in most cases jekyll is faster due to less network requests.

### Liquid - a templating laguage created by Shopify

Objects - for accessing vars - `{{ varName.varName2 }}`

tags - for logic and control flow - `{% if page.sidebar_show %} <div>sidebar</div>{% endif %}`

filters - for changing output of Objects - `{{ 'Hello World!' | downcase }}` - can check https://jekyllrb.com/docs/liquid/filters/ for more

### Front Matter - metadata in YAML format.
YAML starts with 3 hyphens and ends with 3 hyphens with key value pairs in between. Must be present for Jekyll to parse Liquid.
Example:
```
  ---
  title: My Blog
  ---
  ```

You can access Front Matter with Liquid Objects - e.g. `<title>{{ page.title }}</title>`

### Layouts - you can store layouts and set the page to use that particular layout. 

Create a folder called _layouts and in there create a layout e.g. _layouts/default.html. 

In the default.html ->
```
<!doctype html>
<html>
  <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
  </head>
  <body>
    {{ content }}
  </body>
</html>
```

Then can use this layout using:
```
---
layout: default
---
```


### 
