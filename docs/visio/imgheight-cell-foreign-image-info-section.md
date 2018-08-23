---
title: '[ImgHeight] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 983bb919dbfada65b6d9af464ecfa17c04e970c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805574"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="eff66-104">[ImgHeight] セル ([外部画像情報] セクション)</span><span class="sxs-lookup"><span data-stu-id="eff66-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="eff66-p102">枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="eff66-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="eff66-107">= 高さ\*1</span><span class="sxs-lookup"><span data-stu-id="eff66-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eff66-108">注釈</span><span class="sxs-lookup"><span data-stu-id="eff66-108">Remarks</span></span>

<span data-ttu-id="eff66-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgHeight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="eff66-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eff66-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="eff66-110">Cell name:</span></span>  <br/> | <span data-ttu-id="eff66-111">[Imgheight]</span><span class="sxs-lookup"><span data-stu-id="eff66-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="eff66-112">プログラムから、インデックスによって [ImgHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eff66-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eff66-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff66-113">Section index:</span></span>  <br/> |<span data-ttu-id="eff66-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="eff66-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="eff66-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff66-115">Row index:</span></span>  <br/> |<span data-ttu-id="eff66-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="eff66-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="eff66-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="eff66-117">Cell index:</span></span>  <br/> |<span data-ttu-id="eff66-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="eff66-118">**visFrgnImgHeight**</span></span> <br/> |
   

