# Magento 2 GDPR Compliance: Anonymisation of order data

### <mark style="color:blue;">Installation and User Guide for Magento 2 GDPR Compliance: Anonymisation of Transaction Data Extension</mark>

**Table of Contents**

1. __[_Installation_ ](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark0)__
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. __[_Configuration Settings for GDPR_ ](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark3)__
   * _General Settings_&#x20;
   * _Order and Quote Anonymisation Settings_&#x20;
   * _Privacy Settings_&#x20;
3. __[_Configuration Settings for Cookie Popup_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark7) __&#x20;
   * _General Settings_&#x20;
   * _Popup Styling_&#x20;
   * _Additional Tabs_&#x20;
4. __[_Admin Configuration for Manage Cookie Choices_ ](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark11)__
   * _Manage Choice List_&#x20;
   * _Add New Cookie Choice_&#x20;
5. [_Customers Details in Privacy Policy Consent_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark20)__
6. __[_Anonymize Orders from Admin Section_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark21)__
7. __[_Newsletter Subscription_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark22)__
8. __[_Enable / Disable Tracking Without GTM_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark23)__
   * _Using Module_
   * _Manually Adding Code_
9. __[_Integrate Cookies with GTM Pro Tracking_](magento-2-gdpr-compliance-anonymisation-of-order-data.md#integrate-cookies-with-gtm-pro-tracking)__
10. __[_Front-end Site View_ ](magento-2-gdpr-compliance-anonymisation-of-order-data.md#\_bookmark25)__
    * _Front-end Site View - Integrate Cookies with GTM Pro Tracking_&#x20;
    * _Cookie Pop-up- Cookie Accept_&#x20;
    * _Cookie Preferences_&#x20;
    * _Check the Value of the Accepted Cookies on the Front-end_&#x20;
    * _Visibility of "Accept All" Button on the Cookie Popup_&#x20;
    * _Newsletter Subscription_&#x20;
    * _Privacy Policy Checkbox on Registration and Checkout Page_&#x20;
    * _Delete Account from My Account Section_&#x20;

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

### <mark style="color:blue;">Configuration Settings for GDPR</mark> <a href="#_bookmark3" id="_bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > GDPR**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark4" id="_bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com.](mailto:core@scommerce-mage.com)
* **Enable Customer Account Deletion/ Anonymisation -** Set to “Yes” if you want to delete record on the frontend from my account.
* **Attention Message -** The message shown to customers on the frontend before deleting the account.
* **Success Message -** The message shown to customers on the frontend after deleting the account.
* **Email Sender -** Select email sender. The email address used to send the link to the customer to delete their account and confirmation email about deletion. It also sends customer data to administrator just before deleting.
* **Confirmation Email Template -** Select confirmation email template.
* **Delete Confirmation Email Template -** Select template for delete confirmation email.
* **Enable Cookie Message -**This allow you to enable or disable the module.
* **Block access to site until cookie policy is accepted -** If set to “Yes” then **** customer access to site will be blocked until cookie policy is accepted. If set to “No” then just normal cookie message block will be shown until cookie policy is accepted, but the access to the site will be allowed.
* **Page Wrapper Css Class - Add** the page wrapper Css class.
* **Cookie text message -** Enter cookie text message, if you want to display message in cookie policy area.
* **Information Page -** Use this page to learn about cookie settings.
* **Cookie link text -** Text on link to information page.
* **Cookie text color -** Color of cookie text message.
* **Cookie link color -** Cookie of link in cookie policy area.
* **Cookie background color -** Background color of cookie policy area.
* **Message Position -** Select position "Top/Bottom" of the cookie notification message.

![](../../.gitbook/assets/gdpr\_general.jpg)

![](../../.gitbook/assets/gdpr\_general2.jpg)

### <mark style="color:blue;">Order and Quote Anonymisation Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Order anonymisation after (days) -** Enter the number of days to anonymize personal data in order related tables. Leave it blank, if you don’t want to anonymize any personal data automatically.
* **Chunk of order to anonymize –** If you have a huge amount of transactions in the system, then you should limit the number of transactions to be anonymized when the cron job runs every hour.
* **Quote expires after (days) –** Enter number of days to set personal data to NULL in sales\_flat\_quote table.
* **Enable Debugging –** If set to “Yes” it will log debugging data related to quote and order anonymisation in the log file under var/log/anonymisation log.

![](../../.gitbook/assets/gdpr\_orderquotesettings.jpg)

### <mark style="color:blue;">Privacy Settings</mark> <a href="#_bookmark6" id="_bookmark6"></a>

* **Enable Privacy Setting –** This will enable privacy agreement checkbox on pages where you collect personal data.
* **Privacy Setting Text –** This text will appear next to privacy agreement checkbox.
* **Enable Newsletter –** If set to “Yes” then privacy agreement checkbox will appear for the customers to confirm before submitting the newsletter subscription.
* **Enable Registration –** If set to “Yes” then privacy agreement checkbox will appear for the customers to confirm before submitting the registration form.
* **Enable Contact us –** If set to “Yes” then privacy agreement checkbox will appear for customers to confirm before submitting the contact us form.
* **Enable Checkout –** If set to “Yes” then privacy agreement checkbox will appear for customers to confirm before submitting the billing form.

![](../../.gitbook/assets/gdpr\_privacysettings.jpg)

### <mark style="color:blue;">Configuration Settings for Cookie Popup</mark> <a href="#_bookmark7" id="_bookmark7"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Cookie Popup**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark8" id="_bookmark8"></a>

* **Enabled -** Select “Yes” or **“**No**”** to enable or disable the module.
* **Modal Title -** Enter name of the modal title, this will be shown on the frontend cookie popup modal. We’ve set modal title as “Cookie preferences”.
* **Save Choice Button Text -** Enter the title of the save choice button. Click on this button will save the cookies choice. Whatever the current cookie choice is there it will save that choice.
* **Allow All Button Text -** Enter title of the allow all button**.** We've set title as "Allow All". When you click on "ALLOW All" then cookies will allow the provision of enhance functionality, it will keep track of how many people have visited website, and how they interact with the site. All the information used is aggregated and completely anonymous. If you do not allow cookies, then functionalities may not function properly.
* **Accept Button Text -** Enter button title for accepting cookies on the cookie message, it will accept all cookies.
* **Cookies List Header -** Title of the block for the "Used by" list. Cookies name will be shown under this cookies list header. You can see "Used by" list on the frontend Cookie popup.
* **Cookie Settings Link Text -** This link will be shown on the frontend cookies message to show Cookie Popup Settings. Click on this link will open Cookie popup.
* **Cookie Message Settings Link Text -** Please add the cookie message link text
* **GTM -** Select "Yes" or "No" to enable disable the GTM.
* **Use Data Layers -** Select "Yes/No". If set to "Yes" then Data Layers will be used, instead of cookies for GTM. If set to "No", then it won't add Data Layers.
* **Show if not all accepted -** Select “Yes/No”. If set to “Yes” then Cookie notice message will appear if not all cookie accepted.

![](../../.gitbook/assets/gdpr\_cookiepopupgeneral.jpg)

### <mark style="color:blue;">Popup Styling</mark> <a href="#_bookmark9" id="_bookmark9"></a>

* **Modal Border -** Select "Yes", if you want to set modal border. If "Yes" then you can set border color for the settings Modal box.
* **Popup Border Color -** Enter popup border color. We've set the popup border color white, which you can see in the screenshot.
* **Toggle Color –** Enter Toggle color. We’ve set the toggle color. which you can see in the screenshot.
* **Header Background Color -** Enter header background color. Background color of the Modal box title.
* **Header Font Color -** Enter header font color.
* **Header Bottom Border -** Select "Yes", if you want to set the bottom border. If "Yes" then bottom border of the Modal box header will be shown.
* **Header Bottom Border Color -** Enter header bottom color. We’ve set the red header bottom border.
* **Footer Background Color -** Enter footer background color.
* **Footer Font Color -** Enter footer font color.
* **Footer Top Border -** Select "Yes", if you want to set footer top border. If “Yes” then top border of the footer of the Modal Box will be shown.
* **Footer Top Border Color -** Enter footer top border color.
* **Header Logo -** Choose logo for the modal header. It will be shown in the left top corner in header.
* **Close Image -** Upload close image.
* **Active Tab Background Color -** It will highlight the selected choice text.
* **Number Tabs -** Select "Yes", if you want number tabs on cookie modal.
* **Tab Active Color -** Enter active tab color.
* **Tab Header Color -** Enter tab header color.
* **Custom Button Style -** Select "Yes", if you want to style button.
* **Custom Checkbox -** Select "Yes", if you want to show cookie choice button.
* **Font Family -** Enter base font family for the Modal Box. Should be string e.g. Arial. Font should be available on the site.
* **Accept Button Text Color -** Enter text color of the "Accept" button on the Cookie Message
* **Accept Button Background Color -** Enter Background color of the "Accept" button on the Cookie Message.
* **Notice Height -** Set min height of the Cookie Message. E.g. 80
* **Required cookie option text -** Set to "Always Active", this text will replace checkbox for mandatory cookies
* **Custom CSS -** Provide CSS code for custom style.

![](../../.gitbook/assets/gdpr\_popupstyling.jpg)

![](../../.gitbook/assets/gdpr\_popupstyling2.jpg)

### <mark style="color:blue;">Additional Tabs</mark> <a href="#_bookmark10" id="_bookmark10"></a>

* **First Tab Title -** Provide title of the first tab you want to display on the frontend cookie pop up. This tab will be shown first before cookie choices. Both Title and Text should be set to appears on the Modal box
* **First Tab Text -** Enter first tab text. The text will be shown on the Modal box on click of first tab. We've set first tab as "Your Privacy ".
* **More Information Title -** Provide more information title. This will be shown after all cookie choices as a last tab. Both title and link should be set to appears on the Modal box
* **More Information Link -** Provide link where you want to redirect it. Click on this link will redirect you to Information page.

![](../../.gitbook/assets/gdpr\_additionaltabs.jpg)

### <mark style="color:blue;">Admin Configuration for Manage Cookie Choices</mark> <a href="#_bookmark11" id="_bookmark11"></a>

* **Manage Choice List -** To create and manage cookie choices, go to **Admin**
* **Customers > Manage Cookie Choices > Manage Choice List**. If you need to make some modifications in the cookie choices information, you should click “Edit” in the Action column. The grid includes the following columns: -

![](../../.gitbook/assets/gdpr\_integratecookies.jpg)

* <mark style="color:orange;">**Add New Cookie Choice -**</mark>** ** To create a new cookie choice, click on the “Add New Cookie Choice” button from **Admin > Customers > Manage Cookie Choices > Manage Choice List > Add New Cookie Choice**, it redirects on "New Choice" page, by providing all the below configuration details you can create the cookie choice.
  * **Choice Name -** Enter the choice name. This is the text which represents the type of the cookie you are using under it.
  * **Cookie Name -** Define the cookie name. Cookie name will be used to enable/disable your relevant trackings. To explore more about Cookies, please check the [Privacy and Cookie Policy ](http://magento2.scommerce-mage.co.uk/privacy-policy-cookie-restriction-mode/)section.
  * **Store View -** Select store view.
  * **Choice Description -** Add the choice description. This description will appear on the cookie pop up when user clicks on the cookie choice name.
  * **Cookies Created By -** Add the created by details. This is just an information which will appear on the cookie pop up under "Cookies are user by" section.
  * **Required -** Select "Yes" to make cookie essential, else select "No". If set to "Yes" then the cookie choice will always be selected and you can't turn "Off" it.
  * **GTM-** Set this to "Yes" if you want to control GTM using this cookie. GTM will only be enabled when this cookie is accepted.
  * **Set by Default -** Select default status "Yes" or "No". If set to "Yes" then by default the cookie choice will be selected.

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">Customers Details in Privacy Policy Consent</mark> <a href="#_bookmark20" id="_bookmark20"></a>

When customers check the privacy policy agreement checkbox in the process of registration then it saves the details of the customers in backend privacy policy consents at **Admin > Customers > Privacy Policy Consent.**

### Privacy Policy Consent

![](<../../.gitbook/assets/gdpr\_privacy (1).jpg>)

### <mark style="color:blue;">Anonymize Orders from Admin Section</mark> <a href="#_bookmark21" id="_bookmark21"></a>

When you select action "Anonymise order" from **Admin > Sales > Orders > Actions > Anonymise Order > Click on Submit button**, then it anonymise customers data, which can't be reversed. Before "Submit" it asks for confirmation and displays a message popup says "Are you sure you want to anonymise selected transaction data because of this action can't be reversed?".

![](../../.gitbook/assets/gdpr\_anonymizeorders.jpg)

### <mark style="color:blue;">Newsletter Subscription</mark> <a href="#_bookmark22" id="_bookmark22"></a>

To see newsletter subscription records go to **Admin > Marketing > Newsletter Subscription.**

![](../../.gitbook/assets/gdpr\_newslettersub.jpg)

### <mark style="color:blue;">Enable / Disable Tracking Without GTM</mark> <a href="#_bookmark23" id="_bookmark23"></a>

#### <mark style="color:orange;">Using Module</mark>

You can enable or disable GTM tracking using cookies. We have provided an additional check in cookie setup which confirms whether GTM should be checked alongwith the cookie or not. when this check is enabled if the customer doesent accept the cookie then this tracking won't fire. If multiple cookies have the same option enabled then if any one of the cookie is accepted GTM will fire on the store.

Go to Customers>Manage Cookie Choices then create a new cookie or edit the existing one and set GTM to 'Yes'.

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Manually Adding Code</mark>

This section will cover Enabling or Disabling tracking without using Google Tag Manager. You can do that by including tracking function in your code, let us learn how. If you are using any of our tracking extensions or any other third party extension and you don't want to send information to Google then you need to check for the cookie name e.g. "statistics\_cookie" and this will be set to 1 for "accept" and 0 for "decline", based on cookie value it will enable or disable the tracking.

In case you are using a third party extension then you need to add the code given below. This code needs to be added where your tracking has been implemented.

**Here is the function which will force your tracking not to run unless the cookie has been accepted by the customer from cookie notification message.**

**e.g.** You can add name of your GDPR cookie, here for our GDPR extension the name of cookie key is "statistics\_cookie", which we have been using in below code.

```
/**
Check if has cookie with accepted cookie policy
*
@return bool
*/
protected function hasCookie()
{
/**
* @var \Magento\Framework\Stdlib\CookieManagerInterface
*/
$cookie = (string)$this->_cookieManager->getCookie('statistics_cookie'); if ($cookie=="0"){
return false;
}
else{
return true;
}
}
```



### <mark style="color:blue;">**Integrate Cookies with GTM Pro Tracking**</mark>&#x20;

You can integrate cookies with GTM Pro by following the below steps in GTM:-

**Step 1 –** The very first step is to create your cookie from the admin panel. To do that please refer to the 4th Part in this guide. The key thing to remember is the name of the cookie that you create in this step.

![](../../.gitbook/assets/gdpr\_integratecookies.jpg)

**Step 2 –** The next step is to verify whether your cookie is working properly. Go on your website and accept or decline the cookie you have created in the begining. Now navigate to the Page inspector of your browser. Next go into application and then on the left navigation go to storage>cookies and then click on your website. A list of cookies will appear before you as you can see in the image. Now suppose you created a cookie named “Statistics\_cookie” in the first step and have accepted it on the website then the value of this cookie will appear as 1. Vice versa if you have declined this cookie then the value will be 0.

![](../../.gitbook/assets/gdpr\_integratecookies2.jpg)

**Step 3 –** Open google tag manager, go into variables section and Create a new variable named "**statistics\_cookie**", variable type should be **1st-Party cookie** and give the name of the cookie as "**statistics\_cookie**". Keep in mind the name of the cookie should be exactly same as you have created in the admin panel. For instance, we created a cookie named “Statistics\_cookie” so we have a variable named exactly same.

![](../../.gitbook/assets/gdpr\_integratecookies3.jpg)

**Step 4 –** Now navigate to triggers in GTM and select a trigger and add a custom event as follows: -

* From first drop-down- select variable name created in Step 1 i.e. "**statistics\_cookie**"
* From second drop-down- select equals
* Third Input box- put value 1

![](../../.gitbook/assets/gdpr\_integratecookies4.jpg)

**Step 5-** Associate the trigger created in Step 4 with any of the existing tags and that tag will only fire when customer accepts the cookie on your website.

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark25" id="_bookmark25"></a>

#### <mark style="color:orange;">Front-end Site View - Integrate Cookies with GTM Pro Tracking</mark> <a href="#_bookmark26" id="_bookmark26"></a>

Let us see how it works on the front-end.

* Visit the store and go to cookie settings on the pop-up. In the cookie preferences:- -- select your cookie. In this case we have created statistics cookie. -- Next from the top right corner select the checkbox to enable the cookie and save your choice.

![](../../.gitbook/assets/gdpr\_front1.jpg)

* Next check the inspector of your browser to verify whether your cookie is enabled/disabled. If you have enabled the cookie then the value will be 1 and if it is disabled then the value will be 0. Refer to the image below.

![](../../.gitbook/assets/gdpr\_front2.jpg)

* Finally check the GTM pro to see whether the tags that we associated with your cookie have fired or not. In our case universal analytics is fired since we added the cookie settings for google analytics. Similarly if the cookie is disabled I.e value is 0 then this tag won’t be fired.

![](../../.gitbook/assets/gdpr\_front3.jpg)

#### <mark style="color:orange;">Cookie Pop-up- Cookie Accept</mark> <a href="#_bookmark27" id="_bookmark27"></a>

Cookies are used to improve the experience for user. Once you accept, the file is added and the cookie helps analyse web traffic or lets you know when you visit a particular site. Cookies allow web applications to respond to you as an individual.

![](../../.gitbook/assets/gdpr\_front4.jpg)

#### <mark style="color:orange;">Cookie Preferences</mark> <a href="#_bookmark28" id="_bookmark28"></a>

You can configure cookie choices from **Admin > Customers > Manage Cookie Choices > Manage Choice List, configured cookie choice** will be shown on the front-end under "Cookies Settings " section. By clicking on the "Cookie Settings" link, a customer will open a Cookie Preferences pop up, from where a user can Accept or Decline cookies. Below is the description under each cookies category that clarifies how the cookies it contains are used.

* **Strictly Necessary Cookies -** These cookies are essential for the website to function and they cannot be turned off. They are usually only set in response to actions made by you on our site, such as logging in, adding items to your cart or filling in forms. If you browse our website, you accept these cookies.
* **Performance Cookies -** These cookies are essential for the website performance
* **Statistics Cookies -** This cookie gets used by Google Analytics to collect statistics to optimize site functionality, and deliver content tailored to your interests
* **Marketing Cookies -** Marketing cookies are used to track visitors across websites. The intention is to display ads that are relevant and engaging for the individual customers and thereby more valuable for publishers and third party advertisers.

![](../../.gitbook/assets/gdpr\_front5.jpg)

#### <mark style="color:orange;">Check the Value of the Accepted Cookies on the Front-end</mark> <a href="#_bookmark29" id="_bookmark29"></a>

You can check the value of the accepted cookies by using developer tool (F12). Here is the path to check, **Press F12 > Network > Storage > Cookies >** Click on **site URL >** Check the cookies status/value under **"Value"** column.

**When you "accept" cookies, the value will be set to "1".**

![](../../.gitbook/assets/gdpr\_front6.jpg)

**When you "decline" cookies, the value will be set to "0" .**

![](../../.gitbook/assets/gdpr\_front7.jpg)

#### <mark style="color:orange;">Visibility of "Accept All" Button on the Cookie Popup</mark> <a href="#_bookmark30" id="_bookmark30"></a>

The "Accept All" button will be shown on the cookie popup, if all cookie choices are not required and "Set by Default" for cookie choices set to "No" from **Admin > Customers > Manage Cookie Choices > Manage Choice List > Select Cookie Choice > Edit >Set by Default - "Yes/No".** If set to "Yes" then "Accept All" won't appear.

#### <mark style="color:orange;">Newsletter Subscription</mark> <a href="#_bookmark31" id="_bookmark31"></a>

Once Enable Newsletter is configured from **Admin > Stores > Configuration > Scommerce Configuration > GDPR > Privacy Settings > Enable Newsletter - "Yes"** , then you can see the privacy agreement checkbox on the newsletter subscription. This is a mandatory option. Click on "Privacy Policy" link redirects to privacy policy page.

![](../../.gitbook/assets/gdpr\_front8.jpg)

#### <mark style="color:orange;">Privacy Policy Checkbox on Registration and Checkout Page</mark> <a href="#_bookmark32" id="_bookmark32"></a>

The privacy policy checkbox will be shown on the registration and checkout page.

![](../../.gitbook/assets/gdpr\_front9.jpg)

#### <mark style="color:orange;">Delete Account from My Account Section</mark> <a href="#_bookmark33" id="_bookmark33"></a>

You can delete the account from **Front-end > My Account > Delete Account section.**

![](../../.gitbook/assets/gdpr\_front10.jpg)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-2-gdpr.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
