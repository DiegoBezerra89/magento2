# Aplication architecture

### Websites

Websites in Magento 2 are often used to separate large business units such as different brands, business units in different countries, or unrelated product lines.  
Shipping carriers and payment gateways are each configures at website level, and base URL's can be configured at website as well.

### Stores

Stores allow you to create unique catalogs of products, one website can have many stores, and customers can add products from multiple stores into the same shopping cart

### Store View

Store views allows catalogs be displayed in different languages and currencies.

### Scopes

Application Scopes specify at which level data should be unique.

#### Global Scope

Affects everything across the Magento 2 instance, e.g. the _State Options_ setting specifies whether or not every website in your Magento 2 installation will require that customer specifies a state.

#### Website Scope

Shipping method and payment methods can be especified on the website scope level, this means that if you want to do business in markets which require different payment methods, each market will need his own website in your Magento 2 installation.

#### Store view scope

These are the most specific settings, and affect everything on a language and local level, e.g. product information is setted at store view store scope level, so that you can have a different value for a product description for different language speakers within the same region, as an example doing business on Canada, you will need two store views scopes, one to english speakers, and one for french speakers.

##### Store View Dropdown

Used to switch scopes, all data in magento 2 has a default configuration, but you can override the default configuration by specifying changes at different scope levels,
