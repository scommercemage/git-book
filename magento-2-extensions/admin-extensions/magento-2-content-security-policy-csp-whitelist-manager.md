# Magento 2 Content Security Policy (CSP) Whitelist Manager

### <mark style="color:blue;">Installation and User Guide for Magento 2 Content Security Policy (CSP) Whitelist Manager</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-content-security-policy-csp-whitelist-manager.md#bookmark0)
   * _Download Extension_
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_<mark style="color:blue;">Configuration Settings for Content Security Policy (CSP) Whitelist</mark>_](magento-2-content-security-policy-csp-whitelist-manager.md#bookmark3)
   * _General Settings_&#x20;
   * _Sources_
   * _Critical Security Overrides_
3. [_<mark style="color:blue;">Working of the extension</mark>_](magento-2-content-security-policy-csp-whitelist-manager.md#working-of-the-extension)

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Download Extension:**</mark> Once you have placed the order from our site then go to My Account section and click on My Downloadable Products and download the extension package.

![](../../.gitbook/assets/Download.png)

* <mark style="color:orange;">**Installation via app/code:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
composer require orhanerday/open-ai
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

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Sources</mark> <a href="#bookmark4" id="bookmark4"></a>

*   **Default Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for default-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>


*   **Base Uri**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for base-uri
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

    \

*   **Child Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for child-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>


* **Connect Src**
  * **Enabled-** Select “Yes” or “No” to enable or disable csp whitelist for connect-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* **Font Src**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for font-src
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

*   **Form Action**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for form-action
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>



* **Frame Ancestors**
  * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for frame-ancestors
  * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

*   **Frame Src**

    * **Enabled**- Select “Yes” or “No” to enable or disable csp whitelist for frame-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.

    <figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>


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

    <figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>


*   **Style Src**

    * **Enabled-** Select “Yes” or “No” to enable or disable csp whitelist for style-src
    * **Whitelist entries**- Please add URLs that you want to whitelist. By default, the type of entry added would be host. You can also delete this entry and add multiple entries.





<mark style="color:orange;">**Critical Security Overrides**</mark>

*   **Enable Unsafe Inline Script-**This setting permits the execution of unsafe inline scripts, which can be introduced by your developers / third party extensions / attackers. Make sure you assess these unsafe inline scripts before setting this to YES.

    * **Caution**: Enabling unsafe inline scripts is a temporary measure and should only be done under the guidance of your developer. You must ask your developers or third party extension providers to whitelist their inline scripts. This setting must NOT be left on 'YES' permanently, as it significantly increases the risk of security vulnerabilities, making your site an easy target for attackers. Always prioritise the security of your site and user data.



### <mark style="color:blue;">**Working of the extension**</mark>

<mark style="color:orange;">**Steps to check whether the extension is working or not**</mark>

*   Check the errors present in the frontend's console.

    <figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>
*   Check the source of these errors.

    <figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>
*   Check the URL present in these errors.

    <figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>
*   In the backend, add the URL to the source to which that error belongs to.

    <figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>
*   You would no longer see the error on the frontend

    <figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

\




