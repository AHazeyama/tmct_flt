<p akugb=:keft>  
	<img src="./assets/APP_Initialize_titlebar_dark.png#gh-dark-mode-only" alt="banner dark">  
	<img src="./assets/APP_Initialize_titlebar_light.png#gh-light-mode-only" alt="banner light">  
</p>  
  
<!--  
<img src="./assets/APP_Initialize_titlebar_light.png">  
-->  
  
# 開発環境初期化  
　インストール済みの **Flutter** と **Android Studio**  及びその環境、生成物の削除を行います。  
> [!CAUTION]  
> この手順では、Flutter SDK、Android SDK、Android Emulator、  
> Android Studioの設定及び各種キャッシュを削除します。  
>  
> **既存の Flutter / Android 開発環境を継続して使用する場合は、  
> この手順を実行しないでください。**  
>  
> 削除したSDK、仮想端末及び設定は元に戻せません。  
> 必要なプロジェクト、設定、仮想端末及びファイルがある場合は、  
> 必ず事前にバックアップしてください。  
  
> [!NOTE]  
> 凡例  
> [<img src="./assets/env/M_legend.png" width="480">](./assets/env/M_legend.png)  
>  
> 縮小画像 (マウスカーソルが <img src="./assets/env/M_info.png" height="14"> に変化する画像) は <img src="./assets/env/M_click.png" height="14"> で拡大表示します。  
>  
> Source code / コマンド は <img src="./assets/env/M_copy.png" height="14"> <img src="./assets/env/M_click.png" height="14"> でText表示します (表示されたTextの右上にある <img src="./assets/env/M_git-copy.png" height="14"> <img src="./assets/env/M_click.png" height="14"> でコピー)。  
>  
> <img src="./assets/env/M_infoG.png" height="14"> ブラウザを **Darkモード** にして頂けると、見やすくなります。  
>  
> <img src="./assets/env/M_term.png" height="14"> コマンドは全て <img src="./assets/env/M_SHELL_PWSH.png" height="12"> で実行します。  
  
## 環境確認                                                         <!-- APP -->  
### 　Flutter SDK 環境                                              <!-- APP-01 -->  
　現在の開発環境確認  
　Path確認  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_where.exe=flutter.png">  
  
</summary>   
   
```pwsh  
where.exe flutter  
```  
  
</details>  
  
　　<img src="./assets/cmd/M_CMD_APP-01_where.exe=flutter-R.png">  
  
　Flutter確認  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_flutter=doctor=-v.png">  
  
</summary>   
   
```pwsh  
flutter doctor -v  
```  
 
</details>  
 
　[<img src="./assets/cmd/M_CMD_APP-02_flutter=doctor=-v-R.png" width="540">](./assets/cmd/M_CMD_APP-02_flutter=doctor=-v-R.png)  
  
> [!warning]  
> Flutterの新しいバージョンが存在する場合のメッセージ  
> 　　　　　　　　　　　　　　　<img src="./assets/env/M_CMT_flutter-upgrade.png" height="12">  
> 　<img src="./assets/cmd/M_CMD_00-01_flutter=doctor=-v-R-U.png">  
> アップグレード手順  
> <img src="./assets/env/M_caution.png" height="14"> AndroidStudioを終了してから実行すること。  
> <details>  
> <summary>  
> 　<img src="./assets/env/M_copy.png" height="14">  
> 　<img src="./assets/cmd/M_CMD_flutter=upgrade.png">  
>  
> </summary>   
>  
> ```pwsh  
> flutter upgrade  
> ```  
>   
> </details>  
>   
> 　[<img src="./assets/cmd/M_CMD_00-02_flutter=upgrade-R.png" width="540">](./assets/cmd/M_CMD_00-02_flutter=upgrade-R.png)  
### 　Android 環境  
　既存環境確認  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem-Where-Sort.png" align="top">  
  
</summary>   
   
```pwsh  
Get-ChildItem Env: |  
    Where-Object {  
        $_.Name -match 'ANDROID|JAVA|FLUTTER|DART|GRADLE|PUB'  
    } |  
    Sort-Object Name  
```  
</details>  
  
　　<img src="./assets/prtsc/APP-01-03_get-childitem.png">  
  
  
　Path確認  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_$envPath=-split.png" align="top">  
  
</summary>   
   
```pwsh  
$env:Path -split ';' |  
    Where-Object {  
        $_ -match 'flutter|android|dart|gradle|java'  
    }  
```  
  
</details>  
  
　　<img src="./assets/prtsc/APP-01-04_envpath.png">  
  
## 環境削除									    				    <!-- APP-02 -->  
  
> [!WARNING]  
> 本章以降のコマンドは対象ディレクトリを確認してから実行してください。  
> 環境によってインストール先が異なる場合があります。  
  
### プロジェクト内のBuild生成物 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_flutter=clean.png">  
  
</summary>   
   
```pwsh  
flutter clean  
```  
  
</details>  
  
　　<img src="./assets/env/M_CMT_no-message.png">  
  
### Android Studio 削除  
　EmulatorはAndroid Studioから削除  
　残骸が残っていたら削除 : %USERPROFILE%\.android\avd  
　<img src="./assets/env/M_monitor.png" height="14"> 左下 <img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/env/M_ICON_Windows1.png" height="16">️️ <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> ⇒ <img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/env/M_MENU_AndroidStudio1.png"> <img src="./assets/env/M_menu-R.png" height="12"> 右️<img src="./assets/env/M_click.png" height="14"> ⇒ <img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/env/M_MENU_trash-can.png"> <img src="./assets/env/M_menu-R.png" height="12"> ⇒  
　<img src="./assets/env/M_menu-L.png" height="12"> ⚙️Window <img src="./assets/env/M_menu-R.png" height="12"> ⇒ <img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/env/M_MENU_AndroidStudio2.png" height="20"> <img src="./assets/env/M_menu-R.png" height="12"> ️<img src="./assets/env/M_click.png" height="14"> ⇒ <img src="./assets/env/M_menu-L.png" height="12"> アンインストール <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14">  
  
### Android Studio 削除確認 残項目があれば強制削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Test--Path=Android=Studio.png">  
  
</summary>   
   
```pwsh  
Test-Path "C:\Program Files\Android\Android Studio" <⏎>  
```  
</details>  
  
　true　　　　<img src="./assets/env/M_CMT_env-exists.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=C-AndroidStudio.png">  
  
  
</summary>   
   
```pwsh  
Remove-Item -Recurse -Force "C:\Program Files\Android\Android Studio"  
```  
  
</details>  
  
　　　<img src="./assets/env/M_CMT_no-message-output-if-delete-sucsess.png">  
  
### Android SDK環境 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-Sdk.png">  
  
</summary>   
   
```pwsh  
Remove-Item -Recurse -Force "$env:LOCALAPPDATA\Android\Sdk"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-01a_remove-item.png" width="540">](./assets/cmd/M_CMD_APP-02-01a_remove-item.png)  
　　　　　　　　　　　<img src="./assets/env/M_allow-D.png" height="20">  
　[<img src="./assets/cmd/M_CMD_APP-02-01b_remove-item.png" width="540">](./assets/cmd/M_CMD_APP-02-01b_remove-item.png)  
　　　　　　　　　　　<img src="./assets/env/M_allow-D.png" height="20">  
　[<img src="./assets/cmd/M_CMD_APP-02-01c_remove-item.png" width="540">](./assets/cmd/M_CMD_APP-02-01c_remove-item.png)  
　残環境 **：** $HOME\AppData以下はこの後削除します。  
  
### $HOMEの環境 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-USERPROFILE-android.png">  
  
</summary>   
   
```pwsh  
Get-ChildItem "$env:USERPROFILE\.android"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-02_Get-ChildItem-android.png" width="540">](./assets/cmd/M_CMD_APP-02-02_Get-ChildItem-android.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-USERPROFILE-android.png">  
  
</summary>  
  
```pwsh  
Remove-Item -Recurse -Force "$env:USERPROFILE\.android"  
```  
</details>  
  
　<img src="./assets/env/M_CMT_no-message-output-if-delete-sucsess.png">  
  
### 設定 及び キャッシュ 削除  
> [!IMPORTANT]  
> Android Studioで生成されたディレクトリは "**AndroidStudio** "、"**Android Studio**"等のバリエーションが存在します。  
> **Get-ChildItem** で検索出来たディレクトリそれぞれに適した **Remove-Item** コマンドを実行して下さい。  
#### Local環境/キャッシュ  
　対象 <img src="./assets/env/M_folder.png" height="14">  : $HOME\AppData\Local\Google\  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-LOCSLAPPDATA-android.png">  
  
</summary>   
   
```pwsh  
Get-ChildItem "$env:LOCALAPPDATA\Google" -Directory -Filter "Android*"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-03_Get-ChildItem-Loal-Android.png" width="540">](./assets/cmd/M_CMD_APP-02-03_Get-ChildItem-Loal-Android.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-LOCALAPPDATA.png">  
  
</summary>   
   
```pwsh  
Remove-Item -Recurse -Force "$env:LOCALAPPDATA\Google\上記ディレクトリ名"  
```  
  
</details>  
  
　<img src="./assets/env/M_CMT_no-message-output-if-delete-sucsess.png">  
  
　対象 <img src="./assets/env/M_folder.png" height="14"> : $HOME\AppData\Roaming\Google\  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-APPDATA-Google-android.png">  
  
</summary>   
   
```pwsh  
Get-ChildItem "$env:APPDATA\Google" -Directory -Filter "Android*"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-04_Get-ChildItem-Roaming-Android.png" width="540">](./assets/cmd/M_CMD_APP-02-04_Get-ChildItem-Roaming-Android.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-APPDATA.png">  
  
</summary>   
   
```pwsh  
Remove-Item -Recurse -Force "$env:APPDATA\Google\ディレクトリ名"  
```  
</details>  
  
　<img src="./assets/env/M_CMT_no-message-output-if-delete-sucsess.png">  
  
#### Gradleキャッシュ 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-USERPROFILE-gradle.png">  
  
</summary>   
   
```pwsh  
Get-ChildItem "$env:USERPROFILE\.gradle"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-05_Get-ChildItem-grable.png" width="540">](./assets/cmd/M_CMD_APP-02-05_Get-ChildItem-grable.png)  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-USERPROFILE-gradle.png">  
  
</summary>   
  
```pwsh  
Remove-Item -Recurse -Force "$env:USERPROFILE\.gradle"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-06_Remove-Item-grable.png" width="540">](./assets/cmd/M_CMD_APP-02-06_Remove-Item-grable.png)  
　<img src="./assets/env/M_CMT_del-comp-progress-bar.png">  
  
### Flutter SDK 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_where.exe=flutter.png">  
  
</summary>   
  
```pwsh  
where.exe flutter  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-07_where.exe-flutter.png">](./assets/cmd/M_CMD_APP-02-07_where.exe-flutter.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem-flutter.png">  
  
</summary>   
  
```pwsh  
Get-ChildItem "C:\Develop\flutter"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-08_ChildItem-flutter.png" width="540">](./assets/cmd/M_CMD_APP-02-08_ChildItem-flutter.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=C-flutter.png">  
  
</summary>   
  
```pwsh  
Remove-Item -Recurse -Force "C:\Develop\flutter"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-09_Remove-Item-flutter.png" width="540">](./assets/cmd/M_CMD_APP-02-09_Remove-Item-flutter.png)  
　<img src="./assets/env/M_CMT_del-comp-progress-bar.png">  
  
### Flutter & Dart 設定･キャッシュ 削除  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_dartPath=foreach=RemoveItem.png" align="top">  
  
</summary>   
  
```pwsh  
$dartPaths = @(  
  "$env:APPDATA\.dart",  
  "$env:APPDATA\.dart-tool",  
  "$env:LOCALAPPDATA\.dartServer"  
)  
  
foreach ($path in $dartPaths) {  
  if (Test-Path $path) {  
      Remove-Item -Recurse -Force $path  
  }  
}   
```  
  
</details>  
  
　<img src="./assets/env/M_CMT_exec-message-display-briefly.png">  
　<img src="./assets/env/M_CMT_no-other-message-prompt-deletion.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-LOCALAPPDATA-Cache.png">  
  
</summary>   
  
```pwsh  
Get-ChildItem "$env:LOCALAPPDATA\Pub\Cache"  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_
APP-02-10_Get-ChildItem-Local-flutter.png" height="128">](./assets/cmd/M_CMD_APP-02-10_Get-ChildItem-Local-flutter.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env=LOCALAPPDATA=cache.png" width="540">  
  
</summary>   
  
```pwsh  
　Remove-Item -Recurse -Force "$env:LOCALAPPDATA\Pub\Cache" -ErrorAction SilentlyContinue  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_APP-02-11_Remove-Item-Local-flutter.png" width="540">](./assets/cmd/M_CMD_APP-02-11_Remove-Item-Local-flutter.png)  
　<img src="./assets/env/M_CMT_del-comp-progress-bar.png">  
　<img src="./assets/env/M_comment-F.png" height="12">　<img src="./assets/env/M_caution.png" height="14"> <img src="./assets/env/M_CMT_RemoveItemNotes-on-Options.png">   
  
　<img src="./assets/env/M_folder.png" height="14"> :  C:\Development\flutter を削除  
  
## 再起動 ⇒ 削除確認                                               <!-- APP-03 -->  
### 削除対象  
　　　･Windows 環境変数  
　　　･Git for Windows  
　　　･VS Code 機能拡張   
　　　･Flutter SDK  
　　　･Android Studio  
　　　･Android SDK  
　　　･Android Emulator  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-USERPROFILE-android-flutter-dart-gradle.png" align="top">  
  
</summary>   
  
```pwsh  
Get-ChildItem "$env:USERPROFILE" -Force -Directory |  
  Where-Object {  
      $_.Name -match 'android|flutter|dart|gradle'  
  }  
```  
  
</details>  
  
　<img src="./assets/cmd/M_CMD_APP-03-01_Remove-Item-android.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-USERPROFILE-android.png">  
  
</summary>   
  
```pwsh  
Remove-Item -Recurse -Force "$env:USERPROFILE\.android"  
```  
  
</details>  
  
　<img src="./assets/env/M_CMT_no-message.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-LOCALAPPDATA-many-pub.png" align="top">  
  
</summary>   
  
```pwsh  
Get-ChildItem "$env:LOCALAPPDATA" -Force -Directory |  
  Where-Object {  
    $_.Name -match 'android|flutter|dart|gradle|pub'  
  }   
```  
  
</details>  
  
　<img src="./assets/cmd/M_CMD_APP-03-02_Get-ChildItem1.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-LOCALAPPDATA-dir.png">  
  
</summary>   
  
```pwsh  
Remove-Item -Recurse -Force "$env:LOCALAPPDATA\上記DIR"  
```  
  
</details>  
  
 　<img src="./assets/env/M_CMT_Delete-extract-dir.png">  
 　<img src="./assets/env/M_CMT_no-message.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Get-ChildItem=env-APPDATA-Where-Object.png" align="top">  
  
</summary>   
  
```pwsh  
Get-ChildItem "$env:APPDATA" -Force -Directory |  
  Where-Object {  
    $_.Name -match 'android|flutter|dart|gradle|pub'  
  }  
```  
  
</details>  
  
　<img src="./assets/prtsc/APP-03-03_Get-ChildItem2.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_Remove-Item=-Recurse=-Force=env-APPDATA-dart-tool.png">  
  
</summary>   
  
```pwsh  
Remove-Item -Recurse -Force "$env:APPDATA\.dart-tool"  
```  
</details>  
  
 　<img src="./assets/env/M_CMT_no-message.png">  
#### 　　残DIRの削除で初期化完了  