---
title: IMAPIViewContextGetPrintSetup
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetPrintSetup
api_type:
- COM
ms.assetid: eaf3bafb-975d-42c8-99ea-7f9ef9c934ba
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7fdf76bc56feb7e46370e7fcf66c55d229933eca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800880"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="7934e-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="7934e-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="7934e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7934e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7934e-105">現在、印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="7934e-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="7934e-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7934e-106">Parameters</span></span>

 <span data-ttu-id="7934e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7934e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7934e-108">[in]関数が返す文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7934e-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="7934e-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7934e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="7934e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7934e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7934e-111">関数が返す文字列は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="7934e-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="7934e-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。</span><span class="sxs-lookup"><span data-stu-id="7934e-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7934e-113">_lppFormPrintSetup_</span><span class="sxs-lookup"><span data-stu-id="7934e-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="7934e-114">[out]印刷の情報を保持する構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7934e-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7934e-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7934e-115">Return value</span></span>

<span data-ttu-id="7934e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="7934e-116">S_OK</span></span> 
  
> <span data-ttu-id="7934e-117">印刷の情報が正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="7934e-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7934e-118">備考</span><span class="sxs-lookup"><span data-stu-id="7934e-118">Remarks</span></span>

<span data-ttu-id="7934e-119">フォーム オブジェクトは、現在のメッセージを印刷する前に、プリンターのセットアップに関する情報を取得するために**IMAPIViewContext::GetPrintSetup**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7934e-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7934e-120">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="7934e-120">Notes to implementers</span></span>

<span data-ttu-id="7934e-121">**GlobalAlloc**の Win32 関数を使用する[FORMPRINTSETUP](formprintsetup.md)構造体の**hDevMode**および**hDevName**のメンバーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7934e-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7934e-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7934e-122">Notes to callers</span></span>

<span data-ttu-id="7934e-123">予定の場合、 **hDevMode** 、 **hDevName** 、 **FORMPRINTSETUP**構造体のメンバーが Unicode 文字列を指定する_lppFormPrintSetup_パラメーターが指す、 _ulFlags_を MAPI_UNICODE に設定します。</span><span class="sxs-lookup"><span data-stu-id="7934e-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="7934e-124">それ以外の場合、 **GetPrintSetup**では、ANSI 形式でこれらの文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="7934e-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="7934e-125">**GlobalFree**の Win32 関数を呼び出すことによって、 **hDevMode**および**hDevName** 、 **FORMPRINTSETUP**構造体のメンバーを解放します。</span><span class="sxs-lookup"><span data-stu-id="7934e-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="7934e-126">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことによって、全体の**FORMPRINTSETUP**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="7934e-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7934e-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7934e-127">See also</span></span>



[<span data-ttu-id="7934e-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="7934e-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="7934e-129">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7934e-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

