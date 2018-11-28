# OSM Ukraine blog platform

Platform for blogposting from Ukraine OSM Community

---

Цей репозиторій є місцем де зберігаються та публікуються всі статті на <https://blog.openstreetmap.org.ua/> (<https://osm-ua.github.io/blog/>).

Для того щоб розмістити ваш допис в Блозі виконайте наступні дії:

-   зробить форк цього репозиторію до власної обліковки на **github**
-   створіть нову гілку, на базі гілки `master`
-   в теці `_posts/<рік>` створіть новий файл(и) `yyyy-mm-dd-назва-українською.markdown` та/або `yyyy-mm-dd-english-name.markdown`, де `yyyy` - рік, `mm` - місяц та `dd` - день, відповідно.

Для форматування тексту використовується [розмітка markdown](https://help.github.com/articles/basic-writing-and-formatting-syntax/).

На початку файлу додайте YAML-секцію

```YAML
---
layout: "post"
title: "Заголовок статті"
date: "2018-12-01 09:12"
lang: uk
ref: "uniq-post-id"
---
```
де, відповідно:

-   **layout: "post"** - назва шаблону (залиште так як є)
-   **title: "Заголовок статті"** - вкажить в значення змінної `title` назву для вашої статті
-   **date: "2018-12-01 09:12"** - час що буде зазначений в дописі
-   **lang: uk**- зазначте код мови (`uk` - 🇺🇦, `en` - 🇬🇧)
-   **ref: "значення"** -  це унікальний ідетифікатор вашого допису. Якщо ви робити допис двома мовами він має бути однаковим і для файлу з українським текстом, так і для файлу з англійським текстом, але для відмежування від інших дописів він не повинен повторюватись в межах всього блогу.

Ви можете взяти за зразок один із вже опублікованих дописів та зробити за його прикладом.

Ви можете подивитись та перевірити як виглядає ваш допис локально. Для цього вам потрібно клонувати форк до вашого комп'ютера. Зберегти ваш допис та запустити локальний веб сервер **jekyll**. (Більш докладно про Jekyll - <https://jekyllrb.com>)

```
      git clone git@github.com:osm-ua/blog.git
      cd blog
      jekyll s
```

Після запуску **jekyll** відкрийте у вашому інтернет оглядачі посилання <http://127.0.0.1:4000>

```
Configuration file: /Path/to/your/local/folder/osm-ua/blog/_config.yml
            Source: /Path/to/your/local/folder/osm-ua/blog
       Destination: /Path/to/your/local/folder/osm-ua/blog/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.594 seconds.
 Auto-regeneration: enabled for '/Path/to/your/local/folder/osm-ua/blog'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

Перевірте чи все виглядає так як треба та зробіть коміт з вашим дописом до гілки створеної на базі `master`.

```
git branch new_post
git checkout new_post
git add .
git commit -m "commit description"
```

Замість `new_post` ви можете обрати будь-яку назву для вашої гілки.

Надішліть зміни до вашого репозиторію на **github**

```
git push
```

Перейдіть в розділ `Pull requests` у вашому ропозиторії на **github** та зробіть запит на приєднання вашого допису до блогу. Впродовж періоду розгляду можливості публікації вашого допису ви можете вносити в текст зміни та виправляти виявлені помилки.

Після узгодження з адміністратором ваш допис буде злито з гілкою `master` і після цього він з'явиться в блозі.
