# Trade Anything — Guide Page

Публичная страница мода **Trade Anything** (Hearts of Iron IV, Steam Workshop ID
`3438507431`) для GitHub Pages. Репозиторий не содержит исходников мода — только
маркетинговый/справочный материал: скриншоты, текст гайда и файл баланса.

## Структура

```
index.html                     — вся страница (RU/EN, тёмная тема, адаптив)
assets/logo.png                — миниатюра мода (favicon + логотип в шапке)
assets/Trade_Anything_Balance.xlsx — таблица весов/коэффициентов ИИ (кнопка скачивания)
assets/slides/Trade_Anything_slide_0X.png — 9 скриншотов из Workshop-презентации
```

Один файл `index.html` без сборки — чистый HTML/CSS/JS, шрифты подключены с
Google Fonts. Переключатель RU/EN работает через `data-lang` на `<html>` и
`localStorage` (сохраняет выбор языка).

## Публикация на GitHub Pages

1. Создать пустой репозиторий на GitHub (например `trade-anything-guide`).
2. Из этой папки:
   ```powershell
   git init
   git add .
   git commit -m "Initial guide page"
   git branch -M main
   git remote add origin https://github.com/<user>/trade-anything-guide.git
   git push -u origin main
   ```
3. В настройках репозитория → **Settings → Pages** → Source: `Deploy from a branch`,
   ветка `main`, папка `/ (root)`.
4. Страница появится на `https://<user>.github.io/trade-anything-guide/`.

## Обновление контента

- **Скриншоты** — заменить файлы в `assets/slides/`, сохранив имена
  `Trade_Anything_slide_01.png` … `_09.png`, либо поменять список `slides` в
  `<script>` внизу `index.html`.
- **Баланс** — перезаписать `assets/Trade_Anything_Balance.xlsx` тем же именем.
- **Текст гайда / ИИ-блок** — правится прямо в `index.html`: каждый факт продублирован
  двумя `<span data-t="ru">…</span>` / `<span data-t="en">…</span>`.
- **Steam-ссылка** — `https://steamcommunity.com/sharedfiles/filedetails/?id=3438507431`
  встречается в трёх местах (hero, футер, кнопка); при смене ID менять везде.

## Источники контента

Тексты и цифры взяты из `PLAYER_GUIDE_RU.md`, `WORKSHOP_UPDATE_RU.md` и
`WORKSHOP_DECK.html` основного репозитория мода (не включены сюда). Исходный код
мода в этот репозиторий не копировался.
