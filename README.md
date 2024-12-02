# Shopify Setup
A quick guide for my own reference so I can "start from scratch" without actually having to start from scratch. This list is specific to the [Combine](https://themes.shopify.com/themes/combine/styles/objects) theme in Shopify, but should work for other themes with some adjustments.


## Table of Contents 
1. [Theme Content](#theme-content)
2. [Custom Files](#custom-files)
3. [Customize Setup](#customize-setup)


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
