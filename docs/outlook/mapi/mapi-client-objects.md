---
title: MAPI クライアントオブジェクト
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 11304a4c-d986-4ad9-a140-19a59825a8df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6e78c80d861a5a56584bfb03bfdf2895efde8730
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319291"
---
# <a name="mapi-client-objects"></a>MAPI クライアントオブジェクト
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
標準のメッセージングクライアントアプリケーションは、1つのオブジェクト (アドバイズシンク) のみを実装します。 アドバイズシンクは[IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイスから継承し、イベント通知用に MAPI およびサービスプロバイダーによって使用されます。 一部のクライアントは、進行状況のダイアログボックスの表示をサポートするために、進行状況オブジェクトも実装します。 
  
カスタムフォームをサポートするより複雑なクライアントでは、別のアドバイズシンクオブジェクトと、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インターフェイスから継承するメッセージサイトオブジェクト、およびその他のいくつかのオブジェクトを実装します。[imapiviewcontext: IUnknown](imapiviewcontextiunknown.md)インターフェイス。 追加のアドバイズシンクオブジェクトは、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インターフェイスから継承します。 
  
次の表に、標準のメッセージングクライアントと、カスタムフォームの表示をサポートするクライアントによって実装される MAPI オブジェクトの概要を示します。
  
|**クライアントオブジェクト**|**説明**|
|:-----|:-----|
|アドバイズシンク  <br/> |メッセージストア、アドレス帳、またはセッションで発生するイベントのコールバック関数を提供します。  <br/> |
|メッセージサイト  <br/> |form オブジェクトの操作を処理します。  <br/> |
|Progress  <br/> |操作の進行状況を示すダイアログボックスを表示します。  <br/> |
|アドバイズシンクの表示  <br/> |フォームで発生するイベントのコールバック関数を提供します。  <br/> |
|ビューのコンテキスト  <br/> |フォームの印刷および保存、およびフォーム間の移動に使用するコマンドをサポートします。  <br/> |
   
次の図は、これらの異なるクライアントオブジェクト、継承元のインターフェイス、およびそれらを使用する MAPI コンポーネントの関係を示しています。 
  
![クライアントオブジェクトと対応するインターフェイス](media/amapi_65.gif "クライアントオブジェクトと対応するインターフェイス")
  
クライアントは、実装されているよりも多くのオブジェクトを使用します。 すべてのクライアントは session オブジェクトを使用して、MAPI が実装するさまざまなサービスプロバイダーオブジェクトおよびオブジェクトにアクセスします。 クライアントは、サービスプロバイダーを間接的に、セッション、アドレス帳、または MAPI が提供する status オブジェクトを通じて、または特定のサービスプロバイダーが実装しているさまざまなオブジェクトによって対話します。 アドレス帳プロバイダーと直接連絡先を作成するために、クライアントはアドレス帳コンテナー、メッセージングユーザー、および配布リストを使用します。 メッセージストアプロバイダーに直接アクセスする場合、クライアントはメッセージストアオブジェクト、フォルダー、メッセージ、および添付ファイルを使用します。 サービスプロバイダーが status オブジェクトをサポートしている場合、クライアントは status オブジェクトを使用して、サービスプロバイダーの状態を監視できます。
  
サービスプロバイダーとメッセージサービスの構成をサポートするクライアントは、MAPI が実装する3つのオブジェクトを使用します。メッセージサービスの管理オブジェクト、プロファイル管理オブジェクト、およびプロバイダー管理オブジェクトです。 ユーザー設定フォームを表示するクライアントは、フォームライブラリプロバイダーまたはフォームサーバーが実装する複数のフォームオブジェクトを使用します。
  
## <a name="see-also"></a>関連項目

- [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) 
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)  
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
- [MAPI のオブジェクトとインターフェイスの概要](mapi-object-and-interface-overview.md)

