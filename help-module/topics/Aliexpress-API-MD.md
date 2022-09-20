[//]: # (title: Get products API MD)

## Получить схему товара

`GET aliexpress.solution.product.schema.get`

Returns the product schema for a certain category.

The schema is a JSON object that describes the product: its fields, options and constraints. It corresponds to JSON Schema Core standard.

It allows you to simplify the process of data preparation before loading the product, because beforehand you need to collect information from several API: categories, delivery template, size tables. With the help of the product schema this data is transferred in a single format.

Then with the help of the schema you can create and edit products, as well as check the product data before sending it to AliExpress.

| Параметр                    | Тип             | Обязательный | Описание                                                                                                                                |
|-----------------------------|-----------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| aeop_a_e_product_list_query | ItemListQuery[] | Нет          | Объект.                                                                                                                                 |
| ↳ product_status_type       | string          | Да           | Статус товара на AliExpress. Может быть onSelling (В продаже), offline (Сняты с продажи), auditing (На рассмотрении) и editingRequired. |
| ↳ current_page              | int             | Нет          | Страница выдачи результатов, по умолчанию 1.                                                                                            |
| ↳ excepted_product_ids      | list            | Нет          | Список идентификаторов товаров, которые нужно исключить из ответа.                                                                      |
| ↳ off_line_time             | list            | Нет          | Для товаров в статусе offline. Сколько дней прошло с момента снятия с публикации.                                                       |
| ↳ owner_member_id           | string          | Нет          | Логин продавца-владельца товара.                                                                                                        |
| ↳ page_size                 | int             | Нет          | Число товаров на каждой странице выдачи результата.                                                                                     |
| ↳ product_id                | int             | Нет          | Идентификатор товара на AliExpress.                                                                                                     |
| ↳ product_subject           | string          | Нет          | Нечёткий поиск по английскому названию товара.                                                                                          |
| ↳ ws_display                | string          | Нет          | Причина, почему товар снят с продажи. Может быть expire_offline; user_offline, violate_offline, punish_offline и grade_offline.         |
| ↳ have_national_quote       | string          | Нет          | Есть ли у товара квота по стране: y — если да n — если нет.                                                                             |
| ↳ group_id                  | int             | Нет          | Идентификатор группы товаров.                                                                                                           |
| ↳ gmt_create_start          | date            | Нет          | Поиск товаров, созданных после указанной даты и времени в формате yyyy-MM-dd hh:mm:ss.                                                  |
| ↳ gmt_create_end            | date            | Нет          | Поиск товаров, созданных до указанной даты и времени в формате yyyy-MM-dd hh:mm:ss.                                                     |
| ↳ gmt_modified_start        | date            | Нет          | Поиск товаров, изменённых до указанной даты и времени в формате yyyy-MM-dd hh:mm:ss.                                                    |
| ↳ gmt_modified_end          | date            | Нет          | Поиск товаров, изменённых до указанной даты и времени в формате yyyy-MM-dd hh:mm:ss.                                                    |
| ↳ sku_code                  | string          | Нет          | Идентификатор экземпляра (SKU) товара: его артикул или штрихкод.                                                                        |