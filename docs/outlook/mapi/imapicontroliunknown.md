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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280142"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="c0334-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0334-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="c0334-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0334-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0334-105">ボタンコントロールを有効または無効にし、クライアントアプリケーションのユーザーが有効になっているコントロールをクリックしたときにタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c0334-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="c0334-106">サービスプロバイダーは、コントロールオブジェクトを実装して、表示テーブルを使用して定義される構成プロパティシートなどのカスタムボタンをダイアログボックスに作成します。</span><span class="sxs-lookup"><span data-stu-id="c0334-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="c0334-107">表示テーブルとコントロールオブジェクトを操作する方法の詳細については、「[表を表示](display-tables.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0334-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c0334-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c0334-108">Header file:</span></span>  <br/> |<span data-ttu-id="c0334-109">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c0334-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c0334-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="c0334-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="c0334-111">Control オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c0334-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="c0334-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="c0334-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0334-113">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c0334-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="c0334-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c0334-114">Called by:</span></span>  <br/> |<span data-ttu-id="c0334-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0334-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0334-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="c0334-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c0334-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="c0334-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="c0334-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="c0334-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="c0334-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="c0334-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c0334-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="c0334-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c0334-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c0334-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="c0334-122">前のボタンコントロールのエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="c0334-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="c0334-123">Activate</span><span class="sxs-lookup"><span data-stu-id="c0334-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="c0334-124">クライアントアプリケーションユーザーが [ボタン] コントロールをクリックしたときに、ダイアログボックスを表示したり、プログラムによる操作を開始したりするなどのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c0334-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="c0334-125">GetState</span><span class="sxs-lookup"><span data-stu-id="c0334-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="c0334-126">ボタンコントロールが有効であるか無効であるかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c0334-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0334-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0334-127">See also</span></span>



[<span data-ttu-id="c0334-128">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c0334-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

