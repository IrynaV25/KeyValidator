# Отчёт о тестировании приложения KeyValidator

## Краткое описание

30 июля 2020г. было проведено функциональное тестирование приложения KeyValidator, а также его окружения – тестирование установки и совместимости реализации Java OpenJDK11.

На тестирование затрачено: 3 часа.

В результате тестирования выявлены следующие дефекты:
* [Появляется ошибка FAIL при вводе валидных ключей в KeyValidator](https://github.com/IrynaV25/KeyValidator/issues/1#issue-668902712).
* [Отсутствует ошибка при вводе невалидных ключей в KeyValidator](https://github.com/IrynaV25/KeyValidator/issues/2#issue-668921154).


## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* [инструкция по установке OpenJDK11](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md);
* [руководство использования KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md);
* баг-репорты;
* отчет о тестировании.

В качестве тестовых данных использовались данные, приведенные в [руководстве использования KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md).
Валидные ключи:
* Result for 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998: OK
* Result for 80b427f8-92cd-3aae-ba04-3927fbe17c6: OK
* Result for b295bc63-9f03-3b4b-af80-969b39f8c262: OK
* Result for 387eedc6-12e9-3b32-9881-63b6b5e85317: OK
* Result for c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180: OK

Невалидные ключи:
* Result for 18252235-78e0-44a5-8720-556f0c7da17a: FAIL
* Result for e66075b6-ddad-445e-baf6-161b3289522b: FAIL
* Result for b6d53250-f07e-4352-a293-6102ddf7f1ca: FAIL
* Result for c2bc778a-1cb9-46c6-b435-0489649d2a42: FAIL
* Result for 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1: FAIL

Тестирование производилось в следующем окружении:
* утройство – планшет Surface3pro;
* ОС – Windows 10 Pro, версия 1903 (64 бит);
* браузер – Google Chrome, версия 84.0.4147.105 (64 бит);
* версия Java – openjdk version "11.0.8" 2020-07-14;
* версия терминала Git Bash: mintty 3.1.6 (x86_64-pc-msys).