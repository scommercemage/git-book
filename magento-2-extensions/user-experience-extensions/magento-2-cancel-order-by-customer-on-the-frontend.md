# Magento 2 Cancel Order by Customer on the Frontend

### <mark style="color:blue;">Installation and User guide for Magento 2 Cancel Order by Customer on the Frontend Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-cancel-order-by-customer-on-the-frontend.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Cancel Order_ ](magento-2-cancel-order-by-customer-on-the-frontend.md#\_bookmark3)
   * _General Settings_&#x20;
3. [_Front-end Site View for Order Cancellation from My Account Section_ ](magento-2-cancel-order-by-customer-on-the-frontend.md#\_bookmark5)
   * _Cancel Order from My Account Section_&#x20;
   * _Cancel Order Popup_&#x20;
   * _Notification Message for Cancel Order_&#x20;
   * _Cancel Order status (Cancelled)_&#x20;
   * _Order Cancellation Email_&#x20;
   * _Guest Form_&#x20;
   * _Order ID_&#x20;
   * _Billing Last Name_&#x20;
   * _Find Order By_&#x20;
   * _Order Information Page_&#x20;
   * _Cancel Order Successfully_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Cancel Order</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Cancel Order**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Label –** Please provide label text for cancel order link which will be shown on the frontend.
* **Email Sender –** Please enter/sender from email address for Order Cancellation email.
* **Email Template for Guest –** Please select email template for sending cancellation email to guest customer.
* **Email Template for Registered Customer –** Please select email template for sending cancellation email to registered customer.
* **Email BCC –** Please add CC email addresses for Order Cancellation emails in comma separated format.

![](../../.gitbook/assets/cancel\_general.jpg)

* **Reasons –** Select order cancellation reason from the dropdown or select other to define your own reasons. Option “Other” will display a text box on front end, where you can add reason of cancellation**.**
* **Notification Message –** Enter notification message you want to show on frontend for order cancellation.
* **Number of hours to cancel –** Please add number of hours valid for order cancellation.

![](../../.gitbook/assets/cancel\_general2.jpg)

### <mark style="color:blue;">Front-end Site View for Order Cancellation from My Account Section</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* <mark style="color:orange;">**Cancel Order from My Account Section -**</mark> When you enable the module then it shows "Cancel Order" link on the front-end **My Account > My Orders section.**

![](<../../.gitbook/assets/3 (77)>)

* <mark style="color:orange;">**Cancel Order Popup -**</mark> When you click "Cancel Order" button from **My Account > My Orders** section, it displays a pop up, from where you can add/select your own reasons of order cancellation and by clicking "Cancel Order" button you can cancel order.

![](<../../.gitbook/assets/4 (24)>)

* <mark style="color:orange;">**Notification Message for Cancel Order -**</mark> After the order cancellation it shows notification message on the front-end.

![](<../../.gitbook/assets/5 (16)>)

* <mark style="color:orange;">**Cancel Order status (Cancelled) -**</mark> When you cancel the order then it automatically updates the order status from Pending to Cancelled.

![](<../../.gitbook/assets/6 (20)>)

* <mark style="color:orange;">**Order Cancellation Email -**</mark> After the successful order cancellation, it sends an email notification to the administrator and the customer, below is the sample email for the same.

![Confirmation for your order cancellation - jatinnayyar1999 gmail com - Gmail (2)](<../../.gitbook/assets/7 (54)>)

* **Guest Form -** The guest user can cancel order by submitting the Orders and Returns form. Here is the link to access the form [Orders and Returns](http://demo2.scommerce-mage.co.uk/sales/guest/form/). The form will have the following fields: -
* **Order ID -** enter the order Id, you want to cancel.
* **Billing Last Name -** enter the last name.
* **Find Order By -** select the Email / ZIP code.
* **Email -** enter the email address.

![](<../../.gitbook/assets/8 (38)>)

* <mark style="color:orange;">**Order Information Page -**</mark> After filling the Orders and Returns form when you click “Continue” button, it redirects on order information page, from where you can cancel the order by clicking “Cancel Order” button.

![](<../../.gitbook/assets/9 (25)>)

* <mark style="color:orange;">**Cancel Order Successfully -**</mark> Once the order is cancelled, it displays the successful cancellation message.

![](<../../.gitbook/assets/10 (31)>)

If you have a question related to this extension please check out our [**FAQ section**](https://www.scommerce-mage.com/magento-2-cancel-order.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
