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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 63ddf6fd8f61834c7a7faa910f70bfd98715a703
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591325"
---
# <a name="iprovideradmingetlasterror"></a><span data-ttu-id="d0f08-103">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="d0f08-103">IProviderAdmin::GetLastError</span></span>

  
  
<span data-ttu-id="d0f08-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0f08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0f08-105">プロバイダーの管理オブジェクトに発生した前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="d0f08-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to the provider administration object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="d0f08-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d0f08-106">Parameters</span></span>

 <span data-ttu-id="d0f08-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="d0f08-107">_hResult_</span></span>
  
> <span data-ttu-id="d0f08-108">[in]以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="d0f08-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="d0f08-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0f08-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d0f08-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d0f08-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="d0f08-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d0f08-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d0f08-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0f08-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d0f08-113">_LppMAPIError_パラメーターに返される**MAPIERROR**の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="d0f08-113">The strings in the **MAPIERROR** returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="d0f08-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="d0f08-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="d0f08-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="d0f08-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="d0f08-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0f08-116">[out] A pointer to a pointer to the returned **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="d0f08-117">返すには、 **MAPIERROR**がない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d0f08-117">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0f08-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d0f08-118">Return value</span></span>

<span data-ttu-id="d0f08-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0f08-119">S_OK</span></span> 
  
> <span data-ttu-id="d0f08-120">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d0f08-120">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d0f08-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d0f08-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d0f08-122">か、MAPI_UNICODE フラグが設定された**発生しました**が、Unicode をサポートしていませんまたは MAPI_UNICODE が設定されていませんでしたし、 **GetLastError**は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d0f08-122">Either the MAPI_UNICODE flag was set and **GetLastError** does not support Unicode, or MAPI_UNICODE was not set and **GetLastError** supports only Unicode.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d0f08-123">注釈</span><span class="sxs-lookup"><span data-stu-id="d0f08-123">Remarks</span></span>

<span data-ttu-id="d0f08-124">**IProviderAdmin::GetLastError**メソッドでは、失敗したメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d0f08-124">The **IProviderAdmin::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="d0f08-125">呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="d0f08-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0f08-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d0f08-126">Notes to callers</span></span>

<span data-ttu-id="d0f08-127">**MAPIERROR**構造体を使用するには、その場合は、MAPI が提供、 _lppMAPIError_パラメーターが**発生しました**が S_OK を返す場合にのみを指しています。</span><span class="sxs-lookup"><span data-stu-id="d0f08-127">You can use the **MAPIERROR** structure, if MAPI supplies one, that the  _lppMAPIError_ parameter points to only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="d0f08-128">どのような最後のエラーまたはエラーを報告するのにはそれ以上には、MAPI は判断できません。</span><span class="sxs-lookup"><span data-stu-id="d0f08-128">Sometimes MAPI cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="d0f08-129">このような場合は、NULL へのポインターが返されます_lppMAPIError_の代わりにします。</span><span class="sxs-lookup"><span data-stu-id="d0f08-129">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="d0f08-130">**GetLastError**メソッドの詳細については、[拡張エラーの使用](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0f08-130">For more information about the **GetLastError** method, see [Using Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0f08-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0f08-131">See also</span></span>



[<span data-ttu-id="d0f08-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="d0f08-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="d0f08-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d0f08-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d0f08-134">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0f08-134">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)

