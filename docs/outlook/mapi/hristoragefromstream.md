---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bd2d0a662585e8aba91250786f88dd310fe37e32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800310"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="3d83d-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="3d83d-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="3d83d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d83d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d83d-105">**IStream**オブジェクト上に**IStorage**インターフェイスをレイヤーにします。</span><span class="sxs-lookup"><span data-stu-id="3d83d-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3d83d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3d83d-106">Header file:</span></span>  <br/> |<span data-ttu-id="3d83d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3d83d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3d83d-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3d83d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3d83d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3d83d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3d83d-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d83d-110">Called by:</span></span>  <br/> |<span data-ttu-id="3d83d-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3d83d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="3d83d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d83d-112">Parameters</span></span>

 <span data-ttu-id="3d83d-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="3d83d-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="3d83d-114">[in]**IStream**を実装する**IUnknown**オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d83d-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="3d83d-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3d83d-115">_lpInterface_</span></span>
  
> <span data-ttu-id="3d83d-116">[in]ストリーム オブジェクトのインターフェイス id (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d83d-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="3d83d-117">_LpInterface_パラメーターの値は次のいずれかに渡すことができます: NULL、IID_IStream、または IID_ILockBytes。</span><span class="sxs-lookup"><span data-stu-id="3d83d-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="3d83d-118">_LpInterface_に NULL を渡すことは、IID_IStream を渡すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="3d83d-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="3d83d-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d83d-119">_ulFlags_</span></span>
  
> <span data-ttu-id="3d83d-120">[in]記憶域オブジェクトのストリームを基準に作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="3d83d-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="3d83d-121">既定の設定は、ストレージ ・ オブジェクトの読み取り専用アクセスを提供し、ストリームの位置は 0 から始まり、STGSTRM_RESET です。</span><span class="sxs-lookup"><span data-stu-id="3d83d-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="3d83d-122">次のフラグは、前述のように、以外の組み合わせで設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d83d-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="3d83d-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="3d83d-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="3d83d-124">ストリーム オブジェクトの新しいストレージ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d83d-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="3d83d-125">STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d83d-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3d83d-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="3d83d-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="3d83d-127">ストレージ、ストリームの現在位置を開始します。</span><span class="sxs-lookup"><span data-stu-id="3d83d-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="3d83d-128">STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d83d-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3d83d-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="3d83d-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="3d83d-130">返された記憶域への書き込みに呼び出し元のサービス プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3d83d-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="3d83d-131">STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d83d-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3d83d-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="3d83d-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="3d83d-133">0 の位置に記憶域を開始します。</span><span class="sxs-lookup"><span data-stu-id="3d83d-133">Starts storage at position zero.</span></span> <span data-ttu-id="3d83d-134">他のフラグが設定されている場合は、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d83d-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="3d83d-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="3d83d-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="3d83d-136">[out]返された**IStorage**オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d83d-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3d83d-137">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3d83d-137">Return value</span></span>

<span data-ttu-id="3d83d-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d83d-138">S_OK</span></span> 
  
> <span data-ttu-id="3d83d-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="3d83d-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d83d-140">����</span><span class="sxs-lookup"><span data-stu-id="3d83d-140">Remarks</span></span>

<span data-ttu-id="3d83d-141">メッセージは、プロバイダーのサポート**IStorage**インターフェイスを使用して添付ファイルの**HrIStorageFromStream**関数を格納します。</span><span class="sxs-lookup"><span data-stu-id="3d83d-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="3d83d-142">ストア プロバイダーは、 **IStream**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d83d-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="3d83d-143">**HrIStorageFromStream**は、 **IStream**オブジェクトの**IStorage**インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3d83d-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="3d83d-144">**ILockBytes**または_lpUnkIn_の**IStream**インターフェイスのいずれかを渡すことは。</span><span class="sxs-lookup"><span data-stu-id="3d83d-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

