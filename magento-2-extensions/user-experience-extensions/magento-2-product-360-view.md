# Magento 2 Product 360 view



### <mark style="color:blue;">Installation and User Guide for Magento 2 Product 360 view extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-product-360-view.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for <mark style="color:blue;">A</mark>ntispam Extension_](magento-2-product-360-view.md#\_bookmark3)
   * _General Settings_&#x20;
   * _360 view settings_
3. [_Add 360 View Images to a Product_](magento-2-product-360-view.md#add-360-view-images-to-products)
4. [_Frontend_](magento-2-product-360-view.md#frontend)

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

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

### <mark style="color:blue;">Configuration Settings for Product 360 view</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Product 360 view**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).

![](../../.gitbook/assets/360x\_890x.png)

#### <mark style="color:orange;">360 View Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enable Controls –** Select “Yes” or “No” to enable or disable the navigation controls on 360view image.
* **Enable Auto Play –** Select “Yes” or “No” to enable or disable automatically spin 360 view image on page load .
* **Autoplay Speed –** Enter the speed for automatic spin of 360 view image. It controls the Speed of changing frames for autoplay in milliseconds
* **Drag Speed –** Enter the speed with which user can drag on the image. It controls the Speed Factor of changing frames on drag event
* **Reverse Autoplay –** Select “Yes” or “No” to enable or disable reverse autoplay.

![](../../.gitbook/assets/360\_890x.png)

* **Enable Fullscreen Button –** Select “Yes” or “No” to open or close 360 view spin in fullscreen.
* **Magnifier –** Select the Magnifier stregnth from dropdown which controls the zoom for the image.
* **Button Position –** Select the placement of 360 view button on the frontend.
* **Custom Button Image–** Upload custom 360 view button image.
* **Max Popup Width –** Enter the maximum width of 360 view popup.

![](../../.gitbook/assets/361\_890x.png)

### <mark style="color:blue;">**Add 360 View Images to a Product**</mark>

Login to admin panel and go to Catalog>Products, select a product then click **edit** from the Action column. Scroll down to find '360 View Images' and upload the images as shown in the below screengrab:-

![](../../.gitbook/assets/360view\_890x.png)

### <mark style="color:blue;">**Frontend**</mark>

#### <mark style="color:orange;">360 View</mark>  <a href="#bookmark4" id="bookmark4"></a>

![](../../.gitbook/assets/360\_1\_890x.png)

#### <mark style="color:orange;">360 View Full Screen Image</mark> <a href="#bookmark4" id="bookmark4"></a>

![](../../.gitbook/assets/360\_2\_890x.png)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-product-360-view.html#customfaq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
