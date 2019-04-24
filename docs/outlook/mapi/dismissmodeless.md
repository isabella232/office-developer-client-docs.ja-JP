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
ms.openlocfilehash: dd962515a85cb6a4b8661a0fd5294cea55cd6e96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339775"
---
# <a name="dismissmodeless"></a><span data-ttu-id="47036-103">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="47036-103">DISMISSMODELESS</span></span>

  
  
<span data-ttu-id="47036-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47036-105">モードレスアドレス帳ダイアログボックスが閉じられたときに MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="47036-105">Defines a callback function that MAPI calls when it has dismissed a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47036-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="47036-106">Header file:</span></span>  <br/> |<span data-ttu-id="47036-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="47036-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="47036-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="47036-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="47036-109">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="47036-109">Client applications</span></span>  <br/> |
|<span data-ttu-id="47036-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="47036-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="47036-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="47036-111">MAPI</span></span>  <br/> |
   
```cpp
void (STDMETHODCALLTYPE DISMISSMODELESS)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext
);
```

## <a name="parameters"></a><span data-ttu-id="47036-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="47036-112">Parameters</span></span>

 <span data-ttu-id="47036-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="47036-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="47036-114">順番通常、ユーザーインターフェイス情報を関数に渡すために使用される実装固有の値。</span><span class="sxs-lookup"><span data-stu-id="47036-114">[in] An implementation-specific value typically used for passing user interface information to a function.</span></span> <span data-ttu-id="47036-115">たとえば、Microsoft Windows では、このパラメーターはダイアログボックスの親ウィンドウハンドルで、型は HWND で、 **ULONG_PTR**にキャストされます。</span><span class="sxs-lookup"><span data-stu-id="47036-115">For example, in Microsoft Windows this parameter is the parent window handle for the dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="47036-116">値が0の場合は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="47036-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="47036-117">_lpvcontext_</span><span class="sxs-lookup"><span data-stu-id="47036-117">_lpvContext_</span></span>
  
> <span data-ttu-id="47036-118">順番MAPI がコールバック関数に渡す任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="47036-118">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="47036-119">この値は、クライアントアプリケーションにとって重要なアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="47036-119">This value can represent an address of significance to the client application.</span></span> <span data-ttu-id="47036-120">通常、c++ コードでは、 _lpvcontext_は c++ オブジェクトインスタンスのアドレスへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="47036-120">Typically, for C++ code,  _lpvContext_ is a pointer to the address of a C++ object instance.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="47036-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="47036-121">Return value</span></span>

<span data-ttu-id="47036-122">なし</span><span class="sxs-lookup"><span data-stu-id="47036-122">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47036-123">解説</span><span class="sxs-lookup"><span data-stu-id="47036-123">Remarks</span></span>

<span data-ttu-id="47036-124">クライアントアプリケーションは、モードレスアドレス帳ダイアログボックスを起動するときに、 [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに基づいて関数への呼び出しを Windows メッセージループに含めます。このメソッドは、アクセラレータキーをチェックして処理します。</span><span class="sxs-lookup"><span data-stu-id="47036-124">When the client application invokes a modeless address book dialog box, it includes in its Windows message loop a call to a function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype, which checks for and processes accelerator keys.</span></span> <span data-ttu-id="47036-125">ダイアログボックスが閉じられると、MAPI は**DISMISSMODELESS**ベースの関数を呼び出して、クライアントアプリケーションが**ACCELERATEABSDI**ベースの関数の呼び出しを停止するようにします。</span><span class="sxs-lookup"><span data-stu-id="47036-125">When the dialog box is closed, MAPI calls the **DISMISSMODELESS** based function so that the client application will stop calling the **ACCELERATEABSDI** based function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47036-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="47036-126">See also</span></span>



[<span data-ttu-id="47036-127">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="47036-127">ADRPARM</span></span>](adrparm.md)

