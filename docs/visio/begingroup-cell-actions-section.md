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
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407838"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="06767-103">[BeginGroup] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="06767-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="06767-104">このアクションのメニューに区切り記号を挿入するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="06767-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="06767-105">**値**</span><span class="sxs-lookup"><span data-stu-id="06767-105">**Value**</span></span>|<span data-ttu-id="06767-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="06767-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06767-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="06767-107">TRUE</span></span>  <br/> |<span data-ttu-id="06767-108">このアクションのメニューに区切り記号を挿入します。</span><span class="sxs-lookup"><span data-stu-id="06767-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="06767-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="06767-109">FALSE</span></span>  <br/> |<span data-ttu-id="06767-110">このアクションのメニューに区切り記号を挿入しません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="06767-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="06767-111">注釈</span><span class="sxs-lookup"><span data-stu-id="06767-111">Remarks</span></span>

<span data-ttu-id="06767-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginGroup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="06767-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06767-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="06767-113">Cell name:</span></span>  <br/> |<span data-ttu-id="06767-114">アクション.</span><span class="sxs-lookup"><span data-stu-id="06767-114">Actions.</span></span> <span data-ttu-id="06767-115">*名前*です。アクションを実行する begingroup。</span><span class="sxs-lookup"><span data-stu-id="06767-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="06767-116">*name* には [Actions] 行の名前を指定</span><span class="sxs-lookup"><span data-stu-id="06767-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="06767-117">プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="06767-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06767-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="06767-118">Section index:</span></span>  <br/> |<span data-ttu-id="06767-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="06767-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="06767-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="06767-120">Row index:</span></span>  <br/> |<span data-ttu-id="06767-121">**visRowAction** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="06767-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="06767-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="06767-122">Cell index:</span></span>  <br/> |<span data-ttu-id="06767-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="06767-123">**visActionBeginGroup**</span></span> <br/> |
   

