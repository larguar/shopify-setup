# Shopify Setup
A quick guide for my own reference so I can "start from scratch" without actually having to start from scratch. This list is specific to the [Combine](https://themes.shopify.com/themes/combine/styles/objects) theme in Shopify, but may work for others too.


## Table of Contents 
1. [Theme Content](#theme-content)
2. [Custom Files](#custom-files)


## Theme Content

### Edit default theme content
| Section            | Edit |
| :----------------- | :----------------- |
| General            | **Breadcrumb account**<br>Title: `My Account` |
| Collections        | |
| Products           | |
| Cart               | **Cart**<br>Note: `Gift Note` |
| Blog               | |
| Search             | |
| Customers          | |
| Gift card          | |
| Store availability | |
| Checkout & system  | |
| Accounts           | |


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
