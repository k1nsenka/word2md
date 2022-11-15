word → md(実装済み) → push(実装済み) → 文章チェック，スペルチェック（未実装)までをやってくれるテンプレート

参考：https://blog.ue-y.me/word-git-textlint/

# install pandoc
$ brew install pandoc

# 構造  

|-- README.md  
|-- .gitignore  
|-- archive: 初稿，第二版などを適当に置いておくゴミ箱，**GitHubにはpushされない**  
|&emsp;&emsp;&emsp;|-- image.png   
|&emsp;&emsp;&emsp;|-- archive.docx    
|-- src: ワードファイルをマークダウンに変換する儀式を行うディレクトリ  
&emsp;&emsp;&emsp;|-- doc2md.sh  
&emsp;&emsp;&emsp;|-- markdown.md  
&emsp;&emsp;&emsp;|-- word.docx  

# 使い方
0. わーどで論文を書く
1. ファイル名をword.docxに変更
    1. ファイル名を変更したい場合は，./src/word2md.shを編集 
2. word.doxを./srcに配置 
3. $ ./docx2md.sh push　でプッシュまで行われる

### permission denied: ./docx2md.sh と言われた場合は以下を実行
$ chmod 700 ./docx2md.sh

