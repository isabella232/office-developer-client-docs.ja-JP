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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419003"
---
# <a name="imapitablegetlasterror"></a><span data-ttu-id="c168f-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c168f-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="c168f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c168f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c168f-105">表の前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="c168f-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c168f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c168f-106">Parameters</span></span>

 <span data-ttu-id="c168f-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c168f-107">_hResult_</span></span>
  
> <span data-ttu-id="c168f-108">順番前のメソッド呼び出しで生成されたエラーを含む HRESULT。</span><span class="sxs-lookup"><span data-stu-id="c168f-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="c168f-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c168f-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c168f-110">順番返される文字列の型を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c168f-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="c168f-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c168f-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c168f-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c168f-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c168f-113">_lppMAPIError_パラメーターで返される**MAPIERROR**構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="c168f-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c168f-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="c168f-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c168f-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c168f-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c168f-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む、返された**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c168f-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="c168f-117">_lppMAPIError_パラメーターは、適切な情報を持つ**MAPIERROR**構造体を提供できない場合は NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c168f-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c168f-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="c168f-118">Return value</span></span>

<span data-ttu-id="c168f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c168f-119">S_OK</span></span> 
  
> <span data-ttu-id="c168f-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c168f-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c168f-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c168f-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c168f-122">MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode がサポートされているかどうか。</span><span class="sxs-lookup"><span data-stu-id="c168f-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c168f-123">注釈</span><span class="sxs-lookup"><span data-stu-id="c168f-123">Remarks</span></span>

<span data-ttu-id="c168f-124">**IMAPITable:: GetLastError**メソッドは、エラーが発生した前のメソッド呼び出しに関する詳細情報を返します (使用可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="c168f-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="c168f-125">この情報は、メッセージまたはダイアログボックスに表示できます。</span><span class="sxs-lookup"><span data-stu-id="c168f-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c168f-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c168f-126">Notes to callers</span></span>

<span data-ttu-id="c168f-127">エラーに関する情報をユーザーに表示する必要がある場合は、必ず**GetLastError**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c168f-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="c168f-128">table オブジェクトが S_OK を返す場合にのみ、 _lppMAPIError_パラメーターでポイントする[MAPIERROR](mapierror.md)構造を使用できます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c168f-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c168f-129">場合によっては、テーブルの実装によって、最後のエラーが発生したかどうか、またはエラーについてのレポートを作成できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="c168f-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="c168f-130">この状況では、 _lppMAPIError_にあるポインターが NULL に設定されています。</span><span class="sxs-lookup"><span data-stu-id="c168f-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="c168f-131">**MAPIERROR**構造体に割り当てられているすべてのメモリを解放するには、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c168f-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="c168f-132">**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c168f-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c168f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c168f-133">See also</span></span>



[<span data-ttu-id="c168f-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c168f-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c168f-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c168f-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c168f-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c168f-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

