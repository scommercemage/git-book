# Jquery Asynchronous Image Loader (JAIL)

### <mark style="color:blue;">Magento Jquery Asynchronous Image Loader Extension Installation/Set-up Guide</mark>

* <mark style="color:orange;">**Disable Compilation Mode**</mark><mark style="color:orange;">:</mark> To check that this is disabled, go to System->Tools->Compilation. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right**-**hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (System->Cache Management), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change. Log out and login back in Admin.
* <mark style="color:orange;">**Admin Configuration:**</mark> Go to Admin ->System->Configuration->Scommerce Configuration -> Lazy Load Images -> General&#x20;
  * **Enable :** Enable / Disable Module
  * **License key :** Enter License key provided by Scommerce Mage

<mark style="color:orange;">**Theme changes:**</mark> If you are not using your custom theme then this module should work out of the box. But if you are using custom theme then follow the following steps -:

* **Check if you have the following file in your custom theme folder**&#x20;
  * **/app/design/frontend/default/\<custom>/template/cate gory /list.phtml**

**If the above file does exist in your custom theme then copy the differences from the following file -:**

* **/app/design/frontend/default/base/template/category/list.phtml**
* <mark style="color:orange;">**Clear Caches:**</mark> Once you are done with everything above, clear the cache to get the changes reflect on your website.

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-lazy-image-loader-jail.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
