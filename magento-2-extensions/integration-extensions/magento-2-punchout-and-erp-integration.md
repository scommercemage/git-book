# Magento 2 PunchOut & ERP Integration

### <mark style="color:blue;">Installation and User Guide for Magento 2 PunchOut & ERP Integration</mark>



1. [_Configuration Settings for PunchOut Integration_ ](magento-2-punchout-and-erp-integration.md#bookmark3)
   * _General Settings_&#x20;
   * _Order Creation Settings_
   * _Catalog Settings_
   * _Punchout Session Settings_&#x20;
2. [_Managing PunchOut Clients_](magento-2-punchout-and-erp-integration.md#managing-punchout-clients)
3. [_Setting Up Catalogs and Pricing_](magento-2-punchout-and-erp-integration.md#setting-up-catalogs-and-pricing)
4. [_Testing the Integration_](magento-2-punchout-and-erp-integration.md#testing-the-integration)
   * _Step-by-Step Testing Guide_
5. [_Handling Purchase Orders (End-to-End Workflow)_](magento-2-punchout-and-erp-integration.md#handling-purchase-orders-end-to-end-workflow)
6. [_Troubleshooting Common Issues_](magento-2-punchout-and-erp-integration.md#troubleshooting-common-issues)

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

### <mark style="color:blue;">Configuration Settings for PunchOut Integration</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Punchout**

#### <mark style="color:orange;">General Settings</mark>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [support@scommerce-mage.com](mailto:support@scommerce-mage.com).

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Order Creation Settings</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Cron for Order import –** Please allow to set cron frequency for order import from Noths.
* **API Url –** Please enter API Url.
* **API Log –** Select “Yes” to enable the API Log. If set to “Yes” then it will log communication with Noths API.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Catalog Settings</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Cron for Order import –** Please allow to set cron frequency for order import from Noths.
* **API Url –** Please enter API Url.
* **API Log –** Select “Yes” to enable the API Log. If set to “Yes” then it will log communication with Noths API.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">Punchout Session Settings</mark> <a href="#bookmark5" id="bookmark5"></a>

* **Cron for Order import –** Please allow to set cron frequency for order import from Noths.
* **API Url –** Please enter API Url.
* **API Log –** Select “Yes” to enable the API Log. If set to “Yes” then it will log communication with Noths API.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">**Managing PunchOut Clients**</mark>

This is the most critical part of the setup. Each corporate client you wish to integrate with must be configured as a "PunchOut Client."

1.  Go to **Admin>Customers>Punchout>Manage Punchout Clients**

    <div data-full-width="true"><figure><img src="../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure></div>
2.  Click **"Add New Punchout Client"** to configure a new connection.&#x20;

    <div data-full-width="true"><figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure></div>
3. Fill in the following fields:
   * **ERP Identifier:** The unique identifier provided by the client’s ERP system. This is often referred to as the `From Identity` or `Sender Identity` in cXML.
   * **Shared Secret:** The password or secret key used for authentication, provided by your client. This must be an exact match.
   * **Customer Group:** This is the key to personalizing the experience. Select the Magento customer group that this client's users should be assigned to upon logging in via PunchOut. This controls the catalog and pricing they see.
   * **Website:** Select Website
   *   **Is Active:** Set to "Yes" to activate the connection for this specific client.&#x20;

       <div data-full-width="true"><figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure></div>
4. Click **"Save Config."**

### <mark style="color:blue;">**Setting Up Catalogs and Pricing**</mark>

The extension leverages Magento's native customer group functionality to deliver a personalized experience.

1. **Create a Customer Group:** Before configuring a PunchOut client, navigate to **Customers > Customer Groups** and create a new group for them (e.g., "PunchOut - Global Office Inc.").
2. **Assign Custom Pricing:** Use **Marketing > Catalog Price Rules** to create rules that apply specific discounts or fixed prices for products and assign the rule to the customer group you just created.
3. **Restrict Catalog (Optional):** If you need to show only specific categories to a client, you may need to use native Magento functionality or a third-party category permissions module to restrict access for the designated customer group.

### <mark style="color:blue;">**Testing the Integration**</mark>

Our extension adheres strictly to industry standards, allowing you to validate your configuration using independent, third-party testing tools. We recommend using the **PunchOut Commerce cXML Order Tester**.

#### <mark style="color:orange;">**Step-by-Step Testing Guide:**</mark>

1. **Get Your PunchOut URL:** Your Magento PunchOut URL is typically your store's base URL followed by `/punchout/`. For example: `https://yourstore.com/punchout/`
2. **Open the Testing Tool:** Navigate to `https://punchoutcommerce.com/tools/cxml-order-tester`.
3. **Configure the Tester:**
   * **PunchOut Login URL:** Enter your Magento PunchOut URL from Step 1.
   * **cXML Payload:** The tool provides a template. You must edit the `Identity` and `SharedSecret` values in the XML to **exactly match** the credentials you configured for your PunchOut Client in the Magento admin.
4. **Initiate the Session:** Click the "PunchOut" button on the tester website.
5. **Shop in Magento:** You should be redirected to your Magento storefront and automatically logged in as a member of the mapped customer group. Browse the site and verify that you see the correct products and contract pricing. Add one or more items to your basket.
6. **Transfer the Cart:** Once you have items in your basket, click the **"Transfer Cart"** button.
7. **Verify the Response:** You will be redirected back to the PunchOut Commerce testing tool. It will now display the **cXML response** sent from your Magento store. Carefully inspect this XML to confirm that the correct SKUs, quantities, and prices are present. A successful test confirms your configuration is working correctly.

### <mark style="color:blue;">**Handling Purchase Orders (End-to-End Workflow)**</mark>

The PunchOut process is typically two-phased.

* **Phase 1 (Shopping):** The buyer transfers their cart from Magento to their ERP for internal approval. This is what you validated during testing.
* **Phase 2 (Ordering):** After the cart is approved, the client's ERP system sends a formal **Purchase Order (PO)** back to Magento as a new cXML message.

Our extension can receive this incoming Purchase Order and automatically create a corresponding sales order in your Magento system, enabling a fully automated, end-to-end workflow. The specific endpoint URL for receiving POs (`/punchout/order/`) should be provided to your client's IT team.

### <mark style="color:blue;">**Troubleshooting Common Issues**</mark>

* **Authentication Failed / Invalid Credentials:** This almost always means the **Identity** or **Shared Secret** in your PunchOut Client configuration does not match what is being sent by the ERP or testing tool. They are case-sensitive and must be an exact match.
* **User Sees Wrong Products or Pricing:** Verify that the PunchOut Client is mapped to the correct **Magento Customer Group**. Then, check the Catalog Price Rules and any category permissions assigned to that specific group.
* **Cart Transfer Fails or Returns an Error:** Check the Magento exception and system logs for detailed error messages. Common causes include products being out of stock or disabled.
* **Connection Timeouts:** Ensure your server's firewall allows incoming POST requests from your client's ERP system IP addresses or from the testing tools you are using.

If you have a question related to this extension please check out our [**FAQ Section**](magento-2-punchout-and-erp-integration.md#installation-and-user-guide-for-magento-2-noths-integration-extension) first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
