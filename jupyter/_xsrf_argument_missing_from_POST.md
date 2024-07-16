### **'_xsrf' argument missing from POSTエラーの単純な対処法**

jupyter notebookを使って深層学習をしているとき、数時間ipynbファイルを開いたまま放置していると発生する。<br>
'_xsrf' argument missing from POSTというエラーが出て、画面の更新が止まるように見える。保存しようとしてもなぜが出来なくなっている。<br>

対処法実:<br>
jupyter notebookファイル選択画面（起動すると最初に開かれるタブ）に戻って、そのファイルをクリックして開きなす<br>
新しく開いたファイル画面は止まっているが、もとのファイル画面にはエラーが消えて学習も進んでいる。<br>
新しく開いたファイル画面は消してOK。特にPythonの設定などを変える必要は無い。

原因:<br>
トークンの処理における問題で、コードの実行自体はバックグラウンドで続いている。<br>
参考：https://stackoverflow.com/questions/55014094/jupyter-notebook-not-saving-xsrf-argument-missing-from-post