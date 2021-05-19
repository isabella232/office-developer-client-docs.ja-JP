---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434250"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="678f2-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="678f2-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="678f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="678f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="678f2-105">以前のアドレス [帳プロバイダー エラー](mapierror.md) に関する情報を含む MAPIERROR 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="678f2-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="678f2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="678f2-106">Parameters</span></span>

 <span data-ttu-id="678f2-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="678f2-107">_hResult_</span></span>
  
> <span data-ttu-id="678f2-108">[in]前のメソッド呼び出しで生成されたエラー値のハンドル。</span><span class="sxs-lookup"><span data-stu-id="678f2-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="678f2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="678f2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="678f2-110">[in]返される文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="678f2-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="678f2-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="678f2-111">The following flag can be set:</span></span>
    
<span data-ttu-id="678f2-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="678f2-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="678f2-113">_lppMAPIError_ パラメーターで返される **MAPIERROR** 構造体の文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="678f2-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="678f2-114">このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="678f2-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="678f2-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="678f2-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="678f2-116">[out]エラーのバージョン、コンポーネント、コンテキスト情報を含む **MAPIERROR** 構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="678f2-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="678f2-117">プロバイダーが適切な情報を MAPIERROR 構造体に指定できない場合は  _、lppMAPIError_ パラメーターを **NULL** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="678f2-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="678f2-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="678f2-118">Return value</span></span>

<span data-ttu-id="678f2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="678f2-119">S_OK</span></span> 
  
> <span data-ttu-id="678f2-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="678f2-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="678f2-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="678f2-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="678f2-122">アドレス帳MAPI_UNICODEフラグが設定され、アドレス帳プロバイダーが Unicode をサポートしていないか、MAPI_UNICODE が設定されていないと、アドレス帳プロバイダーは Unicode のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="678f2-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="678f2-123">注釈</span><span class="sxs-lookup"><span data-stu-id="678f2-123">Remarks</span></span>

<span data-ttu-id="678f2-124">アドレス帳プロバイダーは **、GetLastError メソッドを実装して** 、失敗した以前のメソッド呼び出しに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="678f2-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="678f2-125">発信者は **、MAPIERROR** 構造のデータをダイアログ ボックスに含めて、エラーに関する詳細情報をユーザーに提供できます。</span><span class="sxs-lookup"><span data-stu-id="678f2-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="678f2-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="678f2-126">Notes to callers</span></span>

<span data-ttu-id="678f2-127">アドレス帳プロバイダーが構造体を提供する場合、および **GetLastError** が関数を返す場合にのみ _、lppMAPIError_ パラメーターが示す **MAPIERROR** 構造をS_OK。</span><span class="sxs-lookup"><span data-stu-id="678f2-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="678f2-128">アドレス帳プロバイダーは、最後のエラーが何だったのか、エラーについて報告する必要がなにもない場合があります。</span><span class="sxs-lookup"><span data-stu-id="678f2-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="678f2-129">この状況では、アドレス帳プロバイダーは、代わりに  _lppMAPIError_ で NULL へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="678f2-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="678f2-130">**GetLastError メソッドの詳細については、「MAPI** 拡張 [エラー」を参照してください](mapi-extended-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="678f2-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="678f2-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="678f2-131">See also</span></span>



[<span data-ttu-id="678f2-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="678f2-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="678f2-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="678f2-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="678f2-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="678f2-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

