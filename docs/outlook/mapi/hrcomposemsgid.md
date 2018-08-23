---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800276"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="2d1c5-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="2d1c5-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="2d1c5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2d1c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2d1c5-105">通常メッセージ ストア内のメッセージ オブジェクトは、複合のエントリの識別子を表す ASCII 文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d1c5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2d1c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d1c5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2d1c5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2d1c5-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d1c5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2d1c5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2d1c5-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-110">Called by:</span></span>  <br/> |<span data-ttu-id="2d1c5-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2d1c5-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="2d1c5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2d1c5-112">Parameters</span></span>

 <span data-ttu-id="2d1c5-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-113">_psession_</span></span>
  
> <span data-ttu-id="2d1c5-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="2d1c5-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="2d1c5-116">[in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="2d1c5-117">_CbStoreRecordKey_パラメーターに 0 を渡すと、エントリ id のコピーを_pszMsgID_のパラメーターのポイント テキストに変換します。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="2d1c5-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="2d1c5-119">[in]メッセージまたはその他のオブジェクトを含むメッセージ ストアのレコードのキーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="2d1c5-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="2d1c5-121">[in]メッセージまたはその他のオブジェクトのエントリ id のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="2d1c5-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="2d1c5-123">[in]オブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="2d1c5-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="2d1c5-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="2d1c5-125">[out]返される ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="2d1c5-126">_CbStoreRecordKey_パラメーターが 0 より大きい場合は、複合のエントリの識別子に_pszMsgID_パラメーターのポイントは、テキストに変換します。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="2d1c5-127">_CbStoreRecordKey_が 0 の場合は、普通のエントリの識別子に_pszMsgID_ポイントは、テキストに変換します。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2d1c5-128">Return value</span><span class="sxs-lookup"><span data-stu-id="2d1c5-128">Return value</span></span>

<span data-ttu-id="2d1c5-129">なし。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d1c5-130">注釈</span><span class="sxs-lookup"><span data-stu-id="2d1c5-130">Remarks</span></span>

<span data-ttu-id="2d1c5-131">メッセージ ストアでメッセージまたは複合のエントリの識別子を作成するための他のオブジェクトが存在する場合、識別子の文字列は、オブジェクトのエントリ id とストアのレコードのキーから作成されます。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="2d1c5-132">オブジェクトがストア内にない場合は、 _cbStoreRecordKey_パラメーターで渡されたストアのレコードのキーのバイト数が 0 の場合オブジェクトのエントリ id は、単にコピーされ、文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="2d1c5-133">**HrComposeMsgID**関数の呼び出しは、 [HrComposeEID](hrcomposeeid.md)関数とし、 [HrSzFromEntryID](hrszfromentryid.md)関数を呼び出すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="2d1c5-134">**HrComposeMsgID**は、複合のエントリ id を使用して複数のストア内のオブジェクトを使用するクライアント アプリケーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="2d1c5-135">アプリケーションでは、複合のエントリの識別子を元の住民に分割する[HrDecomposeMsgID](hrdecomposemsgid.md)関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="2d1c5-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

