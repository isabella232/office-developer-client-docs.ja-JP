---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426710"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="2cc8c-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2cc8c-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="2cc8c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cc8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cc8c-105">フォーム オブジェクトの前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2cc8c-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2cc8c-106">Parameters</span></span>

 <span data-ttu-id="2cc8c-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2cc8c-107">_hResult_</span></span>
  
> <span data-ttu-id="2cc8c-108">[in]前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2cc8c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2cc8c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2cc8c-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2cc8c-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2cc8c-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2cc8c-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2cc8c-113">_lppMAPIError_ パラメーターで返される [MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2cc8c-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2cc8c-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2cc8c-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2cc8c-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2cc8c-117">フォームが MAPIERROR 構造に適切な情報を提供できない場合は  _、lppMAPIError_ パラメーターを **NULL に設定** できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2cc8c-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="2cc8c-118">Return value</span></span>

<span data-ttu-id="2cc8c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2cc8c-119">S_OK</span></span> 
  
> <span data-ttu-id="2cc8c-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2cc8c-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2cc8c-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2cc8c-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2cc8c-122">アドレス帳MAPI_UNICODEフラグが設定され、アドレス帳プロバイダーが Unicode をサポートしていないか、MAPI_UNICODE が設定されていないと、アドレス帳プロバイダーは Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2cc8c-123">注釈</span><span class="sxs-lookup"><span data-stu-id="2cc8c-123">Remarks</span></span>

<span data-ttu-id="2cc8c-124">フォーム オブジェクトは **、IPersistMessage::GetLastError** メソッドを実装して、失敗した以前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="2cc8c-125">フォーム ビューアーは、ダイアログ ボックスに [MAPIERROR](mapierror.md) 構造のデータを含め、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="2cc8c-126">**GetLastError の呼び出しは**、フォームの状態には影響を与えかねない。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="2cc8c-127">**GetLastError が** 返された場合、フォームは呼び出しが行われた前の状態のままです。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2cc8c-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2cc8c-128">Notes to callers</span></span>

<span data-ttu-id="2cc8c-129">フォームが 1 つを提供する場合は **、GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターによって指される **MAPIERROR** 構造をS_OK。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2cc8c-130">フォームで、最後のエラーが何だったのかを判断できない場合や、エラーについて報告する必要がなにもない場合があります。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2cc8c-131">この状況では、フォームは代わりに  _lppMAPIError_ で NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2cc8c-132">**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="2cc8c-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cc8c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="2cc8c-133">See also</span></span>



[<span data-ttu-id="2cc8c-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2cc8c-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2cc8c-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2cc8c-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2cc8c-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2cc8c-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

