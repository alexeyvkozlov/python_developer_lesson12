Файл с парсером - hh_request.py.
Результатом работы будет файл result.json.
В файле area.pkl - сохраняются названия городов с цифровыми кодами регионов.
Поиск происходит только по названию вакансии. 

В папке cats находится сервер API, написаный на фреймфорке FastAPI.
 Для запуска нужно перейти в папку в терминале и выполнить команду

```uvicorn main:app --reload```

По ссылке можно получить доступ к серверу и отправить запрос. Пример запроса:
```
import requests

res = requests.get('https://127.0.0.0:8000/cats/cats').json()
print(res)
```

Или использовать автоматически сгенерированную страницу по адресу https://127.0.0.0:8000/docs, которая позволяет
отправлять запросы к серверу.

#~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
#~~~~~~~~~~~~~~~~~~~~~~~~
cd c:\python_developer
.\pydev\Scripts\activate
#~~~~~~~~~~~~~~~~~~~~~~~~
cd c:\python_developer\lesson_12\cats
uvicorn main:app --reload