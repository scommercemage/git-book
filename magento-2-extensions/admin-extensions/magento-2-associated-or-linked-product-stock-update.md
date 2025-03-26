# Magento 2 Associated or Linked Product Stock Update

### <mark style="color:blue;">Installation and User Guide for Magento 2 Associated or Linked Product Stock Update Extension</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-associated-or-linked-product-stock-update.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_&#x20;
2. [_Configuration Settings for Associated Product_ ](magento-2-associated-or-linked-product-stock-update.md#bookmark3)
   * _General Settings_&#x20;
   * _Product Association at Product Level_&#x20;
   * _Product Association for Simple Product_&#x20;
   * _Product Association for Configurable/Child Product_&#x20;
   * _Product Grid at Product Level_&#x20;
   * _Associated or Linked Product Stock Update_&#x20;
3. [_Fix Product Associations_](magento-2-associated-or-linked-product-stock-update.md#bookmark10)
4. [_Import / Export_ ](magento-2-associated-or-linked-product-stock-update.md#bookmark10-1)
   * _Import_&#x20;
   * _Export_&#x20;

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

### <mark style="color:blue;">Configuration Settings for Associated Product</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Associated Product**

### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).
* **Optimise Stock save** - Select "Yes" or "No". If set to "Yes" then it will optimise stock save for better performance on products with large amounts of associated products.

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* <mark style="color:orange;">**Product Association at Product Level –**</mark> You can associate products from **Admin > Catalog > Products > Select Product > Product Association > Click “AddProduct”.**

### <mark style="color:blue;">Product Association for Simple Product</mark> <a href="#bookmark6" id="bookmark6"></a>

![](<../../.gitbook/assets/2 (16)>)

### <mark style="color:blue;">Product Association for Configurable/Child Product</mark> <a href="#bookmark7" id="bookmark7"></a>

![](<../../.gitbook/assets/3 (16)>)

* <mark style="color:orange;">**Product Grid at Product Level –**</mark> You can add products from **Admin > Catalog> Products > Select Product > Product Association >** Click **“Add Product” > Product Grid > Select Products > Click “Add Selected Products”.**

![](<../../.gitbook/assets/4 (4)>)

* <mark style="color:orange;">**Associated or Linked Product Stock Update -**</mark> Associated product stock/quantity will be updated based on the main product, which you can see in the below screen grab. It supports multiple linking where one product can have multiple associated products.

![](<../../.gitbook/assets/5 (59)>)

### <mark style="color:blue;">Fix Product Associations</mark> <a href="#bookmark10" id="bookmark10"></a>

Product associations can be fixed to make sure the following criterias are met:-

* Same product is not associated with itself
* One product is associated with only 1 parent

To fix product associations run the command given below:-

```
php bin/magento scommerce:associatedproducts:fixassociations -f
```

### <mark style="color:blue;">Import / Export</mark> <a href="#bookmark10" id="bookmark10"></a>

#### <mark style="color:orange;">Import</mark> <a href="#bookmark11" id="bookmark11"></a>

To import associated products go **system > Data transfer > Import**. Then select product association from the drop down list. You will see the importing menu opening on your screen as shown in the image below. Select the import file and add import behavior settings as per your preferences. Lastly click on check data button on the right corner of your screen.

![](<../../.gitbook/assets/6 (49)>)

![](<../../.gitbook/assets/7 (36)>)

* <mark style="color:orange;">**Export –**</mark> Go to **System > Data Transfer > Export**. Select product associated in the entity type dropdown list. You should see the export menu popup on your screen as shown in the image below: -

![](<../../.gitbook/assets/8 (55)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-associated-or-linked-product-stock-update.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
