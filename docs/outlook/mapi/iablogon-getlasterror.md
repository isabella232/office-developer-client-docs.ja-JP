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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bead72ab2b394634217c9ae219a03a98752ef27d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800335"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="2720e-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2720e-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="2720e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2720e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2720e-105">以前のアドレス帳プロバイダーのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="2720e-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2720e-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2720e-106">Parameters</span></span>

 <span data-ttu-id="2720e-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="2720e-107">_hResult_</span></span>
  
> <span data-ttu-id="2720e-108">[in]以前のメソッドの呼び出しで生成されたエラーの値へのハンドル。</span><span class="sxs-lookup"><span data-stu-id="2720e-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="2720e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2720e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2720e-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="2720e-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="2720e-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2720e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2720e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2720e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2720e-113">_LppMAPIError_パラメーターに返された**MAPIERROR**構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="2720e-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="2720e-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="2720e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="2720e-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2720e-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2720e-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2720e-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2720e-117">プロバイダーは、適切な情報を含む**MAPIERROR**構造体を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2720e-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2720e-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2720e-118">Return value</span></span>

<span data-ttu-id="2720e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2720e-119">S_OK</span></span> 
  
> <span data-ttu-id="2720e-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="2720e-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2720e-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2720e-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2720e-122">MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2720e-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2720e-123">備考</span><span class="sxs-lookup"><span data-stu-id="2720e-123">Remarks</span></span>

<span data-ttu-id="2720e-124">アドレス帳プロバイダーは、失敗したメソッド呼び出しに関する情報を提供する**GetLastError**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="2720e-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="2720e-125">呼び出し元は、ダイアログ ボックスに**MAPIERROR**構造体のデータを含めることによって、エラーの詳細情報をユーザーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="2720e-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2720e-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2720e-126">Notes to callers</span></span>

<span data-ttu-id="2720e-127">**GetLastError**が S_OK を返す場合にのみ、アドレス帳プロバイダーは、構造体を提供する場合、 _lppMAPIError_パラメーターが指す**MAPIERROR**構造体を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2720e-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="2720e-128">場合によってどのような最後のエラーまたはエラーを報告するのにはそれ以上には、アドレス帳プロバイダーは判断できません。</span><span class="sxs-lookup"><span data-stu-id="2720e-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2720e-129">このような場合は、アドレス帳プロバイダーのポインター NULL に_lppMAPIError_の代わりに返します。</span><span class="sxs-lookup"><span data-stu-id="2720e-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2720e-130">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2720e-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2720e-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="2720e-131">See also</span></span>



[<span data-ttu-id="2720e-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2720e-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2720e-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2720e-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2720e-134">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2720e-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

