# DAO Hibernate Security

Учебный проект по работе с базой данных через **Spring JDBC** и **NamedParameterJdbcTemplate**.
Демонстрирует полный путь от HTTP-запроса до SQL-запроса в PostgreSQL, а также базовую
аутентификацию через **Spring Security**

## Стек технологий

- **Java 17+**
- **Spring Boot 4.x**
- **Spring Data JPA** (Hibernate)
- **PostgreSQL 16**
- **SecurityFilterChain** — 
- **Maven**

## Функциональность

Приложение управляет таблицей `PERSONS` со следующими полями:

| Поле | Тип | Описание |
|---|---|---|
| `name` | String | Имя (часть составного PK) |
| `surname` | String | Фамилия (часть составного PK) |
| `age` | Integer | Возраст (часть составного PK) |
| `phone_number` | String | Телефон |
| `city_of_living` | String | Город проживания |

Доступные операции:

- Получить всех людей из указанного города
- Получить всех людей 



## Требования

Перед запуском убедитесь, что установлено:

- **JDK 17** или выше — [скачать](https://adoptium.net/)
- **Maven** (или используйте встроенный `mvnw`)

## Запуск

### 1. Клонировать репозиторий

```bash
git clone https://github.com/esemeikina-bumer/DAO_Hibernate_Security.git
cd DAO_Hibernate_Security

```
## Безопасность (Spring Security)
В проекте настроена стандартная форма логина Spring Security.

Правила доступа (см. SecurityConfig.java):

### URL	Доступ
/api/persons	Публичный (без авторизации)
Все остальные	Только после авторизации
Логин по умолчанию:

Username: user

Password: генерируется при каждом запуске и печатается в логах:


Например:


text
Using generated security password: 8f4a2b1c-9d3e-4f5a-b6c7-1e2d3f4a5b6c
💡 Пароль меняется при каждом перезапуске приложения.


Приложение поднимется на http://localhost:8080.

Публичный эндпоинт:

text
http://localhost:8080/api/persons