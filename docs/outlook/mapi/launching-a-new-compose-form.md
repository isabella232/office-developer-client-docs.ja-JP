---
title: 新規作成フォームを起動します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8d1b94c70e4de6310d2e84cf002c4e3199fced2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801285"
---
# <a name="launching-a-new-compose-form"></a>新規作成フォームを起動します。

  
  
**適用されます**: Outlook 
  
フォーム サーバーの実装は次の一連のフォームのサーバーへのメソッド呼び出しを期待する必要があり、フォーム オブジェクトの場合、クライアント アプリケーションを作成するための新しいメッセージを開きます。
  
1. クライアント アプリケーションは、フォームのサーバーのメッセージ クラスのクラス情報を取得する[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出します。 
    
2. クライアント アプリケーションは、新しいフォーム オブジェクトを取得する[IMAPIFormMgr::CreateForm](imapiformmgr-createform.md)を呼び出します。 
    
3. MAPI フォーム マネージャーでは、フォームのサーバーから[IMAPIForm](imapiformiunknown.md)インターフェイスを取得し、メモリ、されていない場合は、フォーム サーバーが読み込まれます。 
    
4. クライアント アプリケーションは、結果として得られる**IMAPIForm**インタ フェースし、オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)インターフェイスを取得する[IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)メソッドを呼び出します。 
    
5. クライアント アプリケーションでは、 [IMessage](imessageimapiprop.md)、ビュー コンテキスト、フォーム オブジェクトに関連付けると、アドバイズ シンク オブジェクトの[IPersistMessage::InitNew](ipersistmessage-initnew.md)メソッドを呼び出します。
    
6. クライアント アプリケーションでは、開いている動詞を呼び出すための[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出します。 
    
## <a name="see-also"></a>関連項目



[フォームのサーバー間のやり取り](form-server-interactions.md)
