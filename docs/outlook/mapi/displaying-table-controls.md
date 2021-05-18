---
title: テーブル コントロールの表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422692"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="88214-103">テーブル コントロールの表示</span><span class="sxs-lookup"><span data-stu-id="88214-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="88214-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88214-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88214-105">さまざまな種類のコントロールがあります。MAPI に固有のコントロールは存在します。</span><span class="sxs-lookup"><span data-stu-id="88214-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="88214-106">ただし、MAPI は、各コントロールに関連する一意のデータ セットを記述するために [BuildDisplayTable](builddisplaytable.md) と組み合わせて使用される独自の構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="88214-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="88214-107">次の表に、各種類のコントロールについて説明する構造を示します。</span><span class="sxs-lookup"><span data-stu-id="88214-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="88214-108">**制御構造**</span><span class="sxs-lookup"><span data-stu-id="88214-108">**Control structure**</span></span>|<span data-ttu-id="88214-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="88214-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88214-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="88214-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="88214-111">ボタン コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="88214-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="88214-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="88214-113">チェック ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="88214-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="88214-115">コンボ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="88214-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="88214-117">ドロップダウン リスト ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="88214-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="88214-119">編集コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="88214-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="88214-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="88214-121">グループ ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="88214-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="88214-123">ラベル コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="88214-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="88214-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="88214-125">リスト ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="88214-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="88214-127">複数値のドロップダウン リスト ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="88214-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="88214-129">複数値のリスト ボックス コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="88214-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="88214-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="88214-131">タブ付きページ コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="88214-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="88214-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="88214-133">オプション ボタン コントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88214-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88214-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="88214-134">See also</span></span>



[<span data-ttu-id="88214-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="88214-135">Display Table Implementation</span></span>](display-table-implementation.md)

