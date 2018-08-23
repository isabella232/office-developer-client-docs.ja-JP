---
title: 小さいテーブルに対する QueryRows の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589337"
---
# <a name="calling-queryrows-for-small-tables"></a><span data-ttu-id="0ebe0-103">小さいテーブルに対する QueryRows の呼び出し</span><span class="sxs-lookup"><span data-stu-id="0ebe0-103">Calling QueryRows for Small Tables</span></span>

  
  
<span data-ttu-id="0ebe0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ebe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ebe0-105">小さなテーブルから行を検索する場合は、最初に制約を作成する代わりに[IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-105">When retrieving rows from a small table, call [IMAPITable::QueryRows](imapitable-queryrows.md) instead of first building a restriction.</span></span> <span data-ttu-id="0ebe0-106">制限、パフォーマンスに与える影響を作成するは、プロバイダーがテーブルをまず作成する必要がありますので、元のテーブルに一致する行を検索し、新しいテーブルに行をコピーします。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-106">Creating a restriction impacts performance because the provider must first create a table, find the matching rows in the original table, and then copy the rows to the new table.</span></span> <span data-ttu-id="0ebe0-107">テーブル内の行の合計数が 100 未満の場合は、すべての行を読み取るし、該当する行を見つけるには、 [IMAPITable::FindRow](imapitable-findrow.md)を呼び出すにはより効果的な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-107">If the total number of rows in the table is less than 100, it is probably more effective to read all of the rows and then call [IMAPITable::FindRow](imapitable-findrow.md) to find the appropriate row.</span></span> <span data-ttu-id="0ebe0-108">これは、この情報が常時必要な場合に特に効果的な戦略です。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-108">This is a particularly good strategy if this information is needed only occasionally.</span></span> 
  
<span data-ttu-id="0ebe0-109">制限を使用する適切な時間は、制限またはフィルタ リングされた情報が長い期間にわたって使用されるか、頻繁に使用されるときです。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-109">The proper time to use a restriction is when the restricted or filtered information will be used over a longer period of time or used frequently.</span></span> <span data-ttu-id="0ebe0-110">未読のメッセージでは、ビューが常に必要がある場合、この制限は適切な呼び出しを使用するになります。</span><span class="sxs-lookup"><span data-stu-id="0ebe0-110">For instance, if you always need a view with unread messages, then a restriction is the proper call to use.</span></span>
  

