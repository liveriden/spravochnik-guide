# **Создать - инициализировать систему контроля версий - репозиторий Git ветка main GitHub**

## **linux**

---

### **Вариант с веткой `main`**

- **Во избежание ошибок не инициализируйте новый репозиторий файлами README, лицензии или gitignore. Вы можете добавить эти файлы после того, как ваш проект будет отправлен на GitHub. Для получения дополнительной информации см.** **[Создание репозитория](https://docs.github.com/ru/repositories/creating-and-managing-repositories/creating-a-new-repository)**

---

### 1. **Создать директорию репозитория**

- `mkdir REPOSITORY-DIRECTORY`

---

### 2. **Инициализация git с веткой main**

- **Команда: `git init -b main`**

  Команда `git init -b main` создает новый локальный репозиторий Git c веткой `main` вместо ветки `master`. Для инициализации git с веткой main ввести команду

  ```
  git init -b main
  ```

  В директории репозитория (`REPOSITORY-DIRECTORY/`) после этого будет создан новый репозиторий Git с веткой `main` в качестве основной. Если ветка `main` не существует, она будет создана автоматически, иначе текущая ветка будет переключена на `main`

- **вывод команды:**

  ```
  Initialized empty Git repository in REPOSITORY-DIRECTORY/.git/
  ```

  Эту команду можно использовать вместо команды `git init`, чтобы создать новый репозиторий с веткой `main` вместо ветки `master`.

---

### 3. **Добавление **remote** репозитория**

- **ссылка на гид GitHub [Управление **remote** репозиториями](https://docs.github.com/ru/get-started/getting-started-with-git/managing-remote-repositories)**

- **Команда:** **`git remote add`**

  вести команду в директории репозитория `/REPOSITORY-DIRECTORY`

  Команда `git remote add` добавляет **remote** репозиторий

  **Пример команды: SSH**

  ```
  git remote add origin git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git
  ```

  **Пример команды: HTTPS**

  ```
  git remote add origin https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git
  ```

  Команда `git remote add` принимает два аргумента: имя **remote** репозитория, например, origin; адрес **remote** репозитория, например, `https://github.com/GITHUB-USER-NAME/REPOSITORY.git` или `git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git`

  Дополнительные сведения об том, какой адрес следует использовать, см. в **Документации GitHub [Сведения об **remote** репозиториях](https://docs.github.com/ru/get-started/getting-started-with-git/about-remote-repositories)**

---

- **Команда `git remote -v`**

  Команда `git remote -v` отображает расширенную информацию об **remote** репозиториях, связанных с локальным репозиторием Git **и их** URL-адреса.

  **вывод команды:**

  **SSH**

  ```
  origin  git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git (fetch)
  origin  git@github.com:GITHUB-USER-NAME/REPOSITORY-NAME.git (push)
  ```

  **HTTPS**

  ```
  origin  https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git (fetch)
  origin  https://github.com/GITHUB-USER-NAME/REPOSITORY-NAME.git (push)
  ```

  **`(fetch)`** и **`(push)`** флаги: (`fetch` адрес для чтения) - (`push` адрес для записи)

  **`origin`** - стандартное имя для **remote** репозитория, связанного с локальным репозиторием Git

---

<!-- 'liveridenʳ࿕☦' -->
