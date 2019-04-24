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
# <a name="retrieving-form-properties"></a><span data-ttu-id="3d71d-103">フォームプロパティの取得</span><span class="sxs-lookup"><span data-stu-id="3d71d-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="3d71d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d71d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d71d-105">カスタムメッセージの種類に意味のあるクエリを発行するには、アプリケーションがそのメッセージで想定されるプロパティを知っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d71d-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="3d71d-106">カスタムメッセージクラスが使用するプロパティの一覧を取得するために、クライアントアプリケーションは MAPI フォームマネージャーを照会します。</span><span class="sxs-lookup"><span data-stu-id="3d71d-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="3d71d-107">フォームマネージャーは、この情報を適切なフォーム構成ファイルから取得するので、クライアントアプリケーションはこの情報を使用して、フォームサーバー自体をアクティブにするというオーバーヘッドを発生しません。</span><span class="sxs-lookup"><span data-stu-id="3d71d-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="3d71d-108">これを行うには、クライアントアプリケーションは次のように[imapiformmgr:: ResolveMessageClass](imapiformmgr-resolvemessageclass.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3d71d-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="3d71d-109">**ResolveMessageClass**の3番目の引数は、クエリがフォームサーバーを検索する、関連付けられた contents テーブルを含むフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="3d71d-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="3d71d-110">NULL は、フォームマネージャーが使用可能なすべてのフォームコンテナーを検索する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="3d71d-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="3d71d-111">クエリが特定のフォルダーに対して実行される場合は、代わりに適切な[imapifolder](imapifolderimapicontainer.md)ポインターを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3d71d-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d71d-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d71d-112">See also</span></span>



[<span data-ttu-id="3d71d-113">フォームサーバーの相互作用</span><span class="sxs-lookup"><span data-stu-id="3d71d-113">Form Server Interactions</span></span>](form-server-interactions.md)

