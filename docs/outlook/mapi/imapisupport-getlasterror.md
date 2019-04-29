---
title: imapisupportgetlasterror
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438548"
---
# <a name="imapisupportgetlasterror"></a><span data-ttu-id="795a9-103">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="795a9-103">IMAPISupport::GetLastError</span></span>

  
  
<span data-ttu-id="795a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="795a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="795a9-105">以前のサポートオブジェクトエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="795a9-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous support object error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="795a9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="795a9-106">Parameters</span></span>

 <span data-ttu-id="795a9-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="795a9-107">_hResult_</span></span>
  
> <span data-ttu-id="795a9-108">順番サポートオブジェクトの前のメソッド呼び出しで生成されたエラー値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="795a9-108">[in] A handle to the error value generated in the previous method call for the support object.</span></span>
    
 <span data-ttu-id="795a9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="795a9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="795a9-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="795a9-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="795a9-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="795a9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="795a9-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="795a9-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="795a9-113">_lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="795a9-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="795a9-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="795a9-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="795a9-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="795a9-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="795a9-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="795a9-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="795a9-117">適切なエラー情報を持つ**MAPIERROR**構造を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="795a9-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate error information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="795a9-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="795a9-118">Return value</span></span>

<span data-ttu-id="795a9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="795a9-119">S_OK</span></span> 
  
> <span data-ttu-id="795a9-120">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="795a9-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="795a9-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="795a9-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="795a9-122">MAPI_UNICODE フラグが設定されていて、mapi が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、mapi が unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="795a9-122">Either the MAPI_UNICODE flag was set and MAPI does not support Unicode, or MAPI_UNICODE was not set and MAPI supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="795a9-123">注釈</span><span class="sxs-lookup"><span data-stu-id="795a9-123">Remarks</span></span>

<span data-ttu-id="795a9-124">**imapisupport:: GetLastError**メソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="795a9-124">The **IMAPISupport::GetLastError** method is implemented for all support objects.</span></span> <span data-ttu-id="795a9-125">呼び出し元は、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="795a9-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="795a9-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="795a9-126">Notes to callers</span></span>

<span data-ttu-id="795a9-127">**MAPIERROR**構造体へのポインターは、 _lppMAPIError_パラメーターでは、 **GetLastError**が S_OK を返す場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="795a9-127">You can use the pointer to the **MAPIERROR** structure, if MAPI supplies one, in the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="795a9-128">MAPI では、最後のエラーが発生したかどうかを判断できない場合や、エラーについてのレポートを持っていない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="795a9-128">Sometimes MAPI cannot determine what the last error was or it has nothing more to report about the error.</span></span> <span data-ttu-id="795a9-129">このような状況では、 _lppMAPIError_は代わりに NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="795a9-129">In this situation,  _lppMAPIError_ returns a pointer to NULL instead.</span></span> 
  
<span data-ttu-id="795a9-130">**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="795a9-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
<span data-ttu-id="795a9-131">MAPI によって割り当てられたすべてのメモリを解放するには、返された**MAPIERROR**構造体の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="795a9-131">To release all the memory allocated by MAPI, call the [MAPIFreeBuffer](mapifreebuffer.md) function for the returned **MAPIERROR** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="795a9-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="795a9-132">See also</span></span>



[<span data-ttu-id="795a9-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="795a9-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="795a9-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="795a9-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="795a9-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="795a9-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="795a9-136">MAPI 拡張エラー</span><span class="sxs-lookup"><span data-stu-id="795a9-136">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

