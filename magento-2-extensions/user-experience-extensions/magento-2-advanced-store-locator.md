# Magento 2 Advanced Store Locator

### <mark style="color:blue;">Installation and User Guide for Magento 2 Advanced Store Locator</mark>

**Table of Contents**

1. [_Installation_ ](magento-2-advanced-store-locator.md#bookmark0)
   * _Installation via app/code_&#x20;
   * _Installation via Composer_&#x20;
2. [_Configuration Settings for Advanced Store Locator_](magento-2-advanced-store-locator.md#bookmark3)
   * _General Settings_&#x20;
3. [_Store Locator Region Management (Admin)_](magento-2-advanced-store-locator.md#bookmark6)
   * _Accessing Region Management_
   * _Creating a New Region_
   * _Editing Existing Regions_
   * _Deleting a Region_
4. [_Store Management & Region Association (Admin)_](magento-2-advanced-store-locator.md#id-2.-store-management-and-region-association-admin)
   * _Accessing Store Management_
   * _Creating a New Store_
   * _Editing Existing Stores_
   * _Deleting a Store_
5. [_Store List Display on Frontend (Customer)_](magento-2-advanced-store-locator.md#id-3.-store-list-display-on-frontend-customer)
   * _Viewing Stores Within a Selected Region_
   * _Viewing All Stores (Without Region Selection)_
6. [_Store Detail View (Customer)_](magento-2-advanced-store-locator.md#id-4.-store-detail-view-customer)
   * _Accessing Store Detail View_
   * _Understanding the Layout_
   * _Detailed Store Information_

### <mark style="color:blue;">Installation</mark> <a href="#bookmark0" id="bookmark0"></a>

* <mark style="color:orange;">**Installation via app/code:**</mark> Upload the content of the module to your root folder. This will not overwrite the existing Magento folder or files, only the new contents will be added. After the successful upload of the package, run below commands on Magento 2 root directory.

```
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy
```

* <mark style="color:orange;">**Installation via Composer:**</mark> Please follow the guide provided in the below link to complete the installation via composer.

{% embed url="https://docs.scommerce-mage.com/magento-2-extensions/installation-via-composer" %}

### <mark style="color:blue;">Configuration Settings for Advanced Store Locator</mark> <a href="#bookmark3" id="bookmark3"></a>

Go to **Admin > Stores > Configuration > Scommerce Configuration > Store Locator**

#### <mark style="color:orange;">General Settings</mark> <a href="#bookmark4" id="bookmark4"></a>

* **Enabled -** Select “Yes” or “No” to enable or disable the module.
* **License Key -** Please add the license for the extension which is provided in the order confirmation email. Please note license keys are site URL specific. Please go to _Admin > Stores > Configuration > Scommerce Configuration > Core_ and click on "Verify" to verify the license key.&#x20;
* **Items Per Page -** Add the number of items to be displayed per page
* **Enabled -** Enter the Google Maps API key to fetch the map for each store

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (236).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">Store Locator Region Management (Admin)</mark>  <a href="#bookmark6" id="bookmark6"></a>

This section outlines how administrators can create, edit, and delete regions to categorize your store locations effectively.

#### <mark style="color:orange;">**1.1. Accessing Region Management**</mark>&#x20;

To begin managing your store locator regions:

1. Navigate to **Admin > Stores >** **Scommerce Store Locator** in your Magento 2 Admin sidebar.
2.  From the menu, select **Store Regions**.



<figure><img src="../../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">**1.2. Creating a New Region**</mark>&#x20;

Follow these steps to add a new region to your store locator:

* On the Store Regions grid page, click the **Add New Region** button in the top-right corner.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure></div>

* You will be redirected to the New Region page. Fill in the following details:
  * **Active:** Toggle to activate or deactivate the region.
  * **Region Name:** Enter a unique name for your region (e.g., "North America," "Europe," "Asia Pacific"). This field is **required**.
  * **Description:** (Optional) Provide a brief description for the region. This can be used for internal reference.
  * **Region Image:** (Optional) Upload an image to represent the region. This might be displayed on the frontend depending on your theme and future enhancements.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure></div>

* Click **Save Region** to create the new region. A success message will appear, and you will be redirected back to the Region Management grid.

#### <mark style="color:orange;">**1.3. Editing Existing Regions**</mark>&#x20;

To view or modify details of an existing region:

* From the Region Management grid, locate the region you wish to edit.
* In the **Actions** column for that region, click **Edit.**
  * Clicking **Edit** will open the region details page where you can modify any of the fields (Region Name, Description, Image).

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure></div>

* After making any changes, click **Save Region** to apply your updates.

#### <mark style="color:orange;">**1.4. Deleting a Region**</mark>&#x20;

You can remove regions from your system, provided no stores are currently assigned to them:

* From the Region Management grid, locate the region you wish to delete.
* In the **Actions** column for that region, click **Delete**.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (265).png" alt=""><figcaption></figcaption></figure></div>

* Alternatively you can also edit the region and then use the "Delete" button at the top.
* A confirmation pop-up will appear. Click **OK** to confirm the deletion.
* **Important:** A region can only be deleted if no stores are associated with it. If stores are assigned, you will need to reassign or delete those stores first.
* Once a region is successfully deleted, it will be removed from the grid and will no longer appear as an option for store categorization or on the front-end store locator navigation.
* You can also Mass delete regions using following steps:
  * Select checkboxes next to messages.
  * From the **Actions** dropdown, choose **"Delete"**.
  * Confirm by clicking **"OK"** in the popup.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (267).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**1.5. Mass Action to Activate/Deactivate/Delete Regions**</mark>&#x20;

Go to **Admin>Stores>Scommerce Store Locator>Store Regions** select the regions that you want to **Deactivate/Activate/Delete**. Next click on the mast action button and then select the action as shown below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (277).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**1.6. Import Regions**</mark>

Go to Admin>System>Data Transfer>Import.

From the Entity Type dropdown select "Scommerce Store Locator Regions"

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure></div>

select the import file and other settings as needed then&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure></div>

```
// Sample Import File

Name,Description, Image
Greater London,"The metropolitan area surrounding London, known for its diverse neighborhoods and vibrant commercial activity.", “greater-london.jpg“
West Midlands,"A central region in England known for its industrial heritage and growing retail hubs.", “west-midland.jpg“
North West,"Encompasses major cities like Manchester and Liverpool, with a mix of urban and suburban retail locations.", “north-west.jpg“
```

### <mark style="color:blue;">**2. Store Management & Region Association (Admin)**</mark>

This section describes how administrators can create, manage, and associate individual store locations with the regions you've defined.

#### <mark style="color:orange;">**2.1. Accessing Store Management**</mark>&#x20;

To manage your store locations:

1. Navigate to **Admin > Stores >** **Scommerce Store Locator** in your Magento 2 Admin sidebar.
2. From the menu, select **Store Locations**.

<figure><img src="../../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:orange;">**2.2. Creating a New Store**</mark>&#x20;

Follow these steps to add a new store location:

* On the Store Locations grid page, click the **Add New Store** button in the top-right corner.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure></div>

* You will be redirected to the New Store page. Fill in the following details:
  * **Active:** Toggle to activate or deactivate the region.
  * **Store Title:** (Required) Enter the name of the store (e.g., "Main Street Branch").
  * **Store Address:** (Required) Provide the full physical address of the store. This will be used for the Google Map display on the frontend.
  * **Region Selection:** (Optional) Select an existing region from the dropdown menu to associate this store with. This dropdown will populate with regions created in the "Region Management" section.
  * **Phone:** (Optional) Enter the store's contact number.
  * **Email:** (Optional) Provide the store's email address.
  * **Working Hours:** (Optional) Describe the store's operating hours (e.g., "Mon-Fri: 9 AM - 6 PM, Sat: 10 AM - 4 PM").
  * **Days Open:** (Optional) List the days the store is open (e.g., "Monday - Saturday").
  * **Description:** (Optional) Any other relevant information about the store (e.g., "Free Parking Available," "Wheelchair Accessible" , "Short Description").
  * **Latitude:** Enter lattitude of the store location
  * **Longitude:** Enter longitude of the store location

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (255).png" alt=""><figcaption></figcaption></figure></div>

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (256).png" alt=""><figcaption></figcaption></figure></div>

* Click **Save Store** to create the new store. A success message will appear, and you will be redirected back to the Store Management grid.

#### <mark style="color:orange;">**2.3. Editing Existing Stores**</mark>&#x20;

To modify details of an existing store, including its assigned region:

* From the Store Locations grid, locate the store you wish to edit. The grid displays **ID, Title, Address, Region, Phone, Email, Active, Created, and Actions**.
* In the **Actions** column for that store, click **Edit**
  * Clicking **Edit** will open the store details page where you can modify any of the fields, including the **Region Selection**.
  * Clicking **View** will open the store details page in a read-only mode.
* After making any changes, click **Save Store** to apply your updates.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (257).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**2.4. Deleting a Store**</mark>&#x20;

To remove a store location from your system:

* From the Store Management grid, locate the store you wish to delete.
* In the **Actions** column for that store, click **Delete**.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (258).png" alt=""><figcaption></figcaption></figure></div>

* Alternatively you can also edit the store and then use the "Delete" button at the top.
* A confirmation pop-up will appear. Click **OK** to confirm the deletion.
* Once a store is successfully deleted, it will be removed from the grid and will no longer appear on the front-end Store Locator. Deleting a store only removes that specific store and does not affect other stores within the same region.
* You can also Mass delete regions using following steps:
  * Select checkboxes next to messages.
  * From the **Actions** dropdown, choose **"Delete"**.
  * Confirm by clicking **"OK"** in the popup.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**2.5. Mass Action to Activate/Deactivate/Delete Store Locations**</mark>&#x20;

Go to **Admin>Stores>Scommerce Store Locator>Store Locations** select the stores that you want to **Deactivate/Activate/Delete**. Next click on the mast action button and then select the action as shown below:-

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (281).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**2.6. Import Stores**</mark>

Go to Admin>System>Data Transfer>Import.

From the Entity Type dropdown select "Scommerce Store Locator Stores"

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (282).png" alt=""><figcaption></figcaption></figure></div>

select the import file and other settings as needed then&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (283).png" alt=""><figcaption></figcaption></figure></div>

```
// Sample Import File

Name,Address,Description,Region,Email,Phone,Working Hours,Longitude,Latitude,Days Open
London Central Store,"221B Baker Street, London NW1 6XE","Flagship store near Regent's Park",Greater London,central@storeuk.com,+44 20 7946 0011,"Mon–Sat: 9am–7pm",-0.1586,51.5237,"Monday–Saturday"
Croydon Outlet,"45 High Street, Croydon CR0 1QD","Discount outlet with parking",Greater London,croydon@storeuk.com,+44 20 8760 1122,"Mon–Fri: 10am–6pm",-0.1004,51.3762,"Monday–Friday"
Stratford Hub,"Westfield Stratford City, London E20","Modern store in shopping centre",Greater London,stratford@storeuk.com,+44 20 8221 3344,"Daily: 10am–8pm",-0.0064,51.5430,"All week"
Birmingham City Store,"12 New Street, Birmingham B2 4RQ","High-traffic location near Bullring",West Midlands,birmingham@storeuk.com,+44 121 633 4455,"Mon–Sat: 9am–6pm",-1.8998,52.4797,"Monday–Saturday"
Coventry Retail Point,"88 Broadgate, Coventry CV1 1NB","Family-friendly store with café",West Midlands,coventry@storeuk.com,+44 24 7655 9988,"Tue–Sun: 10am–5pm",-1.5105,52.4081,"Tuesday–Sunday"
Manchester Arndale,"18 Market Street, Manchester M4 3AT","Located in the heart of the city",North West,manchester@storeuk.com,+44 161 832 7788,"Daily: 9am–8pm",-2.2417,53.4839,"All week"
Liverpool One Branch,"Paradise Street, Liverpool L1 8JQ","Stylish store with seasonal offers",North West,liverpool@storeuk.com,+44 151 707 2233,"Mon–Sat: 10am–7pm",-2.9840,53.4045,"Monday–Saturday"
Preston Suburban Spot,"5 Fishergate, Preston PR1 2NJ","Quiet location with easy access",North West,preston@storeuk.com,+44 1772 555 900,"Wed–Sun: 11am–5pm",-2.7034,53.7590,"Wednesday–Sunday"
```

<mark style="color:blue;">**3. Store List Display on Frontend (Customer)**</mark>

This section describes how customers will interact with the Store Locator on your website's front-end.

#### <mark style="color:orange;">**3.1. Viewing Stores Within a Selected Region**</mark>&#x20;

Customers can easily find stores by filtering them by region:

1. Navigate to the Store Locator page on the front-end (typically via a link in the header or footer). **{root\_path}/storelocator**.&#x20;
2. On the left-hand side of the page, a navigation panel displays a list of available regions.
3. Click on any **region name** from this list.
4. The main content area will refresh to display only the stores associated with the selected region.
5. Each store entry will show:
   * A small **Google Map** snippet based on the store's address.
   * The **Store Name**.
   * The **Store Address**.
6. **Pagination:** If there are many stores within a selected region, they will be paginated. Stores are sorted alphabetically by default. You can navigate through the results using the "Next" and "Previous" controls.
7. **No Stores in Region Message:** If a selected region currently has no stores assigned, a message will be displayed: _“There are currently no stores available in this region. Please check back later or select another region from the list."_

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (285).png" alt=""><figcaption></figcaption></figure></div>

#### <mark style="color:orange;">**3.2. Viewing All Stores (Without Region Selection)**</mark>&#x20;

The Store Locator also allows customers to view all stores without initially filtering by region:

1. Navigate to the Store Locator page (without selecting a specific region). This typically happens when a user clicks on a general "Stores" or "Store Locator" link.
2. **Layout Adaptation:**
   * If **no stores** in the system have an associated region, the layout will automatically be **full width**, as there's no need for the left-hand region navigation.
   * If **at least one store** is linked to a region, the available regions will still be displayed in the **left-hand navigation** panel, even when viewing all stores.
3. The main content area will display a list of all available stores.
4. Each store entry will show:
   * A small **Google Map** snippet based on the store's address.
   * The **Store Name**.
   * The **Store Address**.
5. **Pagination:** Stores are paginated and sorted alphabetically. The pagination threshold can be configured by the admin in the module's backend settings. Users can navigate through paginated results using "Next" and "Previous" controls.
6. **No Stores Message:** If there are currently no stores in the system, a message will be displayed: _“There are currently no stores available. Please check back later."_

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (284).png" alt=""><figcaption></figcaption></figure></div>

### <mark style="color:blue;">**4. Store Detail View (Customer)**</mark>

This workflow describes how customers can access and view detailed information for a specific store.

#### <mark style="color:orange;">**4.1. Accessing Store Detail View**</mark>

1. From any store list display (either filtered by region or showing all stores), click on the **name of a specific store** or an associated "View Details" link.

#### <mark style="color:orange;">**4.2. Understanding the Layout**</mark>

* **Region List Visibility:** The presence of the region list on the left-hand navigation on the store detail page is determined by a **configuration setting in the admin panel**. Your administrator will decide whether this list is shown or hidden.
* **Layout Adaptation:**
  * If **no stores** in the system have an associated region, the store detail page will automatically be **full width**.
  * If **at least one store** is linked to a region, the available regions will be displayed in the **left-hand navigation** based on the aforementioned configuration.

#### <mark style="color:orange;">**4.3. Detailed Store Information**</mark>&#x20;

The store detail view provides comprehensive information about the selected store, including:

* **Large Google Map:** A larger, more prominent Google Map showing the precise location of the store based on its address.
* **Show Directions:** Clicking on this button takes you to the map (link) where people can view the directions to the store.
* **Store Name and Full Address:** Clearly displayed for easy identification.
* **Telephone Number:** For direct contact.
* **Email:** For direct email communication.
* **Days Open:** The specific days the store is open.
* **Working Hours:** Detailed operating hours.
* **Additional Store Details:** Any extra information provided by the admin.
* **Region:** (If applicable) The region to which the store is assigned, providing geographical context.
* **Back Button:** A button to go back to the list of stores page.

**4.4. Navigating Back**&#x20;

To return to the store listing:

1. Click the **"Back to Stores" link or button**. This will navigate you back to the previous store listing page, whether it was filtered by region or showing all stores.

<div data-full-width="true"><figure><img src="../../.gitbook/assets/image (286).png" alt=""><figcaption></figcaption></figure></div>

If you have a question related to this extension please check out our **FAQ Section** first. If you can't find the answer you are looking for then please contact [**support@scommerce-mage.com**](mailto:core@scommerce-mage.com)**.**
