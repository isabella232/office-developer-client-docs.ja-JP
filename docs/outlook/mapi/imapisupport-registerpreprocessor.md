---
title: IMAPISupportRegisterPreprocessor
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800789"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="d5246-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="d5246-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="d5246-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5246-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5246-105">トランスポート プロバイダーのプリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録します。</span><span class="sxs-lookup"><span data-stu-id="d5246-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="d5246-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5246-106">Parameters</span></span>

 <span data-ttu-id="d5246-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="d5246-107">_lpMuid_</span></span>
  
> <span data-ttu-id="d5246-108">[in]プリプロセッサ関数を処理するための識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5246-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="d5246-109">_LpMuid_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d5246-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d5246-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="d5246-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="d5246-111">[in]メッセージのアドレスの種類へのポインター、関数では、FAX、SMTP、または X500 などです。</span><span class="sxs-lookup"><span data-stu-id="d5246-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="d5246-112">_LpszAdrType_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d5246-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d5246-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="d5246-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="d5246-114">[in]プリプロセッサ関数のエントリ ポイントを含むダイナミック リンク ライブラリ (DLL) の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5246-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="d5246-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="d5246-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="d5246-116">[in]プリプロセッサ関数の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5246-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="d5246-117">_LpszPreprocess_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d5246-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d5246-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="d5246-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="d5246-119">[in]プリプロセッサの情報 ( [RemovePreprocessInfo](removepreprocessinfo.md)のプロトタイプに準拠する関数) を削除する関数の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5246-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="d5246-120">_LpszRemovePreprocessInfo_パラメーターは NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="d5246-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="d5246-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d5246-121">_ulFlags_</span></span>
  
> <span data-ttu-id="d5246-122">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5246-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d5246-123">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d5246-123">Return value</span></span>

<span data-ttu-id="d5246-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5246-124">S_OK</span></span> 
  
> <span data-ttu-id="d5246-125">プリプロセッサ関数が正常に登録されました。</span><span class="sxs-lookup"><span data-stu-id="d5246-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5246-126">備考</span><span class="sxs-lookup"><span data-stu-id="d5246-126">Remarks</span></span>

<span data-ttu-id="d5246-127">だけに、トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::RegisterPreprocessor**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d5246-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="d5246-128">トランスポート プロバイダーは、プリプロセッサ関数 ( [PreprocessMessage](preprocessmessage.md)プロトタイプに準拠する関数) を登録するのには**RegisterPreprocessor**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5246-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="d5246-129">MAPI スプーラーを呼び出すことができますには、プリプロセッサ関数を登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5246-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="d5246-130">_LpszPreprocess_、 _lpszRemovePreprocessInfo_、および_lpszDLLName_パラメーター、Win32 の**GetProcAddress**関数をプリプロセッサの DLL への呼び出しと組み合わせて使用できる文字列を参照する必要があります。正しく呼び出されるエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="d5246-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d5246-131">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d5246-131">Notes to callers</span></span>

<span data-ttu-id="d5246-132">プリプロセッサの呼び出しでは、トランスポート プロバイダーの順序に固有です。</span><span class="sxs-lookup"><span data-stu-id="d5246-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="d5246-133">これは、する場合は、プロバイダーの前に別のトランスポート プロバイダーは、メッセージを処理することが、プリプロセッサ関数は呼び出されませんそのメッセージを意味します。</span><span class="sxs-lookup"><span data-stu-id="d5246-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="d5246-134">プリプロセッサ関数は、処理するメッセージに対してのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5246-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="d5246-135">[MAPIUID](mapiuid.md)構造体、またはアドレスの種類に格納されているか、特定 id を処理するためのプリプロセッサ関数を記述できます。</span><span class="sxs-lookup"><span data-stu-id="d5246-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="d5246-136">_LpMuid_パラメーターおよび_lpszAdrType_パラメーターのアドレスの種類で、両方の**MAPIUID**構造体を指定すると、 **MAPIUID**またはアドレスの種類のいずれかに一致するメッセージの受信者に対して、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5246-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="d5246-137">_LpMuid_は、NULL、 _lpszAdrType_は、NULL 以外の場合は、 _lpszAdrType_で指定された型に一致するアドレスを持つ受信者にのみ、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5246-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="d5246-138">_LpMuid_は、NULL ではないし、 _lpszAdrType_が NULL の場合、受信者のアドレスの種類に関係なく**MAPIUID**に一致するため、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5246-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="d5246-139">両方が NULL である場合、メッセージのすべての受信者に対して、関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5246-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5246-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5246-140">See also</span></span>



[<span data-ttu-id="d5246-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d5246-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d5246-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="d5246-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="d5246-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="d5246-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="d5246-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5246-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

