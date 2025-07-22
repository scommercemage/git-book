# Magento 2 Content Security Policy (CSP) Whitelist Manager

<mark style="color:blue;">Installation and User Guide for Magento 2 Content Security Policy (CSP) Whitelist Manager</mark>

**Table of Contents**

1. [_Installation_](magento-2-content-security-policy-csp-whitelist-manager.md#bookmark0)
   * _Download Extension_
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Content Security Policy (CSP) Whitelist_](magento-2-content-security-policy-csp-whitelist-manager.md#bookmark3)
   * _General Settings_&#x20;
   * _CSP Directives_
   * _Critical Security Overrides_
3. [_CSP Reports Grid_](magento-2-content-security-policy-csp-whitelist-manager.md#csp-reports-grid)
4. [_Working of the extension_](magento-2-content-security-policy-csp-whitelist-manager.md#working-of-the-extension)
   * _Steps to Check and Fix Console CSP Errors through CSP Grid_
   * _Steps to Check and Fix Console CSP Errors_
5. [_Fixing Inline Script and Inline Style Content Security Policy Issues_](magento-2-content-security-policy-csp-whitelist-manager.md#fixing-inline-script-and-inline-style-content-security-policy-issues)
   * _Inline Style Error Example_
   * _Inline Script Error Example_

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Download Extension:**</mark> Once you have placed the order from our site then go to My Account section and click on My Downloadable Products and download the extension package.

![](../../.gitbook/assets/Download.png)

* <mark style="color:orange;">**Installation via app/code:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy en_GB en_US
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% content-ref url="../installation-via-composer.md" %}
[installation-via-composer.md](../installation-via-composer.md)
{% endcontent-ref %}

{% embed url="https://www.youtube.com/watch?v=sJ_Kj6n_mUo" %}

### <mark style="color:blue;">Configuration Settings for Content Security Policy (CSP) Whitelist</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > CSP Whitelist**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **IMPORTANT INFORMATION**- When adding or changing whitelist, ensure to include only those domains that are recognized and trustworthy. This precaution is crucial because unauthorized or compromised domains may contain malicious scripts.
* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Report Only Mode -** Set "Yes" to enable Report Only mode for CSP ( it will only report CSP vulnerabilities in the CSP reports grid and browser console. Make sure to add Report URL in Configuration>Security>CSP for the CSP grid to collect reports. Set "No" to enable Strict Mode ( it will prevent data from loading or code from getting executed to prevent vulnerabilities).
* **Report Collection Enabled:-** Set "Yes" to enable collecting CSP reports in the CSP grid, Set "No" these errors will only be available in the browser console
* **Report URL Configuration:-** Please add following URLs in _Security > CSP section_ of your Store config **Admin Default** - _https://BASE\_URL/scommercereporturi/report/admin **Storefront**_**&#x20;Default** - _https://BASE\_URL/scommercereporturi/report/storefront_

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">CSP Directives</mark> <a href="#bookmark4" id="bookmark4"></a>

*   **Default Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for default-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


*   **Base Uri**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for base-uri
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

    \

*   **Child Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for child-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>


* **Connect Src**
  * **Enabled-** Select “Yes” or “No” to enable or disable csp whitelist for connect-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (11) (1).png" alt=""><figcaption></figcaption></figure>

* **Font Src**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for font-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

*   **Form Action**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for form-action
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>



* **Frame Ancestors**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for frame-ancestors
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (6) (1) (1).png" alt=""><figcaption></figcaption></figure>

*   **Frame Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for frame-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (10) (1).png" alt=""><figcaption></figcaption></figure>


* **Img Src**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for img-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

* **Manifest Src**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for manifest-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

*   **Media Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for media-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>


*   **Object Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for object-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>


*   **Script Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for script-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.



<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure></div>

* **Style Src**
  * **Enabled-** Select “Yes” or “No” to enable or disable csp whitelist for style-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>



<mark style="color:orange;">**Critical Security Overrides**</mark>

*   **Enable Unsafe Inline Script-**&#x54;his setting permits the execution of unsafe inline scripts, which can be introduced by your developers / third party extensions / attackers. Make sure you assess these unsafe inline scripts before setting this to YES.

    <mark style="color:orange;">**Caution**</mark><mark style="color:orange;">: Enabling unsafe inline scripts is a temporary measure and should only be done under the guidance of your developer. You must ask your developers or third party extension providers to whitelist their inline scripts. This setting must NOT be left on 'YES' permanently, as it significantly increases the risk of security vulnerabilities, making your site an easy target for attackers. Always prioritise the security of your site and user data.</mark>



<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">**CSP Reports Grid**</mark>

The CSP Reports Grid collects and displays all the CSP errors on both frontend and backend. To enable report collection please make sure to add the following URLs in _Security > CSP section_ of your Store config:-

* **Admin Default** - _https://BASE\_URL/scommercereporturi/report/admin_&#x20;
* _**Storefront**_**&#x20;Default** - _https://BASE\_URL/scommercereporturi/report/storefront_

_For eg:-_

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (223).png" alt=""><figcaption></figcaption></figure></div>

To access the grid go to Admin>System>Scommerce CSP Records> CSP Report Only Grid

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure></div>

* **ID:-** Id of the record
* **Blocked URL:-** The URL reported in the CSP error
* **Report Type:-** Store Front (frontend) or Admin(backend), where the error was reported
* **Source URLs:-** The Source URL of the page where this error was reported
* **Policy violation:-** The CSP directive which was violated in this record.
* **Last report date:-** When was this error last reported.

### <mark style="color:blue;">**Working of the extension**</mark>

<mark style="color:orange;">**Steps to Check and Fix Console CSP Errors thorugh CSP Reports Grid**</mark>

Go to Admin>System>Scommerce CSP Records> CSP Report Only Grid, select the error records that you want to whitelist then from the Actions dropdown, select whitelist.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure></div>

Please clear caches as prompted:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure></div>

Once done all the selected entries will be whitelisted into their specific CSP directive and should be visible in the admin configuration.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (228).png" alt=""><figcaption></figcaption></figure></div>

<mark style="color:red;">**Note:-**</mark> _<mark style="color:red;">If you have already whitelisted the entries manually in the configuration then you can delete these records from the grid by selection the records that you want to delete and then click on Action dropdown and select delete.</mark>_

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure></div>

<mark style="color:orange;">**Steps to Check and Fix Console CSP Errors Manually**</mark>

* Check the errors present in the frontend's console.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure></div>

* Check the source of these errors.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure></div>

* Check the URL present in these errors.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure></div>

*   In the backend, add the URL to the source to which that error belongs to.

    <figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
* You would no longer see the error on the frontend

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">**Fixing Inline Script and Inline Style Content Security Policy Issues**</mark>

In this section, we will show you how to fix the inline script and style related console errors for Content Security Policy. Please check the image below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure></div>

* Identify the script or style tag that's causing the console error.
* Create SHA256 hash of contents of with the script or style tag and then use bas64 to encode this hash. It can be done all together :- [https://emn178.github.io/online-tools/sha256.html](https://emn178.github.io/online-tools/sha256.html)
* Alternatively you can generate the hash using PHP as shown below.

```
$whitelistHash = base64_encode(hash('sha256', $content, true));
```

* Next we add this hash to our module in the correct section i.e either style or script.

Let us look at examples to understand this process better:-

<mark style="color:orange;">**Inline Style Error Example**</mark>

* Suppose we identified the style thats causing the issue as follows:-

```
<style>
body {
background-color: #f3f3f3;
}
</style>
```

* Next we will go the site and create a SHA256 hash as well as the base64 encode of this hash of the contents of the style tag as shown in screengrab below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/Screenshot 2024-08-23 182227.png" alt=""><figcaption></figcaption></figure></div>

* Now copy this hash and go to **Stores>Configuration>Scommerce Configuration>CSP Whitelist** and scroll down to find the **Style Src** section. Add the hash here as shown in the image below:-

<figure><img src="../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Please make sure hash is selected in the type dropdown. This should resolve the console error.



<mark style="color:orange;">**Inline Script Error Example**</mark>

* The identified script tag causing the issue is as follows:-

```
<script>
console.log('Hello, world!');
</script>
```

* We will go the site([https://emn178.github.io/online-tools/sha256.html](https://emn178.github.io/online-tools/sha256.html)) and create a SHA256 hash as well as the base64 encode of this hash of the contents of the style tag as shown in screengrab below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/Screenshot 2024-08-23 183053.png" alt=""><figcaption></figcaption></figure></div>

* Now copy this hash and go to **Stores>Configuration>Scommerce Configuration>CSP Whitelist** and scroll down to find the **Script Src** section. Add the hash here as shown in the image below:-

<figure><img src="../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

* Please make sure hash is selected in the type dropdown. This should resolve the console error.



If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
