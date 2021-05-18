---
title: フォーム プロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412920"
---
# <a name="retrieving-form-properties"></a>フォーム プロパティの取得

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カスタム メッセージの種類にとって意味のあるクエリを発行するには、アプリケーションで、そのメッセージで必要なプロパティを知る必要があります。 カスタム メッセージ クラスが使用するプロパティの一覧を取得するには、クライアント アプリケーションが MAPI フォーム マネージャーを照会します。 フォーム マネージャーは、適切なフォーム構成ファイルからこの情報を取得し、クライアント アプリケーションがフォーム サーバー自体をアクティブ化するオーバーヘッドなしにこの情報を使用できます。 これを行うには、クライアント アプリケーションは [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを次のように呼び出します。 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

**ResolveMessageClass** の 3 番目の引数は、クエリがフォーム サーバーを検索する関連付けられたコンテンツ テーブルを含むフォルダーです。 NULL は、フォーム マネージャーが使用可能なすべてのフォーム コンテナーを検索する必要があります。 クエリを特定のフォルダーに対して実行する場合は、代わりに適切な [IMAPIFolder](imapifolderimapicontainer.md) ポインターを含める方が良いです。 
  
## <a name="see-also"></a>関連項目



[フォーム サーバーの操作](form-server-interactions.md)

