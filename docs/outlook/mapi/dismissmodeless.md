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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428187"
---
# <a name="dismissmodeless"></a><span data-ttu-id="623fc-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="623fc-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="623fc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="623fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="623fc-105">モードレス アドレス帳ダイアログ ボックスを閉じ、MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="623fc-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="623fc-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="623fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="623fc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="623fc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="623fc-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="623fc-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="623fc-109">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="623fc-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="623fc-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="623fc-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="623fc-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="623fc-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="623fc-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="623fc-112">Parameters</span></span>

 <span data-ttu-id="623fc-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="623fc-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="623fc-114">[in]実装固有の値は、通常、ユーザー インターフェイス情報を関数に渡す場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="623fc-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="623fc-115">たとえば、Microsoft Windowsでは、このパラメーターはダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型で、ダイアログ ボックスにキャスト **ULONG_PTR。**</span><span class="sxs-lookup"><span data-stu-id="623fc-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="623fc-116">値が 0 の場合は、親ウィンドウが表示されません。</span><span class="sxs-lookup"><span data-stu-id="623fc-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="623fc-117">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="623fc-117">_lpvContext_</span></span>
  
> <span data-ttu-id="623fc-118">[in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="623fc-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="623fc-119">この値は、クライアント アプリケーションにとって重要なアドレスを表します。</span><span class="sxs-lookup"><span data-stu-id="623fc-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="623fc-120">通常、C++ コードの  _場合、lpvContext_ は C++ オブジェクト インスタンスのアドレスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="623fc-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="623fc-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="623fc-121">Return value</span></span>

<span data-ttu-id="623fc-122">なし</span><span class="sxs-lookup"><span data-stu-id="623fc-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="623fc-123">注釈</span><span class="sxs-lookup"><span data-stu-id="623fc-123">Remarks</span></span>

<span data-ttu-id="623fc-124">クライアント アプリケーションがモードレス アドレス帳ダイアログ ボックスを呼び出すと、アクセラレータ キーをチェックして処理する[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに基づく関数の呼び出しが Windows メッセージ ループに含まれます。</span><span class="sxs-lookup"><span data-stu-id="623fc-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="623fc-125">ダイアログ ボックスが閉じられると、MAPI は **DISMISSMODELESS** ベースの関数を呼び出して、クライアント アプリケーションが **ACCELERATEABSDI** ベースの関数の呼び出しを停止します。</span><span class="sxs-lookup"><span data-stu-id="623fc-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="623fc-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="623fc-126">See also</span></span>



[<span data-ttu-id="623fc-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="623fc-127">ADRPARM</span></span>](adrparm.md)

