---
title: MAPI クライアント オブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412409"
---
# <a name="mapi-client-objects"></a>MAPI クライアント オブジェクト
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準のメッセージング クライアント アプリケーションは、1 つのオブジェクト (アドバイス シンク) のみを実装します。 通知シンクは [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスから継承され、MAPI およびサービス プロバイダーによってイベント通知に使用されます。 一部のクライアントでは、進行状況ダイアログ ボックスの表示をサポートする進行状況オブジェクトも実装します。 
  
カスタム フォームをサポートするより複雑なクライアントは [、IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) インターフェイスから継承するメッセージ サイト オブジェクトや [、IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) インターフェイスから継承するビュー コンテキスト オブジェクトなど、別のアアドバイス シンク オブジェクトと他のいくつかのオブジェクトを実装します。 追加のアアドバイス シンク オブジェクトは [、IMAPIViewAdviseSink : IUnknown インターフェイスから継承](imapiviewadvisesinkiunknown.md) します。 
  
次の表は、標準メッセージング クライアントとカスタム フォームの表示をサポートするクライアントによって実装される MAPI オブジェクトの概要を示しています。
  
|**クライアント オブジェクト**|**説明**|
|:-----|:-----|
|シンクのアドバイス  <br/> |メッセージ ストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。  <br/> |
|メッセージ サイト  <br/> |フォーム オブジェクトの操作を処理します。  <br/> |
|Progress  <br/> |操作の進行状況を表示するダイアログ ボックスを表示します。  <br/> |
|View アアドバイス シンク  <br/> |フォームで発生するイベントのコールバック関数を提供します。  <br/> |
|コンテキストの表示  <br/> |フォームの印刷と保存、およびフォーム間の移動のためのコマンドをサポートします。  <br/> |
   
次の図は、これらの異なるクライアント オブジェクト、継承元のインターフェイス、およびそれらを使用する MAPI コンポーネントの関係を示しています。 
  
![クライアント オブジェクトと対応するインターフェイス](media/amapi_65.gif "クライアント オブジェクトと対応するインターフェイス")
  
クライアントは、実装するオブジェクトよりも多くのオブジェクトを使用します。 すべてのクライアントは、セッション オブジェクトを使用して、MAPI が実装するさまざまなサービス プロバイダー オブジェクトとオブジェクトにアクセスします。 クライアントは、間接的に、セッション、アドレス帳、MAPI が提供する状態オブジェクト、または特定のサービス プロバイダーが実装するさまざまなオブジェクトを介して直接、サービス プロバイダーと対話します。 アドレス帳プロバイダーと直接連絡を取る場合、クライアントはアドレス帳コンテナー、メッセージング ユーザー、配布リストを使用します。 メッセージ ストア プロバイダーに直接アクセスするには、クライアントはメッセージ ストア オブジェクト、フォルダー、メッセージ、添付ファイルを使用します。 サービス プロバイダーが状態オブジェクトをサポートする場合、クライアントは status オブジェクトを使用してサービス プロバイダーの状態を監視できます。
  
サービス プロバイダーとメッセージ サービス構成をサポートするクライアントは、MAPI が実装する 3 つのオブジェクト (メッセージ サービス管理オブジェクト、プロファイル管理オブジェクト、プロバイダー管理オブジェクト) を使用します。 カスタム フォームを表示するクライアントは、フォーム ライブラリ プロバイダーまたはフォーム サーバーが実装する複数のフォーム オブジェクトを使用します。
  
## <a name="see-also"></a>関連項目

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [MAPI オブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

