---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566517"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="0bc40-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0bc40-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="0bc40-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bc40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bc40-105">ボタン コントロールを無効にでき、クライアント アプリケーションのユーザーが有効なコントロールをクリックしたときにタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0bc40-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="0bc40-106">サービス プロバイダーは、設定プロパティ シートの表示のテーブルを使用して定義されているなどのダイアログ ボックスにカスタム ボタンを作成するコントロール オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="0bc40-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="0bc40-107">表示のテーブルを操作し、オブジェクトを制御する方法の詳細については、[テーブルの表示](display-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0bc40-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bc40-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0bc40-108">Header file:</span></span>  <br/> |<span data-ttu-id="0bc40-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bc40-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0bc40-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="0bc40-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="0bc40-111">コントロール オブジェクト</span><span class="sxs-lookup"><span data-stu-id="0bc40-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="0bc40-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0bc40-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="0bc40-113">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0bc40-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="0bc40-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0bc40-114">Called by:</span></span>  <br/> |<span data-ttu-id="0bc40-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="0bc40-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="0bc40-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="0bc40-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0bc40-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="0bc40-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="0bc40-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="0bc40-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="0bc40-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="0bc40-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0bc40-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="0bc40-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0bc40-121">発生しました</span><span class="sxs-lookup"><span data-stu-id="0bc40-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="0bc40-122">前のボタン コントロールのエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="0bc40-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="0bc40-123">Activate</span><span class="sxs-lookup"><span data-stu-id="0bc40-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="0bc40-124">ダイアログ ボックスを表示する、クライアント アプリケーションのユーザーは、ボタン コントロールをクリックすると、プログラムの操作を開始するなどのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="0bc40-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="0bc40-125">GetState</span><span class="sxs-lookup"><span data-stu-id="0bc40-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="0bc40-126">ボタン コントロールを有効または無効にするかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0bc40-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bc40-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bc40-127">See also</span></span>



[<span data-ttu-id="0bc40-128">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="0bc40-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

