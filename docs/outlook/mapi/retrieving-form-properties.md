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
# <a name="retrieving-form-properties"></a><span data-ttu-id="53874-103">フォーム プロパティの取得</span><span class="sxs-lookup"><span data-stu-id="53874-103">Retrieving Form Properties</span></span>

  
  
<span data-ttu-id="53874-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53874-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53874-105">カスタム メッセージの種類にとって意味のあるクエリを発行するには、アプリケーションで、そのメッセージで必要なプロパティを知る必要があります。</span><span class="sxs-lookup"><span data-stu-id="53874-105">To issue a query that is meaningful to a custom message type, an application needs to know the properties that are expected on that message.</span></span> <span data-ttu-id="53874-106">カスタム メッセージ クラスが使用するプロパティの一覧を取得するには、クライアント アプリケーションが MAPI フォーム マネージャーを照会します。</span><span class="sxs-lookup"><span data-stu-id="53874-106">To get a list of properties that a custom message class uses, a client application queries the MAPI form manager.</span></span> <span data-ttu-id="53874-107">フォーム マネージャーは、適切なフォーム構成ファイルからこの情報を取得し、クライアント アプリケーションがフォーム サーバー自体をアクティブ化するオーバーヘッドなしにこの情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="53874-107">The form manager gets this information from the appropriate form configuration file so that client applications can use this information without the overhead of activating the form server itself.</span></span> <span data-ttu-id="53874-108">これを行うには、クライアント アプリケーションは [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) メソッドを次のように呼び出します。</span><span class="sxs-lookup"><span data-stu-id="53874-108">To do this, the client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method as follows:</span></span> 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

<span data-ttu-id="53874-109">**ResolveMessageClass** の 3 番目の引数は、クエリがフォーム サーバーを検索する関連付けられたコンテンツ テーブルを含むフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="53874-109">Note that the third argument to **ResolveMessageClass** is the folder that contains the associated contents table that the query will search for form servers.</span></span> <span data-ttu-id="53874-110">NULL は、フォーム マネージャーが使用可能なすべてのフォーム コンテナーを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53874-110">NULL indicates that the form manager should search all available form containers.</span></span> <span data-ttu-id="53874-111">クエリを特定のフォルダーに対して実行する場合は、代わりに適切な [IMAPIFolder](imapifolderimapicontainer.md) ポインターを含める方が良いです。</span><span class="sxs-lookup"><span data-stu-id="53874-111">If the query is to run against a particular folder, it is better to include the appropriate [IMAPIFolder](imapifolderimapicontainer.md) pointer instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53874-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="53874-112">See also</span></span>



[<span data-ttu-id="53874-113">フォーム サーバーの操作</span><span class="sxs-lookup"><span data-stu-id="53874-113">Form Server Interactions</span></span>](form-server-interactions.md)

