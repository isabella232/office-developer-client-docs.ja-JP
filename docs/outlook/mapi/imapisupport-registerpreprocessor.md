---
title: imapisupportregisterpreprocessor プロセッサ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404898"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="f3281-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="f3281-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="f3281-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3281-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3281-105">トランスポートプロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。</span><span class="sxs-lookup"><span data-stu-id="f3281-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f3281-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3281-106">Parameters</span></span>

 <span data-ttu-id="f3281-107">_lpmuid_</span><span class="sxs-lookup"><span data-stu-id="f3281-107">_lpMuid_</span></span>
  
> <span data-ttu-id="f3281-108">順番プリプロセッサ関数が処理する識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f3281-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="f3281-109">_lpmuid_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3281-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f3281-110">_lpszadrtype_</span><span class="sxs-lookup"><span data-stu-id="f3281-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="f3281-111">順番FAX、SMTP、または X500 など、関数が操作するメッセージのアドレスの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f3281-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="f3281-112">_lpszadrtype_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3281-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f3281-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="f3281-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="f3281-114">順番プリプロセッサ関数のエントリポイントが格納されているダイナミックリンクライブラリ (DLL) の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f3281-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="f3281-115">_lpszpreprocess_</span><span class="sxs-lookup"><span data-stu-id="f3281-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="f3281-116">順番プリプロセッサ関数の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f3281-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="f3281-117">_lpszpreprocess_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3281-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f3281-118">_lpszremovepreprocessinfo_</span><span class="sxs-lookup"><span data-stu-id="f3281-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="f3281-119">順番プリプロセッサ情報 ( [removepreprocessinfo](removepreprocessinfo.md)プロトタイプに準拠する関数) を削除する関数の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f3281-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="f3281-120">_lpszremovepreprocessinfo_パラメーターは NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f3281-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f3281-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f3281-121">_ulFlags_</span></span>
  
> <span data-ttu-id="f3281-122">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3281-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3281-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="f3281-123">Return value</span></span>

<span data-ttu-id="f3281-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3281-124">S_OK</span></span> 
  
> <span data-ttu-id="f3281-125">プリプロセッサ関数が正常に登録されました。</span><span class="sxs-lookup"><span data-stu-id="f3281-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3281-126">注釈</span><span class="sxs-lookup"><span data-stu-id="f3281-126">Remarks</span></span>

<span data-ttu-id="f3281-127">**imapisupport:: registerpreprocessor プロセッサ**メソッドは、トランスポートプロバイダーサポートオブジェクトのみに実装されています。</span><span class="sxs-lookup"><span data-stu-id="f3281-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="f3281-128">トランスポートプロバイダーは、 **registerpreprocessor**プロセッサを呼び出してプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。</span><span class="sxs-lookup"><span data-stu-id="f3281-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="f3281-129">MAPI スプーラーが呼び出す前に、プリプロセッサ関数を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3281-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="f3281-130">_lpszpreprocess_、 _lpszremovepreprocessinfo_、および_lpszDLLName_パラメーターは、Win32 **GetProcAddress**関数への呼び出しと共に使用できる文字列をポイントする必要があります。これにより、プリプロセッサの DLL を使用できるようになります。エントリポイントが正しく呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f3281-131">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f3281-131">Notes to callers</span></span>

<span data-ttu-id="f3281-132">preprocessors の呼び出しは、トランスポートプロバイダーの順序によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f3281-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="f3281-133">これは、プロバイダーよりも前の別のトランスポートプロバイダーがメッセージを処理できる場合、そのメッセージに対してプリプロセッサ関数が呼び出されないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f3281-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="f3281-134">プリプロセッサ関数は、処理するメッセージに対してのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="f3281-135">プリプロセッサ関数を記述して、 [MAPIUID](mapiuid.md)構造またはアドレスの種類に格納されている特定の識別子を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="f3281-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="f3281-136">_lpmuid_パラメーターに**MAPIUID**構造体と、 _lpszadrtype_パラメーターにアドレスの種類の両方を指定すると、 **MAPIUID**またはアドレスの種類のいずれかに一致するメッセージ受信者に対して、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="f3281-137">_lpmuid_が null で、 _lpszadrtype_が null 以外の場合、この関数は、 _lpszadrtype_で指定された型に一致するアドレスを持つ受信者に対してのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="f3281-138">_lpmuid_が null 以外で、 _lpszadrtype_が null の場合、アドレスの種類に関係なく、 **MAPIUID**に一致する受信者に対して関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="f3281-139">両方の値が NULL の場合は、メッセージのすべての受信者に対して関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3281-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3281-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="f3281-140">See also</span></span>



[<span data-ttu-id="f3281-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f3281-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f3281-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="f3281-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="f3281-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="f3281-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="f3281-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3281-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

