How to Add Custom JS in Shopify?
Shopify me custom JavaScript add karne ke liye:
Sabse pehle Shopify Admin Panel me Online Store par jayenge.
Uske baad current theme ke saamne diye gaye three dots (⋯) par click karenge aur Edit Code option select karenge.
Ab Assets folder me jayenge aur Add a new asset par click karke ek new JavaScript file create karenge:
custom.js
Ab Layout folder ke andar theme.liquid file open karenge.
Closing </head> tag se pehle custom JS file ko include karenge:
{{ 'custom.js' | asset_url | script_tag }}
Ab custom.js file ke andar jo bhi JavaScript code likhenge, wo Shopify theme par apply ho jayega.
Example:
alert('Hello Testing');