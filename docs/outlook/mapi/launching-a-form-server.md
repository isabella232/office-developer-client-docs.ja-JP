---
title: フォームサーバーの起動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270050"
---
# <a name="launching-a-form-server"></a>フォームサーバーの起動

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが永続的なストレージ (フォームライブラリから) から読み込まれてメッセージを表示するときに発生する一連の対話は、次のようになります。
  
1. メッセージングクライアントは、メッセージのメッセージクラス、メッセージフラグ、およびメッセージの状態を取得します。 この手順は省略できます。このようなデータが手順2で提供されていない場合は、フォームマネージャーが取得します。
    
2. メッセージングクライアントは、ターゲットメッセージと共に[imapiformmgr:: loadform](imapiformmgr-loadform.md)を呼び出します。 
    
3. フォームマネージャーは、フォームサーバーを適切なフォームライブラリから読み込みます。 ターゲットメッセージのフォームサーバーがインストールされていない場合、フォームマネージャーはフォームの実行可能ファイルもインストールします。
    
4. フォームマネージャーは form オブジェクトの[iunknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx)を呼び出して、form オブジェクトの[imapiform: iunknown](imapiformiunknown.md)インターフェイスと[IPersistMessage: iunknown](ipersistmessageiunknown.md)インターフェイスを取得します。 
    
5. フォームマネージャーは、 [IPersistMessage:: Load](ipersistmessage-load.md)というメッセージサイトとメッセージインターフェイスを viewer オブジェクトから呼び出します。 
    
6. form オブジェクトは、メッセージングクライアントの[IMAPIMessageSite:: getsitestatus](imapimessagesite-getsitestatus.md)メソッドに呼び出しを戻します。 
    
7. フォームマネージャーは、フォームオブジェクトの[imapiform:: setviewcontext](imapiform-setviewcontext.md)メソッドによって、メッセージングクライアントからビューコンテキストインターフェイスを呼び出します。 
    
8. form オブジェクトは、メッセージングクライアントの[imapiviewcontext:: SetAdviseSink](imapiviewcontext-setadvisesink.md)メソッドに呼び出しを戻します。 
    
9. form オブジェクトは、メッセージングクライアントの[imapiviewcontext:: getviewstatus](imapiviewcontext-getviewstatus.md)メソッドに呼び出しを戻します。 
    
10. メッセージングクライアントは、フォームオブジェクトの[imapiform:: Advise](imapiform-advise.md)メソッドを viewer オブジェクトおよびメッセージサイトオブジェクトからのビューコンテキストインターフェイスで呼び出します。 
    
11. メッセージングクライアントは、form オブジェクトの[imapiform を呼び出します。:D overb](imapiform-doverb.md)メソッド。 
    
12. form オブジェクトは、必要に応じて、そのユーザーインターフェイスを作成し、ユーザーと対話します。
    
## <a name="see-also"></a>関連項目



[フォームサーバーの相互作用](form-server-interactions.md)

