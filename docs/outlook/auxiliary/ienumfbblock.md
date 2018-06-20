---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799347"
---
# <a name="ienumfbblock"></a><span data-ttu-id="ab2bc-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="ab2bc-102">IEnumFBBlock</span></span>

<span data-ttu-id="ab2bc-103">アクセスと時間の範囲内でのユーザーのデータのブロックの空き時間情報の列挙をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ab2bc-104">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ab2bc-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab2bc-105">継承します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="ab2bc-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab2bc-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="ab2bc-107">提供元:</span><span class="sxs-lookup"><span data-stu-id="ab2bc-107">Provided by:</span></span>  <br/> |<span data-ttu-id="ab2bc-108">プロバイダーの空き/予約済み</span><span class="sxs-lookup"><span data-stu-id="ab2bc-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="ab2bc-109">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ab2bc-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="ab2bc-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ab2bc-111">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="ab2bc-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ab2bc-112">Next/次のレコード</span><span class="sxs-lookup"><span data-stu-id="ab2bc-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="ab2bc-113">列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="ab2bc-114">スキップ</span><span class="sxs-lookup"><span data-stu-id="ab2bc-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="ab2bc-115">指定された空き時間情報データのブロック数をスキップします。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="ab2bc-116">Reset</span><span class="sxs-lookup"><span data-stu-id="ab2bc-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="ab2bc-117">先頭にカーソルを設定することにより、列挙子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="ab2bc-118">Clone</span><span class="sxs-lookup"><span data-stu-id="ab2bc-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="ab2bc-119">同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="ab2bc-120">制限します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="ab2bc-121">指定した期間内に列挙型を制限します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab2bc-122">備考</span><span class="sxs-lookup"><span data-stu-id="ab2bc-122">Remarks</span></span>

<span data-ttu-id="ab2bc-123">列挙体には、時間が重複しないデータのブロック空き時間情報にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="ab2bc-124">これらの項目の優先順位に基づいて列挙体の空き/予約済みブロックの重複を形成する結合 Outlook の予定表に重複する項目がある場合は、: 不在時の予定あり、仮の予定です。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="ab2bc-125">空き/予約済みのプロバイダーは、このインターフェイスは、 [IFreeBusyData](ifreebusydata.md)を使用してユーザーの時間範囲の列挙体を取得します。</span><span class="sxs-lookup"><span data-stu-id="ab2bc-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab2bc-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab2bc-126">See also</span></span>

- [<span data-ttu-id="ab2bc-127">空き時間情報 API について</span><span class="sxs-lookup"><span data-stu-id="ab2bc-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="ab2bc-128">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="ab2bc-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="ab2bc-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="ab2bc-129">IFreeBusyData</span></span>](ifreebusydata.md)

