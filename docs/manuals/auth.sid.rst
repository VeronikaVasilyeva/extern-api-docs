auth.sid
========

Что это такое?
--------------

* Когда пользователь аутентифицируется, API аутентификации создает на сервере запись о сессии и  ставит куку auth.sid на домен kontur.ru
* Сервис по sid'у из куки получает информацию о сессии и идентификатор  пользователя. 

Есть два способа передачи auth.sid на сервер. Рекомендуется поддерживать оба способа.

HTTP-заголовок Authorization
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: http

  GET /drive/documents?skip=10&take=10
  Host: api.kontur.ru
  Accept: application/json
  Authorization: auth.sid FE6CFF8BE5E5B548AB1971874886D5C30E85D9BFA41978478FD26D5FD6B66D81  

Cookie
^^^^^^

.. code-block:: http

  GET /drive/documents?skip=10&take=10
  Host: api.kontur.ru
  Accept: application/json
  Cookie: auth.sid=FE6CFF8BE5E5B548AB1971874886D5C30E85D9BFA41978478FD26D5FD6B66D81

Примечания
^^^^^^^^^^

* Передачу через заголовок Authorization рекомендуется считать приоритетней, чем через Cookie.  
* Параметры auth.sid следует считать регистронезависимыми в каждом способе.

Как получить?
-------------

Подробно о получении auth.sid рассказано в разделе :doc:`Аутентификация </auth/index>`
