# Shopify Setup
A quick guide for my own reference so I can "start from scratch" without actually having to start from scratch. This list is specific to the [Combine](https://themes.shopify.com/themes/combine/styles/objects) theme in Shopify, but should work for other themes with some adjustments.


## Table of Contents 
1. [Theme Content](#theme-content)
2. [Custom Files](#custom-files)
3. [Customize Setup](#customize-setup)
4. [Social Icons](#social-icons)


## Theme Content

### Edit default theme content
| Section            | Update |
| :----------------- | :----------------- |
| General            | **Breadcrumb account**<br>Title: `My Account` |
| Cart               | **Cart**<br>Note: `Gift Note` |


## Custom Files

### Edit code
Create 2 new files in the **assets** folder called `style.css.liquid` and `script.js.liquid`. Copy and paste all CSS and JS from previous theme.

**layout/theme.liquid**

Search for `{{ 'theme.css' | asset_url | stylesheet_tag }}` and paste below:
```
{% comment %} [LG] Custom CSS File {% endcomment %}
{{ 'style.css' | asset_url | stylesheet_tag }}
{% comment %} [LG] End Custom CSS File {% endcomment %}
```

Search for `</body>` and paste above:
```
{% comment %} [LG] Custom JS File {% endcomment %}
{{ 'script.js' | asset_url | script_tag }}
{% comment %} [LG] End Custom JS File {% endcomment %}
```


## Customize Setup

### Customize

**Theme settings**
| Section            | Settings |
| :----------------- | :----------------- |
| Typography         | **Headings**<br>Font family: `Harmonia Sans Regular`<br>Base size: `58px`<br>Line height: `0.9`<br>Letter spacing: `0`<br><br>**Body**<br>Font family: `Harmonia Sans Regular`<br>Base size: `16px`<br>Line height: `1.4`<br><br>**Section titles**<br>Font family: `Harmonia Sans Regular`<br>Base size: `22px` |
| Colors             | **Header**<br>Background: `#FFFFFF`<br>Text: `#1E1E1E`<br><br>**Body**<br>Primary background: `#FFFFFF`<br>Secondary background: `#FAFAFA`<br>Text: `#333333`<br><br>**Footer**<br>Background: `Primary color 1`<br>Text: `#FFFFFF` |
| Layout             | Maximum page width: `1360px`<br>Vertical space between sections: `120px`<br>Horizontal space between grid elements: `40px`<br>Widgets border radius: `0px`
| Forms & buttons    | **Form elements**<br>Border width: `1px`<br>Border radius: `5px`<br><br>**Buttons**<br>Border width: `1px`<br>Border radius: `30px` |
| Product card       | **Product thumbnail**<br>Media aspect ratio: `Tall (5:6)`<br>Fit media inside container: `true`<br>Container inner spacing: `0%`<br>Container background: `Transparent`<br>Container border: `Transparent`<br>Media border radius: `0px`<br>Slide through all product images: `false`<br>Link thumbnail to product page: `true`<br><br>**Product variants**<br>Variants style: `Dropdown`<br>Show color swatches: `true`<br>Color swatches labels: `color,colour,couleur,cor,colore,culoare,farbe,색,色,カラー,färg,farve,szín,barva`<br>Change product image based on selected variant: `true`<br><br>**Quick buy popup**<br>Enable quick buy popup: `false`<br>Hide popup after: `6s`<br>Popup background color: `Secondary Color 2`<br>Popup text color: `#FFFFFF`<br>Popup checkmark color: `#FFFFFF`<br>Popup radius: `0px`<br>Add box shadow: `false`<br><br>**Product rating**<br>Rating app: `Okendo`<br><br>**Product badges**<br>Show badges: `true`<br><br>**Sold out badge**<br>Background color: `#FFFFFF`<br>Text color: `#1E1E1E`<br><br>**Discount badge**<br>Show discount as: `Amount Saved`<br>Background color: `#FFFFFF`<br>Text color: `#1E1E1E`<br><br>**Custom badge 1**<br>Text:<br>Tag:<br>Background color: `#FFFFFF`<br>Text color: `#1E1E1E`<br><br>**Custom badge 2**<br>Text:<br>Tag:<br>Background color: `#FFFFFF`<br>Text color: `#1E1E1E`<br><br>**Custom badge 3**<br>Text:<br>Tag:<br>Background color: `#FFFFFF`<br>Text color: `#1E1E1E`<br><br>**Icon 1**<br>Icon metafield:<br>Label metafield:<br><br>**Icon 2**<br>Icon metafield:<br>Label metafield:<br><br>**Icon 3**<br>Icon metafield:<br>Label metafield: |
| Favicon            | Favicon image: `favicon_13627111-01ad-438f-9881-aab9fc6f42a7.png`
| Cart               | Cart type: `Drawer`<br>Enable cart notes: `true`<br>Show additional checkout buttons: `false`<br><br>**Media aspect ratio**<br>Aspect ratio: `Tall (5:6)`<br>Fit media inside container: `false`<br>Container background: `Transparent`<br><br>**Individual product recommendation**<br>Heading:<br>Product:<br><br>**Product recommendations**<br>Show cart recommendations: `false`<br>Heading:<br><br>**Shipping**<br>Show free shipping minimum amount: `true`<br>Free shipping minimum amount: `50`<br><br>**Gift wrapping**<br>Product:<br>Text: |
| Embellishments     | Show breadcrumb: `true`<br>Show ‘go to top’ button: `false` |
| SEO & performance  | Disable microdata schema: `false`<br>Improve product breadcrumb navigation: `false` |
| Currency format    | Show currency codes: `false` |
| Social             | Behance:<br>Discord:<br>Dribbble:<br>Email:<br>Phone:<br>Facebook: `https://www.facebook.com/pinultimate`<br>Flickr:<br>Instagram: `https://www.instagram.com/pinultimateco`<br>Kickstarter:<br>LinkedIn:<br>Medium:<br>Messenger:<br>Pinterest: `https://www.pinterest.com/pinultimateco`<br>RSS:<br>Snapchat:<br>Telegram:<br>TikTok: `https://www.tiktok.com/@pinultimate`<br>Vimeo:<br>WhatsApp:<br>Twitter:<br>YouTube:<br><br>**Custom link**<br>Icon:<br>Link: `https://www.threads.net/@pinultimateco` |

**App embeds**
| Section            | Settings |
| :----------------- | :----------------- |
| App embeds         | Product Options: `On`<br>Growave: `On`<br>Online store chat: `Off`<br>Klaviyo: `On` |

## Social Icons

### Edit code

**snippets/social-icons.liquid**

Search for `{%- if settings.social_custom != '' -%}` and add to the `<a>`:
```
class="threads"
```

Do the same for Facebook, Instagram, Pinterest, and TikTok:
```
class="facebook"
```
```
class="instagram"
```
```
class="pinterest"
```
```
class="tiktok"
```

In the `{%- if settings.social_custom != '' -%}` section, add above `<span class="icon" aria-hidden="true">`:
```
<span class="visually-hidden">Threads</span>
```

In the same section, replace `<img>` between `<span class="icon" aria-hidden="true"></span>`:
```
<svg fill="none" viewBox="0 0 448 512" xmlns="http://www.w3.org/2000/svg"><path d="M331.5 235.7c2.2 .9 4.2 1.9 6.3 2.8c29.2 14.1 50.6 35.2 61.8 61.4c15.7 36.5 17.2 95.8-30.3 143.2c-36.2 36.2-80.3 52.5-142.6 53h-.3c-70.2-.5-124.1-24.1-160.4-70.2c-32.3-41-48.9-98.1-49.5-169.6V256v-.2C17 184.3 33.6 127.2 65.9 86.2C102.2 40.1 156.2 16.5 226.4 16h.3c70.3 .5 124.9 24 162.3 69.9c18.4 22.7 32 50 40.6 81.7l-40.4 10.8c-7.1-25.8-17.8-47.8-32.2-65.4c-29.2-35.8-73-54.2-130.5-54.6c-57 .5-100.1 18.8-128.2 54.4C72.1 146.1 58.5 194.3 58 256c.5 61.7 14.1 109.9 40.3 143.3c28 35.6 71.2 53.9 128.2 54.4c51.4-.4 85.4-12.6 113.7-40.9c32.3-32.2 31.7-71.8 21.4-95.9c-6.1-14.2-17.1-26-31.9-34.9c-3.7 26.9-11.8 48.3-24.7 64.8c-17.1 21.8-41.4 33.6-72.7 35.3c-23.6 1.3-46.3-4.4-63.9-16c-20.8-13.8-33-34.8-34.3-59.3c-2.5-48.3 35.7-83 95.2-86.4c21.1-1.2 40.9-.3 59.2 2.8c-2.4-14.8-7.3-26.6-14.6-35.2c-10-11.7-25.6-17.7-46.2-17.8H227c-16.6 0-39 4.6-53.3 26.3l-34.4-23.6c19.2-29.1 50.3-45.1 87.8-45.1h.8c62.6 .4 99.9 39.5 103.7 107.7l-.2 .2zm-156 68.8c1.3 25.1 28.4 36.8 54.6 35.3c25.6-1.4 54.6-11.4 59.5-73.2c-13.2-2.9-27.8-4.4-43.4-4.4c-4.8 0-9.6 .1-14.4 .4c-42.9 2.4-57.2 23.2-56.2 41.8l-.1 .1z"/></svg>
```
