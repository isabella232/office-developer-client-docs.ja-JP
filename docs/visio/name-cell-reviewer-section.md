---
title: '[Name] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: 図面校閲者の名前が含まれます。
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805917"
---
# <a name="name-cell-reviewer-section"></a><span data-ttu-id="039d2-103">[Name] セル ([Reviewer] セクション)</span><span class="sxs-lookup"><span data-stu-id="039d2-103">Name Cell (Reviewer Section)</span></span>

<span data-ttu-id="039d2-104">図面校閲者の名前が含まれます。</span><span class="sxs-lookup"><span data-stu-id="039d2-104">Contains the name of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="039d2-105">注釈</span><span class="sxs-lookup"><span data-stu-id="039d2-105">Remarks</span></span>

 <span data-ttu-id="039d2-106">デフォルト値は**Visio のオプション**] ダイアログ ボックスの [**全般**] タブに、[**ユーザー名**] ボックスに名前 (、[**ファイル**] タブをクリックして、**オプション**] をクリックし、し、[**全般**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="039d2-106">This value defaults to the name found in the **User name** box on the **General** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General**).</span></span> 
  
<span data-ttu-id="039d2-107">取得する Name] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="039d2-107">To get a reference to the Name cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="039d2-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="039d2-108">Cell name:</span></span>  <br/> | <span data-ttu-id="039d2-109">Reviewer.Name [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="039d2-109">Reviewer.Name [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="039d2-110">プログラムから、インデックスによって [Name] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="039d2-110">To get a reference to the Name cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="039d2-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="039d2-111">Section index:</span></span>  <br/> |<span data-ttu-id="039d2-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="039d2-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="039d2-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="039d2-113">Row index:</span></span>  <br/> |<span data-ttu-id="039d2-114">**visRowReviewer** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="039d2-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="039d2-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="039d2-115">Cell index:</span></span>  <br/> |<span data-ttu-id="039d2-116">**visReviewerName**</span><span class="sxs-lookup"><span data-stu-id="039d2-116">**visReviewerName**</span></span> <br/> |
   

