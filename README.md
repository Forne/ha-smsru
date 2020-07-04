# О плагине
Плагин для отправки сообщений в Home Assistant через сервис SMS.RU

# Установка и настройка
Для установки необходимо поместить папку smsru в /usr/share/hassio/homeassistant/custom_components и прописать в конфигурацию Home Assistant:

```yaml
notify:
  - name: smsru
    platform: smsru
    from_number: HASS
    api_key: key
```

Для получения ключа API необходимо [зарегистрироваться](http://cravs.sms.ru/) в сервисе SMS.RU.

# Использование
Вы можете использовать сервис notify.smsru для отправления SMS сообщений.

```yaml
service: notify.smsru
  message: 'тест'
  target: 
    - '+79950000000'
    - '+79190000000'
```