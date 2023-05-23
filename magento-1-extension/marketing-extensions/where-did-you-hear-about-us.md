# Where Did You Hear About Us?

### <mark style="color:blue;">Where did you hear about us? Extension - Installation/Set-up Guide</mark>

* <mark style="color:orange;">**Disable Compilation Mode**</mark><mark style="color:orange;">:</mark> To check that this is disabled, go to **Admin -> System -> Tools ->Compilation**. If the compiler status is ‘**Disabled**’, you are ready to go. If not, simply click the ‘**Disable**’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**Admin -> System->Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.
* <mark style="color:orange;">**Module Admin Configuration to set up:**</mark>&#x20;

**Step 1:** Go to **Admin->System- >Configuration -> Customers –> Customer Configurations ->Where did you hear about u**

* **License Key:** Enter the licence key received in your order confirmation email.
* **Dropdown Options:** Add **WDYHAU** options for customers and administrators to choose during checkout and creating phone order via admin respectively. They should be semicolon (;) separated values for example **Google;Facebook;Twitter;Word Of Mouth;Friend or Family;Other**

**Step 2:** Go to **Admin->System->Configuration -> General –> Design -> Admin Theme**

* **Admin Theme Name:** Enter **scommerce** as the admin theme name.

<mark style="color:orange;">**Please note:**</mark> Step 2 is only required when you don’t have any admin custom theme installed. Make sure for your admin custom theme you follow theme changes mentioned below in admin section.

* **Generate Report:** Once you have **WDYHAU** data with the orders, you can generate the report from **admin -> reports -> Get WDYHAU CSV**
* **Theme changes:** If you are not using your custom theme then this module should work out of the box. But if you are using custom theme for admin or frontend then follow the following steps -:

### <mark style="color:blue;">**Frontend**</mark>

1. **Check if you have the following files in your custom theme folder**

```
/app/design/frontend/default/<<custom>>/template/persi stent/checkout/onepage/billing.phtml
/app/design/frontend/default/<<custom>>/template/chec kout/onepage/billing.phtml
/app/design/frontend/default/<<custom>>/template/ customer/form/edit.phtml
/app/design/frontend/default/<<custom>>/template/ customer/form/register.phtml
/app/design/frontend/default/<<custom>>/template/persi stent/customer/form/register.phtml
/app/design/frontend/default/<<custom>>/template/onepagecheckout/onepage/billing.phtml (only if you are using IWD one page checkout)
```

1. **If these files do exist in your custom theme folder then copy the following files from the following paths -:**

```
/app/design/frontend/default/default/template/persistent/ checkout/onepage/billing.phtml
/app/design/frontend/default/default/template/checkout/ onepage/billing.phtml
/app/design/frontend/default/default/template/ customer/form/edit.phtml
/app/design/frontend/default/default/template/ customer/form/register.phtml
/app/design/frontend/default/default/template/persi stent/customer/form/register.phtml
/app/design/frontend/default/default/template/ onepagecheckout/onepage/billing.phtml (only if you are using IWD one page checkout)
```

**Admin**

1. **Check if you have the following file in your custom theme folder**
   1. **`/app/design/adminhtml/default/<<custom>>/template/sales/ order/view/info.phtml`**
2. **If this file do exist in your custom theme folder then copy the following file from the following paths -:**
   1. **`/app/design/adminhtml/default/scommerce/template/sales/ order/view/info.phtml`**

<mark style="color:orange;">**Please note:**</mark> You might just need to copy where did you hear about us code from the above files if your custom theme has different version of code from Magento.

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-where-did-you-hear-about-us.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
