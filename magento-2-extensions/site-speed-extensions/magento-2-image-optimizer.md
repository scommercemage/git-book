# Magento 2 Image Optimizer

### <mark style="color:blue;">Installation and User Guide for Magento 2 Image Optimizer</mark>&#x20;

**Table of Contents**

1. [_Installation_ ](magento-2-image-optimizer.md#\_toc\_250004)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. __[_Configuration Settings for Optimiser Base_ ](magento-2-image-optimizer.md#\_toc\_250003)__
   * _General Settings_&#x20;
3. __[_Configuration Settings for Image Optimiser_ ](magento-2-image-optimizer.md#\_toc\_250001)__
   * _General Settings_&#x20;
   * _Compress/Optimize Product Images_&#x20;
   * _Compress/Optimize Category Images_&#x20;
   * _Compress/Optimize CMS Images_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_toc_250004" id="_toc_250004"></a>

* <mark style="color:orange;">**Installation via app/code:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% content-ref url="../installation-via-composer.md" %}
[installation-via-composer.md](../installation-via-composer.md)
{% endcontent-ref %}

### <mark style="color:blue;">Configuration Settings for Optimiser Base</mark> <a href="#_toc_250003" id="_toc_250003"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Optimiser Base**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250002" id="_toc_250002"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)

![](../../.gitbook/assets/config\_speed.png)

### <mark style="color:blue;">Configuration Settings for Image Optimiser</mark> <a href="#_toc_250001" id="_toc_250001"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Image Optimiser**

#### <mark style="color:orange;">General Settings</mark> <a href="#_toc_250000" id="_toc_250000"></a>

* **Enabled -** Select “Yes” or **“**No**”** to enable or disable the module.
* **Compress Images while uploading (All pages, CMS, Category and Product):** Select available options to enable compression for new images uploaded via Magento admin. We recommend this to be enabled because all the new things will be compressed straight away.
* **Number of images to processed –** Define how many number of images you want to process when the cron job runs. Please note this number should be reasonable especially when you have multiple stores and many additional product images.
* **Include folders –** Please select list of folders you want to include for compressing the image.
* **Compress Cached Product Images (Yes/No) –** Select “Yes” to compress cached product images generated by Magento. We could recommend to leave this setting turned off especially when you clear your cached images frequently and you have more than 5 additional images on the product page.
* **Image Compression Provider –** Please select image compression provider.  **Provider API URL: Provider API URL `smush it –`** [**`http://api.resmush.it/ws.php?img=`**](http://api.resmush.it/ws.php?img) **`imageoptim –`** [**`https://im2.io/{ {username} }/full/`**](https://im2.io/%7B%20%7Busername%7D%20%7D/full/) **`kraken.io –`** [**`https://api.kraken.io./v1/url`**](https://api.kraken.io/v1)``
* **API Key –** Please enter API Key (if provider is kraken.io).
* **API Secret Key –** This will be required for certain providers like kraken.io
* **Exclude folders –** Please enter the list of folders you want to exclude from media directory (comma separated) for example foldername1, foldername2, /foldername /subfolder1, foldername/subfolder2
* **Backup Images (Yes/No) –** Select “Yes” to enable this feature to backup original images before compressing original file.
* **Debugging (Yes/No) –** Select “Yes” to enable debugging. This will write logs in var – log – imageoptimize.log
* **Image Optimiser Schedule –** Please define the Cron frequency to optimize images.

![](../../.gitbook/assets/image\_general1.png)

![](../../.gitbook/assets/image\_general2.png)

* <mark style="color:orange;">**Compress/Optimize Product Images -**</mark>** ** You can compress product images by enabling module from **Admin > Stores > Configuration > Scommerce Configuration > Image Optimiser > Enabled - "Yes" > Compress Images while uploading -** Select **"Product ".**

![](<../../.gitbook/assets/8 (15)>)

* <mark style="color:orange;">**Compress/Optimize Category Images -**</mark>** ** You can compress category images by enabling module from **Admin > Stores > Configuration > Scommerce Configuration > Image Optimiser > Enabled - "Yes" > Compress Images while uploading -** Select **"Category ".**

![](<../../.gitbook/assets/9 (22)>)

* <mark style="color:orange;">**Compress/Optimize CMS Images -**</mark>** ** You can compress CMS images by enabling module from **Admin > Stores > Configuration > Scommerce Configuration > Image Optimiser > Enabled - "Yes" > Compress Images while uploading -** Select **"CMS ".**

![](<../../.gitbook/assets/10 (29)>)

If you have a question related to this extension please check out our  [**FAQ section**](https://www.scommerce-mage.com/magento-2-image-optimizer.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**