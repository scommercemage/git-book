# Magento 2 Product Scheduler

### <mark style="color:blue;">Installation and User Guide for Magento 2 Product Scheduler Extension</mark>

**Table of Contents**

1. __[_Installation_ ](magento-2-product-scheduler.md#\_bookmark0)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Product Scheduler_ ](magento-2-product-scheduler.md#\_bookmark3)__
   * _General Settings_&#x20;
   * _Timer/Label Settings_&#x20;
   * _Cron Settings_&#x20;
   * _Start and End Date set up with product_&#x20;
3. [_Front-end Site View_ ](magento-2-product-scheduler.md#\_bookmark8)__
   * _"Launching Soon" Text for the New Product on the Category Page_&#x20;
   * _Launching Soon Timer on the Product Page_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

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

### <mark style="color:blue;">Configuration Settings for Product Scheduler</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enable Product Scheduler –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Enable Log –** Yes/No (If set to yes then this create a log file in var/log folder for each day with a time stamp like product\_scheduler 20190125 log. The log file will record all details about products being set to enable/disable along with the dates/store values).

![](../../.gitbook/assets/general\_pscheduler.png)

#### <mark style="color:orange;">Timer / Label Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Show Timer/Label Before Launch Date –** Set yes to enable the module. If set to yes then the product status will be enabled and will show on the front end but there will be no add to basket on category or product page. Instead of Add to basket button it will either show timer on product page and launching soon label on category page.
* **Launching Soon Label Text on Category Page –** This is a text box. This option will only show if **“Show timer/label before launch date”** is set to yes This is a text for adding label text which will appear with product on category page. Default text should be “Launching Soon”.
* **Launching Soon Label Font Size on Category Page –** This is a text box. This option will only show if **“Show/timer before launch date”** is set to yes. The user can enter the font size for the launching soon label text on the category page. Default size should be 12px.
* **Launching soon Label Font Colour on Category Page –** This is a text box. This option will only show if “Show timer/label before launch date” is set to yes. The user can enter the text colour for the launching soon label text on category page. Default colour should be #ffffff.
* **Launching Soon Label Background Colour –** This is a text box. This option will only show if **“Show timer/label before launch date”** is set to yes. The user can enter the background colour for the launching soon label text on category page. Default colour should be #FF0000.
* **Launching soon Label Text on Product Page –** This is a text box. This option will show if **“Show timer/label before launch date”** is set to yes. This is a text for adding label text which will appear with product on product page. Default text should be “Launching soon”.
* **Launching soon Label Font Size on Product Page –** This is a text box. This option will only show if **“Show timer/label before launch date”** is set to yes. The user can enter the font size for the launching soon label text on product page. Default size should be 14px.
* **Launching Soon Label Font Colour on Product Page –** This is a text box. This option will only show if **“Show timer/label before launch date”** is set to yes. The user can enter the text colour for the launching soon label text on product page. Default colour should be #FF0000.
* **Custom CSS –** Enter custom CSS code and easily change the way Product Scheduler looks.

![](../../.gitbook/assets/timtable\_scheduler.png)



#### <mark style="color:orange;">Cron Settings</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* **Cron Schedule –** This will allow you to define cron frequency, how often you want to run product scheduler cron.

![](../../.gitbook/assets/cron\_scheduler.png)

* **Start and End Date Setup at Product Level -** You can schedule product for launching by selecting ''Start Date'' and ''End Date'' from **Catalog > Products > Select Product > Start Date / End Date**.

![](../../.gitbook/assets/startend\_scheduler.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark8" id="_bookmark8"></a>

* <mark style="color:orange;">**"Launching Soon" Text for the New Product on the Product Page –**</mark> You can show "LAUNCHING SOON" on the category page for the new product from **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler > Timer /Label Settings > Show Timer/Label Before Launch Date - "Yes".**

![](../../.gitbook/assets/launchinsoon1.jpg)

* <mark style="color:orange;">**Launching Soon Timer on the Product Page -**</mark>** ** To show launching soon timer on the product page, go to **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler > Timer /Label Settings > Show Timer/Label Before Launch Date -** Select **"Yes".**

![](../../.gitbook/assets/launchingsoon2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-product-scheduler.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
