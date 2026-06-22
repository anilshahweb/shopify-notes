How to Create Custom Section in Shopify 2.0?
Shopify Online Store 2.0 me custom section create karne ke liye:
Sabse pahle Shopify Admin Panel me Online Store → Themes par jayenge.
Uske baad current theme ke saamne diye gaye three dots (...) par click karenge aur Edit Code option select karenge.
Ab Sections folder me jayenge aur Add a new file par click karke file ka naam custom-section.liquid rakh denge.
Ab custom-section.liquid file ke andar HTML, CSS, JavaScript aur Schema code add karenge.
Example:

<div class="custom-section">
  <h1>{{ section.settings.heading }}</h1>
</div>

<style>
.custom-section {
  background: black;
  color: white;
  padding: 20px;
}
</style>

<script>
document.querySelector('.custom-section').addEventListener('click', function() {
  alert('Section Clicked');
});
</script>

{% schema %}
{
"name": "Custom Section",
"settings": [
{
"type": "text",
"id": "heading",
"label": "Heading",
"default": "Hello Shopify"
}
],
"presets": [
{
"name": "Custom Section"
}
]
}
{% endschema %}
Ab Customize Theme par jayenge.
Uske baad Add Section par click karenge.
Wahan se Custom Section select karke page par add kar denge.
Ab ye section Shopify Online Store 2.0 theme me dynamically use ho jayega.
