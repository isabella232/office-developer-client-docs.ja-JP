---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564816"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="3b263-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="3b263-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="3b263-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b263-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b263-105">通常メッセージ ストア内のメッセージ オブジェクトは、複合のエントリの識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="3b263-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b263-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3b263-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b263-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3b263-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3b263-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="3b263-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b263-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3b263-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3b263-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3b263-110">Called by:</span></span>  <br/> |<span data-ttu-id="3b263-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3b263-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="3b263-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3b263-112">Parameters</span></span>

 <span data-ttu-id="3b263-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="3b263-113">_psession_</span></span>
  
> <span data-ttu-id="3b263-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b263-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="3b263-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="3b263-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="3b263-116">[in]メッセージまたはその他のオブジェクトを保持しているメッセージ ・ ストアのレコードのキーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="3b263-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="3b263-117">_CbStoreRecordKey_パラメーターに 0 を渡した場合、 _ppEID_パラメーターは、オブジェクトのエントリ id のコピーを指します。</span><span class="sxs-lookup"><span data-stu-id="3b263-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="3b263-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="3b263-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="3b263-119">[in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b263-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="3b263-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="3b263-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="3b263-121">[in]メッセージまたはその他のオブジェクトのエントリ id のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="3b263-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="3b263-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="3b263-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="3b263-123">[in]オブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b263-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="3b263-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="3b263-124">_pcbEID_</span></span>
  
> <span data-ttu-id="3b263-125">[out]返される識別子のバイト単位のサイズへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b263-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="3b263-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="3b263-126">_ppEID_</span></span>
  
> <span data-ttu-id="3b263-127">[out]返されるエントリの識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3b263-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="3b263-128">_CbStoreRecordKey_パラメーターの値が 0 より大きい場合は、 _ppEID_パラメーターは、作成される複合エントリの識別子へのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="3b263-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="3b263-129">_CbStoreRecordKey_が 0 の場合は、 _ppEID_オブジェクトのエントリ id のコピーへのポインターが指します。</span><span class="sxs-lookup"><span data-stu-id="3b263-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3b263-130">Return value</span><span class="sxs-lookup"><span data-stu-id="3b263-130">Return value</span></span>

<span data-ttu-id="3b263-131">なし。</span><span class="sxs-lookup"><span data-stu-id="3b263-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b263-132">注釈</span><span class="sxs-lookup"><span data-stu-id="3b263-132">Remarks</span></span>

<span data-ttu-id="3b263-133">メッセージ ストアでメッセージまたは複合のエントリの識別子を作成するための他のオブジェクトが存在する場合、識別子は、オブジェクトのエントリ id とストアのレコードのキーから作成されます。</span><span class="sxs-lookup"><span data-stu-id="3b263-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="3b263-134">オブジェクトがストア内にない場合は、 _cbStoreRecordKey_に渡されたストアのレコードのキーのバイト数が 0 の場合オブジェクトのエントリ id は単にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3b263-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="3b263-135">**HrComposeEID**関数は、複合のエントリ id を使用して複数のストア内のオブジェクトを操作するアプリケーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b263-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="3b263-136">アプリケーションでは、複合のエントリの識別子を元の住民に分割する[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3b263-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b263-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="3b263-137">See also</span></span>



[<span data-ttu-id="3b263-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="3b263-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="3b263-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="3b263-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

