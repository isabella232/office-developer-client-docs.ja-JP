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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431513"
---
# <a name="lpfnbutton"></a><span data-ttu-id="4ffb2-103">LPFNBUTTON</span><span class="sxs-lookup"><span data-stu-id="4ffb2-103">LPFNBUTTON</span></span>

  
  
<span data-ttu-id="4ffb2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ffb2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ffb2-105">アドレス帳ダイアログ ボックスでオプションのボタン コントロールをアクティブ化するために MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-105">Defines a callback function that MAPI calls to activate an optional button control in an address book dialog box.</span></span> <span data-ttu-id="4ffb2-106">通常、このボタンは [詳細] **ボタン** です。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-106">This button is typically a **Details** button.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ffb2-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4ffb2-107">Header file:</span></span>  <br/> |<span data-ttu-id="4ffb2-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4ffb2-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="4ffb2-109">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4ffb2-110">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4ffb2-110">Service providers</span></span>  <br/> |
|<span data-ttu-id="4ffb2-111">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="4ffb2-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4ffb2-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ffb2-112">MAPI</span></span>  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4ffb2-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4ffb2-113">Parameters</span></span>

 <span data-ttu-id="4ffb2-114">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="4ffb2-114">_ulUIParam_</span></span>
  
> <span data-ttu-id="4ffb2-115">[in]この関数が表示するダイアログ ボックスまたはウィンドウの親ウィンドウのハンドル。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-115">[in] Handle of the parent windows for any dialog boxes or windows this function displays.</span></span>
    
 <span data-ttu-id="4ffb2-116">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="4ffb2-116">_lpvContext_</span></span>
  
> <span data-ttu-id="4ffb2-117">[in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-117">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="4ffb2-118">この値は、クライアント アプリケーションにとって重要なアドレスを表します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-118">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="4ffb2-119">通常、C++ コードの場合  _、lpvContext_ は C++ オブジェクトへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-119">Typically, for C++ code,  _lpvContext_ represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="4ffb2-120">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="4ffb2-120">_cbEntryID_</span></span>
  
> <span data-ttu-id="4ffb2-121">[in]  _lpSelection_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-121">[in] Size, in bytes, of the entry identifier pointed to by the  _lpSelection_ parameter.</span></span> 
    
 <span data-ttu-id="4ffb2-122">_lpSelection_</span><span class="sxs-lookup"><span data-stu-id="4ffb2-122">_lpSelection_</span></span>
  
> <span data-ttu-id="4ffb2-123">[in]ダイアログ ボックスで選択範囲を定義するエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-123">[in] Pointer to the entry identifier defining the selection in the dialog box.</span></span>
    
 <span data-ttu-id="4ffb2-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4ffb2-124">_ulFlags_</span></span>
  
> <span data-ttu-id="4ffb2-125">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="4ffb2-125">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4ffb2-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="4ffb2-126">Return value</span></span>

<span data-ttu-id="4ffb2-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ffb2-127">S_OK</span></span> 
  
> <span data-ttu-id="4ffb2-128">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="4ffb2-128">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ffb2-129">注釈</span><span class="sxs-lookup"><span data-stu-id="4ffb2-129">Remarks</span></span>

<span data-ttu-id="4ffb2-130">クライアント アプリケーションは、詳細ダイアログ ボックスでボタンを定義するために **、LPFNBUTTON** プロトタイプに基づいてコールバック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-130">Client applications call a callback function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="4ffb2-131">クライアントは [、IAddrBook::D etails](iaddrbook-details.md) メソッドの呼び出しでコールバック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-131">The client passes a pointer to the callback function in calls to the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="4ffb2-132">サービス プロバイダーは、詳細ダイアログ ボックスでボタンを定義するために **、LPFNBUTTON** プロトタイプに基づいてフック関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-132">Service providers call a hook function based on the **LPFNBUTTON** prototype to define a button in a details dialog box.</span></span> <span data-ttu-id="4ffb2-133">プロバイダーは [、IMAPISupport::D etails](imapisupport-details.md) メソッドの呼び出しで、このフック関数へのポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-133">The provider passes a pointer to this hook function in calls to the [IMAPISupport::Details](imapisupport-details.md) method.</span></span> 
  
<span data-ttu-id="4ffb2-134">どちらの場合も、ダイアログ ボックスが表示され、ユーザーが定義されたボタンを選択すると、MAPI は **LPFNBUTTON を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="4ffb2-134">In both cases, when the dialog box is displayed and the user chooses the defined button, MAPI calls **LPFNBUTTON**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ffb2-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="4ffb2-135">See also</span></span>



[<span data-ttu-id="4ffb2-136">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="4ffb2-136">BuildDisplayTable</span></span>](builddisplaytable.md)

