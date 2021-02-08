## Overview:
[Magento 2 Region & City Dropdown Manager](https://www.magepsycho.com/magento2-region-city-dropdown-manager.html) extension allows the store admin to manage(add, edit, delete, bulk import) regions/states & cities, converts text-input city field to the select dropdown in checkout address (shipping & billing) & customer address pages for both storefront and backend.

Magento 2 by default has only the data-structure for regions/states without any administration capabilities. Also, the city field is displayed as text-input leading typos & invalid addresses.

With this extension, store admin can easily manage both regions & cities from the backend UI. And the list of cities which are managed from the backend will be shown as a select dropdown to the customer during checkout & address management. This will not only avoid the typos/invalid address issue but also help the store owner to target the cities for shipping rates and cart rules.

## Key Features
* Manage regions/provinces/states & cities easily via backend UI
* Ability to bulk import regions & cities via CSV file
* Ability to export regions & cities as a CSV file
* Display city as a dropdown field in the storefront (checkout shipping/billing address & customer address book)
* Display city as a dropdown field in the backend (customer edit address, edit order shipping/billing address & create new order shipping/billing address)

## Feature Highlights

### Easier Management of Regions & Cities
With this extension, store admin can perform the following actions on the entities  
* Add new region/city
* Edit existing region/city
* Delete existing region/city
* Bulk update/delete regions/cities
* Bulk import regions/cities
* Export regions/cities data
* Manage locale-based names

![Magento 2 Region Manager](https://www.magepsycho.com/media/catalog/product/3/_/3.1-m2-region-city-dropdown-manage-regions-listing-actions.png)

![Magento 2 City Manager](https://www.magepsycho.com/media/catalog/product/7/_/7.1-m2-region-city-dropdown-manage-cities-listing-actions.png)

### Export of Regions & Cities
You can easily export all or filtered regions & cities data as a CSV from backend UI.

![Magento 2 Region Export as CSV](https://www.magepsycho.com/media/catalog/product/m/2/m2-region-export.png)

![Magento 2 City Export as CSV](https://www.magepsycho.com/media/catalog/product/m/2/m2-city-export.png)

### Import of Regions & Cities
In case if you have lots of regions/cities to be added in the system, adding them one-by-one is a tedious task.
With this extension, you can easily download the sample CSV file (or export the existing data), prepare the CSV file, and perform the bulk update.

![Magento 2 Region CSV Import](https://www.magepsycho.com/media/catalog/product/5/-/5-m2-region-city-dropdown-bulk-import-regions.png)

![Magento 2 City CSV Import](https://www.magepsycho.com/media/catalog/product/9/-/9-m2-region-city-dropdown-bulk-import-cities.png)

*You can also import locale name(s) for regions & cities in the single go*

**Supported Countries**  
Currently, we have ready-made CSV for regions & cities (with locale name) for the following countries
* United Arab Emirates (UAE)
* ...

### Display City as a Dropdown Select
This extension converts text-input city field to the select dropdown in checkout address (shipping & billing) & customer address pages for both storefront and backend.

![Magento 2 City Dropdown in Checkout Address Page](https://www.magepsycho.com/media/catalog/product/2/0/20-m2-region-city-manager-frontend-checkout-shipping-city-dropdown.png)

![Magento 2 City Dropdown in Customer Edit Address Page](https://www.magepsycho.com/media/catalog/product/2/2/22-m2-region-city-manager-frontend-my-account-address-city-dropdown.png)

![Magento 2 City Dropdown in Admin Customer Edit Page](https://www.magepsycho.com/media/catalog/product/2/3/23-m2-region-city-manager-admin-customer-address-city-dropdown.png)

![Magento 2 City Dropdown in Order Edit Shipping/Billing Address Page](https://www.magepsycho.com/media/catalog/product/2/4/24-m2-region-city-manager-admin-order-details-shipping-billing-city-dropdown.png)

![Magento 2 City Dropdown in New Order Shipping/Billing Address](https://www.magepsycho.com/media/catalog/product/2/5/25-m2-region-city-manager-admin-new-order-shipping-billing-city-dropdown.png)

#### Search Option in Dropdown
The city dropdown is also configurable to have the search box inside the dropdown that can be very handy to the users if the list is big.

![Magento 2 City Dropdown with Search Option](https://www.magepsycho.com/media/catalog/product/2/0/20.2.1-m2-region-city-manager-frontend-checkout-city-dropdown-with-search.png)

![Magento 2 City Dropdown with Search Option - Multilocale](https://www.magepsycho.com/media/catalog/product/2/0/20.2.2-m2-region-city-manager-frontend-checkout-city-dropdown-with-search-arabic-locale.png)

Having city as a dropdown field can have the following advantages for the store:

* Eliminates typos, reduces the entry of incorrect addresses
* Effortless selection of regions/cities for customers
* Can be used in the shipping fee calculator
* Can be used as a shopping condition for the cart rules
* Easier to restrict shipping based on cities

### Support for Multi-Locales
If you have multiple stores with different locales, you can easily manage region & city names based on locales.

*Multi-locale values are also supported by import/export functionality of regions & cities*

In the storefront, the region & city names will be shown as per the locale

![Magento 2 Region/City Multi-Locale Add/Edit](https://www.magepsycho.com/media/catalog/product/8/-/8-m2-region-city-dropdown-add-edit-city.png)

![Magento 2 Region/City Multi-Locale Dropdown](https://www.magepsycho.com/media/catalog/product/2/0/20.1-m2-region-city-manager-frontend-checkout-shipping-city-dropdown-multi-locale.png)


## Installation
1. Download the extension .zip file and extract the files.
1. Copy the extension files from src/ folder to the {magento2-root-dir}/
1. Run the following series of command from SSH console of your server:
```
php bin/magento module:enable MagePsycho_RegionCityPro --clear-static-content
php bin/magento setup:upgrade
```
1. Flush the store cache
```
php bin/magento cache:flush
```
1. Deploy static content - *in Production mode only*
```
rm -rf pub/static/* var/view_preprocessed/*
php bin/magento setup:static-content:deploy
```
1. Go to Admin > STORES > Region & City Manager > Here you can manage regions & cities and configure settings

## Live Demo:

* [Backend Demo](http://m2default.mage-expo.com/admin_m2demo/?module=regioncitypro)
* [Frontend Demo](http://m2default.mage-expo.com/)

## Changelog
**Version 1.0.3 (2021-02-05)**
    
* Added searchable option for city dropdown

**Version 1.0.2 (2020-11-20)**
    
* Fixed `di:compile` issue
* Added Tested compatibility against Magento `v2.4.1`

**Version 1.0.1 (2020-09-19)**
    
* Fixed "Trying to access array offset on value of type bool" issue in `PHP 7.4`
* Fixed Fixed city data not copying issue when guest user is converted to customer
* Fixed Fixed the table prefix issue in regions & cities import
* Fixed Fixed the ACL issue
* Fixed Fixed the city sorting issue in drodpdown
* Added Tested compatibility against Magento `v2.4.0`

**Version 1.0.0 (2020-07-20)**
    
* Initial Release.
