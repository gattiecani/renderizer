# Fetch
<script src="https://rawgit.com/github/fetch/master/fetch.js"></script>
<style>
article:after {
  content: "";
  display: table;
  clear: both;
}
</style>
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
    var categories = Object.keys(p.terms.category).join(', ');
    var tags = Object.keys(p.tags)[0];
    article.innerHTML = "<header><h2>" + p.title + "</h2><p>Categoria: " + categories + "<br>Prezzo: " + tags + "€</p></header>";
    article.innerHTML += p.content;
    return article;
  });
  
  var append = posts.map(function(e){
    document.querySelector('.container').appendChild(e);
  });
}
</script>

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
    var categories = Object.keys(p.terms.category).join(', ');
    var tags = Object.keys(p.tags)[0];
    article.innerHTML = "<header><h2>" + p.title + "</h2><p>Categoria: " + categories + "<br>Prezzo: " + tags + "€</p></header>";
    article.innerHTML += p.content;
    return article;
  });
  
  var append = posts.map(function(e){
    document.querySelector('.container').appendChild(e);
  });
}
```

{% include footer.md %}
