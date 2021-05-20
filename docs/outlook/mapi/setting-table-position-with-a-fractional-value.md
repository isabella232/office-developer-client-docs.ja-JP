---
title: 小数部の値を使用してテーブルの位置を設定する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437337"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="a8535-103">小数部の値を使用してテーブルの位置を設定する</span><span class="sxs-lookup"><span data-stu-id="a8535-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="a8535-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8535-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8535-105">テーブル ユーザーは、合計に対する行のおよその割合を表す位置に移動できます。</span><span class="sxs-lookup"><span data-stu-id="a8535-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="a8535-106">正確な行に移動するのではなく、この配置方法では、表を分数に基づいて部分に分割します。</span><span class="sxs-lookup"><span data-stu-id="a8535-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="a8535-107">テーブル ユーザーは、たとえば、テーブルの中途半端なポイントに移動したり、テーブルの 7/8 の行に移動できます。</span><span class="sxs-lookup"><span data-stu-id="a8535-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="a8535-108">**カーソルを移動するには、およその行数**</span><span class="sxs-lookup"><span data-stu-id="a8535-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="a8535-109">[IMAPITable::SeekRowApprox を呼び出します](imapitable-seekrowapprox.md)。</span><span class="sxs-lookup"><span data-stu-id="a8535-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="a8535-110">**SeekRowApprox は** 、表の先頭に関連する行の特定の割合を表す行に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8535-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="a8535-111">このパーセンテージは  _、ulNumerator パラメーター_ と  _ulDenominator パラメーターで指定_ されます。</span><span class="sxs-lookup"><span data-stu-id="a8535-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="a8535-112">**SeekRowApprox は、** スクロール バーを実装するために頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a8535-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="a8535-113">**テーブルのおおよその位置を決定するには**</span><span class="sxs-lookup"><span data-stu-id="a8535-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="a8535-114">[IMAPITable::QueryPosition を呼び出します](imapitable-queryposition.md)。</span><span class="sxs-lookup"><span data-stu-id="a8535-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="a8535-115">**QueryPosition** を使用して、現在の位置をユーザーに通知できます。</span><span class="sxs-lookup"><span data-stu-id="a8535-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="a8535-116">テーブル内の行数と現在の行の数に基づいて小数部の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a8535-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="a8535-117">この値が近似値を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8535-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="a8535-118">正確な実装は、特に分類されたテーブルでは、呼び出すのにコストがかかる可能性があるため、テーブル実装者は正確な位置を計算しないのでお勧めしています。</span><span class="sxs-lookup"><span data-stu-id="a8535-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8535-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8535-119">See also</span></span>



[<span data-ttu-id="a8535-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="a8535-120">MAPI Tables</span></span>](mapi-tables.md)

