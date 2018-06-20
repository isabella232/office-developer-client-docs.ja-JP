---
title: フォームのプロパティを取得します。
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
# <a name="retrieving-form-properties"></a><span data-ttu-id="8a698-103">フォームのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8a698-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="8a698-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a698-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a698-105">カスタム メッセージの種類に意味のあるクエリを発行するには、アプリケーションはそのメッセージに対して予測されるプロパティを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a698-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="8a698-106">カスタム メッセージ クラスを使用するプロパティの一覧を取得するには、クライアント アプリケーションでは、MAPI フォーム マネージャーを照会します。</span><span class="sxs-lookup"><span data-stu-id="8a698-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="8a698-107">フォーム マネージャーは、クライアント アプリケーションがこの情報は、フォーム サーバー自体をアクティブ化のオーバーヘッドを生じさせずに使用できるように、適切なフォーム構成ファイルからこの情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="8a698-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="8a698-108">これを行うは、クライアント アプリケーションは、 [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを次のように呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8a698-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="8a698-109">**ResolveMessageClass**の 3 番目の引数には、フォームのサーバーのクエリによって検索される内容が関連付けられているテーブルが含まれるフォルダーに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8a698-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="8a698-110">NULL では、フォーム マネージャーが利用可能なフォームのすべてのコンテナーを検索する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="8a698-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="8a698-111">特定のフォルダーに対して実行するクエリがある場合は、代わりに適切な[IMAPIFolder](imapifolderimapicontainer.md)ポインターを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8a698-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a698-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a698-112">See also</span></span>



[<span data-ttu-id="8a698-113">フォームのサーバー間のやり取り</span><span class="sxs-lookup"><span data-stu-id="8a698-113">Form Server Interactions</span></span>](form-server-interactions.md)

