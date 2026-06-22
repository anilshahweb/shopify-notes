How to Create Custom Snippets in Shopify 2.0?
Shopify Online Store 2.0 me custom snippet create karne ke liye:
Sabse pahle Shopify Admin Panel me Online Store → Themes par jayenge.
Uske baad current theme ke saamne diye gaye three dots (...) par click karenge aur Edit Code option select karenge.
Ab Snippets folder me jayenge aur Add a new file par click karke file ka naam custom-snippet.liquid rakh denge.
Ab custom-snippet.liquid file ke andar jo reusable code use karna ho, use add kar denge.
Example:

<div class="custom-snippet">
  <h2>{{ heading }}</h2>
  <p>{{ description }}</p>
</div>
Ab jis bhi section, template ya file me snippet ko use karna ho, us file ko open karenge.
Uske baad snippet ko render karne ke liye niche diya gaya code add karenge.
Example:
{% render 'custom-snippet',
  heading: 'Welcome to Shopify',
  description: 'This is a custom snippet.'
%}
Ab file ko save kar denge.
Uske baad storefront ko refresh karenge.
Ab custom snippet ka content us jagah par show hone lagega jahan snippet ko render kiya gaya hai.
Ab ye snippet Shopify Online Store 2.0 theme me multiple places par reusable component ke roop me use ho jayega.
