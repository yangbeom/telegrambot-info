Telegrambot info
================

텔레그램봇을 만들며 알게 된 것들을 적는 문서입니다.

Telegrambot API 사용하기
------------------------
`https://api.telegram.org/bot<token>/METHOD_NAME` 으로 사용이 가능합니다.
    
    URL query string
    application/x-www.form-urlencoded
    application/json(파일 업로드 제외)
    multipart/form-data(파일 업로드시)

WebHook을 설정 한뒤
-------------------
기본 메세지는 다음과 같은 JSON 형식으로 받게 됩니다.

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

inline메세지는 다음과 같은 JSON 형식으로 받게 됩니다.

.. code-block:: python

    {'update_id': (int), 'inline_query': {'offset': (string), 
                                          'from': {'first_name': (string), 
                                                   'username': (string), 
                                                   'id': (int)}, 
                                          'query': (string), 
                                          'id': (string)}}

Bot을 block한 사용자에게 메세지를 보낼때
----------------------------------------

403에러를 return해줍니다.
