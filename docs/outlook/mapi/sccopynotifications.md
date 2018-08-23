---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803811"
---
# <a name="sccopynotifications"></a><span data-ttu-id="ab53b-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="ab53b-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="ab53b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab53b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab53b-105">イベント通知のグループを単一のメモリ ブロックにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ab53b-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab53b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ab53b-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab53b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ab53b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ab53b-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ab53b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab53b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab53b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab53b-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ab53b-110">Called by:</span></span>  <br/> |<span data-ttu-id="ab53b-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ab53b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="ab53b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab53b-112">Parameters</span></span>

 <span data-ttu-id="ab53b-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="ab53b-113">_cntf_</span></span>
  
> <span data-ttu-id="ab53b-114">[in]_Rgntf_パラメーターで指定された配列内の[通知](notification.md)の構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="ab53b-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="ab53b-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="ab53b-115">_rgntf_</span></span>
  
> <span data-ttu-id="ab53b-116">[in]コピーするイベント通知を定義する**通知**の構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab53b-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="ab53b-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="ab53b-117">_pvDst_</span></span>
  
> <span data-ttu-id="ab53b-118">[out]返された通知へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab53b-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="ab53b-119">_pcb_</span><span class="sxs-lookup"><span data-stu-id="ab53b-119">_pcb_</span></span>
  
> <span data-ttu-id="ab53b-120">[out]変数配列のバイト単位のサイズが_rgntf_パラメーターが指す場所にポインターが格納されます。</span><span class="sxs-lookup"><span data-stu-id="ab53b-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="ab53b-121">かどうか NULL の場合、 _pcb_のパラメーターは、 _pvDst_パラメーターに格納されているバイト数を設定します。</span><span class="sxs-lookup"><span data-stu-id="ab53b-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ab53b-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ab53b-122">Return value</span></span>

<span data-ttu-id="ab53b-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab53b-123">S_OK</span></span>
  
> <span data-ttu-id="ab53b-124">イベント通知が正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="ab53b-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="ab53b-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ab53b-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="ab53b-126">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="ab53b-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab53b-127">注釈</span><span class="sxs-lookup"><span data-stu-id="ab53b-127">Remarks</span></span>

<span data-ttu-id="ab53b-128">_Pcb_のパラメーターに NULL を渡した場合は、コピーは実行されません。_pcb_の null 以外の値が渡された場合、 **ScCopyNotifications**関数は、単一ブロックのメモリをアレイとアレイ自体のサイズをコピーします。</span><span class="sxs-lookup"><span data-stu-id="ab53b-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="ab53b-129">_Pcb_が NULL でない場合は、 _pvDst_パラメーターに格納されているバイト数に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ab53b-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="ab53b-130">_PvDst_パラメーターは、配列全体を格納できる大きさである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab53b-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

