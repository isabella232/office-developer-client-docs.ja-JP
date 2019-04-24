---
title: 列と制限の設定後のテーブルの並べ替え
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57db0314-1df0-4fd2-b443-223b0512f1ad
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 62220794f325165e67db5397da2795d49959ef60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344486"
---
# <a name="sorting-tables-after-setting-columns-and-restrictions"></a><span data-ttu-id="4bafe-103">列と制限の設定後のテーブルの並べ替え</span><span class="sxs-lookup"><span data-stu-id="4bafe-103">Sorting Tables After Setting Columns and Restrictions</span></span>

  
  
<span data-ttu-id="4bafe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bafe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bafe-105">並べ替えられたテーブルの表示を制限する必要がある場合は、常に次の順序で**IMAPITable**呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="4bafe-105">When you need to limit the view of a sorted table, always make the following **IMAPITable** calls in the following order:</span></span> 
  
1. <span data-ttu-id="4bafe-106">[IMAPITable:: SetColumns](imapitable-setcolumns.md)列セットを定義します。</span><span class="sxs-lookup"><span data-stu-id="4bafe-106">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define the column set.</span></span> 
    
2. <span data-ttu-id="4bafe-107">[IMAPITable::](imapitable-restrict.md)制限を課すことができます。</span><span class="sxs-lookup"><span data-stu-id="4bafe-107">[IMAPITable::Restrict](imapitable-restrict.md) to impose the restriction.</span></span> 
    
3. <span data-ttu-id="4bafe-108">[IMAPITable::](imapitable-sorttable.md)並べ替えを実行するための sorttable。</span><span class="sxs-lookup"><span data-stu-id="4bafe-108">[IMAPITable::SortTable](imapitable-sorttable.md) to perform the sort.</span></span> 
    
<span data-ttu-id="4bafe-109">並べ替えられたテーブルが分類されている場合は、必要に応じて**sorttable**の呼び出しの後に、 [IMAPITable:: SetCollapseState](imapitable-setcollapsestate.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4bafe-109">If the sorted table is categorized, make a call to [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md), if necessary, after the **SortTable** call.</span></span> <span data-ttu-id="4bafe-110">ほとんどのサービスプロバイダーは、最高のパフォーマンスを実現するために最後のタスクとしてテーブルを並べ替えるので、この呼び出しの順序は重要です。</span><span class="sxs-lookup"><span data-stu-id="4bafe-110">This ordering of calls is important because most service providers sort a table as the last task to achieve the best performance.</span></span> <span data-ttu-id="4bafe-111">たとえば、メッセージストアプロバイダーが、制限を設定する前にフォルダーの内容テーブルを分類する必要がある場合、この分類は制限の処理中に削除されます。</span><span class="sxs-lookup"><span data-stu-id="4bafe-111">If, for example, a message store provider must categorize a folder contents table before a restriction can be imposed, this categorization will be removed during the processing of the restriction.</span></span> <span data-ttu-id="4bafe-112">2番目の分類が必要になります。</span><span class="sxs-lookup"><span data-stu-id="4bafe-112">A second categorization will be necessary.</span></span> 
  

