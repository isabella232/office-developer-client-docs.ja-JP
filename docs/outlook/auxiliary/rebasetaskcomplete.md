---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: 予定の再配置の完了を報告します。
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388918"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="c7544-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="c7544-103">RebaseTaskComplete</span></span>

<span data-ttu-id="c7544-104">予定の再配置の完了を報告します。</span><span class="sxs-lookup"><span data-stu-id="c7544-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c7544-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c7544-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7544-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c7544-106">Header file:</span></span>  <br/> |<span data-ttu-id="c7544-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="c7544-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="c7544-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c7544-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c7544-109">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c7544-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="c7544-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c7544-110">Called by:</span></span>  <br/> |<span data-ttu-id="c7544-111">Outlook の再配置オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c7544-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="c7544-112">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="c7544-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="c7544-113">**PFNREBASETASKCOMPLETE** tzmovelib.h で定義されています。</span><span class="sxs-lookup"><span data-stu-id="c7544-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="c7544-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c7544-114">Parameters</span></span>

<span data-ttu-id="c7544-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="c7544-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="c7544-116">[in]処理された行です。</span><span class="sxs-lookup"><span data-stu-id="c7544-116">[in] The row that was processed.</span></span> <span data-ttu-id="c7544-117">このインデックスは、 [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)に渡される**[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** 構造体を指します。</span><span class="sxs-lookup"><span data-stu-id="c7544-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="c7544-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="c7544-118">_pRowCur_</span></span>
  
> <span data-ttu-id="c7544-119">in] 項目が処理されたことを説明する**[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c7544-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="c7544-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="c7544-120">_hrResult_</span></span>
  
> <span data-ttu-id="c7544-121">[in]再配置操作の結果を示す**HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="c7544-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="c7544-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="c7544-122">_fModified_</span></span>
  
> <span data-ttu-id="c7544-123">[in]アイテムが変更されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c7544-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="c7544-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="c7544-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="c7544-125">[in]指定送信された会議がメッセージを更新するかどうか。</span><span class="sxs-lookup"><span data-stu-id="c7544-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="c7544-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="c7544-126">_pError_</span></span>
  
> <span data-ttu-id="c7544-127">[in]拡張エラー情報を含む**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c7544-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="c7544-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="c7544-128">Return values</span></span>

<span data-ttu-id="c7544-129">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="c7544-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7544-130">解釈</span><span class="sxs-lookup"><span data-stu-id="c7544-130">Remarks</span></span>

<span data-ttu-id="c7544-131">[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアント アプリケーションは、項目の更新の完了を追跡するためにこの関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="c7544-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7544-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7544-132">See also</span></span>

- [<span data-ttu-id="c7544-133">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="c7544-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

