# Magento 2 FAQ

### <mark style="color:blue;">Installation and User Guide for Magento 2 FAQ Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-faq.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for FAQ_ ](magento-2-faq.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Manage FAQ's_&#x20;
   * _Manage FAQ Category_&#x20;
3. [_Front-end Site view_ ](magento-2-faq.md#\_bookmark7)
   * _FAQ Categories_&#x20;
   * _FAQ Product_&#x20;

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

### <mark style="color:blue;">Configuration Settings for FAQ</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > FAQ**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Enable FAQ Site Wide –** Set “yes” to enable FAQ page.
* **Site Wide FAQ Title –** Title of FAQ page if FAQ for site enabled.
* **Enable FAQ for Products –** If this is set to yes then FAQ Tab will appear on product pages.
* **Product FAQ title –** Tab title on product page if FAQ for product enabled.
* **Admin Email –** Email to send notification about new questions created from product front page.
* **FAQ Email Template –** Email Template for sending to admin with the details when someone asks a question.

![](../../.gitbook/assets/faq\_general.jpg)

<mark style="color:orange;">**Manage FAQ's -**</mark> You can manage, update and add new FAQ's from **Admin > FAQ > Manage FAQ's**. To add new FAQ's follow the below settings:-

<mark style="color:blue;">**Add New FAQ:**</mark>** Add new FAQ > General Tab**

* **Status –** Status of FAQ Active/Inactive
* **Title –** Title for FAQ
* **Most Frequently –** Set "Yes" if the question is asked frequently.
* **Category –** Category for FAQ
* **Sort Order –** To define sort order for FAQ

![A screenshot of a social media post  Description automatically generated](<../../.gitbook/assets/10 (45)>)

<mark style="color:blue;">**Add FAQ Answer:**</mark> To add answer go to **Admin > FAQ > Manage FAQ's > Add new FAQ > Answer > Save FAQ.**

* **Answer –** Add answer to the FAQ

![A screenshot of a social media post  Description automatically generated](<../../.gitbook/assets/11 (25)>)

<mark style="color:blue;">**Add Meta Description /Keywords for FAQ's:**</mark> You can add meta description/keywords from **Admin > FAQ > Manage FAQ's > Add new FAQ > Search Engine Optimization.**

* **URL key –** URL for FAQ
* **Meta Keywords –** Keywords for FAQ
* **Meta Description –** Description for FAQ

![A screenshot of a social media post  Description automatically generated](<../../.gitbook/assets/12 (23)>)

<mark style="color:blue;">**Add Websites:**</mark> To add websites go to, **Admin > FAQ > Manage FAQ's > Add new FAQ > Websites.**

* **Stores view –** Select stores where FAQ will be visible

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/13 (4)>)

<mark style="color:blue;">**Select Products for FAQ:**</mark> You can select product from **Admin > FAQ > Manage FAQ's > Add new FAQ > Selected Products > Save FAQ.**

* **Select Product –** Select products to associated FAQ’s.

![](../../.gitbook/assets/faq\_selectproduct.jpg)

<mark style="color:orange;">**Manage FAQ Category:**</mark> You can manage, update and add new category for FAQ's from **Admin > FAQ > Add new FAQ Category**. Below is the configuration to add new FAQ category:-

<mark style="color:blue;">**Add New FAQ Category:**</mark>** Add new FAQ Category > General Tab**

* **Status –** Status of FAQ Category Active/Inactive
* **Title –** Title for FAQ Category
* **Category Icon –** Icon for Category
* **Sort Order –** To define sort order for FAQ

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/15 (10)>)

<mark style="color:blue;">**Add Meta Description/Keywords for FAQ Category:**</mark> You can add meta description/keywords from **Admin > FAQ > Manage FAQ's > Add new FAQ Category > Search Engine Optimization.**

* **URL Key –** URL for FAQ Category
* **Meta Keywords –** Keywords for FAQ Category
* **Meta Description –** Description for FAQ Category

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/16 (23)>)

<mark style="color:blue;">**FAQ Category in Websites:**</mark> To add websites go to, **Admin > FAQ > Manage FAQ's > Add new Category > FAQ Category in Websites.**

* **Stores view –** Select stores where FAQ will be visible.

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/17 (24)>)

### <mark style="color:blue;">Front-end Site view</mark> <a href="#_bookmark7" id="_bookmark7"></a>

* <mark style="color:orange;">**FAQ Categories -**</mark> When you enable the module and set "Yes" for " **Enable FAQ Site Wide**" from **Admin > Stores > Configuration > Scommerce Configuration> FAQ** , then on the front-end, it shows FAQ page with categories.

![](../../.gitbook/assets/faq\_front1.jpg)

* <mark style="color:orange;">**FAQ Product -**</mark> Select "Yes" for **"** Enable FAQ for Products" from **Admin > Stores > Configuration > Scommerce Configuration > FAQ**

![](../../.gitbook/assets/faq\_front2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-faq.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
