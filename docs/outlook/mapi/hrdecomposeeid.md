---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573370"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="2af07-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="2af07-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="2af07-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2af07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2af07-105">ストア内のオブジェクトのエントリ id とストアのエントリの識別子、メッセージ ・ ストア内のメッセージでは通常、オブジェクトの複合のエントリ id に分割します。</span><span class="sxs-lookup"><span data-stu-id="2af07-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2af07-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2af07-106">Header file:</span></span>  <br/> |<span data-ttu-id="2af07-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2af07-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2af07-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2af07-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2af07-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2af07-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2af07-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2af07-110">Called by:</span></span>  <br/> |<span data-ttu-id="2af07-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2af07-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="2af07-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2af07-112">Parameters</span></span>

 <span data-ttu-id="2af07-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="2af07-113">_psession_</span></span>
  
> <span data-ttu-id="2af07-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="2af07-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-115">_cbEID_</span></span>
  
> <span data-ttu-id="2af07-116">[in]分離する複合エントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="2af07-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="2af07-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-117">_pEID_</span></span>
  
> <span data-ttu-id="2af07-118">[in]分離する複合エントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="2af07-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="2af07-120">[out]返されたサイズ (バイト)、オブジェクトを含むメッセージ ストアのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="2af07-121">_PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _pcbStoreEID_パラメーターが指す値が 0 の。</span><span class="sxs-lookup"><span data-stu-id="2af07-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="2af07-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="2af07-123">[out]オブジェクトを含むメッセージ ストアのエントリが返される識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="2af07-124">_PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppStoreEID_パラメーターに NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="2af07-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="2af07-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="2af07-126">[out]返されたサイズ (バイト)、オブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="2af07-127">_PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _pcbMsgEID_パラメーターは、 _cbEID_パラメーターの値に等しい。</span><span class="sxs-lookup"><span data-stu-id="2af07-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="2af07-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="2af07-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="2af07-129">[out]オブジェクトの返されるエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2af07-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="2af07-130">_PEID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppMsgEID_は、普通のエントリ id のコピーへのポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="2af07-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2af07-131">Return value</span><span class="sxs-lookup"><span data-stu-id="2af07-131">Return value</span></span>

<span data-ttu-id="2af07-132">なし。</span><span class="sxs-lookup"><span data-stu-id="2af07-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2af07-133">注釈</span><span class="sxs-lookup"><span data-stu-id="2af07-133">Remarks</span></span>

<span data-ttu-id="2af07-134">_PEID_パラメーターで指定された識別子は、複合では、メッセージ ・ ストア内のオブジェクトのエントリ id とストアのエントリの識別子に分割されます。</span><span class="sxs-lookup"><span data-stu-id="2af07-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="2af07-135">普通のエントリの識別子の文字列がコピーされるだけです。</span><span class="sxs-lookup"><span data-stu-id="2af07-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="2af07-136">分離する複合識別子は、通常、 [HrComposeEID](hrcomposeeid.md)関数によって作成されたいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2af07-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2af07-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2af07-137">Notes to callers</span></span>

<span data-ttu-id="2af07-138">_PEID_パラメーターを保持しているメモリは、この関数が正常に完了時に解放されます。</span><span class="sxs-lookup"><span data-stu-id="2af07-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="2af07-139">呼び出し元の実装では、出力パラメーター用のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="2af07-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

