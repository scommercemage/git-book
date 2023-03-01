# Magento 2 Not On The High Street Integration

### <mark style="color:blue;">Installation and User Guide for Magento 2 Noths Integration Extension</mark>

**Table of Contents**

1. __[_Installation_ ](magento-2-not-on-the-high-street-integration.md#\_bookmark0)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. __[_Configuration Settings for Noths Integration_ ](magento-2-not-on-the-high-street-integration.md#\_bookmark3)__
   * _General Settings_&#x20;
   * _Integration Settings_&#x20;
3. __[_Noths Order(s) View from Back-end_ ](magento-2-not-on-the-high-street-integration.md#\_bookmark6)__
   * _Noths Order Import_&#x20;
   * _Noths Order Details on Order View Page_&#x20;
   * _Noths Order Logs_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Noths Integration</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Noths**

#### <mark style="color:orange;">General Settings</mark>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com.](file:///C:/Users/jatin/OneDrive/Documents/core%40scommerce-mage.com)

![](../../.gitbook/assets/noths\_general.jpg)

#### <mark style="color:orange;">Integration Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Cron for Order import –** Please allow to set cron frequency for order import from Noths.
* **API Url –** Please enter API Url.
* **API Log –** Select “Yes” to enable the API Log. If set to “Yes” then it will log communication with Noths API.
* **Create Files for Log –** Select “Yes” to enable the create files for log. If set to “Yes” then it will log communication with Noths API.
* **API Key –** Please enter API Key.
* **Select the allowed order statuses –** Please select order status which will be imported from Noths
* **Select the store for NOTHS Orders –** Please select the store for Noths orders.
* **Noths Order Payment Method –** Please add the payment method which will be used to import orders from Noths.
* **Noths Order Shipping Method –** Please add the shipping method which will be used to import orders from Noths.
* **Dispatch Notes Path –** Please add the dispatch notes path in media/noths/dispatchnote/\[order number].pdf
* **Estimated Days to ship –** Please add the days for estimated days to ship.
* **Attributes Mapping –** Please add the mapping of Magento attribute with options in Noths.

![](../../.gitbook/assets/noths\_integ1.jpg)

![](../../.gitbook/assets/noths\_integ2.jpg)

### <mark style="color:blue;">Noths Order(s) View from Back-end</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* <mark style="color:orange;">**Noths Order Import -**</mark> You can view imported Noths order(s) from **Admin > Sales> Orders.** This grid will have "Dispatch Note " and "Noths Id".

![A screenshot of a computer screen  Description automatically generated](<../../.gitbook/assets/3 (48)>)

* <mark style="color:orange;">**Noths Order Details on Order View Page -**</mark>** ** You can view Noths order details at **Admin > Sales > Select Order > View.**

![](../../.gitbook/assets/noths\_front1.jpg)

* <mark style="color:orange;">**Noths Order Logs -**</mark>** ** To view Noths Logs go to **Admin > Scommerce Noths > Order Logs.** This log will have Entity Id, Request, Status, Type, Created At, and Response.

![](../../.gitbook/assets/noths\_front2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](magento-2-not-on-the-high-street-integration.md#installation-and-user-guide-for-magento-2-noths-integration-extension) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
