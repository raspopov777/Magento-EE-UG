### Store Admin

Настроить время обновления уведомлений:
1. System > Configuration
2. ADVANCED > System
3. Notifications

Установить "Use HTTPS to Get Feed" если используется защищенный URL

### Store Details

1. System > Configuration
2. GENERAL > General
    * __Store Information__
    * __Locale Options__ -  настройка языка, часового пояса и дней рабочей недели.
    * __State Options__ - выбрать страны в которых государство, провинция или регион являются обязательной частью почтового адреса.
    * __Countries Options__ - выбрать страну в которой находится бизнес, страны из которых принимается оплата и страны в которых почтовый код не обязателен в адресе.


  Каждый магазин может иметь до 5 различных почт: general contact, sales representative, customer support и 2 кастомных.
  
  * Настроить почты для каждого магазина - GENERAL > Store Email Addresses
  * Настроить sales representative - SALES > Sales Email.
  * Настроить Contact us - GENERAL > Contacts 
 

### Websites Stores and Views

System > Manage Stores

На одном веб-сайте может быть несколько магазинов, каждый из которых может иметь другое главное меню, выбор продукта и внешний вид.

При создании нового Website:
* name - преднзначено для внутренней ссылки, может быть доменом.
* code - используется на сервере чтобы указывать на домен.    
    
Установить языковой пакет - System > Magento Connect > Magento Connect Manager.
Изменить языковой пакет для Store View можно в locale Options 

###### Store URLs   

Magento использует переменные для определения внутренних ссылок по отношению к базовому URL, что позволяет перемещать 
целое хранилище с одного URL на другой без необходимости обновлять внутренние ссылки.      

По умолчанию целевая страница для базового URL - это «cms». 

Настроить base URL можно:  `System > Configuration > GENERAL > Web`

Настроить Admin URL можно через панель администратора: `System > Configuration > ADVANCED > Admin`,
или альтернативным методом: 
1. Поменять `# <frontName><![CDATA[admin]]></frontName>` в `app/etc/local.xml`.
2. Отчистить кеш: `System > Cache Management , click the Flush Magento Cache`
                                            
          
### Industry Compliance

