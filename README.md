# Webpack starter kit &middot; [![Build Status](https://img.shields.io/travis/npm/npm/latest.svg?style=flat-square)](https://travis-ci.org/npm/npm) [![npm](https://img.shields.io/npm/v/npm.svg?style=flat-square)](https://www.npmjs.com/package/npm) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/your/your-project/blob/master/LICENSE)

## Developing

### Prerequisites

Для коректної роботи SASS-компілятора та інших інструментів, необхідно один раз
глобально поставити додаткові пакети, виконавши в терміналі наступні команди.
Користувачам MacOS нічого робити не потрібно.

Користувачам **Windows**, в режимі адміністратора.
[Як запустити Powershell](https://youtu.be/p2tFnxcymwk) в режимі адміністратора.

```shell
npm install --global --production windows-build-tools
```

Ось як виглядає процес успішного встановлення для користувачів **Windows**.

![Встановлення windows-build-tools](https://user-images.githubusercontent.com/1426799/45007904-bde9f280-afb4-11e8-8a35-c77dffaffa2a.gif)

Користувачам **Linux**.

```shell
sudo apt-get install gcc g++ make
```

### Setting up Dev

Для швидкого старту необхідно склонувати репозиторій.

```shell
git clone https://github.com/NataliiaLazorenko/webpack-starter-kit.git
```

Переіменувати папку збірки іменем вашого проекту.

```shell
mv webpack-starter-kit і'мя_проекту
```

Потім перейти в папку проекту.

```shell
cd і'мя_проекту
```

Знаходячись в папці проекту видалити папку `.git`, яка зв'язана з репозиторієм
збірки, виконавши наступну команду.

```shell
npx rimraf .git
```

Встановити всі залежності.

```shell
npm install
```

І запустити режим розробки.

```shell
npm start
```

У вкладці браузера перейти за адресою
[http://localhost:4040](http://localhost:4040).

### Building

Для того, щоб створити оптимізовані файли для хостингу, необхідно виконати
наступну команду.

```shell
npm run build
```

У корені проекту з'явится папка `build` зі всіма оптимізованими ресурсами.

### Deploying/Publishing

Збірка може автоматично депроїти білд на GitHub Pages віддаленого (remote)
репозиторію. Для цього необхідно у файлі `package.json` відкорегувати поле
`homepage`, замінивши ім'я користувача і репозиторія на свої.

```json
"homepage": "https://github.com/ім'я_користувача/ім'я_репозиторія"
```

Після чого в терміналі виконати наступну команду.

```shell
npm run deploy
```

Якщо немає помилок в коді і властивість `homepage` вказано вірно, запуститься
збірка проекту в продакшен, після чого вміст папки `build` буде поміщено у гілку
`gh-pages` на віддаленому (remote) репозиторію. Через певний час живу сторінку
можна буде подивитися за адресою, вказаною у відкорегованій властивості
`homepage`.
