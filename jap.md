# React.js プロジェクトを TypeScript で作成する方法

このガイドでは、TypeScript を使用して新しい React.js プロジェクトを作成する手順を説明します。

## 前提条件

始める前に、以下がインストールされていることを確認してください：

- **Node.js**（バージョン14以上） - [Node.jsをダウンロード](https://nodejs.org/)
- **npm**（Node.jsに付属）または **Yarn**（オプション） - [Yarnをインストール](https://yarnpkg.com/)

Node.jsとnpmがインストールされているか確認するには、以下のコマンドを実行します：

```bash
node -v
npm -v
```

## プロジェクト作成手順

1. **ターミナルを開き**、プロジェクトを作成したいフォルダに移動します。

2. **以下のコマンドを実行して**、TypeScript を使った React.js プロジェクトを作成します：

   ```bash
   npx create-react-app my-app --template typescript
   ```

   `my-app` を希望のプロジェクト名に置き換えてください。

   Yarn を使用する場合は以下を実行します：

   ```bash
   yarn create react-app my-app --template typescript
   ```

3. **プロジェクトフォルダに移動します**：

   ```bash
   cd my-app
   ```

4. **開発サーバーを起動します**：

   ```bash
   npm start
   ```

   または Yarn を使用する場合：

   ```bash
   yarn start
   ```

   デフォルトのブラウザで `http://localhost:3000` が開き、アプリケーションが表示されます。

## プロジェクト構造

プロジェクト作成後、以下のような構造になります：

```
my-app
├── node_modules/       # 依存関係
├── public/             # 静的アセット
├── src/                # アプリケーションのソースコード
│   ├── App.css         # App コンポーネントのスタイル
│   ├── App.tsx         # TypeScript で記述されたメインの App コンポーネント
│   ├── index.css       # グローバルスタイル
│   ├── index.tsx       # アプリのエントリポイント
│   └── react-app-env.d.ts  # TypeScript 環境定義
├── package.json        # プロジェクトの依存関係とスクリプト
├── tsconfig.json       # TypeScript 設定
└── README.md           # ドキュメント
```

## プロジェクトのカスタマイズ

- 必要に応じて追加の依存関係をインストールします。例えば：

  ```bash
  npm install axios react-router-dom
  ```

  または：

  ```bash
  yarn add axios react-router-dom
  ```

- プロジェクトの要件に合わせて `tsconfig.json` 内の TypeScript 設定を更新します。

- `package.json` にカスタムスクリプトを追加して、追加のタスクを管理します。

## TypeScript の機能追加

TypeScript で新しいコンポーネントを作成するには：

1. **`src` フォルダに新しい `.tsx` ファイル**（例：`MyComponent.tsx`）を作成します。
2. コンポーネントとそのプロパティを定義します：

   ```tsx
   import React from 'react';

   interface MyComponentProps {
     title: string;
     count: number;
   }

   const MyComponent: React.FC<MyComponentProps> = ({ title, count }) => (
     <div>
       <h1>{title}</h1>
       <p>Count: {count}</p>
     </div>
   );

   export default MyComponent;
   ```

3. `App.tsx` などでコンポーネントをインポートして使用します。

## 参考資料

- [React ドキュメント](https://reactjs.org/docs/getting-started.html)
- [TypeScript ドキュメント](https://www.typescriptlang.org/docs/)
- [Create React App ドキュメント](https://create-react-app.dev/docs/adding-typescript/)

---
