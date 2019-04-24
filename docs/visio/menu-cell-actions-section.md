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
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360656"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="a1081-103">[Menu] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="a1081-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="a1081-104">図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1081-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1081-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="a1081-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1081-106">解説</span><span class="sxs-lookup"><span data-stu-id="a1081-106">Remarks</span></span>

<span data-ttu-id="a1081-p101">メニューのこの項目の上に区切り記号を挿入するには、[BeginGroup] セルを使用します。メニューの下部にコマンドを表示するには、名前の前にパーセント文字 (%) を付けます。</span><span class="sxs-lookup"><span data-stu-id="a1081-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="a1081-109">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [Menu] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a1081-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1081-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="a1081-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a1081-111">アクション.</span><span class="sxs-lookup"><span data-stu-id="a1081-111">Actions.</span></span> <span data-ttu-id="a1081-112">*名前*です。操作を実行するメニュー。</span><span class="sxs-lookup"><span data-stu-id="a1081-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="a1081-113">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="a1081-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a1081-114">プログラムから、インデックスによって [Menu] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a1081-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1081-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1081-115">Section index:</span></span>  <br/> |<span data-ttu-id="a1081-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a1081-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a1081-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1081-117">Row index:</span></span>  <br/> |<span data-ttu-id="a1081-118">**visRowAction** +  *i* = 0、1、2、...</span><span class="sxs-lookup"><span data-stu-id="a1081-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="a1081-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a1081-119">Cell index:</span></span>  <br/> |<span data-ttu-id="a1081-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="a1081-120">**visActionMenu**</span></span> <br/> |
   

