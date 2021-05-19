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
# <a name="imapitablegetlasterror"></a><span data-ttu-id="a8550-103">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a8550-103">IMAPITable::GetLastError</span></span>

  
  
<span data-ttu-id="a8550-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8550-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8550-105">テーブルの前 [のエラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a8550-105">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error on the table.</span></span> 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a8550-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a8550-106">Parameters</span></span>

 <span data-ttu-id="a8550-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a8550-107">_hResult_</span></span>
  
> <span data-ttu-id="a8550-108">[in]前のメソッド呼び出しで生成されたエラーを含む HRESULT。</span><span class="sxs-lookup"><span data-stu-id="a8550-108">[in] HRESULT containing the error generated in the previous method call.</span></span>
    
 <span data-ttu-id="a8550-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8550-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a8550-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a8550-110">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="a8550-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a8550-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a8550-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8550-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a8550-113">_lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a8550-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a8550-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a8550-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a8550-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a8550-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a8550-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む、返される **MAPIERROR** 構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a8550-116">[out] Pointer to a pointer to the returned **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="a8550-117">_適切な情報を持つ MAPIERROR_ 構造体を指定できない場合は、lppMAPIError パラメーターを **NULL** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a8550-117">The  _lppMAPIError_ parameter can be set to NULL if a **MAPIERROR** structure with appropriate information cannot be provided.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a8550-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="a8550-118">Return value</span></span>

<span data-ttu-id="a8550-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8550-119">S_OK</span></span> 
  
> <span data-ttu-id="a8550-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a8550-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a8550-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a8550-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a8550-122">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定MAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a8550-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation only supports Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8550-123">注釈</span><span class="sxs-lookup"><span data-stu-id="a8550-123">Remarks</span></span>

<span data-ttu-id="a8550-124">**IMAPITable::GetLastError** メソッドは、エラーが発生した以前のメソッド呼び出しに関する詳細情報 (利用可能な場合) を返します。</span><span class="sxs-lookup"><span data-stu-id="a8550-124">The **IMAPITable::GetLastError** method returns detailed information, if available, about a prior method call that failed.</span></span> <span data-ttu-id="a8550-125">この情報は、メッセージまたはダイアログ ボックスに表示できます。</span><span class="sxs-lookup"><span data-stu-id="a8550-125">This information can be displayed in a message or a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a8550-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a8550-126">Notes to callers</span></span>

<span data-ttu-id="a8550-127">ユーザー **にエラーに関** する情報を表示する必要がある場合は常に GetLastError を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a8550-127">Call **GetLastError** whenever you need to display information about an error to the user.</span></span> 
  
<span data-ttu-id="a8550-128">テーブル オブジェクトが 1 つを提供する場合は **、GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターが指す [MAPIERROR](mapierror.md)構造をS_OK。</span><span class="sxs-lookup"><span data-stu-id="a8550-128">You can make use of the [MAPIERROR](mapierror.md) structure pointed to by the  _lppMAPIError_ parameter if the table object supplies one only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a8550-129">テーブルの実装では、最後のエラーが何だったのかを判断できない場合や、エラーについて報告する必要がなにもない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a8550-129">Sometimes the table implementation cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a8550-130">この状況では  _、lppMAPIError のポインターは_ NULL に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a8550-130">In this situation, the pointer at  _lppMAPIError_ is set to NULL.</span></span> 
  
<span data-ttu-id="a8550-131">**MAPIERROR** 構造体に割り当てられているすべてのメモリを解放するには [、MAPIFreeBuffer 関数を呼び出](mapifreebuffer.md)します。</span><span class="sxs-lookup"><span data-stu-id="a8550-131">To release all the memory allocated for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="a8550-132">**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="a8550-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a8550-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a8550-133">See also</span></span>



[<span data-ttu-id="a8550-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a8550-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a8550-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a8550-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a8550-136">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8550-136">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

