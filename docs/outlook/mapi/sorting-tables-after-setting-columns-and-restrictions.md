---
title: 列および制限の設定後のテーブルの並べ替え
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9e75143cb59e782993b9a7f9937432f0b4894d5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803988"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="dd4b2-103">列および制限の設定後のテーブルの並べ替え</span><span class="sxs-lookup"><span data-stu-id="dd4b2-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="dd4b2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dd4b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dd4b2-105">並べ替えられたテーブルのビューを制限するには、常に確認する必要があります次**IMAPITable**は次の順序で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="dd4b2-106">列を定義する[IMAPITable::SetColumns](imapitable-setcolumns.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="dd4b2-107">[IMAPITable::Restrict](imapitable-restrict.md)の制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="dd4b2-108">[IMAPITable::SortTable](imapitable-sorttable.md)の並べ替えを実行します。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="dd4b2-109">ソート後のテーブルを分類すると場合、呼び出しを行う[IMAPITable::SetCollapseState](imapitable-setcollapsestate.md)、必要に応じて、 **SortTable**の呼び出しの後です。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="dd4b2-110">ほとんどのサービス プロバイダーは、最高のパフォーマンスを達成するために最後のタスクとしてテーブルを並べ替えるために、この呼び出しの順序が重要です。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="dd4b2-111">などの制限が適用される前に、メッセージ ストア プロバイダーはフォルダーの内容のテーブルを分類する必要がある場合は、この分類は、制限の処理中に削除されます。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="dd4b2-112">2 つ目の分類は、必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd4b2-112">A second categorization will be necessary.</span></span> 
  

