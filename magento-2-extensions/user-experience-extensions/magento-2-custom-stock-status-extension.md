# Magento 2 Custom Stock Status Extension

### <mark style="color:blue;">Installation and User Guide for Magento 2 Custom Stock Status Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-custom-stock-status-extension.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Custom Stock Status_ ](magento-2-custom-stock-status-extension.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Stock Status Rules Grid_&#x20;
   * _Add New Rule_&#x20;
   * _Custom Stock Status and Rule Name at Product Level_&#x20;
   * _Salable Quantity_&#x20;
   * _Assign Custom Stock Status Rule to Products Automatically or Manually_&#x20;
   * _Manually_&#x20;
   * _Automatically on Cron Run_&#x20;
   * _Multi Websites Selection_&#x20;
   * _Custom Stock Status Product Attribute_&#x20;
3. [_Front-end Site View_ ](magento-2-custom-stock-status-extension.md#\_bookmark14)
   * _Custom Stock Message on the Category & Search Pages_&#x20;
   * _Custom Stock Message for Simple Products on the Product Page_&#x20;
   * _Custom Stock Message for Configurable Products on the Product Page_&#x20;
   * _Custom Stock Message on the Cart & Checkout Pages_&#x20;
   * _Custom Stock Message on Related, Cross-sells and Up-sells Products_&#x20;
   * _Status Message in the Order Confirmation Email_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Installation via app/code:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% content-ref url="../installation-via-composer.md" %}
[installation-via-composer.md](../installation-via-composer.md)
{% endcontent-ref %}

### <mark style="color:blue;">Configuration Settings for Custom Stock Status</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Custom Stock Status**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Custom Stock Message on Related Product –** Select “Yes” to enable the custom stock message on related product.
* **Custom Stock Message on Up-Sells Product –** Select “Yes” to enable the custom stock message on Up-sells product.
* **Custom Stock Message or Cross-Sells Product –** Select “Yes” to enable the custom stock message on Cross-sells product.
* **Cron Schedule –** Schedule cron job to automatically update custom stock status based on correct rule.

![](../../.gitbook/assets/stock\_general.jpg)

<mark style="color:orange;">**Stock Status Rules Grid –**</mark> This will be a grid in admin > Catalog > Stock Status Rules, with below column: -

* **ID:** ID, this is auto generated and non-editable
* **Rule Name:** Name of the rule
* **Status:** Status of the rule, Enabled/Disabled
* **Website:** Name of the website
* **Priority:** Priority of the rule
* **Action:** Edit/Delete

![](../../.gitbook/assets/stock\_rulegrid.jpg)

* **Add New Rule –** You can add new rule by clicking “Add New Rule” from **Admin > Catalog > Products > Stock Status Rules >Add New Rule**, it redirects to the detailed view for Rule from where you can create a new rule by filling the required fields.
* **Rule Name -** Add generic name for rule
* **Website -** Select website from multi-select, from here you can select multiple website
* **Enable -** Please enable/disable rule by slider
* **Priority -** You can add priority (int) for the rule. In case of conflicting rules for a product the lowest number will have highest priority like 0 will be given priority over 1. If no priority defined then any random rule will apply
* **Conditions -** Add the conditions to match, leave blank for all products
* **Default Stock Message -** You can select default stock message from the drop- down, which will be shown on the frontend and replace availability (In Stock / Out Stock) message.
* **Apply Stock Quantity Ranges:** You can enable it by turning "On" this option. If it is enabled then it shows below grid where you can define stock ranges and corresponding status.

![](<../../.gitbook/assets/9 (19)>)

### <mark style="color:blue;">Add New Stock Status Rules - Admin Site View</mark>

![](<../../.gitbook/assets/10 (31)>)

* <mark style="color:orange;">**Custom Stock Status and Rule Name at Product Level -**</mark> You can view the associated rule to product from **Admin > Catalog > Products > Select product.**

![](<../../.gitbook/assets/11 (10)>)

* <mark style="color:orange;">**Salable Quantity -**</mark> On product save it updates the stock status message based on the salable quantity and the quantity rule. To view salable quantity go to **Admin > Catalog> products > Select Product > Product Salable Quantity.**

![](<../../.gitbook/assets/12 (12)>)

#### <mark style="color:orange;">Assign Custom Stock Status Rule to Products Automatically or Manually</mark> <a href="#_bookmark9" id="_bookmark9"></a>

* <mark style="color:blue;">**Manually -**</mark> You can assign rules to product manually from **Admin > Catalog> Products > Select Product > Rule Name -** Select rule from the “Rule Name” drop-down list.

![](<../../.gitbook/assets/13 (2)>)

* <mark style="color:blue;">**Automatically on Cron Run -**</mark> You can schedule the Cron job from **Admin > Stores > Configuration > Scommerce Configuration > Custom Stock Status**, on cron run the rule will be automatically assigned to products based on the matched condition and set the correct message.

<mark style="color:orange;">**Multi Websites Selection -**</mark> It fully supports multi-store and websites, you can select websites from **Admin > Catalog > Products > Select Product > Product in Websites-** check websites.

![](<../../.gitbook/assets/14 (6)>)

* <mark style="color:orange;">**Custom Stock Status Product Attribute -**</mark> You can add values to custom stock status product attribute from **Admin > Store >Attribute > Product> Product Attribute>Select - custom\_stock\_status > Properties > Add option**, the added values will be populated in the default /custom stock status message drop-down.

![](../../.gitbook/assets/stock\_front.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark14" id="_bookmark14"></a>

* <mark style="color:orange;">**Custom Stock Message on the Category & Search Pages –**</mark> In the below image you can see the stock message for the products.

![](<../../.gitbook/assets/16 (5)>)

![](<../../.gitbook/assets/17 (15)>)

* <mark style="color:orange;">**Custom Stock Message for Simple Product**</mark><mark style="color:orange;">s</mark> <mark style="color:orange;"></mark><mark style="color:orange;">**on the Product Page –**</mark> It displays stock status message for simple product based on salable qty and quantity ranges rule.

![](<../../.gitbook/assets/18 (10)>)

* #### <mark style="color:orange;">Custom Stock Message for Configurable Products on the Product Page :-</mark> For configurable product it displays stock status based on variant selection. <a href="#_bookmark17" id="_bookmark17"></a>

![](<../../.gitbook/assets/19 (11)>)

* <mark style="color:orange;">**Custom Stock Message on the Cart & Checkout Pages –**</mark> You can see the stock status message on cart and checkout pages.

![](<../../.gitbook/assets/20 (7)>)

* <mark style="color:orange;">**Custom Stock Message on Related, Cross-sells and Up-sells Products –**</mark> When you select “Yes” for “**Custom Stock Message on Related Product / Up-Sells/ Cross- Sells**” from **Admin > Stores > Configuration > Scommerce Configuration > Custom Stock Status,** then it shows stock status message on related/up-sells/cross- sells products.

![](../../.gitbook/assets/stock\_front2.jpg)

* <mark style="color:orange;">**Status Message in the Order Confirmation Email –**</mark> In the order confirmation email you can see the added stock status message.

![](../../.gitbook/assets/stock\_front3.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-custom-stock-status.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
