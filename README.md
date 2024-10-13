# HTML-CSS-HandsOn
HTMLとCSSを使ったハンズオンのリポジトリです。

## 注意点
このリポジトリをフォークして各々の環境にクローンしてチュートリアルを進めてください

## 目次

1. [環境準備](#1-環境準備)
2. [HTMLの概要](#2-htmlの概要)
3. [見出しと段落を追加](#3-見出しと段落を追加)
4. [プロフィール画像を配置](#4-プロフィール画像を配置)
5. [CSSを学ぶ](#5-cssを学ぶ)
6. [画像の角を丸める](#6-画像の角を丸める)
7. [要素に枠線をつける](#7-要素に枠線をつける)
8. [コピーライト表記を追加](#8-コピーライト表記を追加)
9. [余白を設定する](#9-余白を設定する)
10. [画像やテキストを中央揃えにする](#10-画像やテキストを中央揃えにする)
11. [背景画像を追加する](#11-背景画像を追加する)
12. [GitHubへプッシュ](#12-githubへプッシュ)

## 1. 環境準備

- VSCodeをインストールし、ブラウザで確認しながらハンズオンを行います。Live Server というVScodeの拡張機能を使って確認することもできます。

## 2. HTMLの概要

### **HTMLとは？**

- `HTML (HyperText Markup Language)` は、ウェブページを作成するための基本的なマークアップ言語です。ウェブブラウザがこの言語を読み取り、ページを表示します。
- ウェブページを構造化し、文章、画像、リンク、フォームなどのコンテンツを配置するために使われます。ブラウザはHTMLを読み込んで、ユーザーが視覚的に閲覧できるページを作成します。

### **なぜHTMLが必要なのか？**

- **構造を提供する**：ウェブサイトはテキストや画像などの情報が集まったものであり、これらを整理して表示するためには、コンテンツの構造を定義する方法が必要です。HTMLはその役割を果たします。
- **検索エンジンに理解させる**：検索エンジンはウェブページの内容を正確に把握し、ユーザーが求める情報を検索結果として表示する必要があります。HTMLを使って正しくページを構造化することで、検索エンジンが内容を理解しやすくなり、SEO（検索エンジン最適化）にも効果があります。

### **タグの基本説明**

- HTMLでは、**タグ** を使って構造を定義します。各タグは次の2つの部分から成り立っています。
    - **開始タグ**：例 **`<p>`** (段落を表す)
    - **終了タグ**：例 **`</p>`** (段落の終わり)
    - タグの間にその要素の内容が入ります。例えば、次のコードは「これは段落です。」という文章を段落として表示します。
        
        ```html
        <p>これは段落です。</p>
        ```
        
- **要素**：HTMLタグはページのコンテンツを表す要素であり、以下は代表的なものです。
    - **`<h1>`**: 見出し1（最も重要な見出し）
    - **`<p>`**: 段落
    - **`<img>`**: 画像を表示
    - **`<a>`**: リンクを作成

## 3. 見出しと段落を追加

1. `index.html` を作成し、以下のコードを記述します。
    
    ```html
    <!DOCTYPE html>
    <html lang="ja">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>自己紹介サイト</title>
    </head>
    <body>
    
    </body>
    </html>
    ```
    
    - 各タグの説明
        
        ### **`<!DOCTYPE html>`**
        
        - **HTML文書の宣言`<!DOCTYPE html>`** は、このファイルがHTML5で書かれたことを宣言するもので、HTML文書の最初に書きます。これにより、ブラウザが正しくHTMLを解釈して表示する準備をします。HTML5以降、シンプルな形になっています。
        
        ---
        
        ### **`<html lang="ja">`**
        
        - **HTML要素と言語属性`<html>`** タグは、HTML文書のルート要素であり、全体を囲むもので、HTML文書の開始と終了を表します。**`lang="ja"`** という属性は、このHTMLドキュメントの言語が日本語であることを示しています。これにより、検索エンジンやスクリーンリーダーなどのツールがページの言語を理解しやすくなります。
        
        ---
        
        ### **`<head>`**
        
        - **メタデータの格納`<head>`** タグは、HTMLドキュメントのメタデータ（ページに関する情報）を含む部分です。この中にページタイトルや文字コード、外部スタイルシートやスクリプトのリンクなど、ページの表示には直接関係ないけれども重要な情報を置きます。
        
        ---
        
        ### **`<meta charset="UTF-8">`**
        
        - **文字コードの指定`<meta charset="UTF-8">`** タグは、文書の文字エンコーディングを指定します。**`UTF-8`** はほぼすべての文字（日本語を含む多言語）をサポートしており、標準的な文字エンコーディングとして使用されています。これにより、日本語の文字が正しく表示されるようになります。
        
        ---
        
        ### **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**
        
        - **画面サイズの調整`<meta name="viewport">`** タグは、ページの表示方法をモバイルデバイスに最適化するために使用します。**`content="width=device-width"`** で、デバイスの画面幅に合わせた表示を行うことを指定し、**`initial-scale=1.0`** で初期の拡大率を1倍に設定します。これにより、スマートフォンやタブレットでもページが適切に表示されるようになります。
        
        ---
        
        ### **`<title>自己紹介サイト</title>`**
        
        - **ページタイトル`<title>`** タグは、ページのタイトルを指定します。このタイトルは、ブラウザのタブに表示されるほか、検索エンジンの検索結果にも表示されます。ここでは「自己紹介サイト」と指定されているため、ブラウザのタブにその名前が表示されます。
        
        ---
        
        ### **`<body>`**
        
        - **コンテンツを表示する部分`<body>`** タグは、ページのメインコンテンツが配置される領域です。ユーザーがブラウザ上で目にする要素（テキスト、画像、リンクなど）はすべてこの **`<body>`** 内に記述されます。**`<body>`** タグの中に、**`<h1>`** や **`<p>`** などの要素を追加していきます。
        
        ---
        
        ### **`</html>`**
        
        - **HTMLドキュメントの終了`</html>`** はHTML文書の終了を示すタグです。すべてのコンテンツはこのタグの前に記述され、これ以降には何も記述しません。
    
    上記のコードを書いたら、`<body>`タグの中に`<h1>`タグと`<p>`タグを以下のように追加しましょう。
    
    ```html
    <!DOCTYPE html>
    <html lang="ja">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>自己紹介サイト</title>
    </head>
    <body>
        <h1>自己紹介</h1>
        <p>こんにちは、私はWeb開発者です。</p>
    </body>
    </html>
    ```
    
    ブラウザでどのように表示されるか確認してみましょう。
    
    <img src="https://github.com/user-attachments/assets/f8f00dea-103f-4158-b108-f11d07e75267" width=300>

    このように表示されたと思います。
    

## 4. プロフィール画像を配置

新しく`image` ディレクトリを作成します。

この画像を任意の名前を付けてダウンロードして `image` ディレクトリに移しましょう。
今回は`profile_image.png`とします。

<img src="https://github.com/user-attachments/assets/db33431b-6ba1-41a4-9d29-6a2d4476bde1" width=200>

<details>
<summary>画像を移す方法</summary>

### **方法1: ターミナルで移動させる方法**

1. **ターミナルで画像ファイルを探す**
    - まず、画像がどこにダウンロードされているかを確認します。通常は **`~/Downloads`** ディレクトリに保存されていることが多いです。
    - 以下のコマンドをターミナルで実行して、**`profile_image.png`** を探します：
        
        ```bash
        find ~/Downloads -name "profile_image.png"
        ```
        
2. **プロジェクトディレクトリに画像を移動する**
    - プロジェクトディレクトリが **`~/projects/my-website`** という名前の場合、以下のコマンドでダウンロードディレクトリから画像をプロジェクトディレクトリに移動します：
        
        プロジェクトディレクトリは `pwd` コマンドで確認できます。
        
        ```bash
        pwd
        ```
        
        このコマンドを実行すると、現在作業しているディレクトリの絶対パスが表示されます。例:
        
        ```bash
        /home/user/projects/my-website
        ```
        
        `mv`コマンドを使用して`image` ディレクトリに画像ファイルを入れるように指定してください
        
        ```bash
        mv ~/Downloads/profile_image.png ~/projects/my-website/image
        ```
        

### **方法2: VSCodeにドラッグ&ドロップする方法**

1. **画像をダウンロードディレクトリからドラッグする**
    - まず、**`profile_image.png`** がダウンロードされていることを確認します。通常、ダウンロードされたファイルは **ダウンロードフォルダ** に保存されているため、ファイルエクスプローラでそのフォルダを開きます。
2. **VSCodeに画像をドロップする**
    - VSCodeを開き、左側のエクスプローラ（ファイルビュー）に、画像をドラッグして直接ドロップします。これにより、**`profile_image.png`** がプロジェクトディレクトリに追加されます。

</details>

### **HTMLで画像を表示する**

画像がプロジェクトに移動できたら、HTMLファイルでその画像を表示するコードを<body>要素の中に追加します。

```html
<img src="./image/profile_image.png" alt="プロフィール画像">
```

- コードの説明
    
    ### **`img` タグについて**
    
    ### **1. `img` タグに終了タグがない理由**
    
    - **`img` タグは自己完結型タグ**です。これは、終了タグ（**`</img>`**）を持たないタグの一つです。**`img`** タグは単に画像を表示するだけで、内容を囲む必要がないため、終了タグが不要です。HTML5では、自己完結型タグとして次のように記述するのが一般的です：
        
        ```html
        <img src="./image/profile_image.png" alt="プロフィール画像">
        ```
        
    - この形式で、**`img`** タグは画像を表示するために必要な情報を提供しています。
    
    ### **2. `src` 属性**
    
    - **`src` (source) 属性** は、表示したい画像ファイルのパスを指定するために使用されます。パスには、絶対パスまたは相対パスを使用できます。今回の例では、画像ファイルがプロジェクト内の **`image`** フォルダに保存されているため、相対パスを使用しています：
        
        ```html
        <img src="./image/profile_image.png">
        ```
        
    
    ### **3. `alt` 属性**
    
    - **`alt` (alternative text) 属性** は、画像が表示できない場合に代わりに表示されるテキストを指定するために使います。また、スクリーンリーダーを使用している視覚障害者の方に、画像の内容を伝える役割も果たします。
        
        ```html
        <img src="./image/profile_image.png" alt="プロフィール画像">
        ```
        
    - 例として、画像が読み込めない場合、`alt="プロフィール画像"` の内容が表示されます。さらに、SEO（検索エンジン最適化）にも寄与するため、適切な`alt`テキストを記述することが推奨されます。

これで、プロフィール画像がページに表示されるようになります。

現在のディレクトリ構成

```bash
.
├── image
│   └── profile_image.png
└── index.html
```

現在の `index.html` 

```html
<!DOCTYPE html>
<html lang="ja">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>自己紹介サイト</title>
</head>
<body>
	<img src="./image/profile_image.png" alt="プロフィール画像">
	<h1>自己紹介</h1>
	<p>こんにちは、私はWeb開発者です。</p>
</body>
</html>
```

このままだと画像が大きすぎます。次の章からcssを使って調整していきます。

## 5. CSSを学ぶ

CSS (Cascading Style Sheets) は、HTMLのスタイルを指定するための言語です。ページのレイアウトやフォント、色、余白、画像のサイズ調整などを行います。CSSを使って、見た目を改善するための基本的な方法を学びます。

1. プロジェクトのルートディレクトリに **`styles.css`** という名前のファイルを作成し、次のようにHTMLファイルにリンクします。
    
    ```bash
    .
    ├── image
    │   └── profile_image.png
    ├── index.html
    └── styles.css
    ```
    
    このコードをindex.htmlの **`<head>`** タグ内に追加することで、CSSファイルをHTMLファイルに適用できます。
    
    ```html
    <link rel="stylesheet" href="styles.css">
    ```
    

## **6. 画像の角を丸める**

次に、CSSを使って画像のスタイルを変更してみましょう。今回は、画像の角を丸めて柔らかいデザインにします。

1. **`styles.css`** に以下のコードを追加します：
    
    ```css
    img {
        border-radius: 20%;
        width: 200px;
    }
    ```
    
    - **`border-radius`** プロパティは、画像の角を丸めるために使います。ここでは、画像の角を全体の20%の円弧に設定しています。
    - **`width`** プロパティを使用して、画像の幅を 200px に調整しています。
2. 保存して、ブラウザで変更が適用されているか確認しましょう。
    
    以下のように変わったかと思います。
    
    <img src="https://github.com/user-attachments/assets/e6b18002-74ea-4ed8-984e-e24f97e8e840" width=300>

## **7. 要素に枠線をつける**

次に、画像に枠線を追加して、さらにデザインを改善していきます。

1. **`styles.css`** にさらに次のコードを追加します：
    
    ```css
    img {
        border: 2px solid black;
        border-radius: 20%;
        width: 200px;
    }
    ```
    
    - **`border`** プロパティで枠線を追加しています。ここでは、2ピクセルの黒い実線枠を設定しています。
        - **`2px`**: 枠線の太さ
        - **`solid`**: 実線
        - **`black`**: 枠線の色

枠線が適用されているか、ブラウザで確認してみましょう。

以下のように枠線が追加されていれば成功です。

<img src="https://github.com/user-attachments/assets/c6f2d9e5-f279-4bce-86fa-5302bd4872c8" width=300>

## **8. コピーライト表記を追加**

次に、ページの下部にコピーライト表記を追加しましょう。HTMLの **`<footer>`** タグを使用します。

1. **`index.html`** の **`<body>`** タグ内の一番下に次のコードを追加します。
    
    ```html
    <body>
    	<img src="./image/profile_image.png" alt="プロフィール画像">
    	<h1>自己紹介</h1>
    	<p>こんにちは、私はWeb開発者です。</p>
    	<footer>&copy; 2024 Your Name</footer>
    </body>
    ```
    
    これにより、コピーライトの記号（©）と名前が表示されます。
    
2. コピーライトの見た目を調整するために、**`styles.css`** に以下のコードを追加します：
    
    ```css
    footer {
        font-size: 14px;
        color: gray;
    }
    ```
    

## **9. 余白を設定する**

画像やテキストの周りに適切な余白を設定するために、**`padding`** や **`margin`** を使います。これにより、デザインに余裕を持たせることができます。

1. **`styles.css`** に以下のようにpaddingとmarginを追加します。
    
    ```css
    body {
        padding: 16px;
    }
    
    h1 {
        margin-bottom: 16px;
    }
    
    footer {
        margin-top: 20px;
        font-size: 14px;
        color: gray;
    }
    
    img {
        width: 200px;
        border: 2px solid black;
        border-radius: 20%;
        margin-bottom: 16px;
    }
    ```
    
    - **`padding`**: ボディ全体に16ピクセルの内側余白を設定します。
    - **`margin-bottom`**: 見出しや画像の下に16ピクセルの余白を設定します。

## **10. 画像やテキストを中央揃えにする**

次に、画像やテキストを中央に配置しましょう。CSSの **`text-align`** プロパティを使用します。

1. body要素に `text-align` を追加して次のように書きます：
    
    ```css
    body {
        text-align: center;
        padding: 16px;
    }
    ```
    
    これにより、ページ全体のコンテンツが中央揃えになります。
    
    <img src="https://github.com/user-attachments/assets/0b7a0d8d-341e-4d83-9e75-57867e83bc17" width=300>
    

## **11. 背景画像を追加する**

ページに背景画像を追加して、より魅力的なデザインにしましょう。

1. **下の背景画像** をダウンロードしてプロジェクトの **`image`** ディレクトリに保存します（例: **`background.png`**）。

　

<img src="https://github.com/user-attachments/assets/4476fa33-8be3-49af-bfd1-83231574328f" width=200>

1. **`styles.css`** に以下のコードを追加します。
    
    ```css
    body {
        background-image: url('./image/background.png');
        background-size: cover;
    }
    ```
    
    - **`background-image`**: 背景画像を指定します。
    - **`background-size: cover`**: 画像をページ全体にカバーさせる設定です。
    
    <img src="https://github.com/user-attachments/assets/3bf909a6-390b-4c51-adce-f49dd6dbdef5" width=300>


<details>
<summary>コード完成形</summary>

ディレクトリ構成
```
.
├── README.md
├── image
│   ├── background.png
│   └── profile_image.png
├── index.html
└── styles.css
```


index.html: 

```html
<!DOCTYPE html>
<html lang="ja">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
	<title>自己紹介サイト</title>
</head>
<body>
	<img src="./image/profile_image.png" alt="プロフィール画像">
	<h1>自己紹介</h1>
	<p>こんにちは、私はWeb開発者です。</p>
</body>
<footer>&copy; 2024 Your Name</footer>
</html>
```

styles.css:
```css
body {
    text-align: center;
    padding: 16px;
    background-image: url('./image/background.png');
    background-size: cover;
}

h1 {
    margin-bottom: 16px;
}

footer {
    margin-top: 20px;
    font-size: 14px;
    color: gray;
}

img {
    width: 200px;
    border: 2px solid black;
    border-radius: 20%;
    margin-bottom: 16px;
}
```

</details>

## **12. GitHubへプッシュ**

完成した自己紹介サイトをGitHubにプッシュしましょう。

```bash
git add .
git commit -m "自己紹介サイトの完成"
git push origin main
```

以上で、自己紹介サイトの作成は完了です！ページの見た目を確認しながらCSSを調整したり、他のスタイルを追加したりして、自由にカスタマイズしてみましょう。
