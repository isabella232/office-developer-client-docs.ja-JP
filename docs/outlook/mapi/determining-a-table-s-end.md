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
# <a name="determining-a-tables-end"></a><span data-ttu-id="ce753-103">テーブルの終了を決定する</span><span class="sxs-lookup"><span data-stu-id="ce753-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="ce753-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce753-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ce753-105">一般的なエラーは、次の場合にテーブルの末尾に達したと仮定します。</span><span class="sxs-lookup"><span data-stu-id="ce753-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="ce753-106">[IMAPITable::QueryRows](imapitable-queryrows.md) はループ内で呼び出され、ループの終了は [IMAPITable::GetRowCount](imapitable-getrowcount.md)によって返される行数によって決まります。</span><span class="sxs-lookup"><span data-stu-id="ce753-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="ce753-107">**GetRowCount が返す** 数は、必ずしもテーブル内の行の正確な数を表すとは限らない。概算数です。</span><span class="sxs-lookup"><span data-stu-id="ce753-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="ce753-108">**QueryRows は** 固定数の行で呼び出され、返される行数は少なめになります。</span><span class="sxs-lookup"><span data-stu-id="ce753-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="ce753-109">**QueryRows** が 0 に等しい行数を持つ行セットを返すまで、取得する行がこれ以上ない。</span><span class="sxs-lookup"><span data-stu-id="ce753-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="ce753-110">呼び出し元が、正の行数の表の末尾、または負の行数の表の先頭にカーソルが配置されたと仮定できる唯一の時間は、値 S_OK とゼロ行が返される場合です。</span><span class="sxs-lookup"><span data-stu-id="ce753-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="ce753-111">この値MAPI_E_NOT_FOUND返されません。</span><span class="sxs-lookup"><span data-stu-id="ce753-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce753-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce753-112">See also</span></span>



[<span data-ttu-id="ce753-113">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="ce753-113">MAPI Tables</span></span>](mapi-tables.md)

