---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: ソーシャル コネクタ (OSC) プロバイダーでOutlook方法は次のとおりです。
ms.openlocfilehash: 60856866359521923c225a41a5399b8e20093b1a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608922"
---
# <a name="debugging-a-provider"></a>プロバイダーのデバッグ

ソーシャル コネクタ (OSC) プロバイダーでOutlook方法は次のとおりです。 
  
- Outlook の Office Fluent ユーザー インターフェイスのリボン コンポーネントまたはサポートされている Office クライアント アプリケーションのリボン コンポーネントでデバッグ コマンドを使用して、OSC がさまざまなアクションを実行します。
    
- Fiddler を使用してソーシャル ネットワークとその OSC プロバイダー間で送信される API 呼び出しと XML を追跡する
    
## <a name="debug-buttons"></a>デバッグ ボタン

OSC プロバイダーの機能拡張により、OSC プロバイダーをデバッグできます。 プロバイダーをデバッグするには、キーの下の Windows レジストリに DWORD 型の値を作成し (次の行に示すように)、値を `DebugProviders` `SocialConnector` `DebugProviders` 1 に設定します。 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
既定では、プロバイダーのデバッグはオフです。 値が存在しない場合、または値が存在し、値 0 に設定されている場合、プロバイダー  `DebugProviders` のデバッグは無効になります。 
  
プロバイダーのデバッグが有効になっている場合、エラーが発生した場合、OSC は詳細なエラー情報を含む警告ダイアログ ボックスを表示し、OSC プロバイダー XML スキーマに対して OSC プロバイダー XML を検証します。 XML 文字列に指定された名前空間に基づいて、OSC 1.0 を使用して開発された OSC プロバイダーは、OSC 1.0 スキーマ ファイル OutlookSocialProvider.xsd に対して検証されます。 OSC 1.1 以降を使用して開発された OSC プロバイダーは、スキーマ ファイル OutlookSocialProvider_1.1.xsd に対して検証されます。 この値を使用すると、特定のプロバイダーではなく、読み込まれたすべてのプロバイダーに対してデバッグ  `DebugProviders` アラートが表示されます。 
  
プロバイダーのデバッグに役立つデバッグ ボタンを表示するには、キーの下の Windows レジストリに DWORD 型の値を作成し、値を `ShowDebugButtons` `SocialConnector` 1 に `ShowDebugButtons` 設定します。 デバッグ コマンド バー ボタンを非表示にする場合は、値  `ShowDebugButtons` を 0 に設定します。 
  
Outlook 2013 以降の 201 Office 0 およびクライアント アプリケーションの場合、デバッグ ボタンはエクスプローラーリボンの [アドイン] タブに表示されます。 2007 Outlook 2003 および Outlook 2003 の場合、デバッグ ボタンは、エクスプローラー ウィンドウの標準コマンド バー Outlook表示されます。 
  
次の表に、デバッグ ボタンについて説明します。
  
|**[デバッグ] ボタン**|**関数**|
|:-----|:-----|
|連絡先の同期  <br/> |OSC がキャッシュされた連絡先のみを OSC プロバイダーに求める原因です。  <br/> |
|GAL 同期  <br/> |OSC がグローバル アドレス一覧から連絡先にデータExchangeを設定Outlookします。  <br/> |
|カテゴリ キャッシュの無効化  <br/> |アクティビティ フィードの更新時に、OSC が各ストアのカテゴリ リストを再読み込みします。  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler は、プロバイダーからソーシャル ネットワークに送信される API 呼び出し、およびソーシャル ネットワークからプロバイダーに送信される XML を確認する、ネットワーク上のデバッグ ツールです。 Fiddler は [Fiddler Web デバッグ プロキシでダウンロードできます](https://www.fiddler2.com/fiddler2/version.asp)。
  
## <a name="see-also"></a>関連項目

- [プロバイダーを開発するためのラーニング手順](quick-steps-for-learning-to-develop-a-provider.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [プロバイダーの開発に関するベスト プラクティス](best-practices-for-developing-a-provider.md)
- [OSC の一般的な呼び出しシーケンス](osc-typical-calling-sequences.md)  
- [OSC XML スキーマを使用したプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md)  
- [OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md)

