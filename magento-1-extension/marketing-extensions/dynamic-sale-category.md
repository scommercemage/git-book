# Dynamic Sale Category

### <mark style="color:blue;">Installation and User Guide for Magento 1 Dynamic Sale category</mark>

**Table of Contents**

1. [Installation ](dynamic-sale-category.md#\_bookmark0)
   * Disable Compilation Mode&#x20;
   * Upload Package&#x20;
   * Clear Caches&#x20;
2. [Configuration Settings for Dynamic Sale category ](dynamic-sale-category.md#\_bookmark4)
   * General Settings&#x20;
3. [Product Special Price Set up ](dynamic-sale-category.md#\_bookmark6)
   * Product Assigned to Sale Category in the Back-end&#x20;
4. [Front-end Site View ](dynamic-sale-category.md#\_bookmark8)
   * Sale Products on the Category Page&#x20;

### <mark style="color:blue;">Installation</mark> <a href="#_bookmark0" id="_bookmark0"></a>

* <mark style="color:orange;">**Disable Compilation Mode:**</mark>** ** To check that this is disabled, go to **System >Tools> Compilation**. If the compiler status is ‘Disabled’, you are ready to go. If not, simply click the ‘Disable’ button on the right hand side of the screen.
* <mark style="color:orange;">**Upload Package:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added.
* <mark style="color:orange;">**Clear Caches:**</mark> This can be done from the admin console by navigating to the cache management page (**System > Cache Management**), selecting all caches, clicking ‘refresh’ from the drop-down menu, and submitting the change.

### <mark style="color:blue;">Configuration Settings for Dynamic Sale category</mark> <a href="#_bookmark4" id="_bookmark4"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Sale/Offer Category**

#### <mark style="color:orange;">General Settings</mark> <a href="#_bookmark5" id="_bookmark5"></a>

* **Enabled –** Select “Yes” or “No” to enable or disable the module.
* **License Key –** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. If you require license keys for dev/staging sites then please email us at [core@scommerce-mage.com](mailto:core@scommerce-mage.com)
* **Category Levels –** Choose the category level and save configurations to populate the sale category dropdown. You can then select your desired category where you want to show all the sale products.
* **Sale Category –** Choose the sale category created above to show your sale products. This category will then show all the products set up with special price.

**Please note –** You can set any existing category to be a sale category but this

will then only show sale products and will ignore any other products set up directly in the category itself.

* **Hide Sale Category with no product –** Hides sale category from appearing in the navigation if no sale product found.

![](../../.gitbook/assets/m1sale\_general.jpg)

### <mark style="color:blue;">Product Special Price Set up</mark> <a href="#_bookmark6" id="_bookmark6"></a>

As soon as any product is set with valid special price it automatically assigned to category set up for sale/offers in configurations. You can set special price from **Admin > Catalog > Manage Products > Select Product > Prices > Special Price.**

![](<../../.gitbook/assets/2 (55)>)

* <mark style="color:orange;">**Product Assigned to Sale Category in the Back-end –**</mark>** ** You can see the Sale Products in the back-end under “Sale/Offers” categories from **Admin > Catalog > Manage Categories** > Select Category **“Sales”** > Click on **“Products in Category”**

![](<../../.gitbook/assets/3 (87)>)

### <mark style="color:blue;">Front-end Site View</mark> <a href="#_bookmark8" id="_bookmark8"></a>

* <mark style="color:orange;">**Sale Products on the Category Page –**</mark> The products with special price will be shown under the category which you have selected from **Admin > Stores > Configuration > Sale / Offers category- “Sale”**.

![A screenshot of a cell phone  Description automatically generated](<../../.gitbook/assets/4 (77)>)

If you have a question related to this extension please check out our [**FAQ Section**](https://www.scommerce-mage.com/magento-dynamic-sale-category.html#faq) **** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
