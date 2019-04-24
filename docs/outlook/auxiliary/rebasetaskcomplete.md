---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: 予定のリベースの完了を報告します。
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328323"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="401e4-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="401e4-103">RebaseTaskComplete</span></span>

<span data-ttu-id="401e4-104">予定のリベースの完了を報告します。</span><span class="sxs-lookup"><span data-stu-id="401e4-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="401e4-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="401e4-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="401e4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="401e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="401e4-107">、tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="401e4-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="401e4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="401e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="401e4-109">MAPI クライアントアプリケーション</span><span class="sxs-lookup"><span data-stu-id="401e4-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="401e4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="401e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="401e4-111">Outlook のリベース/再配置オブジェクト</span><span class="sxs-lookup"><span data-stu-id="401e4-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="401e4-112">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="401e4-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="401e4-113">、tzmovelib.h で定義されている**PFNREBASETASKCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="401e4-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="401e4-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="401e4-114">Parameters</span></span>

<span data-ttu-id="401e4-115">_ulrowindex_</span><span class="sxs-lookup"><span data-stu-id="401e4-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="401e4-116">順番処理された行です。</span><span class="sxs-lookup"><span data-stu-id="401e4-116">[in] The row that was processed.</span></span> <span data-ttu-id="401e4-117">このインデックスは、 [IOlkApptRebaser:: beginrebaseappointments](iolkapptrebaser-beginrebaseappointments.md)に渡される**[srowset](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** 構造を参照します。</span><span class="sxs-lookup"><span data-stu-id="401e4-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="401e4-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="401e4-118">_pRowCur_</span></span>
  
> <span data-ttu-id="401e4-119">in] 処理されたアイテムを説明する**[srow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="401e4-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="401e4-120">_hrresult_</span><span class="sxs-lookup"><span data-stu-id="401e4-120">_hrResult_</span></span>
  
> <span data-ttu-id="401e4-121">順番リベース操作の結果を示す**HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="401e4-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="401e4-122">_fmodified_</span><span class="sxs-lookup"><span data-stu-id="401e4-122">_fModified_</span></span>
  
> <span data-ttu-id="401e4-123">順番アイテムが変更されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="401e4-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="401e4-124">_f文の更新_</span><span class="sxs-lookup"><span data-stu-id="401e4-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="401e4-125">順番会議更新メッセージが送信されたかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="401e4-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="401e4-126">_の場合_</span><span class="sxs-lookup"><span data-stu-id="401e4-126">_pError_</span></span>
  
> <span data-ttu-id="401e4-127">順番拡張エラー情報を含む**MAPIERROR**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="401e4-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="401e4-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="401e4-128">Return values</span></span>

<span data-ttu-id="401e4-129">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="401e4-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="401e4-130">解説</span><span class="sxs-lookup"><span data-stu-id="401e4-130">Remarks</span></span>

<span data-ttu-id="401e4-131">[IOlkApptRebaser](iolkapptrebaser.md)インターフェイスを使用する MAPI クライアントアプリケーションは、この関数を実装して、アイテムの更新の完了を追跡します。</span><span class="sxs-lookup"><span data-stu-id="401e4-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="401e4-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="401e4-132">See also</span></span>

- [<span data-ttu-id="401e4-133">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="401e4-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

