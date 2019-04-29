---
title: imapiviewcontextgetprintsetup
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a58e723113f70c10b5c8468f5bdd0d8d9014bd2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425128"
---
# <a name="imapiviewcontextgetprintsetup"></a><span data-ttu-id="69f6f-103">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="69f6f-103">IMAPIViewContext::GetPrintSetup</span></span>

  
  
<span data-ttu-id="69f6f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69f6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69f6f-105">現在の印刷情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-105">Retrieves current printing information.</span></span>
  
```cpp
HRESULT GetPrintSetup(
ULONG ulFlags,
LPFORMPRINTSETUP FAR * lppFormPrintSetup
);
```

## <a name="parameters"></a><span data-ttu-id="69f6f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="69f6f-106">Parameters</span></span>

 <span data-ttu-id="69f6f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69f6f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="69f6f-108">順番返される文字列の型を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="69f6f-108">[in] Bitmask of flags that controls the type of the returned strings.</span></span> <span data-ttu-id="69f6f-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="69f6f-109">The following flag can be set:</span></span>
    
<span data-ttu-id="69f6f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="69f6f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="69f6f-111">返される文字列は、Unicode 形式です。</span><span class="sxs-lookup"><span data-stu-id="69f6f-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="69f6f-112">MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="69f6f-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="69f6f-113">_lppformprintsetup_</span><span class="sxs-lookup"><span data-stu-id="69f6f-113">_lppFormPrintSetup_</span></span>
  
> <span data-ttu-id="69f6f-114">読み上げ印刷情報を保持する構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="69f6f-114">[out] Pointer to a pointer to a structure that holds the printing information.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="69f6f-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="69f6f-115">Return value</span></span>

<span data-ttu-id="69f6f-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="69f6f-116">S_OK</span></span> 
  
> <span data-ttu-id="69f6f-117">印刷情報が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="69f6f-117">The printing information was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69f6f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="69f6f-118">Remarks</span></span>

<span data-ttu-id="69f6f-119">Form オブジェクトは、現在のメッセージを印刷する前に、プリンターの設定に関する情報を取得するために**imapiviewcontext:: getprintsetup**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-119">Form objects call the **IMAPIViewContext::GetPrintSetup** method to retrieve information about the printer setup before attempting to print the current message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="69f6f-120">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="69f6f-120">Notes to implementers</span></span>

<span data-ttu-id="69f6f-121">Win32 関数**GlobalAlloc**を使用して、 [formprintsetup](formprintsetup.md)構造の**hdevmode**および**hDevName**メンバーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="69f6f-121">Allocate the **hDevMode** and **hDevName** members of the [FORMPRINTSETUP](formprintsetup.md) structure using the Win32 function **GlobalAlloc**.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="69f6f-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="69f6f-122">Notes to callers</span></span>

<span data-ttu-id="69f6f-123">_lppformprintsetup_パラメーターで指定された**formprintsetup**構造の**hdevmode**および**hDevName**メンバーが Unicode 文字列であると想定される場合は、 _ulflags_を MAPI_UNICODE に設定します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-123">If you expect the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure pointed to by the  _lppFormPrintSetup_ parameter to be Unicode strings, set  _ulFlags_ to MAPI_UNICODE.</span></span> <span data-ttu-id="69f6f-124">それ以外の場合、 **getprintsetup**は ANSI 形式の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-124">Otherwise, **GetPrintSetup** will return these strings in ANSI format.</span></span> 
  
<span data-ttu-id="69f6f-125">Win32 関数**GlobalFree**を呼び出すことにより、 **formprintsetup**構造の**hdevmode**および**hDevName**メンバーを解放します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-125">Free the **hDevMode** and **hDevName** members of the **FORMPRINTSETUP** structure by calling the Win32 function **GlobalFree**.</span></span> <span data-ttu-id="69f6f-126">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出すことで、 **formprintsetup**構造全体を解放します。</span><span class="sxs-lookup"><span data-stu-id="69f6f-126">Free the entire **FORMPRINTSETUP** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69f6f-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="69f6f-127">See also</span></span>



[<span data-ttu-id="69f6f-128">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="69f6f-128">FORMPRINTSETUP</span></span>](formprintsetup.md)
  
[<span data-ttu-id="69f6f-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69f6f-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

