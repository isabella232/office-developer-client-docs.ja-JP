---
title: 小数値によるテーブルの位置設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579698"
---
# <a name="setting-table-position-with-a-fractional-value"></a><span data-ttu-id="98a5b-103">小数値によるテーブルの位置設定</span><span class="sxs-lookup"><span data-stu-id="98a5b-103">Setting Table Position with a Fractional Value</span></span>

  
  
<span data-ttu-id="98a5b-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98a5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98a5b-105">テーブルのユーザーは、合計を基準にして行のおおよその割合を表す位置に移動できます。</span><span class="sxs-lookup"><span data-stu-id="98a5b-105">Table users can move to a position that represents an approximate percentage of rows in relation to the total.</span></span> <span data-ttu-id="98a5b-106">行を正確に移動するのではなく分割を配置するのには、このメソッドの部分にテーブルに基づく分数。</span><span class="sxs-lookup"><span data-stu-id="98a5b-106">Rather than moving to an exact row, this method of positioning divides the table into portions based on fractions.</span></span> <span data-ttu-id="98a5b-107">テーブルのユーザーは、テーブルの半分のポイントに、またはテーブルを使用する方法の 7/8 の行に移動できます。</span><span class="sxs-lookup"><span data-stu-id="98a5b-107">Table users can move, for example, to a table's half-way point or to the row that is 7/8 of the way through the table.</span></span> 
  
 <span data-ttu-id="98a5b-108">**カーソル行のおおよその数を移動するには**</span><span class="sxs-lookup"><span data-stu-id="98a5b-108">**To move the cursor an approximate number of rows**</span></span>
  
- <span data-ttu-id="98a5b-109">[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98a5b-109">Call [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md).</span></span> <span data-ttu-id="98a5b-110">**SeekRowApprox**は、テーブルの先頭を基準にして行の特定のパーセントを表す行に移動します。</span><span class="sxs-lookup"><span data-stu-id="98a5b-110">**SeekRowApprox** moves to the row that represents a particular percentage of rows in relation to the beginning of the table.</span></span> <span data-ttu-id="98a5b-111">この割合は、 _ulNumerator_および_ulDenominator_パラメーターで指定されます。</span><span class="sxs-lookup"><span data-stu-id="98a5b-111">This percentage is specified in the  _ulNumerator_ and  _ulDenominator_ parameters.</span></span> <span data-ttu-id="98a5b-112">**SeekRowApprox**は、スクロール バーを実装するために頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="98a5b-112">**SeekRowApprox** is used frequently to implement scroll bars.</span></span> 
    
 <span data-ttu-id="98a5b-113">**テーブルのおおよその位置を決定するには**</span><span class="sxs-lookup"><span data-stu-id="98a5b-113">**To determine a table's approximate position**</span></span>
  
- <span data-ttu-id="98a5b-114">[IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="98a5b-114">Call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="98a5b-115">**QueryPosition**は、ユーザーの現在位置を通知するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="98a5b-115">**QueryPosition** can be used to inform the user of the current position.</span></span> <span data-ttu-id="98a5b-116">小数部の値がテーブル内の行の数および現在の行の数に基づいて設定します。</span><span class="sxs-lookup"><span data-stu-id="98a5b-116">It sets a fractional value based on the number of rows in the table and the number of the current row.</span></span> <span data-ttu-id="98a5b-117">この値が近似値を表すことを期待します。</span><span class="sxs-lookup"><span data-stu-id="98a5b-117">Expect that this value represents an approximation.</span></span> <span data-ttu-id="98a5b-118">テーブルの実装側は、正確な実装を呼び出すには、分類されたテーブルでは特に高価なことができるため、正確な位置を計算していないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98a5b-118">Table implementers are encouraged not to calculate the exact position because accurate implementations can be expensive to invoke, especially on categorized tables.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="98a5b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="98a5b-119">See also</span></span>



[<span data-ttu-id="98a5b-120">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="98a5b-120">MAPI Tables</span></span>](mapi-tables.md)

