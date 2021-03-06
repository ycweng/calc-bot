# calc-bot
LINE Messaging APIを使って、数式の計算結果を返します。

[![Build Status](https://travis-ci.org/javecs/calc-bot.svg?branch=master)](https://travis-ci.org/javecs/calc-bot) 
[![codecov](https://codecov.io/gh/javecs/calc-bot/branch/master/graph/badge.svg)](https://codecov.io/gh/javecs/calc-bot) 
[![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/javecs/calc-bot/blob/master/LICENSE)

## 使うもの
- Kotlin 1.1
- Spring Boot 1.5.2
- [Java SDK for Messaging API BOT 1.6](https://github.com/line/line-bot-sdk-java)
- [text2expr 0.1.+](https://github.com/javecs/text2expr) 
  
## Webhook URL
- LINEの`Bot`に設定する`Webhook URL`は、サーバーのエンドポイントに`/callback`をつけます。
- 例：サーバーのエンドポイントが、`https://calc-bot.xxx.xxx/`の場合
    - Webhook URL: https://calc-bot.xxx.xxx/calcback
    
## デプロイ時のアプリ設定
- デプロイするときには、`src/main/resources/application.yml`にChannelsの情報を設定してください。
```
line.bot.channelToken: token
line.bot.channelSecret: secret
```

## 動作画面
![LINE画面](http://i.imgur.com/N8q1AGA.gif)
