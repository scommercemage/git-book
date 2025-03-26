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
   * _Add Cloud Console Email to Google Analytics 4_
4. [Order Tracking INFO](magento-1-google-analytics-synchronization-extension.md#toc65169394-1)
5. [Verify Synced Transactions](magento-1-google-analytics-synchronization-extension.md#toc65169394-2)
   * GA Sync Logs
   * Google Analytics 4 Real Time Reports
6. [_Run GA Synch Manually_ ](magento-1-google-analytics-synchronization-extension.md#toc65169394-3)

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark> To check that this is disabled, go to **System>Tools > Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Google Analytics Synchronization</mark> <a href="#toc65169380" id="toc65169380"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Google Analytics Synchronization**

#### <mark style="color:orange;">**General Settings**</mark> <a href="#toc65169381" id="toc65169381"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Application Name –** It is the project name or the application name that you get from Google console. ( https://console.developers.google.com/ )([ClICK HERE FOR MORE INFO](magento-1-google-analytics-synchronization-extension.md#toc65169382))
* **Security key (JSON) –** Security key JSON file can be obtained from Google Console under account credentials. ([ClICK HERE FOR MORE INFO](magento-1-google-analytics-synchronization-extension.md#toc65169382))
* **Exclude order statuses –** You can choose to exclude certain order statues from sync. These orders won’t be synced with Google Analytics.
* **Send Base Data –** Select whether you want to send base order data or store order data.
* **Brand Attribute –** Select a brand attribute to send with brand names

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

* **Brand Text box –** Input brand name to send to Google
* **Default Landing Page -** This setting allows you to set default landing page value which shows in Google Analytics in case landing page is not available to sent as part of missing transaction.
* **Cron Schedule –** Schedule specific cron time to run the sync automatically.
* **Debugging –** When set Yes, it will generate logs in var/log/ga\_sync.log file otherwise log file will not be generated.
* **Test Mode-** This setting allows you to check missing transactions before we send the transactions to GA. It helps in validating the data before it gets posted to Google Analytics
* **API Secret –** Enter the API secret key here. API secret key can be created by going into GA4>Admin>Data Streams>Select website>Measurement Protocol API Secrets>Create enter the name and click on create to get the key.
*   **Skip Order days –**&#x20;

    Number of Days to Skip Before Sending to GA4:

    * Numeric value starting from 0
    * Set delay for sending transactions to GA4 to at least 2 days to avoid duplicates (GA4 may take up to 48 hours to process transactions)
    * A value less than 2 days risks sending duplicates, as GA4 takes 24-48 hours to populate transactions in your reports
      * If set to 0: Extension compares today's transactions with GA4 and syncs those transactions (may result in duplicates)
      * If set to 1: Extension compares yesterday's transactions with GA4 and syncs those transactions (may result in duplicates)
    * Recommended value is 2 or greater to ensure sufficient time for GA4 to process and populate transactions before comparison and syncing
* **Measurement ID –** Enter the measurement ID of your GA4 property. Ga4 measurement ID can be extracted from **GA4>Admin>Data Streams>Select website and it is available in the top right corner.**
* **Property ID –** Enter the property ID of GA4. **GA4>Admin>Property Settings>Property ID**&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Create Project in Google Developer Console for GA Reporting API</mark> <a href="#toc65169382" id="toc65169382"></a>

Please follow the steps below to create project in Google developer console for GA reporting API and to obtain “application name” and “security key JSON File”: -

* #### Go to [https://console.developers.google.com/](https://console.developers.google.com/). Click on the dropdown on the left as shown in the image below and a popup will appear on your screen. <a href="#toc65169383" id="toc65169383"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/Screenshot 2024-04-18 143824.png" alt=""><figcaption></figcaption></figure></div>

* #### Click on New Project <a href="#toc65169384" id="toc65169384"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Enter your project name and Location then click on create. <a href="#toc65169385" id="toc65169385"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Click on Enable APIS and SERVICES <a href="#toc65169386" id="toc65169386"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### In the next window search for Google Analytics Data API <a href="#toc65169387" id="toc65169387"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (16) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Click on Enable to enable the API <a href="#toc65169388" id="toc65169388"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (15) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Similarly enable the "Google Analytics Reporting API" as well. <a href="#toc65169389" id="toc65169389"></a>
* #### Click on Credentials from the left window then click on Create Credentials and choose service account. <a href="#toc65169389" id="toc65169389"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/Screenshot 2024-04-18 145949 (1).png" alt=""><figcaption></figcaption></figure></div>

* #### In the next window, fill in your service account name and description then click on Create. An email will be automatically created as per your name. We need to add this email in google analytics. We will do it in the steps down below. Your service name will be your Application Name that you will enter in the configuration. <a href="#toc65169390" id="toc65169390"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (17) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Click on continue without selecting a role. <a href="#toc65169391" id="toc65169391"></a>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (18) (1).png" alt=""><figcaption></figcaption></figure></div>

* #### Click Continue again without any selection <a href="#toc65169392" id="toc65169392"></a>
* Click on Create Key from the image below and select json your key file will be downloaded. **Place this key file in the VAR directory of your website**. Copy the exact name with extension “.json” and input it into **security Key** in the configuration.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (19) (1).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Add Cloud Console Email to Google Analytics 4</mark> <a href="#toc65169394" id="toc65169394"></a>

In the earlier step we created a service account ID which is also the service account email. Alternatively, you can go to the "API & Services" section from the left menu and find your service account email there as shown in screengrab below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Now In order for this account to access your GA4 property we are required to add this service email to GA4. To do that copy this email address and go to your GA4 property. Go to admin and click on Property access management:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Click on plus sign to add new email:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Next add the email and set the permissions to Editor and you are done.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (4) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Order Tracking INFO</mark> <a href="#toc65169394" id="toc65169394"></a>

The order tracking info is captured against each order which is later used to sync the transactions to GA4 attributing them to correct sessions and dates to improve report accuracy. The order tracking info can be viewed by going into Admin>Sales>Order>Edit any order. Please refer to the screengrab below.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (5) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

**Note:-** The Order tracking info will only present in the orders that are placed after the module is installed and enabled. It won't be present for historical orders.

### <mark style="color:blue;">Verify Synced Transactions</mark> <a href="#toc65169394" id="toc65169394"></a>

The synced transactions can be verified in two ways. Either checking the GA Sync logs or by checking the Real time reports in GA4 (as it takes 24 to48 hrs for GA4 to attribute data to reports realtime is the quickest way to verify).

#### <mark style="color:orange;">GA Sync Logs</mark>

The GA Sync logs can be viewed by going into your server>Magento installation directory>Var>log>ga\_sync.log.

<figure><img src="../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

This file contains details of each synced transaction alongwith the order data that was sent, please refer to the image below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Google Analytics 4 Real Time Reports</mark>

Go to your Google Analytics 4 Property then from left menu click on reports:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

Next, select realtime from the left menu  and under the event name column you can find the purchase event by clicking on that you can verify the transaction ID that was sent through the sync module.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Google Analytics 4 Custom Reports</mark>

You can create a transaction report in GA4 using custom reports to verify the transactions received. For more information, please check https://www.scommerce-mage.com/blog/how-to-create-transactions-report-in-google-analytics-4-ga4.html

### <mark style="color:blue;">Run GA Synch Manually</mark> <a href="#toc65169394" id="toc65169394"></a>

You can run the synch manually by utilizing the built in frotnend controller to the run the sync. The controller is as follows:-

```
scommerce_gatransactionsync/index/sync
```

Visit the frontend page pointing to the controller in the URL, please refer to below link as an example:-&#x20;

{% embed url="https://demo.scommerce-mage.co.uk/scommerce_gatransactionsync/index/sync" %}

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
