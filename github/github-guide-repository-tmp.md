**в процессе наполнения и выяснения актуальности, корректности информации.
in the process of filling and finding out the relevance and correctness of the information.**

<br>

Если заметили ошибку или есть предложение, предложение и исправления приветствуются.
If You notice a mistake or have a suggestion, suggestions and corrections are welcome.

<br>

# GitHub - репозиторий

# Описание саздания и синхронизации локального репозитория с репозиторием GitHub

**Первое** - создать репозиторий **GitHub см. [Создание репозитория](https://docs.github.com/ru/repositories/creating-and-managing-repositories/creating-a-new-repository)**

**Второе** - создать локальный репозиторий

## Локальный репозиторий

### Linux

<br>

- **Первое** - создать директорию локального репозитория

  **пример:**

  ```bash
  mkdir "NAME-DIRECTORY"
  ```

<br>

- **Второе** - инициализировать систему контроля версий **Git** - вариант с "веткой" "main"

  <br>

  **Во избежание ошибок не инициализируйте новый репозиторий файлами README, лицензии или gitignore. Вы можете добавить эти файлы после того, как ваш проект будет отправлен на GitHub. Для получения дополнительной информации см.** **[Создание репозитория](https://docs.github.com/ru/repositories/creating-and-managing-repositories/creating-a-new-repository)**

<br>

- **Git** - краткое описание:

  **Git** является распределенной системой контроля версий (VCS - Version Control System). Он предоставляет возможность отслеживать изменения в файлах и проектах, сохранять их историю, а также совместно работать над проектами с другими разработчиками. Git позволяет эффективно управлять версиями кода, откатываться к предыдущим версиям, объединять изменения из разных веток и многое другое.
  **[git-scm.com](https://git-scm.com/)**

<br>

- **Инициализации Git-репозитория с "веткой" `main` : ввести команду `git init -b main` в директории будущего репозитория**

  <br>

  - Команда `git init -b main` создаст директорию `.git` и инициализирует пустой Git-репозиторий с "веткой" `main` в качестве основной вместо стандартной "ветки" `master`.

    <br>

    **пример:**

    <br>

    ```bash
    git init -b main
    ```

    <br>

    **вывод команды:**

    <br>

    ```bash
    Initialized empty Git repository in /NAME-DIRECTORY/.git/
    ```

<br>

#### Добавить "remote" репозиторий (репозитория GitHub)

- **ссылка на гид GitHub [Управление remote репозиториями](https://docs.github.com/ru/get-started/getting-started-with-git/managing-remote-repositories)**

<br>

- **Команда: `git remote add`**

  <br>

  **[2.5 Основы Git - Работа с удалёнными репозиториями](https://git-scm.com/book/ru/v2/%D0%9E%D1%81%D0%BD%D0%BE%D0%B2%D1%8B-Git-%D0%A0%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%81-%D1%83%D0%B4%D0%B0%D0%BB%D1%91%D0%BD%D0%BD%D1%8B%D0%BC%D0%B8-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D1%8F%D0%BC%D0%B8)**

  <br>

  **команду ввести в директории локального репозитория**
  <br>

  Команда `git remote add` добавит ссылку на "remote" репозиторий в локальный репозиторий. Это позволяет отправлять изменения из локального репозитория на "remote" сервер и получать изменения из "remote" репозитория.

  При выполнении этой команды в файл `config` в директории `.git` добавляется новая секция `[remote]`, которая содержит информацию о подключении к "remote" репозиторию.

  **Пример команды: SSH**

  ```bash
  git remote add origin git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git
  ```

  **Пример команды: HTTPS**

  ```bash
  git remote add origin https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git
  ```

  Команда `git remote add` принимает два аргумента: имя **"remote"** репозитория, например, origin; адрес **"remote"** репозитория, например, `https://github.com/GITHUB-USER-NAME/REPOSITORY.git` или `git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git`

  Дополнительные сведения об том, какой адрес следует использовать, см. в **Документации GitHub [Сведения об **remote** репозиториях](https://docs.github.com/ru/get-started/getting-started-with-git/about-remote-repositories)**

- **Команда `git remote -v`**

  Команда `git remote -v` отображает расширенную информацию об **"remote"** репозиториях, связанных с локальным репозиторием Git **и их** URL-адреса.

  **вывод команды:**

  **SSH**

  ```bash
  origin  git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git (fetch)
  origin  git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git (push)
  ```

  **HTTPS**

  ```bash
  origin  https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git (fetch)
  origin  https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git (push)
  ```

  **`(fetch)`** и **`(push)`** флаги: (`fetch` адрес для чтения) - (`push` адрес для записи)

  **`origin`** - стандартное имя для **"remote"** репозитория, связанного с локальным репозиторием Git

---

<div align="center">
<h2>Liveriden</h2>
<a href="https://github.com/liveriden" title="Liveriden">
<img alt="Liveriden logo - (Если Вы видите этот текст, это значит ссылка неработающая, если у Вас есть свободная минутка :) сообщите об этом  на электронную почту вставив ссылку страницы в письмо или опишите ситуацию.) (If You see this text, it means the link is broken, if You have a free minute :) let know by e-mail by inserting the page link in the letter or describe the situation.)" height="128" src="https://github.com/liveriden/lidev/raw/main/github-assets/image/smile-browser-image.png" width="128" />
</a>
</div>
<div align="center">

**[:octocat: Github](https://github.com/)**

</div>
<!-- liveridenʳ࿕☦ 2023-06-07 -->
