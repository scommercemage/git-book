# Magento 2 Consent mode's setup guide

**IN MAGENTO**

1. Once you have installed the modules **“Google Tag Manager Pro Tracking”**, **“Tracking Base”**, ”**Cookie Popup**” and “**GDPR**”, enable them and enter the correct license key.

![](<../../.gitbook/assets/0 (1) (1).png>)

2. After that, go to **“Customers”** -> **“Manage Cookie Choices”** and click on **“Add new Cookie Choice”** to set up cookie choices in the Cookie Popup extension.

![](<../../.gitbook/assets/1 (9).png>)



**2a**. You can do the setup of a new cookie as shown in the below image or you can create your own cookie/s. Please note that **“Cookie Name”** and **“Set by default”** are the most important fields as they would be used in the cookie mapping as described in the later steps.

![](<../../.gitbook/assets/2 (5).png>)

**2b.** Once you have created a cookie or multiple cookies, your setup should resemble the below image-

![](<../../.gitbook/assets/3 (5).png>)

3. Now, go to **“System”**->**”Configuration”**->**“Tracking Base”**. Scroll down and you would see the field **“Enable Consent Mode”**, enable it in order to enable the consent mode. The&#x6E;**,** go to **“Cookie mapping”**, add the **“Consent Param”** that are given in the description”(**personalization\_storage**, **functionality\_storage**, **security\_storage** are not mandatory for correct consent setup), set the **“Default value”** of the consent parameter as “**granted”** or “**denied”** based on the **“Set by default”** (step 2a) value of the cookie. Use the **“Cookie Name”** that you used while creating the cookies. For example- **analytics\_storage**, if you want to do mapping of this consent param with Analytics cookie then in the field **“Cookie name”** add **“analytics\_cookie”** because this cookie name was used when you were creating cookies (step 2a). While creating the cookie (in this case Analytics cookie), if the value of **“Set by default”** is set to **“No”** then while doing the mapping the **“Default value”** of the consent param (in this case analytics\_storage) that is associated with that cookie should be set to **“denied”** or vice versa.

![](<../../.gitbook/assets/4 (4).png>)

**On Magento’s end consent mode setup is complete.**

**In GTM**

1. Open the container that is connected with our GTM module, go to **“Admin”**->**“Container Settings”** and enable consent overview present in the additional settings.

![](<../../.gitbook/assets/5 (2).png>)

![](<../../.gitbook/assets/6 (1) (1).png>)

2. Go to **“Workspace”**->**”Tags”** -> click on **“Consent Overview”** (shield) and set up consent for each tag. Make sure to select **“No additional consent required”** for Tags that already have **“Built-In Consent**”. These tags are generally Google related tags.

![](<../../.gitbook/assets/7 (1) (1).png>)

![](<../../.gitbook/assets/8 (1) (1).png>)

**2a**. In order to add **“Additional Consent”**, click on the tag name and go to **”Consent Settings”** and choose **“Require additional consent for tag to fire”** and add the consent param that you want as **“Additional Consent”**. If cookies related to the consent parameter that is chosen as an additional consent are not accepted then that tag would not fire.

![](<../../.gitbook/assets/9 (1) (1).png>)

**On GTM’s end consent mode setup is complete**.

**Verification**

1. In order to verify whether the consent mode is working as per the configuration you have set or not, you can preview your changes and compare them with the frontend as shown in the below images. All the values should be the same.

![](<../../.gitbook/assets/10 (1) (1).png>)

![](<../../.gitbook/assets/11 (1) (1).png>)

![](<../../.gitbook/assets/12 (1) (1).png>)

![](<../../.gitbook/assets/13 (1) (1).png>)

![](<../../.gitbook/assets/14 (1) (1).png>)
