# web-2d-maze-demo
自分で2D迷路を作って解くやつです

![image](https://github.com/user-attachments/assets/79da491c-3aa7-4dc3-b105-837fbc54bb5f)

https://you-sk.github.io/web-2d-maze-demo/

## 概要 📝

このウェブアプリケーションは、ユーザーがインタラクティブに2D迷路を作成・編集し、その迷路がアルゴリズムによって解かれる様子をリアルタイムで観賞できるツールです。迷路の自動生成機能も備えており、ワンクリックで複雑な迷路を作成することも可能です。

## 主な機能 🌟

-   **🎨 迷路の手動作成・編集**:
    -   マウスのクリック＆ドラッグで「壁」や「道」を自由に配置できます。
    -   任意の場所に「スタート」と「ゴール」を設定できます。

-   **🤖 迷路の自動生成**:
    -   「迷路を自動生成」ボタンを押すだけで、ランダムな迷路を生成します。
    -   スタートは左上、ゴールは右下に自動で設定されます。

-   **🧩 迷路の自動解決**:
    -   「解決！」ボタンを押すと、アルゴリズムがスタートからゴールまでの最短経路を探索します。
    -   探索の過程がアニメーションで可視化され、どのセルを調べているかが一目でわかります。

-   **⚙️ カスタマイズ可能な設定**:
    -   迷路の幅と高さを自由に変更できます。
    -   探索アニメーションの速度を調整できます。

## 使い方 🚀

### 実行方法

特別な環境構築は不要です。

1.  このリポジトリにある`index.html`をダウンロードします。
2.  そのファイルをウェブブラウザ（Google Chrome, Firefox, Edgeなど）で開きます。

これだけでアプリケーションが起動します。

### 操作手順

1.  **迷路の準備**:
    -   **自動生成する場合**: `[迷路を自動生成]`ボタンをクリックします。
    -   **手動作成する場合**:
        1.  `[手動作成用にリセット]`ボタンで盤面をクリアします。
        2.  右のツールパネルから「壁」や「道」を選択し、キャンバスに迷路を描きます。
        3.  必ず「スタート」と「ゴール」を1つずつ配置してください。

2.  **解決の実行**:
    -   `[解決！]`ボタンをクリックすると、探索アニメーションが開始されます。
    -   探索が完了すると、最短経路がハイライト表示されます。

3.  **設定の変更**:
    -   迷路のサイズや探索速度を変更したい場合は、設定欄の数値を変更し、`[サイズを適用してリセット]`ボタンを押してください。

## 使用技術 🛠️

-   **HTML5**: アプリケーションの骨格
-   **CSS3**: スタイリングとレイアウト
-   **JavaScript (ES6+)**: アプリケーションの全ロジック（DOM操作、アルゴリズム、描画）

フレームワークやライブラリは使用しておらず、いわゆる「Vanilla JS」で実装されています。

## 実装されているアルゴリズム 🧠

このアプリケーションでは、2つの主要なアルゴリズムが利用されています。

### 1. 迷路生成: 再帰的バックトラッカー法 (Recursive Backtracker)

穴掘り法とも呼ばれる、深さ優先探索（DFS）を応用したアルゴリズムです。壁で埋め尽くされた盤面からランダムに穴を掘り進めるように道を生成していくことで、必ず解が存在する複雑な迷路を作成します。

### 2. 迷路解決: 幅優先探索 (BFS: Breadth-First Search)

スタート地点から近い順に全方向へ均等に探索範囲を広げていくアルゴリズムです。重みがないグラフ（今回の迷路のようなグリッド）において、**最短経路を保証する**という特徴があります。その探索の様子が視覚的にも分かりやすいため、今回の観賞用アプリに採用しました。


## ライセンス 📜

このプロジェクトはMITライセンスの下で公開されています。
