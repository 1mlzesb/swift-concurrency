# 正誤表

商業版、同人版の正誤表をこちらのページで記載いたします。


## 2023年9月25日

### 対象書籍

* 商業版「一冊でマスター！Swift Concurrency入門」初版発行Ver1.0
* 同人版「Swift Concurrency入門」第2版


### 修正箇所

商業版書籍25ページ、同人版書籍29ページ、「リスト2.1:データ競合」の後の文。

誤
```
③と④はそれぞれ別スレッドで同じscoreインスタンスに対してメソッドを実行します。データ競合がなければ、それぞれ渡した点数がhighScoreとして出力されるはずです。
```

正
```
③と⑤はそれぞれ別スレッドで同じscoreインスタンスに対してメソッドを実行します。データ競合がなければ、それぞれ渡した点数がhighScoreとして出力されるはずです。
```

修正の理由：「リスト2.1:データ競合」での`DispatchQueue.global`の`async`メソッドのクロージャー内はそれぞれ別スレッドで実行されます。別スレッドで実行される行の比較は③と⑤が正しいです。


