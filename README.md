## Install
クローンおよびコンパイル
```
git clone git://github.com/stanfordnlp/CoreNLP
cd CoreNLP
ant
cd classes
jar -cf ../stanford-corenlp.jar edu
```

パスの設定（OS、シェル依存。下記は一例）
```
(in $HOME/.bash_profile: export CLASSPATH="$HOME/git/CoreNLP/stanford-corenlp.jar")
```

## DocumentPreprocessor
実行
```
java edu.stanford.nlp.process.DocumentPreprocessor [OPTIONS] [file]
```

オプション例
* **-help** : 使用方法を表示
* **-printOriginalText** : 文分割した位置に改行を挿入したテキストを表示（同じ位置に改行が複数挿入される場合がある）
* **-suppressEscaping** : 文を改行、トークンをスペースで分割したテキストを表示（元のテキストにあった改行とスペースは削除される。改行の直前には、元のテキストにない文字が挿入される場合がある）