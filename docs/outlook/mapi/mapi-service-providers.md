---
title: MAPI サービス プロバイダー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 369a87b0adc5f36a59beb2663f6204feb8f34e19
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595785"
---
# <a name="mapi-service-providers"></a>MAPI サービス プロバイダー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービス プロバイダーには、次の 3 つの一般的な種類があります。
  
- アドレス帳プロバイダー。
    
- メッセージ ストア プロバイダー。
    
- トランスポート プロバイダー。
    
アドレス帳とメッセージ ストア プロバイダーには、多くの類似点があります。 オブジェクトのエントリ識別子を作成するために使用する一意の識別子を MAPI に登録します。 クライアントがアクセスおよび操作できるオブジェクトとプロパティの階層を提供します。 コンテナー オブジェクトでは、階層テーブルとコンテンツ テーブルがサポートされます。 これらのテーブルおよび必要に応じて個々のオブジェクトに対するイベント通知をサポートし、セッション中に発生した変更をクライアントに通知できます。 操作が長くなると、進行状況インジケーターを表示して、操作の状態をユーザーに通知できます。 クライアントは [、IAddrBook : IMAPIProp](iaddrbookimapiprop.md) および [IMAPISession : IUnknown](imapisessioniunknown.md) インターフェイスを使用するか、次の表のいずれかのサービス プロバイダー インターフェイスを使用して、MAPI を介して間接的にアドレス帳およびメッセージ ストア プロバイダーと通信できます。 
  
|**アドレス帳プロバイダー インターフェイス**|**メッセージ ストア プロバイダー インターフェイス**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
トランスポート プロバイダーは、MAPI とクライアントとの通信方法でアドレス帳プロバイダーやメッセージ ストア プロバイダーとは異なります。 トランスポート プロバイダーは、通常、MAPI が通信を開始するのではなく、情報の入力を求めるのを待ちます。 他のプロバイダーとは異なり、トランスポート プロバイダーは、クライアントが一般的にアクセスするさまざまなオブジェクトとテーブルをサポートしません。 ただし、すべてのサービス プロバイダーと同様に、状態オブジェクトをサポートし、そのプロパティを状態テーブルに発行します。 アドレス帳とメッセージ ストア プロバイダーは [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドを呼び出して、エントリ識別子を作成するための一意の識別子を登録します。トランスポート プロバイダーは [、IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して一意の識別子を登録し、特定のメッセージの配信の責任を負うアドレスの種類を呼び出します。 
  
サービス プロバイダーには、1 つのパブリック ヘッダー ファイルと 2 つの内部ファイルという 3 つのヘッダー ファイルが必要です。 構成およびプロパティとその値の文書化には、パブリック ヘッダー ファイルを使用します。 内部ヘッダー ファイルの 1 つに、必要なすべてのパブリック MAPI ヘッダーを含めます。このヘッダー ファイルは、すべてのサービス プロバイダー ソース ファイルに含める必要があります。 他の内部ファイルを使用して、リソース識別子を定義します。
  
アドレス帳、メッセージ ストア、およびトランスポート プロバイダーは、次のタスクを実行します。
  
- エントリ ポイント関数を指定します。 
    
- ログオンと初期化を処理するプロバイダーとログオン オブジェクトを指定します。 
    
- プロバイダーがメッセージ サービスに属している場合は、メッセージ サービスエントリ ポイント関数を指定します。 
    
- プロパティ シートを実装して構成をサポートします。
    
- status オブジェクトを実装し、状態テーブルをサポートします。 
    
- シャットダウンを処理します。
    
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

