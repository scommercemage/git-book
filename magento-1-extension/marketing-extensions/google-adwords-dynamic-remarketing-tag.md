# Google Adwords Dynamic Remarketing Tag

### <mark style="color:blue;">Installation and User Guide for Magento 1 Google Adwords Dynamic Remarketing Tag</mark>

**Table of Contents**

1. [Installation ](google-adwords-dynamic-remarketing-tag.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Google Remarketing ](google-adwords-dynamic-remarketing-tag.md#\_bookmark4)
   * General Settings&#x20;
   * Dynamic Remarketing Tag, Code Snippets on the Homepage&#x20;
   * Dynamic Remarketing Tag/Code Snippets with Product Details&#x20;
   * Dynamic Remarketing Ad&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Google Remarketing</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Remarketing**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Google Conversion Id –** Enter your Google Conversion Id.
* **Enable Tracking for other sites –** This will enable other site variables ([https://developers.google.com/adwords-remarketing-tag/parameters#other](https://developers.google.com/adwords-remarketing-tag/parameters#other)) instead of retail site variable.
* **Enable dynamic remarketing tags –** Set yes to enable dynamic remarketing tag.
* **Product ID attribute –** Use the same id you have submitted in your Google base feed.
* **Enable GDPR cookie check –** If you are using our GDPR extension or any other GDPR Extension and you want to block sending information to Google then set this to “yes” based on customer preference. **Please note this is optional as far as you are not sending any PII to Google this setting needs to be turned off.**

![](../../.gitbook/assets/m1dynamic\_general.png)

* <mark style="color:orange;">**Dynamic Remarketing Tag, Code Snippets on the Homepage –**</mark> To view remarketing tag and code snippets go to **Homepage > View Source**. In the below image you can see the conversion ID and Custom variable. You can add conversion Id from **Admin > Stores > Configuration > Google Remarketing > Google Conversion Id.**

![](<../../.gitbook/assets/2 (10)>)

* <mark style="color:orange;">**Dynamic Remarketing Tag/Code Snippets with Product Details –**</mark>** ** In the code snippet you can see the product details with Product ID and Google conversion id. You can select Product Id attribute from **Admin > Stores > Configuration > Google Remarketing > Product Id attribute** – Select **“SKU”.**

![](<../../.gitbook/assets/3 (25)>)

* <mark style="color:orange;">**Dynamic Remarketing Ad –**</mark> When you enable the dynamic remarketing from **Admin > Stores > Configuration > Google Remarketing > Enable dynamic remarketing tags**, then it shows ads to people who have previously visited your website.

![](<../../.gitbook/assets/4 (60)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-google-adwords-dynamic-remarketing-tag.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
