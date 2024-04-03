# Magento 2 Creditsafe Integration

### <mark style="color:blue;">Installation and User Guide for Magento 2 Creditsafe Integration Extension</mark>

#### **Table of Contents**

1. [_Installation_](magento-2-creditsafe-integration.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_
2. _Configuration Settings for Creditsafe Integration_
   * _General Settings_&#x20;
   * _API Configuration_
   * _Limits and Messages Configuration_
   * _Limits Configuration_
   * _Emails_
   * _Customer Configuration_
3. _Frontend_

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

### <mark style="color:blue;">Configuration Settings for Creditsafe Integration</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to _Admin> Stores> Configuration> Scommerce  > Credit Safe_

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enable Module –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL-specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Show Address Form on Registration –** Set "Yes" to collect billing address from customer on user registration or signup form. If set "No" billing address won't be captured on user registration.
* **Archiving Log –** Set "Yes" to archive credit safe logs after a certain number of days and set "No" to turn off archiving.
* **Archive Log After Number Of Days –** Enter the number of days after which the logs will be archived.&#x20;

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 15.08.52.png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">API Configuration</mark> <a href="#bookmark4" id="bookmark4"></a>

* **User Name –** Enter the Creditsafe Username
* **Password –** Enter the Creditsafe Password. Once both username and password are entered and saved click on the "Test API Creds" button if it shown "success" in green then your credentials are correct if not then please re verify your credentials.
* **Use Test Mode –** Set "Yes" to enable sandbox creditsafe and set "No" to use live creditsafe.
* **Enable API Logging –** Set "Yes" or "No" to Enable/Disable API logging in DB

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.17.52.png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Limits and Messages Configuration</mark> <a href="#bookmark4" id="bookmark4"></a>

Create creditsafe rules based on your requirements.

* **Type –** Select the user type either "Buisness" or "Consumer" this rule will be created for the appropriate applicant type.
* **CS Credit Limit/Score Range -** Enter the credit limit or credit score range for the particular rule.
* **Limit–** Enter the credit limit to be assigned for this rule based on the score entered previously. If the score is in this range then the entered limit should be provided to the applicant.
* **Limit Type –** You can choose to define the limit type to be assigned from either an absolute value or the percentage of the Credit Limit/Score.&#x20;
* **Response –** Enter the response shown to the customer when they fullfill the criteria for this rule and the the limit is assigned to them
* **Response Type –** Choose the response type from either Success or Failure.

Similarly you can create multiple rules as per your requirements to appropriately assign the credit limits to your applicants.

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.18.14.png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Limits Configuration</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Credit Applied Message –** Enter the message that will be displayed to user when they have previously applied for Creditsafe application.

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.18.31.png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Emails</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enable Email –** Select “Yes” or “No” to enable or disable the creditsafe application emails.
* **Success Email Template –** Select the template to be used for success emails (successfull credit safe application).
* **Success Email Sender –** Select the Email Sender, the email to be used to send the success emails.&#x20;
* **Success Email Recipient –** You can add an additional email where the success emails will be sent alongside the applicant.&#x20;
* **Fail Email Template –** Select the template to be used for fail emails (failed credit safe application).
* **Fail Email Sender –** Select the Email Sender, the email to be used to send the failure emails.&#x20;
* **Fail Email Recipient –** You can add an additional email where the failure emails will be sent alongside the applicant.
* **Admin Fail Email Template –** Please add the
* **Admin Fail Email Sender –** Please add the
* **Admin Fail Email Recipient –** Please add the
* **Admin API Result Email Template –** Please add the
* **Admin API Result Email Sender –** Please add the
* **Admin API Result Email Recipient –** Please add the

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.18.41.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.18.56 (1).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">Customer Configuration</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Approval Type  –** Select either "disabled" "manual" or "automatic", if selected "disabled" the approval will be disabled. if selected "manual" the credtisafe applications will be only approved by the magento admin. If selected "automatic" the credisafe applications will be automatically approved or denied based on the Credit limits and Messages Configuration.
* **Allow customers to retry –** If set to "Yes" customers will be able to re-apply for creditsafe application. If set to "No" once creditsafe application is submitted they won't be able to retry the application.
* **Email Sender –** Select the email sender which will be used to send out applicant verification emails
* **Verification Success Email Template –** Select the Email template to be used for successfull applicant verification.
* **Verification Rejected Email Template –** Select the Email template to be used for failed applicant verification.
* **Failed Credit Limit Message  –** Please add the
* **Failed Credit Limit (retries left)  –** Please add the
* **Failed Credit Limit Message  –** Please add the
* **Failed Credit Limit (no retries)  –** Please add the

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.19.28.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2024-04-03 at 17.19.38.png" alt=""><figcaption></figcaption></figure>

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
