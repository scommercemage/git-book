# Google AdWords Conversion Tracking

### <mark style="color:blue;">Google Adwords Conversion Tracking - Installation/Set-up Guide</mark>

1. <mark style="color:orange;">**Disable Compilation Mode**</mark><mark style="color:orange;">:</mark> To check that this is disabled, go to **System->Tools->Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
2. <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
3. <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (System->Cache Management), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change. Logout and login back in Admin.
4. <mark style="color:orange;">**Configuration settings for Google Adwords Conversion Tracking:**</mark> Go to **Admin->System->Configuration->Scommerce Configuration->Google Adwords**->**General**
   1. **Enable:** Set yes to enable the module.
   2. **License Key:** Enter the License key provided by Scommerce Mage.
   3. **Conversion Id:** Enter your Google conversion Id.
   4. **Conversion Language:** Enter your Google Conversion Language
   5. **Conversion Format:** Enter your Google conversion format
   6. **Conversion Label:** Enter your Google conversion label
   7. **Conversion Color:** Enter your Google conversion color.
   8. **Remarketing tag only:** Specify if needed remarketing tag only
   9. **Additional Tracking Enable:** Set yes to enable another Google Adword tracking.
   10. **Conversion Id:** Enter your second Google conversion Id.
   11. **Conversion Language:** Enter your second Google Conversion Language
   12. **Conversion Format:** Enter your second Google conversion format
   13. **Conversion Label:** Enter your second Google conversion label
   14. **Conversion Color:** Enter your second Google conversion color.
   15. **Remarketing tag only:** Specify if needed remarketing tag only for your second tracking.
   16. **Enable GDPR cookie check:** If you are using our [GDPR extension ](https://www.scommerce-mage.com/magento1-gdpr-compliance.html)or any other GDPR extension and you want to block sending information to Google then set this to "yes" based on customer preference. Please note this is optional as far as you are not sending any PII to Google this setting needs to be turned off
   17. **Force decline:** If you set this to yes then Adwords tracking will be turned off unless customer accepts the cookie policy from the cookie notification message from your website
   18. **GDPR Cookie Key:** You can add name of your GDPR cookie here for our [GDPR extension ](https://www.scommerce-mage.com/magento1-gdpr-compliance.html)the name of cookie key is cookie\_accepted but if you are using other GDPR extension then please check with extension developer

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-google-adwords-conversion-tracking.html#faq) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
