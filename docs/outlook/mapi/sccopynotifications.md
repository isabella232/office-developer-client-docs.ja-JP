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
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357485"
---
# <a name="sccopynotifications"></a><span data-ttu-id="724fd-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="724fd-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="724fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="724fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="724fd-105">イベント通知のグループをメモリの単一のブロックにコピーします。</span><span class="sxs-lookup"><span data-stu-id="724fd-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="724fd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="724fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="724fd-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="724fd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="724fd-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="724fd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="724fd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="724fd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="724fd-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="724fd-110">Called by:</span></span>  <br/> |<span data-ttu-id="724fd-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="724fd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="724fd-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="724fd-112">Parameters</span></span>

 <span data-ttu-id="724fd-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="724fd-113">_cntf_</span></span>
  
> <span data-ttu-id="724fd-114">順番_rgntf_パラメーターで指定された、配列内の[通知](notification.md)構造の数。</span><span class="sxs-lookup"><span data-stu-id="724fd-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="724fd-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="724fd-115">_rgntf_</span></span>
  
> <span data-ttu-id="724fd-116">順番コピーするイベント通知を定義する**通知**構造の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="724fd-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="724fd-117">_pvdst_</span><span class="sxs-lookup"><span data-stu-id="724fd-117">_pvDst_</span></span>
  
> <span data-ttu-id="724fd-118">読み上げ返された通知へのポインター。</span><span class="sxs-lookup"><span data-stu-id="724fd-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="724fd-119">_設計_</span><span class="sxs-lookup"><span data-stu-id="724fd-119">_pcb_</span></span>
  
> <span data-ttu-id="724fd-120">読み上げ(オプション) _rgntf_パラメーターによって指定された配列のサイズ (バイト単位) が格納されている変数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="724fd-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="724fd-121">NULL でない場合、 _pcb_パラメーターは_pvdst_パラメーターに格納されているバイト数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="724fd-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="724fd-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="724fd-122">Return value</span></span>

<span data-ttu-id="724fd-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="724fd-123">S_OK</span></span>
  
> <span data-ttu-id="724fd-124">イベント通知が正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="724fd-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="724fd-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="724fd-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="724fd-126">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="724fd-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="724fd-127">解説</span><span class="sxs-lookup"><span data-stu-id="724fd-127">Remarks</span></span>

<span data-ttu-id="724fd-128">_pcb_パラメーターで NULL が渡された場合、コピーは実行されません。_pcb_で null 以外の値が渡された場合、 **sccopynotifications**関数は、配列のサイズと配列自体をメモリの単一のブロックにコピーします。</span><span class="sxs-lookup"><span data-stu-id="724fd-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="724fd-129">_pcb_が NULL でない場合は、 _pvdst_パラメーターに格納されているバイト数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="724fd-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="724fd-130">_pvdst_パラメーターは、配列全体を格納するのに十分な大きさでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="724fd-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

