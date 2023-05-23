# Surcharge or Additional Fee

### <mark style="color:blue;">Magento Surcharge or Additional Fee Module Extension - Installation/Set-up Guide</mark>

1. <mark style="color:orange;">**Disable Compilation Mode**</mark><mark style="color:orange;">:</mark> To check that this is disabled, go to System>Tools->Compilation. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
2. <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
3. <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (System->Cache Management), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Changes</mark>

<mark style="color:red;">**Admin -> Scommerce Configuration -> Surcharge**</mark>

* **Enabled**: Enable /Disable Module
* **License Key**: Valid key provided by Scommerce Mage
* **Label**: This label text gets used in the frontend of the website which will be shown on basket, review, invoice, order, shipment, email confirmation and refund
* **Surcharge Amount Type**: This option allows you to choose fixed amount or percentage value. Percentage value gets calculated based on the grand total or subtotal attribute been selected
* **Surcharge Percentage or Fixed Amount**: This is the surcharge or additional fee which will be shown to the customer based on surcharge amount type (fixed or percentage)
* **Grand or SubTotal Attribute**: This option allows you to choose whether you want to apply percentage additional fee on grand or subtotal. This will also apply on **Minimum Order Total**.
* **Minimum Order Total**: This value will be checked / validated
* **Grand or SubTotal Attribute** value been selected based on the
* **Skip with Free Shipping? –** This option can be used if you don’t want to charge additional fee when the shipping price is zero. This is useful when you are charging additional fee based on the shipping country but when the shipping is free then you might not want to charge additional fee.
* **Shipping Countries**: The additional fee will be applied only to the specific shipping country(s). Please select all if you want to charge additional fee for all shipping countries.
* **Payment Method –** The additional fee will be applied only to the specific payment method (s). Please select all if you want to charge additional fee for all payment methods.

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-surcharge-or-additional-fee.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**

<mark style="color:red;">**Please Note: It is advised to back up your live site before installation.**</mark>
