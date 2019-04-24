---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357443"
---
# <a name="lpfnbutton"></a><span data-ttu-id="bd366-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="bd366-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="bd366-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd366-105">[アドレス帳] ダイアログボックスでオプションのボタンコントロールをアクティブ化するために MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="bd366-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="bd366-106">通常、このボタンは [**詳細**] ボタンです。</span><span class="sxs-lookup"><span data-stu-id="bd366-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd366-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bd366-107">Header file:</span></span>  <br/> |<span data-ttu-id="bd366-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bd366-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bd366-109">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="bd366-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="bd366-110">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="bd366-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="bd366-111">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="bd366-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="bd366-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="bd366-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="bd366-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bd366-113">Parameters</span></span>

 <span data-ttu-id="bd366-114">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="bd366-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="bd366-115">順番この関数が表示する、任意のダイアログボックスまたはウィンドウの親ウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="bd366-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="bd366-116">_lpvcontext_</span><span class="sxs-lookup"><span data-stu-id="bd366-116">_lpvContext_</span></span>
  
> <span data-ttu-id="bd366-117">順番MAPI がコールバック関数に渡す任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bd366-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="bd366-118">この値は、クライアントアプリケーションにとって重要なアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="bd366-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="bd366-119">通常、c++ コードでは、 _lpvcontext_は c++ オブジェクトへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="bd366-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="bd366-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bd366-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="bd366-121">順番_lpselection_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="bd366-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="bd366-122">_lpselection_</span><span class="sxs-lookup"><span data-stu-id="bd366-122">_lpSelection_</span></span>
  
> <span data-ttu-id="bd366-123">順番ダイアログボックスの選択範囲を定義するエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bd366-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="bd366-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd366-124">_ulFlags_</span></span>
  
> <span data-ttu-id="bd366-125">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="bd366-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd366-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="bd366-126">Return value</span></span>

<span data-ttu-id="bd366-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd366-127">S_OK</span></span> 
  
> <span data-ttu-id="bd366-128">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="bd366-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd366-129">解説</span><span class="sxs-lookup"><span data-stu-id="bd366-129">Remarks</span></span>

<span data-ttu-id="bd366-130">クライアントアプリケーションは、 **LPFNBUTTON**プロトタイプに基づいてコールバック関数を呼び出し、[詳細] ダイアログボックスにボタンを定義します。</span><span class="sxs-lookup"><span data-stu-id="bd366-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="bd366-131">クライアントは、 [IAddrBook::D etails](iaddrbook-details.md)メソッドへの呼び出しで、コールバック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="bd366-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="bd366-132">サービスプロバイダーは、 **LPFNBUTTON**プロトタイプに基づいて、[詳細] ダイアログボックスにボタンを定義するためのフック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bd366-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="bd366-133">プロバイダーは、 [imapisupport::D etails](imapisupport-details.md)メソッドへの呼び出しで、このフック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="bd366-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="bd366-134">どちらの場合も、ダイアログボックスが表示され、ユーザーが [定義済み] ボタンを選択すると、MAPI は**LPFNBUTTON**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bd366-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd366-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd366-135">See also</span></span>



[<span data-ttu-id="bd366-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="bd366-136">BuildDisplayTable</span></span>](builddisplaytable.md)

