---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ef5fee7a2e84133f88a00703f7602831d26e3d3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594727"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="53739-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="53739-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="53739-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53739-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53739-105">前のボタン コントロールのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="53739-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="53739-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="53739-106">Parameters</span></span>

 <span data-ttu-id="53739-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="53739-107">_hResult_</span></span>
  
> <span data-ttu-id="53739-108">[in]以前のメソッドの呼び出しで生成されたエラーの値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="53739-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="53739-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53739-109">_ulFlags_</span></span>
  
> <span data-ttu-id="53739-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="53739-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="53739-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="53739-111">The following flag can be set:</span></span>
    
<span data-ttu-id="53739-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53739-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53739-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="53739-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="53739-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="53739-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="53739-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="53739-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="53739-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="53739-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="53739-117">プロバイダーは、適切な情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="53739-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="53739-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="53739-118">Return value</span></span>

<span data-ttu-id="53739-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="53739-119">S_OK</span></span> 
  
> <span data-ttu-id="53739-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="53739-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="53739-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="53739-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="53739-122">か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="53739-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53739-123">注釈</span><span class="sxs-lookup"><span data-stu-id="53739-123">Remarks</span></span>

<span data-ttu-id="53739-124">サービス プロバイダーでは、失敗したメソッド呼び出しに関する情報を提供する**IMAPIControl::GetLastError**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="53739-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="53739-125">MAPI は、メッセージまたはダイアログ ボックスで、 **MAPIERROR**構造体のデータを表示することで、エラーに関する詳細な情報をユーザーに与えることができます。</span><span class="sxs-lookup"><span data-stu-id="53739-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="53739-126">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="53739-126">Notes to implementers</span></span>

<span data-ttu-id="53739-127">情報がすべてのエラー、構造体の**MAPIERROR**にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="53739-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="53739-128">前のエラーのあったものを決定することができないことがあります。</span><span class="sxs-lookup"><span data-stu-id="53739-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="53739-129">情報がある場合は、 **MAPIERROR**構造体に S_OK と適切なデータを返します。</span><span class="sxs-lookup"><span data-stu-id="53739-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="53739-130">情報がない場合は、S_OK とポインターに戻ります NULL _lppMAPIError_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="53739-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="53739-131">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53739-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53739-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="53739-132">See also</span></span>



[<span data-ttu-id="53739-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="53739-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="53739-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="53739-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="53739-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53739-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

