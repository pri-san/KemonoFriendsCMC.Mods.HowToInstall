# KemonoFriendsCMC.Mods.HowToInstall
けものフレンズ Cellien May Cry（以下「ゲーム本体」とする）の MOD対応化の手順

## ゲーム本体の情報
* 製作者様
  * 坂本龍様
    * 連絡先はゲーム本体付属の説明書を参照してください
* ダウンロードURL
  * ふりーむ！：https://www.freem.ne.jp/win/game/25092
  * フリーゲーム夢現：https://freegame-mugen.jp/action/game_9372.html

## 前提条件

* OS
  * Windows 10 (x64)
* PCスペック
  * MOD未対応状態でスムーズに動く程度
    * MOD対応化すると処理が重くなる為

## 手順

1. バックアップを作成する
  * ゲーム本体KemonoFriendsCMC\KirisameZensen.KemonoFriendsCMC.savedata.json
    * 同一バージョンのゲーム本体インストーラを使用して別フォルダに展開、または既存のフォルダをコピーまたは圧縮等
  * セーブファイル
    * `%UserProfile%\AppData\LocalLow\KirisameZensen\KemonoFriendsCMC\KirisameZensen.KemonoFriendsCMC.savedata.json`をコピーまたは圧縮等
2. マネージコードストリッピングされたアセンブリをされていないアセンブリに置き換える
  * https://github.com/pri-san/KemonoFriendsCMC.Mods.HowToInstall/releases から最新バージョンのUnityManagedDllFull.zipをダウンロードする
  * `(ゲーム本体のルートフォルダ)\KemonoFriendsCMC_Data\Managed`にダウンロードしたzipファイルの内容(zip内のUnityManagedDllFullフォルダ配下)を展開する
    * 上書き確認のダイアログは全て置き換えるを選択する
    * ゲーム本体のルートフォルダ: `KemonoFriendsCMC.exe`が配置されているフォルダ
3. BepInExを配置する
  * https://github.com/BepInEx/BepInEx/releases から バージョン5.x（動作確認済みバージョン: 5.4.11.0）、x64のzipファイルをダウンロードする
  * `(ゲーム本体のルートフォルダ)`にダウンロードしたzipファイルの内容を展開する
    * 展開後の構造が`(ゲーム本体のルートフォルダ)\BepInEx\core`となるようにする
4. BepInExを適用する
  * 一度ゲーム本体を起動し、タイトル画面まで進めて終了する
  * `(ゲーム本体のルートフォルダ)\BepInEx\`配下に`patchers`や`plugins`フォルダが作成される
5. BepInEx.ConfigurationManagerのパッチを導入する【任意・推奨】
  * MODの設定変更等をGUIで行えるようになるパッチ
    * ゲーム実行中にF1キーで設定変更画面を開く事ができる
  * https://github.com/BepInEx/BepInEx.ConfigurationManager/releases からバージョン16（動作確認済みバージョン: 16.3）のzipファイルをダウンロードする
  * `(ゲーム本体のルートフォルダ)`にダウンロードしたzipファイルの内容を展開する
    * 展開後の構造が`(ゲーム本体のルートフォルダ)\BepInEx\plugins\ConfigurationManager.dll`となるようにする

## pri-sanが公開しているMOD一覧

* かばんちゃん操作MOD
  * https://github.com/pri-san/KemonoFriendsCMC.Mods.KabanMode/releases
  * サーバルちゃんをかばんちゃんに置き換えるMOD
* MOD使用中表示MOD
  *  https://github.com/pri-san/KemonoFriendsCMC.Mods.ShowUsingMod/releases
  *  画面右下に`MOD(Addon)`という赤色の表示を追加することで、MOD利用であることを明示的にするMOD
    * 画面を見ただけでMODを利用しているかどうか見分けがつくようにすることが目的

## 連絡先

* Twitter: @Puri_san_P
* e-mail: pri.san.pg@gmail.com
