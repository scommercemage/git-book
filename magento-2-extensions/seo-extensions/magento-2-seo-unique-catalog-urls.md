# Magento 2 SEO Unique Catalog URLs

### <mark style="color:blue;">Installation and User Guide for Magento 2 SEO Unique Catalog URLs</mark>&#x20;

**Table of Contents**

1. [_Installation_ ](magento-2-seo-unique-catalog-urls.md#toc\_250008)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for SEO Base_](magento-2-seo-unique-catalog-urls.md#toc\_250007)&#x20;
   * _General Settings_
3. [_Configuration settings for Catalog URL_ ](magento-2-seo-unique-catalog-urls.md#toc\_250027)
   * _General Settings_&#x20;
   * _Configuration Path to Set Up Primary Category_&#x20;
   * _Primary Category settings for Category_&#x20;
   * _Run the script to setup primary category of one or all products together_&#x20;
4. [_Set Primary Categories_](magento-2-seo-unique-catalog-urls.md#set-primary-categories)
5. [_Front-end Site View_ ](magento-2-seo-unique-catalog-urls.md#toc\_250024)
   * _Product Page Unique URL_&#x20;
   * _Search Page / Category Page Unique Catalog Product URL_&#x20;

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

### <mark style="color:blue;">Configuration Settings for SEO Base</mark> <a href="#toc_250007" id="toc_250007"></a>

Go to _Admin > Stores > Configuration > Scommerce Configuration > SEO Base_

#### <mark style="color:orange;">General Settings</mark> <a href="#toc_250006" id="toc_250006"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).

![](../../.gitbook/assets/config\_seo.png)

### <mark style="color:blue;">Configuration Settings for Catalog URL</mark> <a href="#toc_250027" id="toc_250027"></a>

Go to _Admin > Stores > Configuration > Scommerce Configuration > Catalog URL_

#### <mark style="color:orange;">General Settings</mark> <a href="#toc_250026" id="toc_250026"></a>

* **Enabled -** Select “Yes” or **“**No**”** to enable or disable the module.
* **Exclude Root Categories –** Exclude some root categories to appear as primary category dropdown against products.

![](../../.gitbook/assets/general\_catalog.png)

### <mark style="color:blue;">Configuration Path to Set Up Primary Category</mark> <a href="#toc_250025" id="toc_250025"></a>

Go to _Admin > Catalog > Select Product > Search Engine Optimization > Primary Category_ . The drop down will show all the categories selected for the product from where you can select the primary category of the product.

![](<../../.gitbook/assets/13 (2)>)

### <mark style="color:blue;">Primary Category settings for Category</mark> <a href="#toc_250002" id="toc_250002"></a>

Go to _Admin > Catalog > Categories > Select Category > Primary Category Settings._ The drop down will show two primary category settings for the selected category: -

* <mark style="color:orange;">**Exclude from Primary Category (Yes/No) -**</mark> Select Yes/No whether you want this category to excluded from the primary category or not.
* <mark style="color:orange;">**Exclude Root Categories –**</mark> Set the priority for the category, the highest priority will be selected as the primary category.

![](<../../.gitbook/assets/4 (77)>)

### <mark style="color:blue;">Run the script to setup primary category of one or all products together</mark> <a href="#toc_250001" id="toc_250001"></a>

We have included a PHP script that can be utilized to set primary category for one or all products together. Simply run the script in the url and the primary categories will get updated for the set products.&#x20;

* <mark style="color:orange;">**For one product –**</mark> Run the script given and refer to the image below to update the primary category of a single product.

`{{Website_URL}}/SetPrimaryCategoryM2.php?deleteSku s=MH01`

![](<../../.gitbook/assets/5 (3)>)

* <mark style="color:orange;">**For all Products –**</mark> Run the script given and refer to the image below to update the primary category of all products.

`{{Website_URL}}/SetPrimaryCategoryM2.php?deleteSkus=all`

![](<../../.gitbook/assets/6 (29)>)

If the script doesen't work in the URL then make sure to place the script inside PUB directory and change line number 6 as follows:-&#x20;

```
require realpath(__DIR__) . '/../app/bootstrap.php';
```

Once updated, please run the script again.

### <mark style="color:blue;">Set Primary Categories</mark>

You can use a script provided with the extension to automatically add primary categories for products. Admin can exclude certain categories from primary category and also prioritise one category over the other to be picked as the primary category.

Go to Admin>Catalog>Categories select a category then scroll down to find the option "Primary Category Settings". Here click on "Exclude From Primary Category" to exclude this category from primary category or enter the priority 0 being the highes. The highest priority category will be picked first for the primary category.

![](<../../.gitbook/assets/1 (3).png>)

_<mark style="color:red;">**N.B -**</mark>_ R_<mark style="color:red;">un the script provided in the extension folder at the path Data/SetPrimaryCategoryM2.php from ssh</mark>_

### <mark style="color:blue;">Front-end Site View</mark> <a href="#toc_250024" id="toc_250024"></a>

* <mark style="color:orange;">**Product Page Unique URL -**</mark> You can assign primary category to any product from _Admin > Catalog > Select Product > Search Engine Optimization > Primary Category._ In the below image you can see the assigned category of product Rival Field Messenger is "Gear->Bags"**.**

![](<../../.gitbook/assets/14 (23)>)

### &#x20;<a href="#toc_250023" id="toc_250023"></a>

* <mark style="color:orange;">**Search Page / Category Page Unique Catalog Product URL –**</mark> We have assigned “**Strive Shoulder Pack**” product to “**Gear**” Category and the URL stays the same when we access the product from the search or category page

![](<../../.gitbook/assets/8 (19)>)

If you have a question related to this extension please check out our [**FAQ section**](https://www.scommerce-mage.com/magento-2-seo-unique-product-url.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
