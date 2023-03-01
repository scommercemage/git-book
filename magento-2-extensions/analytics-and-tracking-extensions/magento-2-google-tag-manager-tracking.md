# Magento 2 Google Tag Manager Tracking

### <mark style="color:blue;">Magento Google Tag Manager Tracking - Installation/Set-up Guide</mark>

### <mark style="color:blue;">Installation</mark>

* <mark style="color:orange;">**Upload Package:**</mark>** ** Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Install extension:**</mark>** ** After the successful upload of the package you have to run the commands on Magento2 root directory via SSH

```
php bin/magento setup:upgrade 
php bin/magento setup:upgrade
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Clear Caches:**</mark>** ** This can be done from the admin console by navigating to the cache management page (System->Cache Management), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change. Logout and login back in Admin.
* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% content-ref url="../installation-via-composer.md" %}
[installation-via-composer.md](../installation-via-composer.md)
{% endcontent-ref %}

### <mark style="color:orange;">**Configuration settings for Google Tag Manager Tracking:**</mark>

Go to **Admin->System->Configuration->Scommerce Configuration->Google Tag Manager Tracking->General**

1. **Enable:** Set yes to enable the module.
2. **License Key:** Enter the License key provided by Scommerce Mage.
3. **Account Id:** Enter your Google Tag Manager Account Id.

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-google-tag-manager-tracking-m2.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
