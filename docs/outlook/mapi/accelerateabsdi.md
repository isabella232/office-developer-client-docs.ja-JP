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
# <a name="accelerateabsdi"></a><span data-ttu-id="5e745-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="5e745-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="5e745-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e745-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e745-105">モードレス アドレス帳ダイアログ ボックスでアクセラレータ キーを処理するコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5e745-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e745-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5e745-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e745-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e745-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5e745-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="5e745-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="5e745-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5e745-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5e745-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="5e745-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="5e745-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5e745-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="5e745-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5e745-112">Parameters</span></span>

 <span data-ttu-id="5e745-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5e745-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="5e745-114">[in]ユーザー インターフェイス情報を関数に渡す場合に使用される実装固有の値。</span><span class="sxs-lookup"><span data-stu-id="5e745-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="5e745-115">Microsoft Windows で実行されているアプリケーションでは _、ulUIParam_ はダイアログ ボックスの親ウィンドウ ハンドルであり、HWND 型で、ULONG_PTR に **キャストされます**。</span><span class="sxs-lookup"><span data-stu-id="5e745-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="5e745-116">値が 0 の場合は、親ウィンドウが表示されません。</span><span class="sxs-lookup"><span data-stu-id="5e745-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="5e745-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="5e745-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="5e745-118">[in]メッセージへのポインター Windowsします。</span><span class="sxs-lookup"><span data-stu-id="5e745-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e745-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e745-119">Return value</span></span>

<span data-ttu-id="5e745-120">**ACCELERATEABSDI プロトタイプを持つ** 関数は、メッセージを処理する場合は TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="5e745-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e745-121">注釈</span><span class="sxs-lookup"><span data-stu-id="5e745-121">Remarks</span></span>

<span data-ttu-id="5e745-122">**ACCELERATEABSDI** プロトタイプに基づく関数は、モードレス ダイアログでのみ使用されます。つまり、クライアント アプリケーションが [ADRPARM](adrparm.md)構造体の _ulFlags_ メンバーで DIALOG_SDI フラグを設定している場合のみです。</span><span class="sxs-lookup"><span data-stu-id="5e745-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="5e745-123">モードレス ダイアログは、独自のループをWindows、クライアント アプリケーションのメッセージ ループを共有します。</span><span class="sxs-lookup"><span data-stu-id="5e745-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="5e745-124">メッセージ ループを制御するアプリケーションは、ダイアログで使用するアクセラレータ キーを知らないので **、ACCELERATEABSDI** ベースの関数を呼び出して、印刷用の Ctrl + P などのアクセラレータ キーをテストして処理します。</span><span class="sxs-lookup"><span data-stu-id="5e745-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="5e745-125">クライアントのメッセージ ループは、クライアントが [IAddrBook::Address](iaddrbook-address.md)メソッドを使用してモードレス アドレス帳ダイアログ ボックスを呼び出すと **、ACCELERATEABSDI** ベースの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5e745-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="5e745-126">この呼び出しは、MAPI が DISMISSMODELESS 関数プロトタイプに基づいて関数 [を呼び出す場合に](dismissmodeless.md) 終了します。</span><span class="sxs-lookup"><span data-stu-id="5e745-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

