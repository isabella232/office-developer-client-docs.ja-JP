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
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348070"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="d38e5-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="d38e5-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="d38e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d38e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d38e5-105">オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) を、ストア内のそのオブジェクトのエントリ id、およびストアのエントリ識別子に分割します。</span><span class="sxs-lookup"><span data-stu-id="d38e5-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d38e5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d38e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="d38e5-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="d38e5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d38e5-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d38e5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d38e5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d38e5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d38e5-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d38e5-110">Called by:</span></span>  <br/> |<span data-ttu-id="d38e5-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d38e5-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d38e5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d38e5-112">Parameters</span></span>

 <span data-ttu-id="d38e5-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="d38e5-113">_psession_</span></span>
  
> <span data-ttu-id="d38e5-114">順番クライアントアプリケーションによって使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d38e5-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="d38e5-115">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-115">_cbEID_</span></span>
  
> <span data-ttu-id="d38e5-116">順番分離する複合エントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="d38e5-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="d38e5-117">_peid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-117">_pEID_</span></span>
  
> <span data-ttu-id="d38e5-118">順番分離する複合エントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d38e5-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="d38e5-119">_pcbstoreeid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="d38e5-120">読み上げオブジェクトを含むメッセージストアのエントリ id の、返されるサイズをバイト単位で示したポインターです。</span><span class="sxs-lookup"><span data-stu-id="d38e5-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d38e5-121">_peid_パラメーターが非複合エントリ識別子を指している場合、 _pcbstoreeid_パラメーターは0の値を指しています。</span><span class="sxs-lookup"><span data-stu-id="d38e5-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="d38e5-122">_ppstoreeid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="d38e5-123">読み上げオブジェクトを含むメッセージストアの返されたエントリ id へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d38e5-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d38e5-124">_peid_パラメーターが非複合エントリ識別子を指している場合、 _ppstoreeid_パラメーターでは NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="d38e5-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="d38e5-125">_pcbmsgeid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="d38e5-126">読み上げオブジェクトのエントリ識別子のバイト単位で返されたサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d38e5-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="d38e5-127">_peid_パラメーターが非複合エントリ識別子を指している場合、 _pcbmsgeid_パラメーターは_cbeid_パラメーターの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d38e5-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="d38e5-128">_ppmsgeid_</span><span class="sxs-lookup"><span data-stu-id="d38e5-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="d38e5-129">読み上げオブジェクトの返されたエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d38e5-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="d38e5-130">_peid_パラメーターが非複合エントリ識別子を指している場合、 _ppmsgeid_は非複合エントリ識別子のコピーへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="d38e5-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d38e5-131">Return value</span><span class="sxs-lookup"><span data-stu-id="d38e5-131">Return value</span></span>

<span data-ttu-id="d38e5-132">なし。</span><span class="sxs-lookup"><span data-stu-id="d38e5-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d38e5-133">解説</span><span class="sxs-lookup"><span data-stu-id="d38e5-133">Remarks</span></span>

<span data-ttu-id="d38e5-134">_peid_パラメーターで指定された識別子が複合である場合、その id はメッセージストア内のオブジェクトのエントリ id とストアのエントリ識別子に分割されます。</span><span class="sxs-lookup"><span data-stu-id="d38e5-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="d38e5-135">非複合エントリ識別子の文字列は単にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d38e5-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="d38e5-136">分離する複合識別子は通常、hrの " [id](hrcomposeeid.md) " 関数で作成されたものです。</span><span class="sxs-lookup"><span data-stu-id="d38e5-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d38e5-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d38e5-137">Notes to callers</span></span>

<span data-ttu-id="d38e5-138">_peid_パラメーターを保持するメモリは、この関数が正常に完了した時点で解放されます。</span><span class="sxs-lookup"><span data-stu-id="d38e5-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="d38e5-139">呼び出し側の実装は、出力パラメーターのメモリを解放する役割を担います。</span><span class="sxs-lookup"><span data-stu-id="d38e5-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

