# Automated Product Publish Date

### <mark style="color:blue;">Automated Product Publish Date - Installation/Set-up Guide</mark>

1. <mark style="color:orange;">**Disable Compilation Mode**</mark><mark style="color:orange;">:</mark> To check that this is disabled, go to System->Tools->Compilation. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
2. <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
3. <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (System->Cache Management), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change. Log out and login back in admin.
4. <mark style="color:orange;">**Admin Configuration:**</mark>** ** Go to Admin ->System->Configuration-> Scommerce Configuration -> Publish Date-> General
   1. **Enable :** Enable / Disable Module
   2. **License key :** Enter License key provided by Scommerce Mage
   3. **Log Process:** If set to yes then you should be able debug queries running for enabling/disabling products as part of cron job. The debugging log gets created in var/log folder using the following format publish\_products\_YYYYMMDD\_HHMM.log.
5. <mark style="color:orange;">**Product Publish Date Set Up:**</mark>** ** Go to Admin->Catalog->Manage products
   1. Select the product you want to set publish date on.
   2. Go to General -> Publish Start Date – Date from which products will be available on site.
   3. Go to General -> Publish End Date –Date after which products will be unavailable on site.

You can either enter both the dates and any one of them.

If Start Date entered and End Date left blank then product will available forever after Start Date.

If End Date entered and Start Date left blank then product will be available straight and will be disabled after set End Date.

<mark style="color:orange;">**Please note: If you don’t see publish start date and end date attributes when creating or updating products then you need to assign them to your attribute set manually from Admin -> Catalog -> Attributes -> Manage Attributes Sets**</mark>

1. <mark style="color:orange;">**Bulk set publish date:**</mark>** ** Go to Admin->Catalog->Manage products
   1. Select the products you want to set publish date on.
   2. From actions drop-down choose update attributes and click submit button
   3. On the pop-up screen, select publish start date or end date or both
   4. Depending on the given dates after 5 minutes all the products will either be disabled or enabled on the given store or website and will be displayed or taken out from the website or store based on the publish start or end date given.

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-automated-product-publish-date.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
