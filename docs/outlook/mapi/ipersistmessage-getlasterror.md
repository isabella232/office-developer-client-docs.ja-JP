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
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="a2cd3-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a2cd3-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="a2cd3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2cd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2cd3-105">form オブジェクトの前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="a2cd3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2cd3-106">Parameters</span></span>

 <span data-ttu-id="a2cd3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="a2cd3-107">_hResult_</span></span>
  
> <span data-ttu-id="a2cd3-108">順番前のメソッド呼び出しで生成されたエラー値を含む HRESULT データ型。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="a2cd3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2cd3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a2cd3-110">順番返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="a2cd3-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a2cd3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a2cd3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a2cd3-113">_lppMAPIError_パラメーターで返される[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="a2cd3-114">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="a2cd3-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="a2cd3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="a2cd3-116">読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="a2cd3-117">フォームが**MAPIERROR**構造に適切な情報を提供できない場合は、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a2cd3-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="a2cd3-118">Return value</span></span>

<span data-ttu-id="a2cd3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2cd3-119">S_OK</span></span> 
  
> <span data-ttu-id="a2cd3-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a2cd3-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a2cd3-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a2cd3-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a2cd3-122">MAPI_UNICODE フラグが設定されていて、アドレス帳プロバイダーが unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、アドレス帳プロバイダーが unicode のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2cd3-123">注釈</span><span class="sxs-lookup"><span data-stu-id="a2cd3-123">Remarks</span></span>

<span data-ttu-id="a2cd3-124">Form オブジェクトは、失敗した前のメソッド呼び出しに関する情報を提供する**IPersistMessage:: GetLastError**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="a2cd3-125">フォームビューアーでは、 [MAPIERROR](mapierror.md)構造体のデータをダイアログボックスに含めることによって、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="a2cd3-126">**GetLastError**を呼び出しても、フォームの状態には影響しません。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="a2cd3-127">**GetLastError**が戻ると、フォームは呼び出しが行われる前の状態のままになります。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a2cd3-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a2cd3-128">Notes to callers</span></span>

<span data-ttu-id="a2cd3-129">フォームが S_OK を返す場合にのみ、 _lppMAPIError_パラメーターによってポイントされている場合は、 **MAPIERROR**構造体を使用できます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a2cd3-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="a2cd3-130">場合によっては、フォームで、エラーについてのレポートに最後のエラーがあったかどうかを判断できないこともあります。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="a2cd3-131">このような状況では、フォームは代わりに_lppMAPIError_で NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="a2cd3-132">**GetLastError**メソッドの詳細については、「 [MAPI 拡張エラー](mapi-extended-errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2cd3-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2cd3-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2cd3-133">See also</span></span>



[<span data-ttu-id="a2cd3-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="a2cd3-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="a2cd3-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a2cd3-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a2cd3-136">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2cd3-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

