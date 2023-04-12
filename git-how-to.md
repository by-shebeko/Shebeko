## How to authorise SSH key
<sub>This text was written using [GitHub Pages](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) </sub>

  **1. Авторизация**
 Ввести в терминале след команду с указанием почты:
  >ssh-keygen -t ed25519 -C "shebeko.aiu@phystech.edu"

  **2. Создание нового SSH ключа**
>Generating public/private ed25519 key pair

  **3. Ввести название файла, в который сохранится ключ. Нажмите Enter, чтобы принять предложенное название и
расположение файла по умолчанию.**
> Enter a file in which to save the key (/Users/you/.ssh/id_ed25519): [Press enter]

*Не используйте пароль при генерации ключа
> Enter passphrase (empty for no passphrase): [Press enter]
> Enter same passphrase again: [Press enter]

В папке /c/Users/Имя/.ssh переименовываем два файла в что-то удобное, например
key.

  **4. Добавление ключа на сайт**
  1) copypaste текста ключа SSH из файла
  2) в настройках пользователя (Settings) и выбрать раздел SSH and GPG keys
  3) Кликните на _New SSH key_ или _Add SSH key_.
  4) Вставить ключ из буфера обмена
  5)  Нажмите "Add SSH key". Если будет предложено, введите пароль для подтверждения 

  **5. Добавьте свой приватный ключ SSH в ssh-agent.**
  
*Если вы создали свой ключ под другим именем, замените id_ed25519 в команде именем вашего
приватного ключа.*
> $ ssh-add ~/.ssh/id_ed25519

Или добавляем ключ к агенту с помощью команды : 
> ssh-add “C:/Users/имя/.ssh/имяключа”

Для проверки наличия ключа испозуем команду
> ssh-add -l.

Вводим >git config --global user.name "Имя" и >git config --global user.email “Почта”

Устанавливаем соединение с сайтом > ssh -T git@github.com 

## How to clone repository by SSH key

**1. Code -> SSH -> copy -> Enter in terminal:**
  > git clone [copypaste]

проверить статус репозитория: 
> git status
подготовить новый файл для комита:
> git add git-how-to.md
сделать комит:
> git commit -m “initial commit”
отправить изменения на сервер:
> git push


