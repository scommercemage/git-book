# Magento 1 Google Analytics Synchronization Extension

### <mark style="color:blue;">Installation and User Guide for Magento 1 Google Analytics Synchronization Extension</mark> <a href="#toc62670227" id="toc62670227"></a>

**Table of Contents**

1. [_Installation_](magento-1-google-analytics-synchronization-extension.md#bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [_Configuration Settings for Google Analytics Synchronization_](magento-1-google-analytics-synchronization-extension.md#toc65169380)
   * _General Settings_
3. [_Create Project in Google Developer Console for GA Reporting API_ ](magento-1-google-analytics-synchronization-extension.md#toc65169382)

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark> To check that this is disabled, go to **System>Tools > Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Google Analytics Synchronization</mark> <a href="#toc65169380" id="toc65169380"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Analytics Synchronization**

#### <mark style="color:orange;">**General Settings**</mark> <a href="#toc65169381" id="toc65169381"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Application Name –** It is the project name that you get from Google console. ( https://console.developers.google.com/ )
* **Security key (JSON) –** Security key JSON file can be obtained from Google Console under account credentials.
* **Exclude order statuses –** You can choose to exclude certain order statues from sync. These orders won’t be synced with Google Analytics.
* **Send Base Data –** Select whether you want to send base order data or store order data.
* **Brand Attribute –** Select a brand attribute to send with brand names
* **Brand Text box –** Input brand name to send to Google
* **Default Landing Page -** This setting allows you to set default landing page value which shows in Google Analytics in case landing page is not available to sent as part of missing transaction.
* **Cron Schedule –** Schedule specific cron time to run the sync automatically.
* **Debugging –** Enabling debugging will generate a detailed log report in /var/log directory
* **Test Mode-** This setting allows you to check missing transactions before we send the transactions to GA. It helps in validating the data before it gets posted to Google Analytics
* **API Secret –** Enter the API secret key here. API secret key can be created by going into GA4>Admin>Data Streams>Select website>Measurement Protocol API Secrets>Create enter the name and click on create to get the key.
* **Skip Order days –** Enter the number of days that will be skipped before sending to GA4. Please put greater than 0 value. This is done to avoid duplicate transactions. For eg:- Suppose if you enter 2 then orders from 2days ago will be synced today.
* **Measurement ID –** Enter the measurement ID of your GA4 property. Ga4 measurement ID can be extracted from **GA4>Admin>Data Streams>Select website and it is available in the top right corner.**
* **Property ID –** Enter the property ID of GA4. **GA4>Admin>Property Settings>Property ID**&#x20;

### <mark style="color:blue;">Create Project in Google Developer Console for GA Reporting API</mark> <a href="#toc65169382" id="toc65169382"></a>

Please follow the steps below to create project in Google developer console for GA reporting API and to obtain “application name” and “security key JSON File”: -

#### Go to [https://console.developers.google.com/](https://console.developers.google.com/). Click on the dropdown on the left as shown in the image below and a popup will appear on your screen. <a href="#toc65169383" id="toc65169383"></a>

![](<../../.gitbook/assets/sync1 (1).jpg>)

#### Click on New Project <a href="#toc65169384" id="toc65169384"></a>

![](<../../.gitbook/assets/sync2 (1).jpg>)

#### Enter your project name and Location then click on create. <a href="#toc65169385" id="toc65169385"></a>

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

#### Click on Enable APIS and SERVICES <a href="#toc65169386" id="toc65169386"></a>

![](../../.gitbook/assets/sync4.jpg)

#### In the next window search for Google Analytics Reporting API <a href="#toc65169387" id="toc65169387"></a>

![](../../.gitbook/assets/sync5.jpg)

#### Click on Enable to enable the API <a href="#toc65169388" id="toc65169388"></a>

![](../../.gitbook/assets/sync6.jpg)

#### Similarly enable the below API's as well:- <a href="#toc65169389" id="toc65169389"></a>

* Google Analytics API&#x20;
* Google Analytics Data API (Used to access GA4 report Data) [https://developers.google.com/analytics/devguides/reporting/data/v1?hl=en\_US](https://developers.google.com/analytics/devguides/reporting/data/v1?hl=en\_US)

#### Click on Credentials from the left window then click on Create Credentials and choose service account. <a href="#toc65169389" id="toc65169389"></a>

![](../../.gitbook/assets/sync7.jpg)

#### In the next window, fill in your service account name and description then click on Create. An email will be automatically created as per your name. We need to add this email in google analytics. We will do it in the steps down below. Your service name will be your Application Name that you will enter in the configuration. <a href="#toc65169390" id="toc65169390"></a>

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

#### Click on continue without selecting a role. <a href="#toc65169391" id="toc65169391"></a>

![](../../.gitbook/assets/sync9.jpg)

#### Click Continue again without any selection <a href="#toc65169392" id="toc65169392"></a>

![](../../.gitbook/assets/sync10.jpg)

* Click on Create Key from the image above and select json your key file will be downloaded. **Place this key file in the VAR directory of your website**. Copy the exact name with extension “.json” and input it into **security Key** in the configuration.
* Login to your Google Analytics account. Go to **Admin > User Management**. Add the **email** we got in the steps above with “Read and Analyse” permissions.

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
