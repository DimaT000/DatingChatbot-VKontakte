# VkAPI-DatingChatbot
## Чат Бот для работы в среде Vkontakte:
### Задачи которые выполняет Бот:
1. Ищет людей, подходящих под условия, на основании информации о пользователе из VK:

* Возраст, пол, город, семейное положение.

*  Если информации недостаточно Бот дополнительно уточнит её у пользователя.

2. У тех людей, которые подошли по требованиям пользователю на основании профиля и запрошенных данных, получает топ-3 популярных фотографии профиля и отправляет их пользователю в чат вместе со ссылкой на найденного человека. Популярность определяется по количеству лайков к фото.*

3. Добавляет человека в избранный список, используя БД PostgreSQL.

4. Добавляет человека в черный список используя БД PostgreSQL.

5. Люди не повторяюся при повторном поиске.

--------
### Для работы Бота в чате в Vkontakte Вам понадобится:
1. Сообщество, от имени которого ваш бот будет общаться с пользователями ВКонтакте. 
2. Токен сообщества 
3. Токен пользователя


### Активация Бота:
1. Заполнить в файле [configdata](https://github.com/ViolinaS/VkAPI-DatingChatbot/blob/main/configdata.py): access_token(токен пользователя), postgres_password, group_id(идентификатор сообщества), group_token(токен сообщества)
2. Корректно указать путь к базе PostgreSQL, где будут созданы таблицы для работы Бота:

* заменить название базы vkinder на свою в файле [PostgreSQL](https://github.com/ViolinaS/VkAPI-DatingChatbot/blob/main/postgreSQL_db.py) или создать базу vkinder

3. Бот активируется словом "Привет" в чате ВКонтакте.
