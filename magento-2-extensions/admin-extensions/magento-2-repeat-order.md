# Magento 2 Repeat Order

<mark style="color:blue;">Installation and User Guide for Magento 2 Repeat Order Subscription Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-repeat-order.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Repeat Order Subscription_ ](magento-2-repeat-order.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Repeat Order Subscription Email_&#x20;
   * _Payment / Order Failed Emailed_&#x20;
   * _Subscription Status Update Notification_&#x20;
3. [_Manage Subscription Grid_ ](magento-2-repeat-order.md#manage-subscription-grid)
   * _Re-start/Pause, Cancel Subscriptions_&#x20;
   * _Subscribed Items and Order History on the Edit Subscription Page_&#x20;
   * _Backend Order Page Link through Subscription Order_&#x20;
4. [_Subscriptions Payment Grid_ ](magento-2-repeat-order.md#subscriptions-payment-grid)
   * _View Subscription Payment Details_&#x20;
5. [_Front-end Site View_ ](magento-2-repeat-order.md#\_bookmark14)
   * _Subscription Options on the Checkout Page_&#x20;
   * _Frequency Selection Drop-down_&#x20;
   * _My Subscription Section on the My Account Page_&#x20;
   * _Subscription Details on the My Subscriptions Page_&#x20;
   * _View / Edit Subscription Information from the Front-end/ My Account_&#x20;
   * _Subscription Confirmation Email_ &#x20;

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

### <mark style="color:blue;">Configuration Settings for Repeat Order Subscription</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Repeat Order Subscription**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Module Enable -** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Subscription Title –** Enter the title of subscription, which will be shown on the front-end.
* **Subscription Frequency Drop down Title –** Enter the title of subscription frequency.
* **Subscription Frequency Drop down Options –** Select the frequency option from the dropdown list.
* **Subscription Discount Percent –** Enter the discount percent, this will be offered on subscription orders. If left blank, then no discount will be offered.
* **Use Tier Prices in Subscription –** Select “Yes” to use tier prices in subscription.

![](../../.gitbook/assets/repeat\_general.jpg)

#### <mark style="color:orange;">Repeat Order Subscription Email</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Email Sender –** Please enter sender/from email address for Repeat Order Confirmation Email.
* **Email Template –** Select order confirmation email template for repeat order. The template will contain Subscription Id, Order Amount, Discount Subscription Frequency, Subscription Start Date, Billing address, Shipping address, Payment Method, Subscribed items.
* **Email CC –** Please add CC email addresses for Repeat Order emails in comma separated format.

![](../../.gitbook/assets/repeat\_confirmationmail.jpg)

#### <mark style="color:orange;">Payment / Order Failed Emailed</mark> <a href="#bookmark6" id="bookmark6"></a>

* **Email Sender –** Please enter sender/from email addresses for Payment order failed email.
* **Email Template –** Select Order/Payment failure email template for repeat order. The template will contain Subscription Id, Due Order Date (for which payment/order failed).
* **Email CC –** Enter CC email address.

![](../../.gitbook/assets/repeat\_paymentfailed.jpg)

#### <mark style="color:orange;">Subscription Status Update Notification</mark> <a href="#bookmark7" id="bookmark7"></a>

* **Email Sender –** Please enter sender/from email addresses for Subscription status update email.
* **Email Template for Subscription Pause/Suspend –** Select notification template for subscription pause.
* **Email Template for Subscription Pause/Suspend for admin –** Notification template for Subscription Pause for Admin.
* **Email Template for Subscription Restart –** Select notification template for subscription Re-start.
* **Email Template for Subscription Restart for Admin –** Notification template for subscription Re-start for Admin.
* **Email Template for Subscription Cancellation –** Select notification template for Subscription Cancellation.
* **Email Template for Subscription Cancellation for Admin –** Notification template for Subscription cancellation for admin.
* **Email CC –** Enter CC from email address.
* **Email Receiver –** Enter receiver email address to receive Card Expiration notification email.
* **Email Template for Card Expiration for Admin –** Email template for Card Expiration for admin.
* **Email Template for Card Expiration –** Select email template for Card Expiration.

![](../../.gitbook/assets/repeat\_substatus.jpg)

### <mark style="color:blue;">**Manage Subscription Grid**</mark>

You can manage subscriptions from, **Admin > Scommerce Mage > Repeat Order > Manage Subscriptions**. This grid will have all the details about the subscriptions like Subscription ID, Frequency, Customer Email, Last Order date, Status, Action (Edit). With the action ‘Edit’ you can easily update subscription details and can also perform Cancel/Pause/Re-start actions.

![](../../.gitbook/assets/repeat\_managesubgrid.jpg)

* <mark style="color:orange;">**Re-start/Pause, Cancel Subscriptions -**</mark> You can re-start, pause and cancel subscriptions from **Admin > Scommerce Mage > Repeat Order > Manage Subscriptions > Select Subscription > Edit.**

![](../../.gitbook/assets/repeat\_restart.jpg)

* <mark style="color:orange;">**Subscribed Items and Order History on the Edit Subscription Page -**</mark>** You** can see the subscribed items and order history from **Admin > Scommerce Mage > Repeat Order > Manage Subscriptions > Select Subscription > Edit.**

![](../../.gitbook/assets/repeat\_subhistory.jpg)

* <mark style="color:orange;">**Backend Order Page Link through Subscription Order –**</mark> When you click on subscription order URL visible under Orders History section at **Admin > Scommerce Mage > Repeat Order > Manage Subscriptions > Select Subscription > Edit,** then it redirects to backend order page.

![](../../.gitbook/assets/repeat\_backendorder.jpg)

**Subscription order link redirected to order view page**

![](../../.gitbook/assets/repeat\_subscriptionorderlink.jpg)

### <mark style="color:blue;">**Subscriptions Payment Grid**</mark>&#x20;

&#x20;To see subscriptions payment details go to **Admin>** **Scommerce Mage > Repeat Order > Subscription Payments**. This grid will provide a view of payment status for the Payment transactions processed for automated subscription order. This will mainly have Subscription Id, First name, Transactions date and time, Transaction error/response.

![](../../.gitbook/assets/repeat\_subpaymentgrid.jpg)

* <mark style="color:orange;">**View Subscription Payment Details -**</mark> You can view payment details from Admin**> Scommerce Mage > Repeat Order > Subscription Payments > Select Subscription > View.**

![](../../.gitbook/assets/repeat\_viewsubpaydetail.jpg)

### Front-end Site View <a href="#bookmark14" id="bookmark14"></a>

* <mark style="color:orange;">**Subscription Options on the Checkout Page -**</mark> When you enable the module then it shows subscription options on the checkout page, by checking "Yes please I would like to receive future discounts" you can subscribed for the repeat order.

![](../../.gitbook/assets/repeat\_front1.jpg)

* <mark style="color:orange;">**Frequency Selection Drop-down -**</mark> On the checkout page when you check the subscription option then it shows frequency drop down, from where you can select the repeat order frequency.

![](../../.gitbook/assets/repeat\_front2.jpg)

* <mark style="color:orange;">**My Subscription Section on the My Account Page -**</mark> On the front-end you can see the subscription details at My Account > My Subscriptions

![](../../.gitbook/assets/repeat\_front3.jpg)

* <mark style="color:orange;">**Subscription Details on the My Subscriptions Page -**</mark> To view subscriptions details go to My Account > My Subscriptions.

![](../../.gitbook/assets/repeat\_front4.jpg)

* <mark style="color:orange;">**View / Edit Subscription Information from the Front-end/ My Account -**</mark> On the front-end you can view and edit the subscriptions from My **Account > My Subscriptions > Select Order > Edit.**

![](../../.gitbook/assets/repeat\_front5.jpg)

* <mark style="color:orange;">**Subscription Confirmation Email –**</mark> When you subscribed for repeat order, it sends subscription confirmation email.

![](../../.gitbook/assets/repeat\_front6.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-repeat-order.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
