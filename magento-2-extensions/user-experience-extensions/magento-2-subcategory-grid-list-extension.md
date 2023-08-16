# Magento 2 Subcategory Grid/List Extension

### <mark style="color:blue;">Installation and User Guide for Magento 2 Subcategory Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-subcategory-grid-list-extension.md#\_bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. [_Configuration Settings for Subcategory Extension_ ](magento-2-subcategory-grid-list-extension.md#\_bookmark3)
   * _General Settings_&#x20;
   * _Subcategories Widget_&#x20;
   * _Display Mode Selection Drop-down “Subcategories Only”_&#x20;
   * _Sub-categories Settings Dropdown_&#x20;
3. [_Front-end Screenshots_ ](magento-2-subcategory-grid-list-extension.md#\_bookmark8)
   * _Subcategories Grid View on the Front- end_&#x20;
   * _Subcategories List View on the Front- end_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

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

### <mark style="color:blue;">Configuration Settings for Subcategory Extension</mark> <a href="#_bookmark3" id="_bookmark3"></a>

#### Go to Admin > Stores > Configuration > Scommerce Configuration > SubCategory

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Subcategories Background Color –** Please select the Subcategories background colour.
* **Thumbnail Placeholder –** Please choose the file of Thumbnail placeholder
* **Thumbnail width –** Please add the Thumbnail width.
* **Thumbnail height –** Please add the Thumbnail height.

![](../../.gitbook/assets/subcategory\_general.jpg)

#### <mark style="color:orange;">Subcategories Widget</mark> <a href="#_bookmark5" id="_bookmark5"></a>

Subcategories widget will allow you to display subcategories in a Grid/list view on any page. Navigate to **Content > Pages,** edit the page that where you want to display the subcategories. Go into Content and then simply click on insert widget and you will have options such as widget type where you have to select the widget named “Subcategories List” then select the category and the number of columns you want to display the subcategories in. Then Lastly click on insert widget.

![](<../../.gitbook/assets/7 (59)>)

#### <mark style="color:orange;">Display Mode Selection Drop-down “Subcategories Only”</mark> <a href="#_bookmark6" id="_bookmark6"></a>

Go to any of the categories page where you want to display subcategories on by navigating to **Catalog > Categories**. Next go to display settings where you can select the display mode as “subcategories only” so that the page can display subcategories instead of products

![](<../../.gitbook/assets/8 (56)>)

#### <mark style="color:orange;">Sub-categories Settings Dropdown</mark> <a href="#_bookmark7" id="_bookmark7"></a>

Go to any of the categories pages where you can select the settings by going into

**Sub-categories settings** dropdown. You can change the following settings: -

* **Thumbnail Category Image –** Here you can upload a thumbnail image for the category.
* **Sub-category Short Description –** You can add a short description here.
* **Number of columns –** Select the number of columns you want to display your subcategories in.

![](<../../.gitbook/assets/9 (26)>)

### <mark style="color:blue;">Front-end Screenshots</mark> <a href="#_bookmark8" id="_bookmark8"></a>

#### <mark style="color:orange;">Subcategories Grid View on the Front- end</mark> <a href="#_bookmark9" id="_bookmark9"></a>

After successfully enabling subcategories you can see them listed in a Grid view on the frontend. You can select the number of columns depending upon that the frontend will review the Grid view. To select the columns Navigate to **Catalog > Categories** and then select the category. Scroll down to **Sub-Categories Settings**. Here you will have the option to upload the thumbnail image, short description and number of columns. Please refer to the image below. Each of the subcategories will be listed with a description, background and image as defined by you.

![](../../.gitbook/assets/subcategory\_front1.jpg)

#### <mark style="color:orange;">Subcategories List View on the Front- end</mark> <a href="#_bookmark10" id="_bookmark10"></a>

Navigate to **Catalog > Categories**, select the category, and then scroll down to **Sub-Categories settings.** You can select the number of columns here. Similarly display the subcategories in a list view by selecting the number of columns as “1”. See the image below for reference.

![](<../../.gitbook/assets/11 (9)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-subcategory-grid.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
