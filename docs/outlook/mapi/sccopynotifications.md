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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435923"
---
# <a name="sccopynotifications"></a><span data-ttu-id="914de-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="914de-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="914de-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="914de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="914de-105">イベント通知のグループを 1 つのメモリ ブロックにコピーします。</span><span class="sxs-lookup"><span data-stu-id="914de-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="914de-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="914de-106">Header file:</span></span>  <br/> |<span data-ttu-id="914de-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="914de-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="914de-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="914de-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="914de-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="914de-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="914de-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="914de-110">Called by:</span></span>  <br/> |<span data-ttu-id="914de-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="914de-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="914de-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="914de-112">Parameters</span></span>

 <span data-ttu-id="914de-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="914de-113">_cntf_</span></span>
  
> <span data-ttu-id="914de-114">[in]_rgntf_[パラメーターで](notification.md)示される配列内の NOTIFICATION 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="914de-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="914de-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="914de-115">_rgntf_</span></span>
  
> <span data-ttu-id="914de-116">[in]コピーするイベント **通知を** 定義する NOTIFICATION 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="914de-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="914de-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="914de-117">_pvDst_</span></span>
  
> <span data-ttu-id="914de-118">[out]返される通知へのポインター。</span><span class="sxs-lookup"><span data-stu-id="914de-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="914de-119">_pcb_</span><span class="sxs-lookup"><span data-stu-id="914de-119">_pcb_</span></span>
  
> <span data-ttu-id="914de-120">[out]  _rgntf_ パラメーターが指す配列のサイズ (バイト単位) が格納される変数へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="914de-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="914de-121">NULL 以外の場合  _、pcb_ パラメーターは  _pvDst_ パラメーターに格納されているバイト数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="914de-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="914de-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="914de-122">Return value</span></span>

<span data-ttu-id="914de-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="914de-123">S_OK</span></span>
  
> <span data-ttu-id="914de-124">イベント通知が正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="914de-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="914de-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="914de-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="914de-126">無効な通知が発生しました。</span><span class="sxs-lookup"><span data-stu-id="914de-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="914de-127">注釈</span><span class="sxs-lookup"><span data-stu-id="914de-127">Remarks</span></span>

<span data-ttu-id="914de-128">NULL が pcb パラメーター  _で渡された_ 場合、コピーは実行されません。null 以外の値が  _pcb_ で渡された場合 **、ScCopyNotifications** 関数は配列と配列自体のサイズを 1 つのメモリ ブロックにコピーします。</span><span class="sxs-lookup"><span data-stu-id="914de-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="914de-129">_pcb が_ NULL ではない場合、pvDst パラメーターに格納されているバイト数 _に設定_ されます。</span><span class="sxs-lookup"><span data-stu-id="914de-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="914de-130">_pvDst パラメーターは_、配列全体を含むのに十分な大きい値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="914de-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

