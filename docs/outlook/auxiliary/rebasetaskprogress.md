---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: 列挙体は、単独の予定の再配置の進行状況を報告します。
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799585"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="0c05c-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="0c05c-103">RebaseTaskProgress</span></span>

<span data-ttu-id="0c05c-104">列挙体は、単独の予定の再配置の進行状況を報告します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0c05c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0c05c-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c05c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c05c-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c05c-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="0c05c-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="0c05c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0c05c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c05c-109">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0c05c-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="0c05c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0c05c-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c05c-111">Outlook の再配置オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0c05c-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="0c05c-112">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="0c05c-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="0c05c-113">**PFNREBASETASKPROGRESS** tzmovelib.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="0c05c-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="0c05c-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c05c-114">Parameters</span></span>

<span data-ttu-id="0c05c-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="0c05c-115">_ulMin_</span></span>
  
> <span data-ttu-id="0c05c-116">[in]処理中の予定の範囲の下限です。</span><span class="sxs-lookup"><span data-stu-id="0c05c-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="0c05c-117">一般的には、ゼロです。</span><span class="sxs-lookup"><span data-stu-id="0c05c-117">It is usually zero.</span></span>
    
<span data-ttu-id="0c05c-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="0c05c-118">_ulMax_</span></span>
  
> <span data-ttu-id="0c05c-119">[in]処理中の予定の範囲の上限です。</span><span class="sxs-lookup"><span data-stu-id="0c05c-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="0c05c-120">これは、通常、処理中の予定表フォルダー内のアイテムの数です。</span><span class="sxs-lookup"><span data-stu-id="0c05c-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="0c05c-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="0c05c-121">_ulCur_</span></span>
  
> <span data-ttu-id="0c05c-122">[in]処理されている現在の項目。</span><span class="sxs-lookup"><span data-stu-id="0c05c-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="0c05c-123">_State_</span><span class="sxs-lookup"><span data-stu-id="0c05c-123">_State_</span></span>
  
> <span data-ttu-id="0c05c-124">[in]処理されている項目のステータスを示す値。</span><span class="sxs-lookup"><span data-stu-id="0c05c-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="0c05c-125">**REBASE_APPT_STATE**列挙体は、tzmovelib.h で定義されます。</span><span class="sxs-lookup"><span data-stu-id="0c05c-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="0c05c-126">_状態_は、次の値のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0c05c-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="0c05c-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** -スキャンし、項目を確認します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="0c05c-128">**REBASE_APPT_STATE_SCANNING_FOUND** -スキャンの項目が見つかったとします。</span><span class="sxs-lookup"><span data-stu-id="0c05c-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="0c05c-129">**REBASE_APPT_STATE_BEGIN** -修正および項目を開始します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="0c05c-130">**REBASE_APPT_STATE_REBASING** -修正および項目を調整します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="0c05c-131">**REBASE_APPT_STATE_SENDING** -修正し、会議の更新を送信します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="0c05c-132">**REBASE_APPT_STATE_DONE** : 解決であり、項目を実行します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="0c05c-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="0c05c-133">_pRowCur_</span></span>
  
> <span data-ttu-id="0c05c-134">[in]スキャンまたは固定されている項目を説明する**[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c05c-134">[in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="0c05c-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="0c05c-135">Return values</span></span>

<span data-ttu-id="0c05c-136">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="0c05c-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0c05c-137">解釈</span><span class="sxs-lookup"><span data-stu-id="0c05c-137">Remarks</span></span>

<span data-ttu-id="0c05c-138">[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、項目の処理を追跡するためにこの関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="0c05c-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c05c-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c05c-139">See also</span></span>

- [<span data-ttu-id="0c05c-140">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="0c05c-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

