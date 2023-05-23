# Magento 2 Delivery Instructions and Delivery Date

### <mark style="color:blue;">Installation and User Guide for Magento 2 Delivery Instructions and Delivery Date Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-delivery-instructions-and-delivery-date.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Delivery Instruction_ ](magento-2-delivery-instructions-and-delivery-date.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Configuration Settings_&#x20;
   * _Back-end - Delivery Instruction Details_&#x20;
3. [_Front-end Site View_ ](magento-2-delivery-instructions-and-delivery-date.md#\_bookmark7)
   * _Delivery Instruction Section on the Checkout page_&#x20;
   * _Delivery Time Selection_&#x20;
   * _Delivery Date Selection_&#x20;
   * _Delivery Instructions Details in Order Confirmation Emails_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Delivery Instruction</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce  > Diamond Search**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Module Enable -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com.](mailto:core@scommerce-mage.com)

![](../../.gitbook/assets/delivery\_general.jpg)

### Configuration Settings <a href="#_bookmark5" id="_bookmark5"></a>

* **Delivery Instruction Label –** Enter delivery instruction label, this label will be shown on the frontend checkout page under delivery instruction section.
* **Delivery Date Label –** Enter delivery date label, this label will be shown on the frontend checkout page.
* **Delivery Time Label –** Enter delivery time label, this label will be shown on the frontend checkout page under delivery instruction.
* **Choose Time Label –** Enter time label, this label will be shown on the frontend checkout page under delivery instruction.
* **Max Length -** Enter max length of delivery instruction.
* **Enable Delivery Date –** Select “Yes” to enable the delivery date on checkout.
* **Delivery Date cut off time –** Select delivery date cut off time, after this time the order will be treated for next day.
* **Order Processing time –** Number of days which is required for order processing. If this is set to 2 then the date calendar on checkout will show delivery dates of 2 days from order placement.
* **Exclude Dates –** Dates which will be disabled on the date grid on checkout.
* **Timeslots –** Times will be available in date calendar on checkout.
* **Disable days –** Select weekdays which will be disabled on the checkout calendar.

![](../../.gitbook/assets/deliver\_config1.jpg)

![](../../.gitbook/assets/deliver\_config2.jpg)

* <mark style="color:orange;">**Back-end - Delivery Instruction Details -**</mark> To view the delivery instructions details, go to **Admin > Sales > Order > Select Order > View**.

![](../../.gitbook/assets/delivery\_payment.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark7" id="_bookmark7"></a>

* <mark style="color:orange;">**Delivery Instruction Section on the Checkout page -**</mark> When you enable the module and select the "Enable Delivery Date" to "Yes" from **Admin > Stores > Configuration > Scommerce Configuration > Delivery Instruction > Configuration Settings**, then it shows Delivery Date, Delivery Time under Delivery Instruction section on the checkout page.

![Untitled (2)](<../../.gitbook/assets/4 (73)>)

* <mark style="color:orange;">**Delivery Time Selection -**</mark> You can add time slots from, **Admin > Stores > Configuration > Scommerce Configuration > Delivery Instruction > Configuration Settings > Timeslots**, and added time slots will be shown on the checkout page from where you can choose the convenient time slot for delivery.

![](<../../.gitbook/assets/5 (38)>)

* <mark style="color:orange;">**Delivery Date Selection -**</mark> To show delivery date on the checkout page, select "Enable Delivery Date" to "Yes" from **Admin > Stores > Configuration > Scommerce Configuration > Delivery Instruction > Configuration Settings**.

![](<../../.gitbook/assets/6 (16)>)

* <mark style="color:orange;">**Delivery Instructions Details in Order Confirmation Emails -**</mark> It sends delivery instructions details in order confirmation emails, which you can see in the below screengrab.

![](<../../.gitbook/assets/7 (40)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-delivery-date-and-instructions.html#faq') first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
