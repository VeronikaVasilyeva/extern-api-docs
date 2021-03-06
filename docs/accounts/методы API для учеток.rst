.. _Accounts: http://extern-api.testkontur.ru/swagger/ui/index#/Accounts
.. _`GET All`: http://extern-api.testkontur.ru/swagger/ui/index#!/Accounts/Accounts_GetAll
.. _`POST Account`: http://extern-api.testkontur.ru/swagger/ui/index#!/Accounts/Accounts_Create
.. _`GET Account`: http://extern-api.testkontur.ru/swagger/ui/index#!/Accounts/Accounts_Get

Методы для работы с учетными записями
=====================================

Подробная спецификация методов показана в сваггере в разделе Accounts_.

Список доступных методов:

* `Получение списка всех доступных учетных записей`_
* `Создание новой учетной записи`_
* `Получение конкретной учетной записи`_

Получение списка всех доступных учетных записей
-----------------------------------------------

Метод: `GET All`_

При вызове этого метода можно получить список доступных учетных записей авторизованного пользователя. Пользователь определяется по :doc:`/manuals/auth.sid` из запроса. 

Для :doc:`Компаний-Партнеров Контура </scenarios/Компания-партнер-Контура>` и :doc:`дополнительно ещё и УЦ Контура </scenarios/Компания-партнер-УЦ-Контура>` отдельно происходит фильтрация доступных учетных записей согласно переданному в запросе :doc:`/manuals/api-key`, таким образом происходит фильтрация пользователей по продуктам.

Создание новой учетной записи
-----------------------------

Метод: `POST Account`_

С помощью данного метода есть возможность создавать новые учетные записи для пользователей сервис Компаний-Партнеров, если организации этих пользователей ещё не существуют в Контур.Экстерне.

.. important::  Доступно только для работы в сценариях :doc:`Компаний-Партнеров Контура </scenarios/Компания-партнер-Контура>` и :doc:`дополнительно ещё и УЦ Контура </scenarios/Компания-партнер-УЦ-Контура>`. 

Получение конкретной учетной записи
-----------------------------------

Метод: `GET Account`_
