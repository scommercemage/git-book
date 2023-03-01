# Magento 2 Lazy Load Image

### <mark style="color:blue;">Installation and User Guide for Magento 2 Lazy Load Image</mark>&#x20;

**Table of Contents**

1. [_Installation_ ](magento-2-lazy-load-image.md#\_toc\_250005)__
   * _Installation via app/code_
   * _Installation via Composer_
2. [_Configuration Settings for Optimiser Base_ ](magento-2-lazy-load-image.md#\_toc\_250004)__
   * _General Settings_&#x20;
3. __[_Configuration Settings for Lazy Loading_ ](magento-2-lazy-load-image.md#\_toc\_250002)__
   * _General Settings_&#x20;
4. [_Front-end Screenshots_ ](magento-2-lazy-load-image.md#\_toc\_250000)__
   * _Lazy Loading on the Homepage_&#x20;
   * _Home Page Excluded from Lazy Loading_&#x20;
   * _Lazy Loading on the Category Page_&#x20;
   * _Lazy Loading on the Search Page_&#x20;
   * _Lazy Loading on the Cart Page._&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_toc_250005" id="_toc_250005"></a>

* <mark style="color:orange;">**Installation via app/code:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% content-ref url="../installation-via-composer.md" %}
[installation-via-composer.md](../installation-via-composer.md)
{% endcontent-ref %}

### <mark style="color:blue;">Configuration Settings for Optimiser Base</mark> <a href="#_toc_250004" id="_toc_250004"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Optimiser Base**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250003" id="_toc_250003"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com).

![](../../.gitbook/assets/config\_speed.png)

### <mark style="color:blue;">Configuration Settings for Lazy Loading</mark> <a href="#_toc_250002" id="_toc_250002"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Lazy Loading**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250001" id="_toc_250001"></a>

* **Enabled -** Select “Yes” or **“**No**”** to enable or disable the module.
* **Loading Icon –** Show a preview image before the real image loads.
* **Skip Images Count by page category –** Enter a valid image count to skip the images from lazy load. Based on the count this option will decide how many images to load without lazy loading.
* **Ignore Images that Contain –** Provide a part of an image tag content into the field to exclude the image from the lazy load.
* **Exclude Pages –** Select the page(s) from multi-select options to exclude from the lazy load.
* **Lazy loading for product only on category page –** Select “Yes” to apply lazy load on product images only on category page.

![](../../.gitbook/assets/gen\_lazy1.png)

![](../../.gitbook/assets/gen\_lazy2.png)



### <mark style="color:blue;">Front-end Screenshots</mark> <a href="#_toc_250000" id="_toc_250000"></a>

* <mark style="color:orange;">**Lazy Loading on the Homepage –**</mark>** ** To implement lazy loading on the homepage, enable the module from **Admin > Stores > Configuration > Lazy Loading- Enable "Yes".**

![](<../../.gitbook/assets/9 (14)>)

* <mark style="color:orange;">**Home Page Excluded from Lazy Loading –**</mark>** ** You can exclude homepage images from lazy loading by selecting option "Home Page" from **Admin > Stores > Configuration > Lazy Loading > Exclude Pages .**

![](<../../.gitbook/assets/10 (25)>)

* <mark style="color:orange;">**Lazy Loading on the Category Page –**</mark> To implement lazy loading on the category page, enable the module from **Admin > Stores > Configuration > Lazy Loading - Enable "Yes"**.

![](<../../.gitbook/assets/11 (28)>)

* <mark style="color:orange;">**Lazy Loading on the Search Page –**</mark>** ** You can implement lazy loading on search page from **Admin > Stores > Configuration > Lazy Loading - Enable** "**Yes**".

![](<../../.gitbook/assets/12 (11)>)

* <mark style="color:orange;">**Lazy Loading on the Cart Page –**</mark> You can implement lazy loading on the cart page by enabling the module from **Admin > Stores > Configuration > Lazy Loading- Enable "Yes".**

![](<../../.gitbook/assets/13 (9)>)

If you have a question related to this extension please check out our [**FAQ section**](https://www.scommerce-mage.com/magento-2-lazy-load-image-extension.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
