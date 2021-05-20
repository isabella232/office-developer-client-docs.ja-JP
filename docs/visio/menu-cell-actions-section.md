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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436329"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="4db22-103">[Menu] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="4db22-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="4db22-104">図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="4db22-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4db22-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="4db22-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4db22-106">注釈</span><span class="sxs-lookup"><span data-stu-id="4db22-106">Remarks</span></span>

<span data-ttu-id="4db22-p101">メニューのこの項目の上に区切り記号を挿入するには、[BeginGroup] セルを使用します。メニューの下部にコマンドを表示するには、名前の前にパーセント文字 (%) を付けます。</span><span class="sxs-lookup"><span data-stu-id="4db22-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="4db22-109">別の数式または CellsU プロパティを使用してプログラムから、名前によって **[メニュー** ] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4db22-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4db22-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="4db22-110">Cell name:</span></span>  <br/> |<span data-ttu-id="4db22-111">アクション。</span><span class="sxs-lookup"><span data-stu-id="4db22-111">Actions.</span></span> <span data-ttu-id="4db22-112">*name*  .Menuwhere Actions。</span><span class="sxs-lookup"><span data-stu-id="4db22-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="4db22-113">*name*  は [アクション] 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="4db22-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="4db22-114">プログラムから、インデックスによって [Menu] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4db22-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4db22-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4db22-115">Section index:</span></span>  <br/> |<span data-ttu-id="4db22-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="4db22-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="4db22-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4db22-117">Row index:</span></span>  <br/> |<span data-ttu-id="4db22-118">**visRowAction**  +  *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="4db22-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="4db22-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4db22-119">Cell index:</span></span>  <br/> |<span data-ttu-id="4db22-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="4db22-120">**visActionMenu**</span></span> <br/> |
   

