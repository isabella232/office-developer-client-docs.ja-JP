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
  
フォーム サーバーの実装者は、クライアント アプリケーションが作成用の新しいメッセージを開く際に、フォーム サーバーとフォーム オブジェクトへのメソッド呼び出しの次のシーケンスを期待する必要があります。
  
1. クライアント アプリケーションは [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを呼び出して、フォーム サーバーのメッセージ クラスに関するクラス情報を取得します。 
    
2. クライアント アプリケーションは [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) を呼び出して新しいフォーム オブジェクトを取得します。 
    
3. MAPI フォーム マネージャーは、まだメモリ内に存在しない場合はフォーム サーバーを読み込み、フォーム サーバーから [IMAPIForm](imapiformiunknown.md) インターフェイスを取得します。 
    
4. クライアント アプリケーションは、結果の **IMAPIForm** インターフェイスを受け取り [、IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) メソッドを呼び出して、オブジェクトの [IPersistMessage インターフェイスを取得](ipersistmessageiunknown.md) します。 
    
5. クライアント アプリケーションは [、IPersistMessage::InitNew](ipersistmessage-initnew.md) メソッドを呼び出して、フォーム オブジェクトを [IMessage](imessageimapiprop.md)に関連付け、コンテキストを表示し、シンク オブジェクトにアドバイスします。
    
6. クライアント アプリケーションは [、IMAPIForm::D oVerb](imapiform-doverb.md) メソッドを呼び出して、開いている動詞を呼び出します。 
    
## <a name="see-also"></a>関連項目



[フォーム サーバーの操作](form-server-interactions.md)

