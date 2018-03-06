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

##### Store URLs   

Magento использует переменные для определения внутренних ссылок по отношению к базовому URL, что позволяет перемещать 
целое хранилище с одного URL на другой без необходимости обновлять внутренние ссылки.      

По умолчанию целевая страница для базового URL - это «cms». 

Настроить base URL можно:  `System > Configuration > GENERAL > Web`

Настроить Admin URL можно через панель администратора: `System > Configuration > ADVANCED > Admin`,
или альтернативным методом: 
1. Поменять `# <frontName><![CDATA[admin]]></frontName>` в `app/etc/local.xml`.
2. Отчистить кеш: `System > Cache Management , click the Flush Magento Cache`
                                            
          
### Industry Compliance

The Payment Card Industry (PCI) - установила набор требований для предприятий, 
которые принимают платежи с помощью кредитной карты через Интернет.

Отредактировать текст Privacy policy: `CMS > Pages > Manage Content`.

##### Cookie Law Compliance

Методы получения согласия клиентов:
* __Implied Consent__. Означает, что посетители магазина четко понимают, что файлы cookie являются необходимой частью операций,
 и с помощью вашего сайта косвенно давали разрешение на их использование.
* __Expressed Consent__. Означает, что посетители должны выразить свое согласие до того, как файлы cookie будут сохранены компьютерах. 
Если согласие не предоставлено, многие функции магазина будут недоступны, например Google Analytics.

##### Cookie Restriction Mode

Настроить можно в `System > Configuration > GENERAL > Web > Session Cookie Management`

Чтобы файлы cookie были доступны в любом месте сайта, нужно ввести `/` в `Cookie Path`.

Отредактировать текст Cookie Restriction Mode - `CMS > Static Blocks, find the Cookie Restriction Notice`.

Отредактировать текст Privacy Policy - `CMS > Pages > Manage Content, find the Privacy Policy`.

##### Cookie Reference

Magento Standard Cookies
<table>
  <tr>
    <th>COOKIE NAME</th>
    <th>COOKIE DESCRIPTION</th> 
  </tr>
  <tr>
    <td>USER_ALLOWED_SAVE_COOKIE</td>
    <td>Указывает, разрешено ли клиенту использовать файлы cookie.</td> 
  </tr>
  <tr>
    <td>external_no_cache</td>
    <td>Флаг, указывающий, отключено ли кэширование.</td> 
  </tr>
  <tr>
    <td>persistent_shopping_cart</td>
    <td>Ключ сессии</td> 
  </tr>
  <tr>
    <td>Stf</td>
    <td>Если ссылки на продукты были отправлены друзьям, 
    они сохраняют временные метки в формате: $ timeStamp1, $ timestamp2, ..., $ timestampN
    </td> 
   </tr>
  <tr>
    <td>pollN</td>
    <td>Идентификатор опроса, который указывает, произошло ли голосование.</td> 
  </tr>
  <tr>
    <td>frontend</td>
    <td>ID сессии</td> 
  </tr>
  <tr>
    <td>guest-view</td>
    <td>Позволяет гостям редактировать свои заказы.</td> 
  </tr>
</table>


Magento Cookies Used with Full Page Cache
<table>
  <tr>
    <th>COOKIE NAME</th>
    <th>COOKIE DESCRIPTION</th> 
  </tr>
  <tr>
    <td>CUSTOMER</td>
    <td>Хеширование значения ID клиента в формате: customer_$customerId</td>                                          
  </tr>
  <tr>
    <td>CUSTOMER_INFO</td>
    <td>Хеширование значения ID группы клиента в формате: customer_group_ $ customerGroupId</td>                                                          
  </tr>
  <tr>
    <td>NEWMESSAGE</td>
    <td>Указывает, получено ли новое сообщение.</td> 
  </tr>
  <tr>
    <td>CART</td>
    <td>Хешированное значение ID котировки в формате: $ quoteId</td> 
   </tr>
  <tr>
    <td>COMPARE</td>
    <td>ID продуктов, добавленные в продукт, сравниваются в формате:
        $ productId 1, $ productId 2, ..., productId N</td> 
  </tr>
  <tr>
    <td>POLL</td>
    <td>ID недавно опротестованного опроса.</td> 
  </tr>
  <tr>
    <td>RECENTLYCOMPARED</td>
    <td>ID продуктов недавно сравниваемых продуктов в формате:
        $ productId 1, $ productId 2, ..., productId N</td> 
  </tr>
  <tr>
    <td>WISHLIST</td>
    <td>Хешированный список продуктов, добавленных в список пожеланий, в формате:
        $ productId 1_ $ productId 2_ ..., _productId N</td> 
  </tr>
</table>


Magento Cookies Used with Full Page Cache (cont.)
<table>
  <tr>
    <th>COOKIE NAME </th>
    <th>COOKIE DESCRIPTION</th> 
  </tr>
  <tr>
    <td>WISHLIST_CNT</td>
    <td>Хешированное количество элементов в списке пожеланий клиента в
        format: wishlist_item_count_ $ productCount</td> 
  </tr>
  <tr>
    <td>CUSTOMER_AUTH</td>
    <td>Указывает, зарегистрирован ли клиент. Хешированное значение в формате:
        customer_logged_in_0 | 1</td> 
  </tr>
  <tr>
    <td>CATEGORY_INFO</td>
    <td>Сохраняет информацию о категории, чтобы страницы могли загружаться быстрее.</td> 
  </tr>
  <tr>
    <td>LAST_CATEGORY </td>
    <td>Недавно просмотренный идентификатор категории в формате: $ categoryID</td> 
   </tr>
  <tr>
    <td>VIEWED_PRODUCT_IDS</td>
    <td>Недавно просмотренные идентификаторы продуктов в формате: $ productId 1,
        $ productId 2, ..., productId N</td> 
  </tr>
  <tr>
    <td>currency </td>
    <td>Код валюты, выбранный клиентом («USD», «UAH»,
        «GBP» и т. Д.)</td> 
  </tr>
  <tr>
    <td>store</td>
    <td>Код вида магазина</td> 
  </tr>
  <tr>
    <td>NO_CACHE</td>  
    <td>Указывает, разрешено ли использование кеша.</td> 
  </tr>
  <tr>
    <td>LAST_PRODUCT</td>  
    <td>Идентификатор продукта последнего просмотренного продукта.</td> 
  </tr>
</table>


Google Analytics Cookies
<table>
  <tr>
    <th>COOKIE </th>
    <th>DESCRIPTION</th> 
  </tr>
  <tr>
    <td>_utma</td>
    <td>Различает пользователей и сеансы.</td> 
  </tr>
  <tr>
    <td>_utmb</td>
    <td>Определяет новые сеансы / посещения.</td> 
  </tr>
  <tr>
    <td>_utmc</td>
    <td>Определяет был ли пользователь в новом сеансе / посещении</td> 
  </tr>
  <tr>
    <td>_utmz</td>
    <td>Хранит источник трафика или кампанию, в которой объясняется, как пользователь достиг вашего сайта.</td> 
   </tr>
</table>
