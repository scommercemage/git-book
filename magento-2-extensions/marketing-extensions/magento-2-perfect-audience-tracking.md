# Magento 2 Perfect Audience Tracking

### <mark style="color:blue;">Installation and User Guide for Magento 2 Perfect Audience Extension</mark>

**Table of Contents**

1. __[_Installation_ ](magento-2-perfect-audience-tracking.md#\_bookmark0)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. __[_Configuration Settings for Perfect Audience_ ](magento-2-perfect-audience-tracking.md#\_bookmark3)__
   * _General Settings_&#x20;
   * _Perfect Audience Tag_&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

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

### <mark style="color:blue;">Configuration Settings for Perfect Audience</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Perfect Audience**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Tracking Tag ID –** Enter tag Id only without .js.

![](../../.gitbook/assets/general\_perfectaudience.png)

#### <mark style="color:orange;">**Perfect Audience Tag**</mark>&#x20;

You can add perfect audience tracking tag from **Admin > Stores > Configuration > Scommerce Configuration > Perfect Audience > Tracking Tag ID.**

![](<../../.gitbook/assets/2 (34)>)

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
