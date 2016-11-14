Telegrambot info
================

텔레그램봇을 만들며 알게 된 것들을 적는 문서입니다.

WebHook을 설정 한뒤
-------------------
기본 메세지는 다음과 같은 JSON 형식으로 날아오게 된다.

.. code-block:: python

    {'message': {'message_id': (int), 
                 'chat': {'id': (int), 
                          'username': (string), 
                          'first_name': (string), 
                          'type': 'private'}, 
                 'date': (int), 
                 'from': {'id': (string), 
                          'username': (string), 
                          'first_name': (string)}, 
                 'text': (string)}, 
     'update_id': (int)}


