---
title: '[BeginGroup] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: このアクションのメニューに区切り記号を挿入するかどうかを示します。
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804802"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="97ffc-103">[BeginGroup] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="97ffc-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="97ffc-104">このアクションのメニューに区切り記号を挿入するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="97ffc-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="97ffc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="97ffc-105">**Value**</span></span>|<span data-ttu-id="97ffc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="97ffc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="97ffc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="97ffc-107">TRUE</span></span>  <br/> |<span data-ttu-id="97ffc-108">区切り記号は、このアクションのメニューに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="97ffc-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="97ffc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="97ffc-109">FALSE</span></span>  <br/> |<span data-ttu-id="97ffc-110">このアクション (デフォルト) のメニューには、区切り文字は挿入されません。</span><span class="sxs-lookup"><span data-stu-id="97ffc-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97ffc-111">備考</span><span class="sxs-lookup"><span data-stu-id="97ffc-111">Remarks</span></span>

<span data-ttu-id="97ffc-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって BeginGroup] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="97ffc-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97ffc-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="97ffc-113">Cell name:</span></span>  <br/> |<span data-ttu-id="97ffc-114">アクションです。</span><span class="sxs-lookup"><span data-stu-id="97ffc-114">Actions.</span></span> <span data-ttu-id="97ffc-115">*名*です。BeginGroup で動作します。</span><span class="sxs-lookup"><span data-stu-id="97ffc-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="97ffc-116">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="97ffc-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="97ffc-117">プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="97ffc-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97ffc-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="97ffc-118">Section index:</span></span>  <br/> |<span data-ttu-id="97ffc-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="97ffc-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="97ffc-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="97ffc-120">Row index:</span></span>  <br/> |<span data-ttu-id="97ffc-121">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="97ffc-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="97ffc-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="97ffc-122">Cell index:</span></span>  <br/> |<span data-ttu-id="97ffc-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="97ffc-123">**visActionBeginGroup**</span></span> <br/> |
   

