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
  console.log(j);
}
</script>

{% include footer.md %}
