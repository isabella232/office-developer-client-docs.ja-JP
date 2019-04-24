---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279644"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="3d1ac-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3d1ac-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="3d1ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d1ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d1ac-105">プロバイダー管理オブジェクトに発生した前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="3d1ac-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d1ac-106">Parameters</span></span>

 <span data-ttu-id="3d1ac-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="3d1ac-107">_hResult_</span></span>
  
> <span data-ttu-id="3d1ac-108">順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="3d1ac-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d1ac-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3d1ac-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="3d1ac-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3d1ac-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3d1ac-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3d1ac-113">_lppMAPIError_パラメーターで返される**MAPIERROR**の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="3d1ac-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="3d1ac-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="3d1ac-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="3d1ac-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="3d1ac-117">返す**MAPIERROR**が存在しない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3d1ac-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="3d1ac-118">Return value</span></span>

<span data-ttu-id="3d1ac-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d1ac-119">S_OK</span></span> 
  
> <span data-ttu-id="3d1ac-120">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="3d1ac-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3d1ac-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3d1ac-122">MAPI_UNICODE フラグが設定されていて、 **getlasterror**が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、 **getlasterror**が unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3d1ac-123">解説</span><span class="sxs-lookup"><span data-stu-id="3d1ac-123">Remarks</span></span>

<span data-ttu-id="3d1ac-124">**IProviderAdmin:: GetLastError**メソッドは、失敗した前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="3d1ac-125">呼び出し元は、 **MAPIERROR**構造のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d1ac-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="3d1ac-126">Notes to callers</span></span>

<span data-ttu-id="3d1ac-127">**MAPIERROR**構造体は、MAPI が1を提供する場合に、 **GetLastError**が S_OK を返す場合にのみ、 _lppMAPIError_パラメーターがポイントすることを示します。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="3d1ac-128">MAPI では、エラーについてのレポートを作成するために最後のエラーが発生したかどうかを判断できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="3d1ac-129">このような場合、代わりに_lppMAPIError_で NULL へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="3d1ac-130">**GetLastError**メソッドの詳細については、「[拡張エラーの使用](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d1ac-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3d1ac-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d1ac-131">See also</span></span>



[<span data-ttu-id="3d1ac-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="3d1ac-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="3d1ac-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3d1ac-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3d1ac-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d1ac-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

