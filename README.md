# Browser Fingerprinting
ブラウザフィンガープリント（Browser Fingerprinting）とは、Webブラウザから得られる情報だけで（それらデータをマージしたハッシュ値を特定することで）、個人を特定するための方法である。  
  
近年、EUを中心に起きている **「GDPR」** や **「ePrivacy規則」** などといったCookie取得の制限の強化から、ブラウザフィンガープリントは新しい個人の特定手法として注目をされている。
  

## 取得できる情報
- userAgent
- language
- clolorDepth
- deviceMemory
- hardwareConcurrency
- screenResolution
- availableScreenResolution
- timezoneOffset
- timezone
- sessionStrage
- localStorage
- indexedDb
- addBehavior
- openDatabase
- cpuClass
- platform（Webブラウザを実行しているプラットフォーム）
- plugins（Webブラウザにインストールされたプラグインのリスト）
- canvas
- webgl
- webglVendorAndRenderer
- adBlock（クラス名がadboxをHTMLに挿入した徳のエラーの有無）
- hasLiedLanguages
- hasLieResolution
- hasLiedOs
- hasliedBrowser
- touchSupport
- fonts
- audio

## できないこと
ユーザーがWebブラウザやプラグインなどの変更があるとハッシュ値が変わってしまいユーザーの追従が難しくなる。  
（同一の情報が得られるような方法も出てきている:クロスブラウザフィンガープリンティング）

## 実行方法
当リポジトリをクローンするなどし、fingerprint.htmlをローカル環境で実行してください。　　
**[Fingerprintjs2](https://github.com/Valve/fingerprintjs2)** を使用しています。  
取得したくない項目はoptionsで[項目名：true]とすることで指定することができます。  
ここでは取得コストの大きい、フォント、WebGL、Audio、Canvasを例として除外しています。　　
