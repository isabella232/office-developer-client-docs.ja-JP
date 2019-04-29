---
title: 小さなテーブルに対する QueryRows の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404177"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="c836d-103">小さなテーブルに対する QueryRows の呼び出し</span><span class="sxs-lookup"><span data-stu-id="c836d-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="c836d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c836d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c836d-105">小さなテーブルから行を取得するときは、最初に制限を作成するのではなく、 [IMAPITable:: QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c836d-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="c836d-106">プロバイダーが最初にテーブルを作成し、その後、元のテーブルで一致する行を見つけて、その行を新しいテーブルにコピーする必要があるため、制限の作成はパフォーマンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="c836d-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="c836d-107">表の行数の合計が100よりも低い場合は、すべての行を読み取ってから、 [IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して適切な行を検索する方が効率がよいでしょう。</span><span class="sxs-lookup"><span data-stu-id="c836d-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="c836d-108">これは、この情報がたまにしか必要ない場合に特に適した戦略です。</span><span class="sxs-lookup"><span data-stu-id="c836d-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="c836d-109">制限を適切に使用するには、制限またはフィルター処理された情報を長期間にわたって使用したり、頻繁に使用したりすることが適切な時間です。</span><span class="sxs-lookup"><span data-stu-id="c836d-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="c836d-110">たとえば、未読メッセージがあるビューが常に必要な場合は、適切な呼び出しを使用するように制限を行います。</span><span class="sxs-lookup"><span data-stu-id="c836d-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

