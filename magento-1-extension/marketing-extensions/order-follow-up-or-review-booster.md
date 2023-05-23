# Order Follow Up or Review Booster

### <mark style="color:blue;">Installation and User Guide for Magento 1 Order Follow up or Review Booster</mark>

**Table of Contents**

1. [Installation ](order-follow-up-or-review-booster.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Follow up ](order-follow-up-or-review-booster.md#\_bookmark4)
   * General Settings&#x20;
   * Follow up Email Template&#x20;
   * Product Review&#x20;
   * Rollback Plan&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark> To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Follow up</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Follow up**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Email Sender –** Select sender email address.
* **Email Template –** Select email template from drop-down if you have created your own version of Follow up email template using system > transaction email section of admin. If not selected it will use default email template provided as part of the module.
* **Send Alerts (days) –** Enter the number of days you want delay before sending order follow up email alert to customers after shipment.
* **Admin Email Address (Bcc) –** Please add email address to send Bcc email to administrator.
* **Log Process –** Set it to yes, if you want to see if the follow up emails are going to customers or not. Logs can be downloaded from /var/log/follow\_up\_email\[YYYYMMDD\_HHMM].log

![](../../.gitbook/assets/m1orderfollow\_general.jpg)

* <mark style="color:orange;">**Follow up Email Template -**</mark> Below is the template for the follow up email.

![](../../.gitbook/assets/m1orderfollow\_template.jpg)

#### <mark style="color:orange;">Product Review</mark> <a href="#_bookmark7" id="_bookmark7"></a>

![](<../../.gitbook/assets/3 (83)>)

#### <mark style="color:orange;">Rollback Plan:</mark> <a href="#_bookmark8" id="_bookmark8"></a>

* **Delete the following folders from FTP**
  * **app/code/community/Scommerce/Followup**
  * **app/etc/modules/Scommerce\_Followup.xml**
* **Run the following sql commands: -**

```
DELETE FROM core_resource WHERE CODE=’scommerce_followup_setup’;
ALTER TABLE sales_flat_order DROP COLUMN followup_alert
```

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-order-follow-up-or-review-booster.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
