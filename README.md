# (NAIST非公式) 修論・博論のTeXテンプレート

# 特徴
VSCode + Docker に最適化した修論・博論のTeXテンプレートです。  
devcontainerを使うことでVScode内で簡単にDockerを使用することができます。

# ディレクトリの構造
```bash
├── .devcontainer           
├── .vscode
├── img                        # 図など
├── mthesis.bib                # 参考文献の管理
├── mthesis.pdf                # 見本のPDFファイル
├── mthesis.tex                # メインのTeXファイル
└── tex
    ├── abstract.tex           # アブストラクト
    ├── acknowledgements.tex   # 謝辞
    ├── appendix.tex           # 付録
    ├── chapter1.tex           # 第1章
    ├── chapter2.tex           # 第2章
    ├── chapter3.tex           # 第3章
    ├── chapter4.tex           # 第4章
    ├── cmember.tex            # 主査と副査の方の名前
    └── personal_setting.tex   # 名前、学籍番号など
```

## .vscode
VScodeの設定が書いてあります。必要に応じて追記して下さい。

## .devcontainer
VSCode devcontainerの設定ファイルです。

docker imageは下記のを使用させて頂きました。  
https://hub.docker.com/r/korosuke613/ubuntu-texlive-ja-devcontainer

# LaTeX Workshop
VSCodeの拡張機能です。コンテナ立ち上げ時に自動的にインストールされます。


# コンパイル方法
## VScode
VScode LaTeX Workshopを用いることで、コンパイル、不要ファイルの削除もできます。

## Latexmk
下記のコマンドを実行でコンパイル可能。
```
latexmk
```

## make
VScode のTexWorkshopから以外にもmakeを用いてコンパイルすることもできます。

### all
ptex2pdf → pbibtex → ptex2pdf×2を実行します。
```
make all
```

### clean
不必要な関連ファイルを削除します。
```
make clean
```

# 謝辞
以下のを参考にさせて頂きました。ありがとうございます。　　
https://github.com/kmiya/naist-thesis-tmpl　　
https://github.com/sdlab-naist/mthesis-style　　

# License
The source code is licensed MIT.