# EpisoPass CLI

- EpisoPassをコマンドラインから使う

## インストール

    $ gem install episopass

## 使い方

EpisoPass画面をブラウザで開いてパスワード文字列を標準出力で得る

    % episopass [EpisoPassのHTMLのファイル名またはURL]

`~/.episopass.html` があればこれが使われる


パスワードつきzipを作る

    % zip -e my.zip -P `episopass` file1 file2

パスワードつきzipを解凍する

    % unzip -P `episopass` my.zip

## episozip, episounzip

    % episozip [-P EpisoPassのHTMLのファイル名またはURL] output.episopass file1 file2 ...

file1, file2, ... を暗号化して output.episopass というzipファイルを作る

## 考察

秘密ファイルをこれで全部隠しておき、必要になったときEpisoPassで復元すると良いかもしれない

    % zip -e secretfiles.zip -P `episopass` .netrc .gem .npmrc .ssh/id_rsa ...

## Issues

