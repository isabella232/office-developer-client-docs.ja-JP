---
title: フォーム プロパティの取得
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803778"
---
# <a name="retrieving-form-properties"></a>フォーム プロパティの取得

  
  
**適用対象**: Outlook 
  
カスタム メッセージの種類に意味のあるクエリを発行するには、アプリケーションはそのメッセージに対して予測されるプロパティを確認する必要があります。 カスタム メッセージ クラスを使用するプロパティの一覧を取得するには、クライアント アプリケーションでは、MAPI フォーム マネージャーを照会します。 フォーム マネージャーは、クライアント アプリケーションがこの情報は、フォーム サーバー自体をアクティブ化のオーバーヘッドを生じさせずに使用できるように、適切なフォーム構成ファイルからこの情報を取得します。 これを行うは、クライアント アプリケーションは、 [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを次のように呼び出します。 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

**ResolveMessageClass**の 3 番目の引数には、フォームのサーバーのクエリによって検索される内容が関連付けられているテーブルが含まれるフォルダーに注意してください。 NULL では、フォーム マネージャーが利用可能なフォームのすべてのコンテナーを検索する必要があることを示します。 特定のフォルダーに対して実行するクエリがある場合は、代わりに適切な[IMAPIFolder](imapifolderimapicontainer.md)ポインターを含めることをお勧めします。 
  
## <a name="see-also"></a>関連項目



[フォーム サーバーの相互作用](form-server-interactions.md)

