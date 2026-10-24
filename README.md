# Сайт AlkoCalk

Сайт разработчика для приложения **AlkoCalk**. Публикуется GitHub Pages
из папки `docs` этого репозитория.

Адрес: `https://takomak2012-cyber.github.io/C2H5OH/`

## Страницы

| Файл | Назначение |
| --- | --- |
| `index.html` | Главная — описание AlkoCalk, восемь режимов, кнопки загрузки |
| `privacy.html` | Политика конфиденциальности (нужна RuStore и 4PDA) |
| `download/AlkoCalk_*.apk` | Прямая загрузка сборки |
| `favicon.svg` | Иконка |

## Важно про app-ads.txt

Файл `app-ads.txt` лежит **не здесь**, а в корне домена —
`https://takomak2012-cyber.github.io/app-ads.txt`, в отдельном репозитории
`takomak2012-cyber.github.io`.

Это принципиально: стандарт IAB и Яндекс требуют, чтобы файл находился
в корне домена. Адрес сайта — подпапка `/C2H5OH/`, поэтому если положить
файл рядом со страницами, он окажется в `.../C2H5OH/app-ads.txt` и робот
Яндекса его не найдёт.

Ссылка на файл с сайта ведёт на корневой адрес, а не на подпапку.

## Обновление версии APK

В `index.html` версия упоминается в трёх местах, менять их нужно **вместе**:

1. Имя файла в кнопке: `href="download/AlkoCalk_X.YZ.apk"`
2. Атрибут `download="AlkoCalk_X.YZ.apk"` у той же кнопки
3. Текст кнопки и подпись `.dlnote` под ней

Сам файл кладётся в `docs/download/` с тем же именем.

## Настройка Pages

Репозиторий → Settings → Pages:

- Source: **Deploy from a branch**
- Branch: **main**, папка: **/docs**

## Локальная проверка

```
cd docs
python -m http.server 8000
```

Затем открыть `http://localhost:8000/`.

## Обновление

```
git add docs
git commit -m "описание"
git push
```

GitHub Pages публикует изменения примерно за минуту.
