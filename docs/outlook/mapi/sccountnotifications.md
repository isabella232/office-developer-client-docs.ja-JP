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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803837"
---
# <a name="sccountnotifications"></a><span data-ttu-id="01782-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="01782-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="01782-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01782-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01782-105">イベント通知では、配列のバイト単位のサイズを決定し、配列に関連付けられているメモリを確認します。</span><span class="sxs-lookup"><span data-stu-id="01782-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01782-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="01782-106">Header file:</span></span>  <br/> |<span data-ttu-id="01782-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="01782-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="01782-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="01782-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="01782-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="01782-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="01782-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="01782-110">Called by:</span></span>  <br/> |<span data-ttu-id="01782-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="01782-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="01782-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="01782-112">Parameters</span></span>

 <span data-ttu-id="01782-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="01782-113">_cntf_</span></span>
  
> <span data-ttu-id="01782-114">[in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="01782-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="01782-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="01782-115">_rgntf_</span></span>
  
> <span data-ttu-id="01782-116">[in]サイズを確認する**通知**の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="01782-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="01782-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="01782-117">_pcb_</span></span>
  
> <span data-ttu-id="01782-118">[out]ポインターを_rgntf_パラメーターが指す配列のバイト単位のサイズを指します。</span><span class="sxs-lookup"><span data-stu-id="01782-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="01782-119">NULL の場合、 **ScCountNotifications**は、通知の配列を検証します。</span><span class="sxs-lookup"><span data-stu-id="01782-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="01782-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="01782-120">Return value</span></span>

<span data-ttu-id="01782-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="01782-121">S_OK</span></span>
  
> <span data-ttu-id="01782-122">カウントが正常に確認されました。</span><span class="sxs-lookup"><span data-stu-id="01782-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="01782-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="01782-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="01782-124">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="01782-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01782-125">備考</span><span class="sxs-lookup"><span data-stu-id="01782-125">Remarks</span></span>

<span data-ttu-id="01782-126">_Pcb_のパラメーターに NULL が渡されると、 **ScCountNotifications**関数は、さまざまな通知だけを検証が、カウントは行われません。**ScCountNotifications**が配列のサイズを決定し、原因を格納する_pcb_の null 以外の値が渡された場合_pcb_です。</span><span class="sxs-lookup"><span data-stu-id="01782-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="01782-127">_Pcb_のパラメーターは、配列全体を格納できる大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="01782-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

