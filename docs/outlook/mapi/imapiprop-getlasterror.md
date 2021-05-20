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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435832"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="b3e61-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b3e61-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="b3e61-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3e61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3e61-105">前のエラー [に関する](mapierror.md) 情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="b3e61-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="b3e61-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b3e61-106">Parameters</span></span>

 <span data-ttu-id="b3e61-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="b3e61-107">_hResult_</span></span>
  
> <span data-ttu-id="b3e61-108">[in]前のメソッド呼び出しで生成されたエラー コードのハンドル。</span><span class="sxs-lookup"><span data-stu-id="b3e61-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="b3e61-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3e61-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b3e61-110">[in]_lppMAPIError_ によって指される **MAPIERROR** 構造で返されるテキストの形式を示すフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b3e61-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="b3e61-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b3e61-111">The following flag can be set:</span></span>
    
<span data-ttu-id="b3e61-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b3e61-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b3e61-113">文字列は Unicode 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3e61-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="b3e61-114">このフラグMAPI_UNICODE設定しない場合、文字列は ANSI 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3e61-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="b3e61-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="b3e61-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="b3e61-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="b3e61-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="b3e61-117">_lppMAPIError パラメーター_ は、返すエラー情報がない場合は NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b3e61-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b3e61-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="b3e61-118">Return value</span></span>

<span data-ttu-id="b3e61-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3e61-119">S_OK</span></span> 
  
> <span data-ttu-id="b3e61-120">エラー情報が返されました。</span><span class="sxs-lookup"><span data-stu-id="b3e61-120">The error information was returned.</span></span>
    
<span data-ttu-id="b3e61-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="b3e61-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="b3e61-122">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b3e61-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3e61-123">注釈</span><span class="sxs-lookup"><span data-stu-id="b3e61-123">Remarks</span></span>

<span data-ttu-id="b3e61-124">**IMAPIProp::GetLastError** メソッドは、失敗した以前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b3e61-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="b3e61-125">クライアントは、ダイアログ ボックスに **MAPIERROR** 構造のデータを含め、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="b3e61-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="b3e61-126">MAPI によって提供される **GetLastError** の実装はすべて [、IAddrBook](iaddrbookimapiprop.md) 実装を除く ANSI 実装です。</span><span class="sxs-lookup"><span data-stu-id="b3e61-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="b3e61-127">**IAddrBook に含まれる GetLastError** メソッド **は Unicode** をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b3e61-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b3e61-128">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="b3e61-128">Notes to implementers</span></span>

<span data-ttu-id="b3e61-129">リモート トランスポート プロバイダーによるこのメソッドの実装の詳細と、このメソッドが返すメッセージの詳細は、さまざまな HRESULT 値につながる特定のエラー条件がトランスポート プロバイダーによって異なってきます。</span><span class="sxs-lookup"><span data-stu-id="b3e61-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b3e61-130">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b3e61-130">Notes to callers</span></span>

<span data-ttu-id="b3e61-131">戻り値が指定されている場合にのみ **、GetLastError** が 1 を提供する場合は _、lppMAPIError_ パラメーターが指す **MAPIERROR** 構造をS_OK。</span><span class="sxs-lookup"><span data-stu-id="b3e61-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="b3e61-132">**GetLastError では、** 最後のエラーが何だったのか、またはエラーについて報告する必要がなにもない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b3e61-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="b3e61-133">この状況では、代わりに  _lppMAPIError_ で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="b3e61-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="b3e61-134">**MAPIERROR** 構造体のメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。</span><span class="sxs-lookup"><span data-stu-id="b3e61-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="b3e61-135">**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="b3e61-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3e61-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3e61-136">See also</span></span>



[<span data-ttu-id="b3e61-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b3e61-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="b3e61-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="b3e61-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="b3e61-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b3e61-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b3e61-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3e61-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="b3e61-141">MAPI 拡張エラー</span><span class="sxs-lookup"><span data-stu-id="b3e61-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

