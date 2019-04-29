---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415202"
---
# <a name="screlocnotifications"></a><span data-ttu-id="6a1a6-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="6a1a6-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="6a1a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a1a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a1a6-105">指定されたイベント通知配列内のポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a1a6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6a1a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="6a1a6-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="6a1a6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6a1a6-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="6a1a6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6a1a6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6a1a6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6a1a6-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="6a1a6-110">Called by:</span></span>  <br/> |<span data-ttu-id="6a1a6-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="6a1a6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="6a1a6-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a1a6-112">Parameters</span></span>

 <span data-ttu-id="6a1a6-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="6a1a6-113">_cntf_</span></span>
  
> <span data-ttu-id="6a1a6-114">順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="6a1a6-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="6a1a6-115">_rgntf_</span></span>
  
> <span data-ttu-id="6a1a6-116">順番ポインターが調整される必要のあるイベント通知を定義する**通知**構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="6a1a6-117">_pvbaseold_</span><span class="sxs-lookup"><span data-stu-id="6a1a6-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="6a1a6-118">順番_rgntf_パラメーターで指定された配列の元のベースアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="6a1a6-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="6a1a6-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="6a1a6-120">順番**ScRelocNotifications**が_rgntf_パラメーターで指定された配列の新しいベースアドレスを書き込む場所。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="6a1a6-121">_設計_</span><span class="sxs-lookup"><span data-stu-id="6a1a6-121">_pcb_</span></span>
  
> <span data-ttu-id="6a1a6-122">読み上げ_pvBaseNew_パラメーターで指定された配列のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a1a6-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a1a6-123">Return value</span></span>

<span data-ttu-id="6a1a6-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a1a6-124">S_OK</span></span>
  
> <span data-ttu-id="6a1a6-125">ポインターが正常に調整されました。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="6a1a6-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6a1a6-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="6a1a6-127">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a1a6-128">注釈</span><span class="sxs-lookup"><span data-stu-id="6a1a6-128">Remarks</span></span>

<span data-ttu-id="6a1a6-129">**ScRelocNotifications**関数の_pcb_パラメーターは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="6a1a6-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a1a6-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="6a1a6-130">See also</span></span>



[<span data-ttu-id="6a1a6-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="6a1a6-131">ScRelocProps</span></span>](screlocprops.md)

