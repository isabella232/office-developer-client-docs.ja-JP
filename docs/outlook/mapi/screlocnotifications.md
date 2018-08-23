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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583968"
---
# <a name="screlocnotifications"></a><span data-ttu-id="f6e05-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="f6e05-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="f6e05-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6e05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6e05-105">指定したイベント通知の配列内のポインターを調整します。</span><span class="sxs-lookup"><span data-stu-id="f6e05-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6e05-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f6e05-106">Header file:</span></span>  <br/> |<span data-ttu-id="f6e05-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f6e05-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f6e05-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f6e05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f6e05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f6e05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f6e05-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f6e05-110">Called by:</span></span>  <br/> |<span data-ttu-id="f6e05-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f6e05-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f6e05-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f6e05-112">Parameters</span></span>

 <span data-ttu-id="f6e05-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="f6e05-113">_cntf_</span></span>
  
> <span data-ttu-id="f6e05-114">[in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="f6e05-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f6e05-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="f6e05-115">_rgntf_</span></span>
  
> <span data-ttu-id="f6e05-116">[in]ポインターを調整するのには、イベント通知を定義する**通知**の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6e05-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="f6e05-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="f6e05-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="f6e05-118">[in]_Rgntf_パラメーターで指定された配列の元のベース アドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6e05-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f6e05-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="f6e05-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="f6e05-120">[in]**ScRelocNotifications**の_rgntf_パラメーターで指定された配列の新しいベース アドレスの書き込み先の場所。</span><span class="sxs-lookup"><span data-stu-id="f6e05-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="f6e05-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="f6e05-121">_pcb_</span></span>
  
> <span data-ttu-id="f6e05-122">[out]_PvBaseNew_パラメーターで指定された配列のバイト単位のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f6e05-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6e05-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f6e05-123">Return value</span></span>

<span data-ttu-id="f6e05-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6e05-124">S_OK</span></span>
  
> <span data-ttu-id="f6e05-125">ポインターが正常に調整されました。</span><span class="sxs-lookup"><span data-stu-id="f6e05-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="f6e05-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6e05-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="f6e05-127">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="f6e05-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6e05-128">注釈</span><span class="sxs-lookup"><span data-stu-id="f6e05-128">Remarks</span></span>

<span data-ttu-id="f6e05-129">_Pcb_ **ScRelocNotifications**関数のパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="f6e05-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6e05-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="f6e05-130">See also</span></span>



[<span data-ttu-id="f6e05-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="f6e05-131">ScRelocProps</span></span>](screlocprops.md)

