# Отчёт о тестировании KeyValidator
## Краткое описание

10.05.2021 - 10.05.2021 было проведено тестирование установки, тестирование требований, функциональное тестирование, позитивное и негативное тестирование приложения KeyValidator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* [Результат проверки на валидацию не соответствует требованиям Руководства использования ](https://github.com/kassiopea-coder/java-hw12-KeyValidator/issues/1)
* [В результате тестирования ключ невалидный , в руководстве использования указан валидным](https://github.com/kassiopea-coder/java-hw12-KeyValidator/issues/2)
* [В результате тестирования ключ валидный , в руководстве указан как невалидный](https://github.com/kassiopea-coder/java-hw12-KeyValidator/issues/4)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты*:
* ТЗ на тестирование
* Инструкция по установке OpenJDK 11
* Руководство использования приложения



В качестве тестовых данных использовались данные Руководства использования KeyValidator
Запуск осуществляется следующим образом:
```shell script
java KeyValidator 00000000-0000-0000-0000-000000000000 00000000-0000-0000-0000-000000000001
```
В результате работы вывод приложения будет выглядеть следующим образом:
```shell script
Result for 00000000-0000-0000-0000-000000000000: OK
Result for 00000000-0000-0000-0000-000000000001: FAIL
```
где `OK` означает, что ключ валидный, `FAIL` - невалидный.

* Валидные ключи: 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998, 80b427f8-92cd-3aae-ba04-3927fbe17c6, b295bc63-9f03-3b4b-af80-969b39f8c262, 387eedc6-12e9-3b32-9881-63b6b5e85317, c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180
* Невалидные ключи: 18252235-78e0-44a5-8720-556f0c7da17a, e66075b6-ddad-445e-baf6-161b3289522b, b6d53250-f07e-4352-a293-6102ddf7f1ca, c2bc778a-1cb9-46c6-b435-0489649d2a42, 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1

Тестирование производилось в следующем окружении:
*  Windows 7, 32 bit
*  Java version 11.0.11
