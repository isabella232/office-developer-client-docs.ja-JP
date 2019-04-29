---
title: テーブルの終了を決定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420088"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="59e9b-103">テーブルの終了を決定する</span><span class="sxs-lookup"><span data-stu-id="59e9b-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="59e9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59e9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="59e9b-105">一般的なエラーは、次のような場合にテーブルの最後に到達したと仮定します。</span><span class="sxs-lookup"><span data-stu-id="59e9b-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="59e9b-106">[imapitable:: QueryRows](imapitable-queryrows.md)がループで呼び出され、 [IMAPITable:: getrowcount](imapitable-getrowcount.md)から返される行の数によってループの終わりが決定されます。</span><span class="sxs-lookup"><span data-stu-id="59e9b-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="59e9b-107">**getrowcount**が返すカウントは、必ずしもテーブル内の行数の正確な数を表すわけではありません。これはおおよそのカウントです。</span><span class="sxs-lookup"><span data-stu-id="59e9b-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="59e9b-108">**QueryRows**は固定数の行で呼び出されており、返される行が少なくなっています。</span><span class="sxs-lookup"><span data-stu-id="59e9b-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="59e9b-109">**QueryRows**は、行数が0である行セットを返し、それ以上行を取得しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="59e9b-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="59e9b-110">呼び出し元が、カーソルが正の行数の場合はテーブルの末尾に配置されていること、または負の行数に対してテーブルの先頭にある場合は、値 S_OK および0の行が返された場合のみ、そのことを前提とすることができます。</span><span class="sxs-lookup"><span data-stu-id="59e9b-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="59e9b-111">値 MAPI_E_NOT_FOUND は返されません。</span><span class="sxs-lookup"><span data-stu-id="59e9b-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59e9b-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="59e9b-112">See also</span></span>



[<span data-ttu-id="59e9b-113">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="59e9b-113">MAPI Tables</span></span>](mapi-tables.md)

