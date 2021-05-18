---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 予定の列挙と再適用の進行状況を報告します。
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326454"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="6b37b-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="6b37b-103">RebaseTaskProgress</span></span>

<span data-ttu-id="6b37b-104">予定の列挙と再適用の進行状況を報告します。</span><span class="sxs-lookup"><span data-stu-id="6b37b-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6b37b-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="6b37b-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b37b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6b37b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b37b-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="6b37b-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="6b37b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6b37b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b37b-109">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6b37b-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="6b37b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6b37b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b37b-111">Outlook の再basing オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6b37b-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="6b37b-112">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="6b37b-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="6b37b-113">tzmovelib.h で定義されている **PFNREBASETASKPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="6b37b-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="6b37b-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b37b-114">Parameters</span></span>

<span data-ttu-id="6b37b-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="6b37b-115">_ulMin_</span></span>
  
> <span data-ttu-id="6b37b-116">[in]処理される予定の範囲の低い端。</span><span class="sxs-lookup"><span data-stu-id="6b37b-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="6b37b-117">通常は 0 です。</span><span class="sxs-lookup"><span data-stu-id="6b37b-117">It is usually zero.</span></span>
    
<span data-ttu-id="6b37b-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="6b37b-118">_ulMax_</span></span>
  
> <span data-ttu-id="6b37b-119">[in]処理される予定の範囲の高端。</span><span class="sxs-lookup"><span data-stu-id="6b37b-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="6b37b-120">これは通常、処理される予定表フォルダー内のアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="6b37b-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="6b37b-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="6b37b-121">_ulCur_</span></span>
  
> <span data-ttu-id="6b37b-122">[in]現在処理されているアイテム。</span><span class="sxs-lookup"><span data-stu-id="6b37b-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="6b37b-123">_State_</span><span class="sxs-lookup"><span data-stu-id="6b37b-123">_State_</span></span>
  
> <span data-ttu-id="6b37b-124">[in]処理されるアイテムの状態を示す値。</span><span class="sxs-lookup"><span data-stu-id="6b37b-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="6b37b-125">列挙型 **REBASE_APPT_STATE** tzmovelib.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="6b37b-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="6b37b-126">_State_ は、次のいずれかの値です。</span><span class="sxs-lookup"><span data-stu-id="6b37b-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="6b37b-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —アイテムをスキャンして調べる。</span><span class="sxs-lookup"><span data-stu-id="6b37b-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="6b37b-128">**REBASE_APPT_STATE_SCANNING_FOUND** — アイテムをスキャンして見つかりました。</span><span class="sxs-lookup"><span data-stu-id="6b37b-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="6b37b-129">**REBASE_APPT_STATE_BEGIN** —アイテムの固定と開始。</span><span class="sxs-lookup"><span data-stu-id="6b37b-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="6b37b-130">**REBASE_APPT_STATE_REBASING** —アイテムの固定と調整。</span><span class="sxs-lookup"><span data-stu-id="6b37b-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="6b37b-131">**REBASE_APPT_STATE_SENDING** —会議の更新プログラムを修正して送信します。</span><span class="sxs-lookup"><span data-stu-id="6b37b-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="6b37b-132">**REBASE_APPT_STATE_DONE** —アイテムを修正して完了します。</span><span class="sxs-lookup"><span data-stu-id="6b37b-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="6b37b-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="6b37b-133">_pRowCur_</span></span>
  
> <span data-ttu-id="6b37b-134">[in]スキャンまたは修正されるアイテムを記述する **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b37b-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6b37b-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="6b37b-135">Return values</span></span>

<span data-ttu-id="6b37b-136">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="6b37b-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b37b-137">注釈</span><span class="sxs-lookup"><span data-stu-id="6b37b-137">Remarks</span></span>

<span data-ttu-id="6b37b-138">[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、アイテム処理を追跡するためにこの関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="6b37b-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b37b-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b37b-139">See also</span></span>

- [<span data-ttu-id="6b37b-140">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="6b37b-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

