---
title: DISMISSMODELESS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DISMISSMODELESS
api_type:
- COM
ms.assetid: ef93ef3d-c159-40ae-9b8d-0af8a0567565
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c66ff2338eb5751dbffe392a6a26258fb1c89476
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565838"
---
# <a name="dismissmodeless"></a><span data-ttu-id="6392c-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="6392c-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="6392c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6392c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6392c-105">モードレスのアドレス帳のダイアログ ボックスを閉じるにはときに、MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="6392c-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6392c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6392c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6392c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6392c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="6392c-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="6392c-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6392c-109">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6392c-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="6392c-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="6392c-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6392c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="6392c-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="6392c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6392c-112">Parameters</span></span>

 <span data-ttu-id="6392c-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6392c-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="6392c-114">[in]ユーザー インターフェイスの情報を関数に渡すために使用される通常の実装に固有の値です。</span><span class="sxs-lookup"><span data-stu-id="6392c-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="6392c-115">などの Microsoft Windows でこのパラメーター] ダイアログ ボックスの親ウィンドウ ハンドル、キャスト、 **ULONG_PTR**型 HWND の。</span><span class="sxs-lookup"><span data-stu-id="6392c-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="6392c-116">0 の値は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6392c-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="6392c-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="6392c-117">_lpvContext_</span></span>
  
> <span data-ttu-id="6392c-118">[in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="6392c-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="6392c-119">この値は、クライアント アプリケーションにとって意味のアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="6392c-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="6392c-120">通常、C++ コードでは、 _lpvContext_は、C++ オブジェクトのインスタンスのアドレスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6392c-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6392c-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="6392c-121">Return value</span></span>

<span data-ttu-id="6392c-122">なし</span><span class="sxs-lookup"><span data-stu-id="6392c-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6392c-123">注釈</span><span class="sxs-lookup"><span data-stu-id="6392c-123">Remarks</span></span>

<span data-ttu-id="6392c-124">モードレスのアドレス帳のダイアログ ボックスを呼び出すと、クライアント アプリケーションが含まれます Windows メッセージ ループで[ACCELERATEABSDI](accelerateabsdi.md)のプロトタイプをチェックし、アクセラレータ キーを処理するには関数の呼び出しには。</span><span class="sxs-lookup"><span data-stu-id="6392c-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="6392c-125">ダイアログ ボックスが閉じられると、 **DISMISSMODELESS**ベースの関数**ACCELERATEABSDI**を呼び出すクライアント アプリケーションを停止するため、MAPI 呼び出しは、関数を基づいています。</span><span class="sxs-lookup"><span data-stu-id="6392c-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6392c-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="6392c-126">See also</span></span>



[<span data-ttu-id="6392c-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="6392c-127">ADRPARM</span></span>](adrparm.md)

