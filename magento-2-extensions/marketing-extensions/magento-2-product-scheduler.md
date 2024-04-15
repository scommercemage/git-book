# Magento 2 Product Scheduler

### <mark style="color:blue;">Installation and User Guide for Magento 2 Product Scheduler Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-product-scheduler.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Product Scheduler_ ](magento-2-product-scheduler.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Timer/Label Settings_&#x20;
   * _Cron Settings_&#x20;
3. [_Setting UP Product Scheduler_](magento-2-product-scheduler.md#setting-up-product-scheduler)
   * _Start and End Date set up with product_&#x20;
4. [_Front-end Site View_ ](magento-2-product-scheduler.md#\_bookmark8)
   * _"Launching Soon" Text for the New Product on the Category Page_&#x20;
   * _Launching Soon Timer on the Product Page_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Product Scheduler</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enable Product Scheduler –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Enable Log –** Yes/No (If set to yes then this create a log file in var/log folder for each day with a time stamp like product\_scheduler 20190125 log. The log file will record all details about products being set to enable/disable along with the dates/store values).

![](../../.gitbook/assets/general\_pscheduler.png)

#### <mark style="color:orange;">Timer / Label Settings</mark> <a href="#bookmark5" id="bookmark5"></a>

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



#### <mark style="color:orange;">Cron Settings</mark> <a href="#bookmark6" id="bookmark6"></a>

* **Cron Schedule –** This will allow you to define cron frequency, how often you want to run product scheduler cron.

![](../../.gitbook/assets/cron\_scheduler.png)

### <mark style="color:blue;">Setting UP Product Scheduler</mark>

The module enables you to pre-launch products with a custom label text such as “Coming Soon/Launching Soon”. This label appears on various pages of your store such as cross-sell products, up sell products, category pages, etc. The style of the label is completely customizable from the backend. We have provided several individual styling options in the configuration that allows you to style aspects such as font size, font color, label background color, etc.

You can add an start and End date to your products based on which a label or a timer or both can be displayed on products and category pages. The time on the timer or the duration in which the label is displayed is calculated from the start date and end date provided in the product scheduler settings by going into **Admin>catalog>Products.**

The product stays disabled until the start date and once the start date arrives it is enabled automatically but without 'Add to cart' button, instead a label and/or timer is displayed informing users of the pre-launch. This label/timer stays throughout the duration of end date and start date. (this scenrio is not applicable in cases where start date and end date are equal/same. In this case the product simply stays disabled and is enabled on the set date)

Once you have set a start/End date to a product, it automatically adds the lable and/or timer to these products which are displayed on products and category pages. Upon the completion of the end date the product is automatically released on the store i.e can be purchased by customers. The products are enabled, disabled and labels are all added when the scheduled cron job runs.

Let us look at how to set up start and end date for products.&#x20;

* <mark style="color:orange;">**Start and End Date Setup at Product Level -**</mark> You can schedule product for launching by selecting ''Start Date'' and ''End Date'' from **Catalog > Products > Select Product > Start Date / End Date**. Make sure that end date is always greater than or equal to start date because End date minus start date will be duration when the product iwll be in prelaunch phase and upon the end date's completion it will be available for customers.&#x20;

![](../../.gitbook/assets/startend\_scheduler.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#bookmark8" id="bookmark8"></a>

* <mark style="color:orange;">**"Launching Soon" Text for the New Product on the Product Page –**</mark> You can show "LAUNCHING SOON" on the category page for the new product from **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler > Timer /Label Settings > Show Timer/Label Before Launch Date - "Yes".**

![](../../.gitbook/assets/launchinsoon1.jpg)

* <mark style="color:orange;">**Launching Soon Timer on the Product Page -**</mark> To show launching soon timer on the product page, go to **Admin > Stores > Configuration > Scommerce Configuration > Product Scheduler > Timer /Label Settings > Show Timer/Label Before Launch Date -** Select **"Yes".**

![](../../.gitbook/assets/launchingsoon2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-product-scheduler.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
