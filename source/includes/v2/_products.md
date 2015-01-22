# Products #

This section lists all API that can be used to create, edit or otherwise manipulate products.

@TODO

<aside class="warning">
Documentation under construction.
</aside>

## Products Properties ##

|        Attribute        |   Type  |                                                                                                                           Description                                                                                                                            |
| ----------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `title`                 | string  | Product name                                                                                                                                                                                                                                                     |
| `id`                    | integer | Product ID (post ID) <i class="label label-info">read-only</i>                                                                                                                                                                                                   |
| `created_at`            | string  | UTC DateTime when the product was created <i class="label label-info">read-only</i>                                                                                                                                                                              |
| `updated_at`            | string  | UTC DateTime when the product was last updated <i class="label label-info">read-only</i>                                                                                                                                                                         |
| `type`                  | string  | Product type. By default in WooCommerce the following types are available: `simple`, `grouped`, `external`, `variable`. Default is `simple`                                                                                                                      |
| `status`                | string  | Product status (post status)                                                                                                                                                                                                                                     |
| `downloadable`          | boolean | If the product is downloadable or not. Downloadable products give access to a file upon purchase                                                                                                                                                                 |
| `virtual`               | boolean | If the product is virtual or not. Virtual products are intangible and aren't shipped                                                                                                                                                                             |
| `permalink`             | string  | Product URL (post permalink) <i class="label label-info">read-only</i>                                                                                                                                                                                           |
| `sku`                   | string  | SKU refers to a Stock-keeping unit, a unique identifier for each distinct product and service that can be purchased                                                                                                                                              |
| `price`                 | float   | Current product price. This is setted from `regular_price` and `sale_price` <i class="label label-info">read-only</i>                                                                                                                                            |
| `regular_price`         | float   | Product regular price                                                                                                                                                                                                                                            |
| `sale_price`            | float   | Product sale price                                                                                                                                                                                                                                               |
| `sale_price_dates_from` | float   | Sets the sale start date. Date in the `YYYY-MM-DD` format <i class="label label-info">write-only</i>                                                                                                                                                             |
| `sale_price_dates_to`   | float   | Sets the sale end date. Date in the `YYYY-MM-DD` format <i class="label label-info">write-only</i>                                                                                                                                                               |
| `price_html`            | string  | Price formatted in HTML, e.g. `<del><span class=\"amount\">&#36;&nbsp;3.00</span></del> <ins><span class=\"amount\">&#36;&nbsp;2.00</span></ins>` <i class="label label-info">read-only</i>                                                                      |
| `taxable`               | boolean | Show if the product is taxable or not <i class="label label-info">read-only</i>                                                                                                                                                                                  |
| `tax_status`            | string  | Tax status. The options are: `taxable`, `shipping` (Shipping only) and `none`                                                                                                                                                                                    |
| `tax_class`             | string  | Tax class                                                                                                                                                                                                                                                        |
| `managing_stock`        | boolean | Enable stock management at product level                                                                                                                                                                                                                         |
| `stock_quantity`        | integer | Stock quantity. If is a variable product this value will be used to control stock for all variations, unless you define stock at variation level.                                                                                                                |
| `in_stock`              | boolean | Controls whether or not the product is listed as "in stock" or "out of stock" on the frontend.                                                                                                                                                                   |
| `backorders_allowed`    | boolean | Shows if backorders are allowed <i class="label label-info">read-only</i>                                                                                                                                                                                        |
| `backordered`           | boolean | Shows if a product is on backorder (if the product have the stock_quantity negative) <i class="label label-info">read-only</i>                                                                                                                                   |
| `backorders`            | mixed   | If managing stock, this controls whether or not backorders are allowed. If enabled, stock quantity can go below 0. The options are: `false` (Do not allow), `notify` (Allow, but notify customer), and `true` (Allow) <i class="label label-info">write-only</i> |
| `sold_individually`     | boolean | When `true` this only allow one item to be bought in a single order                                                                                                                                                                                              |
| `purchaseable`          | boolean | Shows if the product can be bought <i class="label label-info">read-only</i>                                                                                                                                                                                     |
| `featured`              | boolean | Featured Product                                                                                                                                                                                                                                                 |
| `visible`               | boolean | Shows whether or not the product is visible in the catalog <i class="label label-info">read-only</i>                                                                                                                                                             |
| `catalog_visibility`    | string  | Catalog visibility. The following options are available: `visible` (Catalog and search), `catalog` (Only in catalog), `search` (Only in search) and `hidden` (Hidden from all)                                                                                   |
| `on_sale`               | boolean | Shows if the product is on sale or not <i class="label label-info">read-only</i>                                                                                                                                                                                 |
| `weight`                | string  | Product weight in decimal format                                                                                                                                                                                                                                 |
| `dimensions`            | array   | List of the product dimensions. See [Dimensions Properties](#dimensions-properties)                                                                                                                                                                              |
| `shipping_required`     | boolean | Shows if the product need to be shipped or not <i class="label label-info">read-only</i>                                                                                                                                                                         |
| `shipping_taxable`      | boolean | Shows whether or not the product shipping is taxable <i class="label label-info">read-only</i>                                                                                                                                                                   |
| `shipping_class`        | string  | Shipping class slug. Shipping classes are used by certain shipping methods to group similar products                                                                                                                                                             |
| `shipping_class_id`     | integer | Shipping class ID <i class="label label-info">read-only</i>                                                                                                                                                                                                      |
| `description`           | string  | Product description                                                                                                                                                                                                                                              |
| `short_description`     | string  | Product short description                                                                                                                                                                                                                                        |
| `reviews_allowed`       | boolean | Shows/define if reviews are allowed                                                                                                                                                                                                                              |
| `average_rating`        | string  | Reviews average rating <i class="label label-info">read-only</i>                                                                                                                                                                                                 |
| `rating_count`          | integer | Amount of reviews that the product have <i class="label label-info">read-only</i>                                                                                                                                                                                |
| `related_ids`           | array   | List of related products IDs (`integer`) <i class="label label-info">read-only</i>                                                                                                                                                                               |
| `upsell_ids`            | array   | List of up-sell products IDs (`integer`). Up-sells are products which you recommend instead of the currently viewed product, for example, products that are more profitable or better quality or more expensive                                                  |
| `cross_sell_ids`        | array   | List of cross-sell products IDs. Cross-sells are products which you promote in the cart, based on the current product                                                                                                                                            |
| `parent_id`             | integer | Product parent ID (post_parent)                                                                                                                                                                                                                                  |
| `categories`            | array   | List of product categories names (`string`). In write-mode need to pass a array of categories IDs (`integer`) ([uses wp_set_object_terms()](http://codex.wordpress.org/Function_Reference/wp_set_object_terms))                                                  |
| `tags`                  | array   | List of product tags names (`string`). In write-mode need to pass a array of tags IDs (`integer`) ([uses wp_set_object_terms()](http://codex.wordpress.org/Function_Reference/wp_set_object_terms))                                                              |
| `images`                | array   | List of products images. See [Images Properties](#images-properties)                                                                                                                                                                                             |
| `featured_src`          | string  | Featured image URL <i class="label label-info">read-only</i>                                                                                                                                                                                                     |
| `attributes`            | array   | List of product attributes. See [Attributes Properties](#attributes-properties)                                                                                                                                                                                  |
| `downloads`             | array   | List of downloadable files. See [Downloads Properties](#downloads-properties)                                                                                                                                                                                    |
| `download_limit`        | integer | Amount of times the product can be downloaded. In write-mode you can sent a blank string for unlimited re-downloads. e.g `''`                                                                                                                                    |
| `download_expiry`       | integer | Number of days that the customer has up to be able to download the product. In write-mode you can sent a blank string for never expiry. e.g `''`                                                                                                                 |
| `download_type`         | string  | Download type, this controls the [schema](http://schema.org/). The available options are: `''` (Standard Product), `application` (Application/Software) and `music` (Music)                                                                                      |
| `purchase_note`         | string  | Optional note to send the customer after purchase.                                                                                                                                                                                                               |
| `total_sales`           | integer | Amount of sales <i class="label label-info">read-only</i>                                                                                                                                                                                                        |
| `variations`            | array   | List of products variations. See [Variations Properties](#variations-properties)                                                                                                                                                                                 |
| `parent`                | array   | List the product parent data when query for a variation <i class="label label-info">read-only</i>                                                                                                                                                                |
| `product_url`           | string  | Product external URL. Only for `external` products <i class="label label-info">write-only</i>                                                                                                                                                                    |
| `button_text`           | string  | Product external button text. Only for `external` products <i class="label label-info">write-only</i>                                                                                                                                                            |

### Dimensions Properties ###

| Attribute |  Type  |                      Description                       |
| --------- | ------ | ------------------------------------------------------ |
| `length`  | string | Product length in decimal format                       |
| `width`   | string | Product width in decimal format                        |
| `height`  | string | Product height in decimal format                       |
| `unit`    | string | Product name <i class="label label-info">read-only</i> |

### Images Properties ###

|  Attribute   |   Type  |                                      Description                                       |
| ------------ | ------- | -------------------------------------------------------------------------------------- |
| `id`         | integer | Image ID (attachment ID)                                                               |
| `created_at` | string  | UTC DateTime when the image was created <i class="label label-info">read-only</i>      |
| `updated_at` | string  | UTC DateTime when the image was last updated <i class="label label-info">read-only</i> |
| `src`        | string  | Image URL. In write-mode you can use to send new images                                |
| `title`      | string  | Image title (attachment title) <i class="label label-info">read-only</i>               |
| `alt`        | string  | Image alt text (attachment image alt text) <i class="label label-info">read-only</i>   |
| `position`   | integer | Image position. `0` means that the image is featured                                   |

### Attributes Properties ###

|  Attribute  |   Type  |                                            Description                                             |
| ----------- | ------- | -------------------------------------------------------------------------------------------------- |
| `name`      | string  | Attribute name                                                                                     |
| `slug`      | string  | Attribute slug                                                                                     |
| `position`  | string  | Attribute position                                                                                 |
| `visible`   | boolean | Shows/define if the attribute is visible on the "Additional Information" tab in the product's page |
| `variation` | boolean | Shows/define if the attribute can be used as variation                                             |
| `options`   | array   | List of available attributes names                                                                 |
| `position`  | integer | List of terms of the attribute in the product                                                      |

### Downloads Properties ###

| Attribute |  Type  |                             Description                             |
| --------- | ------ | ------------------------------------------------------------------- |
| `id`      | string | File ID (file md5 hash) <i class="label label-info">read-only</i>   |
| `name`    | string | File name                                                           |
| `file`    | string | File URL. In write-mode you can use this property to send new files |

### Variations Properties ###

|        Attribute        |   Type  |                                                                                              Description                                                                                               |
| ----------------------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `id`                    | integer | Variation ID (post ID) <i class="label label-info">read-only</i>                                                                                                                                       |
| `created_at`            | string  | UTC DateTime when the variation was created <i class="label label-info">read-only</i>                                                                                                                  |
| `updated_at`            | string  | UTC DateTime when the variation was last updated <i class="label label-info">read-only</i>                                                                                                             |
| `downloadable`          | boolean | If the variation is downloadable or not. Downloadable variations give access to a file upon purchase                                                                                                   |
| `virtual`               | boolean | If the variation is virtual or not. Virtual variations are intangible and aren't shipped                                                                                                               |
| `permalink`             | string  | Variation URL (post permalink) <i class="label label-info">read-only</i>                                                                                                                               |
| `sku`                   | string  | SKU refers to a Stock-keeping unit, a unique identifier for each distinct product and service that can be purchased                                                                                    |
| `price`                 | float   | Current variation price. This is setted from `regular_price` and `sale_price` <i class="label label-info">read-only</i>                                                                                |
| `regular_price`         | float   | Variation regular price                                                                                                                                                                                |
| `sale_price`            | float   | Variation sale price                                                                                                                                                                                   |
| `sale_price_dates_from` | float   | Sets the sale start date. Date in the `YYYY-MM-DD` format <i class="label label-info">write-only</i>                                                                                                   |
| `sale_price_dates_to`   | float   | Sets the sale end date. Date in the `YYYY-MM-DD` format <i class="label label-info">write-only</i>                                                                                                     |
| `taxable`               | boolean | Show if the variation is taxable or not <i class="label label-info">read-only</i>                                                                                                                      |
| `tax_status`            | string  | Tax status. The options are: `taxable`, `shipping` (Shipping only) and `none`                                                                                                                          |
| `tax_class`             | string  | Tax class                                                                                                                                                                                              |
| `managing_stock`        | boolean | Enable stock management at variation level                                                                                                                                                             |
| `stock_quantity`        | integer | Stock quantity. If is a variable variation this value will be used to control stock for all variations, unless you define stock at variation level.                                                    |
| `in_stock`              | boolean | Controls whether or not the variation is listed as "in stock" or "out of stock" on the frontend.                                                                                                       |
| `backordered`           | boolean | Shows if a variation is on backorder (if the variation have the stock_quantity negative) <i class="label label-info">read-only</i>                                                                     |
| `purchaseable`          | boolean | Shows if the variation can be bought <i class="label label-info">read-only</i>                                                                                                                         |
| `visible`               | boolean | Shows whether or not the product parent is visible in the catalog <i class="label label-info">read-only</i>                                                                                            |
| `on_sale`               | boolean | Shows if the variation is on sale or not <i class="label label-info">read-only</i>                                                                                                                     |
| `weight`                | string  | Variation weight in decimal format                                                                                                                                                                     |
| `dimensions`            | array   | List of the variation dimensions. See [Dimensions Properties](#dimensions-properties)                                                                                                                  |
| `shipping_class`        | string  | Shipping class slug. Shipping classes are used by certain shipping methods to group similar products                                                                                                   |
| `shipping_class_id`     | integer | Shipping class ID <i class="label label-info">read-only</i>                                                                                                                                            |
| `images`                | array   | Variation featured image. See [Images Properties](#images-properties)                                                                                                                                  |
| `attributes`            | array   | List of variation attributes. Similar to a `simple` or `variable` product, but for `variation` indicate the attributes used to form the variation. See [Attributes Properties](#attributes-properties) |
| `downloads`             | array   | List of downloadable files. See [Downloads Properties](#downloads-properties)                                                                                                                          |
| `download_limit`        | integer | Amount of times the variation can be downloaded. In write-mode you can sent a blank string for unlimited re-downloads. e.g `''`                                                                        |
| `download_expiry`       | integer | Number of days that the customer has up to be able to download the varition. In write-mode you can sent a blank string for never expiry. e.g `''`                                                      |