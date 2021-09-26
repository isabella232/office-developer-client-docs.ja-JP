---
title: 新規作成フォームの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 29ad3393340d356a043f5df5115b9112d8e3b3df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610357"
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

