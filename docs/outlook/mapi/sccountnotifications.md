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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437995"
---
# <a name="sccountnotifications"></a><span data-ttu-id="a861d-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="a861d-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="a861d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a861d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a861d-105">イベント通知の配列のサイズ (バイト単位) を決定し、配列に関連付けられているメモリを検証します。</span><span class="sxs-lookup"><span data-stu-id="a861d-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a861d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a861d-106">Header file:</span></span>  <br/> |<span data-ttu-id="a861d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a861d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a861d-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a861d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a861d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a861d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a861d-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a861d-110">Called by:</span></span>  <br/> |<span data-ttu-id="a861d-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a861d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="a861d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a861d-112">Parameters</span></span>

 <span data-ttu-id="a861d-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="a861d-113">_cntf_</span></span>
  
> <span data-ttu-id="a861d-114">[in]_rgntf_[パラメーターで](notification.md)示される配列内の NOTIFICATION 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="a861d-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="a861d-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="a861d-115">_rgntf_</span></span>
  
> <span data-ttu-id="a861d-116">[in]サイズを決定する **NOTIFICATION** 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a861d-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="a861d-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="a861d-117">_pcb_</span></span>
  
> <span data-ttu-id="a861d-118">[out]  _rgntf_ パラメーターが指す配列のサイズ (バイト単位) へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="a861d-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="a861d-119">NULL の場合 **、ScCountNotifications は** 通知の配列を検証します。</span><span class="sxs-lookup"><span data-stu-id="a861d-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a861d-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="a861d-120">Return value</span></span>

<span data-ttu-id="a861d-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="a861d-121">S_OK</span></span>
  
> <span data-ttu-id="a861d-122">カウントが正常に決定されました。</span><span class="sxs-lookup"><span data-stu-id="a861d-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="a861d-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a861d-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="a861d-124">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="a861d-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a861d-125">注釈</span><span class="sxs-lookup"><span data-stu-id="a861d-125">Remarks</span></span>

<span data-ttu-id="a861d-126">_NULL_ が pcb パラメーターで渡された場合 **、ScCountNotifications** 関数は通知の配列のみを検証しますが、カウントは行われます。null 以外の値が _pcb_ で渡された場合 **、ScCountNotifications は** 配列のサイズを決定し、原因 _の pcb_ を格納します。</span><span class="sxs-lookup"><span data-stu-id="a861d-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="a861d-127">pcb  _パラメーターは_ 、配列全体を格納するのに十分な大きい値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a861d-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

