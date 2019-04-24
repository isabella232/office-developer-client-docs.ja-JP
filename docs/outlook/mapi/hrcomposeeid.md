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
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348063"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="9baac-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="9baac-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="9baac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9baac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9baac-105">オブジェクト (通常はメッセージストア内のメッセージ) の複合エントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="9baac-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9baac-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9baac-106">Header file:</span></span>  <br/> |<span data-ttu-id="9baac-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="9baac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9baac-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="9baac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9baac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9baac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9baac-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="9baac-110">Called by:</span></span>  <br/> |<span data-ttu-id="9baac-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9baac-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="9baac-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9baac-112">Parameters</span></span>

 <span data-ttu-id="9baac-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="9baac-113">_psession_</span></span>
  
> <span data-ttu-id="9baac-114">順番クライアントアプリケーションによって使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9baac-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="9baac-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="9baac-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="9baac-116">順番メッセージまたはその他のオブジェクトを保持しているメッセージストアのレコードキーのサイズ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="9baac-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="9baac-117">_cbStoreRecordKey_パラメーターに0が渡された場合、 _ppeid_パラメーターはオブジェクトのエントリ識別子のコピーを指します。</span><span class="sxs-lookup"><span data-stu-id="9baac-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="9baac-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="9baac-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="9baac-119">順番メッセージまたはその他のオブジェクトを含むメッセージストアの record キーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9baac-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="9baac-120">_cbmsgeid_</span><span class="sxs-lookup"><span data-stu-id="9baac-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="9baac-121">順番メッセージまたはその他のオブジェクトのエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="9baac-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="9baac-122">_pmsgeid_</span><span class="sxs-lookup"><span data-stu-id="9baac-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="9baac-123">順番オブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9baac-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="9baac-124">_pcbeid_</span><span class="sxs-lookup"><span data-stu-id="9baac-124">_pcbEID_</span></span>
  
> <span data-ttu-id="9baac-125">読み上げ返される識別子のサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9baac-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="9baac-126">_ppeid_</span><span class="sxs-lookup"><span data-stu-id="9baac-126">_ppEID_</span></span>
  
> <span data-ttu-id="9baac-127">読み上げ返されたエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9baac-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="9baac-128">_cbStoreRecordKey_パラメーターの値が0より大きい場合、 _ppeid_パラメーターは作成された複合エントリ識別子へのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="9baac-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="9baac-129">_cbStoreRecordKey_が0の場合、 _ppeid_は、オブジェクトのエントリ識別子のコピーへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="9baac-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9baac-130">Return value</span><span class="sxs-lookup"><span data-stu-id="9baac-130">Return value</span></span>

<span data-ttu-id="9baac-131">なし。</span><span class="sxs-lookup"><span data-stu-id="9baac-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9baac-132">解説</span><span class="sxs-lookup"><span data-stu-id="9baac-132">Remarks</span></span>

<span data-ttu-id="9baac-133">複合エントリ識別子が作成されているメッセージまたはその他のオブジェクトがメッセージストアに存在する場合は、そのオブジェクトのエントリ識別子とストアの record キーから識別子が作成されます。</span><span class="sxs-lookup"><span data-stu-id="9baac-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="9baac-134">オブジェクトがストアにない場合、つまり、 _cbStoreRecordKey_で渡されたストアレコードキーのバイト数が0の場合は、オブジェクトのエントリ識別子が単純にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="9baac-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="9baac-135">hrの参照**id**関数を使用すると、アプリケーションは複合エントリ識別子を使用して複数のストア内のオブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="9baac-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="9baac-136">アプリケーションは[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出して、複合エントリ識別子を元の constituents に分割できます。</span><span class="sxs-lookup"><span data-stu-id="9baac-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9baac-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="9baac-137">See also</span></span>



[<span data-ttu-id="9baac-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="9baac-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="9baac-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="9baac-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

