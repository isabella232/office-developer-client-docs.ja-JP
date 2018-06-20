---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3095907498b1ce7ae6b3666e0678dd0c5f76c23e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800280"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="47265-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="47265-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="47265-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47265-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47265-105">メッセージ ・ ストア内のメッセージでは通常、オブジェクトの複合のエントリ id ストア内のオブジェクトのエントリ id とストアのエントリの識別子に ASCII 文字を分離します。</span><span class="sxs-lookup"><span data-stu-id="47265-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47265-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="47265-106">Header file:</span></span>  <br/> |<span data-ttu-id="47265-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="47265-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="47265-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="47265-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="47265-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="47265-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="47265-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="47265-110">Called by:</span></span>  <br/> |<span data-ttu-id="47265-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="47265-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="47265-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="47265-112">Parameters</span></span>

 <span data-ttu-id="47265-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="47265-113">_psession_</span></span>
  
> <span data-ttu-id="47265-114">[in]クライアント アプリケーションによって使用中のセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47265-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="47265-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="47265-115">_szMsgID_</span></span>
  
> <span data-ttu-id="47265-116">[in]オブジェクトのエントリ id を表す文字列です。</span><span class="sxs-lookup"><span data-stu-id="47265-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="47265-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="47265-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="47265-118">[out]返されたサイズ (バイト)、オブジェクトを含むメッセージ ストアのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47265-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="47265-119">普通のエントリの識別子に、 _szMsgID_パラメーターが指している場合は文字列、 _pcbStoreEID_パラメーターが指す 0 です。</span><span class="sxs-lookup"><span data-stu-id="47265-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="47265-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="47265-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="47265-121">[out]オブジェクトを含むメッセージ ストアのエントリが返される識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47265-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="47265-122">_SzMsgID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppStoreEID_パラメーターに NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="47265-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="47265-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="47265-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="47265-124">[out]返されたサイズ (バイト)、そのストア内のオブジェクトのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47265-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="47265-125">_SzMsgID_パラメーターは、普通のエントリの識別子の文字列をポイントしている場合、 _pcbMsgEID_パラメーターは、 _cbEID_パラメーターの値に等しい。</span><span class="sxs-lookup"><span data-stu-id="47265-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="47265-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="47265-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="47265-127">[out]そのストア内のオブジェクトの返されるエントリの識別子の文字列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="47265-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="47265-128">_SzMsgID_パラメーターは、普通のエントリの識別子をポイントしている場合、 _ppMsgEID_は、普通のエントリ id の変換されたコピーへのポインターをポイントします。</span><span class="sxs-lookup"><span data-stu-id="47265-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="47265-129">Return value</span><span class="sxs-lookup"><span data-stu-id="47265-129">Return value</span></span>

<span data-ttu-id="47265-130">なし。</span><span class="sxs-lookup"><span data-stu-id="47265-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47265-131">備考</span><span class="sxs-lookup"><span data-stu-id="47265-131">Remarks</span></span>

<span data-ttu-id="47265-132">_SzMsgID_パラメーターで指定された識別子は、複合、ascii 変換し、メッセージ ・ ストア内のオブジェクトのエントリ id とストアのエントリ id を分割します。</span><span class="sxs-lookup"><span data-stu-id="47265-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="47265-133">単に普通のエントリの識別子の文字列が変換され、コピーされます。</span><span class="sxs-lookup"><span data-stu-id="47265-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="47265-134">複合識別子文字列が区切られている、通常は[HrComposeMsgID](hrcomposemsgid.md)関数によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="47265-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="47265-135">**HrDecomposeMsgID**関数の呼び出しは、 [HrEntryIDFromSz](hrentryidfromsz.md)関数とし、 [HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すことと同じです。</span><span class="sxs-lookup"><span data-stu-id="47265-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

