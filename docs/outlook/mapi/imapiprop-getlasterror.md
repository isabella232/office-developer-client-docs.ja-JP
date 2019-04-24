---
title: imapipropgetlasterror
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342050"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="a6ae7-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6ae7-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="a6ae7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6ae7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6ae7-105">前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a6ae7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6ae7-106">Parameters</span></span>

 <span data-ttu-id="a6ae7-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a6ae7-107">_hResult_</span></span>
  
> <span data-ttu-id="a6ae7-108">順番前のメソッド呼び出しで生成されたエラーコードへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="a6ae7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6ae7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a6ae7-110">順番_lppMAPIError_でポイントされている**MAPIERROR**構造体で返されるテキストの形式を示すフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="a6ae7-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a6ae7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a6ae7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a6ae7-113">文字列は、Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="a6ae7-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="a6ae7-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a6ae7-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a6ae7-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="a6ae7-117">エラー情報を返さない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a6ae7-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6ae7-118">Return value</span></span>

<span data-ttu-id="a6ae7-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6ae7-119">S_OK</span></span> 
  
> <span data-ttu-id="a6ae7-120">エラー情報が返されました。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-120">The error information was returned.</span></span>
    
<span data-ttu-id="a6ae7-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a6ae7-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a6ae7-122">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6ae7-123">解説</span><span class="sxs-lookup"><span data-stu-id="a6ae7-123">Remarks</span></span>

<span data-ttu-id="a6ae7-124">**imapiprop:: GetLastError**メソッドは、失敗した前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="a6ae7-125">クライアントは、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="a6ae7-126">MAPI で提供される**GetLastError**のすべての実装は、 [IAddrBook](iaddrbookimapiprop.md)の実装を除く ANSI 実装です。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="a6ae7-127">**IAddrBook**に含まれている**GetLastError**メソッドは、Unicode をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6ae7-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a6ae7-128">Notes to implementers</span></span>

<span data-ttu-id="a6ae7-129">このメソッドのリモートトランスポートプロバイダーによる実装の詳細と、このメソッドが返すメッセージは、トランスポートプロバイダーによって異なります。これは、さまざまな HRESULT 値につながる特定のエラー条件が異なるトランスポートに対して異なるためです。会社.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6ae7-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a6ae7-130">Notes to callers</span></span>

<span data-ttu-id="a6ae7-131">_lppMAPIError_パラメーターで示されている**MAPIERROR**構造体は、戻り値\*\*\*\* が S_OK の場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="a6ae7-132">**GetLastError**では、最後のエラーが発生したかどうか、またはエラーについてのレポートを何にも持っていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a6ae7-133">このような場合、代わりに_lppMAPIError_で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="a6ae7-134">**MAPIERROR**構造体のメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a6ae7-135">**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a6ae7-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6ae7-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6ae7-136">See also</span></span>



[<span data-ttu-id="a6ae7-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a6ae7-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="a6ae7-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a6ae7-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a6ae7-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a6ae7-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a6ae7-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6ae7-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="a6ae7-141">MAPI 拡張エラー</span><span class="sxs-lookup"><span data-stu-id="a6ae7-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

