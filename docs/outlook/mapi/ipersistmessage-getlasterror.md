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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 16f091f4d9527cd82ebc1d1eadee2fb55b481929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801115"
---
# <a name="ipersistmessagegetlasterror"></a><span data-ttu-id="c6d0a-103">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="c6d0a-103">IPersistMessage::GetLastError</span></span>

  
  
<span data-ttu-id="c6d0a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6d0a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c6d0a-105">フォーム オブジェクトでは、前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="c6d0a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="c6d0a-106">Parameters</span></span>

 <span data-ttu-id="c6d0a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="c6d0a-107">_hResult_</span></span>
  
> <span data-ttu-id="c6d0a-108">[in]以前のメソッドの呼び出しで生成されたエラー値を含む HRESULT のデータ型です。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-108">[in] An HRESULT data type that contains the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="c6d0a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c6d0a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c6d0a-110">[in]返される文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="c6d0a-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="c6d0a-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6d0a-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c6d0a-113">_LppMAPIError_パラメーターに返された[MAPIERROR](mapierror.md)構造体の文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-113">The strings in the [MAPIERROR](mapierror.md) structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="c6d0a-114">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="c6d0a-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="c6d0a-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="c6d0a-116">[out]エラーのバージョン、コンポーネント、およびコンテキストの情報を格納する**MAPIERROR**構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="c6d0a-117">フォームは、 **MAPIERROR**構造体の適切な情報を提供できない場合、 _lppMAPIError_パラメーターを NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-117">The  _lppMAPIError_ parameter can be set to NULL if the form cannot supply appropriate information for a **MAPIERROR** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6d0a-118">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c6d0a-118">Return value</span></span>

<span data-ttu-id="c6d0a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6d0a-119">S_OK</span></span> 
  
> <span data-ttu-id="c6d0a-120">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c6d0a-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c6d0a-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c6d0a-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c6d0a-122">MAPI_UNICODE フラグが設定されたアドレス帳プロバイダーが Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、アドレス帳プロバイダーは、Unicode だけをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6d0a-123">備考</span><span class="sxs-lookup"><span data-stu-id="c6d0a-123">Remarks</span></span>

<span data-ttu-id="c6d0a-124">フォーム オブジェクトでは、失敗したメソッド呼び出しに関する情報を提供する**IPersistMessage::GetLastError**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-124">Form objects implement the **IPersistMessage::GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="c6d0a-125">フォーム ビューアーは、ダイアログ ボックスに[MAPIERROR](mapierror.md)構造体のデータを含めることによって、ユーザーにエラーに関する詳細な情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-125">Form viewers can provide their users with detailed information about the error by including the data from the [MAPIERROR](mapierror.md) structure in a dialog box.</span></span> 
  
<span data-ttu-id="c6d0a-126">**GetLastError**の呼び出しは、フォームの状態には影響しません。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-126">A call to **GetLastError** does not affect the state of the form.</span></span> <span data-ttu-id="c6d0a-127">**GetLastError**から制御が戻るとき、フォームは、呼び出しが行われた前の状態には。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-127">When **GetLastError** returns, the form remains in the state that it was in before the call was made.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c6d0a-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c6d0a-128">Notes to callers</span></span>

<span data-ttu-id="c6d0a-129">フォームが用意されて、1 つが**発生しました**が S_OK を返す場合にのみ、 _lppMAPIError_パラメーターで示される場合は、 **MAPIERROR**構造体を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-129">You can use the **MAPIERROR** structure, if the form supplies one, that is pointed to by the  _lppMAPIError_ parameter only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="c6d0a-130">どのような最後のエラーまたはエラーを報告するのにはそれ以上には、フォームは判断できません。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-130">Sometimes the form cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="c6d0a-131">このような場合は、フォームにポインターを返します NULL _lppMAPIError_の代わりにします。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-131">In this situation, the form returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="c6d0a-132">**GetLastError**メソッドの詳細については、 [MAPI の拡張エラー](mapi-extended-errors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6d0a-132">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6d0a-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6d0a-133">See also</span></span>



[<span data-ttu-id="c6d0a-134">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="c6d0a-134">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="c6d0a-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c6d0a-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="c6d0a-136">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6d0a-136">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

