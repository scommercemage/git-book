# Magento 2 Admin Message Manager

### <mark style="color:blue;">Installation and User Guide for Magento 2 Admin Message Manager</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-admin-message-manager.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_&#x20;
2. [_Configuration Settings for Admin Message Manager_](magento-2-admin-message-manager.md#bookmark3)
   * _General Settings_&#x20;
3. [_Admin Message Manager Workflow_](magento-2-admin-message-manager.md#bookmark6)
   * _Step 1: Access the Admin Message Grid_
   * _Step 2: Create a New Message_
   * _Step 3: Edit or Delete Messages_
4. [_Display logic for Admin Messages_](magento-2-admin-message-manager.md#display-logic-for-admin-messages)
   * _Why do messages appear?_
   * _How do messages appear?_
   * _HTML Support_
5. [_View Messages in Admin Panel_](magento-2-admin-message-manager.md#view-messages-in-admin-panel)
   * _Notice Message_
   * _Warning Message_
   * _Success Message_
   * _Error Message_

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

Go to **Admin > Stores > Configuration > Scommerce Configuration > Admin Message Manager**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. Please go to _Admin > Stores > Configuration > Scommerce Configuration > Core_ and click on "Verify" to verify the license key.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (232).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Admin Message Manager Workflow</mark> <a href="#bookmark6" id="bookmark6"></a>

Using this extension an admin create custom messages for the other admins and pass on critical updates based on user roles.

The admin can only use this functionality if the have the "Scommerce Admin Message Manager Section" selected under role resources for their user role.&#x20;

#### <mark style="color:orange;">**Step 1: Access the Admin Message Grid**</mark>

* Navigate to **Admin>System>Admin Message Manager**
* Only users with **"Scommerce Admin Message Manager Section"** permission can access this grid.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**Step 2: Create a New Message**</mark>

* Go to **Admin>System>Admin Message Manager**&#x20;
* Click **"Add New Message"**.

<figure><img src="../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

* Fill in the form:
  * **Enabled :-** Turn it on to enable the message (Active/Inactive toggle)
  * **Message Label** (Optional identifier)
  * **Severity Type** (Notice, Warning, Success, Error)
  * **User Roles** (Multi-select roles that should see the message)
  * **Message Text** (Supports HTML links, bold, italics via WYSIWYG editor)
* Click **"Save"**.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure></div>

**Note:**

* Required fields: **Enabled, Message Label, Severity, at least one User Role,** **Message Text.**
* HTML is sanitized for security (only `<a>`, `<strong>`, `<em>` allowed).

#### <mark style="color:orange;">**Step 3: Edit or Delete Messages**</mark>

**Edit A Message**

1. In the grid, click **"Edit"** on the desired message.
2. Modify any field (Label, Text, Severity, User Roles, Enabled).
3. Click **"Save"** or **"Delete"** (if removing the message).

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure></div>

**Delete A Message**

**Option 1: Single Deletion (From Grid)**

* Click **"Delete"** on the Edit row then confirm deletion

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure></div>

**Option 2: Single Deletion (From Edit Form)**

* Open the message>Click **"Delete Message"**>Confirm.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure></div>

**Option 3: Mass Delete (Bulk Action)**

1. Select checkboxes next to messages.
2. From the **Actions** dropdown, choose **"Delete"**.
3. Confirm by clicking **"OK"** in the popup.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:blue;">**Display Logic for Admin Messages**</mark>

#### <mark style="color:orange;">**When Do Messages Appear?**</mark>

A message is displayed in the admin panel if:

* **Status = Active**
* **Admin user’s role matches at least one selected role** in the message.\


<mark style="color:orange;">**How Do Messages Appear?**</mark>

* **Sticky banner** at the top of the admin panel.
* **Severity-based styling** (colors match Magento’s standard alerts):
  * **Success** (Green)
  * **Notice** (Blue)
  * **Warning** (Yellow)
  * **Error** (Red)

#### <mark style="color:orange;">**HTML Support**</mark>

* Allowed tags: `<a>`, `<strong>`, `<em>`.
* Links are clickable.

### <mark style="color:blue;">**View Messages in Admin Panel**</mark>

* Messages appear as **sticky banners** at the top of the admin panel.
* Only **active** messages matching the user’s role are displayed.

#### <mark style="color:orange;">Notice Message</mark>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Warning Message</mark>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Success Message</mark>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Error Message</mark>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure></div>

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
