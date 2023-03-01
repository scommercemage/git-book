# Magento 2 AJAX Infinite Scroll

### <mark style="color:blue;">Installation and User Guide for Magento 2 AJAX Infinite Scroll</mark>&#x20;

**Table of Contents**

* &#x20;__ [_Installation_](magento-2-ajax-infinite-scroll.md#\_toc\_250007)__
  * _Installation via app/code_
  * _Installation via Composer_
* [_Configuration Settings for Optimiser Base_ ](magento-2-ajax-infinite-scroll.md#\_toc\_250006)__
  * _General Settings_&#x20;
* __[_Configuration Settings for Infinite Scrolling_ ](magento-2-ajax-infinite-scroll.md#\_toc\_250004)__
  * _General Settings_&#x20;
* [_Front-end Site View of Infinite Scroll_ ](magento-2-ajax-infinite-scroll.md#\_toc\_250002)__
  * _Infinite Scroll with ‘Load More Button’ on the Category Page_&#x20;
  * _Infinite Scroll with Auto Loading on the Category and Search Pages_&#x20;
  * _Auto Loading on the Category Page_&#x20;
  * _Auto Loading on the Search Page_&#x20;
  * _Infinite Scroll with ‘Load More Button’ and Page Number_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_toc_250007" id="_toc_250007"></a>

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

### <mark style="color:blue;">Configuration Settings for Optimiser Base</mark> <a href="#_toc_250006" id="_toc_250006"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Optimiser Base**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250005" id="_toc_250005"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)

![](../../.gitbook/assets/general\_infinite.png)

### <mark style="color:blue;">Configuration Settings for Infinite Scrolling</mark> <a href="#_toc_250004" id="_toc_250004"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Infinite Scrolling**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250003" id="_toc_250003"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **Loading Type -** Select loading type “Load Automatically” or “Load with Button”.
* **Button Label -** Enter button label. This will be shown only when the “Loading Type” is set to “Load with Button”.
* **Button Label Font Color -** Set font color for "Load with Button" which appears on site front-end.
* **Button Label Background Color -** Select button label background color. This will be shown only when the “Loading Type” is set to “Load with Button”.
* **Button Label Size –** Define font size for the “Load with Button” which appears on the site.
* **Display Page Numbers (Yes/No) –** Select “Yes” to show the page information on the side panel.
* **Grid Dom Class –** This is the class for grid view of product listing pages.
* **List Dom Class –** This is the class for list view of product listing pages.

![](../../.gitbook/assets/general\_infiniteloading.png)

### <mark style="color:blue;">Front-end Site View of Infinite Scroll</mark> <a href="#_toc_250002" id="_toc_250002"></a>

* <mark style="color:orange;">**Infinite Scroll with ‘Load More Button’ on the Category Page –**</mark>** ** You can display the “Load More Button” on the category page by selecting “Load with Button” option from **Admin > Stores > Configuration > Infinite Scrolling > Loading Type**.

![](<../../.gitbook/assets/3 (80)>)

* <mark style="color:orange;">**Infinite Scroll with Auto Loading on the Category and Search Pages –**</mark>** ** You can implement auto loading on the category and search pages by selecting the option "Load Automatically" from **Admin > Stores > Configuration > Infinite Scrolling > Loading Type**.
* <mark style="color:orange;">**Auto Loading on the Category Page**</mark>

### &#x20;<a href="#_toc_250001" id="_toc_250001"></a>

![](<../../.gitbook/assets/4 (15)>)

* <mark style="color:orange;">**Auto Loading on the Search Page**</mark>

<mark style="color:orange;">****</mark>

![](<../../.gitbook/assets/5 (70)>)

* <mark style="color:orange;">**Infinite Scroll with ‘Load More Button’ and Page Number –**</mark>** ** To display Load More Button with page numbers on category and search pages first select option “Load with Button” from **Admin > Stores > Configuration > Infinite Scrolling > Loading Type** and then select “Yes “ from **Admin > Stores > Configuration > Infinite Scrolling > Display Page Numbers**. This will display page numbers with Load More Button as shown in screen grab below.

![](<../../.gitbook/assets/6 (62)>)

If you have a question related to this extension please check out our [**FAQ section**](https://www.scommerce-mage.com/magento-2-infinite-scroll.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
