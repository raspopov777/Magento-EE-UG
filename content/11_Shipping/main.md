### Basic Shipping Methods

Методы доставки:
* __flat rate__ (единая ставка) - фиксированная плата, которая может быть применена к каждому предмету или к каждой отправке. 
* __free shipping__. Может основываться на минимальной покупке (имеет больший приоритет если применяются оба) 
или настраиваться как правило цены корзины покупок.
* __table rates__ (таблица ставок) - позволяет настроить таблицу для расчета скорости доставки для сочетания условий.
Условия: цена, тункт отправления, пункт назначения, колл-во __(по записям Ильи в доставку может быть включен виртуальный продукт)__


### Shipping Carriers

Перевозчики:
* __UPS__.Тип `United Parcel XML` позволяет создавать метки доставки. `Shipping labels` поддерживаются только для отправок из США.
* __USPS__ - внутренняя служба доставки США.
* __FedEx__. Не предлагает внутренние поставки для стран, кроме США. За пределами США `Shipping labels` только для международных перевозок.
* __DHL__ - `Shipping labels` поддерживаются только для отправок из США.


### Shipping Labels

Этикетки могут быть созданы для регулярных доставок и для возвращаемых товаров. На этикетке дополнительно указываются:
* номер заказа Magento
* номер пакета и общее количество пакетов для отправки Magento.

При попытке распечатать этикетки доставки будет ошибка, если в `General -> Store Information` не заполнены поля.

Процесс создания этикетки - Magento связывается с перевозчиком, создает заказ в системе перевозчика и получает 
отгрузочную этикетку и номер для отслеживания для отправки.


__Signature Confirmation__
* _Not required_ - письмо с подтверждением доставки не отправляется.
* _No signature_ - письмо с подтверждением доставки отправляется, но без подписи.
* _Signature Required_ - перевозчик получает подпись получателя и предоставляет вам свою печатную копию.
* _Adult Signature Required_ - тоже самое что и предудущий пункт, только для взрослых.