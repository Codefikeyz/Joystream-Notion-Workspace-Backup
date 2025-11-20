# Налаштування середовища розробки Joystream на комп'ютері з Windows

# Налаштування середовища розробки Joystream на комп'ютері з Windows.

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled.png)

# **Постановка задачі**

Ми помітили, що у нашій спільноті Joystream багато технічно підкованих людей приєднуються до нас з комп'ютерами на базі операційної системи Windows, через відсутність у них комп'ютерів з MacOS або Unix систем вони не можуть зробити свій внесок у нашу спільноту.

# Огляд

Підготовка комп'ютера з Windows до налаштування середовища розробки Joystream. Користувачі нашої спільноти з комп'ютерами на базі операційної системи Windows зможуть приступити до роботи.

## Процеси встановлення

1. **Встановлення WSL на Windows комп'ютер**
2. Встановлення операційну систему Ubuntu на комп'ютер Windows
3. Встановлення VS Code
4. Налаштування WSL у VS Code
5. Клонування репозиторіїв Joystream pioneer із GitHub
6. Запуск Joystream Pioneer на локальному хості.

## 1. Установите WSL на Windows компьютер

Пожалуйста, следуйте этой документации, чтобы установить WSL на ваш компьютер.

[[https://docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install)] ([https://docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install))

## 1. Встановлення WSL на Windows комп'ютер

Будь ласка, дотримуйтесь цієї документації, щоб встановити WSL на ваш комп'ютер.

[[https://docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install)] ([https:// docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install))

# 2. Встановлення Ubuntu

Перейдіть до Microsoft Store і знайдіть Ubuntu.

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%201.png)

Після встановлення введіть **sudo apt update && sudo apt upgrade**, щоб завершити налаштування.

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%202.png)

# 3. Встановлення VS Code

За посиланням нижче є повний посібник зі встановлення VS Code. Будь ласка, ознайомтеся з ним і дотримуйтесь інструкцій вказаних там.

[https://code.visualstudio.com/docs/setup/windows](https://code.visualstudio.com/docs/setup/windows)

# 4. Налаштування WSL в VS Code

Відкрийте VS Code, перейдіть до пошуку розширень та знайдіть Remote WSL.

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%203.png)

Встановіть його.

Тепер закрийте VS Code та знову відкрийте.

Відкрийте вікно New WSL із VS Code та відкрийте нове вікно термінала.

- [https://github.com/Joystream/pioneer#quickstart](https://github.com/Joystream/pioneer#quickstart) **уважно ознайомтеся з цим матеріалом та спробуйте зрозуміти структуру**.

# 5. Клонування репозиторіїв Joystream pioneer з GitHub

З термінала VS Code WSL клонуйте репозиторій Joystream Pioneer

[https://github.com/Joystream/pioneer.git](https://github.com/Joystream/pioneer.git)

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%204.png)

**Це** **дуже важливий крок** після клонування. Змініть директорію на Pioneer.

Введіть yarn та enter, після успішної установки ви побачите наступне.

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%205.png)

Тепер виконайте building. Для цього закрийте код VS, перейдіть у Windows PowerShell, перейдіть в каталог Pioneer і виконайте yarn building.

## 6. Запустіть Joystream Pioneer на локальному хості.

############ Створіть файл .env і вставте наступний код #############

REACT_APP_TESTNET_NODE_SOCKET=wss://rpc.joystream.org:9944 REACT_APP_TESTNET_QUERY_NODE=https://query.joystream.org/graphql REACT_APP_TESTNET_QUERY_NODE_SOCKET=wss://query.joystream. .2=https://query.joystream.org/graphql .io/member-faucet/register

Додайте файл .env до папки Pioneer/packages/ui.

Тепер запустіть yarn

[http://localhost:8080/#/settings](http://localhost:8080/#/settings) і виберіть «Joystream-Testnet» у розкривному списку!

![Untitled](../../Past%20Bounties/Setting%20up%20Joystream%20Development%20Environment%20in%20Wi/Untitled%206.png)

Ось і все тепер ви можете почати роботу зі свого комп'ютера на Windows!

# Висновок

Навіть після цього у вас можуть виникнути незначні проблеми. Будь ласка, в першу чергу  перевірте, чи все ви зробили так як в цій інструкції. Якщо навіть після перевірки ви не зможете знайти рішення, то не соромтеся та запитуйте у спільноті.