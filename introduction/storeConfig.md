# Admin overview

## Stores Configuration

### stores > configuration

In the stores menu, the configuration option provides you various tools for configuring store behavior.

## Site, Store and View Scope

Every Adobe Commerce and Magento Open Source installation has a hierarchy of websites, stores, and store views.  
The term _scope_ determines where in the hierarchy a database entity — such as a product, attribute, or category — content element, or configuration setting applies.  
Websites, stores, and store views have one-to-many parent/child relationships. A single installation can have multiple websites, and each website can have multiple stores and store views.

*https://experienceleague.adobe.com/docs/commerce-admin/start/setup/websites-stores-views.html#scope-settings*

### Websites

Installations begins with a single website, which is called _website_ by default. You can also set a multiple websites for a single installation, each with its own IP address and domain.

### Stores

A single website can have multiple stores, each with its own main menu. The stores share the product catalog, but can have a different selection of products and design. All stores under the same website share the Admin and Checkout.

### Store View

Each store that is available to customers is presented according to a specific _view_.  
Initially a store has a single default view. Additional store views can be added to support different languages, or for other purposes. Customers can use the language chooser in the header to change the store view.

When working with websites, stores, and store views, keep the following in mind:

- Commerce instances have a Cascading model: _global -> website -> store -> store view_.
- Every website has at least one default store and a store view.
- Each store view can have a different base URL.
- The primary function of a _website_ is top-level feature configuration.
- The primary function a _store_ is root category configuration.
- The primary function of a _store view_ is translation information and currency symbol configuration.

### Scope settings

If your Adobe Commerce or Magento Open Source installation has a hierarchy of websites, stores, or views, you can set the context, or “scope” of a configuration setting to apply to a specific part of the installation. The context of many database entities can also be assigned a specific scope to determine how it is used in the store hierarchy. To learn more, see Product Scope and Price Scope.

Some configuration settings such as postal code, have a global scope because the same value is used throughout the system. The website scope applies to any stores below that level in the hierarchy, including all stores and their views. Any item with the scope of store view can be set differently for each store view, which is typically used to support multiple languages. To override the default values of configuration settings, see Changing Scope.

Unless the store is running in Single Store Mode, the scope of each configuration setting appears in small text below the field label. If your installation includes multiple websites, stores, or views, choose the Store View where the settings apply before making any changes.

- Global: System-wide settings and resources that are available throughout the installation.
- Website: Settings and resources that are limited to the current website. Each website has a default store.
- Store: Settings and resources that are limited to the current store. Each store has a default root category (main menu) and default store view.
- Store View: Setting and resources that are limited to the current store view.

![Scope Settings](https://experienceleague.adobe.com/docs/commerce-admin/assets/scope-multisite.svg?lang=en "Scope Settings diagram")

### Single Store Mode

If your Adobe Commerce or Magento Open Source installation has only a single store and store view, you can simplify the display by turning off all store view options and scope indicators. Single Store Mode is overridden if you add more store views later.

![Single Store Mode](https://experienceleague.adobe.com/docs/commerce-admin/assets/scope-single-view.svg?lang=en "Single Store Mode")

- On the _Admin_ sidebar go to Stores > Settings > Configuration
- Under _General_, scroll down to the bottom of the page and expand the _Single-Store Mode_ section.
- Set Enable Single-Store Mode to Yes.
- Click _Save Config_.
- When prompted to refresh the cache, do the following:
  - Click the Cache Management link in the system message at the top of the page.
  - Select the Page Cache checkbox.
  - With Actions set to Refresh, click Submit
