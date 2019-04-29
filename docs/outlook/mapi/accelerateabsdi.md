---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420375"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="a7c0e-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="a7c0e-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="a7c0e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7c0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7c0e-105">[モードレスアドレス帳] ダイアログボックスで、アクセラレータキーを処理するためのコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a7c0e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a7c0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="a7c0e-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7c0e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a7c0e-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="a7c0e-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a7c0e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a7c0e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a7c0e-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="a7c0e-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a7c0e-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a7c0e-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="a7c0e-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a7c0e-112">Parameters</span></span>

 <span data-ttu-id="a7c0e-113">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="a7c0e-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="a7c0e-114">順番ユーザーインターフェイス情報を関数に渡すために使用される実装固有の値。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="a7c0e-115">Microsoft Windows 上で実行されているアプリケーションでは、 _uluiparam_はダイアログボックスの親ウィンドウハンドルで、 **ULONG_PTR**にキャストする型 HWND です。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="a7c0e-116">値が0の場合は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="a7c0e-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="a7c0e-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="a7c0e-118">順番Windows メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7c0e-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="a7c0e-119">Return value</span></span>

<span data-ttu-id="a7c0e-120">**ACCELERATEABSDI**プロトタイプを使用している関数は、メッセージを処理する場合は TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a7c0e-121">注釈</span><span class="sxs-lookup"><span data-stu-id="a7c0e-121">Remarks</span></span>

<span data-ttu-id="a7c0e-122">**ACCELERATEABSDI**プロトタイプに基づく関数は、モードレスダイアログでのみ使用されます。つまり、クライアントアプリケーションが[ADRPARM](adrparm.md)構造の_ulflags_メンバーで DIALOG_SDI フラグを設定している場合に限られます。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="a7c0e-123">モードレスダイアログは、独自のループを持たずに、クライアントアプリケーションの Windows メッセージループを共有します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="a7c0e-124">メッセージループを制御するアプリケーションでは、ダイアログで使用されるアクセラレータキーがわからないため、 **ACCELERATEABSDI**ベースの関数を呼び出して、CTRL + P などのアクセラレータキーをテストし、操作することができます。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="a7c0e-125">クライアントのメッセージループは、 [IAddrBook:: address](iaddrbook-address.md)メソッドを使用して、モードレスアドレス帳ダイアログボックスを呼び出したときに**ACCELERATEABSDI**ベースの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="a7c0e-126">この呼び出しは、MAPI が[DISMISSMODELESS](dismissmodeless.md)関数プロトタイプに基づいて関数を呼び出したときに終了します。</span><span class="sxs-lookup"><span data-stu-id="a7c0e-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

