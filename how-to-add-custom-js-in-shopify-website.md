How to Add Custom JS in Shopify?
Shopify me custom JavaScript add karne ke liye:
Sabse pahle Shopify Admin Panel me Online Store → Themes par jayenge.
Uske baad current theme ke saamne diye gaye three dots (...) par click karenge aur Edit Code option select karenge.
Ab Assets folder me jayenge aur Add a new file par click karke file ka naam custom.js rakh denge.
Ab Layout folder ke andar theme.liquid file open karenge.
Uske baad closing </head> tag se pahle custom JS file ko include karne ke liye niche diya gaya code add karenge:
{{ 'custom.js' | asset_url | script_tag }}
Ab custom.js file ke andar jo bhi JavaScript code likhenge, wo Shopify theme par apply ho jayega.
Example:
alert('Hello Testing');
