---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Outlook ソーシャル コネクタ (OSC) プロバイダーをデバッグするいくつかの方法があります。
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386853"
---
# <a name="debugging-a-provider"></a>プロバイダーのデバッグ

Outlook ソーシャル コネクタ (OSC) プロバイダーをデバッグするいくつかの方法があります。 
  
- さまざまなアクションを実行するのには OSC が発生する Outlook またはサポートしている Office クライアント アプリケーションに Office Fluent ユーザー インターフェイスのリボン コンポーネントのデバッグ コマンドを使用しています。
    
- トレース API 呼び出しとソーシャル ネットワークと OSC プロバイダーの間で送信される XML に Fiddler を使用して、
    
## <a name="debug-buttons"></a>デバッグ ボタン

OSC プロバイダーの拡張機能は、デバッグ、OSC プロバイダーの機能を提供します。 プロバイダーをデバッグするには、作成、`DebugProviders`の下の Windows レジストリに DWORD 型の値、 `SocialConnector` (のように、次の行)、キーし、設定、`DebugProviders`値を 1。 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
既定では、プロバイダーのデバッグはオフです。 場合、`DebugProviders`の値が存在しないか、存在していて値が 0 では、プロバイダーのデバッグの設定がオフになっています。 
  
プロバイダーのデバッグを有効にする場合、OSC は、エラーが発生し、OSC プロバイダーの XML スキーマに対しては、OSC プロバイダーの XML を検証するときに詳細なエラー情報を使用して警告ダイアログ ボックスを表示します。 OSC 1.0 を使用して開発された、OSC プロバイダーは XML 文字列に指定した名前空間に基づいて、OSC 1.0 スキーマ ファイルで、OutlookSocialProvider.xsd に対して検証されます。 OSC プロバイダーは、OSC 1.1 を使用して開発されたまたは後で、スキーマ ファイル、OutlookSocialProvider_1.1.xsd に対して検証します。 使用する場合、`DebugProviders`の値を特定のプロバイダーではなくプロバイダーが読み込まれているすべてのデバッグの警告が表示されます。 
  
プロバイダーをデバッグするために役立つデバッグ ボタンを表示するには、次のように作成します。、`ShowDebugButtons`の下の Windows レジストリに DWORD 型の値、`SocialConnector`キー、および設定、 `ShowDebugButtons` 1 の値です。 デバッグのコマンド バー ボタンを非表示に設定、`ShowDebugButtons`値を 0 にします。 
  
Outlook 2010 と Office 2013 以降のクライアント アプリケーションでは、エクスプ ローラーのリボンの **[アドイン**] タブで、デバッグ ボタンが表示されます。 Outlook 2007 および Outlook 2003 の Outlook エクスプ ローラー ウィンドウの標準的なコマンド バーのデバッグ ボタンが表示されます。 
  
次の表では、デバッグ ボタンについて説明します。
  
|**デバッグ ボタン**|**関数**|
|:-----|:-----|
|連絡先を同期します。  <br/> |キャッシュされた取引先担当者の OSC プロバイダーに確認するのには OSC が発生します。  <br/> |
|グローバル アドレス一覧の同期  <br/> |Exchange のグローバル アドレス一覧から Outlook の連絡先にデータを設定するのには OSC が発生します。  <br/> |
|カテゴリのキャッシュを無効に  <br/> |アクティビティ フィードが更新されたときに各店舗のカテゴリの一覧を再読み込みするのには OSC が発生します。  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler は、API の呼び出しは、プロバイダーから、ソーシャル ネットワークに送信されると、プロバイダー、ソーシャル ネットワークから送信された XML を確認するのには、ワイヤ上のデバッグ ツールです。 Fiddler では、 [Fiddler Web デバッグ プロキシ](https://www.fiddler2.com/fiddler2/version.asp)からダウンロードできます。
  
## <a name="see-also"></a>関連項目

- [プロバイダーを開発する学習のためのクイック ステップ](quick-steps-for-learning-to-develop-a-provider.md)  
- [友人や活動を同期します。](synchronizing-friends-and-activities.md) 
- [プロバイダーを開発するためのベスト プラクティス](best-practices-for-developing-a-provider.md)
- [OSC の典型的な呼び出しシーケンス](osc-typical-calling-sequences.md)  
- [OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)  
- [OSC プロバイダーをリリースする準備をします。](getting-ready-to-release-an-osc-provider.md)

