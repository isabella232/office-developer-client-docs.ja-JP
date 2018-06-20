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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801279"
---
# <a name="lpfnbutton"></a><span data-ttu-id="a1136-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="a1136-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="a1136-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a1136-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a1136-105">MAPI が、アドレス帳] ダイアログ ボックスで、オプション ボタン コントロールをアクティブにするために呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1136-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="a1136-106">このボタンは、通常、**詳細**ボタンです。</span><span class="sxs-lookup"><span data-stu-id="a1136-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1136-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1136-107">Header file:</span></span>  <br/> |<span data-ttu-id="a1136-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1136-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a1136-109">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="a1136-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a1136-110">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a1136-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="a1136-111">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1136-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a1136-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1136-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a1136-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="a1136-113">Parameters</span></span>

 <span data-ttu-id="a1136-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a1136-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="a1136-115">[in]すべてのダイアログ ボックスの親ウィンドウまたはこの関数を表示するウィンドウのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="a1136-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="a1136-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="a1136-116">_lpvContext_</span></span>
  
> <span data-ttu-id="a1136-117">[in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="a1136-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="a1136-118">この値は、クライアント アプリケーションにとって意味のアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="a1136-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="a1136-119">通常、C++ コードでは、 _lpvContext_のポインターを表します C++ オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="a1136-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="a1136-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a1136-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="a1136-121">[in]_LpSelection_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="a1136-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="a1136-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="a1136-122">_lpSelection_</span></span>
  
> <span data-ttu-id="a1136-123">[in]ダイアログ ボックスで選択範囲を定義するエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1136-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="a1136-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1136-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a1136-125">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a1136-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1136-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a1136-126">Return value</span></span>

<span data-ttu-id="a1136-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1136-127">S_OK</span></span> 
  
> <span data-ttu-id="a1136-128">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a1136-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1136-129">����</span><span class="sxs-lookup"><span data-stu-id="a1136-129">Remarks</span></span>

<span data-ttu-id="a1136-130">クライアント アプリケーションでは、[詳細] ダイアログ ボックスのボタンを定義するのには**LPFNBUTTON**プロトタイプに基づいてコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1136-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="a1136-131">クライアントは、 [IAddrBook::Details](iaddrbook-details.md)メソッドの呼び出しでコールバック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="a1136-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="a1136-132">サービス プロバイダーでは、[詳細] ダイアログ ボックスのボタンを定義するのには**LPFNBUTTON**のプロトタイプのフック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1136-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="a1136-133">プロバイダーは、 [IMAPISupport::Details](imapisupport-details.md)メソッドの呼び出しでは、このフック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="a1136-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="a1136-134">どちらの場合も、ダイアログ ボックスが表示され、定義済みのボタンを選択した場合、MAPI は**LPFNBUTTON**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1136-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1136-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1136-135">See also</span></span>



[<span data-ttu-id="a1136-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="a1136-136">BuildDisplayTable</span></span>](builddisplaytable.md)

