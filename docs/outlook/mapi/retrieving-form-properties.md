---
title: フォーム プロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6fb1c828803063fbc77d1732ca18b527c08fd0f3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586832"
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

