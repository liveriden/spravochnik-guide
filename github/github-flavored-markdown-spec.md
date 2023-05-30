---
tags: [Liveriden]
source: https://github.com/liveriden
created: 2023-05-22T06:47:50.205Z
---

# Если заметили ошибку, сообщите об этом. If you notice an error, please report it.

- **инструменты онлайн - online tools**

  - [Free Markdown to HTML Converter](https://markdowntohtml.com/)
  - [commonmark.org](https://commonmark.org/help/)
  - [stackedit](https://stackedit.io/)

# GitHub Flavored Markdown Spec

**[линк-якорный - link-anchor](#линк-якорный---link-anchor)**

---

## Заголовок - Headings

- **Чтобы создать заголовок, добавьте от одного до шести символов "#" перед текстом заголовка. Количество символов "#" определяет размер заголовка.**

- **To create a title, add one to six "#" characters in front of the title text. The number of "#" characters determines the size of the header.**

```markdown
# This is an h1 tag

## This is an h2 tag

### This is an h3 tag

#### This is an h4 tag

##### This is an h5 tag

###### This is an h6 tag
```

---

## линк-якорный - link-anchor

```markdown
[линк-якорный — link-anchor](#линк-якорный---link-anchor)

# линк-якорный - link-anchor

[link](#link)␠ ␠

# link␣␣

[link I](#link-2)␣␣

# link 2␣␣

[link'I](#linkI)

# link'I

[link'I I:](#linkI-I)

# link'I I:

[link'I I: I](#linkI-I-I)

# link'I I: I

[link'I I: I I](#linkI-I-I-I)

# link'I I: I I
```

## линк по (ID-id) - link to ID

It's also possible to create named custom anchors, if for example you have a bunch of (sub-)headings with the same name. To do this with a header insert an HTML tag

HTML tag:

```html
<h4 id="login-optional-fields">Optional Fields</h4>
```

Then link to it by the ID attribute:

`[see above](#login-optional-fields)`

Also adding an anchor tag directly to the document works as well:

```html
<a id="my-anchor"></a>
```

.

.

Также возможно создавать названные пользовательские якоря, если, например, у вас есть куча (под-)заголовков с тем же именем. Чтобы сделать это с заголовком, вставьте HTML -тег

HTML -тег:

```html
<h4 id="login-optional-fields">Optional Fields</h4>
```

Затем ссылка на него по атрибуту ID:

[see above](#login-optional-fields)

пример - example

```html
[see above](#login-optional-fields)
<h4 id="login-optional-fields">Optional Fields</h4>
```

```html
<h4 id="login-optional-fields">Optional Fields</h4>
[see above](#login-optional-fields)
```

```html
[see above](#login-optional-fields-2)
<h4 id="login-optional-fields-2">Optional Fields</h4>
```

Также работает якорный тег непосредственно в документ:

[my-anchor](#my-anchor)

```html
[my-anchor](#my-anchor) <a id="my-anchor">my-anchor</a>
```

[my-anchor](#m-anchor)

```html
[my-anchor](#my-anchor) <a id="m-anchor">my anchor</a>
```

---

## Относительные ссылки - Relative links

- **[docs.github.com: syntax](https://docs.github.com/ru/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#relative-links)**

Вы можете определить относительные ссылки и пути к изображениям в отображаемых файлах, чтобы читателям было проще переходить к другим файлам в репозитории.

Относительная ссылка — это ссылка, заданная относительно текущего файла. Например, если есть файл сведений в корне репозитория и еще один файл в _docs/CONTRIBUTING.md_, относительная ссылка на _CONTRIBUTING.md_ в файле сведений может выглядеть следующим образом:

```markdown
[Contribution guidelines for this project](docs/CONTRIBUTING.md)
```

GitHub автоматически преобразует относительную ссылку или путь к изображению с учетом текущей ветви, чтобы ссылка или путь всегда работали. Путь ссылки будет относительным к текущему файлу. Ссылки, начинающиеся с `/`, будут относительными к корневому каталогу репозитория. Можно использовать любые операнды относительных ссылок, например `./` и `../`.

Относительные ссылки удобнее для пользователей, которые клонируют репозиторий. Абсолютные ссылки могут не работать в клонах репозитория. Мы рекомендуем использовать относительные ссылки на другие файлы в репозитории.

---

## Таблица - Table

```markdown
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ | :-------------: | ------------: |
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      |    centered     |           $12 |
| zebra stripes |    are neat     |        ~~$1~~ |

**двоеточия выравнивают текст**
:- выравнивание по левой стороне
-: выравнивание по правой стороне
:-: выравнивание по центру

**colons align the text**
:- alignment on the left side
-: right side alignment
:-: center alignment
```

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ | :-------------: | ------------: |
| col 3 is      | some wordy text |     **$1600** |
| col 2 is      |    centered     |           $12 |
| zebra stripes |    are neat     |        ~~$1~~ |

---


## Color Reference

```markdown
| Color         | Hex                                                              |
| ------------- | ---------------------------------------------------------------- |
| Example Color | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) #0a192f |
| Example Color | ![#f8f8f8](https://via.placeholder.com/10/f8f8f8?text=+) #f8f8f8 |
| Example Color | ![#00b48a](https://via.placeholder.com/10/00b48a?text=+) #00b48a |
| Example Color | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) #00d1a0 |
```

| Color         | Hex                                                              |
| ------------- | ---------------------------------------------------------------- |
| Example Color | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) #0a192f |
| Example Color | ![#f8f8f8](https://via.placeholder.com/10/f8f8f8?text=+) #f8f8f8 |
| Example Color | ![#00b48a](https://via.placeholder.com/10/00b48a?text=+) #00b48a |
| Example Color | ![#00d1a0](https://via.placeholder.com/10/00b48a?text=+) #00d1a0 |

---

## сноска-примечание - footnote

**сноски рендерит в нижней части документа - footnotes render at the bottom of the document** [^i]

[^i]: **сноски - footnotes render**

```markdown
Some text with a footnote. [^ii]
[^ii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iiii]
[^iiii]: The footnote.
```

Some text with a footnote. [^ii]
[^ii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iii]
[^iii]: The footnote.

Some text with a footnote. [^iiii]
[^iiii]: The footnote.

```markdown
Some text with a footnote. [^1]
[^1]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^2]
[^2]: The footnote.
```

Some text with a footnote. [^1]
[^1]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^11]
[^11]: The footnote.

Some text with a footnote. [^2]
[^2]: The footnote.

---

### linux сгенерировать структуру папок в markdown - generate folder structure in markdown

$ tree

```bash
.
├── 1.md
├── 2
│   ├── 2.md
│   └── 1.md
├── 1.md
├── 2.md
├── 3.md
├── 4.md
└── 5.md
```

```js

          userinfo       host      port
          ┌──┴───┐ ┌──────┴──────┐ ┌┴┐
  https://john.doe@www.example.com:123/forum/questions/?tag=networking&order=newest#top
  └─┬─┘   └─────────────┬────────────┘└───────┬───────┘ └────────────┬────────────┘ └┬┘
  scheme          authority                  path                  query           fragment

  ldap://[2001:db8::7]/c=GB?objectClass?one
  └┬─┘   └─────┬─────┘└─┬─┘ └──────┬──────┘
  scheme   authority   path      query

  mailto:John.Doe@example.com
  └─┬──┘ └────┬─────────────┘
  scheme     path

  news:comp.infosystems.www.servers.unix
  └┬─┘ └─────────────┬─────────────────┘
  scheme            path

  tel:+1-816-555-1212
  └┬┘ └──────┬──────┘
  scheme    path

  telnet://192.0.2.16:80/
  └─┬──┘   └─────┬─────┘│
  scheme     authority  path

  urn:oasis:names:specification:docbook:dtd:xml:4.1.2
  └┬┘ └──────────────────────┬──────────────────────┘
  scheme                    path
```
