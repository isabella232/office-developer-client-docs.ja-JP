---
title: MAPI オブジェクトおよびプロパティのアクセス許可
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32669cbe-5460-4043-99cc-c609608f48da
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aad19bbc016af6bdc0b17124b46112656af53a4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801716"
---
# <a name="permissions-for-mapi-objects-and-properties"></a>MAPI オブジェクトおよびプロパティのアクセス許可

  
  
**適用されます**: Outlook 
  
アクセス許可、または一連の permissable の操作には、MAPI オブジェクトおよびそれらのオブジェクトでサポートされている個々 のプロパティの特性がある場合ができます。 オブジェクトへのアクセスは、オブジェクトの親によって決定されます。 メッセージは、そのフォルダーはアクセス許可を決定します。 メッセージングのユーザーまたは配布リスト、アドレス帳コンテナーはこの決定をなります。 2 つのフォルダー、メッセージなどのオブジェクトが存在する場合、オブジェクトの 2 つのコピーのアクセス許可が異なる場合ができます。 
  
これらのオブジェクトを使用してクライアントに対するアクセス許可オブジェクトの[IMAPISession::OpenEntry](imapisession-openentry.md)の呼び出しで MAPI_BEST_ACCESS フラグを設定することで最高のレベルを要求できます。 オブジェクトを実装するサービス プロバイダーによって、クライアントは、必要なアクセス権のレベルは許可されません。 クライアントは、オブジェクト ([PidTagAccess](pidtagaccess-canonical-property.md)) である**PR_ACCESS**プロパティを取得するために**GetProps**メソッドを呼び出すことによって許可されたことをアクセスのレベルを決定できます。 ただし、サービス プロバイダーは、このプロパティの値を動的に生成する必要があります、ためには、クライアントが必要な場合にのみを取得するをお勧めします。 
  
フォルダー、アドレス帳コンテナー、または配布リストなどのコンテナーに変更ができるかどうかを確認するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得するために**GetProps**メソッドを呼び出します。 コンテナー レベルのアクセスでは、クライアントで、ユーザー インターフェイスを表示する方法に影響します。 ユーザー インターフェイスの表示と、一般的な実装ではコンテナー内のオブジェクトの実装も影響を受けます。 
  
特定のプロパティへのアクセスは、MAPI プロパティを所有するオブジェクトの設定、プロパティ スキーマによって決まります。 プロパティ スキーマは、オブジェクトとそのアクセス許可の必須およびオプションのプロパティのセットを指定します。 オブジェクトの親によって決定されるオブジェクトへのアクセスとは異なり、プロパティへのアクセスはグローバルです。 オブジェクトの親のアクセスの要件にかかわらず、すべてのオブジェクトは、スキーマによって決定されたプロパティの同じ権限を持ちます。
  
プロパティが読み取り専用の場合は、常に**GetProps**または**OpenProperty**の呼び出しで使用可能なことができます。 ただし、プロパティをサポートするオブジェクトの実装によっては、プロパティとそれを削除するための**DeleteProps**メソッドを変更するための**SetProps**メソッドの 2 つの可能な結果があります。 
  
- 失敗し、MAPI_E_NO_ACCESS を返す
    
- 正常に処理は実行されません。
    
プロパティとオブジェクト アクセスの取得または**IMAPIProp**インターフェイスを継承する[IPropData](ipropdataimapiprop.md)インターフェイスを使用して設定もできます。 MAPI には、メモリ内のデータに基づく**IPropData**の実装が用意されています。 サービス ・ プロバイダーは、状態オブジェクトのように特定の状況で**IMAPIProp**を実装するために**IPropData**を使用することができます。 または組み込みのトランザクションのないデータベースを使用している場合。 **IPropData**は、ロックし、データのロックを解除する必要がないように、メモリ内でのみ動作します。 
  
## <a name="see-also"></a>関連項目



[MAPI Property Overview](mapi-property-overview.md)
