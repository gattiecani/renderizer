# Fetch
<script src="https://rawgit.com/github/fetch/master/fetch.js"></script>

<script>
fetch('https://public-api.wordpress.com/rest/v1.1/sites/gattiecani.wordpress.com/posts/').then(function(response){
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
    article.innerHTML = "<header><h2>" + p.title + "</h2><p>" + categories + "</p></header>";
    article.innerHTML += p.content;
    return article;
  });
  
  var append = posts.map(function(e){
    document.querySelector('.container').appendChild(e);
  });
}
</script>

{% include footer.md %}
