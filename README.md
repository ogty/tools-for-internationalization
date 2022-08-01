<h1 align="center">Tools for Internationalization</h1>

## ⚙️ Setup

```zsh
$ git clone https://github.com/ogty/tools-for-internationalization
$ source ./tools-for-internationalization/setup.sh
```

## 📖 Usage

```zsh
$ i18nseg [OPTIONS]
```

## 🔍 Options

```
Options:
    -f, --file FILE
                    Path to the translation file
    -l, --languages LANGUAGE ...
                    Languages to be segmented
    -b, --base_language LANGUAGE
                    Most reliable language
    -o, --output DIRECTORY
                    Path to the output directory
    -t, --table
                    Output translation table
    -n, --file_name FILE
                    Output file name
    -h, --help
                    Show this help message and exit
```

## ✏️ Example

```zsh
$ i18nseg --file ./sample/i18n.yaml --languages ja en --output ./sample/public/locales --table
```

## 🖨️ Output

<table><tr><td>Path</td><td>JA</td><td>EN</td><td>EMPTY</td></tr><tr></tr><tr></tr><tr><td>

```
header.title
```

</td><td>

```js
"タイトル"
```

</td><td>

```js
"Title"
```

</td><td>

```js
""
```

</td></tr><tr></tr><tr><td>

```
header.items
```

</td><td>

```js
[
    "ログイン",
    "会員登録",
    {
        "企業情報": [
            "ブログ",
            "採用情報",
            "会社紹介",
            "ヘルプセンター"
        ]
    }
]
```

</td><td>

```js
[
    "Log in",
    "Sign up",
    {
        "Company": [
            "Blog",
            "Careers",
            "Our story",
            "Help Center"
        ]
    }
]
```

</td><td>

```js
[
    "",
    "",
    {
        "": [
            "",
            "",
            "",
            ""
        ]
    }
]
```

</td></tr><tr></tr><tr><td>

```
main.heroSentence
```

</td><td>

```js
"一人ではすごいものは完成できない。"
```

</td><td>

```js
"Nothing great is made alone."
```

</td><td>

```js
""
```

</td></tr><tr></tr><tr><td>

```
main.firstLevelComponent.secondLevelComponent
```

</td><td>

```js
[
    "ブレインストーミング",
    "デザイン",
    "ビルド"
]
```

</td><td>

```js
[
    "Brainstorm",
    "Design",
    "Build"
]
```

</td><td>

```js
[
    "",
    "",
    ""
]
```

</td></tr></table>
