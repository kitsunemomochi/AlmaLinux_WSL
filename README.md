# AlmaLinux_WSL
WSL上のAlmaLinux環境用の設定ファイル

## エミュレーターインストール方法
1. コマンドプロンプトを起動
2. ```wsl --install``` で Windows Subsystem for Linux をインストールする。OS再起動。
3. ```wsl --version``` でバージョンを確認。
4. Ubuntuがインストールされているので削除する。```wsl --unregister Ubuntu```
5. アプリとしても Ubuntu on Windows を削除する。
6. Microsoft store から AlmaLinux9 を検索してインストール。

## gitの設定
1. 確かデフォルトでAlmaLinuxにインストールされていたのでインストール飛ばす
2. ```git config --global user.name "yourGitHubusername"```
3. ```git config --global user.email "your.email.address@xxx.com"```
4. ```git config --global core.quotepath false```
5. ```mkdir ~/.ssh ; cd ~/.ssh```
6. ```ssh-keygen -t rsa -b 4096 -C "some comments to identify ssh-key" -f rsa_GitHub```
7. ```git config --global core.sshCommand "ssh -T -i ~/.ssh/rsa_GitHub"```
8. ```ssh -T git@github.com -i rsa_GitHub```

## gcc コンパイラーの設定

