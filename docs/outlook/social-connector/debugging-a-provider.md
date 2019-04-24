---
title: プロバイダーのデバッグ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d2dfaeed-7635-4c6b-9c35-b955ca1a85e9
description: Outlook Social Connector (.osc) プロバイダーをデバッグするには、いくつかの方法があります。
ms.openlocfilehash: 39deb7b6c0b11460826bdbf1957ffd8404d926e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281070"
---
# <a name="debugging-a-provider"></a>プロバイダーのデバッグ

Outlook Social Connector (.osc) プロバイダーをデバッグするには、いくつかの方法があります。 
  
- Outlook の office Fluent ユーザーインターフェイスのリボンコンポーネントにあるデバッグコマンドを使用するか、office クライアントアプリケーションをサポートして、.osc にさまざまなアクションを実行させることができます。
    
- Fiddler を使用して、ソーシャルネットワークと .osc プロバイダーとの間で送信される API 呼び出しと XML をトレースする
    
## <a name="debug-buttons"></a>デバッグボタン

.osc プロバイダー拡張機能は、.osc プロバイダーをデバッグする機能を提供します。 プロバイダーをデバッグするには、 `DebugProviders` Windows レジストリの`SocialConnector`キーの下にある (次の行に示すように) DWORD 型の値を作成`DebugProviders`し、値を1に設定します。 
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector`
  
既定では、プロバイダーデバッグはオフになっています。 `DebugProviders`値が存在しない場合、または存在し、値が0に設定されている場合は、プロバイダーデバッグがオフになります。 
  
プロバイダーデバッグが有効になっている場合は、エラーが発生したときに詳細なエラー情報を含む警告ダイアログボックスが表示され、.osc プロバイダーの xml スキーマに対して、.osc プロバイダ xml を検証します。 XML 文字列に対して指定された名前空間に基づいて、.osc 1.0 を使用して開発された .osc プロバイダーが、.osc 1.0 スキーマファイル、outlookの形式に対して検証されます。 .osc 1.1 以降を使用して開発した .osc プロバイダーは、スキーマファイル outlooksocialprovider_ 1.1 に対して検証されます。 `DebugProviders`値を使用すると、特定のプロバイダーではなく、読み込まれたすべてのプロバイダーのデバッグ警告が表示されます。 
  
プロバイダーをデバッグするのに役立つデバッグボタンを表示するには`ShowDebugButtons` 、 `SocialConnector`キーの下の Windows レジストリに DWORD 型の値を作成し`ShowDebugButtons` 、値を1に設定します。 デバッグコマンドバーボタンを非表示にするに`ShowDebugButtons`は、値を0に設定します。 
  
Office 2013 以降の Outlook 2010 およびクライアントアプリケーションの場合、[デバッグ] ボタンはエクスプローラーリボンの [**アドイン**] タブに表示されます。 outlook 2007 および outlook 2003 の場合、[デバッグ] ボタンは、outlook エクスプローラーウィンドウの標準のコマンドバーに表示されます。 
  
次の表で、デバッグボタンについて説明します。
  
|**[デバッグ] ボタン**|**Function**|
|:-----|:-----|
|連絡先を同期する  <br/> |.osc は、キャッシュされた連絡先のみを、.osc プロバイダーに要求します。  <br/> |
|GAL 同期  <br/> |.osc が Exchange のグローバルアドレス一覧から Outlook の連絡先にデータを設定するようにします。  <br/> |
|カテゴリキャッシュを無効にする  <br/> |アクティビティフィードが更新されたときに、.osc が各ストアのカテゴリリストを再読み込みするようにします。  <br/> |
   
## <a name="fiddler"></a>Fiddler

Fiddler は、プロバイダーからソーシャルネットワークに送信された API 呼び出しと、ソーシャルネットワークによってプロバイダーに送信される XML をチェックする、ネットワーク上のデバッグツールです。 Fiddler は、 [Fiddler Web デバッグプロキシ](https://www.fiddler2.com/fiddler2/version.asp)でダウンロードできます。
  
## <a name="see-also"></a>関連項目

- [プロバイダーを開発するための簡単な手順](quick-steps-for-learning-to-develop-a-provider.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md) 
- [プロバイダーを開発するためのベストプラクティス](best-practices-for-developing-a-provider.md)
- [通常の呼び出しシーケンスの .osc](osc-typical-calling-sequences.md)  
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)  
- [.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md)

