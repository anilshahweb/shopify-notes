How to Add Custom CSS in Shopify Website?
Shopify me custom CSS add karne ke liye:
Sabse pehle Shopify Admin Panel me Online Store par jayenge.
Uske baad current theme ke saamne diye gaye three dots (…) par click karenge aur Edit Code option select karenge.
Ab Assets folder me jayenge aur Add a new asset par click karke ek new CSS file create karenge:
custom.css
Ab Layout folder ke andar theme.liquid file open karenge.
Closing </head> tag se pehle custom CSS file ko include karenge:
{{ 'custom.css' | asset_url | stylesheet_tag }}
Ab custom.css file ke andar jo bhi CSS code likhenge, wo Shopify theme par apply ho jayega.
Example:
.custom-button {
background: black;
color: white;
}
