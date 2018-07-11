### 🤔 FAQ

> Заметка: FAQ — это аббревиатура от Frequently Asked Questions (часто задаваемые вопросы).

### Вопрос: как обновить Node.js?
###### Ответ: с помощью установщика Node.js последней версии, который можно [скачать](https://nodejs.org/en/) на официальном сайте.

### Вопрос: как обновить Git?
###### Ответ: с помощью установщика Git последней версии, который можно [скачать](https://git-scm.com/download/) на официальном сайте.

### Вопрос: почему весь мой код подсвечивает редактор?
###### Ответ: возможно два варианта.
> Первый — ваш редактор расценивает код как не правильный. Это может произойти, когда вы пишете разметку JSX React без поддержки вашим редактором такого синтаксиса. Чтобы включить поддержку — нужно скачать соответствующий плагин для редактора. [Вот](https://atom.io/packages/language-babel) пример такого плагина для редактора Atom.

> Второй — ваш код посдвечивает линтер, указывая на стилистические ошибки.

### Вопрос: Что такое линтер?
###### Ответ: линтер — это статический анализатор кода.
> Он сообщает разработчику о стилистических, и функциональных ошибках в программном коде. Мы используем [ESLint](https://eslint.org/) для JavaScript, и [stylelint](https://stylelint.io/) для CSS. Детально о том, как работает линтер на примере ESLint можно узнать [здесь](https://www.youtube.com/watch?v=hppJw2REb8g).

### Вопрос: как остановить запущенный проект командой npm run start (или yarn start)?
###### Ответ: В терминале нажми сочетание клавиш CTRL+C.

