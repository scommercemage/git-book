# Magento 2 Cash Back Discount

### <mark style="color:blue;">Installation and User Guide for Magento 2 Cash Back Discount Extension</mark>

### Table of Contents

1. [Installation ](magento-2-cash-back-discount.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [Configuration Settings for Cash Back Discount ](magento-2-cash-back-discount.md#configuration-settings-for-cash-back-discount)
   * General Settings&#x20;
   * Cash Back&#x20;
   * Cash Back Reminder&#x20;
   * Create Cart Price Rules for Cashback Discount&#x20;
   * Cashback Transactions&#x20;
3. [Front-end Site View](magento-2-cash-back-discount.md#bookmark9)&#x20;
   * Cashback Qualifying Message on the Checkout Page&#x20;
   * Cashback Discount Option on the Checkout Page&#x20;
   * Applied Cashback Discount on the Checkout Page&#x20;
   * Auto Apply Discount&#x20;
   * Cashback Discount Details on the Front-end - My Account Section&#x20;
   * Cashback Expiry Reminder Email&#x20;
   * Second Cashback Expiry Reminder Email&#x20;
   * Order Confirmation Email&#x20;
   * Invoice Email&#x20;

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

### <mark style="color:blue;">Configuration Settings for Cash Back Discount</mark>&#x20;

Go to **Admin > Stores > Configuration > Scommerce Configuration > Cash Back**

#### <mark style="color:orange;">General Settings</mark>

* **Module Enable -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).

![](<../../.gitbook/assets/1 (55)>)

#### <mark style="color:orange;">Cash Back</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Auto Apply Discount –** Please select “Yes” if you would like to auto apply discount.
* **Select discount in case of multiple cash back rules are applied –** Please choose whether the customer will get minimum discount or maximum discount, in case there are more than one cashback rules are applicable on cart.
* **Include Shipping (Yes/No) –** Please select “Yes” if you would like to include shipping price in Cash Back qualifying amount.
* **Cashback Title Message –** Please add cashback discount title to show on checkout page. This will appear just before cashback discount message.
* **Cashback Qualifying Message –** Please add cashback qualifying message. This will appear on checkout pages when a user will qualify for cashback discount %s and %d is dynamic variable for amount and date.
* **Apply Cashback Checkbox Label –** Please add label for apply discount checkbox on checkout.
* **Cashback Email Message –** Please add cashback qualifying message. This will appear on order confirmation %s and %d is dynamic variable for amount and date,
* **Transactions Update Schedule –** This setting will be used to allow you to define schedule how often you want to update transactions.
* **Summary Update Schedule –** This setting will be used to allow you to define schedule how often you want to update summary.

![](../../.gitbook/assets/cashback\_settings.png)

#### <mark style="color:orange;">Cash Back Reminder</mark> <a href="#bookmark6" id="bookmark6"></a>

* **Enable (Yes/No) –** This setting will enable or disable module.
* **Email Sender –** Please select sender/from email address for Cash Back reminder email.
* **Email Template –** Please select email template for Cash Back reminder email.
* **Second Email Template –** Please select email template for second Cash Back reminder email.
* **Cashback Reminder Message –** Please add a custom message for Cash back expiry reminder %1 and %2 is dynamic variable for amount and date.
* **Cashback Second Reminder Message –** Please add a custom Message for Cas back expiry second reminder %1 and %2 is dynamic variable for amount and date.
* **Cashback Expiry Reminder Schedule –** Please define how often you want to run cron for the cash back reminder email.
* **Send reminder (days) –** Please add number of days for reminder email to be sent to the user before the Cash back Discount expires. For e.g. If set to “1” day, then an email will be sent 1 day before the Cash Back Discount expiry date.
* **Send second reminder (days) -** Please add number of days for second reminder email to be sent to the user before the Cash back Discount expires. For e.g. If set to “1” day, then an email will be sent 1 day before the Cash Back Discount expiry date.

![](../../.gitbook/assets/cashbackreminder\_settings.png)

* <mark style="color:orange;">**Create Cart Price Rules for Cashback Discount -**</mark> You can create cart price rules from **Admin > Marketing > Promotions > Cart Price Rules >** Click on "**Add New Rule"**, it redirects on new cart price rule and by filling all the required details you can create the new cart price rule.

![](../../.gitbook/assets/cashback\_createcart.png)

* <mark style="color:orange;">**Cashback Transactions -**</mark> To view cash back transaction go to **Admin > Sales > Scommerce Cash Back > Cash Back > Cashback Transactions.**

The grid will have following columns/information:-

* **Customer Email –** Customer email Id
* **Cashback Amount –** Cashback amount
* **Cashback Expiry –** Cashback discount expiry date
* **Transaction Date –** Date of added or deducted cash back discount
* **Status –** Cash Back discount status (Applied/Processing/Used)
* **Updated\_at –** Updated date

![](../../.gitbook/assets/cashback\_transactions.jpg)

* <mark style="color:orange;">**Applied Cashback Details on the Order View Page -**</mark> You can view the applied cashback discount at **Admin > Sales > Orders > select Order > View.**

![](../../.gitbook/assets/cashback\_applied.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#bookmark9" id="bookmark9"></a>

* <mark style="color:orange;">**Cashback Qualifying Message on the Checkout Page -**</mark> You can define qualifying message from **Admin > Stores > Configuration > Scommerce Configuration > Cashback Qualifying Message - " "**, the message will be shown on the checkout page.
* <mark style="color:orange;">**Cashback Discount Option on the Checkout Page -**</mark> When you enable the module and if there is any cash back discount available then it shows "Apply cash back discount" option on the checkout page and by checking this option you can apply for cash back discount.

![CashbackDiscountCheckBoxOnTheCheckoutPage\_006.png](<../../.gitbook/assets/8 (18)>)

* <mark style="color:orange;">**Applied Cashback Discount on the Checkout Page -**</mark> You can see the applied cash back discount on the checkout page under "Order Summary" section.

![](../../.gitbook/assets/cashback\_summary.jpg)



* <mark style="color:orange;">**Auto Apply Discount -**</mark> To apply discount automatically and hide checkbox on checkout, set ‘Auto apply discount’ to ‘Yes’ from **Admin > Stores > Configuration > Scommerce Configuration > Cash Back > Auto apply discount – “Yes/No”.**

![](../../.gitbook/assets/cashback\_auto.jpg)

* <mark style="color:orange;">**Cashback Discount Details on the Front-end - My Account Section -**</mark> You can view cash back details on the front-end from **My Account > My Cashback History.**

![](../../.gitbook/assets/cashback\_history.jpg)

* <mark style="color:orange;">**Cashback Expiry Reminder Email -**</mark> When you enable the "Cash Back Reminder" from Admin > Stores > Configuration > Scommerce Configuration > Cash Back **> Cash Back Reminder > Enable - "Yes",** it sends an expiry reminder email to customers before the period of the discount expired.

![](../../.gitbook/assets/cashback\_expiry1.jpg)

* <mark style="color:orange;">**Second Cashback Expiry Reminder Email –**</mark> You can set the email templates and reminder days for second email from **Admin > Store > Configuration > Scommerce Configurations > Cash Back Reminder- Second Email Template and Send second reminder (days).**

![](../../.gitbook/assets/cashback\_expiry2.jpg)

* <mark style="color:orange;">**Order Confirmation Email –**</mark> You can see the applied cashback discount on the order confirmation and invoice emails.

![](../../.gitbook/assets/cashback\_orderconfirm.jpg)

* <mark style="color:orange;">**Invoice Email –**</mark> Below is the image where you can see applied cashback discount.

![](../../.gitbook/assets/cashback\_invoice.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-next-order-discount.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
