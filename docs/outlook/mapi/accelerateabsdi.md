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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799624"
---
# <a name="accelerateabsdi"></a><span data-ttu-id="2cddb-103">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="2cddb-103">ACCELERATEABSDI</span></span>
 
<span data-ttu-id="2cddb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2cddb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2cddb-105">モードレスのアドレス帳のダイアログ ボックスのアクセラレータ キーを処理するコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-105">Defines a callback function to process accelerator keys in a modeless address book dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2cddb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2cddb-106">Header file:</span></span>  <br/> |<span data-ttu-id="2cddb-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cddb-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2cddb-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="2cddb-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2cddb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2cddb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2cddb-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2cddb-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2cddb-111">Client applications</span></span>  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a><span data-ttu-id="2cddb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="2cddb-112">Parameters</span></span>

 <span data-ttu-id="2cddb-113">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2cddb-113">_ulUIParam_</span></span>
  
> <span data-ttu-id="2cddb-114">[in]ユーザー インターフェイスの情報を関数に渡すために使用される実装固有の値です。</span><span class="sxs-lookup"><span data-stu-id="2cddb-114">[in] An implementation-specific value used for passing user interface information to a function.</span></span> <span data-ttu-id="2cddb-115">Microsoft Windows で実行中のアプリケーションで_ulUIParam_ ] ダイアログ ボックスの親ウィンドウ ハンドルは、され型の HWND の**ULONG_PTR**にキャストします。</span><span class="sxs-lookup"><span data-stu-id="2cddb-115">In applications running on Microsoft Windows,  _ulUIParam_ is the parent window handle for a dialog box and is of type HWND, cast to a **ULONG_PTR**.</span></span> <span data-ttu-id="2cddb-116">0 の値は、親ウィンドウがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-116">A value of zero indicates there is no parent window.</span></span> 
    
 <span data-ttu-id="2cddb-117">_lpvmsg_</span><span class="sxs-lookup"><span data-stu-id="2cddb-117">_lpvmsg_</span></span>
  
> <span data-ttu-id="2cddb-118">[in]Windows メッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="2cddb-118">[in] Pointer to a Windows message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2cddb-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="2cddb-119">Return value</span></span>

<span data-ttu-id="2cddb-120">**ACCELERATEABSDI**のプロトタイプを持つ関数は、メッセージを処理する場合に TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-120">A function with the **ACCELERATEABSDI** prototype returns TRUE if it handles the message.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2cddb-121">備考</span><span class="sxs-lookup"><span data-stu-id="2cddb-121">Remarks</span></span>

<span data-ttu-id="2cddb-122">**ACCELERATEABSDI**のプロトタイプでは関数は、クライアント アプリケーションが、 _ulFlags_ 、 [ADRPARM](adrparm.md)構造体のメンバーで、DIALOG_SDI フラグを設定する場合にのみは、モードレス ダイアログ ボックスでのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-122">A function based on the **ACCELERATEABSDI** prototype is used only with a modeless dialog, that is, only if the client application has set the DIALOG_SDI flag in the  _ulFlags_ member of the [ADRPARM](adrparm.md) structure.</span></span> 
  
<span data-ttu-id="2cddb-123">モードレス ダイアログ ボックスでは、独自のループではなく、クライアント アプリケーションの Windows メッセージ ループを共有します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-123">A modeless dialog shares the client application's Windows message loop, instead of having its own loop.</span></span> <span data-ttu-id="2cddb-124">アプリケーション メッセージ ループを制御するには、CTRL キーを押しながら P キーを押すなど印刷用のアクセラレータ キー、 **ACCELERATEABSDI**を呼び出すため、ダイアログの使用に基づいて関数をテストし、動作にどのようなアクセラレータ キーを認識しません。</span><span class="sxs-lookup"><span data-stu-id="2cddb-124">The application, which controls the message loop, does not know what accelerator keys the dialog uses, so it calls an **ACCELERATEABSDI** based function to test for and act upon accelerator keys such as CTRL+P for printing.</span></span> 
  
<span data-ttu-id="2cddb-125">クライアントのメッセージ ループの呼び出し**ACCELERATEABSDI**は、クライアントが[IAddrBook::Address](iaddrbook-address.md)メソッドを使用して、モードレスのアドレス帳] ダイアログ ボックスを呼び出したときに関数を基づいています。</span><span class="sxs-lookup"><span data-stu-id="2cddb-125">A client's message loop calls the **ACCELERATEABSDI** based function when the client invokes a modeless address book dialog box with the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> <span data-ttu-id="2cddb-126">MAPI は、 [DISMISSMODELESS](dismissmodeless.md)関数のプロトタイプでは関数を呼び出すと、この呼び出しが終了します。</span><span class="sxs-lookup"><span data-stu-id="2cddb-126">This call is terminated when MAPI calls a function based on the [DISMISSMODELESS](dismissmodeless.md) function prototype.</span></span> 
  

