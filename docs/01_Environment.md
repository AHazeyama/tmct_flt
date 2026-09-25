<p akugb=:keft>  
	<img src="./assets/01_Environment_titlebar_dark.png#gh-dark-mode-only" alt="banner dark">  
	<img src="./assets/01_Environment_titlebar_light.png#gh-light-mode-only" alt="banner light">  
</p>  
<!--  
<img src="./assets/01_Environment_titlebar_light.png">  
-->  
  
# 開発ツールインストール												<!-- 01 -->    
　**SDK(Flutter)** 及び **IDE(Android Studio)** のインストールと環境設定を行います。  
  
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
  
## インストール済みツール確認							<!-- 01-01 -->  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_git=--version.png">  
  
</summary>   
  
```pwsh  
git --version  
```  
</details>  
  
　  <img src="./assets/cmd/M_CMD_01-01_git=--version-R.png">  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_code=--version.png">  
  
</summary>   
   
```pwsh  
code --version  
```  
  
</details>  
  
　　<img src="./assets/cmd/M_CMD_01-02_code=--version-R.png">  
  
  
  
## Flutter(Framework) & Dart(Language) インストール						<!-- 01-02 -->  
　　<img src="./assets/env/M_here.png" height="18" align="top"> ボタンより **FlutterSDK** バンドルをダウンロード  
　　[<img src="./assets/env/M_flutter-download.png" height="18" align="top">](https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.44.8-stable.zip)　<img src="./assets/env/M_link.png" height="14"> [Install Flutter manually](https://docs.flutter.dev/install/manual)  
　解凍して任意のフォルダへ保存　　推奨：<img src="./assets/env/M_folder.png" height="14"> C : \Develop\  
  
## 環境変数登録															<!-- 01-03 -->  
### インストール&Path確認  
　<img src="./assets/env/M_monitor.png" height="14"> 左下の <img src="./assets/env/M_search-bar.png" height="18" align="top"> へ <img src="./assets/env/M_text-LR.png" height="12">環境変数<img src="./assets/env/M_text-LR.png" height="12"> を入力して [<img src="./assets/env/M_env-val-icon.png" height="18">](./assets/env/M_env-val-icon.png) を <img src="./assets/env/M_click.png" height="14">   
　<img src="./assets/env/M_win.png" height="14"> 環境変数/ <img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/env/M_text-M.png" height="12"> のユーザー環境変数(<u>U</u>) <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> Path <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_button-L.png" height="12"> 編集(<u>E</u>)… <img src="./assets/env/M_button-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">  
　　　<img src="./assets/env/M_win.png" height="14"> 環境変数名の編集/ <img src="./assets/env/M_button-L.png" height="12"> 新規 <img src="./assets/env/M_button-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　**追加** <img src="./assets/env/M_text-LR.png" height="12">C:\Develop\flutter\bin<img src="./assets/env/M_text-LR.png" height="12"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_button-L.png" height="12"> **OK** <img src="./assets/env/M_button-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">  
　<img src="./assets/env/M_win.png" height="14"> 環境変数/ <img src="./assets/env/M_button-L.png" height="12"> **OK** <img src="./assets/env/M_button-R.png" height="12"> <img src="./assets/env/M_click.png" height="14">  
　　　[<img src="./assets/prtsc/M_CNTL_env-user-path.png" width="200">](./assets/prtsc/M_CNTL_env-user-path.png)　<img src="./assets/env/M_allow-T.png" height="32" align="top">　[<img src="./assets/prtsc/M_CNTL_env-user-path-add.png" width="170" align="top">](./assets/prtsc/M_CNTL_env-user-path-add.png)  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_flutter=--version.png">  
  
</summary>   
  
```pwsh  
　flutter --version  
```  
  
</details>  
  
　　[<img src="./assets/cmd/M_CMD_01-03_flutter=--version-R.png" width="540">](./assets/cmd/M_CMD_01-03_flutter=--version-R.png)  
  
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
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_dart=--version.png">  
  
</summary>   
   
```pwsh  
　dart --version  
```  
  
</details>  
  
　　[<img src="./assets/cmd/M_CMD_01-04_dart=--version-R.png" width="540">](./assets/cmd/M_CMD_01-04_dart=--version-R.png)  
  
### VS Code への機能拡張追加  
　左ツールバーの <img src="./assets/prtsc/M_VSC_extention.png" height="20" align="top"> <img src="./assets/env/M_click.png" height="14">️ 、又は  <img src="./assets/prtsc/M_VSC_setting.png" height="20" align="top">️️ <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_vxc_ext_ext.png" align="top">️ <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">  
　<img src="./assets/prtsc/M_VSC_flutter-extention.png" height="32" align="top">　<img src="./assets/env/M_slash.png" height="12"> 　<img src="./assets/prtsc/M_VSC_dart-extention.png" height="32" align="top">　インストール   
  
### Flutter初回診断  
  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_flutter=doctor=-v.png">  
  
</summary>   
  
```pwsh  
　flutter doctor -v  
```  
  
</details>  
  
　　[<img src="./assets/cmd/M_CMD_01-05_flutter=doctor=-v-R-E.png" width="540">](./assets/cmd/M_CMD_01-05_flutter=doctor=-v-R-E.png)  
> [!IMPORTANT]  
> この時点では Android Studio / cmdline-tools がインストールされていないため、にエラーが出る。  
> Flutterがインストールされていれば **OK**  
  
## Android Studio(IDE) インストール										<!-- 01-04 -->  
　![](./assets/env/M_IDE_AndroidStudo_20.png)  
　<img src="./assets/env/M_IDE_AndroidStudio.png" height="20">  
　インストーラ入手  
　　<img src="./assets/env/M_link.png" height="14"> [Android Studio](https://developer.android.com/studio?hl=ja)　※使用許諾の必要があるため、リンク先の <img src="./assets/env/M_androidstudio-install.png" height="18"> よりダウンロード  
　　<img src="./assets/env/M_androidstudio-installer0.png" height="24"> W<img src="./assets/env/M_click.png" height="14"> デフォルト設定でインストール  
　　SDKインストール先 : <img src="./assets/env/M_folder.png" height="14"> C:\Users\ユーザー名\AppData\Local\Android\Sdk  
  
### プロジェクト作成  
|Welcome to<br>Android Studio|Trust and Open<br>Project|  
|:---:|:---:|  
|[<img src="./assets/prtsc/M_AS_01-04_welcomeAS.png" width="128">](./assets/prtsc/M_AS_01-04_welcomeAS.png) |[<img src="./assets/prtsc/M_AS_01-04_trust-and-openproject.png" width="128">](./assets/prtsc/M_AS_01-04_trust-and-openproject.png)|  
|<img src="./assets/env/M_menu-L.png" height="12"> Open <img src="./assets/env/M_menu-R.png" height="12"> ️<img src="./assets/env/M_click.png" height="14">|<img src="./assets/prtsc/M_AS_trust-project.png" height="18" align="top"> <img src="./assets/env/M_click.png" height="14">|  
  
> [!important]  
> **tmct_flt** は **main.dart** 及び **pubspec.yaml** を別途作成し、Android Studioに読み込ませています。  
  
### SDK インストール  
　<img src="./assets/env/M_IDE_AndroidStudio.png" height="20">  
　<img src="./assets/prtsc/M_AS_APR-LU.png" height="18"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_Tolls.png" height="14"> <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_menu-bar-SDK_Maneger-button.png" height="14"><img src="./assets/env/M_menu-R.png" height="12"> ️<img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　SDKインストール   
　[<img src="./assets/prtsc/M_AS_menu-bar-SDK_Maneger.png" height="48">](./assets/prtsc/M_AS_menu-bar-SDK_Maneger.png)  
  
|Item|Content|Remarks|  
|:--|:--|:--|  
|SDK Platforms|Android 16.0 ("Baklava")|Emulator用なので、一般的なSDKで|  
|SDK Tools|Android SDK Build-Tools<br>　　37.0.0<br>　　36.1.0<br>　　36.0.0<br>Android Emulator<br>Android SDK Platform-Tools|<br>┐<br>┼─　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_SDK-ShowPackageDetails-on.png" height="18" align="top"> <img src="./assets/env/M_menu-R.png" height="12"> で表示<br>┘<br> <br> <br>|  
  
#### 　<img src="./assets/env/M_tech-documents.png" height="20"> [SDKインストール方法 詳細](./SDK-Introduction.md)  
  
### Emulator(Pixel7)インストール  
　<img src="./assets/env/M_IDE_AndroidStudio.png" height="20">  
　<img src="./assets/prtsc/M_AS_APR-LU.png" height="18"> ️<img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_Tolls.png" height="12"> <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_menu-bar_Device_Maneger-button.png" height="12">  <img src="./assets/env/M_menu-R.png" height="12">️ <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　スマートフォンイメージ インストール   
　[<img src="./assets/prtsc/M_AS_menu-bar_Device_Maneger.png" height="48">](./assets/prtsc/M_AS_menu-bar_Device_Maneger.png)  
  
　<img src="./assets/env/M_win.png" height="14"> Device Maneger <img src="./assets/env/M_slash.png" height="12"> <img src="./assets/env/M_button-L.png" height="12"><img src="./assets/prtsc/M_AS_plus.png" height="14"><img src="./assets/env/M_button-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_CreateVirtualDevice.png" height="14"> <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　　　　　　<img src="./assets/env/M_win.png" height="14"> スマートフォン登録  
　[<img src="./assets/prtsc/M_AS_DeviceManeger-1st.png" width="180" align="top">](./assets/prtsc/M_AS_DeviceManeger-1st.png)　<img src="./assets/env/M_allow-R.png" height="18" align="top">　[<img src="./assets/prtsc/M_AS_DeviceManeger-1st-CreateVirtualDevice.png" width="180">](./assets/prtsc/M_AS_DeviceManeger-1st.png)　<img src="./assets/env/M_allow-R.png" height="18" align="top">　[<img src="./assets/prtsc/M_AS_AddDevice.png" width="96" align="top">](./assets/prtsc/M_AS_DeviceManeger-1st.png)  
  
#### スマートフォン登録内容  
|Item|Content|Remarks|  
|:---|:---|:---|  
|name|Pixel 7||  
|API|API 36.1 "Baklava";Android 16||  
|Services|Google Play Store||  
|System Image|16KB Page Size Google Play Intel x86 64 Atom System Image||  
#### 　<img src="./assets/env/M_tech-documents.png" height="20"> [スマートフォン登録方法 詳細](./Device-Introduction.md)  
  
### Android ライセンス承認  
<details>  
<summary>  
　<img src="./assets/env/M_copy.png" height="14">  
　<img src="./assets/cmd/M_CMD_flutter=doctor=--android-licenses.png">  
  
</summary>   
   
```pwsh  
　flutter doctor --android-licenses  
```  
  
</details>  
  
　[<img src="./assets/cmd/M_CMD_01-06_flutter=doctor=--android-licenses-R.png" width="540">](./assets/cmd/M_CMD_01-06_flutter=doctor=--android-licenses-R.png)  
　以降、何度か  <img src="./assets/env/M_text-LR.png" height="12">Accept? (y/N)<img src="./assets/env/M_text-LR.png" height="12"> と聞かれるので、全て <img src="./assets/env/M_key-L.png" height="12"> y <img src="./assets/env/M_key-R.png" height="12">で **OK**  
　　　　　　　　　<img src="./assets/env/M_allow-D.png" height="14">  
　<img src="./assets/cmd/M_CMD_01-07_flutter=doctor=--android-licenses-Q.png">  
　上記メッセージを確認できれば承認完了。  
  
### 完了確認  
次の状態になっていれば、開発環境の構築は完了です。  
- `flutter doctor -v` でFlutter及びAndroid toolchainが認識される  
- Androidライセンスが承認済み  
- Android StudioからPixel 7 Emulatorを起動できる  
- VS CodeでFlutter及びDart拡張機能が有効になっている  
  
  
## Emulator起動															<!-- 01-05 -->  
　<img src="./assets/env/M_IDE_AndroidStudio.png" height="20">  
　<img src="./assets/prtsc/M_AS_APR-LU.png" height="18"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_Tolls.png" height="14"> <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_next.png" height="14">　<img src="./assets/env/M_menu-L.png" height="12"> <img src="./assets/prtsc/M_AS_menu-bar_Device_Maneger-button.png" height="14"> <img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">  
　<img src="./assets/prtsc/M_AS_menu-bar_Device_Maneger.png" height="48">  
  
　<img src="./assets/env/M_win.png" height="14"> Device Maneger <img src="./assets/env/M_slash.png" height="12"> <img src="./assets/env/M_menu-L.png" height="12">Pixel7<img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　　<img src="./assets/env/M_menu-L.png" height="12"><img src="./assets/prtsc/M_AS_run.png" height="14"><img src="./assets/env/M_menu-R.png" height="12"> <img src="./assets/env/M_click.png" height="14"> <img src="./assets/env/M_next.png" height="14">　　　　　　　　　　<img src="./assets/env/M_win.png" height="14"> Pixel7 Home  
　<img src="./assets/prtsc/M_AS_DeviceManager-2nd.png" width="128" align="top">　　　　　　<img src="./assets/env/M_allow-R.png" height="18" align="top">　　　　　<img src="./assets/prtsc/M_AS_DeviceManager-3rd.png" width="128" align="top">　<img src="./assets/env/M_allow-R.png" height="18" align="top">　[<img src="./assets/prtsc/M_AS_Pixel7-HOME-initial.png" height="256" align="top">](./assets/prtsc/M_AS_Pixel7-HOME-initial.png)  