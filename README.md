# 2024年度GraphQL勉強会【watnow】
## 概要
GraphQL勉強会のハンズオンで使用するサンプルリポジトリ
<br>
https://speakerdeck.com/masamichi2004/get-started-with-graphqlmian-qiang-hui-zi-liao

## 使用技術
[![My Skills](https://skillicons.dev/icons?i=typescript,nestjs,graphql,prisma,mysql)](https://skillicons.dev)

## Architecture
![GraphQL_Architecture](https://github.com/MasamichiKanakubo/my-first-nestjs/assets/133827507/f9bb52f5-3239-4e61-9036-af085d0e4ac4)

## Quick Start
### 1. リポジトリをクローンする
```bash
git clone https://github.com/masamichi2004/nestjs-graphql-study.git
cd nestjs-graphql-study
```

### 2. パッケージをインストールする
```bash
npm install
```

### 3. 環境構築する（できてない人向け）
#### HomeBrewが入ってない人向け
以下のコマンドを実行してHomeBrewをインストールします（sudoのパスワードが必要です）
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### MySQLが入ってない人向け
```bash
brew install mysql
```
インストールできたかは以下のコマンドで確認できます
```bash
brew info mysql
```

### 4. MySQLのデータベースをセットアップ
mysqlを起動
```mysql
mysql.server start
```
mysqlにログイン
```bash
 mysql -uroot
```

mydbというDBを作成
```mysql
CREATE DATABASE mydb;
```

### 5. mysqlのenv情報を.envファイルに追加
`.env.examples`のフォーマットに従ってenv情報を追加します
```env
DATABASE_URL="mysql://root:pasword@localhost:3306/mydb"
```

### 6. Prismaのマイグレーションを実行
マイグレーション＝データベースのスキーマの状態を変更する行為
```bash
npx prisma migrate dev --name post
```

### 7. サーバーを起動
```
npm run start
```

### 8. GraphQLエンドポイントにアクセス
```
localhost:3000/graphql
```
