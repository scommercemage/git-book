# Cash Back Discount

### <mark style="color:blue;">Installation and User Guide for Magento 1 Cash Back Discount</mark>

**Table of Contents**

1. [Installation ](cash-back-discount.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Cashback Discount ](cash-back-discount.md#\_bookmark4)
   * General Settings&#x20;
   * Reminder&#x20;
   * Shopping Cart Price Rules Setup&#x20;
   * Conditions&#x20;
   * Actions&#x20;
   * Labels&#x20;
   * Manage Coupon Codes&#x20;
   * Applied Cashback Details on the order view page&#x20;
   * Theme Changes&#x20;
3. [Front-end site view ](cash-back-discount.md#\_bookmark14)
   * Cashback Discount Option on the Checkout Page&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Cashback Discount</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Cashback**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Cashback Expiry Date (YYYY-MM-DD HH:MM:SS) –** Expiry date and time for Cash back offer. Orders placed before this date and time will get cash back offer for their next order. It should be in (YYYY-MM-DD HH:MM:SS**)** format.
* **Cashback Validity Months -** Cash back discount validity period. It defines the period for the validity of cash back discount for next order.
* **Cashback Minimum Order Value –** The discount will only apply when the basket value exceeds the minimum order value.
* **Exclude Order Statuses –** Order status excluded from cash back offer.
* **Cashback Discount Including Shopping –** Include shipping in discount or not.
* **Cashback Title Message –** Cashback title appears to appear on basket, order review and order confirmation email.
* **Cashback Qualifying Message –** Message to appear on basket and review order page to show that they qualified for cash back offer for their next purchase.
* **Cashback Email Message –** Message will appear on the order confirmation email. Default message, “%s” will be replaced with validity period.

![](../../.gitbook/assets/m1cashback\_general.jpg)

#### <mark style="color:orange;">Reminder</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* **Enable –** Select “Yes” to enable the Reminder.
* **Email Sender –** Email address to appear as sender.
* **Email Template –** Email Template Default is Cashback Reminder.
* **Send reminder (days) –** Number days defined for reminder email before cash back validity expires.
* **Log Process –** If set to yes, logs the reminder email logs in var/log folder.

![](../../.gitbook/assets/m1cashback\_reminder.jpg)

*   <mark style="color:orange;">**Shopping Cart Price Rules Setup –**</mark>** ** Steps to set up discount offer:

    1. Go to Promotions > Shopping Cart Price Rules > Add new rule
    2. Set up discount details as required.
    3. Make sure discount From and To date matches to the discount validity. From Date Start Date for cash back discount.

    To Date should be the Expiry date of Cash Back + Validity Months

    1. Select “Cash Back Percentage” in Action > Apply
    2. Save Rule.

<mark style="color:red;">**Please refer to the below screen grabs for setting up cash back discount rule:**</mark>

**From Date –** This should be start date of the cash back promotion

**To Date –** This should be expiry date of the cash back promotion specified in system <mark style="color:orange;">****</mark> configuration plus validity month specified in system configuration.

**For example ,** in system configuration of cash back, if you have specified expiry date is on **30/05/2020** and validity month is 1 month then To Date should be **30/06/2020**, this will allow customers to redeem their offer in next 30 days especially those who have placed their first order on **30/05/2020**

![](<../../.gitbook/assets/3 (78)>)

#### <mark style="color:orange;">Conditions</mark> <a href="#_bookmark8" id="_bookmark8"></a>

![](<../../.gitbook/assets/4 (66)>)

#### <mark style="color:orange;">Actions</mark> <a href="#_bookmark9" id="_bookmark9"></a>

![](<../../.gitbook/assets/5 (9)>)

#### <mark style="color:orange;">Labels</mark> <a href="#_bookmark10" id="_bookmark10"></a>

![](<../../.gitbook/assets/6 (54)>)

#### <mark style="color:orange;">Manage Coupon Codes</mark> <a href="#_bookmark11" id="_bookmark11"></a>

![](<../../.gitbook/assets/7 (30)>)

#### <mark style="color:orange;">Applied Cashback Details on the order view page</mark> <a href="#_bookmark12" id="_bookmark12"></a>

![](<../../.gitbook/assets/8 (50)>)

#### <mark style="color:orange;">**Theme Changes**</mark>&#x20;

If you are not using your custom theme then this module should work out of the box. But if you are using custom theme then follow the following steps: -

* **Check if you have the following files in your custom theme folder**

```
/app/design/frontend/default/<<custom>>/template/checkout/cart.phtml
/app/design/frontend/default/<<custom>>/template/checkout/onepage/r eview/info.pthml
/app/design/frontend/default/<<custom>>/template/email/order/items.p html
```

* **If these files don’t exist in your custom theme then copy them form the following paths into your custom theme with folders:-**

```
app/design/frontend/default/default/template/checkout/cart.phtml
app/design/frontend/default/default/template/checkout/onepage/review/ info.phtml
app/design/frontend/default/default/template/email/order/items.phtml
```

* **If these files do exist in your custom theme then copy the differences in your version of files**
* <mark style="color:orange;">**Clear Caches –**</mark>** ** Once you are done with everything above, clear the cache to get the changes reflect on your website

### <mark style="color:blue;">Front-end site view</mark> <a href="#_bookmark14" id="_bookmark14"></a>

#### <mark style="color:orange;">Cashback Discount Option on the Checkout Page</mark> <a href="#_bookmark15" id="_bookmark15"></a>

![](<../../.gitbook/assets/9 (39)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-next-order-discount.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
