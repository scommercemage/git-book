# Magento 2 Apply Discount coupon Code Via Link

### <mark style="color:blue;">Installation and User Guide for Magento 2 Apply Discount Coupon Code via Link Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-apply-discount-coupon-code-via-link.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Auto Coupon_ ](magento-2-apply-discount-coupon-code-via-link.md#bookmark3)
   * _General Settings_&#x20;
3. [_Discount Setup_](magento-2-apply-discount-coupon-code-via-link.md#discount-setup)
4. [_Discount Link_ ](magento-2-apply-discount-coupon-code-via-link.md#discount-link)
5. [_Front-end site view_ ](magento-2-apply-discount-coupon-code-via-link.md#bookmark7)
   * _Successful Applied Discount Message on the Front-end_&#x20;
   * _Coupon Code On the Checkout Page_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Auto Coupon</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Auto Coupon**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Message After Applying Code –** Message which will displays on the site after successful application of coupon code.

![](../../.gitbook/assets/general\_applydiscount.png)

### <mark style="color:blue;">**Discount Setup**</mark>&#x20;

You can set up the discount coupon code **from Admin > Marketing > Cart Price Rules >** Click **"Add New Rule",** it redirects on **"**New Cart Price Rule" and by providing all the required details you can create the new rule and set up the discount code.

![](../../.gitbook/assets/applydiscount\_cartpricerules.png)

### <mark style="color:blue;">**Discount Link**</mark>&#x20;

Once the discount is set up then on the front-end it can be applied using the below link :-

**http://{\[siteurl\}}/applydiscount/?code={\[discount\_code\}}\&redirect\_url={\[any\_url\_ of\_your\_site\}}**

1. **Site url –** Site base URL.
2. **Discount Code –** Discount code as set up in discount.
3. **Returning Site URL –** This is optional parameter. If defined, user will be redirected to this URL after successful application of the discount code. If not defined then User will be redirected to the Home page.

![](../../.gitbook/assets/applydiscount\_discountlink.jpg)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#bookmark7" id="bookmark7"></a>

* <mark style="color:orange;">**Successful Applied Discount Message on the Front-end -**</mark> The message you have set from **Admin > Stores > Configuration > Scommerce Configuration > Auto Coupon > Message After Applying Code**, will be shown on the front-end homepage.

![](../../.gitbook/assets/applydiscount\_front1.jpg)

* <mark style="color:orange;">**Coupon Code On the Checkout Page -**</mark> Applied discount coupon code will be shown on the front-end checkout page under "Order Summary" section.

![](../../.gitbook/assets/applydiscount\_front2.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-apply-coupon-via-link.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
