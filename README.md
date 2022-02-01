# Mattermost
## Описание

Бот для Mattermost, выполняющий вспомогательные функции в каналах консультирования отдела поддержки и разработки Directum 5.
Возможности:
- приветственное сообщение в треде для новых участников в канале;
- автоматическое закрепление (pin) новых сообщений в канале;
- уведомление об неактивных консультациях и их автоматическое открепление (unpin);
- скачивание треда с вложениями.

## Настройка Workspace

- На странице администратора Mattermost конфигурации бота (http://your-mattermost/admin_console/integrations/bot_accounts) включить возможность создавать бота ("Enable Bot Account Creation");

- перейти на страницу интеграций команды http://your-mattermost/admin_console/integrations/bot_accounts;

- добавить новый аккаунт для бота (кнопка "Add Bot Account");

- заполнить поля, назначить боту роль member и выдать максимальные права по ней;

Внимание! При создании бота создается токен личного доступа. **Значение токена доступно только сразу после создания аккаунта бота**, поэтому требуется его сразу скопировать и сохранить. ИД токена, который всегда доступен в окне информации о боте, не эквивалентен значению токена.

- добавить бота в команды и каналы, в которых он будет использоваться.

## Настройка приложения

В файле appsettings.json заполнить следующие настройки:

- MattermostUri: Uri, где развернут Mattermost;

- BotToken: токен бота, который можно получить при создании аккаунта бота;

- BotId: id бота;

- Channels: список каналов, в которых бот будет отпинивать неактивные сообщения:
  - ChannelID: Id канала, за сообщениями которого следит бот (можно найти в свойствах канала в Mattermost); ![image](https://user-images.githubusercontent.com/58815407/151989734-4653ea23-8f9a-4bdb-828f-3fa3697d0f77.png)

  - DaysBeforeWarning: количество дней после последнего сообщения, через которое бот отправит предупреждение об неактивном треде;

  - DaysBeforeUnpining: количество дней после предупреждения, через которое бот открепит неактивный тред.

  - AutoPinMessage: автоматическое закрепление новых сообщений.
 
  - WelcomeMessage: приветственное сообщение.

## Пример

< будет позже >
