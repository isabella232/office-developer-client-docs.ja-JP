---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2a20f0f48eebe2194bc92afb98a620f9b39bb88d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800735"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="ddf59-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="ddf59-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="ddf59-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddf59-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddf59-105">以前のサポート オブジェクトのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ddf59-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="ddf59-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ddf59-106">Parameters</span></span>

 <span data-ttu-id="ddf59-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="ddf59-107">_hResult_</span></span>
  
> <span data-ttu-id="ddf59-108">[in]サポート オブジェクトの以前のメソッドの呼び出しで生成されたエラー値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="ddf59-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="ddf59-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ddf59-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ddf59-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ddf59-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="ddf59-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ddf59-111">The following flag can be set:</span></span>
    
<span data-ttu-id="ddf59-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ddf59-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ddf59-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="ddf59-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="ddf59-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="ddf59-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="ddf59-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="ddf59-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="ddf59-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ddf59-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="ddf59-117">適切なエラー情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="ddf59-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ddf59-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ddf59-118">Return value</span></span>

<span data-ttu-id="ddf59-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ddf59-119">S_OK</span></span> 
  
> <span data-ttu-id="ddf59-120">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ddf59-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ddf59-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="ddf59-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="ddf59-122">か、MAPI_UNICODE フラグが設定された MAPI が Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、MAPI は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ddf59-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ddf59-123">備考</span><span class="sxs-lookup"><span data-stu-id="ddf59-123">Remarks</span></span>

<span data-ttu-id="ddf59-124">サポートのすべてのオブジェクトの**IMAPISupport::GetLastError**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="ddf59-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="ddf59-125">呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="ddf59-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ddf59-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ddf59-126">Notes to callers</span></span>

<span data-ttu-id="ddf59-127">MAPI が指定、 _lppMAPIError_パラメーターで**発生しました**が S_OK を返す場合にのみ場合は、 **MAPIERROR**構造体へのポインターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ddf59-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="ddf59-128">場合によっては MAPI が最後にエラーがあったものを判定することはできませんまたはエラーのレポートには関係ありません。</span><span class="sxs-lookup"><span data-stu-id="ddf59-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="ddf59-129">このような場合は、 _lppMAPIError_のポインターを返します NULL に代わりにします。</span><span class="sxs-lookup"><span data-stu-id="ddf59-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="ddf59-130">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ddf59-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="ddf59-131">MAPI によって割り当てられたすべてのメモリを解放するには、返された**MAPIERROR**構造体の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ddf59-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddf59-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="ddf59-132">See also</span></span>



[<span data-ttu-id="ddf59-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="ddf59-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="ddf59-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ddf59-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ddf59-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ddf59-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="ddf59-136">MAPI の拡張エラー</span><span class="sxs-lookup"><span data-stu-id="ddf59-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

