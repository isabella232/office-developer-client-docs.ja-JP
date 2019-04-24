---
title: フォームプロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328652"
---
# <a name="retrieving-form-properties"></a>フォームプロパティの取得

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カスタムメッセージの種類に意味のあるクエリを発行するには、アプリケーションがそのメッセージで想定されるプロパティを知っている必要があります。 カスタムメッセージクラスが使用するプロパティの一覧を取得するために、クライアントアプリケーションは MAPI フォームマネージャーを照会します。 フォームマネージャーは、この情報を適切なフォーム構成ファイルから取得するので、クライアントアプリケーションはこの情報を使用して、フォームサーバー自体をアクティブにするというオーバーヘッドを発生しません。 これを行うには、クライアントアプリケーションは次のように[imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出します。 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

**ResolveMessageClass**の3番目の引数は、クエリがフォームサーバーを検索する、関連付けられた contents テーブルを含むフォルダーです。 NULL は、フォームマネージャーが使用可能なすべてのフォームコンテナーを検索する必要があることを示します。 クエリが特定のフォルダーに対して実行される場合は、代わりに適切な[imapifolder](imapifolderimapicontainer.md)ポインターを含めることをお勧めします。 
  
## <a name="see-also"></a>関連項目



[フォームサーバーの相互作用](form-server-interactions.md)

