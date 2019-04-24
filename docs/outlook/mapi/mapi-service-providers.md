---
title: MAPI サービスプロバイダー
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6511e1b5-697e-4ed1-80af-aa8ca56fd045
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bb40891376ac511869ba157b675e53ee236b24ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346677"
---
# <a name="mapi-service-providers"></a>MAPI サービスプロバイダー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サービスプロバイダーには、次の3つの一般的な種類があります。
  
- アドレス帳プロバイダー。
    
- メッセージストアプロバイダー。
    
- トランスポートプロバイダー。
    
アドレス帳とメッセージストアプロバイダーには多くの類似点があります。 これらのユーザーは、オブジェクトのエントリ識別子を作成するために使用する、MAPI で一意の識別子を登録します。 クライアントがアクセスおよび操作できるオブジェクトおよびプロパティの階層を提供します。 container オブジェクトについては、階層テーブルと contents テーブルをサポートしています。 セッション中に発生した変更をクライアントに通知できるように、これらのテーブルに対するイベント通知と、必要に応じて個々のオブジェクトをサポートします。 操作が長くなると、操作の状態をユーザーに通知するための進行状況インジケーターを表示することができます。 クライアントは、 [IAddrBook: imapiprop](iaddrbookimapiprop.md)と[imapiprop: IUnknown](imapisessioniunknown.md)インターフェイスを使用するか、またはサービスプロバイダーインターフェイスのいずれかを直接使用して、アドレス帳とメッセージストアプロバイダーとの間で間接的に通信できます。次の表。 
  
|**アドレス帳プロバイダーインターフェイス**|**メッセージストアプロバイダーインターフェイス**|
|:-----|:-----|
|[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md) <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) <br/> |
|[IDistList : IMAPIContainer](idistlistimapicontainer.md) <br/> |[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) <br/> |
|[IMailUser : IMAPIProp](imailuserimapiprop.md) <br/> |[IMessage: IMAPIProp](imessageimapiprop.md) <br/> |
| <br/> |[IAttach : IMAPIProp](iattachimapiprop.md) <br/> |
   
トランスポートプロバイダーは、MAPI およびクライアントとの通信と同じ方法で、アドレス帳とメッセージストアプロバイダーとは異なります。 通常、トランスポートプロバイダーは、通信を開始するのではなく、MAPI が情報を求めるメッセージを表示するのを待ちます。 他のプロバイダーとは異なり、トランスポートプロバイダーはクライアントによってよくアクセスされるさまざまなオブジェクトおよびテーブルをサポートしていません。 ただし、すべてのサービスプロバイダーと同様に status オブジェクトをサポートし、そのプロパティを状態テーブルに公開します。 アドレス帳およびメッセージストアプロバイダーは、エントリ id を構築するための一意の識別子を登録するために[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出します。トランスポートプロバイダーは、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出します。特定のメッセージを配信する責任を負うために、一意の識別子およびアドレスの種類を登録します。 
  
サービスプロバイダーは3つのヘッダーファイル (1 つのパブリックヘッダーファイルと2つの内部ファイル) を持っている必要があります。 構成用にパブリックヘッダーファイルを使用し、プロパティとその値を記録します。 必要なすべてのパブリック MAPI ヘッダーを内部ヘッダーファイルのいずれかに含めることができます。このヘッダーファイルは、すべてのサービスプロバイダーのソースファイルに含まれている必要があります。 他の内部ファイルを使用して、リソース識別子を定義します。
  
アドレス帳、メッセージストア、およびトランスポートプロバイダーは、次のタスクを実行します。
  
- エントリポイント関数を指定します。 
    
- ログオンと初期化を処理するプロバイダーとログオンオブジェクトを指定します。 
    
- プロバイダーがメッセージサービスに属している場合は、メッセージサービスエントリポイント関数を指定します。 
    
- プロパティシートを実装することで、構成をサポートします。
    
- status オブジェクトを実装し、状態テーブルをサポートします。 
    
- シャットダウンを処理します。
    
## <a name="see-also"></a>関連項目



[MAPI の概念](mapi-concepts.md)

