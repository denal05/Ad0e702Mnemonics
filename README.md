# Ad0e702Mnemonics

This README file lists mnemonic devices for the AD0-E702 certification because it requires memorizing lots of things that are hard to remember.

According to Wikipedia:
> A mnemonic device (/nəˈmɒnɪk/ nə-MON-ik) or memory device is any learning technique that aids information retention or retrieval in the human memory, often by associating the information with something that is easier to remember.

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

### 1.3 Utilize configuration and configuration variables scope

```CRAWlSPacED Mezzanine```

The capital letters of the "CRAWlSPacED Mezzanine" mnemonic correspond to the first letter of the XML filename:  
Additionally, the first letter repeats in the following pattern, in alphabetical order: 132-322-122
(Hint: I set this number sequence as my mobile phone screen unlock pin to force myself to memorize it.)

1. acl.xml (A 1 time)
2. catalog_attributes.xml (C 3 times)
3. config.xml
4. crontab.xml
5. db_schema.xml (D 2 times)
6. di.xml
7. email_templates.xml (E 3 times)
8. events.xml
9. extension_attributes.xml
10. menu.xml (M 2 times)
11. module.xml
12. product_options.xml (P 2 times)
13. product_types.xml
14. routes.xml (R 1 time)
15. sales.xml (S 2 times)
16. system.xml
17. webapi.xml (W 2 times)
18. widget.xml

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

## 2. REQUEST FLOW PROCESSING

### 2.3 Demonstrate how to use URL rewrites for a catalog product view to a different URL

```RUBiC's 404```

The capital letters of the "RUBiC's 404" mnemonic correspond to the list of Magento routers:  

1. Robots.txt  
   Magento\Robots\Controller\Router  

2) URL Rewrites  
   Magento\UrlRewrite\Controller\Router  

3) Base  
   Magento\Framework\App\Router\Base  

4) CMS  
   Magento\Cms\Controller\Router  

5) Default router, i.e., 404 Not Found  
   Magento\Framework\App\Router\DefaultRouter  
