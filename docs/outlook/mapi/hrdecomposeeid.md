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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436112"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="5a72b-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="5a72b-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="5a72b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a72b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a72b-105">オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) を、ストア内のそのオブジェクトのエントリ識別子とストアのエントリ識別子に分離します。</span><span class="sxs-lookup"><span data-stu-id="5a72b-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a72b-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5a72b-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a72b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5a72b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5a72b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="5a72b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a72b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a72b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a72b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5a72b-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a72b-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5a72b-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5a72b-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a72b-112">Parameters</span></span>

 <span data-ttu-id="5a72b-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="5a72b-113">_psession_</span></span>
  
> <span data-ttu-id="5a72b-114">[in]クライアント アプリケーションで使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="5a72b-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-115">_cbEID_</span></span>
  
> <span data-ttu-id="5a72b-116">[in]区切る複合エントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="5a72b-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="5a72b-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-117">_pEID_</span></span>
  
> <span data-ttu-id="5a72b-118">[in]区切る複合エントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="5a72b-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="5a72b-120">[out]オブジェクトを含むメッセージ ストアのエントリ識別子の返されるサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5a72b-121">_pEID パラメーターが_ 非コンパイルエントリ識別子をポイントする場合 _、pcbStoreEID_ パラメーターは値 0 をポイントします。</span><span class="sxs-lookup"><span data-stu-id="5a72b-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="5a72b-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="5a72b-123">[out]オブジェクトを含むメッセージ ストアの返されるエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5a72b-124">_pEID パラメーターが_ 非コンパイル エントリ識別子をポイントする場合 _、ppStoreEID_ パラメーターに NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="5a72b-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="5a72b-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="5a72b-126">[out]オブジェクトのエントリ識別子の返されるサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="5a72b-127">_pEID パラメーター_ が非コンパイルエントリ識別子をポイントする場合 _、pcbMsgEID_ パラメーターは _cbEID_ パラメーターの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="5a72b-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="5a72b-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5a72b-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="5a72b-129">[out]オブジェクトの返されたエントリ識別子へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="5a72b-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="5a72b-130">_pEID_ パラメーターが非コンパイルエントリ識別子を指している場合 _、ppMsgEID_ は非コンパイルエントリ識別子のコピーへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="5a72b-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5a72b-131">Return value</span><span class="sxs-lookup"><span data-stu-id="5a72b-131">Return value</span></span>

<span data-ttu-id="5a72b-132">なし。</span><span class="sxs-lookup"><span data-stu-id="5a72b-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5a72b-133">注釈</span><span class="sxs-lookup"><span data-stu-id="5a72b-133">Remarks</span></span>

<span data-ttu-id="5a72b-134">_pEID_ パラメーターで指定された識別子が複合の場合、メッセージ ストア内のオブジェクトのエントリ識別子とストアのエントリ識別子に分割されます。</span><span class="sxs-lookup"><span data-stu-id="5a72b-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="5a72b-135">非compound エントリ識別子の文字列は、単にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="5a72b-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="5a72b-136">区切る複合識別子は、通常 [、HrComposeEID 関数によって作成される識別子](hrcomposeeid.md) です。</span><span class="sxs-lookup"><span data-stu-id="5a72b-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5a72b-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5a72b-137">Notes to callers</span></span>

<span data-ttu-id="5a72b-138">_pEID_ パラメーターを保持するメモリは、この関数が正常に完了すると解放されます。</span><span class="sxs-lookup"><span data-stu-id="5a72b-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="5a72b-139">呼び出し元の実装は、出力パラメーターのメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="5a72b-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

