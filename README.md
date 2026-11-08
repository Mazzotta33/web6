# Лабораторная работа 6 — Modeling Users

Методичка: `../methodical/Ch6.odt`. Ruby 3.4.11, Rails 8.1.4,
Bundler 4.0.21, SQLite в development/test.

## Запуск

Откройте терминал в папке `web6`:

```powershell
chcp 65001
rails server -p 3006
```

В браузере: **http://localhost:3006**.
Остановка сервера — Ctrl+C. `chcp 65001` включает UTF-8 для кириллицы в пути;
выполняйте один раз в новом терминале.

Если запускаете единственный проект, достаточно `rails server`:
тогда адрес будет http://localhost:3000.

## Подготовка после изменения зависимостей или в новой копии

```powershell
bundle install
rails db:prepare
rails dartsass:build
```

После изменения SCSS повторите `rails dartsass:build` или откройте второй
терминал в папке проекта и запустите `rails dartsass:watch`.

## Остальные команды

```powershell
rails test
rails console
rails dbconsole
rails routes
```

Если терминал открыт до установки Ruby, закройте и откройте его снова,
чтобы обновился PATH. Для ручного запуска `ruby bin/rails` в пути с кириллицей
сначала выполните `chcp 65001`.

Windows запускает Puma и тесты в одном процессе; настройки Linux сохранены.
База проекта: `storage/development.sqlite3`.

## Содержание главы

Модель User, миграции, валидации имени и email, нормализация email,
уникальный индекс, bcrypt, `has_secure_password` и аутентификация.
В главе 6 `/signup` остаётся заглушкой. Подробности упражнений: [docs/lab6.md](docs/lab6.md).
