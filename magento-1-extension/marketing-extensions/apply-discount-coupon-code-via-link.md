# Apply Discount Coupon Code via Link

### <mark style="color:blue;">Installation and User Guide for Magento 1 Apply Discount Coupon code via link</mark>

**Table of Contents**

1. [Installation ](apply-discount-coupon-code-via-link.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Auto Apply Coupon Code ](apply-discount-coupon-code-via-link.md#\_bookmark4)
   * General Settings&#x20;
3. [Discount Setup](apply-discount-coupon-code-via-link.md#discount-setup)&#x20;
4. [Discount Link](apply-discount-coupon-code-via-link.md#discount-link)&#x20;
5. [Front-end Site View](apply-discount-coupon-code-via-link.md#\_bookmark8)&#x20;
   * Successful Applied Discount Message on the Front-end&#x20;
   * Successful Applied Discount Message on the Cart Page&#x20;
   * Coupon Code on the Checkout Page&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Auto Apply Coupon Code</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Auto Apply Coupon Code**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Message after applying code –** Message which will displays on the site after successful application of coupon code.

![](../../.gitbook/assets/m1dis\_general.jpg)

### <mark style="color:blue;">**Discount Setup**</mark>&#x20;

You can set up the discount coupon code from **Admin > Promotions> Shopping Cart Price Rules** > Click **“Add New Rule”** , it redirects on “New Cart Price Rule” and by providing all the required details you can create the new rule and set up the discount code.

![](../../.gitbook/assets/m1dis\_rules.jpg)

### <mark style="color:blue;">**Discount Link**</mark>&#x20;

Once the discount is set up then on the front-end it can be applied using the below link: -

**`http://{[siteurl}}/applydiscount?code={[discount_code}}&returning_url={[any_url_of_ your_site}}`**

1. **Site url –** Site base URL
2. **Discount Code –** Discount code as set up in discount
3. **Returning Site URL –** This is optional parameter, If defined, user will be redirected to this URL after successful application of the discount code, If not defined then User will be redirected to the Home page.

![](<../../.gitbook/assets/3 (17)>)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark8" id="_bookmark8"></a>

* <mark style="color:orange;">**Successful Applied Discount Message on the Front-end –**</mark> The message set from **Admin > Configuration > Auto Apply Coupon Code > Message After Applying Code**, will be shown on the front-end homepage.

![](<../../.gitbook/assets/4 (75)>)

* <mark style="color:orange;">**Successful Applied Discount Message on the Cart Page -**</mark>

![](<../../.gitbook/assets/5 (53)>)

* <mark style="color:orange;">**Coupon Code on the Checkout Page –**</mark>** ** Applied discount coupon code will be shown on the front-end checkout page under “Order Summary” section.

![](<../../.gitbook/assets/6 (49)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-apply-coupon-via-link.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
