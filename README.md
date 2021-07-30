# Registration
Registration project base 📝

- [x] Spring Boot
- [x] Spring Security
- [x] Java Mail
- [x] Подтверждение почты с истечением срока

## Установка
Для запуска необходима база данных PostgreSQL. В [конфигурационном файле](https://github.com/Zera57/ServerJPA/blob/master/src/main/resources/application.properties) для подключения к БД прописать:
* Url;
* Username;
* Password;

Так же потребуется установить [SMTP-сервер](https://github.com/maildev/maildev). И прописать настройки для него в [конфигурационном файле](https://github.com/Zera57/ServerJPA/blob/master/src/main/resources/application.properties).

## Использование
Регистрация:
* POST {URL}/api/v1/registration

```
Content-Type: application/json
{
	"name": "Pringles Extra Cheese",
	"description": "Snack",
	"cost": 99,
	"count": 11
};
```

Ссылка на подтверждение приходит на почту. Через 15 минут ссылка будет неактивна.
