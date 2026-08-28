# Ad0e702Mnemonics

This README file lists mnemonic devices for the AD0-E702/711/724 certification and the companion Adobe course COM-D201 (#1063) because it requires memorizing lots of things that are hard to remember.

According to Wikipedia:
> A mnemonic device (/nəˈmɒnɪk/ nə-MON-ik) or memory device is any learning technique that aids information retention or retrieval in the human memory, often by associating the information with something that is easier to remember.

----

## 1. MAGENTO ARCHITECTURE AND CUSTOMIZATION TECHNIQUES

### 1.2 Describe the Magento directory structure

```SPLAshBoarD VanGuard```

The capital letters of the "SPLAshBoarD VanGuard" mnemonic correspond to the top-level directories of the following directory structure:  

```
denis@MacBook-Pro-2012:/var/www/ad0-e702$ tree -L 1 -d
.
├── app
├── bin
├── dev
├── generated
├── lib
├── phpserver
├── pub
├── setup
├── var
└── vendor

10 directories
```

----

### 1.3 Utilize configuration and configuration variables scope

```CRAWlSPacED Mezzanine```

The capital letters of the "CRAWlSPacED Mezzanine" mnemonic correspond to the first letter of the XML filename:  
Additionally, the first letter repeats in the following pattern, in alphabetical order: 132-322-122
(Hint: I set this number sequence as my mobile phone screen unlock pin to force myself to memorize it.)

1. `acl.xml` (A 1 time)
2. `catalog_attributes.xml` (C 3 times)
3. `etc/config.xml` <- Sets default config values in the DB table `core_config_data`
4. `crontab.xml` and `cron_groups.xml`
5. `db_schema.xml` (D 2 times)
6. `di.xml`
7. `email_templates.xml` (E 3 times)
8. `events.xml`
9. `extension_attributes.xml`
10. `menu.xml` (M 2 times) <- Adds menu items in Admin
11. `module.xml`
12. `product_options.xml` (P 2 times)
13. `product_types.xml`
14. `routes.xml` (R 1 time)
15. `sales.xml` (S 2 times)
16. `etc/adminhtml/system.xml` <- Defines configuration UI in Admin > Stores > Configuration
17. `webapi.xml` (W 2 times)
18. `widget.xml`

I kept confusing `config.xml` with `system.xml`, so ChatGPT came up with a mnemonic:  
> I'd make this one revolve around C = Content and S = Screen.  
```Config Comes first (core_config_data), System Shows.```

----

```BACkFloW Global```

The capital letters of the "BACkFloW Global" mnemonic correspond to the Magento area:  

1. adminhtml
2. frontend
3. base/global
4. crontab
5. webapi_rest
6. webapi_soap
7. graphql

----

### 1.6 Configure event observers and scheduled jobs

#### How are automatic events created, and how should they be used?

```DSL & git Commit```

The capital letters of the "DSL & git Commit" mnemonic correspond to the automatically triggered events in Magento:  

1. delete before and delete after  
   e.g.:  
   theme_delete_before  
   theme_delete_after  

2. save before and save after  
   e.g.:  
   theme_save_before  
   theme_save_after  

3. save commit after  
   e.g.:  
   theme_save_commit_after  

4. load before and load after  
   e.g.:  
   theme_load_before  
   theme_load_after  

5. clear  
   e.g.:  
   theme_clear  

----

## 2. REQUEST FLOW PROCESSING

### 2.3 Demonstrate how to use URL rewrites for a catalog product view to a different URL

```RUBiC's 404```  
The capital letters of the "RUBiC's 404" mnemonic correspond to the list of Magento routers.  

```RUSCaya Doll```  
Also, the capital letters of the "RUSCaya Doll" mnemonic (referring to a Matryoshka doll, the Russian nesting doll) correspond to the order in which the Front Controller loops through all of the available Magento routers to find a match for the request.  

1. Robots.txt  
   Magento\Robots\Controller\Router  
2) URL Rewrites  
   Magento\UrlRewrite\Controller\Router  

3) Base or Standard   
   Magento\Framework\App\Router\Base  
4) CMS  
   Magento\Cms\Controller\Router  
5) Default router, i.e., 404 Not Found  
   Magento\Framework\App\Router\DefaultRouter  

----

## The Adobe #1238 course "Exam Prep Guide for the E724 Exam" (EPG-E724)  

### Section 2: Customizations  

#### Identify the data flow in and out of Adobe SaaS services  

ChatGPT came up with a funny and easy-to-remember acronym:  
```Lazy Penguins Collect Pizza, Ship Extra Ice```  

There are seven common Adobe SaaS services:  
1. Live Search  
2. Product Recommendations  
3. Catalog Service  
4. Payment Services  
5. SaaS Data Export  
6. Experience Platform Connector  
7. Inventory Management (MSI integrations, i.e., Multi-Source Inventory integrations)  

----

## The Adobe #1063 course: "Adobe Commerce for Developers - Professional" (COM-D201)  

#### DB Indexes

The following are common Magento indices:  
1. Design Config **Grid**  
2. Customer **Grid**  
3. Category **Products**  
4. **Product** Categories  
5. **Product** Price  
6. **Product** Entity Attribute Value  
7. Stock  
8. **Catalog** Rule Product  
9. **Catalog** Product Rule  
10. **Catalog** Search  

There are 2 Grid, 4 Product, 1 Stock, 3 Catalog items in the index list.  
```The 2 GRID has 4 PRODUCTS in STOCK in the 3 CATALOGs.```  

Here's another list:  

| # | ID | Description |  
| --- | --- | --- |  
| 1 | catalogrule_product | Catalog Product Rule |  
| 2 | catalogrule_rule | Catalog Rule Product |  
| 3 | catalogsearch_fulltext | |  
| 4 | catalog_category_product | Category Product |  
| 5 | customer_grid | |  
| 6 | design_config_grid | |  
| 7 | inventory | |  
| 8 | catalog_product_category | Product Category |  
| 9 | catalog_product_attribute | Product EAV |  
| 10 | catalog_product_price | |  
| 11 | sales_order_data_exporter | |  
| 12 | sales_order_status_data_exporter | |  
| 13 | cataloginventory_stock | |  
| 14 | store_data_exporter | |  

----

#### Magento extension mechanisms in order of preference:  
1. Dependency Injection as a `type` node in di.xml, and a related constructor argument
2. Plugin (modify method behavior)
3. Observer (react to events)
4. `preference` node in di.xml to replace an entire class

Think ```DI-PLOP```

----

#### The most common events in Adobe Commerce
`controller_action_predispatch`  
`controller_action_postdispatch`  
`checkout_cart_product_add_after`  
`sales_order_place_before`  
`sales_order_place_after`  
`catalog_product_save_before`  
`catalog_product_save_after`  
`customer_register_success`  

----

## The M.academy course "Adobe Commerce Developer Professional Certification Prep (AD0-E724)"  

### Working with CLI in Magento  

- Flags for deploying static content: think `beLFAST`

```
bin/magento setup:static-content:deploy
[ -l or --language]
[ -f or --force]
[ -a or --area]
[ -s or --strategy]
[ -t or --theme]
```

----

- Flags for Cron: think `re-run in-sta`
```
bin/magento cron:
[remove]
[run --group=my_custom_group]
[install]
[status]
```

----

- Flags for the indexer:
```
bin/magento indexer:info
bin/magento indexer:status
bin/magento indexer:reindex [indexer]  
bin/magento indexer:reset [indexer]  
bin/magento indexer:show-mode [indexer]   
bin/magento indexer:set-mode [realtime/schedule indexer]   
```

----

- Flags for the caches:  

`bin/magento cache:status`
```
config                         - Configuration files
layout                         - Layout XML files
block_html                     - HTML output of blocks
collections                    - Collection data
reflection                     - API interface reflection data
db_ddl                         - Database schema
compiled_config                - Compiled configuration
eav                            - Entity attribute value data
customer_notification          - Customer notifications
graphql_query_resolver_result  - GraphQL resolver query cache
config_integration             - Integration configuration
config_integration_api         - Integration API configuration
full_page                      - Full page cache
config_webservice              - Web service configuration
translate        
```

`bin/magento cache:clean [cache-name]`

`bin/magento cache:flush`

`bin/magento cache:enable|disable [type]`
To implement caching in your class, implement the `Magento\Framework\DataObject\Identities::getIdentities()` method.  

Common cache tags:  
`cat_p_[ID]`

----

- Internationalization:  
```
bin/magento
  i18n:collect-phrases
  i18n:pack
  i18n:uninstall
```

----

### Configuration precedence  

1. environment variables as in `ENV__VAR`
2. `env.php`
3. `config.php`
4. `core_config_data` DB table
5. `config.xml`

----

### Adobe Commerce Cloud  

Adobe Commerce Cloud uses Fastly CDN, NGINX, PHP-FPM, Redis, OpenSearch, MariaDB, and RabbitMQ.  
ChatGPT came up with a great mnemonic device:  
```Fast Ninjas Prefer Red Open Markets Rapidly```  

----

### ChatGPT: Core Adobe Commerce/Magento Principles

```BEST CLOUD```

● B – Build by extending, not modifying the core.  
● E – Encapsulate behind Service Contracts (interfaces).  
● S – Separate concerns with loose coupling and dependency injection.  
● T – Think upgrades first.  
  
Then:  
● C – Configure before coding.  
● L – Leverage Cloud automation (Infrastructure as Code, CI/CD).  
● O – Optimize with caching, indexing, and stateless design.  
● U – Use APIs and SaaS services where appropriate.  
● D – Defend with secure coding practices.  
 
