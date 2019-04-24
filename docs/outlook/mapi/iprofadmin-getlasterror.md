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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317088"
---
# <a name="iprofadmingetlasterror"></a><span data-ttu-id="0b71b-103">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0b71b-103">IProfAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="0b71b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b71b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b71b-105">プロファイル管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="0b71b-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="0b71b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0b71b-106">Parameters</span></span>

 <span data-ttu-id="0b71b-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="0b71b-107">_hResult_</span></span>
  
> <span data-ttu-id="0b71b-108">順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="0b71b-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="0b71b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0b71b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0b71b-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0b71b-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="0b71b-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0b71b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0b71b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0b71b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0b71b-113">_lppMAPIError_パラメーターで返される[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="0b71b-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="0b71b-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="0b71b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="0b71b-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="0b71b-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="0b71b-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0b71b-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="0b71b-117">返す**MAPIERROR**構造体がない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0b71b-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0b71b-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b71b-118">Return value</span></span>

<span data-ttu-id="0b71b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0b71b-119">S_OK</span></span> 
  
> <span data-ttu-id="0b71b-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0b71b-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0b71b-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0b71b-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0b71b-122">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0b71b-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0b71b-123">解説</span><span class="sxs-lookup"><span data-stu-id="0b71b-123">Remarks</span></span>

<span data-ttu-id="0b71b-124">**IProfAdmin:: GetLastError**メソッドは、プロファイル管理オブジェクトのメソッド呼び出しから返された最後のエラーに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="0b71b-124">The **IProfAdmin::GetLastError** method retrieves information about the last error returned from a method call for the profile administration object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0b71b-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0b71b-125">Notes to callers</span></span>

<span data-ttu-id="0b71b-126">**MAPIERROR**構造体は、 _lppMAPIError_パラメーターで指定された MAPI が S_OK を返す場合にのみ\*\*\*\* 使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b71b-126">You can use the **MAPIERROR** structure, if MAPI supplies one, pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="0b71b-127">MAPI では、エラーについてのレポートを作成するために最後のエラーが発生したかどうかを判断できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0b71b-127">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="0b71b-128">このような場合、 _lppMAPIError_で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="0b71b-128">In this situation, a pointer to NULL is returned in  _lppMAPIError_.</span></span> 
  
<span data-ttu-id="0b71b-129">**MAPIERROR**構造の MAPI に割り当てられているすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0b71b-129">To release all the memory allocated by MAPI for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="0b71b-130">**GetLastError**メソッドの詳細については、「[拡張エラーの使用](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b71b-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b71b-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="0b71b-131">See also</span></span>



[<span data-ttu-id="0b71b-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0b71b-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="0b71b-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0b71b-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0b71b-134">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0b71b-134">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

