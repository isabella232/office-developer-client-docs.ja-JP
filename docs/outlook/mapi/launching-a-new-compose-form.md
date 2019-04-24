---
title: 新規作成フォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270057"
---
# <a name="launching-a-new-compose-form"></a>新規作成フォームの起動

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーの実装者は、クライアントアプリケーションが新しいメッセージを作成するときに、次のようなメソッド呼び出しをフォームサーバーとフォームオブジェクトに対して実行することを前提としています。
  
1. クライアントアプリケーションは、 [imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出して、フォームサーバーのメッセージクラスに関するクラス情報を取得します。 
    
2. クライアントアプリケーションは、 [imapiformmgr:: CreateForm](imapiformmgr-createform.md)を呼び出して、新しい form オブジェクトを取得します。 
    
3. MAPI フォームマネージャーが、まだメモリにない場合はフォームサーバーを読み込み、フォームサーバーから[imapiform](imapiformiunknown.md)インターフェイスを取得します。 
    
4. クライアントアプリケーションは、生成された**imapiform**インターフェイスを受け取り、 [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出して、オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを取得します。 
    
5. クライアントアプリケーションは、 [IPersistMessage:: InitNew](ipersistmessage-initnew.md)メソッドを呼び出して、form オブジェクトを[IMessage](imessageimapiprop.md)、ビューコンテキスト、およびアドバイズシンクオブジェクトに関連付けます。
    
6. クライアントアプリケーションは、 [imapiform::D overb](imapiform-doverb.md)メソッドを呼び出して open 動詞を呼び出します。 
    
## <a name="see-also"></a>関連項目



[フォームサーバーの相互作用](form-server-interactions.md)

