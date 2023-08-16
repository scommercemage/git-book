# Magento 2 Ajax Login and Add to Wishlist

### <mark style="color:blue;">Installation and User Guide for Magento 2 AJAX Login and Add to Wishlist</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-ajax-login-and-add-to-wishlist.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Ajax Login & Wishlist_ ](magento-2-ajax-login-and-add-to-wishlist.md#\_bookmark3)
   * _General Settings_&#x20;
3. [_Front-end site view_ ](magento-2-ajax-login-and-add-to-wishlist.md#\_bookmark5)
   * _Ajax Add to Wishlist - Ajax SignIn Popup_&#x20;
   * _Ajax Add to Wishlist – Ajax Create an Account Popup_&#x20;
   * _Ajax Add to Wishlist – Mini Cart Drop-Down Slider_&#x20;
   * _Limit The Quantity of Products to Show In The Cart Slider_&#x20;
   * _Ajax Add to Wishlist – Ajax Add to Wishlist Popup_&#x20;
   * _Ajax Add to Wishlist – Ajax Add to Wishlist Confirmation Message_&#x20;
   * _Ajax Add to Wishlist – Wishlist Products Under my Account – My Wishlist Section_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Ajax Login & Wishlist</mark> <a href="#_bookmark3" id="_bookmark3"></a>

#### Go to Admin > Stores > Configuration > Scommerce Configuration > Ajax Login & Wishlist

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Enable Ajax Wish List –** Select “Yes” or “No” to enable or disable the Ajax Wish List.
* **Enable Ajax Login –** Select “Yes” or “No” to enable or disable the Ajax Login
* **Enable Slide Down Mini Cart –** Select “Yes” or “No” to enable or disable slide down effect of mini cart after adding item to the basket.

![](../../.gitbook/assets/ajax\_general.jpg)

### <mark style="color:blue;">Front-end site view</mark> <a href="#_bookmark5" id="_bookmark5"></a>

#### <mark style="color:orange;">Ajax Add to Wishlist - Ajax SignIn Popup</mark> <a href="#_bookmark6" id="_bookmark6"></a>

No more waiting to be redirected to the Sign In page. When you click on Sign in a pop-up will appear on your screen and you will be able to login to the site without reloading the page. It is great for ease of access as well as saves time. Also, it does not matter which page you are browsing the pop-up will work with most pages. To enable the Ajax login feature first login to your admin panel.

![](<../../.gitbook/assets/7 (8)>)

#### <mark style="color:orange;">Ajax Add to Wishlist – Ajax Create an Account Popup</mark> <a href="#_bookmark7" id="_bookmark7"></a>

Enables users to create an account or register on the website via a pop-up. Initially upon clicking on create an account users were redirected to a different page but now you can stay where you are browsing and create an account without having to reload or redirect the page. It makes convenient for new users to gain access.

You can toggle this feature on or off by loggin into your admin panel and then going to the path **Stores > Configuration > Scommerce Configuration > Ajax Login & Wishlist**. There will be flag named Enable Ajax Login you can select “Yes” or “No” from the drop-down that will turn this feature on or off.

![](<../../.gitbook/assets/8 (14)>)

#### <mark style="color:orange;">Ajax Add to Wishlist – Mini Cart Drop-Down Slider</mark> <a href="#_bookmark8" id="_bookmark8"></a>

When products are added to the cart a drop-down slider appears in the mini cart. It makes easy for users to keep track of their products that they have added to the cart. You can scroll down to browse your products in the cart. The number of products to appear in the list can be changed from settings.

This feature can be enabled or disabled from the admin panel. First Login to your admin panel then go to the following path **Stores > Configuration > Scommerce Configuration > Ajax Login & Wishlist**. There you will have an option named

Enable slide down mini cart, from the drop-down menu select “Yes/No” to Enable/Disable this feature.

#### <mark style="color:orange;">Limit the Quantity of Products to Show in the Cart Slider</mark> <a href="#_bookmark9" id="_bookmark9"></a>

Also, you can limit the quantity of products to show in the cart slider. You can do that by going into **Stores > Configuration > Sales > Checkout > Shopping cart sidebar**. There you will see an option named Number of items to display scrollbar. Here enter your quantity and the scrollbar will appear after that many number of products are added to the cart.

![](<../../.gitbook/assets/9 (52)>)

#### <mark style="color:orange;">Ajax Add to Wishlist – Ajax Add to Wishlist Popup</mark> <a href="#_bookmark10" id="_bookmark10"></a>

Generally, when a product is added to the wishlist you are redirected to another page but while this setting is enabled you will be able to add products to wishlist without redirecting or reloading the page. If you are not signed In, a pop-up will appear on the screen saying either sign in or create an account. This feature can be enabled

or disabled by log in to your admin panel then going to the path **Stores > Configuration > Scommerce Configuration > Ajax Login & Wishlist.** Here you will see an option named Enable Ajax Wish List, from the drop-down select Yes/No to Enable/Disable this functionality.

![](<../../.gitbook/assets/10 (33)>)

#### <mark style="color:orange;">Ajax Add to Wishlist – Ajax Add to Wishlist Confirmation Message</mark> <a href="#_bookmark11" id="_bookmark11"></a>

While this option is enabled when any product is added to the cart you will receive a pop-up message on the screen showing your product has been successfully added to the wishlist. Keep in mind you need to be logged in to add products to wishlist.

![](<../../.gitbook/assets/11 (12)>)

#### <mark style="color:orange;">Ajax Add to Wishlist – Wishlist Products Under my Account – My Wishlist Section</mark> <a href="#_bookmark12" id="_bookmark12"></a>

All the products added to the wishlist should be visible under your account under the wishlist section. Add multiple products to Wishlist without reloading the page every time and view them listed in the wishlist section of your account.

![](../../.gitbook/assets/ajax\_front.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-ajax-login-add-to-wishlist.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
