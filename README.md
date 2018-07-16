<h1 align="center">
<a href="https://lectrum.io" target="_blank" rel="noopener noreferrer"> <img src="./static/favicon/favicon-woodsmoke.svg" alt="Lectrum favicon" width="25" /></a> F.A.Q.</h1>

<br>



<table align="center">
    <tbody>
        <tr>
            <td>
                <h3 align="center">👋🏼 Привет и добро пожаловать!</h3>
                <p>
                    🤔&nbsp;Здесь ты найдешь ответы на часто задаваемые вопросы.
                </p>
                <br>
                <p>👨🏽‍🔬&nbsp;Ответы на вопросы, а также инструкции и ссылки на полезные гайды можно найти дальше в README.md этого репозитория.</p>
            </td>
        </tr>
    <tbody>
</table>

<br>

## 📜 Содержание
<!-- TOC -->

- [🌏 Настройка окружения](#-Настройка-окружения)
    - [❓ Вопрос: как установить Node.js?](#-Вопрос-как-установить-nodejs)
    - [❓ Вопрос: как установить или обновить Git?](#-Вопрос-как-установить-или-обновить-git)
    - [❓ Вопрос: как обновить Node.js?](#-Вопрос-как-обновить-nodejs)
    - [❓ Вопрос: нужно ли запускать `npm audit fix` после установки зависимостей?](#❓-вопрос-нужно-ли-запускать-npm-audit-fix-после-установки-зависимостей)
- [🏎 Запуск и работа с проектом](#-Запуск-и-работа-с-проектом)
    - [❓ Вопрос: У меня не запускается проект. Что делать?](#-Вопрос-у-меня-не-запускается-проект-что-делать)
    - [❓ Вопрос: как остановить запущенный командой npm run start (или yarn start) проект?](#-Вопрос-как-остановить-запущенный-командой-npm-run-start-или-yarn-start-проект)
- [🥊 npm и yarn](#-npm-и-yarn)
    - [❓ Вопрос: в чём разница между npm и yarn?](#-Вопрос-в-чём-разница-между-npm-и-yarn)
    - [❓ Вопрос: что лучше — npm или yarn?](#-Вопрос-что-лучше--npm-или-yarn)
- [✏️ Качество кода: настройка редакторов и IDE](#️-Качество-кода-настройка-редакторов-и-ide)
    - [❓ Вопрос: почему редактор подсвечивает мой код?](#-Вопрос-почему-редактор-подсвечивает-мой-код)
    - [❓ Вопрос: что такое линтер?](#-Вопрос-что-такое-линтер)
    - [❓ Вопрос: как включить поддержку синтаксиса `PostCSS`?](#-Вопрос-как-включить-поддержку-синтаксиса-postcss)
    - [❓ Вопрос: что такое `Prettier`?](#-Вопрос-что-такое-prettier)
    - [❓ Вопрос: как сделать, чтобы `Prettier` и `ESLint` работали вместе?](#-Вопрос-как-сделать-чтобы-prettier-и-eslint-работали-вместе)
    - [❓ Вопрос: Как настроить `Prettier` с `ESlint`, чтобы можно было форматировать код по нажатию сочетания клавиш:](#-Вопрос-как-настроить-prettier-с-eslint-чтобы-можно-было-форматировать-код-по-нажатию-сочетания-клавиш)

<!-- /TOC -->

<br>

## 🌏 Настройка окружения

#### ❓ Вопрос: как установить Node.js?
✅ Ответ: [скачать с официального сайта](https://nodejs.org/en/) и установить последнюю версию Node.js.

<br>

#### ❓ Вопрос: как установить или обновить Git?
✅ Ответ: [скачать с официального сайта](https://git-scm.com/download/) и установить последнюю версию Git.

<br>

#### ❓ Вопрос: как обновить Node.js?
✅ Ответ: есть несколько способов, в зависимости от того, как ты устанавливал Node.js.
+ `Первый`: если ты установил Node.js установщиком с сайта, то обновить тоже нужно с помощью [установщика последней версии](https://nodejs.org/en/).
+ `Второй`: если ты установил Node.js [через `nvm`](https://github.com/creationix/nvm), то обновить тоже нужно с помощью команды `nvm install --lts --latest-npm`.

#### ❓ Вопрос: нужно ли запускать `npm audit fix` после установки зависимостей?
✅ Ответ: нет, не нужно.


<br>

---

<br>

## 🏎 Запуск и работа с проектом

#### ❓ Вопрос: У меня не запускается проект. Что делать?
✅ Ответ: есть несколько решений.

1. Посмотри консоль на наличие ошибок;
2. Прочитай текст ошибки. Чаще всего, текст ошибки сам по себе объясняет её причину.
    + Самая частая ошибка: `Error: listen EADDRINUSE 0.0.0.0:3000`. Давай разберёмся как её решить. Читаем:
        + Первое слово — `Error`, говорит о том, что это ошибка;
        + Второе слово — `listen`, говорит о том, что ошибка связана с процессом «прослушивания»;
        + Далее — `EADDRINUSE 0.0.0.0:3000`, первая часть (буквы) — это описание ошибки, вторая часть (цифры) — адрес в формате хост:порт;
        + `EADDRINUSE` — это аббревиатура. Пу сути её можно разгадать путем обычной логики:
            + `E` — означает Error, ошибка;
            + `ADDR` — сокращение от address, адрес;
            + `INUSE` — сокращение in use — в использовании.
        + Итого, можно составить заключение, что адрес `0.0.0.0:3000` чем-то используется. Webpack поднимает проект именно на этом адресе. Этот адрес уже занят каким-то процессом, поэтому — возникает ошибка;
        + **`Решение`**:
            + Найди, какие процессы твоего компьютера используют данный адрес, и выключи их;
            + Если не можешь найти эти процессией через терминал — перегрузи компьютер.

<br>

#### ❓ Вопрос: как остановить запущенный командой npm run start (или yarn start) проект?
✅ Ответ: В терминале нажми сочетание клавиш `CTRL` + `C`.

<br>

---

<br>

## 🥊 npm и yarn

#### ❓ Вопрос: в чём разница между npm и yarn?
✅ Ответ: это два разных менеджера npm-пакетов. Можно почитать об их отличиях [здесь](https://ua-blog.com/npm-vs-yarn-%D0%BA%D0%B0%D0%BA%D0%BE%D0%B9-%D0%BC%D0%B5%D0%BD%D0%B5%D0%B4%D0%B6%D0%B5%D1%80-%D0%BF%D0%B0%D0%BA%D0%B5%D1%82%D0%BE%D0%B2-%D1%81%D1%82%D0%BE%D0%B8%D1%82-%D0%B8%D1%81%D0%BF%D0%BE%D0%BB/) и [здесь](https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/).

<br>

#### ❓ Вопрос: что лучше — npm или yarn?
✅ Ответ: на этот, как и на многие другие вопросы типа «а что лучше...?», увы, ответа-серебрянной пули нет.
> У каждого пакета есть свои достоинства и недостатки. Мы используем [yarn](https://yarnpkg.com/en/docs), так как по нашему мнению он обладает более удобным и красивым интерфейсом.

<br>

---

<br>

## ✏️ Качество кода: настройка редакторов и IDE

#### ❓ Вопрос: почему редактор подсвечивает мой код?
✅ Ответ: есть несколько возможных причин.
> `Первая`: ваш редактор расценивает код как неправильный. Это может произойти, когда вы пишете разметку JSX React без поддержки вашим редактором такого синтаксиса. Чтобы включить поддержку — нужно скачать соответствующий плагин для редактора. [Вот пример](https://atom.io/packages/language-babel) такого плагина для редактора Atom.

> `Вторая`: ваш код подсвечивает линтер, указывая на стилистические ошибки.

<br>

#### ❓ Вопрос: что такое линтер?
✅ Ответ: линтер — это статический анализатор кода.
> Он сообщает разработчику о стилистических и функциональных ошибках в программном коде. Мы используем [ESLint для JavaScript](https://eslint.org/), и [stylelint для CSS](https://stylelint.io/) . Детально о том, как работает линтер на примере ESLint можно [узнать здесь](https://www.youtube.com/watch?v=hppJw2REb8g).

<br>

#### ❓ Вопрос: как включить поддержку синтаксиса `PostCSS`?
✅ Ответ: есть несколько способов для каждого редактора и IDE.
+ `WebStorm`: [следуй этому гайду](https://plugins.jetbrains.com/plugin/8578-postcss-support).

<br>

#### ❓ Вопрос: что такое `Prettier`? 
✅ Ответ: [`Prettier`](https://prettier.io/) — это интрумент для форматирования JavaScript.

<br>

#### ❓ Вопрос: как сделать, чтобы `Prettier` и `ESLint` работали вместе?
✅ Ответ: всё не так просто.
+ У `ESLint` есть настройки, по которым он проводит анализ кода и говорит вам об ошибках.
+ Пакет [`prettier-eslint-cli`](https://github.com/prettier/prettier-eslint-cli) — это интеграция `Prettier` и `ESLint`, как мостик между двумя берегами.

```
Prettier 🏖 ← мостик prettier-eslint-cli → 🏖 ESLint
```

+ То есть, чтобы `Prettier` понимал, что форматировать код нужно именно по правилам `ESLint` — нужно обязательно [использовать интеграцию `prettier-eslint-cli`](https://github.com/prettier/prettier-eslint-cli#installation).

<br>

#### ❓ Вопрос: Как настроить `Prettier` с `ESlint`, чтобы можно было форматировать код по нажатию сочетания клавиш:
✅ Ответ: есть несколько способов для каждого редактора и IDE.
+ `WebStorm`: [следуй этому гайду](https://prettier.io/docs/en/webstorm.html#using-prettier-with-eslint).
