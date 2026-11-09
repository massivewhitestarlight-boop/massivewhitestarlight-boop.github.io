# Discipline: сайт разработчика

Статичный сайт для GitHub Pages: чистые HTML и CSS, немного JS, без сборки и внешних запросов.

```
index.html  privacy.html  support.html     ← английская версия (основная, её смотрит Apple)
ru/index.html  ru/privacy.html  ru/support.html  ← русская версия
assets/style.css   assets/main.js   assets/favicon.svg
404.html   .nojekyll
```

## 1. Данные на сайте

Имя разработчика на сайте не указывается. Почта для связи: massivewhitestarlight@gmail.com, ссылка на пожертвования: Boosty. Чтобы поменять, используйте в VS Code ⇧⌘H (Replace in Files).

После релиза в `index.html` и `ru/index.html` найдите `href="#" aria-disabled="true"` и поставьте ссылку на приложение в App Store.

## 2. Посмотреть локально

Откройте `index.html` двойным кликом или выполните в терминале в этой папке:

```
python3 -m http.server 8000
```

Затем откройте http://localhost:8000. Если язык системы русский, главная сама перебросит на `/ru/`.

## 3. Опубликовать на GitHub Pages

1. На github.com создайте **публичный** репозиторий с именем `<ваш-логин>.github.io`.
2. В этой папке:
   ```
   git init
   git add .
   git commit -m "Discipline site"
   git branch -M main
   git remote add origin https://github.com/<ваш-логин>/<ваш-логин>.github.io.git
   git push -u origin main
   ```
3. Репозиторий → **Settings → Pages** → Source: *Deploy from a branch*, ветка `main`, папка `/ (root)`.
4. Через 1–2 минуты сайт появится по адресу `https://<ваш-логин>.github.io`.

## 4. Ссылки для App Store Connect

- **Privacy Policy URL:** `https://<ваш-логин>.github.io/privacy.html`
- **Support URL:** `https://<ваш-логин>.github.io/support.html`
- **Marketing URL** (необязательно): `https://<ваш-логин>.github.io/`

В разделе App Privacy при таком поведении приложения обычно отвечают **Data Not Collected**: номер штрихкода, отправленный в Open Food Facts, никак не связан с пользователем. Окончательно сверьтесь с определениями Apple на странице App Privacy Details.
