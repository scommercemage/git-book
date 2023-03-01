# Magento Google Tag Manager with Enhanced Ecommerce Tracking and Google Analytics 4(GA4)

### <mark style="color:blue;">Installation and User Guide for Magento 1 Google Tag Manager with Enhanced Ecommerce Tracking</mark>

**Table of Contents**

1. [Installation ](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Google Tag Manager Pro Tracking ](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark4)
   * General Settings&#x20;
3. [JSONs provided with extension package ](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark6)
   * Enhanced Ecommerce Universal Analytics&#x20;
   * Facebook Pixel&#x20;
   * Adwords Dynamic Remarketing&#x20;
4. [Importing JSONs into GTM](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark10)&#x20;
5. [Setting variable information in GTM](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark11)&#x20;
6. [Publishing Tags in GTM](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark12)&#x20;
7. [Set up Enhanced Ecommerce in Google Analytics](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark13)&#x20;
8. [AJAX Add to Basket or Remove from Basket ](magento-google-tag-manager-with-enhanced-ecommerce-tracking-and-google-analytics-4-ga4.md#\_bookmark14)
   * AJAX Add to Basket&#x20;
   * AJAX Remove from Basket&#x20;
   * Back-end/Admin Tracking&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System>Tools > Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Google Tag Manager Pro Tracking</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Tag Manager Pro Tracking**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Container Id –** Enter your Google Tag Manager Container Id.
* **Enhanced Ecommerce –** Set “yes” to enable the enhanced ecommerce
* **Brand Attribute –** Select brand attribute to send brand information to Google Analytics.
* **Brand text box –** If you don’t have brand attribute and you want to send default brand name to Google Analytics then you can enter here.
* **Base –** Set “Yes” if you want to send base order data and ‘No’ to send store order data to Google. Set this to “Yes” always unless you have multi- store/currency is enabled and you want to send different currency data to Google.
* **Send Phone or Admin Orders –** Enable this feature only if you want to send admin orders on order creation.
* **Source –** Add source you want to pass to Google for admin orders.
* **Medium –** Add medium you want to pass to Google for admin orders**.**
* **Enable dynamic remarketing tags and facebook tracking –** Set yes to enable dynamic remarketing tags and facebook tracking.
* **Product ID Attribute –** Select attribute for Product ID, this should be same attribute as you have in your Google Base Feed.
* **Enable Google Optimize –** Set “Yes” to add page-hiding snippet code for google optimize.
* **Enable GDPR cookie check –** If you are using our GDPR Extension or any other GDPR Extension and you want to block sending information to Google then set this to “yes” based on customer preference. Please note this is optional as far as you are not sending any PII to Google this setting needs to be turned off.
* **Order Total Include VAT –** If set to “Yes” then VAT will be included in order total.

![](../../.gitbook/assets/m1gtm\_general1.jpg)

![](../../.gitbook/assets/m1gtm\_general2.jpg)

### <mark style="color:blue;">JSONs provided with extension package</mark> <a href="#_bookmark6" id="_bookmark6"></a>

The extension package contains JSONs which can be imported in GTM to set up required Tags, Triggers and Variables. The JSONs can be used to set up

* Enhanced Ecommerce Universal Analytics
* Facebook Pixel
* Adwords Dynamic Remarketing

### <mark style="color:blue;">Importing JSONs into GTM</mark> <a href="#_bookmark10" id="_bookmark10"></a>

To import JSONS provided with extension package follow below steps:

1. Log into GTM and navigate to your Account and container
2. In the top navigation, click through the Admin

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/2 (26)>)

1. Under the container options, click on Import Container

![](<../../.gitbook/assets/3 (8)>)

1. Choose the JSON file which you would like to import

![](<../../.gitbook/assets/4 (34)>)

1. Choose to either Overwrite or Merge
   * Overwriting the existing container will remove all your existing tags, triggers, and variables, and will replace them with those in the imported container. A new container version will be created before the import.
   * Merging containers will let you keep your existing tags, triggers, and variables, and just add in the new ones. If you choose to Merge the new container with your existing container, you’ll have to then decide whether you want to overwrite conflicting tags or rename conflicting tags.

* **Overwrite –** If a variable, tag, or trigger in the new container has the same name but the contents are different, overwrite the old one with the new one.
* **Rename –** If a variable, tag, or trigger in the new container has the same name but the contents are different, keep the old one and rename the new one.

1. **Click Continue**. You’ll see a preview of changes, showing how many tags, triggers, and variables will be added, modified, or deleted. You can also click the link to View Detailed Changes to see which tags, triggers, and variables are being added, modified, or deleted.

![](<../../.gitbook/assets/5 (28)>)

1. Once you’re satisfied with the changes, click _Confirm_.

### <mark style="color:blue;">Setting variable information in GTM</mark> <a href="#_bookmark11" id="_bookmark11"></a>

Once the GTM container file has been imported, you need to change variable information with correct value corresponding to the site. To access variables, go to workspace where you have imported the JSONs and click on variables on left hand side navigation.

![](<../../.gitbook/assets/6 (51)>)

#### <mark style="color:orange;">Variables Created with JSON’s</mark>

* **GA ID –** This variable is created when GTM-UniversalAnalytics.json is imported and it holds value for Google Analytics Id for the site. Click on the GA ID and change it to correct value.

![](<../../.gitbook/assets/7 (14)>)

* <mark style="color:orange;">**conversionID -**</mark>** ** This variable is created when GTM- AdwordsDynamicRemarketing.json is imported and it holds value for Google Adwords Conversion Id for the site. Click on the conversionID and change it to correct value.

![](<../../.gitbook/assets/8 (8)>)

* <mark style="color:orange;">**facebookPixelID -**</mark>** ** This variable is created when GTM-Facebook.json is imported and it holds value for Facebook pixel Id for the site. Click on the facebookPixelID and change it to correct value.

![](<../../.gitbook/assets/9 (34)>)

* <mark style="color:orange;">**currencyCode -**</mark>** ** This variable is created when GTM-Facebook.json is imported and it holds value for currency used on site. Click on the currencyCode and change it to correct value.

![](<../../.gitbook/assets/10 (35)>)

### <mark style="color:blue;">Publishing Tags in GTM</mark> <a href="#_bookmark12" id="_bookmark12"></a>

Once all set up is done and verified, need to Publish the tags to make it live on the website.

**Step 1** − Click the SUBMIT button at the top right corner of the screen. It will show the following screen.

![](<../../.gitbook/assets/11 (35)>)

**Step 2** − Enter an identifiable Version name so that it can be easily understood for the changes made.

With the version description, you can be as elaborate as possible on the changes/additions of the tag in that version.

**Step 3** − Scroll down to the Workspace Changes, you will see all the changes made in the tags, which are unpublished or in the PREVIEW mode.

**Step 4** − Click PUBLISH and you will be presented with a summary for this version.

### <mark style="color:blue;">Set up Enhanced Ecommerce in Google Analytics</mark> <a href="#_bookmark13" id="_bookmark13"></a>

#### <mark style="color:orange;">**To turn on Enhanced E-commerce for a view, and label your checkout steps:**</mark>

1. Click Admin at the top of any Analytics page.
2. Select the view for which you want to enable Enhanced E-commerce reporting.
3. In the view column, click E-commerce Settings.
4. Under **Step 1**, Enable E-commerce, set the status to ON.
5. Click Next Step.
6. Under **Step 2**, Enhanced Ecommerce Settings, set the status to ON. When you turn this option on
   * You can see the Enhanced E-commerce reports in the conversions section
   * The older, older category of E-commerce reports is no longer visible

You can turn this option off to restore the older category of E-commerce reports.

* Optionally, enter labels for the checkout steps that you have defined in your Magento steps configuration. Please see screenshots below for reference

![A screenshot of a social media post  Description automatically generated](<../../.gitbook/assets/12 (31)>)

* Click Submit.

### <mark style="color:blue;">AJAX Add to Basket or Remove from Basket</mark> <a href="#_bookmark14" id="_bookmark14"></a>

Add the following two functions in your ajax add to basket js file and call **gaAddToCart** on success of Ajax add to basket and **gaRemoveFromCart** on success of Ajax remove from basket function.

#### <mark style="color:orange;">AJAX Add to Basket</mark> <a href="#_bookmark15" id="_bookmark15"></a>

```
Function gaAddToCart(){jQuery.cookie.json = true;var productToBasket = jQuery.cookie(“productToBasket”);var productlist = jQuery.cookie(“productlist”);if (productToBasket!= undefined){manipulationOfCart(productToBasket,’add’,productlist);jQuery.remo veCookie(“productToBasket” , { path: ‘/’, domain: ‘.’ + document.domain});}}
```

#### <mark style="color:orange;">AJAX Remove from Basket</mark> <a href="#_bookmark16" id="_bookmark16"></a>

```
Function gaRemoveFromCart(){jQuery.cookie.json = true;var productOutBasket = jQuery.cookie(“productOutBasket”);if (productOutBasket != undefined){manipulationOfCart(productOutBasket, ‘remove’, “);jQuery.removeCookie(“productOutBasket” , { path: ‘/’ , domain: ‘.’ + document.domain});}}
```

* <mark style="color:orange;">**Back-end/Admin Tracking -**</mark>** ** When you enable the **"**Send Phone or Admin Orders **"** from **Admin > Stores > Configuration > Scommerce Configuration > Google Tag Manager Pro Tracking,** then it tracks admin orders. To see admin order go to **GA > Conversion > Ecommerce > Sales Performance.**

![A screenshot of a social media post  Description automatically generated](<../../.gitbook/assets/13 (8)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-next-order-discount.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
