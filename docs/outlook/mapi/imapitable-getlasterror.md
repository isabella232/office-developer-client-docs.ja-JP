---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593817"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="57263-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="57263-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="57263-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57263-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57263-105">テーブルの前のエラーに関する情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="57263-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="57263-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57263-106">Parameters</span></span>

 <span data-ttu-id="57263-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="57263-107">_hResult_</span></span>
  
> <span data-ttu-id="57263-108">[in]HRESULT がメソッドの以前の呼び出しで生成されたエラーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="57263-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="57263-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57263-109">_ulFlags_</span></span>
  
> <span data-ttu-id="57263-110">[in]関数が返す文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="57263-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="57263-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="57263-111">The following flag can be set:</span></span>
    
<span data-ttu-id="57263-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="57263-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="57263-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="57263-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="57263-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="57263-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="57263-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="57263-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="57263-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報が含まれている返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57263-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="57263-117">適切な情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="57263-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="57263-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="57263-118">Return value</span></span>

<span data-ttu-id="57263-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="57263-119">S_OK</span></span> 
  
> <span data-ttu-id="57263-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="57263-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="57263-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="57263-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="57263-122">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装には、Unicode のみサポートしています。</span><span class="sxs-lookup"><span data-stu-id="57263-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="57263-123">注釈</span><span class="sxs-lookup"><span data-stu-id="57263-123">Remarks</span></span>

<span data-ttu-id="57263-124">**IMAPITable::GetLastError**メソッドは、可能な場合、失敗したメソッド呼び出しに関する詳細についてを返します。</span><span class="sxs-lookup"><span data-stu-id="57263-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="57263-125">メッセージまたはダイアログ ボックスでは、この情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="57263-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="57263-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="57263-126">Notes to callers</span></span>

<span data-ttu-id="57263-127">エラーに関する情報をユーザーに表示する必要があるときに、 **GetLastError**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57263-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="57263-128">[MAPIERROR](mapierror.md)の使用を行うことができます構造が、 _lppMAPIError_パラメーターが指す場合は、table オブジェクトでは 1 つが提供される**GetLastError**が S_OK を返す場合にのみです。</span><span class="sxs-lookup"><span data-stu-id="57263-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="57263-129">テーブルの実装では、どのような最後のエラーまたはエラーの報告には関係ありませんを決定できません。</span><span class="sxs-lookup"><span data-stu-id="57263-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="57263-130">このような場合は、 _lppMAPIError_でポインターは NULL に設定します。</span><span class="sxs-lookup"><span data-stu-id="57263-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="57263-131">**MAPIERROR**構造体に割り当てられたすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="57263-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="57263-132">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57263-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57263-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="57263-133">See also</span></span>



[<span data-ttu-id="57263-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="57263-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="57263-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="57263-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="57263-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57263-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

