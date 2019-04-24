---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317627"
---
# <a name="ienumfbblock"></a><span data-ttu-id="51778-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="51778-102">IEnumFBBlock</span></span>

<span data-ttu-id="51778-103">時間範囲内のユーザーのデータの空き時間情報ブロックへのアクセスと列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="51778-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="51778-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="51778-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51778-105">継承元:</span><span class="sxs-lookup"><span data-stu-id="51778-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="51778-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="51778-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="51778-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="51778-107">Provided by:</span></span>  <br/> |<span data-ttu-id="51778-108">空き時間情報プロバイダー</span><span class="sxs-lookup"><span data-stu-id="51778-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="51778-109">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="51778-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="51778-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="51778-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="51778-111">v の順序</span><span class="sxs-lookup"><span data-stu-id="51778-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="51778-112">Next</span><span class="sxs-lookup"><span data-stu-id="51778-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="51778-113">列挙で、次に指定された空き時間情報データのブロック数を取得します。</span><span class="sxs-lookup"><span data-stu-id="51778-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="51778-114">Skip</span><span class="sxs-lookup"><span data-stu-id="51778-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="51778-115">空き時間情報データの指定した数のブロックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="51778-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="51778-116">Reset</span><span class="sxs-lookup"><span data-stu-id="51778-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="51778-117">カーソルを先頭に設定して、列挙子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="51778-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="51778-118">Clone</span><span class="sxs-lookup"><span data-stu-id="51778-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="51778-119">同じ時間制限を使用して列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。</span><span class="sxs-lookup"><span data-stu-id="51778-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="51778-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="51778-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="51778-121">列挙を指定した期間に制限します。</span><span class="sxs-lookup"><span data-stu-id="51778-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51778-122">解説</span><span class="sxs-lookup"><span data-stu-id="51778-122">Remarks</span></span>

<span data-ttu-id="51778-123">列挙には、時間内に重複しないデータの空き時間ブロックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="51778-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="51778-124">予定表に重複するアイテムがある場合、Outlook はこれらのアイテムを結合して、この優先順位 (不在、取り込み中、仮承諾) に基づいて列挙で重複しない空き時間ブロックを形成します。</span><span class="sxs-lookup"><span data-stu-id="51778-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="51778-125">空き時間情報プロバイダーは、このインターフェイスと、 [IFreeBusyData](ifreebusydata.md)を通じてユーザーの時間範囲の列挙を取得します。</span><span class="sxs-lookup"><span data-stu-id="51778-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51778-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="51778-126">See also</span></span>

- [<span data-ttu-id="51778-127">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="51778-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="51778-128">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="51778-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="51778-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="51778-129">IFreeBusyData</span></span>](ifreebusydata.md)

