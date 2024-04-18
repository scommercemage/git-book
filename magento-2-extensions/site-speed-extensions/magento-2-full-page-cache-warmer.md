# Magento 2 Full Page Cache Warmer

### <mark style="color:blue;">Installation and User Guide for Magento 2 Full Page Cache Warmer Extension</mark>

**Table Of Contents**

1. [_Installation_ ](magento-2-full-page-cache-warmer.md#\_toc\_250008)
   * _Installation via app/code_
   * _Installation via Composer_&#x20;
2. [_Configuration Settings for Optimiser Base_ ](magento-2-full-page-cache-warmer.md#\_toc\_250007)
   * _General Settings_&#x20;
3. [_Configuration Settings for Full Page Cache Warmer_ ](magento-2-full-page-cache-warmer.md#\_toc\_250005)
   * _General Settings_&#x20;
   * _Cron Settings_&#x20;
4. [_Cache Warmer Grid_ ](magento-2-full-page-cache-warmer.md#\_toc\_250002)
   * _Regenerate_&#x20;
5. [_Console Commands_ ](magento-2-full-page-cache-warmer.md#\_toc\_250001)
   * _Category Page_&#x20;
   * _Product Page_&#x20;
   * _CMS Page_&#x20;
6. [_Front-end Site View_ ](magento-2-full-page-cache-warmer.md#\_toc\_250000)
   * _Cache Hit for the Category Page After the Execution of Category Page Command_&#x20;
   * _Cache Miss for the Category Page_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#toc_250008" id="toc_250008"></a>

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

### <mark style="color:blue;">Configuration Settings for Optimiser Base</mark> <a href="#toc_250007" id="toc_250007"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Optimiser Base**

#### <mark style="color:orange;">General Settings</mark> <a href="#toc_250006" id="toc_250006"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).

![](../../.gitbook/assets/general\_fullpage.png)

### <mark style="color:blue;">Configuration Settings for Full Page Cache Warmer</mark> <a href="#toc_250005" id="toc_250005"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Cache Warmer**

#### <mark style="color:orange;">General Settings</mark> <a href="#toc_250004" id="toc_250004"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **Regenerate cache after page update -** Please select "Yes" or "No" to regenerate cache for updated page.
* **Select Pages -** Please select the page(s) from the multi-select option . This will regenerate the cache selected page(s) on page update.
* **Can Regenerate Cache Manually -** Please select " Yes" or "No". If set to "Yes" then you can regenerate cache manually from cache warmer grid.
* **Generate Log -** Select "Yes" to generate the log.

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

* **Generation order -** Select which page will be generated first by adding the generation order alognside the page type. 1 is the highest priority.
* **Allow bestsellers products to be cached first -** Select "Yes" to give best seller products the highest priority in cache generation.
* **Bestseller Frequency -** Choose the range of bestleer products monthly/yearly. Based on your selection these products will be cached.
* **Website priority -** In multi website structures change the website in order to prioritize which will be cached first. 1 is highest priority.

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Cron Settings</mark> <a href="#toc_250003" id="toc_250003"></a>

* **Cache Cron Schedule -** Schedule cron job to regenerate the cache for all non cached page(s).
* **Number of Concurrent Regeneration request -** Please define the number of concurrent request.

<figure><img src="../../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Cache Warmer Grid</mark> <a href="#toc_250002" id="toc_250002"></a>

When you enable the module and set **General Settings > Can Regenerate Cache Manually >** to **"Yes"** then it adds an additional option "Regenerate" under the "**Actions > Select**" drop-down at **Admin > System > Cache Warmer > Actions.** This grid will have Id, Reference Id, Processed Time, Request Path, Page URL, Last Cache - (Date, Time ), Status - (Cached/Un-cached), Page Type - (Home, Product, Category, CMS), Store View, and Action- (Regenerate, Delete).

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

* <mark style="color:orange;">**Regenerate -**</mark> It regenerates cache manually for Category/Product/CMS page(s). By clicking "Regenerate" action you can regenerate cache manually for a specific URL.

<figure><img src="../../.gitbook/assets/4324324.png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Console Commands</mark> <a href="#toc_250001" id="toc_250001"></a>

You can regenerate cache for Product/Category/CMS page(s) by running the following console commands:-

* <mark style="color:orange;">**Category Page -**</mark> To regenerate cache for the category page, execute the below command.

&#x20;**`scommerce:cachewarmer:category`**

![](<../../.gitbook/assets/6 (18)>)

* <mark style="color:orange;">**Product Page -**</mark> To regenerate cache for the product page(s), execute the below command.

&#x20;**`scommerce:cachewarmer:product`**

![](<../../.gitbook/assets/7 (51)>)

* <mark style="color:orange;">**CMS Page -**</mark> To regenerate cache for CMS page, run the below command.

&#x20;**`scommerce:cachewarmer:cmspage`**

![](<../../.gitbook/assets/8 (49)>)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#toc_250000" id="toc_250000"></a>

* <mark style="color:orange;">**Cache Hit for the Category Page After the Execution of Category Page Command -**</mark> When you execute the command for category page then it regenerates the cache and on the front-end you check the status "Hit" or "Miss" using browser tool (Inspect element) at **Network > Select Page URL > Header > X- Magento-Cache-Debug : HIT**

![](<../../.gitbook/assets/9 (19)>)

* <mark style="color:orange;">**Cache Miss for the Category Page -**</mark> Flush the cache by executing the command, **c:f** and then check cache using browser tool at, **Network > Select Page URL > Header > X-Magento-Cache-Debug : MISS**

![](<../../.gitbook/assets/10 (34)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-full-page-cache-warmer.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
