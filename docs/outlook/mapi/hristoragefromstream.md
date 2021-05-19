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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416833"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="44dba-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="44dba-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="44dba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44dba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44dba-105">**IStorage インターフェイスを** **IStream オブジェクトにレイヤー** します。</span><span class="sxs-lookup"><span data-stu-id="44dba-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44dba-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="44dba-106">Header file:</span></span>  <br/> |<span data-ttu-id="44dba-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="44dba-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44dba-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="44dba-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44dba-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44dba-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44dba-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="44dba-110">Called by:</span></span>  <br/> |<span data-ttu-id="44dba-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="44dba-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="44dba-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44dba-112">Parameters</span></span>

 <span data-ttu-id="44dba-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="44dba-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="44dba-114">[in] **IStream を実装する IUnknown** オブジェクト **へのポインター**。</span><span class="sxs-lookup"><span data-stu-id="44dba-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="44dba-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="44dba-115">_lpInterface_</span></span>
  
> <span data-ttu-id="44dba-116">[in]ストリーム オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="44dba-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="44dba-117">_lpInterface_ パラメーターには、NULL、IID_IStream、またはIID_ILockBytes。</span><span class="sxs-lookup"><span data-stu-id="44dba-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="44dba-118">_lpInterface で NULL を渡す_ のは、引数を渡すのとIID_IStream。</span><span class="sxs-lookup"><span data-stu-id="44dba-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="44dba-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="44dba-119">_ulFlags_</span></span>
  
> <span data-ttu-id="44dba-120">[in]ストリームを基準にストレージ オブジェクトを作成する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="44dba-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="44dba-121">既定の設定は、STGSTRM_RESETオブジェクトに読み取り専用アクセス権を与え、ストリームの位置 0 から開始します。</span><span class="sxs-lookup"><span data-stu-id="44dba-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="44dba-122">以下のフラグは、以下に示す以外の任意の組み合わせで設定できます。</span><span class="sxs-lookup"><span data-stu-id="44dba-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="44dba-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="44dba-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="44dba-124">ストリーム オブジェクトの新しいストレージ オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="44dba-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="44dba-125">このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。</span><span class="sxs-lookup"><span data-stu-id="44dba-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="44dba-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="44dba-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="44dba-127">ストリームの現在の位置で記憶域を開始します。</span><span class="sxs-lookup"><span data-stu-id="44dba-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="44dba-128">このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。</span><span class="sxs-lookup"><span data-stu-id="44dba-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="44dba-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="44dba-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="44dba-130">呼び出し元のサービス プロバイダーが返された記憶域に書き込みを許可します。</span><span class="sxs-lookup"><span data-stu-id="44dba-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="44dba-131">このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。</span><span class="sxs-lookup"><span data-stu-id="44dba-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="44dba-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="44dba-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="44dba-133">位置 0 で記憶域を開始します。</span><span class="sxs-lookup"><span data-stu-id="44dba-133">Starts storage at position zero.</span></span> <span data-ttu-id="44dba-134">他のフラグが設定されている場合は、このフラグを設定できません。</span><span class="sxs-lookup"><span data-stu-id="44dba-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="44dba-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="44dba-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="44dba-136">[out]返される **IStorage オブジェクトへのポインターへの** ポインター。</span><span class="sxs-lookup"><span data-stu-id="44dba-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44dba-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="44dba-137">Return value</span></span>

<span data-ttu-id="44dba-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="44dba-138">S_OK</span></span> 
  
> <span data-ttu-id="44dba-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="44dba-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="44dba-140">注釈</span><span class="sxs-lookup"><span data-stu-id="44dba-140">Remarks</span></span>

<span data-ttu-id="44dba-141">メッセージ ストア プロバイダーは、添付ファイルの IStorage インターフェイスを使用して **HrIStorageFromStream** **関数** をサポートします。</span><span class="sxs-lookup"><span data-stu-id="44dba-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="44dba-142">ストア プロバイダーは **、IStream インターフェイスを実装する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="44dba-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="44dba-143">**HrIStorageFromStream** は **、IStream オブジェクトの IStorage** インターフェイス **を提供** します。</span><span class="sxs-lookup"><span data-stu-id="44dba-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="44dba-144">lpUnkIn で **ILockBytes** または **IStream** インターフェイスを渡  _す可能性があります_。</span><span class="sxs-lookup"><span data-stu-id="44dba-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

