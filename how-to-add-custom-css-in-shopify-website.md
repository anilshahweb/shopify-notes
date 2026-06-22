How to Add Custom CSS in Shopify Website?
Shopify me custom CSS add karne ke liye:
Sabse pahle Shopify Admin Panel me Online Store → Themes par jayenge.
Uske baad current theme ke saamne diye gaye three dots (...) par click karenge aur Edit Code option select karenge.
Ab Assets folder me jayenge aur Add a new file par click karke file ka naam custom.css rakh denge.
Ab Layout folder ke andar theme.liquid file open karenge.
Uske baad closing </head> tag se pahle custom CSS file ko include karne ke liye niche diya gaya code add karenge:
{{ 'custom.css' | asset_url | stylesheet_tag }}
Ab custom.css file ke andar jo bhi CSS code likhenge, wo Shopify theme par apply ho jayega.
Example:
.custom-button {
background: black;
color: white;
}
