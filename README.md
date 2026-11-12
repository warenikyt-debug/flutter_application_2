# Лабораторная работа № 2 «Конвертер валют»

«КОНВАЛ» — приложение на Flutter для конвертации сумм между EUR, RUB и USD. Оно получает курсы через HTTP, показывает курс и время обновления, позволяет менять валюты местами и хранит историю успешных конвертаций до закрытия приложения.

## Запуск на Android

Для сборки использовались Flutter 3.47.7 (Dart 3.13.5), Android SDK Platform 36, Build-Tools 36.0.0 и NDK 28.2.13676358. Настрой Android SDK в Android Studio, запусти эмулятор или подключи телефон с включённой USB-отладкой. [Настройка Android для Flutter](https://docs.flutter.dev/platform-integration/android/setup)

Из корня репозитория выполни следующие команды.

```shell
flutter doctor -v
flutter pub get --enforce-lockfile
flutter devices
flutter run
```

Если устройств несколько, укажи нужное командой `flutter run -d ID_УСТРОЙСТВА`. Для сборки debug APK выполни `flutter build apk --debug --no-pub`. Для загрузки курсов нужно подключение к интернету.

## Проверка приложения

Введи 100, выбери EUR → RUB и нажми «КОН». Сверь результат с курсом в карточке. Нажми «SWAP», повтори расчёт и проверь обе записи в истории. Проверь пустую сумму, отрицательную сумму и работу с выключенным интернетом.

Экран и расчёт находятся в `lib/main.dart`, сетевой запрос и разбор ответа — в `lib/services/`. [Rates By Exchange Rate API](https://www.exchangerate-api.com)
