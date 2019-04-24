---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351373"
---
# <a name="sccountnotifications"></a><span data-ttu-id="ea277-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="ea277-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="ea277-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea277-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea277-105">イベント通知の配列のサイズをバイト単位で指定し、配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="ea277-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea277-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ea277-106">Header file:</span></span>  <br/> |<span data-ttu-id="ea277-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="ea277-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ea277-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ea277-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ea277-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ea277-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ea277-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ea277-110">Called by:</span></span>  <br/> |<span data-ttu-id="ea277-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="ea277-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="ea277-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ea277-112">Parameters</span></span>

 <span data-ttu-id="ea277-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="ea277-113">_cntf_</span></span>
  
> <span data-ttu-id="ea277-114">順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。</span><span class="sxs-lookup"><span data-stu-id="ea277-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="ea277-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="ea277-115">_rgntf_</span></span>
  
> <span data-ttu-id="ea277-116">順番サイズが決定される**通知**構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ea277-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="ea277-117">_設計_</span><span class="sxs-lookup"><span data-stu-id="ea277-117">_pcb_</span></span>
  
> <span data-ttu-id="ea277-118">読み上げ(オプション) _rgntf_パラメーターで指定された配列のサイズ (バイト単位) を指すポインターです。</span><span class="sxs-lookup"><span data-stu-id="ea277-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="ea277-119">NULL の場合、 **sccountnotifications**は通知の配列を検証します。</span><span class="sxs-lookup"><span data-stu-id="ea277-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ea277-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="ea277-120">Return value</span></span>

<span data-ttu-id="ea277-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ea277-121">S_OK</span></span>
  
> <span data-ttu-id="ea277-122">カウントが正常に決定されました。</span><span class="sxs-lookup"><span data-stu-id="ea277-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="ea277-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea277-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="ea277-124">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="ea277-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ea277-125">解説</span><span class="sxs-lookup"><span data-stu-id="ea277-125">Remarks</span></span>

<span data-ttu-id="ea277-126">_pcb_パラメーターで NULL が渡された場合、 **sccountnotifications**関数は通知の配列のみを検証しますが、カウントは行われません。非 null 値が_pcb_で渡された場合、 **sccountnotifications**は配列のサイズを決定し、原因となった_pcb_を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea277-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="ea277-127">_pcb_パラメーターは、配列全体を格納するのに十分な大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea277-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

