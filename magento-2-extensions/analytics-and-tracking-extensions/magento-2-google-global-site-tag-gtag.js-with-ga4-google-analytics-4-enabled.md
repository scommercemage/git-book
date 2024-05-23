# Magento 2 Google Global Site Tag (gtag.js) with GA4(Google Analytics 4) Enabled

### <mark style="color:blue;">Installation and User Guide for Magento 2 Global Site Tag (gtag.js) Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
   * _Installation via Composer(Hyvä Theme)_
2. [_Configuration Settings for Tracking Base_](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Checkout Behaviour_
3. [_Configuration Settings for Global Site Tag (gtag.js)_ ](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark3-1)
   * _General Settings_&#x20;
4. [_Backend Tracking_](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark5)
   * _Backend Order Tracking in Google Analytics_&#x20;
   * _Backend Order Google Analytics Source/Medium_&#x20;
   * _Google Analytics Checkout Behaviour_&#x20;
   * _Google Analytics Shopping Behaviour_&#x20;
   * _Google Analytics Sales Performance_
5. [_Set up Google Analytics 4_](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark11)
6. [_Link Google Optimize with Google Analytics Account_](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark12)
7. [_Front-end Site view_ ](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#\_bookmark12)
   * _Home Page with Tags_&#x20;
   * _Gtag.js Code_&#x20;
   * _Gtag.js Brand Name_&#x20;

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

* <mark style="color:orange;">**Installation via Composer(Hyvä Theme):**</mark> Go to My Account section then go to Composer Instructions. Run the composer config commands mentioned on the page then run the below command to install the module on hyva theme.&#x20;

```
composer require hyva-themes/magento2-scommerce-gtag
```

### <mark style="color:blue;">Configuration Settings for Tracking Base</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Tracking Base**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **Enable Enhanced Ecommerce –** Select ‘Yes’ to enable this module. Please make sure this feature is enabled in Google Analytics first before enabling in Magento2.
* **Product ID Attribute –** Select the attribute which you have submitted in your Google base feed. For e.g. SKU
* **Brand Attribute –** Please select brand attribute, if you have one otherwise put your brand name in the below input box.
* **Use Base Currency -** Set ‘Yes’ if you want to send base order data and ‘No’ to send store order data to Google. Set this ‘No’ only when you have multicurrency and you want to send different currency data to Google.

![](<../../.gitbook/assets/1 (2).png>)

* **Product Price Include Tax-** Set “Yes” then VAT will be included in the price.
* **Order Total Include VAT –** Set “Yes” then VAT will be included in order total.
* **Always Send Parent SKU –** Set “Yes” then it always send parent sku instead of child sku to GA during checkout.
* **Category Attribute-** Please select category attribute if you have one otherwise put your brand name in the below input box. **Attribute should be available for product listing 'Storefront Properties -> Used in Product Listing = Yes'**
* **Is Category ID-** Set "Yes" if "Category Attribute" is ID of the category, "No" if it is plain value

![](<../../.gitbook/assets/2 (1).png>)

* **Send Parent Category –** Set “Yes” to send the category path and Set “No” to send the category name only.
* **Default List-** Enter the default list name if the product impression is not found
* **Send Admin Orders to Google–** Select “Yes” to track orders created in admin
* **Source-**Please add the Campaign Source for backend orders.
* **Medium-**Please define the Campaign Medium for Backend Orders.
* **Send Product Impression on Scroll -** Enable this feature when you have loads of products on product listing / category pages.
* **Category Ajax Enabled –** Enable this feature if you have third party ajax enabled extension on your category page.

![](../../.gitbook/assets/tbase\_890x.png)

#### <mark style="color:orange;">Checkout Behaviour</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Add Carrier Title:-** Use this to add carrier title to the shipping step. Set "Yes" to send _carrier\_code::carrier\_title_. Ex. flatrate::Flat Rate
* **Add Payment Title :-** Use this to add payment method title to payment step. Set "Yes" to send _method::title_. Ex. checkmo::Check / Money Order
* **Steps Configuration:-** define checkout steps
  * **Step:-** number of step
  * **Selector:-** add the selector for the step. Basic selector could be '#customer-email' this is equals to '#customer-email/change' and will send customer email itself
  * **Type:-** choose the step type from the dropdown

![](<../../.gitbook/assets/5 (1).png>)

### <mark style="color:blue;">Configuration Settings for Global Site Tag (gtag.js)</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js)**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Accounts ID –** You can add multiple account id, it can be Analytics, Adwords.
  * **Main Account –** Select ‘Yes’ to set your main analytics id as an account id. This account will be used to connect gtag.js.
  * **Use Linker –** If this is enabled (set to ‘Yes’) then this account will be linked to domains from “Domains to link” field, which is specified below
  * **Action –** You can delete your account\\, if required.
* **Enable Optimize –** Select ‘Yes’ to enable the module, or ‘No’ to disable it.
* **Optimize Container ID –** Enter your Google Optimize container ID here.

![](../../.gitbook/assets/gtag1.png)



* **Enable Linker -** If this is enabled then you can set linker properties, in domain configurations which is specified below e.g. Domain to link, Decorate Forms.
* **Domains to Link -** Enter the domains that you want to link. Example destination.com, dest3.com or /^example.(com|de|nl)$/.
* **Decorate Forms -** If you have forms on site pointing to the destination domain, set this property of the linker parameter to Yes
* **Promotion Tracking –** Here is the format to set up the promotion tracking: \<a href= ”#” data-track-promo-id=”PROMOID” data-track-promo- name=”PROMONAME” data-track-promo-creative=”PROMOCREATIVE” data-track-promo-position=”PROMOPOSITION” >Content\</a>
* **Enable Dynamic Remarketing Tag –** If set to ‘Yes’, then this will enable and install remarketing tag to different pages.
* **Enable Tracking for Other Sites –** This will enable other sites variables ([https://developers.google.com/adwords-remarekting-tag/parameters#other)](https://developers.google.com/adwords-remarekting-tag/parameters#other) instead of retail site variables.

![](../../.gitbook/assets/gtag2.png)

### Backend Tracking <a href="#bookmark5" id="bookmark5"></a>

* <mark style="color:orange;">**Backend Order Tracking in Google Analytics -**</mark> You can track admin orders by selecting "Yes" for " **Enabled Backend Tracking**" from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Backend Tracking Configuration > Enabled Backend Tracking - "Yes".** In the below image you can see the tracked admin orders in Google analytics.

![](../../.gitbook/assets/gtag\_backendorder.jpg)

* <mark style="color:orange;">**Backend Order Google Analytics Source/Medium -**</mark> To track/add Campaign Source and Medium for backend orders, add campaign source and medium from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Backend Tracking Configuration > Backend Campaign Source - "phone" > Campaign Medium -"admin".**

![](<../../.gitbook/assets/4 (51)>)

* <mark style="color:orange;">**Google Analytics Checkout Behaviour -**</mark> You can see the checkout behaviour in GA with billing & shipping method, payment method and transactions details.

![](../../.gitbook/assets/gtag\_checkoutbehaviour.jpg)

* <mark style="color:orange;">**Google Analytics Shopping Behaviour -**</mark> In below image you can see the shopping behaviour with all sessions, product views, add to cart, checkout details.

![](../../.gitbook/assets/gtag\_shoppingbehaviour.jpg)

* <mark style="color:orange;">**Google Analytics Sales Performance -**</mark> Placed order details in GA, with Transaction ID, Tax, Shipping, Refund Amount and Quantity details.

### <mark style="color:blue;">Set up Google Analytics 4</mark> <a href="#bookmark11" id="bookmark11"></a>

* Go to Analytics and select the website on which you want to implement GA4 alongside universal analytics.
* Once you are in universal analytics panel go into admin settings. Here you will notice an UPGRADE TO GA4 button, click on it. You will be walked with creating a new property. Follow along, once you are finished you will see the new GA4 view on your screen

![](../../.gitbook/assets/gtag\_ga41.jpg)

### <mark style="color:blue;">Link Google Optimize with Google Analytics Account</mark> <a href="#bookmark12" id="bookmark12"></a>

If the optimize is enabled in the extension then you need link the Google optimize account with the Google analytics account otherwise the data won't be tracked in GA. Once the optimize setup is complete you need to add the optimizer ID in the Gtag configuration to enable linking. Please follow the steps below to link the optimizer account with Google Analytics account.&#x20;

**Step 1:-** Begin Setup of your Google optimize account by visiting [https://optimize.google.com/optimize/home/#/accounts](https://optimize.google.com/optimize/home/#/accounts)

**Step 2:-** Click on get started to start the setup, click on next after selecting the subscribe options

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

**Step 3:-** Choose the account settings and acknowledge the service aggreements and click on lets go on the next screen upon which a popup window will appear.

<figure><img src="../../.gitbook/assets/image (19) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Step 4:-** Enter the name and URL of the store then select the experience and click on create.

<figure><img src="../../.gitbook/assets/image (12) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

**Step 5:-** In the next window scroll down and click on Link Analytics.

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

**Step 6:-** Select the analytics property that you want to link and then click on the link button

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

**Step 6:-** Click on view instructions which will reveal the optimize code that we will add in the configuration to finish the setup.

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

**Step 7:-** Copy the code from the above screen then go to stores>configuration>Scommerce confguration>Global Site Tag(gtag.js) then enter the ID in optimize container ID as shown below. Once done your Google optimize and Google Analytics accounts are now linked.

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Front-end Site view</mark> <a href="#bookmark12" id="bookmark12"></a>

* <mark style="color:orange;">**Home Page with Tags -**</mark> In Tag Assistant tool you can see all the fired tags.

![](../../.gitbook/assets/gtag\_front1.jpg)

* <mark style="color:orange;">**Gtag.js Code -**</mark> In the below image you can see the UA and AW tracking id’s from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Account Id** > Click on **“Add Account”** – UA – 33387561-8, AW- 12345678.

![](<../../.gitbook/assets/11 (28)>)

* <mark style="color:orange;">**Gtag.js Brand Name –**</mark> You can add brand name from **Admin > Stores > Configuration > Scommerce Configuration > Global Site Tag (gtag.js) > Brand Name – “TestScommerce”.**

![](../../.gitbook/assets/gtag\_front3.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](magento-2-google-global-site-tag-gtag.js-with-ga4-google-analytics-4-enabled.md#installation-and-user-guide-for-magento-2-how-did-you-hear-about-us-extension) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
