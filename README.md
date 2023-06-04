# Next.js に Storybook 入れる／TailwindCSS を Storybook に反映するとこまで

## ▼ 手順

1.  Next.js アプリを作成

        npx create-next-app [アプリ名]

2.  storybook をインストール & 初期セットアップ

        npx storybook@latest init

3.  TailwindCSS が storybook に反映されるようにセットアップ

        npm install --save-dev @storybook/addon-postcss

4.  .storybook/main.ts に上記アドオンを使用する旨を追記

5.  `.storybook/preview.ts` で `/src/app/globals.css` を import（TailwindCSS を Storybook に読み込む）

6.  サンプルで TailwindCSS を使用した Button コンポーネントを作成（106504ab62e25e67a4ec6532b9bee7078e3680be）

## ▼ 動作確認

    npm run storybook

http://localhost:6006/ が立ち上がる

- サイドバーの example は上記手順 2 で自動作成されたもの（あとで削除する）
- サイドバーの atoms は上記手順 4 で作ったもの（src/components/atoms/Button.stories.ts）

## ▼ 参考

https://storybook.js.org/recipes/next
https://zenn.dev/angelecho/articles/d296dea1af8a19
