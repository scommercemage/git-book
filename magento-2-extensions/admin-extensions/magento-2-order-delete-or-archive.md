# Magento 2 Order Delete or Archive

### <mark style="color:blue;">Installation and user Guide for Magento 2 Order Delete or Archive Extension</mark>

**Table Of Contents**

1. __[_Installation_ ](magento-2-order-delete-or-archive.md#\_bookmark0)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. __[_Configuration Settings for Order Delete or Archive_ ](magento-2-order-delete-or-archive.md#\_bookmark3)__
   * _General Settings_&#x20;
   * _Order Archive Settings_&#x20;
   * _Order Delete Settings_&#x20;
3. __[_Order Grid_ ](magento-2-order-delete-or-archive.md#\_bookmark7)__
   * _Archive or Delete Orders from Order View Page_&#x20;
4. __[_Archive Grid_ ](magento-2-order-delete-or-archive.md#\_bookmark9)__
   * _Restore_&#x20;
   * _Restore Orders From Archived Order View Page_&#x20;
5. __[_Automatically Archive Orders_](magento-2-order-delete-or-archive.md#\_bookmark12) __&#x20;

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

* ### <mark style="color:blue;">Configuration Settings for Order Delete or Archive</mark> <a href="#_bookmark3" id="_bookmark3"></a>
* Go to **Admin > Stores > Configuration > Scommerce Configuration > Archive Orders**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Module Enable -** Select “Yes” or “No” to enable or disable the module.
* **License Key -**. Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)

![](../../.gitbook/assets/order\_general.jpg)

#### <mark style="color:orange;">Order Archive Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled (Yes / No) -** Select "Yes" to archive orders automatically.
* **Retention Period -** Please define retention period. This setting will automatically archive orders older than specified number of days
* **Cron Schedule -** Schedule the cron job to automatically archive the orders (**Default - Midnight**)
* **Send Email (Yes / No) -** Select "Yes" to send email after successfully archival orders.
* **Sender -** Please enter sender/from email address to send an email to administrator after the successful archival of order(s).
* **Email Template -** Please select email template for order archival email.
* **Receiver -** Please add email addresses of administrators who will receive order archival email (comma separated).
* **Order Statuses (Multi-select) -** Please select certain order statuses to be allowed by administrators to be archived.

![](../../.gitbook/assets/order\_archive1.jpg)

![](../../.gitbook/assets/order\_archive3.jpg)

#### <mark style="color:orange;">Order Delete Settings</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* **Enabled (Yes / No) -** Please select "Yes" or "No". If set to "Yes" then it will permanently delete orders.
* **Sender -** Please enter sender/from email address .
* **Email Template -** Please select email template for order deletion email.
* **Receiver -** Please add email addresses of administrator, who will receive order deletion email (comma separated).
* **Order Statuses (Multi-select) -** Please select certain order statuses for order deletion.

![](../../.gitbook/assets/order\_delete.jpg)

### <mark style="color:blue;">Order Grid</mark> <a href="#_bookmark7" id="_bookmark7"></a>

When you enable the "Order Archive" and "Order Delete" settings from **Admin > Stores > Configuration > Scommerce Configuration > Archive Orders > Order Archive / Order Delete Settings > Enabled - "Yes"** , then it adds two additional options "Archive" and "Delete " under the "Actions" drop-down at **Admin > Sales > Order > Actions.**

* <mark style="color:orange;">**Archive -**</mark>** ** It moves/archives order(s) to another storage(archive grid) instead of deleting them. This action can be restored from the archive order view page.
* <mark style="color:orange;">**Delete -**</mark>** ** It deletes order(s) permanently. The "Delete" action cannot be reversed and erases all order(s) and related information.

![](../../.gitbook/assets/order\_grid.png)

* <mark style="color:orange;">**Archive or Delete Orders from Order View Page -**</mark>** ** You can delete and archive order(s) from, **Admin > Sales > Orders > Select Order > View**. The order view page will have two additional options "Delete" and "Archive" and using these two buttons you can perform "Delete" and "Archive" actions. Buttons will only be visible when the module is enabled and the administrator has right role to archive/delete order(s).

![](../../.gitbook/assets/order\_archiveordeleteorders.jpg)

### <mark style="color:blue;">Archive Grid</mark> <a href="#_bookmark9" id="_bookmark9"></a>

To view archived orders, go to **Admin > Sales > Archive Orders**. This grid will have an additional option "Restore "under "Actions" drop-down to restore the archived orders.

* <mark style="color:orange;">**Restore -**</mark>** ** By selecting "**Restore**" from **Admin > Sales > Archive Orders> Actions** drop-down you can easily restore archived order(s).

![ArchiveOrders\_02.png](<../../.gitbook/assets/6 (61)>)

* <mark style="color:orange;">**Restore Orders From Archived Order View Page -**</mark> You can restore archived orders from **Admin > Sales > Archive Orders > Select Order > View >** Click **"Restore".**

**Restore -** It restores archived orders.

![](../../.gitbook/assets/order\_final.jpg)

### <mark style="color:blue;">Automatically Archive Orders</mark> <a href="#_bookmark12" id="_bookmark12"></a>

When you enable the module and define the number of days for "Retention Period" from, **Admin > Stores > Configuration > Scommerce Configuration > Archive Orders > Order Archive Settings,** then it automatically archives order(s) older than defined days. After each successful order archival process, it sends an email to an administrator with details like how many numbers of orders being archived etc..

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-delete-or-archive-order.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
