# Magento 2 Google Enhanced Ecommerce Tracking

### <mark style="color:blue;">Installation and User Guide for Magento 2 Google Universal Analytics Enhanced Ecommerce Tracking Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-google-enhanced-ecommerce-tracking.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Google Universal Tracking_ ](magento-2-google-enhanced-ecommerce-tracking.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Enhanced Ecommerce_&#x20;
3. [_To Turn on Enhanced E-commerce for a view, and label your checkout steps:_ ](magento-2-google-enhanced-ecommerce-tracking.md#\_bookmark6)
   * _Real Time Event_&#x20;
   * _Backend Order Tracking in Google Analytics_&#x20;
   * _Shopping Behaviour_&#x20;
   * _Checkout Behaviour_&#x20;
   * _Product Performance_&#x20;
   * _Sales Performance_&#x20;
   * _Product List Performance by Category._&#x20;
4. [_Front-end Site View_ ](magento-2-google-enhanced-ecommerce-tracking.md#\_bookmark14)
   * _Home Page with Tags_&#x20;
   * _GA - UA Tracking Code_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Google Universal Tracking</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Universal Analytics**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Account Id –** Enter your Google Account Id.
* **Anonymize Ip –** Sets the parameter anonymize in tracking. If set to yes, tells Google Analytics to anonymize the information sent by the tracker objects by removing the last octlet of the IP address prior to its storage.
* **Display Feature –** Enable/Disable the display feature plugin. For more information [click here](https://developers.google.com/analytics/devguides/collection/analyticsjs/display-features)
* **Enable User Id –** Enable/Disable User Id feature. Make sure this feature is enabled in Google Analytics first before enabling in Magento. For more information [click here](https://developers.google.com/analytics/devguides/collection/analyticsjs/cookies-user-id)
* **Ecommerce Enabled –** Enable/Disable the ecommerce plugin. For more information [click here](https://developers.google.com/analytics/devguides/collection/analyticsjs/ecommerce).
* **Domain Auto –** Enable/Disable to show ‘auto’ as domain name, when turned off, it shows the domain name itself.
* **Linker Enabled –** Enable/Disable the linker plugin to link cross domains. For more information [click here](https://developers.google.com/analytics/devguides/collection/analyticsjs/cross-domain#autolink).
* **Domains to Link –** Add domain names or regular express for example ‘destination.com’, ‘dest3.com’ or /^example\\.(com]|de|nl)$/ For more information [click here](https://developers.google.com/analytics/devguides/collection/analyticsjs/cross-domain#autolink).
* **Linker Accounts Enabled –** Enable/Disable the linker accounts.
* **Base –** Set “Yes” if you send base order data.
* **Ajax Add to Basket Enabled –** Set “Yes” if you have AJAX add to basket enabled on your website.

![](../../.gitbook/assets/enhanced\_general.png)

#### <mark style="color:orange;">Enhanced Ecommerce</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enable Enhanced Ecommerce –** Select “Yes” to enable the enhanced ecommerce tracking.
* **Steps –** You can select multiple steps here, these steps correspond to Magento onepage standard checkout steps. Also make sure you add these same steps in Google Analytics under Ecommerce settings by turning Enhanced E-commerce on.
* **Brand Attribute –** You can select product attribute which you can use to set your brand names. This will be passed to Google for further reporting.
* **Brand Name –** You can also pass hard coded brand name using this configuration settings.
* **Send Transactional Data Offline –** Set “Yes” to send data on order creation only. This feature could be useful if your payment gateway show their own success instead of Magento order confirmation page.
* **Send Transactional Data Only on Invoice Creation –** Set “Yes” to send data on invoice creation only. This feature could be useful if you take either payment on dispatch or your payment gateway show their own success page instead of Magento order confirmation page.
* **Send Phone or Admin Orders –** Enable this feature only if you want to send admin or phone orders on order creation.
* **Source –** You can add your source here to pass this to Google for admin orders.
* **Medium –** You can add your source here to pass this to Google for admin orders.
* **Send Product Impression on Scroll –** Enable this feature when you have loads of products on product listing / category page.
* **Product item class on category / product listing page –** Make sure this product class item heirarchy is as unique as possible for example for luma theme you can use div.products ol.product-items li.product-item
* **Debugging –** Set “Yes” to generate **GA.log** in var/log directory to log all transactional data which we send to Google using measurement protocol.

![](../../.gitbook/assets/enhanced\_commerce.png)

### <mark style="color:blue;">To Turn on Enhanced E-commerce for a view, and label your checkout steps:</mark> <a href="#_bookmark6" id="_bookmark6"></a>

1. Click Admin at the top of any Analytics page.
2. Select the view for which you want to enable Enhanced E-commerce reporting.
3. In the view column, click **E-commerce Settings**.
4. Under Step 1, Enable E-commerce, set the status to **ON**.
5. Click **Next Step**.
6. Under Step 2, Enhanced E-commerce Settings, set the status to ON. When you turn this option on:
   * You can see the Enhanced E-commerce reports in the conversions section.
   * The older, older category of E-commerce reports is no longer available.

You can turn this option off to restore the older category of E-commerce reports.

* Optionally, enter labels for the checkout steps that you have defined in your Magento steps configuration. Please see screenshot below for reference

![](<../../.gitbook/assets/15 (11)>)

* Click Submit.



* <mark style="color:orange;">**Real Time Event -**</mark> You can view the tracked events from **GA > Realtime > Events.**

![](<../../.gitbook/assets/16 (12)>)

* <mark style="color:orange;">**Backend Order Tracking in Google Analytics -**</mark> You can track admin orders by selecting "Yes" for **"Send Phone or Admin Orders"** from **Admin > Stores > Configuration > Scommerce Configuration > Google Universal Analytics > Enabled Enhanced Ecommerce - "Yes".**

![](<../../.gitbook/assets/17 (19)>)

* <mark style="color:orange;">**Shopping Behaviour**</mark> <mark style="color:orange;"></mark><mark style="color:orange;">-</mark> You can see the shopping behaviour from **GA > Conversion >Ecommerce >Shopping Behaviour.**

![](<../../.gitbook/assets/18 (9)>)

* <mark style="color:orange;">**Checkout Behaviour -**</mark> You can see the checkout behaviour in GA with billing & shipping method, payment method and transactions details from **GA > Conversion**

**> Ecommerce > Checkout Behaviour.**

![](<../../.gitbook/assets/19 (6)>)

* <mark style="color:orange;">**Product Performance -**</mark> To view the product performance go to **GA > Conversion > Ecommerce > Product Performance.**

![](<../../.gitbook/assets/20 (12)>)

* <mark style="color:orange;">**Sales Performance -**</mark> To view tracked sales performance go to **GA > Conversion > Ecommerce > Sales Performance.**
* <mark style="color:orange;">**Product List Performance by Category -**</mark> You can view the product list performance from **GA > Conversion >Ecommerce >Product List Performance.**

### <mark style="color:blue;">Front-end Site view</mark> <a href="#_bookmark14" id="_bookmark14"></a>

* <mark style="color:orange;">**Home Page with Tags -**</mark> In Tag Assistant tool you can see the fired tags.

![](../../.gitbook/assets/enhanced\_front1.jpg)

* <mark style="color:orange;">**GA - UA Tracking Code -**</mark> In the below image you can see the **UA** tracking id's added from **Admin > Stores > Configuration > Scommerce Configuration > Google Universal Analytics > Account Id -** UA -33387561-9.

![](../../.gitbook/assets/enhanced\_front2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](magento-2-google-enhanced-ecommerce-tracking.md#installation-and-user-guide-for-magento-2-how-did-you-hear-about-us-extension) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
