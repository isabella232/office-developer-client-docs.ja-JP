---
title: テーブルのコントロールを表示します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799948"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="6b24d-103">テーブルのコントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="6b24d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b24d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b24d-105">さまざまな種類のコントロールは、MAPI に固有の [なし] があります。</span><span class="sxs-lookup"><span data-stu-id="6b24d-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="6b24d-106">ただし、MAPI では、各制御に関連するデータの一意のセットを記述するのには[BuildDisplayTable](builddisplaytable.md)と組み合わせて使用する独自の構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="6b24d-107">コントロールの種類を記述する構造体を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="6b24d-108">**制御構造**</span><span class="sxs-lookup"><span data-stu-id="6b24d-108">**Control structure**</span></span>|<span data-ttu-id="6b24d-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="6b24d-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b24d-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="6b24d-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="6b24d-111">Button コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="6b24d-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="6b24d-113">チェック ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="6b24d-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="6b24d-115">コンボ ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="6b24d-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="6b24d-117">ドロップダウン リスト ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="6b24d-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="6b24d-119">エディット コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="6b24d-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="6b24d-121">グループ ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="6b24d-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="6b24d-123">Label コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="6b24d-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="6b24d-125">リスト ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="6b24d-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="6b24d-127">複数値ドロップダウン リスト ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="6b24d-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="6b24d-129">複数値リスト ボックス コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="6b24d-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="6b24d-131">タブ付きページのコントロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="6b24d-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="6b24d-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="6b24d-133">オプション ボタン コントロールをについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b24d-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b24d-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b24d-134">See also</span></span>



[<span data-ttu-id="6b24d-135">表示テーブルの実装</span><span class="sxs-lookup"><span data-stu-id="6b24d-135">Display Table Implementation</span></span>](display-table-implementation.md)

