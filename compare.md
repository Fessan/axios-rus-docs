
## Сравнение с Fetch 

В данной заметке мы попытаюемся сравнить Axios и Fetch - два популярный способа для осуществелния HTPP запросов. Для тестов возьмем сервис [jsonplaceholder](http://jsonplaceholder.typicode.com/), который предоставляет фейковые данные для тестирования запросов к серверу в формате JSON.



### Настраиваем рабочую среду

За основу возьмем эту ссылку ```http://jsonplaceholder.typicode.com/users``` которая вернет список пользователей. Создадим папку с нашим проектом где-нибудь на компьютере(*у меня это будет D:\TEST\*).

В папке создадим файл ```index.html``` со следующей структурой
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    
    
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
    <script src="app.js"></script>
</body>
</html>
```
Установим в наш проект [Babel](http://babeljs.io/) для того чтобы иметь возхмоожность писать на современном стандарте JavaScript ES6/ES7. **Внимание!** проверьте, чтобы у вас была установлена свежая версия Node JS. Скачать можно [тут](https://nodejs.org/en/)


> Если ты, мой дорогой читатель "опытный юзер", сможешь сам все настроить, и тебя не испугаешь всякими "бабелями" 
> смело пропускай текст ниже, и скролль до главы с тестированием. :)


Итак, продолжим! Находясь в папке нашего проекта, введем к команднубю строку следующее
```
npm init
```
```
npm install --save-dev babel-core babel-cli babel-preset-env babel-preset-stage-2
```
1. инициализирует наш проект и создаст нам файл ```package.json``` с его описанием
2. установит babel вместе c необходимыми настройками
