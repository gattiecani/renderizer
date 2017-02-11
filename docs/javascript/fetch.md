# Fetch

Include fetch

```html
<script src="https://rawgit.com/github/fetch/master/fetch.js"></script>
```

Fetch posts

```js
fetch('https://public-api.wordpress.com/rest/v1.1/sites/potlachsite.wordpress.com/posts/').then(function(response){
  if (response.status >= 200 && response.status < 300) {
    return response.json();
  } else {
    var error = new Error(response.statusText)
    error.response = response
    throw error
  }
}).then(printList).catch(console.log);

function printList(j){
  var posts = j.posts.map(function(p) {
    var article = document.createElement('article');
    var categories = Object.keys(p.terms.category).join(', ') || '';
    var firstTags = Object.keys(p.tags)[0] || 0;
    article.innerHTML = "<header><h2>" + p.title + "</h2>" +
      "<p>Categoria: " + categories + "<br>Prezzo: " + firstTags + " €</p>" +
      "</header>";
    article.innerHTML += p.content;
    if(p.post_thumbnail) article.innerHTML += "<br>thumbnail: " + p.post_thumbnail.URL;
    return article;
  });
  var parent = document.querySelector('.container');
  var reference = document.querySelector('.footer');
  var append = posts.map(function(e){
    parent.insertBefore(e ,reference);
  });
}
```

Post data

```js
{
  title: "...",
  content: "...",
  tags: {
    15.30: {...}
  },
  terms: {
    category: {
      Cani: {...}
    }
  },
  post_thumbnail: {
    URL: "..."
  }
}
```

<script src="https://rawgit.com/github/fetch/master/fetch.js"></script>
<script>
fetch('https://public-api.wordpress.com/rest/v1.1/sites/potlachsite.wordpress.com/posts/').then(function(response){
  if (response.status >= 200 && response.status < 300) {
    return response.json();
  } else {
    var error = new Error(response.statusText)
    error.response = response
    throw error
  }
}).then(printList).catch(console.log);

function printList(j){
  var posts = j.posts.map(function(p) {
    var article = document.createElement('article');
    var categories = Object.keys(p.terms.category).join(', ') || '';
    var firstTags = Object.keys(p.tags)[0] || 0;
    article.innerHTML = "<header><h2>" + p.title + "</h2><p>Categoria: " + categories + "<br>Prezzo: " + firstTags + " €</p></header>";
    article.innerHTML += p.content;
    if(p.post_thumbnail) article.innerHTML += "<br>thumbnail: " + p.post_thumbnail.URL;
    return article;
  });
  var parent = document.querySelector('.container');
  var reference = document.querySelector('.footer');
  var append = posts.map(function(e){
    parent.insertBefore(e ,reference);
  });
}
</script>

{% include footer.md %}
