---
title: '[Menu] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: 図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805926"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="1bb7a-103">[Menu] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="1bb7a-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="1bb7a-104">図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1bb7a-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1bb7a-106">注釈</span><span class="sxs-lookup"><span data-stu-id="1bb7a-106">Remarks</span></span>

<span data-ttu-id="1bb7a-p101">メニューのこの項目の上に区切り記号を挿入するには、[BeginGroup] セルを使用します。メニューの下部にコマンドを表示するには、名前の前にパーセント文字 (%) を付けます。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="1bb7a-109">取得する [menu] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bb7a-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="1bb7a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="1bb7a-111">アクションです。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-111">Actions.</span></span> <span data-ttu-id="1bb7a-112">*名*です。Menuwhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="1bb7a-113">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="1bb7a-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="1bb7a-114">プログラムから、インデックスによって [menu] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bb7a-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bb7a-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bb7a-115">Section index:</span></span>  <br/> |<span data-ttu-id="1bb7a-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="1bb7a-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="1bb7a-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bb7a-117">Row index:</span></span>  <br/> |<span data-ttu-id="1bb7a-118">**visRowAction** +  *i* i = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="1bb7a-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="1bb7a-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1bb7a-119">Cell index:</span></span>  <br/> |<span data-ttu-id="1bb7a-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="1bb7a-120">**visActionMenu**</span></span> <br/> |
   

