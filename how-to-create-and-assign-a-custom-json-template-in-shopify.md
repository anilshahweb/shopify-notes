How to Create and Assign a Custom JSON Template in Shopify 2.0?
Shopify Online Store 2.0 me custom JSON template create aur assign karne ke liye:
Sabse pahle Shopify Admin Panel me Online Store → Themes par jayenge.
Uske baad current theme ke saamne diye gaye three dots (...) par click karenge aur Edit Code option select karenge.
Ab Templates folder me jayenge aur Add a new file par click karke file ka naam page.demo.json rakh denge.
Ab Sections folder me jayenge aur Add a new file par click karke file ka naam demo-section.liquid rakh denge.
Ab demo-section.liquid file ke andar HTML, CSS, JavaScript aur Schema code add karenge.
Example:

<div class="demo-section">
  <h1>{{ section.settings.heading }}</h1>
</div>

<style>
.demo-section {
  background: black;
  color: white;
  padding: 20px;
}
</style>

<script>
document.querySelector('.demo-section').addEventListener('click', function() {
  alert('Section Clicked');
});
</script>

{% schema %}
{
"name": "Demo Section",
"settings": [
{
"type": "text",
"id": "heading",
"label": "Heading",
"default": "Hello Shopify"
}
]
}
{% endschema %}
Ab page.demo.json file open karenge aur usme section ko add karenge.
Example:
{
"sections": {
"demo": {
"type": "demo-section",
"settings": {}
}
},
"order": [
"demo"
]
}
Ab Shopify Admin Panel me Content → Pages par jayenge.
Uske baad Add Page par click karke ek naya page create karenge.
Page create karne ke baad Theme Template me page.demo select karenge.
Uske baad page ko save kar denge.
Ab demo-section.liquid section us page par show hone lagega.
Ab ye custom JSON template Shopify Online Store 2.0 me successfully create aur assign ho chuka hai.
