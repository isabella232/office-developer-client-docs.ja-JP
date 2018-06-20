---
title: MAPI サービス プロバイダー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3f1cab24ef6bbd632ee3dc204e93f59e6f9ac846
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801466"
---
# <a name="mapi-service-providers"></a>MAPI サービス プロバイダー

  
  
**適用されます**: Outlook 
  
次の 3 つの一般的なサービス ・ プロバイダーの種類があります。
  
- アドレス帳プロバイダーをします。
    
- メッセージ ストア プロバイダーです。
    
- プロバイダーに転送します。
    
アドレス帳、メッセージ ストア プロバイダーでは、多くの類似点があります。 MAPI を使用して、オブジェクトのエントリ id を作成するために一意の識別子を登録するとします。 オブジェクトとクライアントがアクセスしたり、操作したりするプロパティの階層を提供します。 コンテナーのオブジェクトには、階層テーブルおよび内容のテーブルをサポートしています。 サポート イベント通知これらのテーブルにし、必要に応じて個々 のオブジェクトのクライアントは、セッション中に発生する変更通知できるようにします。 操作には時間がかかるになると、操作のステータスをユーザーに通知する進行状況インジケーターを表示することができます。 クライアントと通信できますアドレス帳、メッセージ ストア プロバイダーから間接的に、MAPI を使用して、 [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)と[IMAPISession: IUnknown](imapisessioniunknown.md)インタ フェースまたは直接のサービス プロバイダー インターフェイスのいずれかを使用して、次の表。 
  
|**アドレス帳プロバイダー インターフェイス**|**メッセージ ストア プロバイダーのインターフェイス**|
|:-----|:-----|
|[これにより: IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList: IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser: IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach: IMAPIProp](iattachimapiprop.md) <br/> |
   
トランスポート プロバイダーは、クライアントで MAPI と通信する方法で、アドレス帳、メッセージ ストア プロバイダーによって異なります。 トランスポート プロバイダーは、通常の通信を開始するのではなく、情報を要求するには MAPI の待機します。 他のプロバイダーとは異なりトランスポート プロバイダーはさまざまなオブジェクトとクライアントが頻繁にアクセスされるテーブルをサポートしていません。 ただし、サポートして状態オブジェクトでは、すべてのサービス プロバイダーの操作を行い、状態テーブル内のプロパティを公開します。 トランスポート プロバイダーがする[IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出しますが、アドレス帳、メッセージ ストア プロバイダーは、それらのエントリの識別子を構築するための一意の識別子を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出して、処理の特定のメッセージの配信のための一意の識別子とアドレスの種類を登録します。 
  
サービス ・ プロバイダーは次の 3 つのヘッダー ファイルで必要があります: 1 つのパブリック ヘッダー ファイルと 2 つの内部のファイルです。 パブリック ヘッダー ファイルは、構成し、プロパティとその値を記録するために使用します。 内部ヘッダー ファイルのいずれかですべての必要なパブリック MAPI ヘッダーが含まれますこのヘッダー ファイルは、すべてのサービス プロバイダーのソース ファイルに入れるべき。 その他の内部のファイルを使用すると、リソース識別子を定義します。
  
アドレス帳、メッセージ ・ ストア、およびトランスポート プロバイダーは、次のタスクを実行します。
  
- エントリ ポイント関数を指定します。 
    
- ログオンや初期化を処理するには、プロバイダーとログオン オブジェクトを指定します。 
    
- メッセージ サービス プロバイダーが属している場合は、メッセージ サービスのエントリ ポイント関数を指定します。 
    
- プロパティ シートを実装することによって構成をサポートします。
    
- 状態オブジェクトを実装し、状態テーブルをサポートします。 
    
- ハンドルはシャット ダウンします。
    
## <a name="see-also"></a>関連項目



[MAPI �̊T�O](mapi-concepts.md)

