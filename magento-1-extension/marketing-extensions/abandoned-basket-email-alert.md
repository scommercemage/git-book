# Abandoned Basket Email Alert

### <mark style="color:blue;">Installation and User Guide for Magento 1 Abandoned Basket Email Alert Extension</mark>

**Table of Contents**

1. [Installation ](abandoned-basket-email-alert.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Abandoned cart ](abandoned-basket-email-alert.md#\_bookmark4)
   * General Settings&#x20;
   * Abandoned Cart Email Template&#x20;
   * Abandoned Basket Email Alert&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark> To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Abandoned cart</mark> <a href="#bookmark4" id="bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Abandoned Cart**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Email Sender –** Select sender email address.
* **Email Template –** Select email template from drop-down if you have created your own version of Abandoned cart email template using system > transaction email section of admin. If not selected it will use default email template provided as part of the module.
* **Send Alerts (hours) –** Enter the number of hours you want delay before sending abandoned cart email alerts to customers.
* **Log Process –** Set it to yes, if you want to see if the abandoned cart emails are going to customers or not. Logs can be downloaded from var/log/abandoned\_cart\_email\[YYYYMMDD\_HHMM].log

![](../../.gitbook/assets/m1abandon\_general.jpg)

#### <mark style="color:orange;">Abandoned Cart Email Template</mark> <a href="#bookmark6" id="bookmark6"></a>

![](<../../.gitbook/assets/2 (83)>)

#### <mark style="color:orange;">Abandoned Basket Email Alert</mark> <a href="#bookmark7" id="bookmark7"></a>

![](<../../.gitbook/assets/3 (24)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://scommerce-mage.com/magento-abandoned-cart-or-basket-alert.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
