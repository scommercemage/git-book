# Magento 1 Google Global Site Tag (gtag.js)

### <mark style="color:blue;">Installation and User Guide for Magento 1 Google Global Site Tag (gtag.js)</mark>

**Table of Contents**

1. [Installation ](magento-1-google-global-site-tag-gtag.js.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Google Global Site Tag ](magento-1-google-global-site-tag-gtag.js.md#\_bookmark4)
   * General Settings&#x20;
   * Admin Transactions Tracking&#x20;
   * Backend Order Tracking in Google Analytics&#x20;
   * Backend Order Tracking - Source/Medium&#x20;
   * Google Analytics Checkout Behaviour&#x20;
   * Google Analytics Shopping Behaviour&#x20;
   * Google Analytics Sales Performance&#x20;
3. [Front-end Site view ](magento-1-google-global-site-tag-gtag.js.md#\_bookmark12)
   * Home Page with Tags&#x20;
   * Gtag.js Code&#x20;
   * Gtag.js Brand Name&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Google Global Site Tag</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Global Site Tag**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](file:///C:/Users/ri/Downloads/core%40scommerce-mage.com)
* **Accounts Id –** You can add multiple account id. It can be analysis, adwords.
  * **Main Account –** Select “Yes” to set your main analytics id as an account id. This account will be used to connect gtag.js.
  * **Use Linker –** If this is enabled (set to “Yes”) then this account will be linked to domains from “Domains to link” field, which is specified below.
  * **Action –** You can delete your account.
* **Promotion Tracking –** Here is the format to set up the promotion tracking: `<a href=’#’ data-track-promo-id=”PROMOID” data-track-promo- name=”PROMONAME” data-track-promo-creative=”PROMOCREATIVE” data-track-promo-position=”PROMOPOSITION” >Content</a>`
* **Brand Attribute –** Please select brand attribute, if you have one otherwise put your brand name in the below input box.
* **Brand Text Box –** Enter your brand name. Set brand name if there is no brand name with the product.
* **Enhanced Ecommerce Enabled–** Select “Yes” to enable this module. Please make sure this feature is enabled in Google Analytics first before enabling in Magento.
* **Send Base Data –** Set “Yes” if you want to send base order data and “No” to send store order data to Google.
* **Enable Google Optimize –** Select “Yes” to enable the module, or “No” to disable it.
* **Enable Linker –** If this is enabled then you can set linker properties, which is specified below e.g. Domain to link, Decorate Forms.
* **Dynamic Remarketing Enabled –** If set to “Yes” then this will enable and install remarketing tag to different pages.
* **Dynamic Remarketing other sites –** Set “Yes” to enable other site variables ([https://developers.google.com/adwords-remarketing-](https://developers.google.com/adwords-remarketing-tag/parameters#other) [tag/parameters#other](https://developers.google.com/adwords-remarketing-tag/parameters#other)) instead of retail site variables.

![](../../.gitbook/assets/m1gtag\_general1.jpg)

![](../../.gitbook/assets/m1ua\_general2.jpg)

#### <mark style="color:orange;">Admin Transactions Tracking</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* **Send Backend Transactions –** Set “Yes” if you want to send base order data and “No” to send store order data to Google created from admin panel.
* **Admin Source –** Please add the Campaign source for backend orders.
* **Admin Medium –** Please define the Campaign Medium for Backend Orders.

![](../../.gitbook/assets/m1gtag\_admintrans.jpg)

* <mark style="color:orange;">**Backend Order Tracking in Google Analytics –**</mark>** ** You can track admin orders by selecting “Yes” for **“ Admin Transactions Tracking “** from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Admin Transactions Tracking – “Yes”.** In the below Image you can see the tracked admin orders in Google Analytics.

![](../../.gitbook/assets/m1gtag\_backendordertracking.jpg)

* <mark style="color:orange;">**Backend Order Tracking - Source/Medium –**</mark>** ** To add campaign Source and Medium for backend orders go to **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Admin Transactions Tracking – “phone” > Admin Medium – “admin”.**

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/5 (1)>)

* <mark style="color:orange;">**Google Analytics Checkout Behaviour –**</mark>** ** You can view the checkout behaviour in GA tool under **Conversions > Ecommerce > Checkout Behaviour.**

![](../../.gitbook/assets/m1gtag\_checkoutbeha.jpg)

* <mark style="color:orange;">**Google Analytics Shopping Behaviour –**</mark>** ** You can view the shopping behaviour with all sessions, product views, add to cart and checkout details in GA tool under **Conversions > Ecommerce > Shopping Behaviour.**

![](<../../.gitbook/assets/7 (51)>)

* <mark style="color:orange;">**Google Analytics Sales Performance –**</mark>** ** You can view the shopping behaviour with all sessions, product views, add to cart and checkout details in GA tool under **Conversions > Ecommerce > Sales Performance.**

![](<../../.gitbook/assets/8 (28)>)

### <mark style="color:blue;">Front-end Site view</mark> <a href="#_bookmark12" id="_bookmark12"></a>

* <mark style="color:orange;">**Home Page with Tags –**</mark> In Tag Assistant tool you can see all the fired tags.

![](../../.gitbook/assets/m1gtag\_front1.jpg)

* <mark style="color:orange;">**Gtag.js Code –**</mark>** ** In the below image you can see the **UA** and **AW** tracking id’s added from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Account Id > Click on “Add Account”** – UA - 33387561-3, AW – 123456789.

![](<../../.gitbook/assets/10 (11)>)

* <mark style="color:orange;">**Gtag.js Brand Name –**</mark>** ** You can add brand name from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Brand name – “TestScommerce”**

![](<../../.gitbook/assets/11 (2)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-facebook-conversion-audience-tracking.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
