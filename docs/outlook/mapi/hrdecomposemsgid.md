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
# <a name="hrdecomposemsgid"></a><span data-ttu-id="35db1-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="35db1-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="35db1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35db1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35db1-105">オブジェクトの複合エントリ識別子 (通常はメッセージストア内のメッセージ) の ASCII 表記を、ストア内のそのオブジェクトのエントリ id、およびストアのエントリ識別子に分割します。</span><span class="sxs-lookup"><span data-stu-id="35db1-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35db1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="35db1-106">Header file:</span></span>  <br/> |<span data-ttu-id="35db1-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="35db1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="35db1-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="35db1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35db1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35db1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35db1-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="35db1-110">Called by:</span></span>  <br/> |<span data-ttu-id="35db1-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="35db1-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="35db1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35db1-112">Parameters</span></span>

 <span data-ttu-id="35db1-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="35db1-113">_psession_</span></span>
  
> <span data-ttu-id="35db1-114">順番クライアントアプリケーションによって使用されているセッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="35db1-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="35db1-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="35db1-115">_szMsgID_</span></span>
  
> <span data-ttu-id="35db1-116">順番オブジェクトのエントリ id を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="35db1-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="35db1-117">_pcbstoreeid_</span><span class="sxs-lookup"><span data-stu-id="35db1-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="35db1-118">読み上げオブジェクトを含むメッセージストアのエントリ id の、返されるサイズをバイト単位で示したポインターです。</span><span class="sxs-lookup"><span data-stu-id="35db1-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="35db1-119">_szMsgID_パラメーターが非複合エントリ識別子の文字列を指している場合、 _pcbstoreeid_パラメーターは0を指しています。</span><span class="sxs-lookup"><span data-stu-id="35db1-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="35db1-120">_ppstoreeid_</span><span class="sxs-lookup"><span data-stu-id="35db1-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="35db1-121">読み上げオブジェクトを含むメッセージストアの返されたエントリ id へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="35db1-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="35db1-122">_szMsgID_パラメーターが非複合エントリ識別子を指している場合、 _ppstoreeid_パラメーターでは NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="35db1-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="35db1-123">_pcbmsgeid_</span><span class="sxs-lookup"><span data-stu-id="35db1-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="35db1-124">読み上げ格納されているオブジェクトのエントリ id の、返されるサイズ (バイト数) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="35db1-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="35db1-125">_szMsgID_パラメーターが非複合エントリ識別子の文字列を指している場合、 _pcbmsgeid_パラメーターは_cbeid_パラメーターの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="35db1-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="35db1-126">_ppmsgeid_</span><span class="sxs-lookup"><span data-stu-id="35db1-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="35db1-127">読み上げストア内でのオブジェクトの返されたエントリ識別子文字列へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="35db1-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="35db1-128">_szMsgID_パラメーターが非複合エントリ識別子をポイントしている場合、 _ppmsgeid_は、非複合エントリ識別子の変換されたコピーへのポインターを指します。</span><span class="sxs-lookup"><span data-stu-id="35db1-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="35db1-129">Return value</span><span class="sxs-lookup"><span data-stu-id="35db1-129">Return value</span></span>

<span data-ttu-id="35db1-130">なし。</span><span class="sxs-lookup"><span data-stu-id="35db1-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35db1-131">注釈</span><span class="sxs-lookup"><span data-stu-id="35db1-131">Remarks</span></span>

<span data-ttu-id="35db1-132">_szMsgID_パラメーターによって指定された識別子が複合である場合、その識別子は ASCII から変換され、メッセージストア内のオブジェクトのエントリ id とストアのエントリ識別子に分割されます。</span><span class="sxs-lookup"><span data-stu-id="35db1-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="35db1-133">非複合エントリ識別子の文字列は単に変換およびコピーされます。</span><span class="sxs-lookup"><span data-stu-id="35db1-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="35db1-134">複合識別子の文字列は、通常、 [HrComposeMsgID](hrcomposemsgid.md)関数によって作成されたものです。</span><span class="sxs-lookup"><span data-stu-id="35db1-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="35db1-135">**HrDecomposeMsgID**関数の呼び出しは、 [HrEntryIDFromSz](hrentryidfromsz.md)関数と[HrDecomposeEID](hrdecomposeeid.md)関数を呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="35db1-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

