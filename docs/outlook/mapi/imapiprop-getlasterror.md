---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800650"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="7161d-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7161d-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="7161d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7161d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7161d-105">前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="7161d-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="7161d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7161d-106">Parameters</span></span>

 <span data-ttu-id="7161d-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="7161d-107">_hResult_</span></span>
  
> <span data-ttu-id="7161d-108">[in]以前のメソッドの呼び出しで生成されたエラー コードへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="7161d-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="7161d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7161d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7161d-110">[in]_LppMAPIError_が指す**MAPIERROR**の構造体で返されるテキストの書式を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7161d-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="7161d-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7161d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="7161d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7161d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7161d-113">文字列は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7161d-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="7161d-114">MAPI_UNICODE フラグが設定されていない場合、ANSI 形式の文字列を引き起こすことがあります。</span><span class="sxs-lookup"><span data-stu-id="7161d-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="7161d-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="7161d-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="7161d-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7161d-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="7161d-117">返されるエラー情報がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7161d-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7161d-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7161d-118">Return value</span></span>

<span data-ttu-id="7161d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7161d-119">S_OK</span></span> 
  
> <span data-ttu-id="7161d-120">エラー情報が返されました。</span><span class="sxs-lookup"><span data-stu-id="7161d-120">The error information was returned.</span></span>
    
<span data-ttu-id="7161d-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="7161d-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="7161d-122">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7161d-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7161d-123">注釈</span><span class="sxs-lookup"><span data-stu-id="7161d-123">Remarks</span></span>

<span data-ttu-id="7161d-124">**IMAPIProp::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7161d-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="7161d-125">クライアントは、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="7161d-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="7161d-126">すべての MAPI によって提供されている**GetLastError**の実装は、 [IAddrBook](iaddrbookimapiprop.md)の実装を除いて、ANSI の実装です。</span><span class="sxs-lookup"><span data-stu-id="7161d-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="7161d-127">**IAddrBook**に含まれている**GetLastError**メソッドは、Unicode をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7161d-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7161d-128">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="7161d-128">Notes to implementers</span></span>

<span data-ttu-id="7161d-129">HRESULT 値のさまざまな原因となる特定のエラー条件が異なるさまざまなトランスポートのため、リモートの詳細トランスポート プロバイダーのこのメソッドを実装し、トランスポート プロバイダーでは、このメソッドが返すメッセージとはプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="7161d-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7161d-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7161d-130">Notes to callers</span></span>

<span data-ttu-id="7161d-131">**MAPIERROR**構造体を_lppMAPIError_パラメーターで戻り値が S_OK の場合にのみ、1 つ**発生しました**提供する場合を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7161d-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="7161d-132">どのような最後のエラーまたはエラーを報告するのにはそれ以上には、 **GetLastError**は判断できません。</span><span class="sxs-lookup"><span data-stu-id="7161d-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="7161d-133">このような場合は、NULL へのポインターが返されます_lppMAPIError_の代わりにします。</span><span class="sxs-lookup"><span data-stu-id="7161d-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="7161d-134">**MAPIERROR**構造体のメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7161d-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="7161d-135">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7161d-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7161d-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="7161d-136">See also</span></span>



[<span data-ttu-id="7161d-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7161d-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="7161d-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="7161d-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="7161d-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7161d-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7161d-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7161d-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


<span data-ttu-id="7161d-141">[MAPI �g���G���[](mapi-extended-errors.md)</span><span class="sxs-lookup"><span data-stu-id="7161d-141">[MAPI Extended Errors](mapi-extended-errors.md)</span></span>

