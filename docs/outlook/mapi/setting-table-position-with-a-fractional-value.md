---
title: 小数値によるテーブルの位置設定
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
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="42477-103">小数値によるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="42477-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="42477-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42477-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42477-105">Table ユーザーは、合計に対する行のおおよそのパーセンテージを表す位置に移動できます。</span><span class="sxs-lookup"><span data-stu-id="42477-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="42477-106">この配置方法では、正確な行に移動するのではなく、分数に基づいてテーブルを複数の部分に分割します。</span><span class="sxs-lookup"><span data-stu-id="42477-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="42477-107">表ユーザーは、たとえば、表の中の半方向の位置、または表の中から7/8 の行に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="42477-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="42477-108">**行の概数をカーソルを移動するには**</span><span class="sxs-lookup"><span data-stu-id="42477-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="42477-109">呼び出し[IMAPITable:: seekrowapprox](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="42477-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="42477-110">**seekrowapprox**は、テーブルの先頭を基準にして、特定のパーセンテージの行を表す行に移動します。</span><span class="sxs-lookup"><span data-stu-id="42477-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="42477-111">このパーセンテージは_ulnumerator_パラメーターと_ulnumerator_パラメーターで指定されています。</span><span class="sxs-lookup"><span data-stu-id="42477-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="42477-112">**seekrowapprox**は、スクロールバーを実装するためによく使用されます。</span><span class="sxs-lookup"><span data-stu-id="42477-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="42477-113">**表のおおよその位置を確認するには**</span><span class="sxs-lookup"><span data-stu-id="42477-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="42477-114">呼び出し[IMAPITable:: queryposition](imapitable-queryposition.md)。</span><span class="sxs-lookup"><span data-stu-id="42477-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="42477-115">**queryposition**は、現在の位置をユーザーに通知するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="42477-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="42477-116">表の行数と現在の行の数に基づいて、小数値を設定します。</span><span class="sxs-lookup"><span data-stu-id="42477-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="42477-117">この値は近似値を表すものと想定します。</span><span class="sxs-lookup"><span data-stu-id="42477-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="42477-118">表の実装では、厳密な実装は、特に、カテゴリ化されたテーブルでは、正確に実装するのにコストがかかるため、正確な位置を計算しないことをお勧め</span><span class="sxs-lookup"><span data-stu-id="42477-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="42477-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="42477-119">See also</span></span>



[<span data-ttu-id="42477-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="42477-120">MAPI Tables</span></span>](mapi-tables.md)

