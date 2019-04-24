---
title: テーブルコントロールの表示
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337031"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="99205-103">テーブルコントロールの表示</span><span class="sxs-lookup"><span data-stu-id="99205-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="99205-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99205-105">さまざまな種類のコントロールがあります。 MAPI に固有のものではありません。</span><span class="sxs-lookup"><span data-stu-id="99205-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="99205-106">しかし、MAPI は独自の構造を定義しています。これらは、各コントロールに関連する一意のデータセットを[builddisplaytable](builddisplaytable.md)と組み合わせて記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="99205-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="99205-107">次の表に、各種類のコントロールを説明する構造を示します。</span><span class="sxs-lookup"><span data-stu-id="99205-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="99205-108">**制御構造**</span><span class="sxs-lookup"><span data-stu-id="99205-108">**Control structure**</span></span>|<span data-ttu-id="99205-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="99205-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99205-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="99205-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="99205-111">ボタンコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99205-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="99205-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="99205-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="99205-113">チェックボックスコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99205-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="99205-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="99205-115">コンボボックスコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="99205-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="99205-117">ドロップダウンリストボックスコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99205-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="99205-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="99205-119">編集コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="99205-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="99205-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="99205-121">グループボックスコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="99205-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="99205-123">label コントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="99205-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="99205-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="99205-125">リストボックスコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="99205-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="99205-127">複数値ドロップダウンリストボックスコントロールを表します。</span><span class="sxs-lookup"><span data-stu-id="99205-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="99205-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="99205-129">複数値リストボックスコントロールを記述します。</span><span class="sxs-lookup"><span data-stu-id="99205-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="99205-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="99205-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="99205-131">タブページコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99205-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="99205-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="99205-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="99205-133">オプションボタンコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99205-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99205-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="99205-134">See also</span></span>



[<span data-ttu-id="99205-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="99205-135">Display Table Implementation</span></span>](display-table-implementation.md)

