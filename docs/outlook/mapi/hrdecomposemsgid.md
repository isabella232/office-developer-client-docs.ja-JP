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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404436"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="d7749-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="d7749-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="d7749-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7749-105">オブジェクトの複合エントリ識別子 (通常はメッセージ ストア内のメッセージ) の ASCII 表記を、ストア内のそのオブジェクトのエントリ識別子とストアのエントリ識別子に分離します。</span><span class="sxs-lookup"><span data-stu-id="d7749-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7749-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d7749-106">Header file:</span></span>  <br/> |<span data-ttu-id="d7749-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d7749-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d7749-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d7749-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d7749-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d7749-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d7749-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d7749-110">Called by:</span></span>  <br/> |<span data-ttu-id="d7749-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d7749-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d7749-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d7749-112">Parameters</span></span>

 <span data-ttu-id="d7749-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="d7749-113">_psession_</span></span>
  
> <span data-ttu-id="d7749-114">[in]クライアント アプリケーションで使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7749-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="d7749-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="d7749-115">_szMsgID_</span></span>
  
> <span data-ttu-id="d7749-116">[in]オブジェクトのエントリ識別子を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d7749-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="d7749-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="d7749-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="d7749-118">[out]オブジェクトを含むメッセージ ストアのエントリ識別子の返されるサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7749-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d7749-119">_szMsgID_ パラメーターが非コンパイルエントリ識別子文字列をポイントする場合 _、pcbStoreEID_ パラメーターは 0 をポイントします。</span><span class="sxs-lookup"><span data-stu-id="d7749-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="d7749-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="d7749-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="d7749-121">[out]オブジェクトを含むメッセージ ストアの返されるエントリ識別子へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7749-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="d7749-122">_szMsgID_ パラメーターが非コンパイルエントリ識別子をポイントする場合 _、ppStoreEID_ パラメーターで NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="d7749-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="d7749-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d7749-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="d7749-124">[out]ストア内のオブジェクトのエントリ識別子の返されるサイズ (バイト単位) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d7749-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="d7749-125">_szMsgID_ パラメーターが非コンパイルエントリ識別子文字列をポイントする場合 _、pcbMsgEID_ パラメーターは _cbEID_ パラメーターの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="d7749-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="d7749-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="d7749-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="d7749-127">[out]ストア内のオブジェクトの返されるエントリ識別子文字列へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="d7749-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="d7749-128">_szMsgID_ パラメーターが非コンパイルエントリ識別子を指している場合 _、ppMsgEID_ は非コンパイルエントリ識別子の変換されたコピーへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="d7749-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d7749-129">Return value</span><span class="sxs-lookup"><span data-stu-id="d7749-129">Return value</span></span>

<span data-ttu-id="d7749-130">なし。</span><span class="sxs-lookup"><span data-stu-id="d7749-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7749-131">注釈</span><span class="sxs-lookup"><span data-stu-id="d7749-131">Remarks</span></span>

<span data-ttu-id="d7749-132">_szMsgID_ パラメーターで指定された識別子が複合の場合、ASCII から変換され、メッセージ ストア内のオブジェクトのエントリ識別子とストアのエントリ識別子に分割されます。</span><span class="sxs-lookup"><span data-stu-id="d7749-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="d7749-133">非compound エントリ識別子の文字列は、単に変換され、コピーされます。</span><span class="sxs-lookup"><span data-stu-id="d7749-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="d7749-134">区切る複合識別子文字列は、通常 [、HrComposeMsgID](hrcomposemsgid.md) 関数によって作成される文字列です。</span><span class="sxs-lookup"><span data-stu-id="d7749-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="d7749-135">**HrDecomposeMsgID** 関数を呼び出すのは [、HrEntryIDFromSz](hrentryidfromsz.md)関数を呼び出してから [HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="d7749-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

