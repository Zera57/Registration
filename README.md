# Registration
Registration project base 📝

- [x] Spring Boot
- [x] Spring Security
- [x] Java Mail
- [x] Подтверждение почты с истечением срока

## Установка
Для запуска необходима база данных PostgreSQL. В [конфигурационном файле](https://github.com/Zera57/Registration/blob/master/src/main/resources/application.yml) для подключения к БД прописать:
* Url;
* Username;
* Password;

Так же потребуется установить [SMTP-сервер](https://github.com/maildev/maildev). И прописать настройки для него в [конфигурационном файле](https://github.com/Zera57/Registration/blob/master/src/main/resources/application.yml).

## Использование
Регистрация:
* POST {URL}/api/v1/registration

```
Content-Type: application/json
{
  "firstName": "Svyatoslav",
  "secondName": "Avtonomov",
  "email": "svyat@gmail.com",
  "password": "password123"
};
```

Ссылка на подтверждение приходит на почту. Через 15 минут ссылка будет неактивна.
