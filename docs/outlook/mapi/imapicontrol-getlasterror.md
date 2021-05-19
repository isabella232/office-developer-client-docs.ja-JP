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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421152"
---
# <a name="imapicontrolgetlasterror"></a><span data-ttu-id="335a3-103">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="335a3-103">IMAPIControl::GetLastError</span></span>

  
  
<span data-ttu-id="335a3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="335a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="335a3-105">前のボタン コントロール エラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="335a3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="335a3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="335a3-106">Parameters</span></span>

 <span data-ttu-id="335a3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="335a3-107">_hResult_</span></span>
  
> <span data-ttu-id="335a3-108">[in]前のメソッド呼び出しで生成されたエラー値のハンドル。</span><span class="sxs-lookup"><span data-stu-id="335a3-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="335a3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="335a3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="335a3-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="335a3-110">[in] A bitmask of flags that controls the type of the strings returned.</span></span> <span data-ttu-id="335a3-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="335a3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="335a3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="335a3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="335a3-113">_lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="335a3-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="335a3-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="335a3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="335a3-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="335a3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="335a3-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="335a3-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="335a3-117">プロバイダーが適切な情報を MAPIERROR 構造体に指定できない場合は  _、lppMAPIError_ パラメーターを **NULL** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="335a3-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="335a3-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="335a3-118">Return value</span></span>

<span data-ttu-id="335a3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="335a3-119">S_OK</span></span> 
  
> <span data-ttu-id="335a3-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="335a3-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="335a3-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="335a3-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="335a3-122">このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="335a3-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="335a3-123">注釈</span><span class="sxs-lookup"><span data-stu-id="335a3-123">Remarks</span></span>

<span data-ttu-id="335a3-124">サービス プロバイダーは **、IMAPIControl::GetLastError** メソッドを実装して、失敗した以前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="335a3-124">Service providers implement the **IMAPIControl::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="335a3-125">MAPI は、メッセージまたはダイアログ ボックスに **MAPIERROR** 構造のデータを表示することで、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="335a3-125">MAPI can give users detailed information about the error by displaying the data from the **MAPIERROR** structure in a message or dialog box.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="335a3-126">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="335a3-126">Notes to implementers</span></span>

<span data-ttu-id="335a3-127">エラーごとに **MAPIERROR** 構造に含める情報を持つ必要はない。</span><span class="sxs-lookup"><span data-stu-id="335a3-127">You do not need to have information to include in the **MAPIERROR** structure for every error.</span></span> <span data-ttu-id="335a3-128">以前のエラーが何だったかを判断できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="335a3-128">It may not be possible to determine what the previous error was.</span></span> <span data-ttu-id="335a3-129">情報がある場合は **、MAPIERROR** S_OK適切なデータを返します。</span><span class="sxs-lookup"><span data-stu-id="335a3-129">If you have information, return S_OK and the appropriate data in the **MAPIERROR** structure.</span></span> <span data-ttu-id="335a3-130">情報が使用できない場合は  _、lppMAPIError_ パラメーター S_OK NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="335a3-130">If no information is available, return S_OK and a pointer to NULL for the  _lppMAPIError_ parameter.</span></span> 
  
<span data-ttu-id="335a3-131">**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="335a3-131">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="335a3-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="335a3-132">See also</span></span>



[<span data-ttu-id="335a3-133">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="335a3-133">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="335a3-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="335a3-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="335a3-135">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="335a3-135">IMAPIControl : IUnknown</span></span>](imapicontroliunknown.md)

