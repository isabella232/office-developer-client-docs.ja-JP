---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430774"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="34887-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="34887-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="34887-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34887-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34887-105">プロファイル管理オブジェクト [に発生](mapierror.md) した以前のエラーに関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="34887-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="34887-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="34887-106">Parameters</span></span>

 <span data-ttu-id="34887-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="34887-107">_hResult_</span></span>
  
> <span data-ttu-id="34887-108">[in]前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="34887-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="34887-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34887-109">_ulFlags_</span></span>
  
> <span data-ttu-id="34887-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="34887-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="34887-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="34887-111">The following flag can be set:</span></span>
    
<span data-ttu-id="34887-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="34887-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="34887-113">_lppMAPIError_ パラメーターで返される [MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="34887-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="34887-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="34887-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="34887-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="34887-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="34887-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="34887-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="34887-117">_戻す MAPIERROR 構造体がない場合、lppMAPIError_ パラメーターを **NULL に** 設定できます。</span><span class="sxs-lookup"><span data-stu-id="34887-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="34887-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="34887-118">Return value</span></span>

<span data-ttu-id="34887-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="34887-119">S_OK</span></span> 
  
> <span data-ttu-id="34887-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="34887-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="34887-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="34887-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="34887-122">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="34887-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34887-123">注釈</span><span class="sxs-lookup"><span data-stu-id="34887-123">Remarks</span></span>

<span data-ttu-id="34887-124">**IProfAdmin::GetLastError** メソッドは、プロファイル管理オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="34887-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="34887-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="34887-125">Notes to callers</span></span>

<span data-ttu-id="34887-126">MAPI が 1 つを提供する場合 **、MAPIERROR** 構造体を使用できます  _。lppMAPIError_ パラメーターが指すのは **、GetLastError** が値を返す場合S_OK。</span><span class="sxs-lookup"><span data-stu-id="34887-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="34887-127">MAPI では、最後のエラーが何だったのか、またはエラーについて報告する必要がなにもない場合があります。</span><span class="sxs-lookup"><span data-stu-id="34887-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="34887-128">この状況では  _、lppMAPIError_ で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="34887-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="34887-129">**MAPIERROR** 構造体に対して MAPI によって割り当てられたすべてのメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。</span><span class="sxs-lookup"><span data-stu-id="34887-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="34887-130">**GetLastError メソッドの詳細については、「Using Extended Errors** [」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="34887-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34887-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="34887-131">See also</span></span>



[<span data-ttu-id="34887-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="34887-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="34887-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="34887-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="34887-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34887-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

