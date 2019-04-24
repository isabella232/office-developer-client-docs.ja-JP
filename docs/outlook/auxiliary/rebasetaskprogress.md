---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 予定の列挙およびリベースの進行状況を報告します。
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326454"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="5700e-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="5700e-103">RebaseTaskProgress</span></span>

<span data-ttu-id="5700e-104">予定の列挙およびリベースの進行状況を報告します。</span><span class="sxs-lookup"><span data-stu-id="5700e-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5700e-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5700e-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5700e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5700e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5700e-107">、tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="5700e-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="5700e-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5700e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5700e-109">MAPI クライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="5700e-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="5700e-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5700e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5700e-111">Outlook のリベース/再配置オブジェクト</span><span class="sxs-lookup"><span data-stu-id="5700e-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="5700e-112">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="5700e-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="5700e-113">、tzmovelib.h で定義されている**PFNREBASETASKPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5700e-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="5700e-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5700e-114">Parameters</span></span>

<span data-ttu-id="5700e-115">_ulmin_</span><span class="sxs-lookup"><span data-stu-id="5700e-115">_ulMin_</span></span>
  
> <span data-ttu-id="5700e-116">順番処理されている予定の範囲の下限。</span><span class="sxs-lookup"><span data-stu-id="5700e-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="5700e-117">通常は0になります。</span><span class="sxs-lookup"><span data-stu-id="5700e-117">It is usually zero.</span></span>
    
<span data-ttu-id="5700e-118">_ulmax_</span><span class="sxs-lookup"><span data-stu-id="5700e-118">_ulMax_</span></span>
  
> <span data-ttu-id="5700e-119">順番処理されている予定の範囲の上限です。</span><span class="sxs-lookup"><span data-stu-id="5700e-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="5700e-120">通常は、処理されている予定表フォルダー内のアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="5700e-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="5700e-121">_ulcur_</span><span class="sxs-lookup"><span data-stu-id="5700e-121">_ulCur_</span></span>
  
> <span data-ttu-id="5700e-122">順番処理されている現在のアイテムです。</span><span class="sxs-lookup"><span data-stu-id="5700e-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="5700e-123">_State_</span><span class="sxs-lookup"><span data-stu-id="5700e-123">_State_</span></span>
  
> <span data-ttu-id="5700e-124">順番処理されているアイテムの状態を示す値。</span><span class="sxs-lookup"><span data-stu-id="5700e-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="5700e-125">列挙**REBASE_APPT_STATE**は、tzmovelib.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="5700e-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="5700e-126">_State_ は、次のいずれかの値です。</span><span class="sxs-lookup"><span data-stu-id="5700e-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="5700e-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** -アイテムをスキャンし、検査します。</span><span class="sxs-lookup"><span data-stu-id="5700e-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="5700e-128">**REBASE_APPT_STATE_SCANNING_FOUND** —アイテムをスキャンして検出しました。</span><span class="sxs-lookup"><span data-stu-id="5700e-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="5700e-129">**REBASE_APPT_STATE_BEGIN** —アイテムを修正して開始します。</span><span class="sxs-lookup"><span data-stu-id="5700e-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="5700e-130">**REBASE_APPT_STATE_REBASING** —アイテムを修正し、調整します。</span><span class="sxs-lookup"><span data-stu-id="5700e-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="5700e-131">**REBASE_APPT_STATE_SENDING** —会議の更新を修正し、送信します。</span><span class="sxs-lookup"><span data-stu-id="5700e-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="5700e-132">**REBASE_APPT_STATE_DONE** —アイテムを修正して実行します。</span><span class="sxs-lookup"><span data-stu-id="5700e-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="5700e-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="5700e-133">_pRowCur_</span></span>
  
> <span data-ttu-id="5700e-134">順番スキャンまたは固定されているアイテムを記述する**[srow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5700e-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5700e-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="5700e-135">Return values</span></span>

<span data-ttu-id="5700e-136">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="5700e-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5700e-137">解説</span><span class="sxs-lookup"><span data-stu-id="5700e-137">Remarks</span></span>

<span data-ttu-id="5700e-138">[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアントアプリケーションは、この関数を実装してアイテム処理を追跡します。</span><span class="sxs-lookup"><span data-stu-id="5700e-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5700e-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="5700e-139">See also</span></span>

- [<span data-ttu-id="5700e-140">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="5700e-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

