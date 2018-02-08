# React Telegram Login

> A Telegram oAUth Sign-in / Log-in Component for React

## Install

```
npm install react-telegram-login
```

or

```
yarn add react-telegram-login
```

## How to use

```js
import React from 'react';
import ReactDOM from 'react-dom';
import TelegramLogin from 'react-telegram-login';

const responseTelegram = response => {
  console.log(response);
};

ReactDOM.render(
  <TelegramLogin dataOnauth={this.responseTelegram} botName="OdauBot" />,
  document.getElementById('telegramButton')
);
```

## Parameters

Telegram Scopes List: https://core.telegram.org/widgets/login

## onSuccess callback ( w/ offline false)

onSuccess callback returns a TelegramUser object which provides access
to all of the TelegramUser methods listed here: https://core.telegram.org/widgets/login.

You can also access the returned values via the following properties on the returned object.

| property name | value  |    definition    |
| :-----------: | :----: | :--------------: |
|     user      | object | user information |

You can also pass child components such as icons into the button component.

```js
<TelegramButton dataOnauth={this.handleUserInfo} botName="OdauBot" />
```

## Dev Server

```
npm run start
```

Default dev server runs at localost:8080 in browser.
You can set IP and PORT in webpack.config.dev.js

## Run Tests

```
npm run test:watch
```

## Production Bundle

```
npm run bundle
```
