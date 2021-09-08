# BeautifulSoup4でスクレイピング

## task.1 BeautifulSoup4で実装

requests + BeautifulSoup4を使って課題３と全く同じツールを作りましょう。  
課題３をコピーしてそれを改造しても構いません。  
BeautifulSoup4の使い方に関しては各自調べて実装させましょう！

## task.2 マルチスレッド

マルチスレッドで高速化を図りましょう。  
ただし、スレッド数ほぼ同時に処理するわけですが、最終的に表示順を崩さないようにしましょう。  
[マルチスレッドの使い方](https://qiita.com/disk131/items/7ee924d01671f1c4d182)

## task.3 モジュール化
BeautifulSoapの処理の部分をモジュール化しましょう。  

```
common
  └ beautiful_soup.py
main.py
```

beautiful_soup.pyにクラス又は関数を作成し、BeautifulSoapの処理をそこでするようにしましょう。  
main.pyでbeautiful_soup.pyのクラス又は関数を呼び出しましょう。

モジュール化することによって一度作ってしまえば、他のプロジェクトでもそのまま使えたりするので便利です。

## task.4 seleniumとBeautifulSoup4の使い分けについて
これは課題ではなく知識です。  
基本静的なページにおいてはブラウザを立ち上げる必要がないBeautifulSoupの方が断然処理速度は速いです。  
しかしseleniumは操作が必要なときに使うことになります。（ログイン処理、Javaの操作、スクショ保存など）  
なので一つのツールの中でも自動操作が必要な箇所はselenium、URLで直接抽出できる箇所についてはBeautifulSoupと使い分けるのがよいです。
