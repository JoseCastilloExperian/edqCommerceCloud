# Summary
Experian offers an 

# Touchpoints
* Add/Edit Address
* Information (Shipping)
* Checkout (Billing)

# Experian Integration Files
Donwload the Shopify/Experian integration files.
Ope your prefered command line prompt "Bash" or "CMD" and locate the integration file root "Shopify".
Run the following command ``` npm run build```
Next locate "lib" folder; within the "lib" folder there will be "shopifySinglePage.js" and "edqShopify.js" files.

#### Pre-requisits
Install Node and npm

# Integration
## Steps
1. Download the file from "".
2. Log in to your Shopify Sandbox.
3. Add the following files into **"Asset"** section:
*	shopifySinglePage.js
*	edqShopify.js

![Assets](https://raw.githubusercontent.com/JoseCastilloExperian/edqCommerceCloud/master/ShpifyImages/Assets.png)

![AddAssets](https://raw.githubusercontent.com/JoseCastilloExperian/edqCommerceCloud/master/ShpifyImages/addAsset.png)

## How the integration works
There two separate files:

#### shopifySinglePage.js 

This file is a single integration page for cases where there's no multi-Address on the page.

#### edqShopify.js

This file is for cases where there's multi-Address on the page (Add/Edit Address touchpoint).

Touchpoint | Shopify file | Integration file
------------ | -------------
Add/Edit Address | templates/customers/addresses.liquid | edqShopify.js
Shipping Address | templates/checkout/shippingAddress.liquid | shopifySinglePage.js
Billing Address | templates/customers/billingAddress.liquid | shopifySinglePage.js

Adding the following line ```<script src="{{ 'edqShopify.js' | asset_url }}"></script>``` at the end of the file.

![AddAssets](https://raw.githubusercontent.com/JoseCastilloExperian/edqCommerceCloud/master/ShpifyImages/addAsset.png)


