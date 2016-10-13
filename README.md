category-color-extended
=======================

Extending WordPress Plugin "Category Color" (https://wordpress.org/plugins/category-color/) with an additional color field.

Easily set custom colors per Post Category and use the colors in your Wordpress templates to spice up your theme.

## Description

Easily set custom colors per Post Category and use the colors in your Wordpress templates to spice up your theme. You can use it to color your Category names, your Post titles, background, lines, etc. in your Theme. Colors are always easily adjustable through your Category Edit screen.

This Form povides a second color field to be able to add background and accent colors to Categories.

## Installation

Please refer to the official documentation: https://codex.wordpress.org/Managing_Plugins

## How to us these colors

```php
<?php
    $category = get_the_category();
    $the_category_id = $category[0]->cat_ID;

    if(function_exists('rl_color_extended')){
        $rl_category_color_fg = rl_color_extended($the_category_id)['fg'];
        $rl_category_color_bg = rl_color_extended($the_category_id)['bg'];
    }
?>
```

Now you can use the colors in your template in an inline stylesheet. The variables `$rl_category_color_fg` and `$rl_category_color_bg` can be used in yout template.
