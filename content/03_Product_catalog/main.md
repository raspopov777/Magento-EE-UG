
### Navigation

##### Product List Configuration
Настроить параметры отображения списка продуктов: list/grid, кол-во на странице, дефолтна сортировка, плоский каталог -  
`System > Configuration > CATALOG > Catalog > Frontend`

Подробнее о [flat catalog](main.md#flat-catalog) в CH 12.

##### Pagination Controls
Настроить - `System > Configuration > GENERAL > Design > Pagination`
* __Pagination Frame__ - кол-во ссылок которые отображаются.
* __Pagination Frame Skip__ - если нажать на `...` то перейдет в следующем наборе ссылок на позицию, значение которой указали.

##### Layered Navigation

`System > Configuration > CATALOG > Catalog > Layered Navigation`
Настроить отображение кол-ва товаров у каждого каждого атрибута, установить интервалы цен на товары.

Чтобы добавить атрибут в __Layered Navigation__, нужно: 
1. Выбрать атрибут в `Catalog > Attributes > Manage Attributes`, далее перейти в `Frontend Properties` и
настроить поля `Use In Layered Navigation` и `Use In Search Results Layered Navigation`.
2. Проверить включена ли в нужной категории __Layered Navigation__, для этого перейти в `Catalog > Manage Categories`, 
выбрать категорию и на вкладке ` Display Settings` установить в поле `Is Anchor` да.



### Categories

Установить максимальную глубину категорий в навигации - `System > Configuration > CATALOG > Catalog > Category Top Navigation`
Если значение `0`, то глубина не ограничена.

##### Hidden Categories

Чтобы сделать категорию скрытной, нужно в категории и субкатегорях:
1. На вкладке `General Information` установить:
    * `Is Active` на `No`
    * `Include in Navigation Menu` на `No`
2. На вкладке `Display Settings` установить `Is Anchor` на `No`

##### Вкладки категорий
###### General Information
<table>
  <tr>
    <th>FIELD</th>
    <th>SCOPE</th> 
    <th>DESCRIPTION</th>
  </tr>
  <tr>
    <td>Name</td>
    <td>Store view</td> 
    <td>отображается не только в навигации, но и в URL-адресе страницы категории и связанных страницах продукта.</td>
  </tr>
  <tr>
    <td>URL Key</td>
    <td>Store View</td> 
    <td>URL-адрес является относительным путем к категории и автоматически генерируется при сохранении категории. 
    Ключ URL должен быть всем строчным символом без пробелов. Как лучшая практика, каждое слово разделяется дефисом. 
    Если вы редактируете ключ URL по умолчанию, настраиваемый переадресация создается автоматически. 
    У корневой категории нет ключа URL.</td>
  </tr>
  <tr>
    <td>Page Title</td>
    <td>Store View</td> 
    <td>Лучшей практикой считается чтобы заголовок имел длину не более двенадцати слов и включал комбинацию первичных и вторичных ключевых слов.</td>
  </tr>
  <tr>
    <td>Meta Keywords</td>
    <td>Store View</td> 
    <td> Общее правило - использовать не более тридцати ключевых слов или 180 символов. Избегать повторений и пустых слов.</td>
  </tr>
</table>

###### Display Settings
<table>
  <tr>
    <th>FIELD</th>
    <th>SCOPE</th> 
    <th>DESCRIPTION</th>
  </tr>
  <tr>
    <td>Is Anchor</td>
    <td>Global</td> 
    <td>Включает "фильтр по атрибуту" в layered navigation</td>
  </tr>
  <tr>
    <td>Layered Navigation Price Step</td>
    <td>Store View</td> 
    <td>Изменить диапазон ценового шага (по умолчанию 10, 100, 1000)</td>
  </tr>
</table>

###### Custom Design
На этой вкладке можно настроить кастомную тему для категории и задать время, которое она будет действовать.

###### Category Permissions
Прежде чем назначать разрешения для определенной категории, необходимо настроить права категории для магазина в 
`System > Configuration > CATALOG > Catalog > Category Premissions`.






### Managing Attributes
### Flat Catalog
### Creating Products
### Product Images
### Swatches
### Product Pricing
### Inventory
### Product Information