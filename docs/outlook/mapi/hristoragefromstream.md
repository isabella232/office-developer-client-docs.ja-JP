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
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347783"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="14af4-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="14af4-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="14af4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14af4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14af4-105">**IStream**オブジェクトに**IStorage**インターフェイスを階層的に配置します。</span><span class="sxs-lookup"><span data-stu-id="14af4-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="14af4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="14af4-106">Header file:</span></span>  <br/> |<span data-ttu-id="14af4-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="14af4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="14af4-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="14af4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="14af4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="14af4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="14af4-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="14af4-110">Called by:</span></span>  <br/> |<span data-ttu-id="14af4-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="14af4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="14af4-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="14af4-112">Parameters</span></span>

 <span data-ttu-id="14af4-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="14af4-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="14af4-114">順番**IStream**を実装している**IUnknown**オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="14af4-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="14af4-115">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="14af4-115">_lpInterface_</span></span>
  
> <span data-ttu-id="14af4-116">順番stream オブジェクトのインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="14af4-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="14af4-117">_lpinterface_パラメーターには、次のいずれかの値を渡すことができます。 NULL、IID_IStream、または IID_ILockBytes。</span><span class="sxs-lookup"><span data-stu-id="14af4-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="14af4-118">_lpinterface_で NULL を渡すことは、IID_IStream を渡すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="14af4-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="14af4-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14af4-119">_ulFlags_</span></span>
  
> <span data-ttu-id="14af4-120">順番ストリームに対するストレージオブジェクトの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="14af4-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="14af4-121">既定の設定は STGSTRM_RESET です。これにより、ストレージオブジェクトの読み取り専用アクセスが可能になり、ストリームの0の位置で開始されます。</span><span class="sxs-lookup"><span data-stu-id="14af4-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="14af4-122">次のフラグを任意の組み合わせで設定できます (記載されている場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="14af4-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="14af4-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="14af4-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="14af4-124">stream オブジェクトの新しいストレージオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="14af4-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="14af4-125">STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。</span><span class="sxs-lookup"><span data-stu-id="14af4-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="14af4-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="14af4-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="14af4-127">ストリームの現在の位置でストレージを開始します。</span><span class="sxs-lookup"><span data-stu-id="14af4-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="14af4-128">STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。</span><span class="sxs-lookup"><span data-stu-id="14af4-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="14af4-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="14af4-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="14af4-130">呼び出し元のサービスプロバイダーが、返されたストレージに書き込むことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="14af4-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="14af4-131">STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。</span><span class="sxs-lookup"><span data-stu-id="14af4-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="14af4-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="14af4-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="14af4-133">位置0でストレージを開始します。</span><span class="sxs-lookup"><span data-stu-id="14af4-133">Starts storage at position zero.</span></span> <span data-ttu-id="14af4-134">他のフラグが設定されている場合、このフラグを設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="14af4-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="14af4-135">_lppstorageout_</span><span class="sxs-lookup"><span data-stu-id="14af4-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="14af4-136">読み上げ返された**IStorage**オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="14af4-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="14af4-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="14af4-137">Return value</span></span>

<span data-ttu-id="14af4-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="14af4-138">S_OK</span></span> 
  
> <span data-ttu-id="14af4-139">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="14af4-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="14af4-140">解説</span><span class="sxs-lookup"><span data-stu-id="14af4-140">Remarks</span></span>

<span data-ttu-id="14af4-141">メッセージストアプロバイダーは、添付ファイル用の**IStorage**インターフェイスを使用して、 **hristoragefromstream**関数をサポートします。</span><span class="sxs-lookup"><span data-stu-id="14af4-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="14af4-142">ストアプロバイダーは、 **IStream**インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14af4-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="14af4-143">**hristoragefromstream**は、 **IStream**オブジェクトの**IStorage**インターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="14af4-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="14af4-144">_lpUnkIn_では、 **ILockBytes**または**IStream**インターフェイスのいずれかを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="14af4-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

