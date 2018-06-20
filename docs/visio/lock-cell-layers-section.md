---
title: '[Lock] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805735"
---
# <a name="lock-cell-layers-section"></a><span data-ttu-id="5cac4-103">[Lock] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="5cac4-103">Lock Cell (Layers Section)</span></span>

<span data-ttu-id="5cac4-104">レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5cac4-104">Specifies whether shapes belonging to the layer are locked against being selected or edited.</span></span>
  
|<span data-ttu-id="5cac4-105">**値**</span><span class="sxs-lookup"><span data-stu-id="5cac4-105">**Value**</span></span>|<span data-ttu-id="5cac4-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="5cac4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cac4-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5cac4-107">TRUE</span></span>  <br/> |<span data-ttu-id="5cac4-108">図形をロックします。</span><span class="sxs-lookup"><span data-stu-id="5cac4-108">Shapes are locked.</span></span>  <br/> |
|<span data-ttu-id="5cac4-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5cac4-109">FALSE</span></span>  <br/> |<span data-ttu-id="5cac4-110">図形をロックしません。</span><span class="sxs-lookup"><span data-stu-id="5cac4-110">Shapes are not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cac4-111">注釈</span><span class="sxs-lookup"><span data-stu-id="5cac4-111">Remarks</span></span>

<span data-ttu-id="5cac4-112">**[レイヤー プロパティ**] ダイアログ ボックスで、**ロック**を選択することによって、この値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="5cac4-112">You can also set this value by selecting **Lock** in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="5cac4-113">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Lock] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cac4-113">To get a reference to the Lock cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5cac4-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="5cac4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="5cac4-115">Layers.Locked [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="5cac4-115">Layers.Locked[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5cac4-116">プログラムから、インデックスによって [Lock] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5cac4-116">To get a reference to the Lock cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5cac4-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cac4-117">Section index:</span></span>  <br/> |<span data-ttu-id="5cac4-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="5cac4-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="5cac4-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cac4-119">Row index:</span></span>  <br/> |<span data-ttu-id="5cac4-120">**visRowLayer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="5cac4-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="5cac4-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5cac4-121">Cell index:</span></span>  <br/> |<span data-ttu-id="5cac4-122">**visLayerLock**</span><span class="sxs-lookup"><span data-stu-id="5cac4-122">**visLayerLock**</span></span> <br/> |
   

