# Magento 2 Previously Ordered Products

### <mark style="color:blue;">Installation and User Guide for Magento 2 Reorder Previous Products Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-previously-ordered-products.md#\_toc\_250007)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Reorder Previous Products_ ](magento-2-previously-ordered-products.md#\_toc\_250006)
   * _General Settings_&#x20;
3. [_Hide One or Multiple Columns from the Previous Purchases Grid_](magento-2-previously-ordered-products.md#\_toc\_250004)
4. [_Front-end Site view_ ](magento-2-previously-ordered-products.md#\_toc\_250003)
   * _Previous Purchase Grid_&#x20;
   * _Hide Columns in the Previous Purchase Grid_&#x20;
   * _Add One or Multiple Products to Cart Directly From the Grid_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_toc_250007" id="_toc_250007"></a>

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

### <mark style="color:blue;">Configuration Settings forReorder Previous Products</mark> <a href="#_toc_250006" id="_toc_250006"></a>

#### Go to Admin> Stores> Configuration> Scommerce Configuration> Global Site Tag (gtag.js)

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250005" id="_toc_250005"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Hidden Columns –** You can hide one or multiple columns from the previous purchases grid. The columns that can be hidden are listed below:-                                                                                                &#x20;
* #### Thumbnail
* **Qty**(Quantity)
* #### Last Order Date
* #### Last Order Number
* #### Last Order Price(Ex. tax)
* #### Last Order Price(Incl. tax)
* #### Current Product Price
* #### Number of Orders

![](../../.gitbook/assets/reorder\_general.jpg)

### <mark style="color:blue;">Hide One or Multiple Columns from the Previous Purchases Grid</mark> <a href="#_toc_250004" id="_toc_250004"></a>

To hide one or multiple columns from the previous purchases grid please go to **Admin> Stores> Configuration> Scommerce Configuration> Previous Products.**Find the setting named Hidden Columns select one or multiple columns that you want to hide and save the settings.

![](../../.gitbook/assets/reorder\_general2.jpg)

### <mark style="color:blue;">Front-end Siteview</mark> <a href="#_toc_250003" id="_toc_250003"></a>

#### <mark style="color:orange;">Previous Purchase Grid</mark> <a href="#_toc_250002" id="_toc_250002"></a>

Go to the website and login to your account then navigate to **My Account** section and from the left menu click on My Previous Products. This grid shows detailed information about all off your previous purchases. You can easily navigate through the list with the help of pagination and selectors. The previous purchases grid will open as shown in the image below:-

![](<../../.gitbook/assets/3 (63)>)

#### <mark style="color:orange;">Hide Columns in the Previous Purchase Grid</mark> <a href="#_toc_250001" id="_toc_250001"></a>

Please go to **Admin> Stores> Configuration> Scommerce Configuration >Previous Products** and select the columns in **Hidden Columns** that you want to hide. For eg:- we have selected Thumbnail, QTY, Last Order Price(Incl taxes) and Last Order Price(Excl Taxes). You can see in the image below that these columns are now hidden in the grid.

![](<../../.gitbook/assets/4 (43)>)

#### <mark style="color:orange;">Add One or Multiple Products to Cart Directly from the Grid</mark> <a href="#_toc_250000" id="_toc_250000"></a>

If you want to add one product to cart then click on the checkbox in the selector column then click on Add to Cart from the rightmost column Whereas if you want to add multiple products to cart then select the products that you want to purchase then click on the Add All Selected to Cart button either on the top or bottom of the list.

If you have a question related to this extension please check out our [**FAQ section**](https://www.scommerce-mage.com/magento2-reorder-previous-products.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
