# Magento 2 Admin Message Manager

### <mark style="color:blue;">Installation and User Guide for Magento 2 Admin Message Manager</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-admin-message-manager.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_&#x20;
2. _Configuration Settings for Admin Message Manager_
   * _General Settings_&#x20;
3. [_Admin Account Switcher Workflow_](magento-2-admin-message-manager.md#bookmark6)
4. [_Admin Account Switcher Role_](magento-2-admin-message-manager.md#bookmark6-1)

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Installation via app/code:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% embed url="https://docs.scommerce-mage.com/magento-2-extensions/installation-via-composer" %}

### <mark style="color:blue;">Configuration Settings for Admin Message Manager</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Admin Account Switcher**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. Please go to _Admin > Stores > Configuration > Scommerce Configuration > Core_ and click on "Verify" to verify the license key.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Admin Account Switcher Workflow</mark> <a href="#bookmark6" id="bookmark6"></a>

Using this extension an admin can login into another admin's account directly from admin edit form section without requiring a password which allows them to debug easily without having to reset the other admin's password.

The admin can only use this functionality if the have the "Scommerce Switch Admin Account" selected under role resources for their user role.&#x20;

Go to Admin>System>Permissions>All Users, here select(click edit) the admins account in which you want to login.

From the top menu click on "Switch User" and you will be logged into that admin's account without password authentication.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (235).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Admin Account Switcher Role</mark> <a href="#bookmark6" id="bookmark6"></a>

The “Switch to User” button is displayed **only if** the current admin user has the **“Scommerce Switch Admin Account“** permissions in their user role.

To check this, you can go to _Admin>System>Permissions>User Roles>Role Resources_ and check whether the user role has "Scommerce Switch Admin Account Role" selected.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (234).png" alt=""><figcaption></figcaption></figure></div>

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
